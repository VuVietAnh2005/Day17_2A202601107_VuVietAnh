# Báo cáo Thực Hành Lab 17 - Multi-Memory Agent với Zep

## 1. Phân tích Kiến trúc & Thực hành

- **Tầng memory quan trọng nhất**: **Long-term memory** (chiếm các case E02, E03, E08, E09 và 1 phần E07). Tầng này xử lý sở thích lâu dài, open-loop deadlines, cập nhật conflict/recency và đảm bảo cô lập dữ liệu (user isolation).
- **Trade-off Zep Context Block vs Redis/Qdrant**: Zep Cloud tự động trích xuất entity graph, facts, temporal validity và ráp Context Block tối ưu ngữ cảnh. Đổi lại, Zep phụ thuộc latency/chi phí API; trong khi Redis/Qdrant cho tốc độ truy xuất cực nhanh (<1ms) và tự chủ dữ liệu hoàn toàn.
- **Guardrail chống Memory Poisoning**:
  1. Phân quyền và cô lập namespace theo `user_id`.
  2. Bắt buộc Consent Opt-in và lọc PII (Redact phone/email) trước khi ingest.
  3. Heartbeat chỉ cleanup/de-duplicate, không tự nạp facts không rõ nguồn gốc.

---

## 2. Phân tích Kết quả Benchmark

- **Hit rate**: No-Memory chỉ đạt 18.2% (2/11 từ STM). Khi bật Multi-Memory (`student`), hit rate đạt **100% (11/11 PASS)**.
- **Query tốn token nhất**: Case **E03** (1482 tokens) và **E02** (1461 tokens) do Context Block tổng hợp toàn bộ user summary và fact edges liên quan.
- **Case hỗn hợp (E07)**: Kết hợp **Long-term Memory** (sở thích `Python`) và **Semantic Memory** (quy tắc `Idempotency-Key`). Thiếu 1 trong 2 sẽ FAIL.
- **Token Reduction**: Hệ thống chắt lọc đúng evidence (Semantic giảm 67-74%). Baseline No-memory có reduction cao giả tạo (81.8%) vì không nạp gì, gây mất ngữ cảnh.

---

## 3. Cơ chế Recency (E08) & Compaction (E10)

- **E08 Recency**: Khi Minh đổi BLUEBIRD-42 sang TypeScript/NestJS, Zep gán nhãn `valid_at`/`invalid_at` để ưu tiên fact mới nhất.
- **E10 Compaction**: Sliding window kết hợp Durable Notes giữ lại constraint `REVIEW-DEADLINE-1600` dù message cũ đã trôi khỏi buffer.

---

## 4. Minh chứng (Screenshots)
- `submission/long_term.png`, `submission/episodic.png`, `submission/semantic.png`, `submission/privacy.png`
