## 1. Đăng nhập hệ thống
### Mô tả: 
- Người dùng nhập thông tin đăng nhập để xác thực và truy cập vào hệ thống iLearn. Sau khi xác thực thành công, người dùng sẽ được chuyển đến giao diện chính của hệ thống.

Analysis Classes:
1. Entity
   
  a. UserAccount: Lớp này đại diện cho tài khoản người dùng trong hệ thống. Nó chứa thông tin về tên đăng nhập, mật khẩu đã mã hóa và vai trò của người dùng
     - username, passwordHash, role
     - Methods: validateCredentials(), getUserDetails()

3. Boundary
  a. LoginUI: Lớp này đại diện cho giao diện người dùng trong quá trình đăng nhập. Nó hiển thị trang đăng nhập, thu thập thông tin từ người dùng và hiển thị thông báo lỗi khi có sự cố.
     - Methods: displayLoginPage(), captureLoginInput(), displayErrorMessage(), LoginNotification().

4. Control: Lớp này kiểm soát luồng công việc của quá trình đăng nhập. Nó nhận yêu cầu từ giao diện người dùng, xác thực thông tin đăng nhập, tạo token phiên làm việc và ghi lại các lần đăng nhập.
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
---

## Biểu đồ Sequence Diagram
![Login](
https://www.planttext.com/plantuml/png/X9AzJiCm58LtFyLz0LuW0m8X10Z4GYknfeuLMwJNnRskoDo1WOc92QaHGWYaIY2nu0mTNF4UVW9U0INzeN_0wEISSpyVtwzojDEbs91jPopcf0qqkyAmbhQOn2Q74vqgR1unhf6CpYRdlSaX4uO994LvRThbN5kakNGVkSaxf3IU2TDJN31MoM1hUvOQGSFO77XmmmwaAjQGg51U8unlntrC0MNrXqtLbR4AYE1GXRAFG3AKDq0cndJ5iJRdjFuE9Fqxfa3gZn4hDupW89H31Rb_iHNfazra_T7FAATjJAzuPODxfCNvc7w-Xl9UGU8_C6KB5jZQHD4mmJqi1f0VABYGEhW7t0InLdy4vxxWTMjl7Dh13GakP73FbgrfDpCS1pSYkBGLoTLF5eipMiecwGSeWLUi35PpbXSWk493Hoh_Wf3vGHjwrGhmcMtnsVUapUk77zy6DyAbZU7I3r4oaNN52afTV2kuGls7CkcsvGiDMIZlvlfVLs-Y4fYm7O69RMVV0000__y30000)

---

## Biểu đồ Class Diagram

![Login](
https://www.planttext.com/plantuml/png/P95DJWCn38NtEKMMiEWD8jIgLA8Ie8hI0vYCEnEHIGRRAHgXdem5H-8AAEbCwSyoxzd-dftVxvyf2v2arYlhWLbl66bcRKn1j34On4b_T_UbjDOwCLA05ikZ0-RFIDK3S5C4YlxWxC2x2WJdX5KU09vlRejJe-JvzoZWYhXN0_OnrYvibjgOjvWge2EpSjnvw8k_WXg7IHOwIOH5NeOkoQ0FvGkYI4_8_DzHIf-ZkAsp82w6A_my1g7eFP8snXuUOum6GkKFk1VyICWZS8VajdtUQan6289hP7OnlCPtpA1i-5YN_fa8jbtkF-8NmLBVvL1hf9spg8r9ulp9xHlWPZMS_0nz8kwLElk-oUHoCNMvw5YoMLvPkVqgc9fYg5Bh_m000F__0m00)



2. Đăng ký tài khoản

### Mô tả:
- Người dùng tạo tài khoản mới để tham gia hệ thống iLearn. Người dùng sẽ cung cấp thông tin cá nhân, bao gồm tên, email, mật khẩu, và các thông tin cần thiết khác. Sau khi thông tin được xác thực và lưu trữ trong cơ sở dữ liệu, người dùng sẽ nhận thông báo thành công và có thể tiếp tục sử dụng hệ thống.

Analysis Classes:
1. Entity:
   a. UserAccount: Đại diện cho tài khoản người dùng với các thông tin cơ bản như tên, email, mật khẩu được mã hóa và vai trò trong hệ thống.
     - name, email, passwordHash, role
     - Methods: validateCredentials(), getUserDetails()
    b. DatabaseService: Quản lý việc lưu trữ thông tin người dùng vào cơ sở dữ liệu.
    - Methods: saveUser(user: User), checkUserExists(email: String)
2. Boundary:
   a. RegistrationUI:  Đại diện cho giao diện người dùng để đăng ký tài khoản mới.
   - Methods: displayRegistrationPage(), captureRegistrationInput(), displayErrorMessage(), displaySuccessMessage().
3. Control:
   a.RegistrationController: Quản lý luồng xử lý của quá trình đăng ký tài khoản.
   - Methods: handleRegistrationRequest(), validateUserData(), saveUserAccount(), sendConfirmationEmail().

Responsibility:
1. RegistrationUI: Giao diện đăng ký tài khoản mới
2. RegistrationController: Xử lý luồng công việc trong quá trình đăng ký
3. UserAccount: Đại diện cho tài khoản người dùng và lưu trữ thông tin xác thực và thông tin đăng nhập
4. DatabaseService: Quản lý việc lưu trữ thông tin người dùng vào cơ sở dữ liệu và kiểm tra sự tồn tại của người dùng
---
- Squence Diagram
  ![](
https://www.planttext.com/plantuml/png/h9I_Rjim4CPtFiMDCf2yW8OYHHEq7PgXJO2kDCMAX6ag84z6CsV8qCdeqAbe3KyjODH3bue8EiZmU_09yWe1QRULPJb_a0hGGjnztzsFTxnslmyiKeFbK17Ai31mQhaX_QBK6JNdy9hdqgAXA0jz-fAmGgCfrCRnizMPuePmZHBFeyHJnefIuv-ZGugqJor_myr8Cav8Y87z9os355vvzmNGK9t3Ohouq3aCwYko6HNoGduABwHt5nfGUFS1tXLcs4pQPN4iV3Kx0nJrJvq3Ijr8WWJhxteF-91AjGT3NyqG1i9NtyfUHnNT759uxjrCTZiGqfrqczo8AfbHvA6ZG3Bf4QeG3htx0KfwTrd2OEKbl9kUWVBkaW303i4kA1iabNUVv9P04_oQeVBLfDaduShoZRhkNL1hGb9WWhD1S3jwBotQ95v9Bwg4ve_pvToxpnAo-bSSbdeAwDr73HYAYd7XQ-d2_YsSZuB5Rgd7q8IaMtpLq3rGn_R3DKzOJ8caMn2OMCxfVwAm7gY7SMXiVWedlfeKi1XxDvQ0eT2fpfiXa0XgHMl9xZRPcXHBHt4raj9oyq_X8Js_hISCT22jGItdPPZfhre02n0UEm3h_UZN4SVVf-PEY-OKd3GqjXAvpaZu3xZEmaj-0m00__y30000)
  

---
- CLass Diagram:
  ![diagram](https://planttext.com/plantuml/png/V59BRi8m4Dtd55w61HT04QBGI6LHgG9nWAaz3LOTEvqPqwAAatNH8_KALKW0XtwMypxsUsD_VNpEM80arYxJ3fZL2YlBGY0s-CrI5SKyH6-0zjEfUi-KKiPous2VwXwWmdpKaXeQYOGfkVHDb8xjhILHe7jaFjjwOXsrHkOBTSX-IRK8NYWuXwIAeXzEuRRWZHjSlyANYDm7s86p1WGtZ7GB0XtAi3iYDrg7w7ifepUBu9yirSTpoXgiIoCb3bKKfHShvnrvg76YraBML-sChJa56c1-3MJkWBSfJi4DZAV02qA3NYmupaSJDG_18VXMKQ4Ssw20xSXslCHiQpu2unffPpN-Y7egdqT6wip32_GMzNCBbs-MXVD1bqHwoBBiwlECnzC_NcwWJ1wqTIIB_KzsLIoReJUnTjy0003__mC0)
  
