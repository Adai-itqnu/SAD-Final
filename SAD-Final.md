# 📑 Báo cáo Phân tích và Thiết kế Hệ thống

## 1. Mô tả tóm tắt bài toán
  ### Hệ thống iLearn là một môi trường học tập kỹ thuật số (DLE) được sử dụng để hỗ trợ việc học trong các trường học có học sinh từ 4 đến 18 tuổi. Hệ thống này được thiết kế để thay thế một hệ thống hiện có (Glow) được xây dựng đặc biệt cho mục đích này và bao gồm các ứng dụng riêng cho email, v.v. Glow là một hệ thống khép kín, nơi người dùng không thể giới thiệu các ứng dụng riêng của họ. Hệ thống này ngày càng ít được sử dụng vì các tiện ích trong các hệ thống miễn phí vượt trội hơn nhiều so với các tiện ích được cung cấp trong hệ thống khép kín.
### Sự cần thiết và lợi ích khi giải quyết bài toán
#### **Sự cần thiết**
- **Thay thế hệ thống cũ (Glow)**: Glow, một hệ thống học tập số dành riêng cho các trường học ở Scotland, đã trở nên **lỗi thời** vì:  
  - Tính chất **đóng kín**, không hỗ trợ tích hợp các ứng dụng mới.  
  - Tính năng hạn chế và không còn đáp ứng được nhu cầu hiện đại.  
  - Sự xuất hiện của các **hệ thống miễn phí** với tính năng vượt trội đã thay thế Glow.  
- **Hỗ trợ đổi mới trong giáo dục**: Cần một **môi trường học tập số mở, hiện đại, linh hoạt** để phục vụ học sinh, giáo viên và phụ huynh.  
- **Đồng bộ hóa**: Đảm bảo tính thống nhất với hệ thống quản lý và mạng lưới trường học nhưng vẫn cho phép **tùy chỉnh** linh hoạt theo nhu cầu từng khu vực và độ tuổi học sinh.

#### **Lợi ích**
- **Tăng tính linh hoạt và mở rộng**:  
  - Cho phép **tích hợp các ứng dụng và dịch vụ mới** một cách dễ dàng.  
  - Linh hoạt trong việc thay thế hoặc nâng cấp dịch vụ.  
- **Tùy chỉnh theo nhu cầu người dùng**:  
  - Cung cấp dịch vụ có thể **cá nhân hóa** cho từng nhóm người dùng.  
  - Tạo môi trường học tập phù hợp với từng đối tượng học sinh, giáo viên.  
- **Cải thiện sự hợp tác**:  
  - Hỗ trợ chia sẻ tài nguyên và thông tin dễ dàng giữa học sinh, giáo viên và phụ huynh.  
- **Khả năng tích hợp đa dạng**:  
  - Liên kết với các **hệ thống quản lý mạng và dịch vụ bên ngoài** mà không bị giới hạn bởi kiến trúc cũ.  

---

## 2. Yêu cầu hệ thống

### 2.1. Yêu cầu chức năng
#### **Dịch vụ tiện ích (Utility Services)**
- Cung cấp các chức năng **cơ bản** hỗ trợ hệ thống, ví dụ:  
  - Xác thực và quản lý danh tính người dùng.  
  - Lưu trữ và bảo mật dữ liệu người dùng.  
- Cho phép **tùy chỉnh** hoặc phát triển mới các dịch vụ tiện ích.  

#### **Dịch vụ ứng dụng (Application Services)**
- Hỗ trợ các ứng dụng phục vụ nhu cầu học tập và cộng tác như:  
  - **Email**, hội thảo trực tuyến, chia sẻ ảnh và tài liệu học tập.  
  - Truy cập tài nguyên giáo dục như **phim khoa học, tài liệu lịch sử**.  
- Cho phép sử dụng các dịch vụ miễn phí hoặc tích hợp thêm các dịch vụ bên ngoài.  

#### **Dịch vụ cấu hình (Configuration Services)**
- Cung cấp khả năng tùy chỉnh môi trường học tập:  
  - Tùy chỉnh giao diện và bộ dịch vụ ứng dụng theo nhu cầu từng nhóm người dùng.  
  - Xác định cách **chia sẻ dịch vụ** giữa học sinh, giáo viên và phụ huynh.  

---

### 2.2. Yêu cầu phi chức năng
#### **Tính mở và linh hoạt**
- Hệ thống phải cho phép **tích hợp dịch vụ mới** hoặc thay thế dịch vụ sẵn có một cách dễ dàng.  

#### **Khả năng tương thích**
- Hỗ trợ tích hợp với các **hệ thống quản lý mạng và quản trị** trường học hiện tại.  
- Đảm bảo tính **đồng bộ** nhưng vẫn linh hoạt để phù hợp với nhu cầu từng khu vực.  

#### **Tính dễ sử dụng**
- Hệ thống phải **thân thiện** với người dùng không chuyên về kỹ thuật.  
- Sử dụng các phương pháp đơn giản như **user stories** để thu thập và triển khai yêu cầu.  

#### **Tính bảo mật và kiểm soát**
- Bảo vệ **dữ liệu cá nhân** của học sinh, giáo viên và phụ huynh.  
- Kiểm soát truy cập dịch vụ dựa trên **quyền hạn người dùng** (ví dụ: học sinh, giáo viên, quản trị viên).  

#### **Hiệu năng cao**
- Đảm bảo hệ thống hoạt động ổn định khi có số lượng lớn người dùng truy cập đồng thời.  
- Phục vụ đối tượng người dùng đa dạng từ học sinh **4 tuổi đến 18 tuổi**.  

#### **Khả năng mở rộng**
- Cho phép phát triển thêm các dịch vụ hoặc tính năng mới trong tương lai một cách dễ dàng.  

---

# Phân tích ca sử dụng

## Mô hình kiến trúc

Hệ thống iLearn được đề xuất sử dụng kiến trúc phân lớp (N-tier), bao gồm các thành phần chính:

### Lớp giao diện người dùng (UI Layer)
- Cung cấp giao diện dựa trên trình duyệt cho người dùng (học sinh, giáo viên, quản trị viên).
- Hỗ trợ khả năng tùy chỉnh giao diện theo nhóm người dùng.

### Lớp ứng dụng (Application Layer)
- Chịu trách nhiệm xử lý logic nghiệp vụ của hệ thống.
- Quản lý các dịch vụ như xác thực, quản lý khóa học, tài liệu, nhóm học tập và chuyển giao đến lớp phù hợp.
- Cung cấp API để tích hợp với các dịch vụ bên thứ ba.

### Lớp dữ liệu (Data Layer)
- Quản lý cơ sở dữ liệu người dùng, tài liệu học tập và nhật ký hoạt động.
- Đảm bảo an toàn dữ liệu và cung cấp khả năng truy vấn hiệu quả.

---

## Các cơ chế phân tích

### 1. Cơ chế tính bền vững (Persistency)
Đảm bảo hệ thống hoạt động ổn định, có thể mở rộng và tiết kiệm tài nguyên.

#### Ứng dụng trong iLearn
- **Kiến trúc linh hoạt**:
  - Sử dụng kiến trúc Microservices để các thành phần hoạt động độc lập, giảm tải và dễ dàng nâng cấp.
- **Hỗ trợ mở rộng**:
  - Triển khai trên đám mây (AWS, Azure) để tăng khả năng đáp ứng khi số lượng người dùng tăng cao.

#### Ví dụ
Trong mùa thi, lượng truy cập tăng mạnh, hệ thống tự động thêm máy chủ để duy trì hiệu năng ổn định.

---

### 2. Cơ chế định tuyến tin nhắn (Message Routing)
Đảm bảo thông tin và yêu cầu được gửi đúng nơi, đúng lúc.

#### Ứng dụng trong iLearn
- **Thông báo sự kiện**:
  - Gửi thông báo tự động (qua email, ứng dụng) đến đúng nhóm người dùng khi có sự kiện mới (bài giảng mới, hạn nộp bài tập).
- **Hệ thống hàng đợi tin nhắn**:
  - Sử dụng RabbitMQ hoặc Kafka để xử lý thông báo và giao tiếp giữa các dịch vụ trong hệ thống.

#### Ví dụ
Khi giáo viên thêm tài liệu mới, hệ thống gửi thông báo đến tất cả học sinh trong lớp qua email.

---

### 3. Cơ chế quản lý giao dịch (Transaction Management)
Đảm bảo tính toàn vẹn và an toàn của giao dịch trong hệ thống.

#### Ứng dụng trong iLearn
- **Thanh toán học phí**:
  - Sử dụng các nền tảng thanh toán trực tuyến (Stripe, PayPal) và cơ chế kiểm tra để xác nhận giao dịch thành công trước khi đăng ký khóa học.
- **Đăng ký khóa học**:
  - Áp dụng nguyên tắc ACID để đảm bảo dữ liệu không bị lỗi khi người dùng thực hiện đăng ký hoặc hủy bỏ.

#### Ví dụ
Một học sinh thanh toán phí khóa học. Nếu quá trình thanh toán thất bại, hệ thống không thêm họ vào danh sách học viên.

---

### 4. Kiểm soát và đồng bộ hóa tiến trình (Process Control and Synchronization)
Đảm bảo các tác vụ được thực hiện theo thứ tự và tránh xung đột.

#### Ứng dụng trong iLearn
- **Quản lý chỉnh sửa tài nguyên**:
  - Sử dụng cơ chế khóa (lock) khi giáo viên chỉnh sửa tài liệu để tránh hai người cùng thay đổi.
- **Đồng bộ hóa giao dịch**:
  - Đảm bảo tiến trình đăng ký khóa học hoàn tất trước khi tài liệu được phân phối cho học sinh.

#### Ví dụ
Nếu hai giáo viên chỉnh sửa cùng một bài tập, chỉ một người được phép thay đổi tại một thời điểm.

---

### 5. Bảo mật (Security)
Bảo vệ dữ liệu người dùng và hệ thống khỏi các cuộc tấn công.

#### Ứng dụng trong iLearn
- **Xác thực**:
  - Sử dụng OAuth 2.0 và JWT để quản lý phiên đăng nhập của người dùng.
- **Mã hóa dữ liệu**:
  - Mã hóa mật khẩu và dữ liệu nhạy cảm bằng AES-256.
- **Bảo vệ khỏi tấn công**:
  - Tường lửa ứng dụng web (WAF) để ngăn chặn SQL Injection, XSS, hoặc CSRF.

#### Ví dụ
Học sinh đăng nhập và hệ thống sử dụng JWT để xác minh danh tính mà không tiết lộ thông tin nhạy cảm.

---

### 6. Giao diện cũ (Legacy Interface)
Đảm bảo giao diện đơn giản, quen thuộc với người dùng đã sử dụng hệ thống trước đó.

#### Ứng dụng trong iLearn
- **Thiết kế tối giản**:
  - Giữ lại bố cục quen thuộc (menu bên trái, nội dung ở giữa) để người dùng không phải làm quen lại từ đầu.
- **Hỗ trợ thiết bị cũ**:
  - Tối ưu giao diện để tương thích với các trình duyệt và thiết bị cấu hình thấp.

#### Ví dụ
Học sinh sử dụng trình duyệt cũ vẫn có thể truy cập giao diện iLearn mà không bị lỗi hiển thị.

---

### 7. Phát hiện lỗi (Error Detection)
Phát hiện và xử lý lỗi nhanh chóng để duy trì hoạt động của hệ thống.

#### Ứng dụng trong iLearn
- **Giám sát hệ thống**:
  - Sử dụng công cụ như Prometheus hoặc New Relic để theo dõi hiệu năng và cảnh báo khi có lỗi.
- **Quản lý lỗi người dùng**:
  - Hiển thị thông báo lỗi rõ ràng (ví dụ: "Sai mật khẩu", "Khóa học đã hết chỗ").

#### Ví dụ
Khi người dùng nhập sai mật khẩu nhiều lần, hệ thống cảnh báo và khóa tài khoản tạm thời.

---

## Kết quả các ca sử dụng:

## 1. Đăng nhập hệ thống

### Cơ chế phân tích:
- **Tính bền vững (Persistency)**: Lưu thông tin người dùng và quyền truy cập trong cơ sở dữ liệu.
- **Bảo mật (Security)**: Xác thực thông tin đăng nhập và bảo mật thông tin tài khoản.
- **Phát hiện lỗi (Error Detection/Handling/Reporting)**: Xử lý lỗi đăng nhập (ví dụ: sai mật khẩu, tài khoản không tồn tại).

### Luồng sự kiện chính:
1. Người dùng nhập tên đăng nhập và mật khẩu.
2. Hệ thống xác thực thông tin với cơ sở dữ liệu (kiểm tra tài khoản và mật khẩu).
3. Nếu thông tin hợp lệ:
   - Hệ thống tạo JWT token và lưu trữ trên cookies của người dùng.
   - Chuyển người dùng đến giao diện chính.
4. Nếu thông tin không hợp lệ:
   - Hiển thị thông báo lỗi.
   - Ghi log lỗi vào hệ thống để theo dõi.

### Luồng sự kiện phụ:
- Nếu kết nối đến cơ sở dữ liệu bị gián đoạn, hệ thống sẽ hiển thị thông báo lỗi kết nối và yêu cầu thử lại sau.
  
 ![Login](https://www.planttext.com/plantuml/png/b9C_YXin6CLxdU9TO2_W8gp1iFb7cXqpjQnHHc9cfMH6Cd4PjaYHogH86GzB25amII0Ga0eNCdiFdI1N29Azu0dP8iqWzBtlq-yzQNxxtNblQ6ViLKieCxh3lESTQ8yvMMYhAjgjKFB54sLuzv8odaebOLgPJhUOMYCkURUKXyAKLDJG1UqvPlSBscD6o1ndZr1Ey494jtq54suLzklzjQgX3blBiC5LT5k3HaJtrP8ojKmdk8X-Ax4AjnOikYyMRyB0O4JqFnZ8DAbc4nITNM4PtMS58y9FLSD81HCs4etGqTqea1dE3YEBBheRBAD_-x2OjWR5wOw9_aFwka5csFqwE5MFcG4W4vKJ5D4D6a_B0aOtNEKUamzkejiPlBPfRKJOA06MA79xjZsVuFdTTvkxbs6ZmRHk9E_p42RiAlhh561qEuLQKerAHlzEWOcmLOBmjkTZ-kReyyH4glnY8mFegHoRoC37a1PXq6YZ_oX7f8zbfZ4Y-lSFIEzlwK98jBe-L8xExWRqqNz25VqtjCc69LnL9D_0inoLYduj_wd48XrQop2aE7HqWnhp_urp33zF_0yNEVYJDvXaMxGfnmnxpbML_g4_0000__y30000)

---------

## 2. Đăng ký tài khoản

### Cơ chế phân tích:
- **Tính bền vững (Persistency)**: Lưu trữ thông tin tài khoản mới trong cơ sở dữ liệu.
- **Error Handling**: Xử lý các lỗi liên quan đến dữ liệu đầu vào hoặc kết nối hệ thống.
  
### Luồng sự kiện chính:

1. Người dùng truy cập giao diện đăng ký tài khoản.
2. Nhập thông tin đăng ký bao gồm tên, email, mật khẩu, và các thông tin cần thiết khác.
3. Lưu thông tin vào cơ sơ dữ liệu
4. Gửi thông báo đăng ký thành công và chuyển về giao diện chính

### Luồng sự kiện phụ
- Dữ liệu không hợp lệ
- Lỗi kết nối cơ sở dữ liệu:
 ![Đăng ký tài khoản](https://www.planttext.com/plantuml/png/b5JFYjf07BxFKtnuQi7r0JoKfGJQOl5YhRsEIJH39fCbcInuzh27NkgfXnwgI5cw85rAJncAXyY-npn1Nw7C9Ex66fHwYiptzpU_v8_QNgQI9ZABEA6kZ1CCKpy1JJ4aupWJ7arc6FdZDqBwoOIwlZaQ4JSMCecv1G_yv9gL1mFYKKd7DFNXx1ze2kSHtuybcp2NIXQB6gzFo10NBp3gubsIpU3gV7E5AQCnFARLZS1kiPkBASBYDnaPvB2BrqohkO0CjFg8IPn4TT1UhXzOAHaKlyGKajMLy4mMTw8DFwACjn7fV2CH1Zh_dhNHwNIUbrQ3BbvfjM6O5NUPYNQR8JJU4MH2SLqimH_kive76LIytXDC5XiH8D1gVGMkrGrShMufFAr-W9kE6Q5SmddwNmCJ0B2YJXTl3yqWYoL36CGwNmj4MdrX9bCCzs65LAkl1nv6oFZiHPOYW6kax8dvERWemtyeLYw4cPzuB7WCjwdw-n5LiSR5AguFkf7Ph-wnxdF8BzQO6jb3ir6JMQD3uwRKMQtTfyQCBNkhRf3DB76tqFbM7EoZ6vZxj4u-J_tzF7N-JMAiynKxdkTBuyYr-ioEzkLyFyixNOnRwLQlaWsqclzhrC7xZ84NFol01jnaxRJA8i8Zjanz2SEItBIBPuAU2kcSScWHayI-3ZsTRoM4LWlMkC_78p-J3E4PnRFH_ojIMUNI5vxvmFu5003__mC0)

## 3. Học viên tham gia khóa học

### Cơ chế phân tích:
- **Tính bền vững (Persistency)**: Lưu trạng thái đăng ký khóa học của học viên.
- **Quản lý giao dịch (Transaction Management)**: Đảm bảo quá trình thanh toán đăng ký khóa học hoàn tất hoặc bị hủy hoàn toàn.
- **Định tuyến tin nhắn (Message Routing)**: Gửi thông báo xác nhận đăng ký qua email hoặc thông báo trong hệ thống.

### Luồng sự kiện chính:
1. Học viên chọn khóa học muốn tham gia từ danh sách.
2. Hệ thống kiểm tra tình trạng khóa học (còn chỗ trống hay không).
3. Học viên thực hiện thanh toán qua hệ thống tích hợp (ví dụ: thẻ tín dụng, momo, vnpay,...).
4. Hệ thống kiểm tra và xác nhận thanh toán thành công.
5. Lưu thông tin học viên vào danh sách học viên tham gia khóa học.
6. Gửi thông báo xác nhận đến email hoặc thông báo trong hệ thống cho học viên.

### Luồng sự kiện phụ:
- Nếu thanh toán thất bại:
  - Hệ thống hoàn tác mọi thay đổi liên quan đến đăng ký khóa học.
  - Hiển thị thông báo lỗi và hướng dẫn học viên thử lại.
 ![dangkykhoahoc](https://www.planttext.com/plantuml/png/X5GzQzn04EtrArvf5oQzYc2u0pia70TtS4wvjv9l5-jsGLeTkJAuS65INEKYHKuO4t0uudmrMeoBDVuV-mlo5yAkB5do4QngOTxCU_DcHd_rtNwcIAhoUH8GgcIAaSgZM2YG3ADWAdCHaNI9IJnz8rIS7XCQkz0ae5AeL2ReoJpDub6SBdWLwZMX8LdEOw5QiM4G4KMc98lHhnyaG_-9Q20LF-QKA2v5At4G12FilSOaH8zP_KdWX9bV1EvDCS-jNWaeHkQOSH9C7BGNuYst-dGEbHAer9Q5c44nK_1EyWurFmKei_h2eVHApC38qc5-Yzbkq7F5-Y76QRx4mfPNZiY5e7X7Hj37NiKxJcrvYONL7__F6v14uMrBnxQC000y_IJ4aIae1BFbfjjxPii_0fbPF-9hcyRCwXyKZ5jzvgqH34gQGdYKTsWOuhsvpa5j-JLlGx136OVYjhnJpb29oEfpodPzxl0nzyZg3H9pkrNSTJPkLLFCh0K3TQPvm6ELxSRKIrdrPDyztEJFlBrVtP-A6KxCBHPcBK4V2cHMVt7QloDnFkHDdNge1upNt9MT2swkHLKWSbeoKr3McLjTefdseJHh0MNBAuN4wshMeyit275WzORNWAaf93wqsj-9vuGdhzfXbKgtZrQVGJ6_5TKGt3Vm2aOX3blI6oUR6XuV9rdyR2XUyDIM1TyUohWb8R7wmcdk3hcPXkDtT-PBwlDESrNgmgp17cwi_YncY6pvhO9ka3JaiOW2Bx5z4VShSmdcbz3VHUSUsWhRzr2TRUkQdlRzHQM1ax4VYyZz3ly1003__mC0)

## 4. Giáo viên thêm bài học mới

### Cơ chế phân tích:
- **Tính bền vững (Persistency)**: Lưu trữ nội dung bài học trong cơ sở dữ liệu.
- **Tính bảo mật (Security)**: Kiểm tra quyền hạn của giáo viên để đăng nội dung.
- **Phát hiện lỗi (Error Detection/Handling/Reporting)**: Phát hiện và xử lý lỗi khi tải tệp hoặc lưu trữ thông tin.

### Luồng sự kiện chính:
1. Giáo viên chọn "Thêm bài học mới" trong giao diện quản lý khóa học.
2. Nhập thông tin bài học (tiêu đề, mô tả) và tải lên tài liệu hoặc video.
3. Hệ thống kiểm tra định dạng và kích thước tệp tải lên.
4. Lưu thông tin bài giảng và tài liệu liên quan vào cơ sở dữ liệu.
5. Hiển thị thông báo thành công cho giáo viên.

### Luồng sự kiện phụ:
- Nếu tệp tải lên không hợp lệ, hệ thống sẽ hiển thị thông báo lỗi và yêu cầu thử lại.
-![Giáo viên thêm bài](https://www.planttext.com/plantuml/png/Z58zQnmn5EprAmRt9lqMnf0hOhAuoSAcSAFLofQmLdjejGSkGuehJ8fKATpSSONXuC15gbMHGi7_u_q2_uMWs_CNd4rKIM_cpSnxw27yEUuyTxvl3EF2jmw5v4991zwXO5NRsvgxAvIoEh5UkdCkP89A9bhhNMkGowvhxHVfPdg4SbPppolUIKmUBxp3XB42XqSeCtnK57vOd1qKAguRL76XaKe23OKRVNR0oiGiCdpI5BvRU4NX6kUjQs0L3Pifl8g_xGMyjY_QdmnEto5X5XVmDAmqJ5nR-8GOJM7UVvZfMhQZUPxXSp9lu1t7tvyKhgr2JSFINcmbBkD6A7XrVqVXHi1Jc4yP0m1kF8hqJ8QhAGo5-HP89q_Yampv_Lt_Ni3dL4-j4noEmRx6fHWNOM5sEWkh89BQQwSoGp6QL77PxYVkNVOkslukQJgv6_5ovBqrQV9tDAmme_3jbQYXy4l_VuOjVRkQgxZk8MYuJNDJsC3Gi1oLfAqPEvQsJj_v7m000F__0m00)

## 5. Gửi thông báo đến học viên

### Cơ chế phân tích:
- **Định tuyến tin nhắn (Message Routing)**: Định tuyến thông báo đến đúng học viên hoặc nhóm học viên.
- **Phân phối (Distribution)**: Phân phối thông báo qua nhiều kênh (email, SMS, thông báo trong hệ thống).
- **Phát hiện lỗi (Error Detection/Handling/Reporting)**: Xử lý lỗi khi không gửi được thông báo.

### Luồng sự kiện chính:
1. Quản trị viên hoặc giáo viên chọn "Gửi thông báo" trên giao diện quản lý.
2. Chọn nhóm học viên hoặc cá nhân nhận thông báo.
3. Nhập nội dung thông báo và chọn kênh gửi (email, SMS, thông báo trong hệ thống).
4. Hệ thống định tuyến và gửi thông báo đến người nhận.
5. Lưu thông tin lịch sử gửi thông báo vào cơ sở dữ liệu.

### Luồng sự kiện phụ:
- Nếu không gửi được thông báo qua một kênh, hệ thống sẽ:
  - Ghi nhận lỗi vào log.
  - Thử lại gửi qua kênh khác (nếu có).
- ![Gửi thông báo](https://www.planttext.com/plantuml/png/b5J1Qjj05BphAuQS4d1-G8SIDuQqKBa76zphUhtHBf6VMcbbyB7qq4FemQVIGo5kA8KKqq0A1UcGmuRyntv1Vw6i53jIegJjGR3elPatCs_PtyNbNgfPehDfv36kumJToLJHosGe69SY0KlH7NhZEAC9I-OOYV5pqY8vP5ousiZZCUaaZj2FjJfKd6aLqq0aCrKrzBq9qspCKe7U-i1Iz3QuGAGf2nM5-v8HYSXL0y_h3h7x12CV-z8M7mXR1xPOAMXfVbA8iLd6Mzx8jNI7FfufMxmZQ6cBOnp6oHIyGb5uVMwBpmeaRRuYpCn9TNmDiiKdXKb6uRrP9Ct55ExCCLFcZ21Zc__Yu6RfYb-eSv-bBgspddzapaWYTD8hjNqVbP6vESl0RVujgyfrkDTthJqVBwxFCqIsEEOIgIrMzIPiZst-G-DguKXsl1vsA_vNPidNVgCx11Lpi1PHftkJiHkvLmjpkZQmBQPCHHqCWa6dqQwJc4ANqViozWM5EnwBT0knbkQ49BZxum50qAPq4qApjzGxyZ5CR7wAcItUGYSsNrPvBriGxPUYBgZqrp9FHAberM_phnfZcozLK_zJLuviyL6rx72ZlkVZGAgRlfavYH75DNE1Zw5qkwqeRjTm95qyssJpompSNEoKcDkC8oS8TGTtmINWVnDlf5wBuNxxW-CUM45ZR-5ZT5goUPdxPSbPMqnbUcRpxoLjSp6FBsUTLmle7svP2-hlDwqSNrcWYUU-FK4JzzR-0G00__y30000)
  
## 6. Tạo nhóm học tập

### Cơ chế phân tích:
- **Bảo mật (Security)**: Xác minh danh tính người dùng qua email hoặc số điện thoại.
- **Phát hiện lỗi (Error Detection/Handling/Reporting)**: Xử lý các lỗi như tạo nhóm thất bại, thành viên không tồn tại, hoặc lỗi kết nối.
- **Tính bền vững (Persistency)**: Lưu thông tin nhóm vào cơ sở dữ liệu.
  
### Luồng sự kiện chính:
1. Giáo viên hoặc học sinh chọn "Tạo nhóm" trên giao diện.
2. Nhập thông tin về nhóm.
3. Hệ thống lưu nhóm vào cơ sở dữ liệu.
4. Hệ thống gửi thông báo đến các thành viên được mời.
5. Hệ thống kiểm tra mã xác minh hợp lệ và cho phép đặt lại mật khẩu.
6. Hệ thống Hiển thị thông báo thành công và chuyển người dùng đến giao diện nhóm vừa tạo.

### Luồng sự kiện phụ:
- Tên nhóm bị trùng:
- Danh sách thành viên có lỗi (email không tồn tại).
-Kết nối cơ sở dữ liệu thất bại:
 ![](https://www.planttext.com/plantuml/png/b9InYXin54Nx-OgB-_q15s5934v8S8grSLgDHbw97Kj6ep5i6L9i4LAO52cpWma1Wyb2qcHKkD3Y_z0Nv1U2PkprJDQBIJVmvfvxtzEJ_jZDUMQ8DlaqZGWrIcF82ELClzKN9a-OD20PHb6iSfaGVOqnYrz9m_I4K1PAuuWgQRHAqTSgdrqmFHTrfHybn92OP0oz_GV9q7iG39GH4q694KesT8Ce6k7i6SPTlE3UVfBe37rPA4ZkVauxqJWKHrsy5Dv-a33Ssu-OA3s5EVpsW1XmNwvdCDpzafSmGjPrpDqj4Y8vCbTG7kgtacCkt4hM3lqk-jwk1QxTAWVrvVUyPK1IWw5RxNbNEmFjVilBckxj3wJ2sviStDlb3ActDn40z8D1huitsxlyQ3G5kYsGUVkrYQcqFPpLwTwvWaA6zYJI7IZqG0FkO3FOzx7pYLsXSB_mvKQ21aIhzI0Rx0OyR0csTzukAIuhrax_I5evZhiOQbykCVVsFOpsPH7wuwuGZpCUFSrcr7eczUHRQfPch7a2SQMivj_Eqe2btduHC4-BZiQfLPs6r_t2BM6y_IohPA9Jf-aTNwWQS2BK4ykuNopUtg2JO_iN6Z6PHDNIllRbna1wkn17jop0ocy6SMYi5Vhv0Nnr0l8_8SDbQLuoxkqQQUKUGfypcOJdwIy0003__mC0)

## 7. Tham gia nhóm học tập 

- **Bảo mật (Security)**: Xác minh quyền truy cập của người dùng trước khi tham gia nhóm.
- **Tính bền vững (Persistency)**: Lưu thông tin thành viên mới vào danh sách nhóm trong cơ sở dữ liệu.
- **Xử lý lỗi (Error Handling)**: Xử lý các lỗi như mã tham gia không hợp lệ hoặc nhóm không tồn tại.
  
### Luồng sự kiện chính:
1. Người dùng chọn chức năng "Tham gia nhóm học tập" trên giao diện hệ thống.
2. Hệ thống Yêu cầu người dùng nhập mã tham gia nhóm (hoặc chọn từ danh sách nhóm được mời tham gia).
3. Hệ thống kiểm tra thông tin mã tham gia:
4. Hệ thống Lưu thông tin người dùng vào danh sách thành viên của nhóm trong cơ sở dữ liệu.
5. Hệ thống Gửi thông báo đến chủ nhóm và các thành viên về việc người dùng mới tham gia.
6. Hệ thống Hiển thị thông báo thành công và chuyển người dùng đến giao diện nhóm học tập.
### Luồng sự kiện phụ:
- Mã tham gia không hợp lệ
- Nhóm không tồn tại
- Người dùng đã là thành viên
- Kết nối cơ sở dữ liệu thất bại
  ![Tham gia nhóm học tập](https://www.planttext.com/plantuml/png/f5M_Qjj06D_r53yyjKDUm4C9hS4jQRKqnkruFYdIOUbaf9F1SuSCfOFfq2aqmfH083JGGgbkyA3WzxWdw2kKqqcs7Ck9IpUX-tv_lk_xdVH7BeyJGMAHXe55g8XY318t1aami4PHoXqIpp1qHw-uSECpGbrzDBHen4KS1UZ7KJfvwyPJPaxwbaC46P74HQz-80bwQu0T2NR6A14iuWsSRLa373t3i8iNlfAVE3gdFWdXCGBk5pz2wBSKGkKtauurrBM3BjuNroceogzIS5yV8ImM4Dl89twaybyKr12RbtVprQsI2ufGoGlsTArkxwCnclqk-ahUCCmsocEcv8SG8YPRCAkl0RqkJjhFCIqk8MALPzo3y8kCLK8a47ZJBFILN4mGA7bUOam3GidFNCyZOnO0z71a_BqhCcgcmJNjJytEU8EaBA_DlLxTfiqoxkcvN30unM_kQRq83k4-aYAZlgwyv3wchBYk9hbVFAYeDO1gWOsmNO-nKXuLMOIxkSgNl5pJLTMaRfTgogPkIMDN2MZfjY8h5fibUrfi8p_iuhHHk-EnZjTBlJdDg-J7BVOcmfZqqrbPMpNXCHB1OKgUrsDoWyJTNklO4DvRp7gKJOU1abzOcPvsKB_gQdUe9N9_KuQuyx2lZZ5lbokfJlV6RzSsVmZtlyxtcQezRyUvJ4MWxztzFBKcc1-ARalLOVwVw_lVpWogv5NrzUbOBdUiyjDmelAb05Topa1N6H8bly9HyZi2dJTzvLJ-JM1qw8mnVeJnqIR-oP9fvTZbZlxd_0K00F__0m00)
  
## 8. Tự động sao lưu dữ liệu hệ thống

### Cơ chế phân tích:
- **Tính bền vững (Persistency)**: Sao lưu dữ liệu vào cơ sở dữ liệu dự phòng hoặc hệ thống lưu trữ đám mây.
- **Phát hiện lỗi (Error Detection/Handling/Reporting)**: Báo cáo lỗi nếu quá trình sao lưu thất bại.

### Luồng sự kiện chính:
1. Hệ thống kích hoạt tiến trình sao lưu dữ liệu định kỳ.
2. Sao lưu cơ sở dữ liệu chính vào cơ sở dữ liệu dự phòng hoặc đám mây.
3. Kiểm tra tính toàn vẹn của dữ liệu sau sao lưu.
4. Ghi nhận trạng thái sao lưu (thành công hoặc thất bại) vào log hệ thống.

### Luồng sự kiện phụ:
- Nếu sao lưu thất bại, hệ thống sẽ gửi thông báo đến quản trị viên để xử lý.
- ![Tự động sao lưu](https://www.planttext.com/plantuml/png/d9EzRjH058LxFyLvWOZU1OgibL8iMgqqUO7PiV6COiyau_6ABH45HQfKbAo941AmuYyDdYB5H7cF-mIy0Xel8GwRI41fNPzplkDx_SDVxZUEMzVMLSA5CnPirRYYPa8MULiL5hm1OuamsbbJ8UFYg3rcXLqgKSHPbkJSyGLl2iojghbTJMwUUOFvP3J_fNN6ydAhdTuQpunJJvNWJXazifyb2MFOUuminJHiX8Gqr7SEJb5_gU5i-AWb6cvGNNzkSNL6_bHB797_bcHHE9zaAGvjkyApblgt3ZdvJwWK-PSj7FaF4DST6lAlxqo431ij4ruvJCQ2aP6JOQqbHBZGPG8WHc5lotfegJ_7alppiUlmra2LJLcA9v5u7BeCQtC_Jax-2uvb-AhBHrTdeQjHXpUhmIyYifl-EqotYIccYloB6ivokDWEpeIrnfBwxng2_3k-0_jRpbYA0wbGcHBEKj_fCePrQZUog9fYJ3Hyh0NrdVfxouSqinG7v3T3weKkiGYTYKkFjt3IKdyUJuByAPOglDTR79qd0zA3H_1dscYFMVIloBzITrP_xqx_eS__T8azzWkTnr_r9m000F__0m00)
  

