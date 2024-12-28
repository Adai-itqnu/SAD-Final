# Use Case Chi Tiết

## 1. Đăng nhập vào hệ thống (Login to System)
- **Actor**: User, Teacher, Admin.
- **Mục tiêu**: Xác thực người dùng để truy cập hệ thống.
- **Luồng chính**:
  1. Người dùng nhập thông tin đăng nhập.
  2. Hệ thống kiểm tra thông tin qua dịch vụ Authentication.
  3. Nếu hợp lệ, cho phép truy cập giao diện chính.
- **Luồng phụ**:
  - Sai thông tin → Hiển thị lỗi.
  - Tài khoản bị khóa → Hướng dẫn liên hệ quản trị viên.

## 2. Tìm kiếm tài nguyên (Search Resources)
- **Actor**: User.
- **Mục tiêu**: Tra cứu tài liệu học tập.
- **Luồng chính**:
  1. Người dùng nhập từ khóa tìm kiếm.
  2. Hệ thống truy vấn kho tài nguyên.
  3. Hiển thị kết quả phù hợp.
- **Luồng phụ**:
  - Không tìm thấy tài liệu → Gợi ý từ khóa khác.
  - Tài liệu yêu cầu quyền truy cập → Hiển thị thông báo.

## 3. Truy cập dịch vụ (Access Service)
- **Actor**: User.
- **Mục tiêu**: Truy cập vào các ứng dụng năng suất hoặc học tập.
- **Luồng chính**:
  1. Người dùng chọn dịch vụ từ giao diện chính.
  2. Hệ thống kiểm tra quyền truy cập.
  3. Cung cấp quyền truy cập vào dịch vụ.
- **Luồng phụ**:
  - Không có quyền → Hiển thị lỗi.

## 4. Nộp bài tập (Submit Assignment)
- **Actor**: User.
- **Mục tiêu**: Tải bài tập lên hệ thống qua VLE.
- **Luồng chính**:
  1. Người dùng chọn bài tập cần nộp.
  2. Tải tệp bài tập lên.
  3. Xác nhận hoàn tất nộp bài.
- **Luồng phụ**:
  - Sai định dạng tệp → Thông báo lỗi.
  - Tệp vượt dung lượng → Gợi ý nén tệp.

## 5. Tạo nhóm học (Create Learning Group)
- **Actor**: Teacher.
- **Mục tiêu**: Tạo nhóm học mới.
- **Luồng chính**:
  1. Truy cập giao diện quản lý lớp học.
  2. Nhập thông tin nhóm (tên, mô tả, danh sách học sinh).
  3. Xác nhận và lưu nhóm.
- **Luồng phụ**:
  - Trùng tên nhóm → Thông báo lỗi.

## 6. Tham gia nhóm học (Join Learning Group)
- **Actor**: User, Teacher.
- **Mục tiêu**: Tham gia nhóm học qua mã mời hoặc lời mời.
- **Luồng chính**:
  1. Nhập mã nhóm hoặc chấp nhận lời mời.
  2. Hệ thống xác thực quyền và thêm người dùng vào nhóm.
- **Luồng phụ**:
  - Mã nhóm không hợp lệ → Hiển thị lỗi.

## 7. Quản lý nhóm học (Manage Learning Group)
- **Actor**: Teacher.
- **Mục tiêu**: Quản lý danh sách học viên, tài liệu và bài tập trong nhóm học.
- **Luồng chính**:
  1. Chọn nhóm học cần quản lý.
  2. Thực hiện các thao tác:
     - Thêm/xóa học viên.
     - Đăng tài liệu hoặc bài tập.
     - Theo dõi tiến độ học tập.
  3. Lưu thay đổi.
- **Luồng phụ**:
  - Không thể lưu thay đổi → Hiển thị lỗi.

## 8. Cấu hình dịch vụ (Configure Services)
- **Actor**: Admin.
- **Mục tiêu**: Quản trị viên cấu hình hệ thống và dịch vụ.
- **Luồng chính**:
  1. Thay đổi cấu hình dịch vụ (thêm, sửa, xóa).
  2. Lưu và áp dụng cấu hình.
- **Luồng phụ**:
  - Cấu hình không hợp lệ → Hiển thị lỗi.

## 9. Thêm/Thay thế dịch vụ (Add/Replace Service)
- **Actor**: Admin.
- **Mục tiêu**: Thêm mới hoặc thay thế dịch vụ.
- **Luồng chính**:
  1. Chọn dịch vụ cần thêm hoặc thay thế.
  2. Hệ thống kiểm tra tính khả dụng.
  3. Cập nhật cấu hình.
- **Luồng phụ**:
  - Dịch vụ không khả dụng → Hiển thị lỗi.

## 10. Giám sát hệ thống (Monitor System)
- **Actor**: Admin.
- **Mục tiêu**: Theo dõi hoạt động và trạng thái hệ thống.
- **Luồng chính**:
  1. Truy cập giao diện giám sát.
  2. Xem báo cáo và log hệ thống.
  3. Thực hiện xử lý nếu cần thiết.
- **Luồng phụ**:
  - Không truy cập được log → Hiển thị lỗi.
