# 7. Tham gia nhóm học tập  

## Các lớp phân tích  

### 1. Entity  
- **Group**: Đại diện cho nhóm học tập trong hệ thống.  
  - **Thuộc tính**:  
    - `groupID`  
    - `groupName`  
    - `members`  
  - **Phương thức**:  
    - `getGroupDetails()`  
    - `addMember(userID)`  
- **User**: Đại diện cho thành viên trong nhóm.  
  - **Thuộc tính**:  
    - `userID`  
    - `role` (Student/Teacher)  
  - **Phương thức**:  
    - `getMemberDetails()`  

### 2. Boundary  
- **GroupJoinUI**: Giao diện cho phép người dùng tham gia nhóm học tập.  
  - **Thuộc tính**: *(không có trong mô tả)*  
  - **Phương thức**:  
    - `displayJoinOptions()`  
    - `captureJoinCode()`  
    - `displaySuccessMessage()`  
    - `displayErrorMessage()`  

### 3. Control  
- **GroupJoinController**: Điều phối tương tác giữa người dùng, hệ thống iLearn, và các dịch vụ backend.  
  - **Thuộc tính**: *(không có trong mô tả)*  
  - **Phương thức**:  
    - `verifyJoinCode(code)`  
    - `addUserToGroup(userID, groupID)`  
    - `notifyGroupMembers(groupID, userID)`  

### 4. Utility
- **NotificationService**: Gửi thông báo đến các thành viên trong nhóm về việc tham gia của thành viên mới.  
  - **Thuộc tính**:  
    - `notifications`  
    - `recipientList`  
  - **Phương thức**:  
    - `sendNotification(details)`  
    - `trackNotification()`  

---

## Responsibility 

### 1. GroupJoinUI:  
- Cung cấp giao diện cho người dùng để nhập mã tham gia hoặc chọn nhóm từ danh sách mời.  
- Hiển thị thông báo thành công hoặc lỗi khi tham gia nhóm.  

### 2. GroupJoinController:  
- Xác minh mã tham gia và kiểm tra quyền truy cập.  
- Thêm người dùng vào danh sách thành viên của nhóm.  
- Gửi thông báo đến các thành viên hiện tại và chủ nhóm.  

### 3. Group:  
- Đại diện và lưu trữ thông tin nhóm học tập.  
- Quản lý danh sách thành viên.  

### 4. User:  
- Đại diện và lưu trữ thông tin thành viên trong nhóm.  

### 5. NotificationService:  
- Gửi thông báo đến các thành viên nhóm về việc tham gia của người dùng mới.  

---


## Squence Diagram
![tham gia nhom hoc](https://www.planttext.com/plantuml/png/b9E_Jm8n5CVt_XKlxCQTmP0mu8_88YIkfNVIncjBoeE4sO71E3Wvk4ZOC4owI0U6-e_qB_1VCFKuEF4ESBnt_Rpljz_t-cMNjJvIWmEP4CfG6sZtOqCwUg0YQaRGC7hGEzT2jSy8qmgDJZQrUbf8OaDYXG9NnxEForXsDh-Q6iMDO1I5LbUn6GeM4nB4uEWaBrE5ElVsGK6bnQc4hg2Wk7kJ4AeCq2_clGh90O4FVQfmAhozKu3Sstj0zp42bhPIF50WtVGOiwRexIj4L77ekmdZnLQQQn0oS5kw88qgDBoTYn9iSswDL-4YM9U0XXPGfJANRXfYcVOWyNQyHwB5tKm2SlUYE0o5cocGtZwBFHhNRiBI04EosotAD0kcdQM2tBshBdJSHCFderyi5R2WyQjj0N-Gm-wsnCvGiZ6tSfPMDbYe7B1cNK4rHCBRSLYphJqbX2RuCwNrsjscKhcfGUfbvv1BgNzSBF7sIUIvygVpXufLH6gnYWOo-GO00F__0m00) .

---

## Class Diagram
![Tham gia nhom hoc](
https://www.planttext.com/plantuml/png/V99DRi8m48NtFeMNiCW5gWWXGLMbAdH1EO2nXyYgOqVZCL9KSR8kUgHUeV9F2QIeE_jxutdpR7z_VYqz2QJG6IQDy9u_eGizhskmf6bOB3uOvvotaJRhSRqL7QHT1zq1q6S5A1rV0mbj_6oUg51gaufcStPcnIQJAn-UZO87RDOFV4UeRPiGEWCte0NAnqUVIz_a_-oqtJUyhWykA85ZTwLzRyGGzTUUjBE_CqhHKq28miefABIKxuAKuFq6l1VjH7j4T3WgV-TOEKleZ4bXPTvSvZa1wkCmSHLAxJtWcqiz2hIEz75896U_IRsDgfOYHje1dhG4NjU1jBc-szIZLEK7Gv2wrs3fHNjAn8DLrzsAFQ6GxnD-PgnybghYvK4pcUJcLRNW-KR-qUza6AltJQowTwji2LR5x_i3003__mC0)
