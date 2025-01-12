# Đăng nhập hệ thống

## Mô tả
Người dùng nhập thông tin đăng nhập để xác thực và truy cập vào hệ thống iLearn. Sau khi xác thực thành công, người dùng sẽ được chuyển đến giao diện chính của hệ thống.

---

## Các lớp phân tích

### 1. Thực thể (Entity)
- **UserAccount**: Đại diện cho tài khoản người dùng trong hệ thống.
  - **Thuộc tính**:
    - `username`
    - `passwordHash`
    - `role`
  - **Phương thức**:
    - `validateCredentials()`
    - `getUserDetails()`

### 2. Biên (Boundary)
- **LoginUI**: Giao diện người dùng trong quá trình đăng nhập.
  - **Phương thức**:
    - `displayLoginPage()`
    - `captureLoginInput()`
    - `displayErrorMessage()`
    - `LoginNotification()`

### 3. Điều khiển (Control)
- **LoginController**: Điều phối luồng công việc đăng nhập.
  - **Phương thức**:
    - `handleLoginRequest()`
    - `verifyUser()`
    - `createSessionToken()`
    - `logLoginAttempt()`
- **EncryptionService**: Cung cấp các phương thức mã hóa mật khẩu.
  - **Phương thức**:
    - `hashPassword(password)`
    - `verifyPassword(password, hash)`

---

## Trách nhiệm (Responsibility)

### 1. LoginUI:
- Hiển thị giao diện đăng nhập và thu thập thông tin từ người dùng.
- Thông báo lỗi khi đăng nhập thất bại.

### 2. LoginController:
- Xử lý luồng công việc đăng nhập, bao gồm xác thực thông tin người dùng và tạo phiên làm việc.

### 3. UserAccount:
- Đại diện cho tài khoản người dùng và lưu trữ thông tin xác thực.

### 4. EncryptionService:
- Cung cấp các phương thức để mã hóa và kiểm tra mật khẩu an toàn.

---

## Biểu đồ Sequence Diagram
![Login](
https://www.planttext.com/plantuml/png/X9AzJiCm58LtFyLz0LuW0m8X10Z4GYknfeuLMwJNnRskoDo1WOc92QaHGWYaIY2nu0mTNF4UVW9U0INzeN_0wEISSpyVtwzojDEbs91jPopcf0qqkyAmbhQOn2Q74vqgR1unhf6CpYRdlSaX4uO994LvRThbN5kakNGVkSaxf3IU2TDJN31MoM1hUvOQGSFO77XmmmwaAjQGg51U8unlntrC0MNrXqtLbR4AYE1GXRAFG3AKDq0cndJ5iJRdjFuE9Fqxfa3gZn4hDupW89H31Rb_iHNfazra_T7FAATjJAzuPODxfCNvc7w-Xl9UGU8_C6KB5jZQHD4mmJqi1f0VABYGEhW7t0InLdy4vxxWTMjl7Dh13GakP73FbgrfDpCS1pSYkBGLoTLF5eipMiecwGSeWLUi35PpbXSWk493Hoh_Wf3vGHjwrGhmcMtnsVUapUk77zy6DyAbZU7I3r4oaNN52afTV2kuGls7CkcsvGiDMIZlvlfVLs-Y4fYm7O69RMVV0000__y30000)

---

## Biểu đồ Class Diagram

![Login](
https://www.planttext.com/plantuml/png/P95DJWCn38NtEKMMiEWD8jIgLA8Ie8hI0vYCEnEHIGRRAHgXdem5H-8AAEbCwSyoxzd-dftVxvyf2v2arYlhWLbl66bcRKn1j34On4b_T_UbjDOwCLA05ikZ0-RFIDK3S5C4YlxWxC2x2WJdX5KU09vlRejJe-JvzoZWYhXN0_OnrYvibjgOjvWge2EpSjnvw8k_WXg7IHOwIOH5NeOkoQ0FvGkYI4_8_DzHIf-ZkAsp82w6A_my1g7eFP8snXuUOum6GkKFk1VyICWZS8VajdtUQan6289hP7OnlCPtpA1i-5YN_fa8jbtkF-8NmLBVvL1hf9spg8r9ulp9xHlWPZMS_0nz8kwLElk-oUHoCNMvw5YoMLvPkVqgc9fYg5Bh_m000F__0m00)
