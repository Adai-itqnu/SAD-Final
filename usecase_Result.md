# Phân tích Use Case

## **Use Case 1: Đăng nhập**
### **Luồng chính**
1. Người dùng mở ứng dụng và nhập thông tin đăng nhập (tên người dùng, mật khẩu).
2. Hệ thống kiểm tra thông tin đăng nhập.
3. Nếu thông tin chính xác, hệ thống chuyển hướng người dùng đến trang chính.
4. Người dùng có thể tiếp tục sử dụng các tính năng khác.

### **Luồng phụ**
- **Sai mật khẩu**: Hệ thống hiển thị thông báo và yêu cầu nhập lại.
- **Tài khoản bị khóa**: Hệ thống cảnh báo sau nhiều lần đăng nhập sai và tạm khóa tài khoản.

---

## **Use Case 2: Quản lý khóa học**
### **Luồng chính**
1. Giáo viên đăng nhập và truy cập trang quản lý khóa học.
2. Giáo viên chọn "Tạo khóa học mới" hoặc "Chỉnh sửa khóa học".
3. Điền thông tin chi tiết như tên khóa học, mô tả, thời gian.
4. Lưu thông tin khóa học vào cơ sở dữ liệu.

### **Luồng phụ**
- **Thiếu thông tin**: Hệ thống yêu cầu người dùng điền đủ thông tin cần thiết.
- **Lỗi lưu trữ**: Nếu lỗi cơ sở dữ liệu, hệ thống thông báo và không lưu thay đổi.
- **Xóa khóa học**: Xác nhận hành động trước khi xóa khóa học.

---

## **Use Case 3: Quản lý tài liệu học tập**
### **Luồng chính**
1. Giáo viên vào khóa học và chọn tính năng "Tải tài liệu".
2. Tải tài liệu học tập (PDF, video, tài liệu tham khảo).
3. Hệ thống lưu tài liệu và gửi thông báo đến học sinh trong lớp.

### **Luồng phụ**
- **Lỗi tải tệp**: Nếu tệp quá lớn hoặc định dạng không hỗ trợ, hệ thống hiển thị lỗi.
- **Trùng tài liệu**: Hệ thống cảnh báo nếu tài liệu đã tồn tại.
- **Chỉnh sửa tài liệu**: Nếu tài liệu đang được chỉnh sửa bởi giáo viên khác, khóa chỉnh sửa tạm thời.

---

## **Use Case 4: Đăng ký khóa học**
### **Luồng chính**
1. Học sinh đăng nhập và chọn "Danh sách khóa học".
2. Tìm khóa học phù hợp và nhấn "Đăng ký".
3. Hệ thống xác nhận đăng ký và lưu vào cơ sở dữ liệu.

### **Luồng phụ**
- **Hết chỗ**: Hiển thị thông báo nếu khóa học đã đầy.
- **Hủy đăng ký**: Học sinh có thể hủy đăng ký khóa học, và hệ thống cập nhật lại danh sách.
- **Lỗi thanh toán**: Nếu khóa học yêu cầu phí, lỗi thanh toán sẽ hủy quá trình đăng ký.

---

## **Use Case 5: Gửi thông báo**
### **Luồng chính**
1. Giáo viên tạo thông báo và chọn đối tượng nhận (học sinh, phụ huynh, tất cả).
2. Nhập nội dung thông báo và nhấn gửi.
3. Hệ thống gửi thông báo qua email hoặc ứng dụng.

### **Luồng phụ**
- **Lỗi kết nối**: Nếu mạng bị gián đoạn, hệ thống lưu thông báo và thử gửi lại sau.
- **Sai đối tượng**: Hệ thống cảnh báo nếu danh sách người nhận không hợp lệ.
