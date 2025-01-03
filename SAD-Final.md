# 📑 Báo cáo Phân tích và Thiết kế Hệ thống

# 1. Mô tả tóm tắt bài toán
  #### Hệ thống iLearn là một môi trường học tập kỹ thuật số (DLE) được sử dụng để hỗ trợ việc học trong các trường học có học sinh từ 4 đến 18 tuổi. Hệ thống này được thiết kế để thay thế một hệ thống hiện có (Glow) được xây dựng đặc biệt cho mục đích này và bao gồm các ứng dụng riêng cho email, v.v. Glow là một hệ thống khép kín, nơi người dùng không thể giới thiệu các ứng dụng riêng của họ. Hệ thống này ngày càng ít được sử dụng vì các tiện ích trong các hệ thống miễn phí vượt trội hơn nhiều so với các tiện ích được cung cấp trong hệ thống khép kín.
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

# 2. Phân tích ca sử dụng

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

## Kết quả phân tích các ca sử dụng:

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
  
 ![Login](https://www.planttext.com/plantuml/png/R9CnRzGm68Pt_ufNDu54_q07LEb0G5lTqeCotE8cnhQI-tnAd4eLOkfm0zDDJ4YDEe5qKf5OI8ORNFL_-1Vm5oexD62L9N6Szts-z_kS_Evt1xNbbMsM9Il51mjhK6cfB79TYSngGupnp9eARsjHWTUOpEJTZU-_QkJk5ya92pfEiXGukQYjME8Z0u2c5Xcl1IOpvRlj2jPz9znkRYz9WeQjStU5fU-s5eNotRTc4lXlQDNObF3UjHciylsFS7C_IS9gMj0Jwwuq2cLyTqtF4jJJo7h7IvrpArBSt7UjmU7f7DOKWcACykwcMP2jGiZCc4ABEX8EJ-UfUQgQ2zzVXbPyjoD8pGroxVir8LDkIohwPlnSoqULN-je3QryVkZapBK6fU-_w6XyMLMcIbslb4Pfv20AQGsKxzSHio4PRST6_iTvvBkT1Vb-ep4zUN6Cir1OQjU6_CPtBIqe2LN66iLVNwHF3T60_yHO_13szfx_EQbuZS_Zj1yMSJVCUH_pyTX2zkjLABHcuLtGZDDAdB5YwYs6vJ-8GHJaumWIo1WT-tWqZjWjOmU2yl07t0C00F__0m00)

---

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
  
 ![Đăng ký tài khoản](https://www.planttext.com/plantuml/png/X5InRXCn6Dxz59yoWTJc0JAWGbD1HSZ0bOg1nVYSEoiNN-JpLKI80NNemDI92QbL1mHIH95OY8KwNDNty1Fm2iWEIUmaWkdit_w-__-_xp__DZTxbQPArwE257oWeKieaUKQgL2SQL5AGYZJfSABYYlG2gr-TdTjpIU1jFafinPnzwZC2evaKca-mbi207N56QquMaUgde3PsNICJD0IgR3cJEBs_FPKPXWslrgEzY5ZlAfYP3_tA9qtFsG6BKBGAtdlgFagTt0megBOmJCxcseCSplxKhVRxVkUz52EQtqe1sNC-rHOSpg2LXIwcSeSkJLNOnJMd85Pyva6AJtFCIr4IZNVfEhTNTTXWIVDHOdzfDlpk8IUy2xLDCOySUabT6xDXmNsTNDP1jsvy8NCmToXf-gNMWmcIRr5flsyddZ64slUHngptBNdyS_vtD5_b59Oyr4WjUOR2eUlCPmNjv8dAEL0gL9vWVzBERIp6mrfpRbOQHEmT1_558-jcGfmPopUD9SCqWt2niWaNARU_HZzqY5S-k_iBySQxfWhbzaZtn7Y1tjtzy5Y1ESV7rdDptBbuz4ya73dZnUseuDkeEPAHhAyuQyl-rYkV3osFDhvywMbcnMiMxHMoN3TLn9N57c33dfRRGoa2oH51mbrASJ2Dcy22Q_uhlrZiH6Es-pCV--mqks0gDNvuPOczxXCtLFt1m00__y30000)

## 3. Học viên tham gia khóa học

### Cơ chế phân tích:
- **Tính bền vững (Persistency)**: Lưu trạng thái đăng ký khóa học của học viên.
- **Quản lý giao dịch (Transaction Management)**: Đảm bảo quá trình thanh toán đăng ký khóa học hoàn tất hoặc bị hủy hoàn toàn.
- **Định tuyến tin nhắn (Message Routing)**: Gửi thông báo xác nhận đăng ký qua email hoặc thông báo trong hệ thống.

### Luồng sự kiện chính:
1. Học viên chọn khóa học muốn tham gia từ danh sách.
2. Hệ thống kiểm tra tình trạng khóa học (còn chỗ trống hay không).
3. Lưu thông tin học viên vào danh sách học viên tham gia khóa học.
4. Gửi thông báo xác nhận đến email hoặc thông báo trong hệ thống cho học viên.

### Luồng sự kiện phụ:
- Nếu khóa học không còn chỗ trống:
  - Gợi ý các khóa học tương tự hoặc thêm học viên vào danh sách chờ (waitlist).
  - Gửi thông báo đến email hoặc trong hệ thống khi có chỗ trống.
    
 ![dangkykhoahoc](https://www.planttext.com/plantuml/png/h9F1IiD048Rl-nG_ETb3Ny2353meA5xw1EicPfSs6qWcHH5FddleoPDWy5OiL2i8MQI7XRx7Fa5VGT8aK95A2htjuPlv__bdTcsMlPHuGbaqPCFWXa0n4XLAWg-IG92ADMDSK9p0EtTcB31ITgezy1Hzoln04sCbo7Ku3E3rxr8A8W_t302EJgKpOus1j0kEyYqGPSvCD4Zo2A7YdGgyKCuyHg24W-oRbg345RaEjqjhz78rpq3IVkeGf3H6zYM6pxL4QdCXQvcDpRhYp9cPQagkRHxZrkO2MhfYjiMyAjZlNrvfDL-L9iYPTyZO5L-YR3ED_eWAwSppJhc1L11siQ6Uoj7CH8STzi1OdI6wtPDsQRM1gcxj8cs7LHttIHx7k7B5CeEm7xeQV2-jW-m3ZGdfYYKrBlOQep7ptm4ToEmEgHt7mtg1zijl-mC00F__0m00)

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

  
![Giáo viên thêm bài](https://www.planttext.com/plantuml/png/b9JFQjim7CVlVeelkNI3vGLoA1sb-qFB62JRtP7LICIMF5lsA6E7iaCEPR2UTkXX2Q671KfxA0oimmuAUGyzmLvXo4wMs6d6ThD-aZ_wVltzub_wvq6g_4HbKUY5z5H1IIHym1G2db2Yk1IUvnCb4_IeJnXDuATeFUTc8f5pCnCjptC7VJ48ARfdgQ8HFdW0aAMK-2b5wv1P_LbWhyVCB4BVZ3dSX22o-ehljHooIqDArDCWEA5fAaKTSCoj_XH19JxUPMTMdmimMqm41Xiw7EMGKJ9S2drDauYdAM_2NZ5RtCHGpDoB0HGNcueUAMvc6UQNLfy_GMJkeMmnVLp2ZuIYIINlfJYLTMhF5bEEqCm4bCE5tEfH1YPjyOCWvm6L9UHD74e_UCP3kjEYk_n2C0JEuW2v6MDeRWY3Oeixgwy8bDMZkCIzzKCU-8fk0qyMTzaEaxaPIv351AdLtn1OVRkKMoNXvtINonTEfO1YLb-iu7qNWM9cB1Y8crGK9jztCq9ecluZ8hJwAw-iOLZDcTNJs6sC_Z2TqQCaaSb_KSFoOoHMtwx5-VaIzD7pLjrkj_UtcjXObsTszEpXSVb6eppeOFx5fJabY9dv7l_jtPflT71S-PjVrW1UyufsUt-pRkl7SgVMdCr5TMMj1EYWL-Qo3iHhd5ZfN6N-0BBXeY9k9RqJlCeB7LJTTd6wn8jhXRuj9jmxe29mVxBV0000__y30000)

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

     ![Gửi thông báo](https://www.planttext.com/plantuml/png/b5InQXmn4Etr5SCrhanw5y7XC74H7Epp3woryahStiZMpbuuZ8kGyWWaLKZdZKbZE0X98B0gNCZaF_G5_WMZrGNltkuLwQJHp9lttWnwjFVx1IM6obdESd5EG1gCoYH1gepWf3Gobd3I1bwbCuMG530wBdrzYq36soNCbRl35vbobOxd4MEXCi4i5p1P52HcSCK00Cf2yAGGC1fBRpyYxBpsTgM0fFkD6PovIk-CGeE9o0Md8qtgNF6auJ1KZjBzca4uyzWPfFRr7mxSLU7n6xRGJWHN5qeW5Lsi8-dhrGMWjryLf2LcC7Stm6E7gRj32LbWsK0T80apraW2gGlpyCdR9KgWSk7hUsnhQYfFT4bYkwAU4N1P9a47ZnpMGZ3T3l7cxuyISc-NN4BXxIhIxX6P9FCEZqDLa3QBBjQXylP34146d7lxHRMjW6d49EbkK08FbuWjzRknJ115Vc2CDbtGK_dCAgYBY5FfAXuj4cGMRqaAiyOes3LZSUjsTryERKK_rCfiJNmpq6HrXjc-DA_zWVKYwruRGvbi16BMiEkm1wSj4zbmxOQhJP6llnES-RfIhFVUqE-P2NimTZ__xNHZEnl8-W-sswe7-3PqkQzluU6pj-_Bi5hF2lO5fk43UW800F__0m00)
  
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

 ![Tạo nhóm học tập](https://www.planttext.com/plantuml/png/V9InRjim48PtFiN1IwQWkuSYW1FOHPmiJhiprDaa8f46UN8H59qwP2WoPEhO6Dq212tGBZ473oho7do2la91sauiMScemtq__xl_e7z-UU28MogBdEKu9Y03LaqaGQOi2b96CyO56Gll7LhW3ZfzLSqDp5HrfzyCWhyMu9IM7SOYmFKaHnXTEi82FZ40WDAXu0wXqvF1NslOEmkBkG4jgz_5NYTAZZ17GJsBdB1lJJcjSwSoBEwdGBBweoT0Ig_OX1vfGfkOTtfiwjon2lvB0MGvK7Mtfe1izQ0d2Uv951U7vJHNeltbBOMCQmckcWiPZTngkTf0qld0SvLnmXCipj6wkiRmyLUvVdfMtHeGZtDmmN-7BFYVaAlWhyhL5lYipKC_-7kr6VuyhlxlJLWizQwDKqDgVDbgOX07YKZmNsjQQn4HAoiNqdmSbKAWSoVe79_WAqfvyD_K4tPahR7iCsFfLFRttxO4krD9VOqKwv-feosgbbhgRSG1NJXUdqwA_aNkQGRembdpO5XJDH6RoA0BW-1_JED6hjfRjyI7SMqlNHHx5erSBTHeR2kmHklk4nTXiIJGmTyew8qEXwokje4QUH-Wpk8FuJy0003__mC0)

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
  
  ![Tham gia nhóm học tập](https://www.planttext.com/plantuml/png/X9JDQXin58NtUegBDrdb1Rme0TUaFxQxcBPxHRuUYSn8HjB43QMhBheeXOOkkYY512y2XO2XXLBF8einVWyzGL-XI3DEvyTfbxhSy-dSgpFpExyzCfPgcwK9IN1cmIhG8kOMfa8Ziq99GYYpIiCBWngeWTuatgvS_bN0jFWbunuXlf7AE468pet555uJ083C8AC6eJVWBlyWuU0vfod4WeBanVSKV9M1TUkR-K7FaoDCaDadIiXZhR9v4pBXlX7IOWbsn-7AhNyoO2K_K0DeA2tgm1YeAJOvJuNBtwPWDMsmWkubJSIKMlo_rBhya_JUhmGmbrzNCmNAW2Cx3OZXAs7i_GnUN4eEPwBu9c5pqJOJC6DCJr0RBbhR66rNcGVya35O8PkirELVHBbHUeObuh6SgIRYsEKtOiSuAQuKR2xS-bQ6TLxNvfaeAsRdOQ1d2ucwYNda1_86NFw-GQiiCLyfpN2rY3B6q9Wn6aDZ_0SfSVddQWQk5aEjbIPl20aXF3nyqCbAwnnwMZ5e7aD7zy4xbT3NUbBemxXO-W0lvzxfktjaqSvw9JWjrrFJjS5tb_rzUEZ397mljSpjrTLlcmH5TLz7M8C7OICbq8S1twvyFiiqxjVKBjjyB9QG59UD598MrOiwIMeNxj2jdEnXrGsCV5XW43qSaIEKK_yp-mC00F__0m00)
  
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

![Tự động sao lưu](https://www.planttext.com/plantuml/png/T9AzIWGn58NxFCLXUr_0GjH6H155iO-psIGuasZcpi8YLXOMLbQsEuYDiFZRE2csYFWUUG9VGJB-i3jgUNFF-NBlITxzTBaaxgWgSfQB0O4id9QAqDTEPAIjOOndP1rM-eKsu2LwErLihWt8HN-1eGwtfiUIc1kP2wpoxB0wsXsL90gSC02eIf7nKg2t4IQPWhAngGabjyZVxYkyNaP_OHGEet_gfHlsd9PIk4_IF67tszIF_WwvZlwymZ2CRJfum94AZqQsa6tX1jOLVq4sTFHd1SXnK9WO1R9XR32CpOkP1RUSVU7qOBHkI4YdQJHFMbCQkPKfYwOs4gH2hNysQ_sRLdv5GfogikEFVgAJwzb878JQ8e_-IgT8cgd1yU-a4tBBaXwCsWTXfupDnOM5XQNExdDLs-_krAbRJMTkB69FXR5HoDAmVrfcvchbiRaX7CIcrcosbQJVedy2OCl2zDEd_0000F__0m00)

---

# 3. Các phần tử thiết kế trong hệ thống iLearn

#### **1. Phần tử giao diện người dùng (UI Components)**
- **Trang đăng nhập và xác thực**: 
  - Thành phần: Form nhập thông tin (email/password), nút đăng nhập, liên kết quên mật khẩu.
  - Giao diện thân thiện, hỗ trợ xác thực qua OAuth 2.0 hoặc SSO.
  
- **Dashboard chính**:
  - Thành phần: Menu bên trái (dành cho các mục như tài liệu, khóa học, thông báo), khu vực hiển thị chính, bảng điều khiển thông báo.
  - Hỗ trợ tùy chỉnh giao diện theo nhóm người dùng (học sinh, giáo viên, quản trị viên).

- **Trang khóa học**:
  - Thành phần: Danh sách khóa học, nút thêm/sửa/xóa khóa học, nút tải tài liệu.
  - Hỗ trợ hiển thị lịch học, bài tập, và nội dung khóa học.

- **Trang quản trị**:
  - Thành phần: Bảng điều khiển quản lý tài khoản, danh sách học sinh/giáo viên, công cụ thống kê.
  - Giao diện quản trị cho phép thiết lập cấu hình hệ thống.

#### **2. Phần tử logic nghiệp vụ (Business Logic Components)**
- **Xác thực và quản lý quyền**:
  - Thành phần: Module xác thực dựa trên JWT, phân quyền dựa trên vai trò (học sinh, giáo viên, quản trị viên).
  - Chức năng kiểm tra quyền truy cập theo từng nhóm người dùng.

- **Quản lý khóa học**:
  - Thành phần: API xử lý logic tạo, sửa, xóa khóa học.
  - Tự động gán tài liệu, bài tập khi thêm khóa học mới.

- **Thông báo và nhắc nhở**:
  - Thành phần: Hệ thống gửi thông báo qua email, giao diện, hoặc ứng dụng di động.
  - Tích hợp cơ chế định tuyến tin nhắn với RabbitMQ hoặc Kafka.

- **Hỗ trợ thanh toán**:
  - Thành phần: Module xử lý giao dịch qua Stripe hoặc PayPal.
  - Tích hợp logic đảm bảo tính toàn vẹn giao dịch (ACID).

#### **3. Phần tử dữ liệu (Data Components)**
- **Cơ sở dữ liệu người dùng**:
  - Thành phần: Bảng người dùng với thông tin cá nhân, quyền hạn, lịch sử hoạt động.
  - Dữ liệu mã hóa (AES-256) đảm bảo an toàn.

- **Cơ sở dữ liệu khóa học**:
  - Thành phần: Bảng lưu thông tin khóa học, tài liệu, danh sách học viên.
  - Hỗ trợ tìm kiếm và phân loại khóa học.

- **Cơ sở dữ liệu nhật ký**:
  - Thành phần: Ghi nhận nhật ký hoạt động, thay đổi tài liệu, lịch sử đăng nhập.
  - Phục vụ mục đích giám sát và xử lý lỗi.

#### **4. Phần tử tích hợp và tương tác (Integration Components)**
- **Tích hợp dịch vụ bên ngoài**:
  - Thành phần: API kết nối với Google Drive, Zoom, Microsoft Teams.
  - Hỗ trợ tích hợp với hệ thống quản lý mạng trường học hiện có.

- **Hệ thống hàng đợi tin nhắn**:
  - Thành phần: RabbitMQ hoặc Kafka để xử lý thông báo hoặc các yêu cầu giao tiếp giữa các dịch vụ.

#### **5. Phần tử bảo mật (Security Components)**
- **Xác thực**:
  - Thành phần: OAuth 2.0, quản lý phiên đăng nhập với JWT.
  - Cơ chế kiểm tra đa yếu tố (MFA) để tăng cường bảo mật.

- **Kiểm soát truy cập**:
  - Thành phần: Module quản lý vai trò và quyền hạn dựa trên Role-Based Access Control (RBAC).

- **Mã hóa dữ liệu**:
  - Thành phần: Module mã hóa mật khẩu và dữ liệu nhạy cảm.

#### **6. Phần tử hiệu năng và mở rộng (Performance & Scalability Components)**
- **Hệ thống cân bằng tải**:
  - Thành phần: NGINX hoặc HAProxy để phân phối tải khi số lượng người dùng tăng cao.

- **Khả năng mở rộng**:
  - Thành phần: Hỗ trợ triển khai trên đám mây (AWS, Azure).
  - Module quản lý tài nguyên để thêm bớt máy chủ tự động.

- **Cơ chế giám sát**:
  - Thành phần: Công cụ như Prometheus hoặc New Relic để theo dõi hiệu năng hệ thống.

#### **7. Phần tử giao diện cũ (Legacy Interface Components)**
- **Thiết kế tương thích**:
  - Thành phần: Giao diện tối giản để hỗ trợ người dùng thiết bị cũ.
  - Module kiểm tra khả năng tương thích trình duyệt.

- **Hỗ trợ nhập liệu từ hệ thống cũ**:
  - Thành phần: Công cụ nhập và chuyển đổi dữ liệu từ hệ thống Glow.

#### **8. Phần tử xử lý lỗi (Error Handling Components)**
- **Phát hiện lỗi**:
  - Thành phần: Module giám sát và gửi cảnh báo khi phát hiện lỗi hệ thống.

- **Xử lý lỗi người dùng**:
  - Thành phần: Hiển thị thông báo lỗi rõ ràng và gợi ý cách khắc phục.

---

# 4.Thiết kế hệ thống con cho iLearn

#### **1. Hệ thống con quản lý người dùng (User Management Subsystem)**

- **Chức năng**:
  - Quản lý thông tin tài khoản (tạo, sửa, xóa).
  - Xác thực người dùng (login, logout, MFA).
  - Phân quyền theo vai trò (học sinh, giáo viên, quản trị viên).

- **Thành phần**:
  - **Authentication Service**: Xử lý xác thực bằng OAuth 2.0 và JWT.
  - **User Profile Management**: Lưu trữ và xử lý thông tin người dùng (họ tên, email, vai trò).
  - **Role-Based Access Control (RBAC)**: Kiểm soát quyền hạn truy cập.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Users`**:
      - Cột: `UserID`, `Email`, `PasswordHash`, `Role`, `Status`, `CreatedAt`, `UpdatedAt`.
    - **Bảng `Roles`**:
      - Cột: `RoleID`, `RoleName`, `Description`.
    - **Bảng `Permissions`**:
      - Cột: `PermissionID`, `RoleID`, `ServiceAccess`.

  - API:
    - POST `/api/auth/login`: Xác thực và trả JWT.
    - GET `/api/users/{id}`: Lấy thông tin người dùng.
    - PUT `/api/users/{id}`: Cập nhật thông tin người dùng.

#### **2. Hệ thống con quản lý khóa học (Course Management Subsystem)**

- **Chức năng**:
  - Tạo, sửa, xóa khóa học.
  - Quản lý tài liệu học tập và bài tập.
  - Gán học viên và giáo viên vào khóa học.

- **Thành phần**:
  - **Course Service**: Quản lý thông tin khóa học và logic liên quan.
  - **Resource Manager**: Quản lý tài liệu và bài tập.
  - **Enrollment Manager**: Quản lý danh sách học viên và giáo viên.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Courses`**:
      - Cột: `CourseID`, `Name`, `Description`, `TeacherID`, `CreatedAt`.
    - **Bảng `Enrollments`**:
      - Cột: `EnrollmentID`, `CourseID`, `UserID`, `Role` (Student/Teacher).
    - **Bảng `Resources`**:
      - Cột: `ResourceID`, `CourseID`, `FilePath`, `UploadedAt`.

  - API:
    - POST `/api/courses`: Tạo khóa học mới.
    - GET `/api/courses/{id}`: Lấy thông tin khóa học.
    - POST `/api/courses/{id}/enroll`: Gán học viên/giáo viên vào khóa học.

#### **3. Hệ thống con thông báo (Notification Subsystem)**

- **Chức năng**:
  - Gửi thông báo sự kiện (qua email, giao diện, ứng dụng di động).
  - Tích hợp với hệ thống định tuyến tin nhắn (RabbitMQ/Kafka).

- **Thành phần**:
  - **Notification Scheduler**: Lập lịch gửi thông báo.
  - **Message Queue**: Hàng đợi tin nhắn xử lý đồng thời.
  - **Delivery Service**: Gửi thông báo đến người dùng qua email hoặc API.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Notifications`**:
      - Cột: `NotificationID`, `UserID`, `Message`, `Type`, `CreatedAt`, `Status`.

  - API:
    - POST `/api/notifications`: Tạo thông báo mới.
    - GET `/api/notifications/user/{id}`: Lấy danh sách thông báo của người dùng.

#### **4. Hệ thống con quản lý tài liệu (Document Management Subsystem)**

- **Chức năng**:
  - Lưu trữ và phân phối tài liệu học tập.
  - Hỗ trợ tải lên, chỉnh sửa, xóa tài liệu.

- **Thành phần**:
  - **Storage Service**: Lưu trữ tài liệu trên nền tảng đám mây (AWS S3, Azure Blob).
  - **Document Manager**: Quản lý metadata và quyền truy cập tài liệu.
  - **File Uploader**: Xử lý tải lên, kiểm tra định dạng.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Documents`**:
      - Cột: `DocumentID`, `UploaderID`, `CourseID`, `FileName`, `FilePath`, `UploadedAt`.

  - API:
    - POST `/api/documents/upload`: Tải tài liệu lên hệ thống.
    - GET `/api/documents/course/{id}`: Lấy danh sách tài liệu của khóa học.

#### **5. Hệ thống con thanh toán (Payment Subsystem)**

- **Chức năng**:
  - Xử lý thanh toán học phí.
  - Quản lý trạng thái giao dịch.

- **Thành phần**:
  - **Payment Gateway**: Tích hợp với Stripe hoặc PayPal.
  - **Transaction Manager**: Đảm bảo tính toàn vẹn giao dịch (ACID).
  - **Invoice Generator**: Tạo hóa đơn và lưu trữ lịch sử thanh toán.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Transactions`**:
      - Cột: `TransactionID`, `UserID`, `Amount`, `Status`, `CreatedAt`.

  - API:
    - POST `/api/payments`: Tạo giao dịch thanh toán mới.
    - GET `/api/payments/user/{id}`: Lấy lịch sử thanh toán của người dùng.

#### **6. Hệ thống con bảo mật (Security Subsystem)**

- **Chức năng**:
  - Bảo vệ dữ liệu và hệ thống khỏi các cuộc tấn công.
  - Mã hóa dữ liệu nhạy cảm.

- **Thành phần**:
  - **Authentication Service**: Quản lý phiên đăng nhập với JWT.
  - **Encryption Manager**: Mã hóa dữ liệu (AES-256).
  - **Firewall**: Tường lửa ứng dụng ngăn SQL Injection, XSS, CSRF.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Sessions`**:
      - Cột: `SessionID`, `UserID`, `Token`, `CreatedAt`, `ExpiresAt`.

  - API:
    - POST `/api/auth/refresh-token`: Cấp token mới khi hết hạn.
    - POST `/api/security/verify`: Xác minh tính hợp lệ của token.

---
# **5. Thiết kế các lớp**

![](https://www.planttext.com/plantuml/png/b5LDQnf16BxxAuOzjG43kIwX1BKOY9461x77HUtEW3iRrjb2QNi8EPQ2FPJIGy559218IvDBPmWvZFH_lB-WVw7igZipxXh8qUTzzfdd_VIVV3WPSo_YSJ2gz4VUU8pQ_jzV87_GXlh3VFI-Wb0LdQkP1Rk8Cfv5i5em5urvH9cV0Iy3ZuuifEjH7AdV1eRGQhAwPdwRW5XUFdlkehSX7HY1NWnYpgr0FQLc7t1Cr1tpCMKvuMDbOxv9LH9sgLgmp3b2TG9Y7jJKb5fg5p686Mkf-pEYRhrJa9_xHR4Cxb16DbfjaDyl2rAzOR2QK93NGL51g-j2QiokeeaRrJjNTnZ4pC8Q7YCTbVH9xj15BJhcnrQJNcHSNP5N1EGSH-bthjtbB0zCr2B81UqKjywiI9vbBGRvbUwaQO16dYHziqazLWFnawyc86vY5mqyFkGq6Evmpa0yfCqM_HsApgcOo5EgWv1XmyfOFrsIhah2kaf28zSDOYHArI9UJK1UMOrB9uWsudI1Z6N0899mgr5yBv_LDb6tWR6HwKzxXZQGyI8cQih8fbRxgf2rtc0McbyMCzVa6uv0phIrrseHrzUztThhWfYpOaLm129XFYOgeSMYv3gMeoO5CQCNyRkqIKMASGoyi07oKvzePnhJrZeWls0AyegvwCqezFZZpdeWborrZud720vLOfVhD5HJjbOhEbfVhhJLsf76jAEoEQdcevvTmPBHHwW9Sacre6d0Fkl77whc6fL5y-sf65VCENBGGRMAdAF3mmDdnq4fpp6VCI-5ynHAoMlv6ff2DcLdSnwLqrEyNyyOgFqaeyVxIIT3DaZ_Sly3003__mC0)
