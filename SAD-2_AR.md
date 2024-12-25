### **Kết quả phân tích từng ca sử dụng**

#### **Ca sử dụng 1: Quản lý người dùng**
- **Mô tả:**  
  Quản lý việc đăng ký, đăng nhập, và quản trị thông tin người dùng (học sinh, giáo viên, quản trị viên).  
- **Liên hệ cơ chế:**  
  - **Bảo mật:** Xác thực bằng OAuth 2.0, phân quyền theo vai trò.  
  - **Phát hiện lỗi:** Hiển thị thông báo khi thông tin đăng nhập sai.  
- **Ví dụ:**  
  Học sinh đăng nhập, cập nhật thông tin cá nhân, và nhận thông báo về khóa học.

---

#### **Ca sử dụng 2: Quản lý khóa học**
- **Mô tả:**  
  Giáo viên tạo, quản lý khóa học và học sinh đăng ký tham gia.  
- **Liên hệ cơ chế:**  
  - **Cơ chế quản lý giao dịch:** Áp dụng nguyên tắc ACID khi đăng ký hoặc hủy khóa học.  
  - **Kiểm soát tiến trình:** Đồng bộ hóa tài nguyên để tránh xung đột chỉnh sửa.  
- **Ví dụ:**  
  Giáo viên tạo khóa học mới, thêm tài liệu và hệ thống gửi thông báo tự động đến học sinh.

---

#### **Ca sử dụng 3: Học tập và tương tác**
- **Mô tả:**  
  Học sinh tham gia học tập, tải tài liệu, nộp bài tập, và tương tác với giáo viên.  
- **Liên hệ cơ chế:**  
  - **Cơ chế định tuyến tin nhắn:** Gửi thông báo tự động về bài tập hoặc tài liệu mới.  
  - **Tính bền vững:** Hỗ trợ nhiều người dùng đồng thời truy cập tài liệu trong mùa thi.  
- **Ví dụ:**  
  Học sinh nhận thông báo bài tập qua email, tải xuống và nộp trực tiếp trên hệ thống.

---

#### **Ca sử dụng 4: Quản trị hệ thống**
- **Mô tả:**  
  Quản trị viên quản lý tài khoản, cấu hình hệ thống, và giám sát hoạt động.  
- **Liên hệ cơ chế:**  
  - **Phát hiện lỗi:** Sử dụng Prometheus để theo dõi nhật ký và phát hiện bất thường.  
  - **Bảo mật:** Kiểm tra quyền truy cập trước khi thực hiện thay đổi cấu hình.  
- **Ví dụ:**  
  Quản trị viên khóa tài khoản vi phạm và theo dõi các hoạt động hệ thống trong thời gian thực.

---

#### **Ca sử dụng 5: Xử lý thanh toán**
- **Mô tả:**  
  Học sinh hoặc phụ huynh thanh toán học phí qua hệ thống.  
- **Liên hệ cơ chế:**  
  - **Quản lý giao dịch:** Đảm bảo giao dịch thành công trước khi cấp quyền tham gia khóa học.  
  - **Phát hiện lỗi:** Hiển thị cảnh báo nếu giao dịch thất bại.  
- **Ví dụ:**  
  Phụ huynh thanh toán bằng PayPal và hệ thống xác nhận giao dịch thành công trước khi kích hoạt khóa học.  
