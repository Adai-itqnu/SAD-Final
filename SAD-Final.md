# 📑 Báo cáo Phân tích và Thiết kế Hệ thống

## 1. Mô tả tóm tắt bài toán

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

### 1. Cơ chế tính bền vững (Sustainability)
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



