# Đề xuất kiến trúc phân lớp (N-tier)

## Lý do lựa chọn:
Kiến trúc phân lớp tách biệt các chức năng rõ ràng giữa các lớp, từ giao diện người dùng, logic ứng dụng, nghiệp vụ đến dữ liệu. Cụ thể:
- **Lớp Giao diện người dùng (Presentation Layer)**: Chịu trách nhiệm hiển thị thông tin và giao tiếp với người dùng.
- **Lớp Logic ứng dụng (Application Layer)**: Xử lý các yêu cầu từ người dùng và chuyển giao đến các lớp phù hợp.
- **Lớp Dịch vụ (Business Logic Layer)**: Chứa các quy tắc nghiệp vụ chính, chẳng hạn như xác thực và quản lý khóa học.
- **Lớp Dữ liệu (Data Layer)**: Quản lý việc lưu trữ và truy xuất dữ liệu từ cơ sở dữ liệu.

---

## Các thành phần trong kiến trúc phân lớp

### 1. Lớp Giao diện người dùng (Presentation Layer):
Các thành phần trong lớp này bao gồm giao diện người dùng (UI) và các chức năng tương tác với người dùng.

#### Cơ chế cần giải quyết:
- **Giao diện người dùng thân thiện**: Tạo các trang giao diện đẹp mắt và dễ sử dụng, ví dụ: trang đăng nhập, trang tìm kiếm khóa học, trang quản lý tài liệu học tập.
- **Tìm kiếm và lọc**: Cho phép người dùng tìm kiếm khóa học, tài liệu học tập hoặc sinh viên.
- **Đăng nhập và đăng ký**: Cung cấp giao diện đăng nhập, đăng ký tài khoản cho sinh viên và giảng viên.
- **Quản lý người dùng**: Giao diện cho phép admin quản lý tài khoản người dùng, phân quyền cho sinh viên và giảng viên.

### 2. Lớp Logic ứng dụng (Application Layer):
Lớp này chịu trách nhiệm xử lý các yêu cầu từ lớp giao diện người dùng và chuyển giao các yêu cầu này đến lớp dịch vụ phù hợp. Lớp này đóng vai trò như cầu nối giữa UI và lớp dịch vụ.

#### Cơ chế cần giải quyết:
- **Xử lý yêu cầu đăng ký khóa học**: Xử lý các yêu cầu từ người dùng để đăng ký vào khóa học.
- **Quản lý tài liệu học tập**: Tạo, chỉnh sửa và xóa tài liệu học tập.
- **Gửi thông báo**: Gửi thông báo đến người dùng khi có tài liệu mới hoặc thay đổi trong khóa học.
- **Xử lý đăng nhập và phân quyền**: Xử lý các yêu cầu xác thực người dùng và phân quyền người dùng (admin, giảng viên, sinh viên).

### 3. Lớp Dịch vụ (Business Logic Layer):
Lớp này chứa tất cả các quy tắc nghiệp vụ chính của hệ thống, ví dụ như xác thực người dùng, quản lý khóa học, xử lý các hoạt động của sinh viên, và các tác vụ học tập khác.

#### Cơ chế cần giải quyết:
- **Quản lý đăng ký và hủy đăng ký khóa học**: Thực hiện quy trình đăng ký và hủy đăng ký khóa học cho sinh viên.
- **Xử lý quy trình học tập**: Bao gồm tạo lớp học, gửi tài liệu học tập, theo dõi tiến trình học tập của sinh viên.
- **Quản lý người dùng**: Xác thực người dùng, phân quyền và xử lý các yêu cầu từ sinh viên và giảng viên.
- **Thông báo và nhắc nhở**: Gửi thông báo, nhắc nhở về các bài tập, kỳ thi, hoặc tài liệu học tập mới.

### 4. Lớp Dữ liệu (Data Layer):
Lớp này quản lý việc lưu trữ và truy xuất dữ liệu từ cơ sở dữ liệu. Đây là nơi mà các dữ liệu quan trọng của hệ thống như thông tin người dùng, khóa học, bài tập, tài liệu được lưu trữ và truy cập.

#### Cơ chế cần giải quyết:
- **Quản lý kết nối cơ sở dữ liệu**: Cung cấp các phương thức kết nối và đóng kết nối cơ sở dữ liệu.
- **Quản lý truy vấn dữ liệu**: Thực hiện các thao tác CRUD (Create, Read, Update, Delete) đối với dữ liệu người dùng, khóa học, bài tập.
- **Bảo mật dữ liệu**: Đảm bảo rằng dữ liệu nhạy cảm như mật khẩu người dùng được mã hóa và bảo vệ.
- **Tối ưu hóa hiệu suất**: Sử dụng các chỉ mục (indexes) và các phương pháp tối ưu hóa truy vấn để đảm bảo hệ thống hoạt động hiệu quả.

### 5. Lớp Bảo mật (Security Layer):
Lớp bảo mật đảm bảo rằng chỉ những người dùng hợp lệ mới có thể truy cập vào các dịch vụ và dữ liệu của hệ thống.

#### Cơ chế cần giải quyết:
- **Xác thực người dùng (Authentication)**: Sử dụng các phương thức xác thực mạnh mẽ như JWT, OAuth hoặc xác thực hai yếu tố (2FA) để bảo vệ hệ thống.
- **Phân quyền người dùng (Authorization)**: Cung cấp các cơ chế phân quyền để đảm bảo mỗi người dùng chỉ có quyền truy cập vào các phần của hệ thống mà họ được phép.
- **Bảo mật dữ liệu**: Áp dụng các biện pháp bảo mật như mã hóa dữ liệu khi lưu trữ và truyền tải, bảo vệ dữ liệu khỏi các cuộc tấn công (SQL Injection, XSS, CSRF).
- **Kiểm tra và giám sát**: Giám sát các hành vi đáng ngờ và kiểm tra các lỗ hổng bảo mật định kỳ.

---
