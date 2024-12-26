### **Kết quả phân tích từng ca sử dụng**

#### **Ca sử dụng 1: Quản lý người dùng**
- **Mô tả:**  
  Quản lý việc đăng ký, đăng nhập, và quản trị thông tin người dùng (học sinh, giáo viên, quản trị viên).  
- **Liên hệ cơ chế:**  
  - **Bảo mật:** Xác thực bằng OAuth 2.0, phân quyền theo vai trò.  
  - **Phát hiện lỗi:** Hiển thị thông báo khi thông tin đăng nhập sai.  
- **Ví dụ:**  
  Học sinh đăng nhập, cập nhật thông tin cá nhân, và nhận thông báo về khóa học.
- **Biểu đồ**:

  ![diagram](https://www.planttext.com/plantuml/png/P90zZi8m48LxdsAKdYkie5gANOc_2rZEh6qH9iYUx0Ke4H9NWErMegCYGXJc8Za1Lq2400RAUU_JUtfpAWzjpz9nCSc4L9mxIBfLkL3WBPa4f8SX5oaItznF6rOv_DhmJxKzGgaCkflTBwhT7m6xgfn7L2UTM1AYyAYaHqYEo-ECD92fTfjfJNpbsj8RC0xxsXsWjfxHFO2cA0jxO1Esf84jWGeh81FMrzPlIL9Zp-K_DaCXcYNGQdqqTR5ohuZ5buHcR9GGAozmlJb27_Sps4PAB-y_0m00__y30000)
---

#### **Ca sử dụng 2: Quản lý khóa học**
- **Mô tả:**  
  Giáo viên tạo, quản lý khóa học và học sinh đăng ký tham gia.  
- **Liên hệ cơ chế:**  
  - **Cơ chế quản lý giao dịch:** Áp dụng nguyên tắc ACID khi đăng ký hoặc hủy khóa học.  
  - **Kiểm soát tiến trình:** Đồng bộ hóa tài nguyên để tránh xung đột chỉnh sửa.  
- **Ví dụ:**  
  Giáo viên tạo khóa học mới, thêm tài liệu và hệ thống gửi thông báo tự động đến học sinh.

- **Biểu đồ**:

  ![diagram](https://www.planttext.com/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aOAIU-RXXVaAPPc7L-KfAIGMAuIa9YPdf1R1f3qUxkvDLYZEpCi0omQNbAQavfLmSPKMfoOd5gSgA8KytBKmNo4xu_3cH8KCa6AmEkUYrCIILEVyqgBYL8JQ8nEEDEUbAsGVtekXmJMlA3yd1rs3nyFTooinrBeKvHT0LN91dQkWgsk7QYdKfM095CEH9P1CSaZDIm452m000F__0m00)
  
---

#### **Ca sử dụng 3: Học tập và tương tác**
- **Mô tả:**  
  Học sinh tham gia học tập, tải tài liệu, nộp bài tập, và tương tác với giáo viên.  
- **Liên hệ cơ chế:**  
  - **Cơ chế định tuyến tin nhắn:** Gửi thông báo tự động về bài tập hoặc tài liệu mới.  
  - **Tính bền vững:** Hỗ trợ nhiều người dùng đồng thời truy cập tài liệu trong mùa thi.  
- **Ví dụ:**  
  Học sinh nhận thông báo bài tập qua email, tải xuống và nộp trực tiếp trên hệ thống.
- **Biểu đồ**:

  ![diagram](https://www.planttext.com/plantuml/png/T90nRi9044NxFSN8FLT0H48AJIW85nYl9tWaUnPvP-48gN80Eb2wI7HKTf5YJx8du0gH7H189FLxC__FdBllYLTiDDILGQkkWMoMkWyBdgNC03syQYX8z4gVEHuSR3X-oO2NXBQanfZWoQ8do9Qf_MJGk6UeE7NlOV2cRYkLm-85bHh6wkRFKxTRGzxxcjhZ-ZSrv3Nha_UyahgFl-bbQey2MiQJh22F1pSCBCWIRsZkbD_Oeh8JOoxTOJGQFnQuXmznz_3FrPUx_nKc94N_r1y0003__mC0)
---

#### **Ca sử dụng 4: Quản trị hệ thống**
- **Mô tả:**  
  Quản trị viên quản lý tài khoản, cấu hình hệ thống, và giám sát hoạt động.  
- **Liên hệ cơ chế:**  
  - **Phát hiện lỗi:** Sử dụng Prometheus để theo dõi nhật ký và phát hiện bất thường.  
  - **Bảo mật:** Kiểm tra quyền truy cập trước khi thực hiện thay đổi cấu hình.  
- **Ví dụ:**  
  Quản trị viên khóa tài khoản vi phạm và theo dõi các hoạt động hệ thống trong thời gian thực.
- **Biểu đồ**:

  ![diagram](https://www.planttext.com/plantuml/png/N90n2W8n44Nxd6BOVgyWBXOMQY6U8CIu2ReJI2OBdi32ojBEHMp4piuK5l4YEO5Na5s4HTkPzsO-_nsUGqVSagysZ0io5hAvJuyp0jaKzb3hUCKCk8DYMMbap3ifk9EGJLIySw1uqh1MfbKwR6h4kX32UAIU7UlOLE1YGz2Y3S7haC8HoqwP6THaR258rvgslJPAZui75M-eGAMm0r8f7BxMoE1AbzxAnTQHh1Zh0aAU3tuozDF_D_tc_zHGuh8jv0C00F__0m00)
---

#### **Ca sử dụng 5: Xử lý thanh toán**
- **Mô tả:**  
  Học sinh hoặc phụ huynh thanh toán học phí qua hệ thống.  
- **Liên hệ cơ chế:**  
  - **Quản lý giao dịch:** Đảm bảo giao dịch thành công trước khi cấp quyền tham gia khóa học.  
  - **Phát hiện lỗi:** Hiển thị cảnh báo nếu giao dịch thất bại.  
- **Ví dụ:**  
  Phụ huynh thanh toán bằng PayPal và hệ thống xác nhận giao dịch thành công trước khi kích hoạt khóa học.
  - **Biểu đồ**:

  ![diagram](https://www.planttext.com/plantuml/png/V8yx2i9048RxFSMGFbSGmSP629Z2TjYipgAPbNqKEODuY1IMkO1RMEGaUmAl87ae268xtp_VpF-CZwNpQ7seJmAbDnQoTOfN2KupPO0EjZvKYlsR5fJY3IWqCoxG3bG4foGw1Lb9o0JUz2q3ZQepzTsOtU1H5TZKmy8dl-jR2KpftZ4SD1geKhp8IRuolDUsBYsoG-crOI6cWv3dYo_V_ERV-G_TKd4rT7y1003__mC0)  
