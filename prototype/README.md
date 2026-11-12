# Prototype — T2 Giáo dục · Nhóm OHOHO

| Mục | Thông tin |
|---|---|
| Công cụ | HTML, CSS, JavaScript thuần (một file `index.html`) |
| Cách mở | Mở `index.html` bằng trình duyệt. Không cần cài, không đăng nhập, không backend |
| Màn hình | **Màn 1 · Học viên** (ca khó KB#5, KB#2) · **Màn 2 · TA / Giảng viên** (hàng chờ phiếu, FAQ chờ duyệt) |
| Phần mock | Câu trả lời trợ lý viết sẵn theo kịch bản trong `spec.md`; tin tự gõ được phân loại bằng luật từ khoá; kết quả tool `chuyen_TA` (`queued`), hàng chờ TA, FAQ là mô phỏng trong trình duyệt |
| Có lời gọi AI thật không | Không |
| Ảnh đánh số | `images/man1-hoc-vien.png`, `images/man2-ta.png` — số đỏ [1]–[9] giải thích ở bảng `spec.md` §5 |

## Điều khiển

- **Nút ★ KB#5 / ★ KB#2:** hai ca khó nhất. Các nút còn lại: KB#1, KB#3, KB#4, KB#6, KB#7, KB#8, bài 2 đã hết hạn, tin mồi "trung vị khác trung bình".
- **Ô chat:** gõ ca lạ bất kỳ; không khớp luật nào thì trợ lý nói "chưa tìm thấy trong tài liệu buổi 1–3" và hỏi lại.
- **Giờ mô phỏng:** 23:00 (ngoài giờ TA) ↔ 15:00 (trong giờ TA) — đổi giờ trả lời dự kiến trên phiếu.
- **Hiện số chú thích:** bật các số [1]–[9] để chỉ nguyên tắc HAX/PAIR khi được hỏi.
- **Chụp lại ảnh:** mở `index.html#shot=student` hoặc `index.html#shot=ta`.

## Đường bấm ca khó (KB#5, khoảng 1 phút)

1. Mở trang → trợ lý không xác nhận "15.25 / 11.5", trỏ §3.4 → dải đỏ [2], cột Căn cứ [3].
2. Bấm **Gợi ý bước tiếp (1/2)**, rồi **(2/2)** [4] → hết nấc, chỉ còn nút gửi TA.
3. Bấm **Gửi câu hỏi vào hàng chờ sáng mai** → xem phiếu soạn sẵn [5] → **Gửi** → thấy `queued` + "sau 08:00 sáng mai".
4. Bấm **Rút lại** (hoàn tác), hoặc sang **Màn 2** thấy phiếu trong hàng chờ [8] và FAQ bị khoá [9].

Không nhập dữ liệu người thật hoặc API key vào prototype.
