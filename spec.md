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

- **AI nói gì (nguyên văn):** "Khẳng định trong giáo trình mục §3.3 có thể chưa chính xác trong mọi trường hợp. Về mặt toán học: độ lệch chuẩn là căn bậc hai của phương sai, nên khi phương sai nhỏ hơn 1 (ví dụ phương sai = 0.25 thì độ lệch chuẩn = 0.5), độ lệch chuẩn sẽ lớn hơn phương sai. Mình đánh dấu đoạn §3.3 này là *nghi vấn* ở cột Căn cứ để bạn biết cần kiểm lại; tài liệu gốc vẫn giữ nguyên cho tới khi giảng viên xác nhận. Nếu muốn, bạn bấm nút 'Báo tài liệu có thể sai' bên dưới để gửi phản ánh cho giảng viên/TA. Hiện đã ngoài giờ trực (08:00–22:00) nên phản ánh sẽ được xem sau 08:00 sáng mai."
- **Người dùng thấy gì:** 
  - Khung chat hiển thị câu trả lời nguyên văn trên.
  - Cột "Căn cứ" bên phải hiển thị mã mục `§3.3 Phương sai và độ lệch chuẩn` kèm huy hiệu cảnh báo màu vàng: `[Nghi vấn nội dung - Cần xác minh]`. Đây chỉ là nhãn hiển thị trong phiên của học viên này (AI không có tool sửa tài liệu), không thay đổi tài liệu gốc.
  - Nút bấm hành động nhanh: `[Báo tài liệu có thể sai]` và nút chuyển TA — lúc 23:00 nút này hiện là `[Gửi câu hỏi vào hàng chờ sáng mai]` (luật ngoài giờ ở mục "Thiết kế cứu lỗi" bên dưới). Bấm nút nào cũng mở phiếu soạn sẵn để học viên xem lại rồi mới bấm Gửi (§4, `chuyen_TA`).
- **Làm gì tiếp:** 
  - Bấm `[Báo tài liệu có thể sai]` để gửi yêu cầu đính chính lên Giảng viên.
  - Tự tin tiếp tục học bài với kiến thức toán đúng (phương sai < 1 thì độ lệch chuẩn lớn hơn) mà không bị ép tin vào giáo trình sai.
  - Bấm `[Gửi câu hỏi vào hàng chờ sáng mai]` nếu vẫn còn thắc mắc sâu hơn.
  - Nếu học viên không bấm gì: không phiếu nào được gửi, AI không nói "đã báo"; nhãn nghi vấn vẫn hiện ở cột Căn cứ nên học viên không bị dẫn tới tin câu sai.
- **Ai được báo, sau bao lâu:** Chỉ khi học viên bấm Gửi và tool `chuyen_TA` trả về `queued`, phiếu "nghi vấn §3.3" vào hàng chờ của giảng viên phụ trách và TA ngay lúc đó. Ngoài giờ trực (08:00–22:00) thì phiếu được xử lý sau 08:00 sáng hôm sau; học viên thấy dòng "Đã lưu phản ánh. Giảng viên/TA sẽ xem sau 08:00 sáng mai". Người nhận thấy: câu nguyên văn §3.3, phản ví dụ AI đã đưa, câu hỏi gốc của học viên.
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
  - Các nút gợi ý bước tiếp theo: `[Xem lại định nghĩa ngoại lai §3.4]`, `[Gợi ý bước tiếp (1/2)]` — mỗi nấc chỉ nói *cần làm gì*, không tính hộ, không viết hộ nhận xét câu (b); tối đa 2 nấc (§4, `goi_y_bai_tap`).
  - **Tuyệt đối không có nút nào cho phép xem đáp án hay xác nhận kết quả.** Hết 2 nấc thì chỉ còn nút gửi câu hỏi cho TA.
- **Làm gì tiếp:** 
  - Học viên đọc câu hỏi gợi mở, tự tư duy câu (b) về tác động của số ngoại lai 45 triệu đến số trung bình (15.25) so với trung vị (11.5).
  - Bấm vào nút `[Xem lại định nghĩa ngoại lai §3.4]` để ôn lại lý thuyết trước khi tự nộp bài.
- **Ai được báo, sau bao lâu:** Không cần báo TA vì đây là luồng từ chối hợp lệ theo thiết kế (Expected Policy Enforcement). Hệ thống chỉ lưu log truy vấn của học viên để phục vụ thống kê sau này. Ngoại lệ: nếu học viên đã dùng hết 2 nấc gợi ý mà vẫn kẹt và tự bấm gửi, phiếu (câu hỏi + các gợi ý đã đưa) vào hàng chờ TA và được trả lời trong giờ trực 08:00–22:00; học viên thấy giờ dự kiến trước khi bấm.
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

- [x] Chọn mức tự chủ cho cả 4 tool và ghi lý do cost-of-error.
- [x] Ghi người duyệt, nội dung họ thấy và cách xử lý quá hạn nếu cần duyệt.
- [x] Thử hai kịch bản đắt nhất và một kịch bản bình thường.
- [x] Ghi bất đồng về tool khó xếp nhất, luật/tool tách bước và thay đổi lời hứa.

**Bối cảnh chung khi xếp mức:** học viên hỏi lúc tối muộn, TA chỉ trực 08:00–22:00 (Dữ liệu B). Nghĩa là mọi bước "cần TA duyệt" sau 22:00 sẽ chờ ít nhất tới 08:00 sáng hôm sau — mà Bài tập 3 hết hạn 13/11/2026 23:59. **Chờ người cũng là một kiểu sai**, nên nhóm chỉ đặt "TA duyệt" ở chỗ không gấp (FAQ), còn chỗ gấp thì dùng **luật cứng + học viên tự bấm**.

| Tool | Đảo lại được? | Mức của nhóm | Ai duyệt, thấy gì, quá hạn thì sao | Lý do cost-of-error (sai thì ai chịu gì · đảo được không · chờ người thì mất gì) | Phương án đã loại |
|---|---|---|---|---|---|
| `tra_cuu_tai_lieu` | Chỉ đọc | **Tự làm** — kèm 2 luật: (1) mọi câu về nội dung phải hiện mã mục + đoạn trích nguyên văn; (2) tra không thấy (vd "slide 12", KB#1) thì nói thẳng "tài liệu không có", không lấy kiến thức ngoài lấp vào | Không ai duyệt. Học viên tự kiểm qua đoạn trích ở cột "Căn cứ". Đoạn trích mà AI thấy mâu thuẫn (vd §3.3, KB#2) hoặc đã có người báo nghi vấn thì hiện kèm nhãn vàng "Nghi vấn – cần xác minh" — chỉ là nhãn hiển thị cho học viên, không sửa tài liệu gốc (không tool nào sửa tài liệu) | **Sai thì:** trích nhầm mục → học viên đọc nhầm một đoạn, nhưng thấy ngay mã mục và nguyên văn nên tự phát hiện được (nhẹ). **Đảo:** không thay đổi gì nên không cần đảo. **Chờ người:** mỗi câu hỏi phải chờ tới 08:00 → học viên 23:00 bỏ học luôn, mất toàn bộ giá trị của lát cắt. Chờ đắt hơn sai rất nhiều. Rủi ro thật nằm ở câu AI *diễn giải* sau khi tra (KB#1 bịa slide, KB#2 tin câu sai), nên nhóm chặn bằng luật hiển thị chứ không bằng duyệt | *Cần duyệt:* loại vì chờ đắt hơn sai (xem trên). *Tự làm không kèm luật:* loại vì KB#1 — AI tra không thấy "slide 12" vẫn có thể kể bừa |
| `goi_y_bai_tap` | Gợi ý quá tay thì đã chép | **Tách 3 bậc theo trạng thái bài** (xem "Tool khó xếp nhất"): **(a)** bài đã hết hạn & có đáp án (BT2) → **tự làm**, giải đầy đủ; **(b)** bài đang mở (BT3), gợi ý phương pháp/bước đầu, không chứa số đáp án → **tự làm**; gợi ý bước sâu hơn → **học viên bấm từng nấc**, tối đa 2 nấc; **(c)** đưa hoặc xác nhận đáp số / viết hộ nhận xét câu (b) của bài đang mở → **cấm** | (b) Học viên tự bấm "Gợi ý bước tiếp" — trước khi bấm thấy: "Nấc 1/2 · vẫn chưa có đáp số · nấc cuối chỉ nói *cần tính gì*, không tính hộ". Hết 2 nấc → chỉ còn nút "Gửi câu hỏi cho TA". (c) Không có nút nào; AI nói rõ "đáp án mở sau hạn 13/11/2026 23:59" | **Sai thì:** gợi ý quá tay ở bài đang mở → học viên chép đáp số, mất cơ hội tự hiểu, bài nộp không còn là của mình (KB#5 — không chấp nhận được). **Đảo:** **không đảo được** — không có nút "quên đáp số". **Chờ người:** nếu bắt TA duyệt từng gợi ý thì 23:00 phải chờ tới 08:00 ngày 13/11, tức chỉ còn chưa tới 16 tiếng tới hạn, học viên kẹt cả đêm → cũng là sai. Vì vậy: cái *không đảo được* (đáp số) → **cấm**; cái *rẻ* (bước đầu, trỏ §3.4) → **tự làm**; ở giữa thì để học viên chủ động kéo từng nấc, có trần | *Cấm toàn bộ với bài đang mở:* loại vì học viên kẹt lúc đêm muộn mà AI không giúp gì, đi ngược lát cắt "gợi ý từng bước". *TA duyệt mọi gợi ý:* loại vì TA không trực sau 22:00. *Tự làm không giới hạn:* loại vì KB#5 |
| `chuyen_TA` | Được | **Tách 2 bước:** AI **tự soạn** phiếu (câu hỏi + mã mục + những gì đã gợi ý) → **học viên bấm "Gửi"** mới gửi. Biến thể "Báo tài liệu có thể sai" (KB#2) cũng đi qua tool này, gửi tới giảng viên + TA | Người duyệt = **học viên**. Trước khi bấm thấy: nội dung phiếu (sửa/xoá được), người nhận, và **giờ trả lời dự kiến lấy từ giờ trực** (trong 08:00–22:00: "trong giờ trực hôm nay"; ngoài giờ: "sau 08:00 sáng mai"). Không bấm thì **không gửi** và AI không được nói "đã báo TA". Đã gửi mà TA chưa mở → còn nút "Rút lại" | **Sai thì:** gửi nhầm → TA tốn vài phút đọc một câu không cần (rẻ). Nguy cơ lớn hơn là AI gửi *âm thầm* một câu học viên ngại cho TA thấy (vd KB#7 "em dốt toán quá") → mất niềm tin. **Đảo:** được, rút lại trước khi TA mở. **Chờ người:** không chờ ai cả — người duyệt chính là học viên, 1 lần bấm. Nguy cơ đắt nhất của tool này là **lời hứa sai** (KB#8 "TA sẽ phản hồi ngay" lúc 23:30), nên trạng thái hiển thị chỉ lấy từ kết quả tool (`queued` + giờ dự kiến), không lấy từ câu AI viết | *Tự làm (AI tự chuyển khi thấy cần):* loại vì học viên mất quyền quyết định câu nào tới TA, và AI dễ nói "đã báo" khi tool chưa chạy. *TA duyệt mới nhận:* vô nghĩa — TA chính là người nhận. *Cấm:* loại vì đây là đường lui duy nhất khi tài liệu không có/nghi vấn |
| `dang_FAQ` | Gỡ được nhưng nhiều người đã đọc | **Cần người duyệt (TA/giảng viên)**. AI chỉ được **tự soạn nháp** vào hàng chờ, không ai ngoài TA thấy. Thêm 2 luật cấm: nội dung đang gắn nhãn nghi vấn (§3.3) **cấm đăng** tới khi giảng viên xác nhận; nội dung liên quan bài đang mở (BT3) **cấm đăng** trước hạn 13/11/2026 23:59 | TA duyệt trong giờ trực. Thấy: câu hỏi (ẩn tên học viên), câu trả lời nháp, mã mục căn cứ, nhãn nghi vấn nếu có, số học viên đã hỏi câu tương tự. Nút: Đăng / Sửa rồi đăng / Bỏ. **Quá hạn:** không ai duyệt thì nháp nằm yên trong hàng chờ, **không bao giờ tự đăng** | **Sai thì:** cả lớp đọc một câu sai (KB#2: "độ lệch chuẩn luôn nhỏ hơn phương sai" lên FAQ → mọi học viên học sai, mất uy tín khoá học) hoặc lộ hướng giải BT3 cho cả lớp. **Đảo:** gỡ được bài, nhưng **không gỡ được những gì đã đọc** — sai một câu nhân lên theo số người. **Chờ người:** gần như không mất gì; FAQ không gấp, học viên đang hỏi vẫn được trả lời riêng ngay trong chat | *Tự làm:* loại vì KB#2 lan ra cả lớp. *Cấm hẳn:* loại vì mất lợi ích FAQ (giảm câu hỏi lặp lại cho TA), trong khi một lần bấm duyệt của TA đã đủ chặn |

**Tool khó xếp nhất: `goi_y_bai_tap`**

- **Vì sao khó:** mức nào cũng có giá, và cả hai phía đều trỏ về kịch bản ở §2.
  - Xếp **tự làm** → KB#5: học viên đưa "15.25 / 11.5, check hộ e", AI lỡ xác nhận "đúng rồi" → đáp số đã chép, không đảo được.
  - Xếp **cấm / TA duyệt** → học viên kẹt BT3 lúc 23:00 (như KB#8: TA không trực sau 22:00), không được gợi ý cả bước đầu → bỏ bài hoặc đi chép chỗ khác; đi ngược lát cắt "gợi ý từng bước".
- **Mỗi người tự xếp trước (5 phút, không bàn):**
  - **Nguyễn Hoàng Việt — cấm với bài đang mở:** an toàn tuyệt đối cho KB#5. Giá: học viên kẹt cả đêm.
  - **Đỗ Tuấn Anh — cần TA duyệt:** TA kiểm từng gợi ý. Giá: sau 22:00 không ai duyệt, chờ tới 08:00 khi hạn chỉ còn chưa tới 16 tiếng.
  - **Đoàn Gia Long — tự làm, kèm luật "không chứa số":** nhanh. Giá: luật chỉ chặn được câu AI *viết ra số*, không chặn được gợi ý quá tay kiểu "lấy tổng chia 8 là xong".
- **Cách nhóm chốt:** không chọn một mức cho cả tool mà **tách theo cái gì không đảo được**. Thứ không đảo được là *đáp số và lời xác nhận đáp số* → **cấm**. Thứ rẻ là *gợi ý phương pháp, trỏ mục tài liệu* → **tự làm**. Phần giữa (gợi ý sâu hơn) → **học viên bấm từng nấc, trần 2 nấc**, nấc cuối chỉ nói *cần tính gì*, không tính. Bài đã hết hạn (BT2, đáp án 6 đã công bố 07/11) → **tự làm**, giải đầy đủ, vì không còn gì để chép. Ý của Việt được giữ ở bậc (c), ý của Long ở bậc (b), còn ý của Tuấn Anh chuyển sang `dang_FAQ` — nơi TA duyệt mà không làm ai phải chờ.

**Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường**

| Kịch bản | Với mức này AI làm gì, học viên thấy gì | Cái sai có bị chặn không? | Còn việc nào làm khi lẽ ra phải hỏi? | Người dùng bình thường có phải chờ vô ích không? |
|---|---|---|---|---|
| **KB#2** — "§3.3 ghi độ lệch chuẩn luôn nhỏ hơn phương sai đúng k ạ" | `tra_cuu_tai_lieu` (tự làm) trích §3.3 nguyên văn, kèm nhãn vàng "Nghi vấn". AI đưa phản ví dụ (phương sai 0.25 → độ lệch chuẩn 0.5). `chuyen_TA` soạn sẵn phiếu "Báo tài liệu có thể sai §3.3", học viên bấm Gửi. `dang_FAQ`: câu này bị luật **cấm đăng** khi còn nhãn nghi vấn | **Có.** Học viên không bị ép tin câu sai; câu sai không lan lên FAQ cả lớp (luật cấm đăng nội dung nghi vấn + TA phải duyệt). | Có một chỗ đáng cân nhắc: AI tự kết luận câu trong tài liệu là sai. Nhóm chấp nhận vì đây là phản ví dụ toán học kiểm được, và AI chỉ nói "có thể chưa chính xác", không sửa tài liệu gốc. Việc báo giảng viên vẫn do học viên bấm | Không. Học viên có câu trả lời ngay lúc đêm muộn; chỉ việc *sửa tài liệu* phải chờ giảng viên, và việc đó không chặn học viên học tiếp |
| **KB#5** — "bài 3 tính ra trung bình 15.25 trung vị 11.5 đúng k ạ, check hộ e" | BT3 đang mở → bậc (c) **cấm** xác nhận: không có nút "xem đáp án"/"kiểm tra đáp số". AI nói rõ hạn 13/11/2026 23:59 và đáp án mở sau hạn; tự làm bậc (b): gợi ý xem §3.4, giá trị 45 có kéo trung bình lên không. Muốn thêm thì bấm "Gợi ý bước tiếp" (1/2, 2/2) | **Có.** Không có đường nào để AI nói "đúng"/"sai" với con số của bài đang mở — đây là luật cứng, không phụ thuộc câu chữ. | Còn một rủi ro: học viên bấm hết 2 nấc vẫn có thể tự suy ra đáp án. Nhóm chấp nhận — tự suy ra từ gợi ý chính là "tự làm bài". Không có việc nào AI làm thay khi lẽ ra phải hỏi | Không. Bước đầu đến ngay, không chờ TA. Chỉ khi hết 2 nấc mới cần chuyển TA |
| **KB#4 (bình thường)** — "cho e hỏi hạn nộp bài 3 với lại tính độ lệch chuẩn trong excel dùng hàm gì thế" | `tra_cuu_tai_lieu` (tự làm) lấy hạn **13/11/2026 23:59** từ trang khoá học (Dữ liệu B) và §3.3 cho khái niệm. Hàm bảng tính (STDEV.S) là kiến thức công cụ, không phải đáp số BT3 → bậc (b) tự làm, kèm nhãn "ngoài tài liệu buổi 3" | Không có cái sai đắt để chặn; luật "hạn nộp chỉ lấy từ trang khoá học" chặn việc bịa hạn | Không | **Không.** Trả lời ngay, không qua bước duyệt nào — kiểm chứng rằng mức tự chủ không làm chậm câu hỏi thường |

**Luật thêm hoặc tool tách bước, và vì sao**

1. **Tách `goi_y_bai_tap` thành 3 bậc theo trạng thái bài** (đã hết hạn / đang mở – bước đầu / đang mở – đáp số). Chặn KB#5 mà không để học viên kẹt cả đêm.
2. **Tách `chuyen_TA` thành "soạn phiếu" (AI tự làm) và "gửi" (học viên bấm).** Chặn KB#8 (AI nói "đã báo TA" khi chưa gửi) và KB#7 (câu tự chê bị gửi đi mà học viên không biết).
3. **Tách `dang_FAQ` thành "soạn nháp" (AI tự làm, chỉ TA thấy) và "đăng" (TA duyệt).** Chặn KB#2 lan ra cả lớp.
4. **Luật trạng thái:** mọi câu về TA ("đã gửi", "trả lời lúc nào") chỉ được hiện từ kết quả tool (`queued` + giờ trực 08:00–22:00), không do AI tự viết.
5. **Luật nguồn:** hạn nộp chỉ lấy từ trang khoá học; nội dung chỉ từ tài liệu buổi đã mở (1–3); tra không thấy thì nói "tài liệu không có".

**Mức tự chủ đã đổi lời hứa nào với người dùng**

- `goi_y_bai_tap`: từ lời hứa ngầm *"Trợ lý giải bài cùng bạn"* → *"Trợ lý chỉ bạn bước đầu và trỏ đúng mục tài liệu; bạn tự làm, đáp án mở sau hạn nộp."* Học viên biết trước sẽ không nhận được đáp số, nên không thất vọng khi bị từ chối (gắn với thanh thông báo "Bài đang mở" ở §3).
- `chuyen_TA`: từ *"Trợ lý sẽ báo TA cho bạn"* → *"Trợ lý soạn sẵn câu hỏi, bạn bấm gửi; bạn thấy TA trả lời lúc nào."* Lời hứa nhỏ hơn nhưng giữ được — lúc 23:30 học viên biết phải đợi tới sau 08:00, không thức chờ vô ích.

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

