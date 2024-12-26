#### **Mô hình kiến trúc**
Hệ thống iLearn được đề xuất sử dụng kiến trúc **đa tầng (Multi-tier Architecture)**, bao gồm các thành phần chính:
1. **Tầng giao diện người dùng (UI Layer)**:  
   - Cung cấp giao diện dựa trên trình duyệt cho người dùng (học sinh, giáo viên, quản trị viên).  
   - Hỗ trợ khả năng tùy chỉnh giao diện theo nhóm người dùng.  

2. **Tầng dịch vụ ứng dụng (Application Layer)**:  
   - Chịu trách nhiệm xử lý logic nghiệp vụ của hệ thống.  
   - Quản lý các dịch vụ như xác thực, quản lý khóa học, tài liệu, nhóm học tập.  
   - Cung cấp API để tích hợp với các dịch vụ bên thứ ba.  

3. **Tầng lưu trữ (Data Layer)**:  
   - Quản lý cơ sở dữ liệu người dùng, tài liệu học tập và nhật ký hoạt động.  
   - Đảm bảo an toàn dữ liệu và cung cấp khả năng truy vấn hiệu quả.  
### Các cơ chế phân tích

- **Persistency (Tính bền vững)**: Lưu trữ thông tin tài khoản người dùng trong cơ sở dữ liệu an toàn.  
- **Security (Bảo mật)**: Sử dụng xác thực và mã hóa mật khẩu để bảo vệ thông tin tài khoản.  
- **Transaction Management (Quản lý giao dịch)**: Đảm bảo thao tác đăng ký, sửa đổi thông tin được thực hiện hoàn chỉnh.
- **Information Exchange (Trao đổi thông tin)**: Đồng bộ hóa thông tin giữa giáo viên, học sinh và cơ sở dữ liệu.
- **Message Routing (Định tuyến tin nhắn)**: Phân phối tài liệu đến đúng người dùng.  
- **Error Detection / Handling (Phát hiện và xử lý lỗi)**: Phát hiện lỗi tải lên tài liệu và phản hồi người dùng.
- **Communication (Giao tiếp)**: Cung cấp các công cụ thảo luận, chat nhóm.

#### Kết quả phân tích từng ca sử dụng

## **Ca sử dụng 1: Quản lý người dùng**
### Mô tả
Hệ thống hỗ trợ quản lý tài khoản người dùng, bao gồm đăng ký, đăng nhập, chỉnh sửa thông tin cá nhân và quản lý vai trò (giáo viên, học sinh, quản trị viên).

### Tác nhân
- Người dùng: Học sinh, Giáo viên, Quản trị viên.

### Cơ chế sử dụng
- **Persistency (Tính bền vững)**: Lưu trữ thông tin tài khoản người dùng trong cơ sở dữ liệu an toàn.  
- **Security (Bảo mật)**: Sử dụng xác thực và mã hóa mật khẩu để bảo vệ thông tin tài khoản.  
- **Transaction Management (Quản lý giao dịch)**: Đảm bảo thao tác đăng ký, sửa đổi thông tin được thực hiện hoàn chỉnh.

### Chức năng chính
- Đăng ký tài khoản mới.  
- Đăng nhập vào hệ thống.  
- Chỉnh sửa thông tin cá nhân (email, tên, ảnh đại diện, v.v.).  
- Phân quyền và quản lý vai trò của người dùng.

### Biểu đồ ca sử dụng: Quản lý người dùng

![Quản lý người dùng](https://www.planttext.com/plantuml/png/P55DIWCn5Dxd58_PzmfIAKK5NLZjMi9CJ4AdBoLvqmku4151Rs1r9tGZhXgAY_GYEO5Na4vdEftfzljxNxxy-T--8swfcEQCfsGi9EVHlwJWDAe4k8CRAZA1LBDdEYmCp7NumfA-5JnLmjRqTH5NdmXaety-K9rcKusC5Kwat0b8Dg-R1vGm2MkWyAvXeipMLsh7WxkHaDgHi4S6L76rd86A_X58HV-6ilPS6gcnCGnKz4-em4M_v40g_A04qWXfM02gyB4_DimqNU2zQRpL8_AmXZdNG3Pyr-8hZboAaSc5OwoQ1dgzarRh3hvhrW7tLrcru55A1z-bTC0cfLouhMr1XyNx0hFjX_y3003__mC0)
---

## **Ca sử dụng 2: Tạo và quản lý khóa học**
### Mô tả
Giáo viên có thể tạo mới, chỉnh sửa hoặc xóa các khóa học. Học sinh có thể đăng ký và xem thông tin khóa học.

### Tác nhân
- Giáo viên: Tạo và quản lý khóa học.  
- Học sinh: Đăng ký và tham gia khóa học.

### Cơ chế sử dụng
- **Persistency (Tính bền vững)**: Lưu trữ thông tin khóa học và danh sách học viên.  
- **Transaction Management (Quản lý giao dịch)**: Đảm bảo việc tạo, chỉnh sửa hoặc xóa khóa học diễn ra hoàn chỉnh.  
- **Information Exchange (Trao đổi thông tin)**: Đồng bộ hóa thông tin giữa giáo viên, học sinh và cơ sở dữ liệu.

### Chức năng chính
- Giáo viên tạo mới hoặc chỉnh sửa khóa học (tên, mô tả, tài liệu).  
- Học sinh xem và đăng ký khóa học.  
- Quản lý danh sách học viên tham gia khóa học.

### Biểu đồ ca sử dụng: Tạo và quản lý khóa học

![Tạo và quản lý khóa học](https://www.planttext.com/plantuml/png/P55DIWCn5Dxd58_PzmfIAKK5NLZjMi9CJ4AdBoLvqmku4151Rs1r9tGZhXgAY_GYEO5Na4vdEftfzljxNxxy-T--8swfcEQCfsGi9EVHlwJWDAe4k8CRAZA1LBDdEYmCp7NumfA-5JnLmjRqTH5NdmXaety-K9rcKusC5Kwat0b8Dg-R1vGm2MkWyAvXeipMLsh7WxkHaDgHi4S6L76rd86A_X58HV-6ilPS6gcnCGnKz4-em4M_v40g_A04qWXfM02gyB4_DimqNU2zQRpL8_AmXZdNG3Pyr-8hZboAaSc5OwoQ1dgzarRh3hvhrW7tLrcru55A1z-bTC0cfLouhMr1XyNx0hFjX_y3003__mC0)
---

## **Ca sử dụng 3: Quản lý tài liệu học tập**
### Mô tả
Hệ thống hỗ trợ tải lên, chỉnh sửa và phân phối tài liệu học tập cho các khóa học.

### Tác nhân
- Giáo viên: Quản lý tài liệu.  
- Học sinh: Xem và tải tài liệu.

### Cơ chế sử dụng
- **Persistency (Tính bền vững)**: Lưu trữ tài liệu học tập trên hệ thống.  
- **Message Routing (Định tuyến tin nhắn)**: Phân phối tài liệu đến đúng người dùng.  
- **Error Detection / Handling (Phát hiện và xử lý lỗi)**: Phát hiện lỗi tải lên tài liệu và phản hồi người dùng.

### Chức năng chính
- Giáo viên tải lên và quản lý tài liệu khóa học.  
- Học sinh xem và tải tài liệu liên quan.  
- Xử lý lỗi khi tải lên không thành công.

### Biểu đồ ca sử dụng: Quản lý tài liệu học tập

![Quản lý tài liệu học tập](https://www.planttext.com/plantuml/png/R94xRi9048RxFSN8lQyGMGAKD5Gyb0wDx54yqh96tjcO6o0A2cwGA5saLEcoHGgVP4_05H089_XHV_-_Ez_CoVycLh0KjzOAKobAY1wvVY_WbUjF4m5Qc1EcEPKDVWh-a89bar_fJ5n6HfHobbAq1D4y_7mmIFt6e3dudGFTFBKOhHORNM0sHQ6IKV-tHddmUvE33VuBxzjDSPAnz6lFzVTWUaoQX0Roj1wABvcgVhXlidN17ytBtoz5PLewwhOiYEE70TiERIbrM4T0tVRSuDR07TQRAY6JNGvy1W00__y30000)
---

## **Ca sử dụng 4: Quản lý nhóm học tập**
### Mô tả
Hệ thống hỗ trợ tạo nhóm học tập, chia sẻ tài liệu và thảo luận trong nhóm.

### Tác nhân
- Giáo viên và Học sinh: Tham gia và quản lý nhóm.

### Cơ chế sử dụng
- **Message Routing (Định tuyến tin nhắn)**: Đảm bảo chia sẻ thông tin đúng các thành viên trong nhóm.  
- **Communication (Giao tiếp)**: Cung cấp các công cụ thảo luận, chat nhóm.  
- **Security (Bảo mật)**: Bảo vệ nội dung nhóm khỏi truy cập trái phép.

### Chức năng chính
- Tạo nhóm học tập mới.  
- Thêm hoặc loại bỏ thành viên nhóm.  
- Chia sẻ tài liệu và thảo luận trong nhóm.

### Biểu đồ ca sử dụng: Quản lý nhóm học tập
![Quản lý nhóm học tập](https://www.planttext.com/plantuml/png/V98nQiCm58Ptd-BXFLSeAIwaIvR6WMxbLNvK0biAqbEkqAbtIEWMo9JD7Zhe93f1hr1gnxWMeVFtV-_fb_JTVIqTesNVr1aADXRobGf70tiLJZe7T50I2absn8-n-n3Wb9OztR2lI7EMUKS27K5UnlPeGCjmQK3sOOxjUTUdjyLBOGcPLjRutHz7XbC3BCD1os7rC62KxgjgJSqhsKbv3XVyntYYnkmfbKePsqy3jO_jMGDRez_cMd-k1-M4TquPFPc5L0WkjXrmE2YeLUpU_TpTIBH3iJKoMOLrbbql3nQBkxHyWgQA2PWrITYjbTSN6IDfemJVcB0aNVt-Xny0003__mC0)
---

## **Ca sử dụng 5: Gửi thông báo**
### Mô tả
Hệ thống gửi thông báo quan trọng đến người dùng như cập nhật khóa học, thông tin nhóm học tập hoặc nhắc nhở.

### Tác nhân
- Giáo viên: Gửi thông báo.  
- Học sinh: Nhận thông báo.

### Cơ chế sử dụng
- **Message Routing (Định tuyến tin nhắn)**: Gửi thông báo đến đúng đối tượng mục tiêu.  
- **Communication (Giao tiếp)**: Sử dụng thông báo đẩy hoặc email để truyền tải thông tin.  
- **Error Detection / Handling (Phát hiện và xử lý lỗi)**: Phát hiện lỗi gửi thông báo không thành công.

### Chức năng chính
- Giáo viên tạo thông báo mới.  
- Hệ thống gửi thông báo qua email hoặc thông báo đẩy.  
- Học sinh nhận và xem thông báo.

### Biểu đồ ca sử dụng
![Gửi thông báo](https://www.planttext.com/plantuml/png/V98nQiCm58Ptd-BXFLSeAIwaIvR6WMxbLNvK0biAqbEkqAbtIEWMo9JD7Zhe93f1hr1gnxWMeVFtV-_fb_JTVIqTesNVr1aADXRobGf70tiLJZe7T50I2absn8-n-n3Wb9OztR2lI7EMUKS27K5UnlPeGCjmQK3sOOxjUTUdjyLBOGcPLjRutHz7XbC3BCD1os7rC62KxgjgJSqhsKbv3XVyntYYnkmfbKePsqy3jO_jMGDRez_cMd-k1-M4TquPFPc5L0WkjXrmE2YeLUpU_TpTIBH3iJKoMOLrbbql3nQBkxHyWgQA2PWrITYjbTSN6IDfemJVcB0aNVt-Xny0003__mC0)
