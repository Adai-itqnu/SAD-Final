### 1. đăng nhập
- **LoginController**: Lớp này kiểm soát luồng công việc của quá trình đăng nhập. Nó nhận yêu cầu từ giao diện người dùng, xác thực thông tin đăng nhập, tạo token phiên làm việc và ghi lại các lần đăng nhập.
  - **Methods**: handleLoginRequest(), verifyUser(), createSessionToken(), logLoginAttempt()
- **EncryptionService**: Cung cấp các phương thức để mã hóa và kiểm tra mật khẩu an toàn.
  - **Methods**: hashPassword(password), verifyPassword(password, hash)
----
### 2. đăng ký

- **RegistrationController**: Quản lý luồng xử lý của quá trình đăng ký tài khoản.
  - **Methods**: handleRegistrationRequest(), validateUserData(), saveUserAccount(), sendConfirmationEmail()
----
### 3. Học viên tham gia khóa học
**Controller**
  - **Method**: validateInput(), saveCourse(), listCourses(), notifyStatus()
----
### 4. Giáo viên thêm bài học mới
- **Controller**
  - **Attributes**: title: String
  - **Methods**: validateInput(), saveLesson(), addLesson(), notifyStatus()
----
### 5: Gửi thông báo đến học viên
  #### a. **NotificationController**  
- **Mô tả**: Điều phối các tác vụ liên quan đến việc gửi thông báo, xác thực người nhận, và lưu thông tin thông báo.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `sendNotification()`  
  - `validateRecipients()`  
  - `saveNotification()`  
  - `logNotification()`
----
### 6: Tạo nhóm học tập
#### a. **GroupController**  
- **Mô tả**: Điều phối các tương tác giữa giáo viên, hệ thống iLearn, cơ sở dữ liệu và các dịch vụ thông báo.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `createGroup(groupDetails)`  
  - `inviteMembers(memberList)`  
  - `handleErrors(errorType)`  

---
### 7. Tham gia nhóm học tập  
- **GroupJoinController**: Điều phối tương tác giữa người dùng, hệ thống iLearn, và các dịch vụ backend.  
  - **Thuộc tính**: *(không có trong mô tả)*  
  - **Phương thức**:  
    - `verifyJoinCode(code)`  
    - `addUserToGroup(userID, groupID)`  
    - `notifyGroupMembers(groupID, userID)`
----
### 8. Phụ huynh theo dõi tiến độ học tập của học sinh  '
- **ProgressController**: Điều phối truy vấn dữ liệu tiến độ học tập và giao tiếp với các lớp khác.  
  - **Phương thức**:  
    - `fetchStudentProgress(studentID)`  
    - `generateReport(studentID)`  
    - `sendMessageToTeacher(teacherID, message)`  

---
### 9. Cấu hình dịch vụ
- **ServiceController**: Quản lý các yêu cầu cấu hình dịch vụ.  
  - **Phương thức**:  
    - `getServiceList()`  
    - `updateServiceConfiguration(serviceID, options)`  

---
