### Use Case: Đăng nhập vào hệ thống (Login to System)
- **Actor**: Người dùng (User)
- **Mô tả**: Người dùng nhập tài khoản và mật khẩu, xác thực qua dịch vụ Authentication.

#### Luồng chính:
1. Người dùng nhập thông tin.
2. Dịch vụ Authentication kiểm tra thông tin.
3. Nếu hợp lệ, người dùng được chuyển tới giao diện chính.

#### Luồng phụ:
- **Sai thông tin đăng nhập**: Hiển thị thông báo lỗi.

---

### Use Case: Truy cập dịch vụ (Access Services)
- **Actor**: Người dùng (User)
- **Mô tả**: Người dùng truy cập vào các dịch vụ học tập hoặc năng suất.

#### Luồng chính:
1. Người dùng chọn dịch vụ từ giao diện.
2. Hệ thống cung cấp quyền truy cập (nếu được phân quyền).

#### Luồng phụ:
- **Người dùng không có quyền**: Hiển thị thông báo.

---

### Use Case: Cấu hình hệ thống (Configure System)
- **Actor**: Quản trị viên (Admin)
- **Mô tả**: Quản trị viên tùy chỉnh các nhóm người dùng và quyền hạn.

#### Luồng chính:
1. Admin đăng nhập vào giao diện admin.
2. Được phép chỉnh sửa cấu hình nhóm và quyền.
3. Lưu lại thay đổi.

---

### Use Case: Thêm/Thay thế dịch vụ (Add/Replace Services)
- **Actor**: Quản trị viên (Admin)
- **Mô tả**: Cài đặt dịch vụ mới hoặc thay thế dịch vụ cũ.

#### Luồng chính:
1. Admin chọn thêm dịch vụ mới.
2. Hệ thống kiểm tra tính khả dụng.
3. Thêm dịch vụ vào cấu hình.

---

### Use Case: Nộp bài tập (Submit Assignment)
- **Actor**: Người dùng (User)
- **Mô tả**: Học sinh nộp bài tập qua VLE.

#### Luồng chính:
1. Người dùng chọn bài tập cần nộp.
2. Tải tệp lên hệ thống.
3. Xác nhận hoàn tất nộp bài.

## Diagram
![markdown](https://www.planttext.com/plantuml/png/T951JWCn34NtFeMNpABY1gWZXDWKQSG8zY4nmQ9ngjYfrBEnw95w1TIP0KqrxSxnV_woVqu_nxMQArRJ5i1vomNVbCfKjY6n09mxk5ezuDqcHnQqZFr1ZL8parhlIHLxAdlsf7Efhn-93LjLZf98h04Oh4VvCSidnrhettKcjY7Slz9kwppDl66noKHN-o8nziuuozz00uljSC2xaaFrndks0tREVxju6txVFCqCbpTTeM1vsqWDsJoNN7UABqvSf36MMtn79R4gPxdauNe-K-pZyt9WJHBEd_qB003__mC0)
