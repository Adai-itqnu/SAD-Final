## 1. Đăng nhập hệ thống
### Mô tả: 
- Người dùng nhập thông tin đăng nhập để xác thực và truy cập vào hệ thống iLearn. Sau khi xác thực thành công, người dùng sẽ được chuyển đến giao diện chính của hệ thống.

Analysis Classes:
1. Entity
  a. UserAccount: Lớp này đại diện cho tài khoản người dùng trong hệ thống. Nó chứa thông tin về tên đăng nhập, mật khẩu đã mã hóa và vai trò của người dùng
     - username, passwordHash, role
     - Methods: validateCredentials(), getUserDetails()

2. Boundary
  a. LoginUI: Lớp này đại diện cho giao diện người dùng trong quá trình đăng nhập. Nó hiển thị trang đăng nhập, thu thập thông tin từ người dùng và hiển thị thông báo lỗi khi có sự cố.
     - Methods: displayLoginPage(), captureLoginInput(), displayErrorMessage(), LoginNotification().

3. Control: Lớp này kiểm soát luồng công việc của quá trình đăng nhập. Nó nhận yêu cầu từ giao diện người dùng, xác thực thông tin đăng nhập, tạo token phiên làm việc và ghi lại các lần đăng nhập.
  a. LoginController
     - Methods: handleLoginRequest(), verifyUser(), createSessionToken(), logLoginAttempt()
  b. EncryptionService
     - Methods: hashPassword(password), verifyPassword(password, hash)

Responsibility:
1. LoginUI: Hiển thị giao diện đăng nhập và thu thập thông tin từ người dùng.
2. ErrorNotification: Thông báo lỗi cho người dùng khi đăng nhập thất bại.
3. LoginController: Xử lý luồng công việc đăng nhập, bao gồm xác thực thông tin người dùng và tạo phiên làm việc.
4. UserAccount: Đại diện cho tài khoản người dùng và lưu trữ thông tin xác thực.
5. EncryptionService: Cung cấp các phương thức để mã hóa và kiểm tra mật khẩu an toàn.


Sequence Diagram:


Class diagram 
![](https://planttext.com/plantuml/png/T99RJiCm44N_lGf_9XBTG1L5VL29Ie0gIXSmIgQ9XME7cKbHXBeoFbWIMq3EeuJNf-_SyJqpziVRkrgm04bJMPLPODQtlZ3kiDL9ilADou7QDDMlIckT6wujj9rX1mL6SL0pgAKXxDIjgnlfvS6y8V9qXymNVsUyzsAE9WCntaMnEgjf-Dex8MyjaawIuP2c7K89BhTzrWC-DyX3sWd97Di38mrGX22uHsRZtQD_mf2YjRQ-w9gN8bZLCeqEpSiiyuqJdIGR9qOkapUCvA32kTuB6LS4hGRc5q_v3N0vrSdRRxuJM9E3u9emHoS6B4VnNA-yjmWkE0gK47wD0gOlXkCNsSPbrDPXLNkaaybmkfOUi0GkTmDGD9AD5F4td6vJ_tglkgicdIFdMQdnPyncwS-7wckJXmkUoKR_hF-QIotGvKrbFm400F__0m00)

