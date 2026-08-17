# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **1613.2 ms**
- Average token reduction vs full source context: **6.3%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.2 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.0 | 133 | 0.0% |  |
| G08 | long_term | PASS | 4161.0 | 788 | 0.0% |  |
| G09 | long_term | PASS | 1714.3 | 1477 | 0.0% |  |
| G12 | semantic | PASS | 261.2 | 418 | 8.9% |  |
| G14 | semantic | PASS | 272.4 | 270 | 30.2% |  |
| G15 | semantic | PASS | 362.8 | 270 | 41.2% |  |
| G19 | mixed | PASS | 2342.9 | 581 | 0.0% |  |
| G03 | long_term | PASS | 2910.8 | 1476 | 0.0% |  |
| G04 | long_term | PASS | 2050.7 | 1445 | 0.0% |  |
| G05 | long_term | PASS | 2697.3 | 1471 | 0.0% |  |
| G10 | episodic | PASS | 710.3 | 601 | 0.0% |  |
| G11 | episodic | PASS | 602.2 | 632 | 0.0% |  |
| G13 | semantic | PASS | 915.7 | 416 | 26.4% |  |
| G16 | mixed | PASS | 2562.9 | 581 | 0.0% |  |
| G18 | mixed | PASS | 1211.0 | 500 | 11.5% |  |
| G20 | mixed | PASS | 2869.6 | 831 | 0.0% |  |
| G06 | long_term | PASS | 1829.9 | 1467 | 0.0% |  |
| G07 | long_term | PASS | 1950.6 | 1469 | 0.0% |  |
| G17 | mixed | PASS | 2838.4 | 581 | 8.1% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G08 - long_term

`<USER_SUMMARY> Lan's project is LOTUS-88, with a primary focus on Java and Spring Boot. Python is not used for backend development in this project. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-17 05:28:24     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Evaluation User" }: Minh la Lan, minh dang muon them retry cho phan goi payment trong san pham cua minh va minh muon vi du code hop voi dung stack ma minh dang dung chu dung dua cho minh vi du cua ngon ngu khac. Ban gy y gium minh: dua theo backend ma minh da chon cho san pham cua `

### G09 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`

### G12 - semantic

`EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal `

### G14 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G15 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G19 - mixed

`<LONG_TERM> <USER_SUMMARY> Lan's project is LOTUS-88, with a primary focus on Java and Spring Boot. Python is not used for backend development in this project. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-17 05:29:10     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Evaluation User" }: Lan uu tien stack backend nao cho LOTUS-88?   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi `

### G03 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`

### G04 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`

### G05 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`

### G10 - episodic

`EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Minh dang viet mot cai note tong ket ngan de tuan sau trinh bay cho ca nhom nghe ve cach minh phan biet giua viec ca nhan va viec o cong ty, vi may ban trong nhom hay bi lan lon. D EPISODE: Minh dang setup lai moi truong dev cho mot buoi ngoi code mot minh cuoi tuan nay, kieu khong co ai chung nhom, chi lam project rieng cua minh cho vui thoi. Truoc khi minh chon temp EPISODE: Minh dang ngoi mot minh viet cho xong cai ham retry cho POST payment de toi nay demo, va minh muon no vua dung dung ngon ngu ma minh thich khi lam viec ca nhan, vua bam sat dung po EPISODE: Tuan nay minh phai them chuc nang retry payme`

### G11 - episodic

`EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Minh dang viet mot cai note tong ket ngan de tuan sau trinh bay cho ca nhom nghe ve cach minh phan biet giua viec ca nhan va viec o cong ty, vi may ban trong nhom hay bi lan lon. D EPISODE: Minh dang setup lai moi truong dev cho mot buoi ngoi code mot minh cuoi tuan nay, kieu khong co ai chung nhom, chi lam project rieng cua minh cho vui thoi. Truoc khi minh chon temp EPISODE: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHI EPISODE: Minh dang ngoi mot minh viet cho xong cai ham`

### G13 - semantic

`EPISODE: {"id":"kb-async-http","entity":"Async HTTP Incident Playbook","summary":"When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST.","source":"incident-playbook-2026","updated_at":"2026-08-11T00:00:00Z"} metadata= EPISODE: When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST. metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data witho`

### G16 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await,`

### G18 - mixed

`<EPISODIC> EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Minh dang viet mot cai note tong ket ngan de tuan sau trinh bay cho ca nhom nghe ve cach minh phan biet giua viec ca nhan va viec o cong ty, vi may ban trong nhom hay bi lan lon. D EPISODE: Hay chon huong dan code retry payment phu hop voi preference ca nhan cua Minh. EPISODE: Minh dang setup lai moi truong dev cho mot buoi ngoi code mot minh cuoi tuan nay, kieu khong co ai chung nhom, chi lam project rieng cua minh cho vui thoi. Truoc khi minh chon temp EPISODE: Cap nhat m`

### G20 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await,`

### G06 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`

### G07 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`

### G17 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await,`
