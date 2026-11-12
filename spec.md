# Bài nộp LAB5 — T2 Giáo dục · Nhóm OHOHO

| Họ và Tên | Mã Học Viên | Việc đã làm |
|---|---|---|
| Nguyễn Hoàng Việt | 2A202603487 | Kịch bản & rủi ro (§1, §2, §6), nộp repo |
| Đỗ Tuấn Anh | 2A202603465| Khi AI sai & mức tự chủ (§3, §4) |
| Đoàn Gia Long | 2A202603443 | Prototype (§5), demo thao tác |

**Lớp:** L3A · **Bàn / zone:** A2 · **Track:** T2 Giáo dục

### §1. Lát cắt & phạm vi

> Cần nêu đúng lát cắt được phát và giới hạn phạm vi; mỗi việc không làm cần có lý do gắn với mục tiêu sản phẩm.

- [ ] Chép lát cắt và nêu phạm vi.
- [ ] Nêu 3 việc không làm, mỗi việc một câu lý do.

- **Lát cắt:** Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.
- **Không làm 1:** Không giải hộ hoặc xác nhận đáp số bài đang mở — học viên chép đáp số thì không còn hiểu bài, trái với mục tiêu "không chép đáp án"; `goi_y_bai_tap` không đảo được khi đã chép.
- **Không làm 2:** Không nhận xét năng lực người học (kể cả khi học viên tự chê mình) — AI không có căn cứ đánh giá năng lực, và nhận xét sai dễ làm học viên mất tự tin, bỏ học.
- **Không làm 3:** Không dạy nội dung buổi chưa học (buổi 4–10, ví dụ p-value ở buổi 7) — trang khoá học chỉ có tên buổi, chưa có tài liệu, AI dễ bịa nội dung; chỉ nói buổi nào sẽ học, tối đa một câu.

### §2. Kịch bản rủi ro

> Cần có ít nhất 8 kịch bản, đủ các lớp ①②③④; chỉ ra tool hoặc dữ liệu cụ thể nơi AI có thể sai, hành động tốt của sản phẩm và mức độ lỗi.

- [x] Có ít nhất 8 kịch bản, mỗi lớp ①②③④ có ít nhất một kịch bản.
- [x] Mỗi kịch bản có bằng chứng trỏ về tool/dữ liệu, hành động tốt và nhãn.
- [x] Chọn 2 kịch bản đắt nhất, giải thích lựa chọn và kịch bản suýt chọn.

| # | Tin học viên nhắn | Lớp (①②③④) | AI có thể sai thế nào (trỏ tool/dữ liệu) | Sản phẩm tốt nên làm gì | Nhãn (nhẹ / sửa được / không chấp nhận được) |
|---:|---|---|---|---|---|
| 1 | "cô ơi slide 12 bài giảng nói gì thế em mở k lên" | ① Nguồn sự thật | Dữ liệu buổi 3 chỉ có mục §3.1–§3.5, không có slide đánh số. AI không tra thấy trong `tra_cuu_tai_lieu` nhưng tự bịa ra nội dung "Slide 12 nói về..." bằng kiến thức bên ngoài. | Báo rõ tài liệu môn học chỉ chia theo mục §3.1–§3.5, không có đánh số slide; hỏi học viên muốn hỏi chủ đề cụ thể nào. | Sửa được |
| 2 | "trong §3.3 ghi độ lệch chuẩn luôn nhỏ hơn phương sai đúng k ạ em thấy kì kì" | ① Nguồn sự thật | `tra_cuu_tai_lieu` trích nguyên văn câu sai trong dữ liệu buổi 3 (§3.3), AI khẳng định tài liệu luôn đúng và ép học viên tin vào định lý sai này (khi phương sai < 1 thì sai). | Cảnh báo đây là điểm nghi vấn trong tài liệu §3.3; giải thích trường hợp ngoại lệ (khi phương sai < 1); gợi ý học viên bấm nút "Báo tài liệu có thể sai" để giảng viên đính chính. | Không chấp nhận được |
| 3 | "cái độ lệch ấy là sao ta đọc hoài k hiểu" | ② Mơ hồ / thiếu thông tin | Tin nhắn mơ hồ giữa "độ lệch chuẩn" hay "phương sai" trong §3.3. AI tự đoán bừa là độ lệch chuẩn rồi giảng giải dài dòng, trật ý học viên cần hỏi. | Áp dụng G10 (thu hẹp khi nghi ngờ): Hỏi lại một câu rõ ràng xem học viên đang muốn làm rõ "phương sai" hay "độ lệch chuẩn" ở mục §3.3. | Nhẹ |
| 4 | "cho e hỏi hạn nộp bài 3 với lại tính độ lệch chuẩn trong excel dùng hàm gì thế" | ② Mơ hồ / gộp việc | Gộp 2 ý khác nhau. AI có thể bịa hạn nộp nếu không tra bảng Trang khoá học (Hạn đúng: 13/11/2026 23:59), hoặc chỉ trả lời hàm Excel mà quên mất vế hạn nộp. | Tách làm 2 ý rõ ràng: Trích hạn nộp chính xác 13/11/2026 từ trang khóa học, sau đó gợi ý hàm Excel (STDEV.S) gắn với nội dung §3.3. | Nhẹ |
| 5 | "bài 3 tính ra trung bình 15.25 trung vị 11.5 đúng k ạ, check hộ e với mai nộp r" | ③ Ngoài thẩm quyền | Bài 3 (§3.5) đang mở (hạn 13/11). AI gọi tool `goi_y_bai_tap` nhưng xác nhận thẳng đáp số: "Đúng rồi bạn nhé". Học viên chép số vào nộp mà không cần động não tự làm câu (b) về giá trị ngoại lai 45. | Từ chối xác nhận số cụ thể theo chính sách bài tập đang mở; chỉ gợi ý phương pháp: nhắc học viên xem lại §3.4 xem giá trị 45 có kéo lệch số trung bình không. | Không chấp nhận được |
| 6 | "giải thích giúp e p-value với kiểm định giả thuyết là gì, mai e thi" | ③ Ngoài thẩm quyền | P-value thuộc Buổi 7 chưa mở (hiện lớp mới mở Buổi 1–3). AI dùng kiến thức tổng quát giải thích quá sâu/dùng công thức phức tạp làm học viên hoang mang, đi lệch giáo trình. | Báo rõ nội dung này thuộc Buổi 7 (chưa học); chỉ giới thiệu định hướng tối đa 1 câu và khuyên học viên tập trung nắm vững kiến thức Buổi 3. | Sửa được |
| 7 | "em dốt toán quá học k vô chắc rớt môn này mất" | ④ Đặc thù domain | AI buông lời nhận xét/đánh giá năng lực: "Môn này đúng là khó với người mất gốc, bạn nên cố gắng hơn" khiến học viên tự ti, tổn thương tâm lý và bỏ học. | Tuyệt đối không nhận xét năng lực người học; động viên thái độ học tập, gợi ý quay lại đọc định nghĩa trực quan nhất (§3.1) hoặc đề xuất chuyển TA hỗ trợ 1-1. | Sửa được |
| 8 | "bây giờ 23:30 e kẹt bài 3 quá, báo TA gọi lại cho e gấp" | ④ Đặc thù domain | AI gọi `chuyen_TA` rồi hứa hão: "Đã báo TA, TA sẽ phản hồi ngay", làm học viên thức đợi vô ích vì khung giờ TA trực thực tế chỉ từ 08:00–22:00. | Đưa câu hỏi vào hàng chờ của TA; thông báo rõ hiện tại đã ngoài giờ trực (08:00–22:00); hẹn TA sẽ phản hồi sau 08:00 sáng mai và gợi ý tài liệu học tạm thời. | Sửa được |

**Quyết định: 2 kịch bản đắt nhất**

- **Kịch bản được chọn và vì sao đắt hơn các kịch bản còn lại:**
  1. **Kịch bản #2 (Tài liệu sai ở §3.3):** Đắt nhất vì tạo ra **sai lầm âm thầm có tính lan tỏa hệ thống**. Học viên mặc định tài liệu khóa học và AI là chân lý nên sẽ tiếp thu định lý toán học sai mà không hề hay biết. Tệ hơn nữa, nếu câu này bị đẩy tự động lên `dang_FAQ`, toàn bộ học viên trong lớp sẽ học sai theo. Hậu quả này phá hủy hoàn toàn uy tín học thuật của khóa học.
  2. **Kịch bản #5 (Lộ / xác nhận đáp số Bài tập 3 đang mở):** Đắt nhất về mặt sản phẩm vì mang tính chất **không thể đảo ngược (irreversible)** của tool `goi_y_bai_tap`. Một khi AI đã lỡ miệng xác nhận số 15.25 hay 11.5, học viên lập tức chép vào bài nộp; không có cơ chế hoàn tác (undo) nào xóa được đáp án trong đầu học viên. Điều này phá vỡ hoàn toàn cam kết cốt lõi: "học viên tự hiểu bài, không chép đáp án".
- **Kịch bản suýt chọn và vì sao không chọn:** 
  - **Kịch bản #8 (Hỏi lúc 23:30 đòi TA hỗ trợ gấp):** Suýt được chọn vì gây ức chế tâm lý cao cho học viên lúc nửa đêm nếu AI hứa hão. Tuy nhiên, nó bị loại vì thiệt hại chỉ dừng ở mức trải nghiệm/thời gian chờ (sáng hôm sau TA xử lý được), không gây sai lệch kiến thức vĩnh viễn như #2 và không làm mất tính trung thực của kỳ thi/bài tập như #5.
- **Bằng chứng trỏ về tool/dữ liệu cụ thể:**
  - Kịch bản #2 trỏ thẳng vào lỗi thực tế ở file dữ liệu buổi 3, mục **§3.3 Phương sai và độ lệch chuẩn** (dòng khẳng định sai: *"độ lệch chuẩn luôn nhỏ hơn phương sai"*), liên quan đến tool `tra_cuu_tai_lieu` và nguy cơ lan truyền diện rộng của tool `dang_FAQ`.
  - Kịch bản #5 trỏ thẳng vào **§3.5 Bài tập 3** và bảng Trang khoá học (**Bài tập 3 đang mở**, hạn 13/11/2026 23:59), liên quan trực tiếp đến tính chất không thể đảo ngược của tool `goi_y_bai_tap`.

### §3. Khi AI sai

> Với hai kịch bản đắt nhất, ghi nguyên văn phản hồi, trạng thái người dùng, bước phục hồi, người được báo, quyết định và loại lỗi. Trỏ nguyên tắc HAX/PAIR vào chỗ thiết kế cụ thể.

- [x] Hoàn thành các trường cho cả hai kịch bản đắt nhất.
- [x] Nêu 2–3 nguyên tắc HAX/PAIR gắn với chỗ cụ thể.
- [x] Nêu một lỗi câu chữ không đủ cứu và cách thiết kế phục hồi.

**Kịch bản đắt nhất #1: Kịch bản #2 (Tài liệu §3.3 có định lý sai)**

- **AI nói gì (nguyên văn):** "Khẳng định trong giáo trình mục §3.3 có thể chưa chính xác trong mọi trường hợp. Về mặt toán học: độ lệch chuẩn là căn bậc hai của phương sai, nên khi phương sai nhỏ hơn 1 (ví dụ phương sai = 0.25 thì độ lệch chuẩn = 0.5), độ lệch chuẩn sẽ lớn hơn phương sai. Mình đã tạm gắn nhãn nghi vấn cho nội dung này. Bạn có thể bấm nút 'Báo tài liệu có thể sai' bên dưới để hệ thống chuyển thẳng phản ánh lên Giảng viên/TA xác minh nhé."
- **Người dùng thấy gì:** 
  - Khung chat hiển thị câu trả lời nguyên văn trên.
  - Cột "Căn cứ" bên phải hiển thị mã mục `§3.3 Phương sai và độ lệch chuẩn` kèm huy hiệu cảnh báo màu vàng: `[Nghi vấn nội dung - Cần xác minh]`.
  - Nút bấm hành động nhanh: `[Báo tài liệu có thể sai]` và nút `[Chuyển câu hỏi cho TA]`.
- **Làm gì tiếp:** 
  - Bấm `[Báo tài liệu có thể sai]` để gửi yêu cầu đính chính lên Giảng viên.
  - Tự tin tiếp tục học bài với kiến thức toán đúng (phương sai < 1 thì độ lệch chuẩn lớn hơn) mà không bị ép tin vào giáo trình sai.
  - Bấm `[Chuyển câu hỏi cho TA]` nếu vẫn còn thắc mắc sâu hơn.
- **Ai được báo, sau bao lâu:** Giảng viên phụ trách học phần và TA trực ban nhận ticket cảnh báo nội dung lỗi tại mục §3.3 trong dashboard quản trị ngay lập tức (real-time).
- **Quyết định (hỏi lại / trả lời kèm giới hạn / chuyển người); phương án đã loại và vì sao:**
  - **Chọn:** *Trả lời kèm giới hạn (Graceful degradation / Answer with limitations)* — Đưa ra ngay phản ví dụ toán học cụ thể để giải tỏa bế tắc cho học viên lúc đêm muộn, nhưng không tự tiện sửa giáo trình gốc mà dẫn đường lui để học viên báo cáo giảng viên.
  - **Loại "Hỏi lại":** Vì câu hỏi của học viên đã rất rõ ràng vào mệnh đề so sánh ở §3.3, hỏi lại chỉ làm kéo dài thời gian và thể hiện hệ thống né tránh.
  - **Loại "Dừng và chuyển người ngay":** Lúc 23:00 không có ai trực, nếu ngắt ngang chuyển người thì học viên bị tắc nghẽn việc học suốt đêm trong khi một phản ví dụ toán học đơn giản có thể giải quyết ngay thắc mắc.
- **Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao:** **Lỗi hệ thống / nội dung (System/Content Error)**. Nguyên nhân bắt nguồn từ lỗi sai có sẵn trong dữ liệu giáo trình đầu vào (§3.3), không phải lỗi do người dùng nhập sai hay hiểu nhầm ngữ cảnh. Do đó, AI không được xin lỗi kiểu "tôi chưa hiểu ý bạn", mà phải minh bạch thừa nhận nghi vấn đối chiếu giữa toán học và văn bản giáo trình.

**Kịch bản đắt nhất #2: Kịch bản #5 (Xin đáp số Bài tập 3 đang mở)**

- **AI nói gì (nguyên văn):** "Bài tập 3 hiện đang trong thời gian làm bài (hạn nộp đến 23:59 ngày 13/11/2026), nên theo quy định mình không thể xác nhận con số cụ thể hoặc đưa ra kết quả cuối cùng. Tuy nhiên, mình có thể gợi ý phương pháp: Bạn hãy quan sát kỹ dãy 8 mức lương trong §3.5 xem có giá trị nào khác biệt hẳn so với phần còn lại không (xem mục §3.4 về giá trị ngoại lai). Giá trị ngoại lai đó có kéo số trung bình lệch lên nhiều không? Bạn hãy so sánh xem giữa số trung bình và trung vị, con số nào phản ánh mức lương điển hình tốt hơn nhé!"
- **Người dùng thấy gì:** 
  - Dòng cảnh báo cố định màu vàng phía trên khung chat: `[Bài đang mở: chỉ gợi ý bước đầu, không xác nhận đáp án]`.
  - Cột "Căn cứ" trích dẫn 2 mục liên quan: `§3.4 Giá trị ngoại lai` và `§3.5 Bài tập 3`.
  - Các nút gợi ý bước tiếp theo: `[Xem lại định nghĩa ngoại lai §3.4]`, `[Gợi ý câu (b)]`.
  - **Tuyệt đối không có nút nào cho phép xem đáp án hay xác nhận kết quả.**
- **Làm gì tiếp:** 
  - Học viên đọc câu hỏi gợi mở, tự tư duy câu (b) về tác động của số ngoại lai 45 triệu đến số trung bình (15.25) so với trung vị (11.5).
  - Bấm vào nút `[Xem lại định nghĩa ngoại lai §3.4]` để ôn lại lý thuyết trước khi tự nộp bài.
- **Ai được báo, sau bao lâu:** Không cần báo TA vì đây là luồng từ chối hợp lệ theo thiết kế (Expected Policy Enforcement). Hệ thống chỉ lưu log truy vấn của học viên để phục vụ thống kê sau này.
- **Quyết định (hỏi lại / trả lời kèm giới hạn / chuyển người); phương án đã loại và vì sao:**
- **Chọn:** *Trả lời kèm giới hạn (Scaffolded Guidance / Socratic Questioning)* — Từ chối đưa/xác nhận con số, nhưng gợi ý tư duy phương pháp luận theo từng bước để học viên tự làm bài.
  - **Loại "Xác nhận thẳng / đưa đáp án":** Vi phạm nghiêm trọng đạo đức học thuật và quy chế thi cử; tool `goi_y_bai_tap` một khi đã phát ra đáp án thì không thể hoàn tác (không có nút undo trong đầu người học).
  - **Loại "Từ chối thẳng thừng và dừng":** Khiến học viên nản chí, ức chế và có thể bỏ cuộc khi đang kẹt bài lúc đêm muộn.
- **Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao:** **Lỗi ngữ cảnh (Context / Scope Error)**. Học viên và hệ thống đều làm đúng vai trò của mình (học viên muốn dò đáp án để an tâm nộp bài, AI có khả năng tính toán kết quả), nhưng mong muốn của học viên xung đột với mục tiêu giáo dục của khóa học. Thiết kế phải kiên quyết giữ ranh giới nguyên tắc sư phạm nhưng khéo léo dùng câu hỏi gợi mở để hỗ trợ.

**Nguyên tắc HAX/PAIR và phục hồi**

- **Nguyên tắc 1: G2 — Làm rõ hệ thống làm tốt đến đâu (HAX) / Setting Expectations (PAIR):** Áp dụng tại thanh thông báo cố định trên cùng khung chat: `[Bài đang mở: chỉ gợi ý bước đầu]` và nhãn `[Căn cứ giới hạn trong tài liệu buổi 3]`. Thiết lập ranh giới rõ ràng ngay từ đầu để học viên không kỳ vọng AI là công cụ giải bài hộ.
- **Nguyên tắc 2: G10 — Thu hẹp phạm vi khi nghi ngờ (HAX):** Áp dụng tại Kịch bản #2: Khi phát hiện định lý ở §3.3 có mâu thuẫn toán học, AI không khẳng định liều mạng mà thu hẹp câu trả lời vào trường hợp biên cụ thể (khi phương sai < 1), đồng thời từ chối khẳng định tính tuyệt đối của giáo trình.
- **Nguyên tắc 3: G11 — Giải thích vì sao hệ thống hành xử như vậy (HAX) / Explainability (PAIR):** Áp dụng tại Kịch bản #5: AI không chỉ từ chối cộc lốc mà giải thích rõ căn cứ: vì Bài tập 3 đang mở (hạn 13/11/2026 23:59), trích dẫn chính xác mục §3.4 và §3.5 làm cơ sở hướng dẫn phương pháp thay vì đưa đáp số.
- **Một lỗi sửa câu chữ không cứu được; thiết kế cứu lỗi đó thế nào:**
  - *Lỗi:* AI tự ý hứa hẹn một việc ngoài tầm kiểm soát của mình: *"Mình đã báo TA rồi, bạn đợi chút TA sẽ hỗ trợ ngay"* khi học viên nhắn lúc 23:30 đêm (trong khi khung giờ trực của TA chỉ từ 08:00–22:00).
  - *Vì sao câu chữ không cứu được:* Dù câu chữ AI có trau chuốt, trấn an khéo léo đến đâu ("đang liên hệ", "sắp có người hỗ trợ"), học viên vẫn sẽ thức chờ vô ích trong thất vọng vì thực tế TA đã hết giờ làm việc.
  - *Thiết kế cứu lỗi đó:* 
    1. **Khóa cứng trên giao diện (UI Guardrail):** Kiểm tra đồng hồ máy chủ, nếu ngoài khung giờ `08:00–22:00`, nút `[Chuyển TA]` tự động đổi tên thành `[Gửi câu hỏi vào hàng chờ sáng mai]`.
    2. **Chặn trạng thái (State Validation):** Chỉ khi API của tool `chuyen_TA` trả về mã thành công `queued`, giao diện mới hiển thị thông báo: *"Đã lưu câu hỏi vào hàng chờ. TA sẽ trả lời sau 08:00 sáng mai"*, loại bỏ hoàn toàn khả năng AI bịa lời hứa hẹn.
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

