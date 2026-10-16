# CNTT2
Phần 1. Phân tích lỗi cú pháp

Đoạn mã của bạn sinh viên có 4 lỗi cú pháp chính khiến kết quả render bị lỗi:
1. Sai cú pháp chèn hình ảnh: Bạn sinh viên đang dùng cú pháp của liên kết [Text](URL) thay vì cú pháp hình ảnh ![Alt text](URL). Việc thiếu dấu chấm than (!) và thừa dấu ngoặc nhọn < > quanh link khiến ảnh không hiển thị mà chỉ hiện thành một đường dẫn văn bản.
2. Thiếu khoảng trắng sau dấu băm (#): Trong Markdown, sau các ký tự # bắt buộc phải có một khoảng trắng (space) rồi mới đến chữ. Việc viết dính liền như \# (hoặc \###) khiến trình biên dịch hiểu đây là văn bản thuần túy chứ không phải là tiêu đề (Heading).
3. Phân cấp tiêu đề không hợp lý: Tiêu đề nhảy bậc đột ngột từ H1 (# Lợi ích của rau sạch) xuống thẳng H2/H3 mà bỏ qua thứ tự logic, làm cấu trúc bài viết bị lộn xộn. Ngoài ra, việc sử dụng dấu gạch chéo ngược \ trước dấu # là ký tự thoát (escape character), vô tình vô hiệu hóa chức năng tạo tiêu đề.
4. Sai quy tắc in đậm văn bản: Để in đậm văn bản, Markdown quy định phải sử dụng hai dấu sao **văn bản** hoặc hai dấu gạch dưới __văn bản__. Việc chỉ dùng một dấu sao *Rất quan trọng* sẽ biến văn bản thành chữ in nghiêng.

Phần 2. Hoàn thiện đoạn mã Markdown chuẩn

markdown
# Lợi ích của rau sạch

## Danh sách các loại rau

![Logo Dự án](https://greentech.vn/logo.png)

**Rất quan trọng**
Hãy thận trọng khi sử dụng mã.
Giải thích các điểm đã sửa đổi:
• # Lợi ích của rau sạch: Tiêu đề H1 duy nhất của bài, có khoảng trắng chuẩn.
• ## Danh sách các loại rau: Đã sửa thành tiêu đề H2 (2 dấu #) để đảm bảo tính phân cấp logic ngay sau H1.
• ![Logo Dự án](...): Thêm dấu ! ở đầu và bỏ dấu < > ở link để ảnh render hiển thị chính xác.
• **Rất quan trọng**: Sử dụng cặp 2 dấu sao để ép kiểu chữ in đậm đúng quy định.
