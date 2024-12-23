## Đề xuất kiến trúc phân lớp (N-tier)

#### Lý do lựa chọn:
Kiến trúc phân lớp tách biệt các chức năng rõ ràng giữa các lớp, từ giao diện người dùng, logic ứng dụng, nghiệp vụ đến dữ liệu. Cụ thể:
- **Lớp Giao diện người dùng (Presentation Layer)**: Chịu trách nhiệm hiển thị thông tin và giao tiếp với người dùng.
- **Lớp Logic ứng dụng (Application Layer)**: Xử lý các yêu cầu từ người dùng và chuyển giao đến các lớp phù hợp.
- **Lớp Dịch vụ (Business Logic Layer)**: Chứa các quy tắc nghiệp vụ chính, chẳng hạn như xác thực và quản lý khóa học.
- **Lớp Dữ liệu (Data Layer)**: Quản lý việc lưu trữ và truy xuất dữ liệu từ cơ sở dữ liệu.

---
## Các thành phần trong kiến trúc phân lớp

### 1. Lớp Giao diện người dùng (Presentation Layer):
Các thành phần trong lớp này bao gồm giao diện người dùng (UI) và các chức năng tương tác với người dùng.
- **Cơ chế cần giải quyết**: Cung cấp giao diện thân thiện với người dùng, dễ sử dụng, hỗ trợ các tính năng tìm kiếm, đăng nhập, và quản lý người dùng.

### 2. Lớp Logic ứng dụng (Application Layer):
Lớp này chịu trách nhiệm xử lý các yêu cầu từ lớp giao diện người dùng và chuyển giao các yêu cầu này đến lớp dịch vụ phù hợp. Lớp này đóng vai trò như cầu nối giữa UI và lớp dịch vụ.
- **Cơ chế cần giải quyết**: Xử lý các yêu cầu từ người dùng, như đăng ký khóa học, quản lý tài liệu học tập, gửi thông báo, v.v.

### 3. Lớp Dịch vụ (Business Logic Layer):
Lớp này chứa tất cả các quy tắc nghiệp vụ chính của hệ thống, ví dụ như xác thực người dùng, quản lý khóa học, xử lý các hoạt động của sinh viên, và các tác vụ học tập khác.
- **Cơ chế cần giải quyết**: Quản lý quy trình đăng nhập, phân quyền người dùng, xử lý các hoạt động học tập như tạo lớp học, gửi tài liệu, thông báo, v.v.

### 4. Lớp Dữ liệu (Data Layer):
Lớp này quản lý việc lưu trữ và truy xuất dữ liệu từ cơ sở dữ liệu. Đây là nơi mà các dữ liệu quan trọng của hệ thống như thông tin người dùng, khóa học, bài tập, tài liệu được lưu trữ và truy cập.
- **Cơ chế cần giải quyết**: Quản lý kết nối cơ sở dữ liệu, truy vấn và thao tác với dữ liệu, đảm bảo tính toàn vẹn và bảo mật của dữ liệu.

### 5. Lớp Bảo mật (Security Layer):
Lớp bảo mật đảm bảo rằng chỉ những người dùng hợp lệ mới có thể truy cập vào các dịch vụ và dữ liệu của hệ thống.
- **Cơ chế cần giải quyết**: Cung cấp các cơ chế xác thực và phân quyền người dùng, bảo vệ dữ liệu khỏi truy cập trái phép và đảm bảo bảo mật thông tin người dùng.

