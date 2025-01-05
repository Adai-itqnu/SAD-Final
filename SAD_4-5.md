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

### Sequence Diagram
![](https://www.planttext.com/plantuml/png/R9B1IiD048Rl-nH3Jmhs1NAGDeqe229Q7s2RBCbYEecRIQJ7qgCNFNaIMagF1H4lxXuyfFWU-mI-Wcp4qgZNdVd_-VwV_JJllOAuedASCXvIfg1p5dyyM_Ca8QhVCEu0B-2g48hbN94CPSwHeDClAH58CkGaCuHBeIePYcRPZThB0IS-uiNtEF3Rmmk_FsZftGDZxYHq3nit3uwjMKkWf7x564WYR1usCum14wlNEUmTZRbC3-2S5yLjfg9zvcHE7lWU35KvWShg5UuwO2ic2tpeRiyDbTLBgAoPxYgedakuJZAhbyWOJmaszxiKbDHpJ21q0WO0ZPc3S8ayE9NMpCP0YaF59P2gNtv3E57JntyaD-N4cYb2OlK2M_wkAmy6Lg_oxHQvqA7ZOY8jn1zKgrS48wiNyX-h4uVgshBcxgU1KRt88BNcKJA14MCzWP7xDLy0003__mC0)

### Class Diagram
![](https://www.planttext.com/plantuml/png/b5EzJiCm4Dxz5ATEAMegM3EWIXG92H61P5LTZyIohSPsbTY82dNYMJeoiP61WIV94_0AgFbnsXG69ilVVNVtVNVsT_avAopcrgcC91aM1SJS6JbtciCB0G2uGuz48BMjmMk5CekWiBdKlANPMu7k1Winm1SeQMxwN9gZvbIWFEB573SKJGGfMcQbOXwzmdKiq0uYAMeU2rm7x53A15IZemF64JmQa_cKfKCRZ2DuCZ8bMz9wRYHwmoUAcUwWGsU6uX70KJ-u3TE1mlgi2vpqgaE-LK-iWRbCnCBHtErT--8-jmalCQ729MsDv-RsZpbODDIic0vqlrY_u_5VNUz5Qm-QlYl95CsnrHgemJEPG5gd3GLi2UbVsEXY165O7zs0awztqgwZYvvFfsUZPcuH9DN7RasE1n66bxs128ggV8EqAdUQ_qBqcpnXzGxtlBRVIbRbgmAR8o4pfjFzH_a1003__mC0)
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
### **Thiết kế các lớp**

![](https://www.planttext.com/plantuml/png/b5LDQnf16BxxAuOzjG43kIwX1BKOY9461x77HUtEW3iRrjb2QNi8EPQ2FPJIGy559218IvDBPmWvZFH_lB-WVw7igZipxXh8qUTzzfdd_VIVV3WPSo_YSJ2gz4VUU8pQ_jzV87_GXlh3VFI-Wb0LdQkP1Rk8Cfv5i5em5urvH9cV0Iy3ZuuifEjH7AdV1eRGQhAwPdwRW5XUFdlkehSX7HY1NWnYpgr0FQLc7t1Cr1tpCMKvuMDbOxv9LH9sgLgmp3b2TG9Y7jJKb5fg5p686Mkf-pEYRhrJa9_xHR4Cxb16DbfjaDyl2rAzOR2QK93NGL51g-j2QiokeeaRrJjNTnZ4pC8Q7YCTbVH9xj15BJhcnrQJNcHSNP5N1EGSH-bthjtbB0zCr2B81UqKjywiI9vbBGRvbUwaQO16dYHziqazLWFnawyc86vY5mqyFkGq6Evmpa0yfCqM_HsApgcOo5EgWv1XmyfOFrsIhah2kaf28zSDOYHArI9UJK1UMOrB9uWsudI1Z6N0899mgr5yBv_LDb6tWR6HwKzxXZQGyI8cQih8fbRxgf2rtc0McbyMCzVa6uv0phIrrseHrzUztThhWfYpOaLm129XFYOgeSMYv3gMeoO5CQCNyRkqIKMASGoyi07oKvzePnhJrZeWls0AyegvwCqezFZZpdeWborrZud720vLOfVhD5HJjbOhEbfVhhJLsf76jAEoEQdcevvTmPBHHwW9Sacre6d0Fkl77whc6fL5y-sf65VCENBGGRMAdAF3mmDdnq4fpp6VCI-5ynHAoMlv6ff2DcLdSnwLqrEyNyyOgFqaeyVxIIT3DaZ_Sly3003__mC0)
