# Use Case Chi Tiết

# Use Case: Đăng nhập vào hệ thống (Login to System)
**Actor**: User, Teacher, Admin  
**Mục tiêu**: Xác thực người dùng để truy cập hệ thống.  
**Luồng chính (Main Flow)**:
1. Người dùng nhập thông tin đăng nhập.
2. Hệ thống kiểm tra thông tin qua dịch vụ Authentication (ví dụ: Google, Facebook).
3. Nếu hợp lệ, cho phép truy cập giao diện chính.

**Luồng phụ (Alternative Flow)**:
- Sai thông tin: Hiển thị lỗi và yêu cầu nhập lại.
- Tài khoản bị khóa: Hiển thị hướng dẫn liên hệ với quản trị viên.

**Trang tài liệu liên quan**: Trang 4, Trang 12

---

# Use Case: Tìm kiếm tài nguyên (Search Resources)
**Actor**: User  
**Mục tiêu**: Tra cứu tài liệu học tập.  
**Luồng chính (Main Flow)**:
1. Người dùng nhập từ khóa tìm kiếm.
2. Hệ thống truy vấn kho tài nguyên.
3. Hiển thị kết quả phù hợp.

**Luồng phụ (Alternative Flow)**:
- Không tìm thấy tài liệu: Gợi ý từ khóa khác.
- Tài liệu yêu cầu quyền truy cập: Hiển thị thông báo lỗi.

**Trang tài liệu liên quan**: Trang 12

---

# Use Case: Truy cập dịch vụ (Access Service)
**Actor**: User  
**Mục tiêu**: Truy cập vào các ứng dụng năng suất hoặc học tập.  
**Luồng chính (Main Flow)**:
1. Người dùng chọn dịch vụ từ giao diện chính (ví dụ: họp video, lưu trữ tài liệu).
2. Hệ thống kiểm tra quyền truy cập.
3. Cung cấp quyền truy cập vào dịch vụ.

**Luồng phụ (Alternative Flow)**:
- Không có quyền: Hiển thị lỗi và thông báo liên hệ quản trị viên.

**Trang tài liệu liên quan**: Trang 12

---

# Use Case: Nộp bài tập (Submit Assignment)
**Actor**: User  
**Mục tiêu**: Tải bài tập lên hệ thống qua VLE (Virtual Learning Environment).  
**Luồng chính (Main Flow)**:
1. Người dùng chọn bài tập cần nộp.
2. Tải tệp bài tập lên.
3. Xác nhận hoàn tất nộp bài.

**Luồng phụ (Alternative Flow)**:
- Sai định dạng tệp: Hiển thị thông báo lỗi và yêu cầu sửa đổi.
- Tệp vượt dung lượng: Gợi ý nén tệp hoặc thay đổi tệp khác.

**Trang tài liệu liên quan**: Trang 4, Trang 12

---

# Use Case: Tạo nhóm học (Create Learning Group)
**Actor**: Teacher  
**Mục tiêu**: Tạo nhóm học mới để tổ chức học tập.  
**Luồng chính (Main Flow)**:
1. Giáo viên truy cập giao diện quản lý lớp học.
2. Nhập thông tin nhóm (tên, mô tả, danh sách học sinh).
3. Xác nhận và lưu nhóm.

**Luồng phụ (Alternative Flow)**:
- Trùng tên nhóm: Hiển thị thông báo lỗi.
- Danh sách học sinh không hợp lệ: Yêu cầu kiểm tra lại thông tin.

**Trang tài liệu liên quan**: Trang 0, Trang 1

---

# Use Case: Tham gia nhóm học (Join Learning Group)
**Actor**: User, Teacher  
**Mục tiêu**: Tham gia nhóm học qua mã mời hoặc lời mời.  
**Luồng chính (Main Flow)**:
1. Người dùng nhập mã nhóm hoặc chấp nhận lời mời.
2. Hệ thống xác thực quyền và thêm người dùng vào nhóm.

**Luồng phụ (Alternative Flow)**:
- Mã nhóm không hợp lệ: Hiển thị lỗi và yêu cầu nhập lại.

**Trang tài liệu liên quan**: Trang 3

---

# Use Case: Quản lý nhóm học (Manage Learning Group)
**Actor**: Teacher  
**Mục tiêu**: Quản lý danh sách học viên, tài liệu và bài tập trong nhóm học.  
**Luồng chính (Main Flow)**:
1. Giáo viên chọn nhóm học cần quản lý.
2. Thực hiện các thao tác:
   - Thêm/xóa học viên.
   - Đăng tài liệu hoặc bài tập.
   - Theo dõi tiến độ học tập.
3. Lưu thay đổi.

**Luồng phụ (Alternative Flow)**:
- Không thể lưu thay đổi: Hiển thị thông báo lỗi.

**Trang tài liệu liên quan**: Trang 9

---

# Use Case: Theo dõi tiến độ học tập (Track Learning Progress)
**Actor**: Teacher, Parent  
**Mục tiêu**: Xem và theo dõi tiến độ học tập của học sinh.  
**Luồng chính (Main Flow)**:
1. Người dùng truy cập giao diện báo cáo.
2. Hệ thống hiển thị tiến độ học tập chi tiết.

**Luồng phụ (Alternative Flow)**:
- Không tìm thấy dữ liệu: Hiển thị thông báo và gợi ý kiểm tra lại.

**Trang tài liệu liên quan**: Trang 4, Trang 6

---

# Use Case: Giám sát hệ thống (Monitor System)
**Actor**: Admin  
**Mục tiêu**: Theo dõi hoạt động và trạng thái hệ thống.  
**Luồng chính (Main Flow)**:
1. Admin truy cập giao diện giám sát.
2. Xem báo cáo và log hệ thống.
3. Thực hiện xử lý nếu cần thiết.

**Luồng phụ (Alternative Flow)**:
- Không truy cập được log: Hiển thị lỗi và gợi ý kiểm tra lại cấu hình.
