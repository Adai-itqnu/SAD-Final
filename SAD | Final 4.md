# Giải thích về các lớp trong hệ thống iLearn

Hệ thống iLearn được thiết kế để hỗ trợ việc học trong môi trường học tập kỹ thuật số. Dưới đây là giải thích chi tiết về các lớp và thuộc tính của hệ thống iLearn.

### 1. Lớp **Người dùng** 

Lớp **Người dùng** đại diện cho một người dùng trong hệ thống, có thể là học sinh, giáo viên hoặc quản trị viên. Các thuộc tính của lớp này bao gồm:

### 2. Lớp **Khóa học** 

Lớp **Khóa học** đại diện cho các khóa học trong hệ thống iLearn. Các thuộc tính của lớp này bao gồm:



### 3. Lớp **Bài tập** 

Lớp **Bài tập** đại diện cho các bài tập trong hệ thống iLearn, thuộc về một khóa học cụ thể. Các thuộc tính của lớp này bao gồm:

### 4. Lớp **Dịch vụ người dùng** (Dịch vụ người dùng)

Lớp **Dịch vụ người dùng** cung cấp các dịch vụ liên quan đến người dùng trong hệ thống, bao gồm:


### 5. Lớp **Dịch vụ khóa học** 

Lớp **Dịch vụ khóa học** cung cấp các dịch vụ quản lý khóa học trong hệ thống, bao gồm:



### 6. Lớp **Dịch vụ bài tập**

Lớp **Dịch vụ bài tập** cung cấp các dịch vụ liên quan đến bài tập trong hệ thống, bao gồm:



### 7. Lớp **Quản lý bảo mật** 

Lớp **Quản lý bảo mật** quản lý các yếu tố bảo mật trong hệ thống, bao gồm:


### 8. Lớp **FileManager** (Quản lý tệp tin)

Lớp **FileManager** quản lý việc tải lên và tải xuống các tệp tin trong hệ thống. Các phương thức của lớp này bao gồm:

- **uploadFile(file: File)**: Tải lên một tệp tin (ví dụ: tài liệu học tập hoặc bài tập).
- **downloadFile(fileID: String)**: Tải xuống tệp tin từ hệ thống.

### 9. Lớp **Thông báo** (Thông báo)

Lớp **Thông báo** đại diện cho các thông báo gửi đến người dùng trong hệ thống, bao gồm:


### 10. Lớp **Cấu hình hệ thống** 

Lớp **Configuration** chứa các cài đặt cấu hình của hệ thống, bao gồm:

- **interfaceSettings** (Cài đặt giao diện): Cấu hình các tùy chọn giao diện của hệ thống như màu sắc, kiểu chữ, v.v.
- **applicationServices** (Dịch vụ ứng dụng): Cấu hình các dịch vụ ứng dụng có sẵn trong hệ thống như email, hội thảo trực tuyến.
- **userGroups** (Nhóm người dùng): Cấu hình các nhóm người dùng trong hệ thống như học sinh, giáo viên, quản trị viên.

### 11. Lớp **Nhật ký hoạt động** 

Lớp **Nhật ký hoạt động** lưu trữ các hành động của người dùng trong hệ thống, bao gồm:

---

![](https://www.planttext.com/plantuml/png/b5PTQzH057tFhxZqnRIqHLyN4MqNM-a7IAFuEarZPkXcikvEYelwK7peWmZsiOZGTLcqnLAr1J73qeTP_1_t5_WNP99cacpJtVgsEVTCzioPC_VchxoutnQa9QAWOLctOFW1vJjEWVjqU4IWWV9Z4vwqlHROw_wVxoW_CTXIlxa_RRaDqcv3XjOr2Ayi07XKBu4rs10jndrT4kgO5v-zWB164TWXp6cfdmPwSwsenJ1gjJsmLwWw8q1HldSpJGcqh95CK8wCggck1EhSmRXNXBYl3ZiB69-AuGUClqGrg1FXcSeAnXV2eIfsBmlNAt_GRZEV1nuNO2-eGmO2uvDc9buZZWPIxO7g6QIadQdZIBz-Tu9kYd6NhwCyQEQAjmkRpWqO8radOCDhxJ3N0xkEyfrBOGTb7tXbA5B6KvJzYdWCzuTlkR-Y1ZOlnwJ4dSwfwrHltYvbPHO2Z4_42iNuACh0P8shoSaIVHpdt7SOd_1Faq9MkVFjgxdBjpsQG85nDyn1k_e0HlNVRC5BTKOAp43rhcOw8JOmxdVgXDCDrNLfOSbq3LPPMzpDeNitYc-bBvjN4ftRCfBjn1M3sPjvpWquQiaDs5ndFUTLNQ1Pc1YzibcbrrNOUscWeOtpRyDpenOJdJN2YQyRw-C8unw7XXh09iQzC8rsvbvQNLM31LrRqwNKlPUgwpeKvGztyaLgKlMPFuuwA7V7NuPPeEgGKoty86_Tuwx8GzRmghOYKEurGJ1-PIEEhZYCcn3qsAewvXbi9oiTnckGGTE6-2n2kSzzmmrKB_jz4x7heM3FcKi42pdOQN-0JTKDCv4fjA2weMc_ELGQ1oWFM3qgZxTnpff9iOJoX4qS4eiXVyxyg7KfTH7ZVWHKVUDKzvmz43Gn8jETr9UJSgBRLOTCpwbVOecHiCvGxfK6xvQvaoY_Sh-EiZ-o5QhEWkevFgOrk8BjCD5P3NsmqmiBsse0DCIuAs2udwJAV3gaJKuDbfFoPUQCxwRyFmvNfJS93zMq9KPuqVarbFiCNaI4fwRw3EKf0LTrtNH7Ldb-JTsPWfcvEPYwFJy_CrKOrJNmzQbQXRu_XkjIb4V4gXmNStElxnLdSbNpJ3ZciK0fgqrePOUgciauchcg2IbxiWgtf6BrDUTQmRJkUtnBVtd-0m00__y30000)

   **4.1 Mô tả chức năng**

    **1.1 Mô tả chức năng**
   - Chức năng :
      + Đăng ký tài khoản người dùng mới.
      + Đăng nhập và xác thực tài khoản.
      + Quản lý thông tin cá nhân của người dùng (cập nhật, xóa).
      + Phân quyền người dùng (Quản trị viên, Bác sĩ, Bệnh nhân).
      + Quản lý trạng thái tài khoản (kích hoạt, vô hiệu hóa).
   - Yêu cầu giao diện:
      + Biểu mẫu nhập liệu (Forms) để thêm/sửa thông tin bệnh nhân.
      + Màn hình hiển thị danh sách bệnh nhân kèm chức năng tìm kiếm.
   
