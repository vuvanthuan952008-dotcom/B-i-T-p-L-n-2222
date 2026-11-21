# Nhật ký trao đổi và hỗ trợ từ AI (`AI_LOG`)

* **Người thực hiện:** Vũ Văn Thuận (Lớp 20-02, ngành Công nghệ thông tin)
* **Dự án:** Trang web giới thiệu bản thân (`index.html`, `css/style.css`)
* **Công cụ sử dụng:** Gemini

## 1. Mục đích sử dụng AI trong quá trình làm bài
Mình dùng AI để hỗ trợ rà soát lỗi cú pháp HTML/CSS, căn chỉnh lại khung hiển thị ảnh đại diện và hoàn thiện tài liệu mô tả cho repo. Phần nội dung cá nhân, thông tin học tập, sở thích và mục tiêu đều do mình tự viết và chỉnh sửa lại theo ý mình.

## 2. Quá trình làm việc và các chỉnh sửa chính

### Phần ảnh đại diện (`div.avatar` và `assets/1.jpg`)
* **Vấn đề gặp phải:** Ban đầu thẻ ảnh viết thiếu dấu đóng mở (`<img>`), sau đó khi ảnh hiện lên thì lại bị phóng to tràn bố cục, rồi khi thu nhỏ thì khung ảnh lại hơi bé và khuôn mặt nằm xa.
* **Cách xử lý cùng AI:** Sửa lại thẻ `<img src="./assets/1.jpg" alt="Ảnh đại diện">`, thêm thuộc tính `object-fit: cover`, điều chỉnh kích thước khung và góc lấy ảnh (`object-position`, `transform: scale(...)`) để ảnh cân đối hơn trên nền `.hero`.

### Kiểm tra lại CSS và bố cục trang
* **Các mục đã rà soát trong `style.css`:**
  * Bố cục đầu trang `.hero` với nền gradient xanh và nút bấm `.button`.
  * Lưới thông tin cá nhân `.info-grid` (2 cột trên màn hình lớn, 1 cột trên màn hình nhỏ).
  * Khu vực sở thích `.cards` (3 thẻ `.hobby-card` có hiệu ứng nâng nhẹ khi rê chuột) và danh sách mục tiêu `.goal-box`.
  * Responsive bằng `@media` cho màn hình dưới `700px` và `430px`.
* **Điểm cần lưu ý sửa tiếp trong file hiện tại:** Trong bản CSS gửi đi vẫn còn dấu `- {` ở đầu file cần đổi thành `* {` để reset `box-sizing`, `margin`, `padding`, đồng thời gộp lại hai đoạn định nghĩa `.avatar` cho đỡ bị ghi đè.

### Viết tài liệu dự án (`README.md` và `AI_LOG`)
* Nhờ AI tổng hợp lại cấu trúc các thẻ trong `index.html` và các nhóm quy tắc trong `css/style.css` thành bản nháp `README.md` và bản nhật ký này, sau đó mình đọc lại và chỉnh câu chữ cho tự nhiên, đúng văn phong cá nhân.

## 3. Tự đánh giá sau khi làm
Qua bài này mình nắm rõ hơn cách liên kết file CSS (`css/style.css`), đường dẫn ảnh tương đối (`./assets/1.jpg`), cách chia layout bằng Flexbox/Grid và cách dùng `@media` để trang không bị vỡ khi thu nhỏ cửa sổ trình duyệt.