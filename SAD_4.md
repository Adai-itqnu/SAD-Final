### Thiết kế hệ thống con cho iLearn

#### **1. Hệ thống con quản lý người dùng (User Management Subsystem)**

- **Chức năng**:
  - Quản lý thông tin tài khoản (tạo, sửa, xóa).
  - Xác thực người dùng (login, logout, MFA).
  - Phân quyền theo vai trò (học sinh, giáo viên, quản trị viên).

- **Thành phần**:
  - **Authentication Service**: Xử lý xác thực bằng OAuth 2.0 và JWT.
  - **User Profile Management**: Lưu trữ và xử lý thông tin người dùng (họ tên, email, vai trò).
  - **Role-Based Access Control (RBAC)**: Kiểm soát quyền hạn truy cập.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Users`**:
      - Cột: `UserID`, `Email`, `PasswordHash`, `Role`, `Status`, `CreatedAt`, `UpdatedAt`.
    - **Bảng `Roles`**:
      - Cột: `RoleID`, `RoleName`, `Description`.
    - **Bảng `Permissions`**:
      - Cột: `PermissionID`, `RoleID`, `ServiceAccess`.

  - API:
    - POST `/api/auth/login`: Xác thực và trả JWT.
    - GET `/api/users/{id}`: Lấy thông tin người dùng.
    - PUT `/api/users/{id}`: Cập nhật thông tin người dùng.

#### **2. Hệ thống con quản lý khóa học (Course Management Subsystem)**

- **Chức năng**:
  - Tạo, sửa, xóa khóa học.
  - Quản lý tài liệu học tập và bài tập.
  - Gán học viên và giáo viên vào khóa học.

- **Thành phần**:
  - **Course Service**: Quản lý thông tin khóa học và logic liên quan.
  - **Resource Manager**: Quản lý tài liệu và bài tập.
  - **Enrollment Manager**: Quản lý danh sách học viên và giáo viên.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Courses`**:
      - Cột: `CourseID`, `Name`, `Description`, `TeacherID`, `CreatedAt`.
    - **Bảng `Enrollments`**:
      - Cột: `EnrollmentID`, `CourseID`, `UserID`, `Role` (Student/Teacher).
    - **Bảng `Resources`**:
      - Cột: `ResourceID`, `CourseID`, `FilePath`, `UploadedAt`.

  - API:
    - POST `/api/courses`: Tạo khóa học mới.
    - GET `/api/courses/{id}`: Lấy thông tin khóa học.
    - POST `/api/courses/{id}/enroll`: Gán học viên/giáo viên vào khóa học.

#### **3. Hệ thống con thông báo (Notification Subsystem)**

- **Chức năng**:
  - Gửi thông báo sự kiện (qua email, giao diện, ứng dụng di động).
  - Tích hợp với hệ thống định tuyến tin nhắn (RabbitMQ/Kafka).

- **Thành phần**:
  - **Notification Scheduler**: Lập lịch gửi thông báo.
  - **Message Queue**: Hàng đợi tin nhắn xử lý đồng thời.
  - **Delivery Service**: Gửi thông báo đến người dùng qua email hoặc API.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Notifications`**:
      - Cột: `NotificationID`, `UserID`, `Message`, `Type`, `CreatedAt`, `Status`.

  - API:
    - POST `/api/notifications`: Tạo thông báo mới.
    - GET `/api/notifications/user/{id}`: Lấy danh sách thông báo của người dùng.

#### **4. Hệ thống con quản lý tài liệu (Document Management Subsystem)**

- **Chức năng**:
  - Lưu trữ và phân phối tài liệu học tập.
  - Hỗ trợ tải lên, chỉnh sửa, xóa tài liệu.

- **Thành phần**:
  - **Storage Service**: Lưu trữ tài liệu trên nền tảng đám mây (AWS S3, Azure Blob).
  - **Document Manager**: Quản lý metadata và quyền truy cập tài liệu.
  - **File Uploader**: Xử lý tải lên, kiểm tra định dạng.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Documents`**:
      - Cột: `DocumentID`, `UploaderID`, `CourseID`, `FileName`, `FilePath`, `UploadedAt`.

  - API:
    - POST `/api/documents/upload`: Tải tài liệu lên hệ thống.
    - GET `/api/documents/course/{id}`: Lấy danh sách tài liệu của khóa học.

#### **5. Hệ thống con thanh toán (Payment Subsystem)**

- **Chức năng**:
  - Xử lý thanh toán học phí.
  - Quản lý trạng thái giao dịch.

- **Thành phần**:
  - **Payment Gateway**: Tích hợp với Stripe hoặc PayPal.
  - **Transaction Manager**: Đảm bảo tính toàn vẹn giao dịch (ACID).
  - **Invoice Generator**: Tạo hóa đơn và lưu trữ lịch sử thanh toán.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Transactions`**:
      - Cột: `TransactionID`, `UserID`, `Amount`, `Status`, `CreatedAt`.

  - API:
    - POST `/api/payments`: Tạo giao dịch thanh toán mới.
    - GET `/api/payments/user/{id}`: Lấy lịch sử thanh toán của người dùng.

#### **6. Hệ thống con bảo mật (Security Subsystem)**

- **Chức năng**:
  - Bảo vệ dữ liệu và hệ thống khỏi các cuộc tấn công.
  - Mã hóa dữ liệu nhạy cảm.

- **Thành phần**:
  - **Authentication Service**: Quản lý phiên đăng nhập với JWT.
  - **Encryption Manager**: Mã hóa dữ liệu (AES-256).
  - **Firewall**: Tường lửa ứng dụng ngăn SQL Injection, XSS, CSRF.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Sessions`**:
      - Cột: `SessionID`, `UserID`, `Token`, `CreatedAt`, `ExpiresAt`.

  - API:
    - POST `/api/auth/refresh-token`: Cấp token mới khi hết hạn.
    - POST `/api/security/verify`: Xác minh tính hợp lệ của token.

---
