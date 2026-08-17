# Lab 17 Benchmark Report

- Implementation: `student`
- Kind: `practice`
- Cases: **11**
- Passed: **11/11**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **1393.5 ms**
- Average token reduction vs full source context: **14.2%**

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| E01 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| E06 | semantic | PASS | 1089.5 | 148 | 67.8% |  |
| E09 | long_term | PASS | 1806.2 | 727 | 0.0% |  |
| E10 | short_term | PASS | 0.3 | 195 | 0.0% |  |
| E02 | long_term | PASS | 1937.3 | 1458 | 0.0% |  |
| E03 | long_term | PASS | 1941.2 | 1478 | 0.0% |  |
| E04 | episodic | PASS | 1211.9 | 615 | 0.0% |  |
| E05 | episodic | PASS | 1427.5 | 636 | 0.0% |  |
| E07 | mixed | PASS | 2528.0 | 485 | 14.2% |  |
| E11 | semantic | PASS | 275.5 | 146 | 74.2% |  |
| E08 | long_term | PASS | 3111.4 | 1435 | 0.0% |  |

## Evidence excerpts

### E01 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### E06 - semantic

`EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. metadata=`

### E09 - long_term

`<USER_SUMMARY> Lan's project is LOTUS-88, with a primary focus on Java and Spring Boot. Python is not used for backend development in this project. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend.`

### E10 - short_term

`<SESSION_SUMMARY> user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. | assistant: Acknowledged review constraint. | user: Filler turn 1 about UI spacing. | assistant: Filler answer 1. | user: Filler turn 2 about naming. | assistant: Filler answer 2. | user: Filler turn 3 about logging. | assistant: Filler answer 3. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. - assistant: Acknowledged review constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler turn 4 about tests. assistant: Filler answer 4. user: Filler turn 5 about docs. assistant: Filler answe`

### E02 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`

### E03 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`

### E04 - episodic

`EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Toi nay minh muon viet cho tron ven cai retry payment ma vua dung so thich stack ca nhan cua minh, vua theo dung policy thanh toan chinh thuc, vua tranh dam lai dung cai su co asyn EPISODE: Minh dang setup lai moi truong dev cho mot buoi ngoi code mot minh cuoi tuan nay, kieu khong co ai chung nhom, chi lam project rieng cua minh cho vui thoi. Truoc khi minh chon temp EPISODE: Tuan nay minh moi bi keo vao cai du an ben cong ty va sep hoi lien tuc ve chuyen chuan hoa backend, ma minh thi hoi mo ho vi truoc gio minh xai nhieu thu khac nhau cho project rien EPISODE: Sang mai minh phai hop review tien do voi men`

### E05 - episodic

`EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Toi nay minh muon viet cho tron ven cai retry payment ma vua dung so thich stack ca nhan cua minh, vua theo dung policy thanh toan chinh thuc, vua tranh dam lai dung cai su co asyn EPISODE: Minh dang setup lai moi truong dev cho mot buoi ngoi code mot minh cuoi tuan nay, kieu khong co ai chung nhom, chi lam project rieng cua minh cho vui thoi. Truoc khi minh chon temp EPISODE: Tuan nay minh moi bi keo vao cai du an ben cong ty va sep hoi lien tuc ve chuyen chuan hoa backend, ma minh thi`

### E07 - mixed

`<LONG_TERM> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await,`

### E11 - semantic

`EPISODE: {"id":"kb-async-http","entity":"Async HTTP Incident Playbook","summary":"When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST.","source":"incident-playbook-2026","updated_at":"2026-08-11T00:00:00Z"} metadata= EPISODE: When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST. metadata=`

### E08 - long_term

`<USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. The user needs to complete a benchmark report named LAB-REPORT-1600 before Friday at 4:00 PM. They are currently focused on resolving connection churn for the ASYNC-FIX-20 issue.  Minh prefers Python and dislikes Java. When explaining code, Minh prefers short examples. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used. Minh's preference for Python remains for personal demos like ORCHID-27.  When discussing async/await, coroutines,`
