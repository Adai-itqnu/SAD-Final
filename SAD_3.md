### Các phần tử thiết kế trong hệ thống iLearn

#### **1. Phần tử giao diện người dùng (UI Components)**
- **Trang đăng nhập và xác thực**: 
  - Thành phần: Form nhập thông tin (email/password), nút đăng nhập, liên kết quên mật khẩu.
  - Giao diện thân thiện, hỗ trợ xác thực qua OAuth 2.0 hoặc SSO.
  
- **Dashboard chính**:
  - Thành phần: Menu bên trái (dành cho các mục như tài liệu, khóa học, thông báo), khu vực hiển thị chính, bảng điều khiển thông báo.
  - Hỗ trợ tùy chỉnh giao diện theo nhóm người dùng (học sinh, giáo viên, quản trị viên).

- **Trang khóa học**:
  - Thành phần: Danh sách khóa học, nút thêm/sửa/xóa khóa học, nút tải tài liệu.
  - Hỗ trợ hiển thị lịch học, bài tập, và nội dung khóa học.

- **Trang quản trị**:
  - Thành phần: Bảng điều khiển quản lý tài khoản, danh sách học sinh/giáo viên, công cụ thống kê.
  - Giao diện quản trị cho phép thiết lập cấu hình hệ thống.

#### **2. Phần tử logic nghiệp vụ (Business Logic Components)**
- **Xác thực và quản lý quyền**:
  - Thành phần: Module xác thực dựa trên JWT, phân quyền dựa trên vai trò (học sinh, giáo viên, quản trị viên).
  - Chức năng kiểm tra quyền truy cập theo từng nhóm người dùng.

- **Quản lý khóa học**:
  - Thành phần: API xử lý logic tạo, sửa, xóa khóa học.
  - Tự động gán tài liệu, bài tập khi thêm khóa học mới.

- **Thông báo và nhắc nhở**:
  - Thành phần: Hệ thống gửi thông báo qua email, giao diện, hoặc ứng dụng di động.
  - Tích hợp cơ chế định tuyến tin nhắn với RabbitMQ hoặc Kafka.

- **Hỗ trợ thanh toán**:
  - Thành phần: Module xử lý giao dịch qua Stripe hoặc PayPal.
  - Tích hợp logic đảm bảo tính toàn vẹn giao dịch (ACID).

#### **3. Phần tử dữ liệu (Data Components)**
- **Cơ sở dữ liệu người dùng**:
  - Thành phần: Bảng người dùng với thông tin cá nhân, quyền hạn, lịch sử hoạt động.
  - Dữ liệu mã hóa (AES-256) đảm bảo an toàn.

- **Cơ sở dữ liệu khóa học**:
  - Thành phần: Bảng lưu thông tin khóa học, tài liệu, danh sách học viên.
  - Hỗ trợ tìm kiếm và phân loại khóa học.

- **Cơ sở dữ liệu nhật ký**:
  - Thành phần: Ghi nhận nhật ký hoạt động, thay đổi tài liệu, lịch sử đăng nhập.
  - Phục vụ mục đích giám sát và xử lý lỗi.

#### **4. Phần tử tích hợp và tương tác (Integration Components)**
- **Tích hợp dịch vụ bên ngoài**:
  - Thành phần: API kết nối với Google Drive, Zoom, Microsoft Teams.
  - Hỗ trợ tích hợp với hệ thống quản lý mạng trường học hiện có.

- **Hệ thống hàng đợi tin nhắn**:
  - Thành phần: RabbitMQ hoặc Kafka để xử lý thông báo hoặc các yêu cầu giao tiếp giữa các dịch vụ.

#### **5. Phần tử bảo mật (Security Components)**
- **Xác thực**:
  - Thành phần: OAuth 2.0, quản lý phiên đăng nhập với JWT.
  - Cơ chế kiểm tra đa yếu tố (MFA) để tăng cường bảo mật.

- **Kiểm soát truy cập**:
  - Thành phần: Module quản lý vai trò và quyền hạn dựa trên Role-Based Access Control (RBAC).

- **Mã hóa dữ liệu**:
  - Thành phần: Module mã hóa mật khẩu và dữ liệu nhạy cảm.

#### **6. Phần tử hiệu năng và mở rộng (Performance & Scalability Components)**
- **Hệ thống cân bằng tải**:
  - Thành phần: NGINX hoặc HAProxy để phân phối tải khi số lượng người dùng tăng cao.

- **Khả năng mở rộng**:
  - Thành phần: Hỗ trợ triển khai trên đám mây (AWS, Azure).
  - Module quản lý tài nguyên để thêm bớt máy chủ tự động.

- **Cơ chế giám sát**:
  - Thành phần: Công cụ như Prometheus hoặc New Relic để theo dõi hiệu năng hệ thống.

#### **7. Phần tử giao diện cũ (Legacy Interface Components)**
- **Thiết kế tương thích**:
  - Thành phần: Giao diện tối giản để hỗ trợ người dùng thiết bị cũ.
  - Module kiểm tra khả năng tương thích trình duyệt.

- **Hỗ trợ nhập liệu từ hệ thống cũ**:
  - Thành phần: Công cụ nhập và chuyển đổi dữ liệu từ hệ thống Glow.

#### **8. Phần tử xử lý lỗi (Error Handling Components)**
- **Phát hiện lỗi**:
  - Thành phần: Module giám sát và gửi cảnh báo khi phát hiện lỗi hệ thống.

- **Xử lý lỗi người dùng**:
  - Thành phần: Hiển thị thông báo lỗi rõ ràng và gợi ý cách khắc phục.

