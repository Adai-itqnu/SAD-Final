# Phụ huynh theo dõi tiến độ học tập của học sinh  

## Các lớp phân tích  

### 1. Entity  
- **Student**: Đại diện cho học sinh trong hệ thống.  
  - **Thuộc tính**:  
    - `studentID`  
    - `name`  
    - `progress` (Điểm số, bài tập, tình trạng tham gia)  
  - **Phương thức**:  
    - `getProgress()`  
- **Parent**: Đại diện cho phụ huynh trong hệ thống.  
  - **Thuộc tính**:  
    - `parentID`  
    - `children` (Danh sách học sinh)  
  - **Phương thức**:  
    - `viewChildProgress(studentID)`  
- **Teacher**: Đại diện cho giáo viên cung cấp nhận xét.  
  - **Thuộc tính**:  
    - `teacherID`  
    - `name`  
  - **Phương thức**:  
    - `addComment(studentID, comment)`  

### 2. Boundary  
- **ParentUI**: Giao diện cho phép phụ huynh theo dõi tiến độ học tập.  
  - **Phương thức**:  
    - `displayLogin()`  
    - `displayProgress()`  
    - `downloadReport()`  
    - `contactTeacher()`  

### 3. Control  
- **ProgressController**: Điều phối truy vấn dữ liệu tiến độ học tập và giao tiếp với các lớp khác.  
  - **Phương thức**:  
    - `fetchStudentProgress(studentID)`  
    - `generateReport(studentID)`  
    - `sendMessageToTeacher(teacherID, message)`  

---

## Responsibility  

### 1. ParentUI:  
- Hiển thị giao diện để phụ huynh theo dõi tiến độ.  
- Cung cấp tùy chọn tải xuống báo cáo hoặc liên hệ giáo viên.  

### 2. ProgressController:  
- Lấy dữ liệu tiến độ từ cơ sở dữ liệu.  
- Xử lý yêu cầu liên hệ giáo viên và tạo báo cáo.  

### 3. Student:  
- Lưu trữ và cung cấp thông tin tiến độ học tập.  

### 4. Teacher:  
- Cung cấp nhận xét và phản hồi.  

---


## Biểu đồ Sequence Diagram  

![Phu huynh theo doi tien do](
https://www.planttext.com/plantuml/png/b9EnQkGm48PxFSMGFY-mHGYak5i88P0Dt9MEhBC4pYZ8ut1RfzZYEBYKrwq98H1Ojaab5ocqBw8do2i4sRfppDfijXnhlfdvVy-yrQ_71IM6okkS9PoqWVF422HsfKjC4pEFyUMKSOraT0xdHcT65CL96-V2C86aQ0uNLAQ1ZU5C95mAmrXR0WwF_XURmERFvWupGEdjwWPktLA3zFK2IFhw7hF8N4uxQW9VbQ_li4dv1Mc24WfNSHd0tnmAXNAmrKbun-siM7nBpWI-k-SIkBTF9P1qBvW1AGHIthuYREvz_PTjOw5OT602fzu-pY7rzHfovUj5sQTZ7XoE330ptZwCuyFDEyKjFZhwBcixaB4a9vXv-w3WobKQkAiqWuZrcvv9RnyHq5a26Y4-PxctbUx3-vhDPR_0_dxlRjyf_-BhbO8VAXVZagFFhPK_osR9FsGBJ5klJvLxRdPr0PaApxVXmoSiFnWc3_RpFckaaCBcCjTDuq7ryRZ_YUyHyMtKxM-kuktbXytSsQhJ-n7i9YNfbYY1XwKTiNrelHlpUspu2SS2q_8wVmS00F__0m00)

---

## Biểu đồ Class Diagram  

![Phu huynh theo doi tien do](
https://www.planttext.com/plantuml/png/Z951JiGm34NtEOMNCulUeAgGogOII2EOEO1fJ5ifZIl7PJH2d8m5H-8Ag6a6MkY2NVpZlF_jVBv_t0H5qR5tfdOO0ZpgQCahv3bvxVHI5Ay6023CUdKRAuyznSCWt0Y548k6z93gtTwycOGye6mHXoWdODrspWhvMBnqT2udOOjs9AnRaWKEPfxE5xyJehKbzprv_PlfL46UF_5eKRvZsIuC3Yztt7H-jrzAYpHHvRDtZFQ11fO93jCSx1LhJI5NZkbroLw5dOiZJEt2xkhzJ5gtwGT-t6nQhYT1fPLT86_lAGHiwCWhqxHqu2o3wwUQZGoGPSK_6X8xOK_L96-CPBu0003__mC0)
