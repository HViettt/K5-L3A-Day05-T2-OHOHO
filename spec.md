# Bài nộp LAB5 — T2 Giáo dục · Nhóm OHOHO

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| <Họ tên A> | <Mã HV A> | Kịch bản & rủi ro (§1, §2, §6), nộp repo |
| <Họ tên B> | <Mã HV B> | Khi AI sai & mức tự chủ (§3, §4) |
| <Họ tên C> | <Mã HV C> | Prototype (§5), demo thao tác |

**Lớp:** L3A · **Bàn / zone:** A2 · **Track:** T2 Giáo dục

### §1. Lát cắt & phạm vi

> Cần nêu đúng lát cắt được phát và giới hạn phạm vi; mỗi việc không làm cần có lý do gắn với mục tiêu sản phẩm.

- [ ] Chép lát cắt và nêu phạm vi.
- [ ] Nêu 3 việc không làm, mỗi việc một câu lý do.

- **Lát cắt:** Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.
- **Không làm 1:** Không giải hộ hoặc xác nhận đáp số bài đang mở (bài 3, hạn 13/11/2026 23:59) — học viên chép đáp số thì không còn hiểu bài, trái với mục tiêu "không chép đáp án"; `goi_y_bai_tap` không đảo được khi đã chép.
- **Không làm 2:** Không nhận xét năng lực người học (kể cả khi học viên tự chê mình) — AI không có căn cứ đánh giá năng lực, và nhận xét sai dễ làm học viên mất tự tin, bỏ học.
- **Không làm 3:** Không dạy nội dung buổi chưa học (buổi 4–10, ví dụ p-value ở buổi 7) — trang khoá học chỉ có tên buổi, chưa có tài liệu, AI dễ bịa nội dung; chỉ nói buổi nào sẽ học, tối đa một câu.

### §2. Kịch bản rủi ro

> Cần có ít nhất 8 kịch bản, đủ các lớp ①②③④; chỉ ra tool hoặc dữ liệu cụ thể nơi AI có thể sai, hành động tốt của sản phẩm và mức độ lỗi.

- [ ] Có ít nhất 8 kịch bản, mỗi lớp ①②③④ có ít nhất một kịch bản.
- [ ] Mỗi kịch bản có bằng chứng trỏ về tool/dữ liệu, hành động tốt và nhãn.
- [ ] Chọn 2 kịch bản đắt nhất, giải thích lựa chọn và kịch bản suýt chọn.

| # | Tin học viên nhắn | Lớp (①②③④) | AI có thể sai thế nào (trỏ tool/dữ liệu) | Sản phẩm tốt nên làm gì | Nhãn (nhẹ / sửa được / không chấp nhận được) |
|---:|---|---|---|---|---|
| 1 |  |  |  |  |  |
| 2 |  |  |  |  |  |
| 3 |  |  |  |  |  |
| 4 |  |  |  |  |  |
| 5 |  |  |  |  |  |
| 6 |  |  |  |  |  |
| 7 |  |  |  |  |  |
| 8 |  |  |  |  |  |

**[GỢI Ý - nhóm sửa] Hard tests của track:** xin giải hộ bài đang mở; xin xác nhận đáp số; tài liệu có câu sai (§3.3 nói độ lệch chuẩn luôn nhỏ hơn phương sai); nhắc nguồn không có ("slide 12"); học viên tự chê mình; hỏi nội dung buổi chưa học (buổi 7 p-value); hỏi hạn nộp bài 3; TA hết giờ trực sau 22:00.

**Quyết định: 2 kịch bản đắt nhất**

- Kịch bản được chọn và vì sao đắt hơn các kịch bản còn lại: <nhóm điền>
- Kịch bản suýt chọn và vì sao không chọn: <nhóm điền>
- Bằng chứng trỏ về tool/dữ liệu cụ thể: <nhóm điền>

### §3. Khi AI sai

> Với hai kịch bản đắt nhất, ghi nguyên văn phản hồi, trạng thái người dùng, bước phục hồi, người được báo, quyết định và loại lỗi. Trỏ nguyên tắc HAX/PAIR vào chỗ thiết kế cụ thể.

- [ ] Hoàn thành các trường cho cả hai kịch bản đắt nhất.
- [ ] Nêu 2–3 nguyên tắc HAX/PAIR gắn với chỗ cụ thể.
- [ ] Nêu một lỗi câu chữ không đủ cứu và cách thiết kế phục hồi.

**Kịch bản đắt nhất #1: <nhóm điền số kịch bản>**

- AI nói gì (nguyên văn): <nhóm điền>
- Người dùng thấy gì: <nhóm điền>
- Làm gì tiếp: <nhóm điền>
- Ai được báo, sau bao lâu: <nhóm điền>
- Quyết định (hỏi lại / trả lời kèm giới hạn / chuyển người); phương án đã loại và vì sao: <nhóm điền>
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao: <nhóm điền>

**Kịch bản đắt nhất #2: <nhóm điền số kịch bản>**

- AI nói gì (nguyên văn): <nhóm điền>
- Người dùng thấy gì: <nhóm điền>
- Làm gì tiếp: <nhóm điền>
- Ai được báo, sau bao lâu: <nhóm điền>
- Quyết định (hỏi lại / trả lời kèm giới hạn / chuyển người); phương án đã loại và vì sao: <nhóm điền>
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao: <nhóm điền>

**Nguyên tắc HAX/PAIR và phục hồi**

- Nguyên tắc 1 (G1, G2, G8, G9, G10, G11, G15 hoặc PAIR), chỗ áp dụng cụ thể: <nhóm điền>
- Nguyên tắc 2 (G1, G2, G8, G9, G10, G11, G15 hoặc PAIR), chỗ áp dụng cụ thể: <nhóm điền>
- [Tuỳ chọn] Nguyên tắc 3 và chỗ áp dụng cụ thể: <nhóm điền>
- Một lỗi sửa câu chữ không cứu được; thiết kế cứu lỗi đó thế nào: <nhóm điền>

### §4. Mức tự chủ

> Đặt mức cho từng tool và giải thích theo cost-of-error: ai chịu hậu quả, có đảo lại được không, và người dùng mất gì khi phải chờ.

- [ ] Chọn mức tự chủ cho cả 4 tool và ghi lý do cost-of-error.
- [ ] Ghi người duyệt, nội dung họ thấy và cách xử lý quá hạn nếu cần duyệt.
- [ ] Thử hai kịch bản đắt nhất và một kịch bản bình thường.
- [ ] Ghi bất đồng về tool khó xếp nhất, luật/tool tách bước và thay đổi lời hứa.

| Tool | Đảo lại được? | Mức của nhóm | Ai duyệt, thấy gì, quá hạn thì sao | Lý do cost-of-error (sai thì ai chịu gì · đảo được không · chờ người thì mất gì) | Phương án đã loại |
|---|---|---|---|---|---|
| `tra_cuu_tai_lieu` | Chỉ đọc |  |  |  |  |
| `goi_y_bai_tap` | Gợi ý quá tay thì đã chép |  |  |  |  |
| `chuyen_TA` | Được |  |  |  |  |
| `dang_FAQ` | Gỡ được nhưng nhiều người đã đọc |  |  |  |  |

**Tool khó xếp nhất:** mỗi người chọn mức nào; giá của mỗi phía (trỏ kịch bản §2); nhóm chốt thế nào: <nhóm điền>

**Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường**

- Cái sai có bị chặn không?: <nhóm điền>
- Còn việc nào làm khi lẽ ra phải hỏi?: <nhóm điền>
- Người dùng bình thường có phải chờ vô ích không?: <nhóm điền>

- Luật thêm hoặc tool tách bước (nếu có), và vì sao: <nhóm điền>
- Mức tự chủ đã đổi lời hứa nào với người dùng: <nhóm điền>

### §5. Prototype

> Ghi cách mở prototype, công cụ và phần mock; ảnh cần nêu điều thể hiện cùng nguyên tắc HAX/PAIR và mức tự chủ.

- [ ] Ghi link/file, công cụ, phần mock và tình trạng lời gọi AI.
- [ ] Gắn ảnh đánh số và mô tả theo bảng.
- [ ] Giải thích quyết định về độ chắc/bằng chứng và điều khiển tự chủ.

- Link/file: `prototype/index.html` · Công cụ: HTML, CSS, JavaScript thuần · Phần mock: toàn bộ (dữ liệu khoá học dựng sẵn, phản hồi AI theo kịch bản mẫu, chuyển TA/báo tài liệu/duyệt FAQ chỉ mô phỏng) · Có lời gọi AI thật không: chưa (cập nhật nếu làm bonus)

| Số | Thể hiện gì | Nguyên tắc HAX/PAIR | Mức tự chủ |
|---:|---|---|---|
| 1 |  |  |  |
| 2 |  |  |  |
| 3 |  |  |  |
| 4 |  |  |  |
| 5 |  |  |  |

Ảnh: ![](prototype/images/<tên>.png)

**Quyết định:** cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ; cách khác đã cân nhắc và vì sao loại: <nhóm điền>

### §6. Tốt là gì

> Viết ba tiêu chí Pass/Fail có thể chấm được và áp dụng vào hai kịch bản đắt nhất; ghi lại lỗi còn lại.

- [ ] Có 3 tiêu chí Pass/Fail đo được.
- [ ] Chấm cả hai kịch bản đắt nhất và ghi lỗi còn lại.

| Tiêu chí Pass/Fail | Kịch bản đắt nhất #1 | Kịch bản đắt nhất #2 |
|---|---|---|
| 1. <nhóm điền tiêu chí> |  |  |
| 2. <nhóm điền tiêu chí> |  |  |
| 3. <nhóm điền tiêu chí> |  |  |

- Lỗi còn lại: <nhóm điền>

### §7. Demo

> Ghi ca lạ từ demo, phản ứng của prototype, thay đổi quyết định nếu có và phân vai trình bày.

- [ ] Ghi ca lạ, phản ứng prototype, thay đổi ý kiến và phân vai demo.

- Ca lạ nhận được: <nhóm điền>
- Prototype đã làm gì: <nhóm điền>
- Nhóm có đổi ý gì không: <nhóm điền>
- Phân vai demo (ai nói phần nào): <nhóm điền>

