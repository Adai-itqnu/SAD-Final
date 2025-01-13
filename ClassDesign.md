# UI Layer
## Classes:
### LoginUI
- **Attributes:** None
- **Methods:**
  - `displayLoginForm()`: Hiển thị biểu mẫu đăng nhập cho người dùng.
  - `submitLogin()`: Gửi thông tin đăng nhập tới hệ thống xác thực.

### ParentUI
- **Attributes:** None
- **Methods:**
  - `viewParentDashboard()`: Hiển thị bảng điều khiển dành cho phụ huynh.

### TeacherUI
- **Attributes:** None
- **Methods:**
  - `viewTeacherDashboard()`: Hiển thị bảng điều khiển dành cho giáo viên.

### RegistrationUI
- **Attributes:** None
- **Methods:**
  - `displayRegistrationForm()`: Hiển thị biểu mẫu đăng ký cho người dùng mới.
  - `submitRegistration()`: Gửi dữ liệu đăng ký vào hệ thống.

### CourseManagementUI
- **Attributes:** None
- **Methods:**
  - `displayCourseList()`: Hiển thị danh sách các khóa học cho người dùng.
  - `manageCourse()`: Quản lý các hoạt động liên quan đến khóa học như đăng ký.

### NotificationUI
- **Attributes:** None
- **Methods:**
  - `viewNotifications()`: Hiển thị thông báo cho người dùng.

---

# Application Layer
## Classes:
### GroupController
- **Attributes:** None
- **Methods:**
  - `joinGroup(groupId)`: Cho phép người dùng tham gia một nhóm cụ thể.
  - `addLesson(groupId, lessonData)`: Thêm bài học vào một nhóm cụ thể.

### ServiceController
- **Attributes:** None
- **Methods:**
  - `manageServices()`: Điều phối các dịch vụ hệ thống (ví dụ: thông báo, mã hóa).

### DatabaseService
- **Attributes:** None
- **Methods:**
  - `queryData(query)`: Thực hiện truy vấn cơ sở dữ liệu và trả về kết quả.
  - `updateData(updateCommand)`: Cập nhật dữ liệu trong cơ sở dữ liệu.

### EncryptionService
- **Attributes:** None
- **Methods:**
  - `encryptData(data)`: Mã hóa thông tin nhạy cảm.
  - `decryptData(data)`: Giải mã thông tin nhạy cảm.

### NotificationController
- **Attributes:** None
- **Methods:**
  - `createNotification(notificationData)`: Tạo thông báo mới cho người dùng.
  - `deleteNotification(notificationId)`: Xóa một thông báo hiện có.

### LoginController
- **Attributes:** None
- **Methods:**
  - `authenticateUser(credentials)`: Xác thực thông tin đăng nhập của người dùng.

### RegistrationController
- **Attributes:** None
- **Methods:**
  - `registerNewUser(userData)`: Xử lý đăng ký người dùng mới.

---

# Data Layer
## Classes:
### NotificationLogStorage
- **Attributes:**
  - `logs`: Lưu trữ các bản ghi thông báo.
- **Methods:**
  - `saveLog(logData)`: Lưu một bản ghi thông báo mới.
  - `retrieveLog(logId)`: Truy xuất một bản ghi cụ thể bằng ID.

### UserStorage
- **Attributes:**
  - `userData`: Lưu trữ dữ liệu người dùng.
- **Methods:**
  - `saveUser(user)`: Lưu dữ liệu người dùng vào bộ nhớ.
  - `getUser(userId)`: Truy xuất thông tin người dùng bằng ID.

### Group
- **Attributes:**
  - `groupId`: Định danh duy nhất cho nhóm.
  - `groupName`: Tên của nhóm.
- **Methods:**
  - `createGroup(groupData)`: Tạo một nhóm mới.
  - `deleteGroup(groupId)`: Xóa một nhóm.

### Course
- **Attributes:**
  - `courseId`: Định danh duy nhất cho khóa học.
  - `courseName`: Tên của khóa học.
- **Methods:**
  - `addCourse(courseData)`: Thêm một khóa học mới.
  - `removeCourse(courseId)`: Xóa một khóa học.

### Lesson
- **Attributes:**
  - `lessonId`: Định danh duy nhất cho bài học.
  - `lessonTitle`: Tiêu đề của bài học.
- **Methods:**
  - `addLesson(lessonData)`: Thêm nội dung bài học.
  - `deleteLesson(lessonId)`: Xóa một bài học.
