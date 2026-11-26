# 🚦 Hành trình ATGT: Trò chơi khảo sát và chấm bài

Web trò chơi trắc nghiệm cho buổi tập huấn **Giáo dục an toàn giao thông trong trường tiểu học**.
Gồm 10 câu hỏi (9 câu có đáp án, 1 câu khảo sát) và một trang chấm bài cho ban tổ chức.

## Tính năng

- 🎮 **Chơi:** đường đua xe, đèn giao thông đếm ngược 35 giây, điểm thưởng tốc độ, combo, pháo giấy, âm thanh, danh hiệu cuối game.
- 📨 **Mã kết quả:** cuối game, giáo viên sao chép mã và gửi cho ban tổ chức.
- 📊 **Chấm:** dán các mã vào trang chấm (`#cham`) để tự chấm, xếp hạng, xem tỉ lệ đúng từng câu, thống kê câu khảo sát và sao chép bảng điểm CSV dán vào Excel.
- 🌗 Giao diện tự chuyển sáng/tối theo thiết bị, dùng được trên điện thoại.

## Cách sử dụng

- Giáo viên mở: `https://<tên-github>.github.io/<tên-repo>/`
- Ban tổ chức chấm bài: bấm nút **📊 Chấm** hoặc thêm `#cham` vào cuối link.

## Đưa lên GitHub Pages

1. Tạo repository mới trên GitHub (ví dụ `atgt-khao-sat`).
2. Tải 3 file `index.html`, `README.md`, `.nojekyll` vào repository (Add file → Upload files), rồi Commit.
3. Vào **Settings → Pages**, mục *Source* chọn nhánh `main`, thư mục `/ (root)`, bấm **Save**.
4. Sau 1–2 phút, trang chạy tại địa chỉ ở trên.

> `.nojekyll` là file rỗng, báo cho GitHub Pages phục vụ trang trực tiếp, không xử lý bằng Jekyll.

## Chỉnh sửa nội dung

Mọi thứ nằm trong `index.html`:

- **Câu hỏi, đáp án, lời giải thích:** mảng `Q` trong phần `<script>` (`k` là đáp án đúng, `k:null` là câu khảo sát).
- **Thời gian mỗi câu:** biến `TIME` (mặc định 35 giây).
- **Màu sắc:** các biến `--pri`, `--gold`... ở đầu phần `<style>`.

Nếu đổi thứ tự hoặc số câu hỏi, các mã kết quả đã nộp trước đó sẽ không chấm đúng nữa.

## Lưu ý

- Trang không có máy chủ: điểm chỉ lưu trên máy người chơi cho đến khi họ gửi mã về ban tổ chức.
- Trang chấm tự chấm lại từ đáp án chuẩn, không dùng điểm do người chơi tự báo.
- Font chữ được tải từ Google Fonts, cần có mạng khi mở trang.
