# 📑 Báo cáo Phân tích và Thiết kế Hệ thống

# 1. Mô tả tóm tắt bài toán
  #### Hệ thống iLearn là một môi trường học tập kỹ thuật số (DLE) được sử dụng để hỗ trợ việc học trong các trường học có học sinh từ 4 đến 18 tuổi. Hệ thống này được thiết kế để thay thế một hệ thống hiện có (Glow) được xây dựng đặc biệt cho mục đích này và bao gồm các ứng dụng riêng cho email, v.v. Glow là một hệ thống khép kín, nơi người dùng không thể thêm các ứng dụng riêng của họ. Hệ thống này ngày càng ít được sử dụng vì các tiện ích trong các hệ thống miễn phí vượt trội hơn nhiều so với các tiện ích được cung cấp trong hệ thống khép kín.
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

## Yêu cầu hệ thống

### Yêu cầu chức năng
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
## Biều đồ ca sử dụng hệ thống Ilearn 
![Use-case Model](
https://www.planttext.com/plantuml/png/T5J1RXCn4BtxAqPxxo-WHa5gG14A9N15pkxKjf8THxQt4aASE72eaCYnuaA5SgdegN1P2_Mm-H5_0R-0TfFjEflqEizlvisR6V_p3wVMSUEAVC4MUE70QJ1AI0UPCfWwfOandZfj81a5_pM5IrNTKWBSmXYv8JGjVAQg6nt1K-IfxE2937uDilX0ie4dt22v5drTXF8dWJF1NqKv1bckYB5pJ1qdiK18O1Jy5t0o-1K9UB6eDIGVMM4nvHOXsNpRV2O194Dvjsnol1s-7skXwE3DlFhRFZX7eQn3qxs9cWKdUGv2SPZBwfw3hA6M-L8h6kh2MEouaHFWP7MRmwpweI0F_hjgUOCi6wErcewNfE2lbmsj9RmfPhbo0skLeBnshYiN_9sg2_qc0REwz6OLoWVQ2etShBCWPQ-qKnSgvSrm7xDCGtcZWMHrd--8BhPmQ90xF3EwM4QSrfWdQRKzFLAq2E0aQiYgFmgSQYHlLi5V7qiqDJoTJumM1gtjaWr3kIvWLFqY2S-3lqebl0j-tRLhBbMAbdrYkss5avDdtKhqWezhq8j7G-uX1rCvmjpsptRti2-W5-oseWSSpAs7n-CveEuyODkJsnUm7zjtcJNdzwG4nawHilhd-0y00F__0m00).


---

### Yêu cầu phi chức năng
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

![diagram](https://www.planttext.com/plantuml/png/V5FBJiCm4BpxArQvLzmv8CAxKf6AIa-8m-8kmIArqzqrK11Vne5FuXUGNLfeqd3CU6Oyk-DyVNmUYY9hdDUcGVk85K4n7S88byG5l1c0cwaGmz0hyJrQkatGSHGDS_UAweBFo167vmqFxGf_Dx-cPTFKpcR1bljH5ET914QXSZPxbL4VoEkQFI5-SkkBGsGXk4IF5St9QqRFESIc3PRZOKvJCNRJdA3YLem4t67NEXCdP2CxNMRaAX8lrw4asvhsZc0mEEYC1ljGNA2VrIJ0j8WaAeLfxR9NMSwmKO7fi30xbzqhl6PNLSG2z4G-tMWwh2pjsVhVr7Med2zwzDrgadJrAM3pgVI9Emt-rLRfi5TQjdfEojCN9VPOW_pKbARk4BDyL_79uepKFknDD33131KBivkwCVbz9Jc1byWaq71GoWtzQz1wLCbXpC6I20ai8h5BCnoIdwK_zHi00F__0m00)

---

## Các cơ chế phân tích

### 1. Cơ chế tính bền vững (Persistency)
Đảm bảo hệ thống hoạt động ổn định, lưu trữ và duy trì dữ liệu để có thể truy cập được ngay cả khi ứng dụng, hệ thống, hoặc thiết bị bị tắt.


---

### 2. Cơ chế định tuyến tin nhắn (Message Routing)
Đảm bảo thông tin và yêu cầu được gửi đúng nơi, đúng lúc.

---

### 3. Kiểm soát và đồng bộ hóa tiến trình (Process Control and Synchronization)
Đảm bảo các tác vụ được thực hiện theo thứ tự và tránh xung đột.



---

### 4. Bảo mật (Security)
Bảo vệ dữ liệu người dùng và hệ thống khỏi các cuộc tấn công.


---

### 5. Giao diện cũ (Legacy Interface)
Đảm bảo giao diện đơn giản, quen thuộc với người dùng đã sử dụng hệ thống trước đó.


---

### 7. Phát hiện lỗi (Error Detection)
Phát hiện và xử lý lỗi nhanh chóng để duy trì hoạt động của hệ thống.


---

## Kết quả phân tích các ca sử dụng:

## 1. Đăng nhập hệ thống
### Mô tả: 
- Người dùng nhập thông tin đăng nhập để xác thực và truy cập vào hệ thống iLearn. Sau khi xác thực thành công, người dùng sẽ được chuyển đến giao diện chính của hệ thống.
  
### Các tác nhân:
- Người dùng (học sinh, giáo viên, phụ huynh, quản trị viên): Người cần đăng nhập để truy cập vào hệ thống.
- Hệ thống iLearn: Hệ thống kiểm tra thông tin đăng nhập, xác thực người dùng và cấp quyền truy cập.

### Mục tiêu:
- Cho phép người dùng truy cập vào hệ thống iLearn một cách bảo mật.
- Xác thực thông tin đăng nhập của người dùng và cung cấp quyền truy cập tương ứng.
  
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
  
### Biểu đồ luồng sự kiện:
 ![Login](https://www.planttext.com/plantuml/png/b9C_YXin6CLxdU9TO2_W8gp1iFb7cXqpjQnHHc9cfMH6Cd4PjaYHogH86GzB25amII0Ga0eNCdiFdI1N29Azu0dP8iqWzBtlq-yzQNxxtNblQ6ViLKieCxh3lESTQ8yvMMYhAjgjKFB54sLuzv8odaebOLgPJhUOMYCkURUKXyAKLDJG1UqvPlSBscD6o1ndZr1Ey494jtq54suLzklzjQgX3blBiC5LT5k3HaJtrP8ojKmdk8X-Ax4AjnOikYyMRyB0O4JqFnZ8DAbc4nITNM4PtMS58y9FLSD81HCs4etGqTqea1dE3YEBBheRBAD_-x2OjWR5wOw9_aFwka5csFqwE5MFcG4W4vKJ5D4D6a_B0aOtNEKUamzkejiPlBPfRKJOA06MA79xjZsVuFdTTvkxbs6ZmRHk9E_p42RiAlhh561qEuLQKerAHlzEWOcmLOBmjkTZ-kReyyH4glnY8mFegHoRoC37a1PXq6YZ_oX7f8zbfZ4Y-lSFIEzlwK98jBe-L8xExWRqqNz25VqtjCc69LnL9D_0inoLYduj_wd48XrQop2aE7HqWnhp_urp33zF_0yNEVYJDvXaMxGfnmnxpbML_g4_0000__y30000)

---

## 2. Đăng ký tài khoản

### Mô tả:
- Người dùng tạo tài khoản mới để tham gia hệ thống iLearn. Người dùng sẽ cung cấp thông tin cá nhân, bao gồm tên, email, mật khẩu, và các thông tin cần thiết khác. Sau khi thông tin được xác thực và lưu trữ trong cơ sở dữ liệu, người dùng sẽ nhận thông báo thành công và có thể tiếp tục sử dụng hệ thống.

### Các tác nhân: 
- Người dùng (học sinh, giáo viên, phụ huynh): Người cần đăng ký tài khoản mới để truy cập vào hệ thống iLearn.
- Hệ thống iLearn: Hệ thống tiếp nhận thông tin từ người dùng, kiểm tra tính hợp lệ của thông tin và lưu trữ vào cơ sở dữ liệu.
### Mục tiêu:
- Cho phép người dùng tạo tài khoản mới và truy cập vào hệ thống iLearn.
- Lưu trữ thông tin tài khoản vào cơ sở dữ liệu một cách an toàn và bền vững.
  
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

### Biểu đồ luồng sự kiện:
 ![Đăng ký tài khoản](https://www.planttext.com/plantuml/png/b5JFYjf07BxFKtnuQi7r0JoKfGJQOl5YhRsEIJH39fCbcInuzh27NkgfXnwgI5cw85rAJncAXyY-npn1Nw7C9Ex66fHwYiptzpU_v8_QNgQI9ZABEA6kZ1CCKpy1JJ4aupWJ7arc6FdZDqBwoOIwlZaQ4JSMCecv1G_yv9gL1mFYKKd7DFNXx1ze2kSHtuybcp2NIXQB6gzFo10NBp3gubsIpU3gV7E5AQCnFARLZS1kiPkBASBYDnaPvB2BrqohkO0CjFg8IPn4TT1UhXzOAHaKlyGKajMLy4mMTw8DFwACjn7fV2CH1Zh_dhNHwNIUbrQ3BbvfjM6O5NUPYNQR8JJU4MH2SLqimH_kive76LIytXDC5XiH8D1gVGMkrGrShMufFAr-W9kE6Q5SmddwNmCJ0B2YJXTl3yqWYoL36CGwNmj4MdrX9bCCzs65LAkl1nv6oFZiHPOYW6kax8dvERWemtyeLYw4cPzuB7WCjwdw-n5LiSR5AguFkf7Ph-wnxdF8BzQO6jb3ir6JMQD3uwRKMQtTfyQCBNkhRf3DB76tqFbM7EoZ6vZxj4u-J_tzF7N-JMAiynKxdkTBuyYr-ioEzkLyFyixNOnRwLQlaWsqclzhrC7xZ84NFol01jnaxRJA8i8Zjanz2SEItBIBPuAU2kcSScWHayI-3ZsTRoM4LWlMkC_78p-J3E4PnRFH_ojIMUNI5vxvmFu5003__mC0)

## 3. Học viên tham gia khóa học

### Mô tả:
- Học viên đăng ký và tham gia một khóa học trên hệ thống iLearn. Học viên sẽ chọn khóa học mong muốn từ danh sách các khóa học, hệ thống kiểm tra tình trạng khóa học (còn chỗ hay không), và nếu còn chỗ, học viên sẽ được thêm vào danh sách khóa học và nhận thông báo xác nhận.

### Các tác nhân:
- Học viên: Người tham gia khóa học, có thể là học sinh, sinh viên, hoặc người học ngoài.
- Hệ thống iLearn: Hệ thống quản lý các khóa học, kiểm tra tình trạng khóa học và lưu trữ thông tin đăng ký của học viên.
- Giảng viên : Người tạo và quản lý các khóa học.

### Mục tiêu:
- Cho phép học viên đăng ký tham gia các khóa học và lưu trữ thông tin đăng ký vào cơ sở dữ liệu.
- Cung cấp các thông báo xác nhận tham gia khóa học qua email hoặc thông báo trong hệ thống.
- Quản lý số lượng học viên tham gia khóa học một cách hiệu quả.
  
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

### Biểu đồ luồng sự kiện:
 ![dangkykhoahoc](https://www.planttext.com/plantuml/png/Z5FBQXin5DthAmvUjGl_W2abE0Qdf6GJWzSQMR54PpH1SsVQB4kN9GkliYfqCDs41jB7QaJ9GiN_eI_eBnHvd6IccD2TaCuvzvnxh_wukuE2kAKoInaNb5iCZeAx5AYqlpO3y0AdL2wa8NREBMcXpxaX3EOoUML8sZCkv1OrbqaVSPYNjf2dqbPw1sbl-gW99vxmeWLCnlt7avpqcHQST6wwGjlx2yPspZ1y6SkFSAY2kpHue_mFZdWMoChWLWQaU8QbvcmkamXlhOnmh8Fxa84i1_clHe5iQ6gpx6gm5Xnfa_48CrjUe0hDbwZgVvebIFTgiiaOmqwDcGtD6bLmxn_KIVbQxwrn7-M_I8odXEDEMk6_6mWLt5LakPLPCW3u9_JhpMtPzQuU1uxAVywnu4QXyBLGMte__rHf61MQcoU9FPyT3-teHfW6TwFlJII-pl7Ers8dp6HQo5wmtok_XWhD7RNnkfAxBHZXA0upJYMuZptfDBWhlPSo3MwjuNz1nEhTnQ7DxMRRzU2-xMlYJFdhxCaEHAEVyEmjrvJgWfupQHQFE_jYE7nenadRpevbnWwaMSHF-HS00F__0m00)

## 4. Giáo viên thêm bài học mới

### Mô tả:
- Giáo viên tạo và đăng tải bài học mới lên hệ thống iLearn. Giáo viên nhập thông tin bài học, tải lên tài liệu (ví dụ: tài liệu học, video, hình ảnh) và hệ thống sẽ kiểm tra tính hợp lệ của tài liệu trước khi lưu trữ và thông báo thành công.

### Các tác nhân:
- Giáo viên: Người tạo và quản lý bài học mới cho khóa học.
- Hệ thống iLearn: Hệ thống quản lý bài học, xử lý các tệp tải lên và lưu trữ thông tin bài học.
- Hệ thống lưu trữ tệp: Hệ thống lưu trữ các tài liệu, video hoặc tệp liên quan đến bài học.

### Mục tiêu:
- Cung cấp cho giáo viên một giao diện dễ sử dụng để tạo bài học mới.
- Kiểm tra tính hợp lệ của tài liệu tải lên (định dạng, kích thước).
- Lưu trữ và hiển thị bài học mới trên hệ thống cho học viên tham gia.
- Đảm bảo chỉ những giáo viên có quyền mới có thể thêm bài học mới.

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

### Biểu đồ luồng sự kiện:
![Giáo viên thêm bài](https://www.planttext.com/plantuml/png/Z58zQnmn5EprAmRt9lqMnf0hOhAuoSAcSAFLofQmLdjejGSkGuehJ8fKATpSSONXuC15gbMHGi7_u_q2_uMWs_CNd4rKIM_cpSnxw27yEUuyTxvl3EF2jmw5v4991zwXO5NRsvgxAvIoEh5UkdCkP89A9bhhNMkGowvhxHVfPdg4SbPppolUIKmUBxp3XB42XqSeCtnK57vOd1qKAguRL76XaKe23OKRVNR0oiGiCdpI5BvRU4NX6kUjQs0L3Pifl8g_xGMyjY_QdmnEto5X5XVmDAmqJ5nR-8GOJM7UVvZfMhQZUPxXSp9lu1t7tvyKhgr2JSFINcmbBkD6A7XrVqVXHi1Jc4yP0m1kF8hqJ8QhAGo5-HP89q_Yampv_Lt_Ni3dL4-j4noEmRx6fHWNOM5sEWkh89BQQwSoGp6QL77PxYVkNVOkslukQJgv6_5ovBqrQV9tDAmme_3jbQYXy4l_VuOjVRkQgxZk8MYuJNDJsC3Gi1oLfAqPEvQsJj_v7m000F__0m00)

## 5. Gửi thông báo đến học viên

### Mô tả:
- Quản trị viên hoặc giáo viên gửi thông báo đến học viên trong hệ thống iLearn. Quản trị viên hoặc giáo viên có thể chọn nhóm học viên hoặc cá nhân để gửi thông báo, lựa chọn kênh gửi (email, SMS, hoặc thông báo trong hệ thống), và hệ thống sẽ đảm bảo thông báo được gửi đến đúng đối tượng và lưu trữ lịch sử gửi thông báo.

### Các tác nhân:
- Quản trị viên/giáo viên: Người gửi thông báo, có quyền truy cập vào giao diện quản lý hệ thống.
- Học viên: Người nhận thông báo.
- Hệ thống iLearn: Hệ thống định tuyến và gửi thông báo đến học viên qua các kênh khác nhau.
- Hệ thống gửi email/SMS: Các dịch vụ bên ngoài hoặc hệ thống nội bộ chịu trách nhiệm gửi thông báo qua email hoặc SMS.

### Mục tiêu:
- Cung cấp cho quản trị viên hoặc giáo viên một cách dễ dàng để gửi thông báo đến học viên.
- Đảm bảo thông báo được gửi đúng đối tượng và qua kênh chính xác.
- Lưu trữ thông tin lịch sử gửi thông báo để theo dõi.
  
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

### Biểu đồ luồng sự kiện:
  ![Gửi thông báo](https://www.planttext.com/plantuml/png/b5J1Qjj05BphAuQS4d1-G8SIDuQqKBa76zphUhtHBf6VMcbbyB7qq4FemQVIGo5kA8KKqq0A1UcGmuRyntv1Vw6i53jIegJjGR3elPatCs_PtyNbNgfPehDfv36kumJToLJHosGe69SY0KlH7NhZEAC9I-OOYV5pqY8vP5ousiZZCUaaZj2FjJfKd6aLqq0aCrKrzBq9qspCKe7U-i1Iz3QuGAGf2nM5-v8HYSXL0y_h3h7x12CV-z8M7mXR1xPOAMXfVbA8iLd6Mzx8jNI7FfufMxmZQ6cBOnp6oHIyGb5uVMwBpmeaRRuYpCn9TNmDiiKdXKb6uRrP9Ct55ExCCLFcZ21Zc__Yu6RfYb-eSv-bBgspddzapaWYTD8hjNqVbP6vESl0RVujgyfrkDTthJqVBwxFCqIsEEOIgIrMzIPiZst-G-DguKXsl1vsA_vNPidNVgCx11Lpi1PHftkJiHkvLmjpkZQmBQPCHHqCWa6dqQwJc4ANqViozWM5EnwBT0knbkQ49BZxum50qAPq4qApjzGxyZ5CR7wAcItUGYSsNrPvBriGxPUYBgZqrp9FHAberM_phnfZcozLK_zJLuviyL6rx72ZlkVZGAgRlfavYH75DNE1Zw5qkwqeRjTm95qyssJpompSNEoKcDkC8oS8TGTtmINWVnDlf5wBuNxxW-CUM45ZR-5ZT5goUPdxPSbPMqnbUcRpxoLjSp6FBsUTLmle7svP2-hlDwqSNrcWYUU-FK4JzzR-0G00__y30000)
  
## 6. Tạo nhóm học tập

### Mô tả:
- Giáo viên hoặc học viên sử dụng hệ thống để tạo một nhóm học tập, bao gồm việc nhập thông tin nhóm, thêm các thành viên, và gửi thông báo mời tham gia nhóm. Hệ thống sẽ đảm bảo nhóm được lưu trữ trong cơ sở dữ liệu, các thành viên được mời sẽ nhận thông báo, và các lỗi liên quan đến việc tạo nhóm (như tên nhóm bị trùng, thành viên không tồn tại, hoặc lỗi kết nối) sẽ được phát hiện và xử lý.

### Các tác nhân:
- Giáo viên/Học viên: Người tạo nhóm và mời các thành viên tham gia.
- Hệ thống iLearn: Hệ thống quản lý nhóm và kiểm tra tính hợp lệ của thông tin.
- Thành viên nhóm: Những người nhận được lời mời tham gia nhóm học tập.
- Hệ thống cơ sở dữ liệu: Lưu trữ thông tin nhóm và các thành viên.

### Mục tiêu:
- Tạo một nhóm học tập cho các học viên tham gia cùng nhau học.
- Cho phép giáo viên hoặc học viên thêm các thành viên vào nhóm.
- Gửi thông báo mời thành viên tham gia nhóm.
- Lưu trữ thông tin nhóm học tập vào cơ sở dữ liệu.
  
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

### Biểu đồ luồng sự kiện:
 ![Tạo nhóm học tập](https://www.planttext.com/plantuml/png/b9InYXin54Nx-OgB-_q15s5934v8S8grSLgDHbw97Kj6ep5i6L9i4LAO52cpWma1Wyb2qcHKkD3Y_z0Nv1U2PkprJDQBIJVmvfvxtzEJ_jZDUMQ8DlaqZGWrIcF82ELClzKN9a-OD20PHb6iSfaGVOqnYrz9m_I4K1PAuuWgQRHAqTSgdrqmFHTrfHybn92OP0oz_GV9q7iG39GH4q694KesT8Ce6k7i6SPTlE3UVfBe37rPA4ZkVauxqJWKHrsy5Dv-a33Ssu-OA3s5EVpsW1XmNwvdCDpzafSmGjPrpDqj4Y8vCbTG7kgtacCkt4hM3lqk-jwk1QxTAWVrvVUyPK1IWw5RxNbNEmFjVilBckxj3wJ2sviStDlb3ActDn40z8D1huitsxlyQ3G5kYsGUVkrYQcqFPpLwTwvWaA6zYJI7IZqG0FkO3FOzx7pYLsXSB_mvKQ21aIhzI0Rx0OyR0csTzukAIuhrax_I5evZhiOQbykCVVsFOpsPH7wuwuGZpCUFSrcr7eczUHRQfPch7a2SQMivj_Eqe2btduHC4-BZiQfLPs6r_t2BM6y_IohPA9Jf-aTNwWQS2BK4ykuNopUtg2JO_iN6Z6PHDNIllRbna1wkn17jop0ocy6SMYi5Vhv0Nnr0l8_8SDbQLuoxkqQQUKUGfypcOJdwIy0003__mC0)

## 7. Tham gia nhóm học tập 

### Mô tả: 
- Người dùng (học viên hoặc giáo viên) tham gia vào một nhóm học tập có sẵn trong hệ thống, bằng cách nhập mã tham gia hoặc chọn từ danh sách nhóm được mời. Hệ thống sẽ kiểm tra tính hợp lệ của mã tham gia, lưu thông tin thành viên vào nhóm, và gửi thông báo đến các thành viên về việc tham gia của người dùng mới. Các lỗi như mã tham gia không hợp lệ hoặc nhóm không tồn tại sẽ được xử lý.

### Các tác nhân:
- Người dùng (Học viên/Giáo viên): Người muốn tham gia nhóm học tập.
- Hệ thống iLearn: Hệ thống quản lý nhóm học tập và xác thực mã tham gia.
- Chủ nhóm: Người tạo và quản lý nhóm học tập, nhận thông báo khi có thành viên mới.
- Các thành viên nhóm: Những người đã là thành viên trong nhóm, nhận thông báo khi có thành viên mới tham gia.

### Mục tiêu:
- Tham gia một nhóm học tập bằng cách nhập mã tham gia nhóm hoặc chọn nhóm từ danh sách mời.
- Lưu thông tin người dùng vào nhóm trong cơ sở dữ liệu.
- Gửi thông báo đến chủ nhóm và các thành viên về việc người dùng mới tham gia nhóm.
- Cung cấp giao diện nhóm học tập cho người dùng sau khi tham gia thành công.

### Cơ chế phân tích:
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

### Biểu đồ luồng sự kiện:
  ![Tham gia nhóm học tập](https://www.planttext.com/plantuml/png/f5M_Qjj06D_r53yyjKDUm4C9hS4jQRKqnkruFYdIOUbaf9F1SuSCfOFfq2aqmfH083JGGgbkyA3WzxWdw2kKqqcs7Ck9IpUX-tv_lk_xdVH7BeyJGMAHXe55g8XY318t1aami4PHoXqIpp1qHw-uSECpGbrzDBHen4KS1UZ7KJfvwyPJPaxwbaC46P74HQz-80bwQu0T2NR6A14iuWsSRLa373t3i8iNlfAVE3gdFWdXCGBk5pz2wBSKGkKtauurrBM3BjuNroceogzIS5yV8ImM4Dl89twaybyKr12RbtVprQsI2ufGoGlsTArkxwCnclqk-ahUCCmsocEcv8SG8YPRCAkl0RqkJjhFCIqk8MALPzo3y8kCLK8a47ZJBFILN4mGA7bUOam3GidFNCyZOnO0z71a_BqhCcgcmJNjJytEU8EaBA_DlLxTfiqoxkcvN30unM_kQRq83k4-aYAZlgwyv3wchBYk9hbVFAYeDO1gWOsmNO-nKXuLMOIxkSgNl5pJLTMaRfTgogPkIMDN2MZfjY8h5fibUrfi8p_iuhHHk-EnZjTBlJdDg-J7BVOcmfZqqrbPMpNXCHB1OKgUrsDoWyJTNklO4DvRp7gKJOU1abzOcPvsKB_gQdUe9N9_KuQuyx2lZZ5lbokfJlV6RzSsVmZtlyxtcQezRyUvJ4MWxztzFBKcc1-ARalLOVwVw_lVpWogv5NrzUbOBdUiyjDmelAb05Topa1N6H8bly9HyZi2dJTzvLJ-JM1qw8mnVeJnqIR-oP9fvTZbZlxd_0K00F__0m00)
  

---
## 8. Phụ huynh theo dõi tiến độ học tập của học sinh

### Mô tả:
- Quá trình phụ huynh theo dõi tiến độ học tập của học sinh qua hệ thống iLearn. Sau khi đăng nhập, phụ huynh có thể xem thông tin về điểm số, bài tập, tình trạng tham gia lớp học và nhận xét từ giáo viên của học sinh. Hệ thống cũng cho phép tải xuống báo cáo học tập hoặc liên hệ với giáo viên nếu cần.

### Các tác nhân:
- Phụ huynh: Người theo dõi tiến độ học tập của học sinh.
- Hệ thống iLearn: Cung cấp thông tin về học sinh cho phụ huynh.
- Học sinh: Người mà phụ huynh theo dõi tiến độ học tập.
- Giáo viên: Cung cấp nhận xét và thông tin về học sinh.

### Mục tiêu:
- Cung cấp thông tin chi tiết về tiến độ học tập của học sinh cho phụ huynh.
- Tạo điều kiện cho phụ huynh theo dõi các yếu tố quan trọng như điểm số, bài tập, và sự tham gia lớp học của học sinh.
- Cung cấp báo cáo học tập và liên hệ với giáo viên khi cần thiết.
### Cơ chế phân tích:
- **Tính bền vững (Persistency)**: Lưu trữ dữ liệu về điểm số, bài tập và các nhận xét trong cơ sở dữ liệu.
- **Phát hiện lỗi (Error Detection/Handling/Reporting)**: Hiển thị thông báo lỗi nếu không truy xuất được dữ liệu.
- **Bảo mật (Security)**: Xác thực phụ huynh trước khi cho phép truy cập dữ liệu học sinh.

### Luồng sự kiện chính:
1. Phụ huynh đăng nhập vào hệ thống bằng tài khoản đã được cấp.
2. Phụ huynh chọn chức năng "Theo dõi tiến độ học tập".
3. Hệ thống hiển thị danh sách các con của phụ huynh (nếu có nhiều hơn một học sinh).
4. Phụ huynh chọn học sinh muốn theo dõi.
5. Hệ thống hiển thị:
    Điểm số của học sinh theo môn học.
    Danh sách bài tập đã nộp/chưa nộp.
    Tình trạng tham gia lớp học (đi học đầy đủ, đi trễ, nghỉ học).
    Nhận xét từ giáo viên.
6. Nếu cần, phụ huynh tải xuống báo cáo học tập hoặc nhấn nút "Liên hệ giáo viên".

### Luồng sự kiện phụ:
- Nếu không có dữ liệu: Hệ thống hiển thị thông báo, hướng dẫn phụ huynh liên hệ với giáo viên.
- Nếu có lỗi kết nối: Hệ thống hiển thị "Không thể kết nối đến máy chủ. Vui lòng thử lại sau."


### Biểu đồ luồng sự kiện:
![Theo Doi Tien Do Hoc Tap](https://www.planttext.com/plantuml/png/b5RDRjf04BxxAKO-jLBQ1-1GHGfIM-M209NsQ6pNkyACaRr6uLZbmA6AL4vLrKD124L96_KlkNWF71RbFVO9-WhLhY7sKaEQ2w3T-RwP-RwTNVxmvM72d9Yb_T1oN1R5q71Y7nau2JIiRfIYvyGZwFZTbyZy-AtZ-cghOxaHiZWAr-4jFnxIVAjbUGvpkaxYGttpmqcWVeTe-eCeBYEQbcKruCapwDHWzM5rYW4WaTdL08PY6W6HV0oCI3x1m7921g_5pDKBFzMNc281LrnZO040T1HHgmRF9R-YC1ANARWoEq_Xf43fm9OAhDVWc4f-sWSMEuhi6WDW564rATMXu-lm96VMwVK60XDJ2ZqIoMoEgj3v04B9nvi4UKzbWC5hLk-7YR_LcymM3Beocr6JCMzkNMvNp2ALzICj16ZKu8Ng2pNNUx1DNSlCJ-5LIY4KlrJdHF8h2FMoRVdeMLhmRV2Mv1llZeZaPmWkaVp21TGOkqty23nnGu5HcIsL0f9_KbgTkS0KeMtuzgPmp7EGG29cBbc79rJbbVpSWG6HV04a7I4nt6p7wGY6CbjWDLm7gvxgrUJYDoGokq4TPzZUZcKsXw7ax_Om6oxzDwBIilsGBSr9qK8_LPC2RAExcQLfAYpvTmYfvEEqxCWTf5cXQZKaprTHgDPw1qOh3OcOhW-IgNdJKD2OpNna4yad1z1L8wZv3ZP3TY8kc47OhBAaACg8hJJZuIat1hLbDgTmearPpwghFiewF4APBNDFyF6_nPYUCPdDeeAeki_yWYYohIPYdYEtwVDcZr8C5FzYKC6iBwRZN7yr8BkKQ-w-dkpo4UZb6psYlF0aNs1Wtsz1cMuefa1kVqZ-6GFmPFOL8QJYKi_160AgOzH2qGDwLbKl5IUsQkBjwlQBidTVpVkdV4FCnBT-VYsFoiFCuWW3umMqypRGAwxdOvaj6Q3a4mhkxKmTqY_6d5Oz9FlU4UZTmxZxeSdnzeDAsl42GUAawrVeq4TF_KFv2m00__y30000)

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
   
    ### Sequence Diagram
    ![UserManagementSubSystemSequenceDiagram](https://www.planttext.com/plantuml/png/b5B1Ji904BtlLqmuGGA1UEo1WDGe2jAa5RqEfUbkf5kotKBu1iyUFH32mOE962-s1mzD_8_z0d_1j8fQqnwyxMRUU_FUpBp7hvr0ef2XDoDeIr_0HU08m03EtRT75TynFNdXBfcZaCncS-GIAbsZ3ySedIMkAYcqf-9RxdQD_XzOAAd39RDHCf-3wOW5ivsCeQlungPZ5M-lahLjKHNlx3nPHuaJ33xXFLCV499p18tsJryDZ95fGHFdh8cXfCsPxp9ElkifkAYb1kaRPFO1IPDdxe9a7Af77h9P7OOgUf1mJLLq7zP8aKJcmzG76bWYNC52HLiE4nNjk0jEAaBIAZHA7HogQCF1fGpuLpwOPW7t7WmCWgKlfYSOq3gCaO4KoLEv6xqygCSupUdzKyHIqTe7BzdiPpL9rZwSNbebElaT3GjulrRKQETlJeE3LWj6Pr0j8DP8n-7Jz6e_0000__y30000)

    ---
    ### Class Diagram
    ![UserManagementSubsystemClassDiagram](https://www.planttext.com/plantuml/png/T5HBRjim4Dtp50GtbOiaGBTQ577j0icYWHkx1vX8Ouc8HAgSOMgZwCcww95wXOBKNtQr4jyySjwR6VBlxp_tnE3OrvKGx-Ic0YAvrL0ugENHElcDqCalOA306WtBlN-XCp7MGcIH70a_XOnVM3nkKwaDTyZd6dILIcAdJT5XEo3wOLt-05GkGi-smWMqPs1F2t3Z41ZpDQSo1qRMDVOIclm_aHDaNFeiQRhq_P6hLBvOMo4OyQjt5NGChi9YxYeWJr0lfMwHCgSRrjOi8WMOh_wC9cdGrPeeCdR3_ogLRrRdO_unDAWOeKijSsIFxardkCuofB5mmzbhpoKQrXa4eHrvI9E3AKm9JOBJpjt8ArMREGpxJXuuOVkAW_tUMCjvrLYpWyYuu5tq80pJpjcZhd0oWBtE2iw7qfhYeCrJuQtUUbCaEezrMALnSyVCe34byCZoXAvbh6RoJXQk7JNlpFEdzMOG4GmT7BIjTPFPlP7KrlMwmNXfr0SbRs-bUg_QSKkbAe6KY8j9S38BgLGv7hL1Kk9w6-_kFhPNCfMg6tWLqrrMSahzxi5KPoMYkn3e5GM7P86L4FTeyl1E_0C00F__0m00)

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
   
    ---
    ### Class Diagram
    ![CourseManagementSubsystemClassDiagram](https://www.planttext.com/plantuml/png/j9JFQjmm4CRlVef1bsn24iXLb2LbdPAIFvHialjKcjW2MGgI7BAKFbaFVQIyGbXRMkrg3Q6K-6IFVXfztyp8Rt_-7i12e_TGAsmSTl1a7Inixpp13Hfig2CJODd_z2iVgAigCU0H-LN1y8oVtsiEoeGOkyMEEFZWb6bYg2Old7eEoffYvPvGjEHsComSOI3vDN2G62YeZk9AQAcxHtMjg9yvyhPtWZZSnRT33YzMoSY-MYpHU4pYVYTNAS76LmeKkYRSVbEQVc1e2ryFpzgYdFQ0wXCiN1XdjHwQbapaqCSs7dpPX3khopOsQ2wjU5HaPilGo_LPVa_8c7r9xaLj5JIWlMejNben4mF08xXhMECgOKeceoEOIx9FJ7Tpd6ENDVp3y6XS9NJKc-j-hNpuadRD_wTJfK29fhbQvHh53CVGv-uSWzjgp9xe6asxHD7MGwffxLd0FAkF6wYScItvyUwpCmOd9y2EMBut75YBdaqWMtF9WIaZT2zfGwOnEJsTfryB1zODTV6iAZkvndRFD5AlmVsQhj7TipTmTKv6zfsktW400F__0m00)

    ---
    ### Sequence Diagram
    ![CourseManagementSubsystemSequenceDiagram](https://www.planttext.com/plantuml/png/V5AzJiCm4Dxz59-wG2Mgx1qGb02g4AAYHMAzkYQnIC_WEA0ACJ4pyG94R4XCCAL3Xpo9du1NG4b1RVaRBD-TlZ_h_3wTRQMEhCl6YLX3NrrcYgL2g2coDCQPiTXbQv94SmJ2IQgi42ITiVDwQ38UaPsWiTthOf-SkgP90vHYkzVzR8KqxAn9q9XBZHKx719Jf6mDNOm_fqAnqsw2HaYEXfIg6XPsXAXCqTfSKc-ZTzGV8A0B7KYJsLIbmOqUtGQgLXKBPCNxOTN6VfapOZ-zbxZIvJC7aIvpCwznLJuQdCVbAyqXueT0fHfssZZGVdetXhEqZ8VpqmU6yqMkHTX1w_SCWxXyumXEymfvVQT-K3Ti_kqxy4LkCFJ54oEATNr6n37M5vHkk84lgOrwSTLzR1BL_2VKQPbBSEoB5uQBoqUE8QkOlsNvjf83NymSBZDVF2q5wcTIgZGDzaWdcLNDbTsqDkjWArmXjXIFgh_v0G00__y30000)
    


#### **3. Hệ thống con thông báo (Notification Subsystem)**

- **Chức năng**:
  - Gửi thông báo qua các kênh: email, thông báo trong hệ thống.
  - Quản lý nội dung thông báo.
  - Lưu trữ lịch sử gửi thông báo.
  - Hỗ trợ định tuyến và mở rộng dễ dàng.

- **Thành phần**:
  - **Notification Formatter**: Xử lý logic gửi thông báo, định tuyến thông báo đến kênh tương ứng.
  - **Message Queue**: Định dạng nội dung thông báo tùy theo kênh (email, hệ thống).
  - **Channel Services**:
        - Email Service: Gửi thông báo qua email.
        - In-System Notification Service: Gửi thông báo hiển thị trên giao diện.
  - **Notification Repository**: Lưu trữ lịch sử gửi thông báo vào cơ sở dữ liệu.
    
- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Notifications`**:
      - Cột: `NotificationID`, `Title`, `Content`, `Channel`, `Status`, `CreatedAt`.
    - **Bảng `Bảng NotificationLogs`**
      - Cột: `LogID`, `NotificationID`, `UserID`, `Channel`, `SentAt`, `Status`, `ErrorMessage`.

  - API:
    - POST `/api/notifications/send`: Gửi thông báo đến người dùng hoặc nhóm người dùng.
        - Dữ liệu:
            - title: Tiêu đề thông báo.
            - content: Nội dung thông báo.
            - channels: Danh sách kênh gửi.
            - users: Danh sách ID người nhận.
    - GET `/api/notifications/history`: Lấy lịch sử gửi thông báo
 
    ---
    ### Sequence Diagram
    ![](https://www.planttext.com/plantuml/png/d9I_JkD04CRxVOeHLLn4z2aYZZy5keZYu0KsZl6kS6OZUun4URhY2ggKT5WH3GX1GUKjA1pn7lC4lCB9DhRN8f7WkjdHxvkPRqRskttTIqZ6bCuZ8NqoCVoOpJM2J42MWLZ8cBIl5n89TauCwNFjIz86JuFuKll1JeacTRmThYXq4dtqG4d48Aeeluwtr_eLB4oYoSHN5H-tpxxaQ2vrv1OEoaIVESRJguI2kOlfZvmGrG9WE6ximGX2je_wJ1Kl6EuNcHdCs3vDDDk_QPVqHCCFnptFC0BYF3FVqNziesaz86Kmd4hZmS1N1eZj0uPmKToZyaG33yUrsKqgvFmrXQYuXP-bgDgI9shSqQsNRAzH7NAUONZ2zaOVfXXMT5UjatL7W154Ry_fn8IEpSY4BTmpHJ7dAxXa-nj85RUem2z5kwGuloEOSfvfuVfghlC5QzNK-snlFD6g-XMKPli7pnJRQsTOQksvigyuxFZ_CEaS_LElZTErWk6u_bRBLXK8qo8pi5uMArWltvxPhlnwMp3OEe0dzWASbR-1Vm000F__0m00)
    ---
    ### Class Diagram
    ![](https://www.planttext.com/plantuml/png/h5HBJiCm4Dtd55wsY_O0KLKLyP4g1HOK3c2IgHd9cQayqqeLz6GiE19NG6cIDWvGySlEVc-UttYUy_RoEXErGTUbJt9lHSmDAounjufC2mWRpC4y9QRw1AZemWFgBDAeSfYQ3MEHx99FP1kzaQ9wICr20vAhjt8c1TBUvgCb0Y-foL1qSbulfpKO8CSL0caBtmk46ZCEz8f3QLMXk0OHws0mF6ZlaWH98Inj3gOHxRPwkhq7PW-MZXrUbXRzhsNslIptPckX-Y9E5nyRgItCQR4LXV9lBWgKbRVR_vZqBQnOK3bi3rxi1dweVAZBs0qykvYLiJjf8MFNvispcnTnjAZ3x6E7PAMcobIKnPWfG7gcgRcm2dTOGhEhLjSICo443aqKFywlEgOrknO8VKTG9QFNW2qZeS-UxsWqZQxaIrAJcs-974SRqIETDeUJv_4uUXynqejjfDT9KDz1nYwYLfEkEFjXpO2AwgVs3W00__y30000)

#### **4. Hệ thống con quản nhóm học**

- **Chức năng**:
  - Tạo, chỉnh sửa, và xóa nhóm học tập.
  - Quản lý thành viên trong nhóm.
  - Gửi thông báo đến thành viên nhóm.

- **Thành phần**:
  - **Group Service**: Quản lý các nghiệp vụ liên quan đến nhóm học tập.
  - **Notification Service**: Gửi thông báo đến thành viên nhóm qua nhiều kênh (email, hệ thống).
  - **Group Repository**: Lưu trữ thông tin nhóm và thành viên trong cơ sở dữ liệu.
  - **User Service**: Hỗ trợ tìm kiếm thông tin thành viên.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Groups`**:
      - Cột: `GroupID`, `GroupName`, `CreatedBy`, `CreatedAt`.
    - **Bảng `GroupMembers`**:
      - Cột: `MemberID`, `GroupID`, `UserID`, `JoinedAt`.
   - **Bảng `Notifications`**:
      - Cột: `NotificationID`, `GroupID`, `Message`, `SentAt`.


  - API:
    - POST `/api/groups/create`: Tạo nhóm học tập mới.
    - POST `/api/groups/{groupId}/send-notification`: Gửi thông báo đến tất cả thành viên nhóm.
    - GET `/api/groups/{groupId}/add-member`: Thêm thành viên vào nhóm.
    - DELETE `/api/groups/{groupId}/remove-member/{userId}`: Xóa thành viên khỏi nhóm.

---
### Sequence Diagram
![](https://www.planttext.com/plantuml/png/X5HDQzj04BtlhtZu54DDxpwOX0ICQMjCwq8BXRAMjzOIQ-MkLYu-bXnwBZdqK4fZGYWOGWFjfTg33oh-7_CB-XVAIlwG79bSX3Hwy-QzcTdzPvV7aU7QnC6OSS-46jtHwexiD_dsBFsZHk0HNaP2imdNHdfomfL1xQJNGPiRyO7FQWvnqkkiFykujWxZ2Lu8FPMUo91PP1semZuNap2I9jGvSHRSnSePtT38TzBZHeQgLAJuexBMwMgEYEnt3Cd-n5YI_HHdcMVSy06F16FED1gjWZKqyJfTnF0e-H73-EaYSCyhvMCgquN2DBqAeVpqL_167OsSyixm4U98wCwmpWf4ZLQf3sZYr8zdP2yKZAHaES5iMuYLa9lCNKlGn1D9zYA0qJolZatnEji7DrfRYsYYh-CPffJSA6Vajnh1I9Lpi2siKLcphocvnfJin_kfZ8yDkfaIG_PImL0obmn0sNObyTFLNLoaB7Ku8FjLLZLtottOwu5v3IYvLgCy-Pa81a976Ti3_b-bSm_Af-GsaxYZzfpoIg_T-rk99jfaR-N6y22TX_ZxcPBb0UD5lrLyZLPsMdE_MqPJb2R6aLXFvtpTvWU6LC4u9ll5wQaT8ghLcL13jhUz--Sftw9pIfO6xsFtVjGlQ7tSzocvCMv6Sra-GJjPFTzD43xPIrcaOiT23TsrzXy00F__0m00)

---
### Class Diagram
![](https://www.planttext.com/plantuml/png/j5HBQiCm4Dtd528h1v8Sm8GGGjiGQBEesmEerjWCM5AGv81fUx8kUgHUeKYoZULFQHRnpc-UPjwy6Uddwtkd3LMcvCKiBQZMv5M38kypOhzIWpgoc2H6eSWz9YY7405EiGWX9OiUgP0vYcWHauj4raAoD2tsEQiL79Gipus4tFxqDJZmD12IAg06sBwANHSUvC3VGEcOFA8s6ujlksnNBEesjVGHgNoMG39bxCdbYwmr8mG5N5xWRquEnbMz0qEnqDQ0kelGWcSuIur6ggenGzDBBTWv47jUa3n3mHowhuuiwhctg4zuAeC26WE6n6OcA0oeZAP0Jj9WXYarA4K2we8fjC90i6uuug0rpJkUAaZnZ21CQ4ZRyRrTefjMI2fjWD-qnC6w66PTvSqeu_vKVLmC1JNBEgBrwjtjpBjTtXSvElGb-STIFoZ9hplj6gmcplGixZZgtg7LQbi_1p6PeoQqliv4PlEP3xIKpdM9oTnU5KPGrBIa7agGa5D1Sz1Jb31XgIrpR7qs7-lrzFvQuVnS00TX_aemlPwz30En4sUyu1q8PX_tNm000F__0m00)

#### **5. Hệ thống Sao Lưu Dữ Liệu**

- **Chức năng**:
  - Tự động sao lưu dữ liệu định kỳ để đảm bảo tính toàn vẹn và khả năng khôi phục khi có sự cố.
  - Quản lý lịch sử sao lưu và trạng thái sao lưu.

- **Thành phần**:
  - **Backup Scheduler**:
      - Lên lịch tự động sao lưu dữ liệu định kỳ.
      - Gửi thông báo khi quá trình sao lưu hoàn tất hoặc thất bại.
  - **Storage Service**: Lưu trữ bản sao dữ liệu lên cơ sở dữ liệu dự phòng hoặc nền tảng đám mây (AWS S3, Google Cloud Storage).
  - **Integrity Checker**:
      - Kiểm tra tính toàn vẹn dữ liệu sau khi sao lưu.
      - So sánh bản sao với dữ liệu gốc để phát hiện lỗi hoặc hỏng hóc.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `Backups`**:
      - Cột: `BackupID`, `BackupTime`, `Status`, `FilePath`, `ErrorLog`.
    - **Bảng `BackupSettings`**:
      - Cột: `ScheduleID`, `Frequency`, `StorageLocation`.


  - API:
    - POST `/api/backup/run`: Chạy sao lưu dữ liệu ngay lập tức.
    - GET `/api/backup/history`: Lấy lịch sử các bản sao lưu trước đây.
    - POST `/api/backup/schedule`: Tạo hoặc cập nhật lịch sao lưu.

--- 
### Sequence Diagram 
![](https://www.planttext.com/plantuml/png/P9AnJiD038RtF8N7CY3s3AWK8OHW8dc1QthAdPBS1STNgIDYOEx4IbGXndPWkWmTKlKz_0Iy0eegeLwxsl_t-xVbtsuxRaWWkQgCH4OMuMPMQQCRGa4MereWwKpNmX1CH5QuEbaq9AkWaP15aSj4ubndCcWz698vQbhSAfaLCZIyGxJuB6kB936AWibmUHqCZ672VasmMxB_Tj082-L-uw9ZpS24MM9uscySpBXRGwcvUpyYG-N0deQDuL5pzrO1eGWyTij-TJ0vHSvZfyX-1NFkNg5WloLuSKEX-7S-Mo6uGmofwdzC3jE-jK38lZKvaEfR3QDKzPz6GJO8hbB5_ejWohxL5sUcmQrZk5SQIku-D8mC-wq32kYnDBFX9Vu0003__mC0)

---
### Class Diagram
![](https://www.planttext.com/plantuml/png/P5593i8m3Bpd5Jx2WIyW5Y71bRuWIarh4MBak4K8yJ8EF8ale409j1mzdh4zuyVjFejgHPk3Dnvt2ieWLDKA9Gaw9Gx6UHiZBApRDyV2rLWs7WKk1W0WTlMxEng_mC1Ak_EyF50OZStLT1CAPR4L5YWjEVmCi6rVBAX2-0Dc_IOeLa9wNjRezla4bwhS-nMiH5YsU6JHpFPSlU2yBNK_I5Q-boyvgB3_kfKcz6vj2KzhYihIxVtJJIRJON8TwPjaulIpCOEe4cFetlp5aLWzosQ6eKoVVG800F__0m00)
#### **6. Hệ thống con giam sát và theo dõi tiến độ học tập**

- **Chức năng**:
  - Hiển thị tiến độ học tập của học sinh.
  - Lưu trữ và truy xuất thông tin học tập.
  - Tạo báo cáo học tập theo yêu cầu.

- **Thành phần**:
  - **Progress Tracker**: Theo dõi tiến độ học tập (bài tập đã hoàn thành, điểm số).
  - **Report Generator**: Tạo báo cáo tiến độ học tập chi tiết.
  - **Data Access Service**: Truy cập dữ liệu từ cơ sở dữ liệu.

- **Thiết kế chi tiết**:
  - Cơ sở dữ liệu:
    - **Bảng `StudentProgress`**:
      - Cột: `ProgressID`, `StudentID`, `CourseID`, `CompletedTasks`, `TotalTasks`,`LastUpdated`.
    - **Bảng `StudentReports`**:
      - Cột: `ReportID`, `StudentID`, `CourseID`, `GeneratedAt`, `ReportPath`.

  - API:
    - POST `/api/progress/report/{id}`: Tạo báo cáo tiến độ học tập.
    - GET `/api/progress/student/{id}`: Truy xuất tiến độ học tập của học sinh.

---
### Sequence Diagram
![](https://www.planttext.com/plantuml/png/Z5EnIWD15EptArwP5Fx05H9HqK8an3IMcysIMtAtUxpR2wOK2mknI2MM8OI0A29skqYAou-yB_0Nv8XWBdS9DjlCctapixlVVjbABKURnH7ZmXg4DaUfBKiuMYLKmhM5Dfe1oZIz6gTMnYNeX5j-94G1IXmf8KjeHoO6xPdK4harMC9E4Gsk1oGojbuB1uTRsmAupbyo4EGM6QJaFy0gSaiDFVBF8CWlE8Ja7mMaIeUiJ2xaAWu3wEQlCMXoqmJwvDyXKkJliqrXLc7LEUiYkHcCoD_krAdwMGSDu5oHlzDWG_8F9Sh_gkZbKmEYE7wvgqdzlgqx2A1BRcfsyRUcTnHuGMu-BcKMuOPaVNkTYf7Q-keix2d-ByTgai_05k7sj7wSwK7Hu3pPO3OYfOS5TQRW9YC_qOCcgn4fFTa0BaDoRnQ6-HT4v9yKD3IvPGOY_soobjJzubFz0000__y30000)

---
### Class Diagram
![](https://www.planttext.com/plantuml/png/b5HjIWCn4FsVK-Hd1Nk18gK5HGI5Oki1mcRS1hF9EZFR8kB9_E6Hl8BaezqssuBzix0lRzwRcRpTt--V6R52xXehH6KLaLme1CVoKqWfvSR0Te6-HY0Q4NSQ73_eYJIEhoPouusED8Jt3eYVeVN8PtXVUuEij_mWXYORrS3BL7RUhY3aEWUe6CvP9xmtlrMivbKLx04tfeBi_mfShI-pZYL9FwWEYnuDyKquclR-YN-VklQudpvDKMXSopOR1fL3mHEJ5Ir6vV5U82j6xDWaGfNlaE0OQLeB37gbw8rwd3qhMs1M4R-qMZ7eITWmh4m3vSov8Oml5xUpsv2Uyu55BxXGl0xNXCRLSQNQRvtrIey6-Rj3z9XwWjq5M5z7U0JX-GH4geQTte52_ZZ6usaHOr6aEZ06MJj5AW8Xoe3yM-XeB37CUU2KCJvbbdCbPk1q-2ty0G00__y30000)
# **5. Thiết kế các lớp**

![](https://www.planttext.com/plantuml/png/b5TBZjiu4Dth5BMp3DWN40QDz3Vfm1qqOWUpPalLCc69zB2e3emW9yjYZZHN6F0ZYwJSSjihiKXMlNfyHPR_-_Fl9z9CwQvjicm6otT_sGn-42fuOeBLsABGiEvUw40Qs-cDMTam8hZkz1Q5vYNJN8ergZTU8lpA0A2HDHSvjemt1Qorug9Um9uH_PIgwYtp0hx-lV7BPQTpBNSeh75Um9labPbxOmslcCQDcOoNt4ZP81FPxnwHoSV4NvgFnxi27eKsm_iGY34yUoXV66r3-tVPO3XUQwOx2Yst2fd6wbeNSCSqsc3xAZ51ZTf0k4FDU4DvDy2P5nQbMTJPVMOKBbX0GfiACFMy73CsW2tb5dgGiXb-OssKpHrIgVZUd5PW1aR4Qs4sn3Wc0p-ZQZaHbu9S_C6Ge0Y6NYFNPOaKichu2Xpc9lB0rugJ_ikjlJ80Pl0T6wivsl8zPQTrk5nUMQOBQAt0ARDgDsPtobj6DiNCScZi0OJ2iq9JDPJDu5PsYl3I6kf9zBijV-ux8EjZfxVS82ktaTh74eNIcbo8N0IE5r2DtIv0HqxdXKSwgDQxAaFG2pZhUIIZUw5aqrZYB0l3E4mefIOfxwHg0QsJjUug53h5U5RY0A2mbMzuti6u795af_mjkEn7Kwayy0QVcOvkeH_xHh8gFi7EsdgFAQRNn4i0BAqMhpcZzu7i0hWecwx2QBwFvcl5ZoWB3cseCaSwLl1oo8uqc6ddq1QKBBbH9lpaUlj-OMKp-2OrV_K5_O6AwkcFjjaZ22q1wnkkuul-LWfjUGXCMoO4DfS-1q0egZ1ihiDW2oZZK0ieuq1EOUJllKUXhqOo2zslPErINSawl3rE9vvKpgaSKUZmTHldVA-KL4z8nEgex1fPHtcBCOIa_2ZoFI7Qw62Dg1862XFyn38dJJ9ArN9ISP-LxFQNtUFzQRYjzWpiPy2l7QSNkTVCpU7yZMttvtNgPU6dUn_pme6mhtbLFM7xWifjcxgsZZVTHpSS1MYZkLsd4qzqzbLo4UTtXBcHGP8Ne7rGiltWpjzZGRapCn89KYbiRJ8k_BnFS10I9s3GEgjydMolindSi7BNxM5zjgFkMVKRBA7kEw3G6JRSgE3zsZprdDXwjKKorAhgX7EOZyxMsTUeDHUrR-xMvHQhBkhb7XJ-qw4e3_45AHMhSILT3OOH2RNtx7tbhwa7So6St3_2-2Wqrehhm-qMovqN8PHcu8dh5-Gl8P7nduPK59v_Szun2GMG1ssVjs1T2gHm8DowC_fuLh9MI0GRnSeT5_K5Kl6zoT65Qy7zAEoutRgf3kHMjli6DLORHZiQdaYfMHERLeoq_xCp5B8suFl8EKNnp6CNzIdbEDQ97celbMy7tVTb-Nn6WIhzZ-OS9PK1jL_gPgV1JrmcwM6uticuB8uXJFzaB2SNzorImuMHZfQP9y5C9Xk2LYtxXA8o__F_1m00__y30000)
# Kết luận

Báo cáo đã trình bày chi tiết các khía cạnh quan trọng liên quan đến hệ thống iLearn, từ việc thiết kế cấu trúc lớp cho từng chức năng cụ thể đến mối quan hệ giữa các thành phần trong toàn bộ hệ thống. Các vấn đề chính được giải quyết bao gồm:
  * Quản lý người dùng: Hệ thống cho phép xác thực, phân quyền và quản lý vai trò người dùng chặt chẽ thông qua việc tích hợp các lớp AuthenticationService, User,     Role, và Permissions. Điều này đảm bảo tính bảo mật, phân quyền rõ ràng cho từng đối tượng tham gia hệ thống.
  * Quản lý khóa học: Module khóa học đã được thiết kế để hỗ trợ tạo, chỉnh sửa, quản lý khóa học và các tài liệu liên quan. Cùng với đó, module đăng ký           
    (Enrollment) giúp tổ chức mối quan hệ giữa học viên, giảng viên, và khóa học một cách hiệu quả.
  * Theo dõi tiến độ: Hệ thống cung cấp tính năng ghi nhận và báo cáo tiến độ học tập thông qua StudentProgress và Report, hỗ trợ giáo viên và học viên dễ dàng         theo dõi kết quả học tập và đề xuất cải thiện.
  * Quản lý nhóm học tập: Khả năng tạo và quản lý nhóm học tập được hỗ trợ để tăng cường sự hợp tác giữa các thành viên trong hệ thống.
  * Sao lưu và thông báo: Hệ thống đảm bảo an toàn dữ liệu bằng module sao lưu định kỳ, kiểm tra tính toàn vẹn, và quản lý lịch sử thông báo để cung cấp các chức năng hỗ trợ tốt hơn cho người dùng.

## Hướng phát triển

Hệ thống đã giải quyết các vấn đề chính trong phạm vi ban đầu, nhưng vẫn còn không gian để mở rộng và cải tiến:
* Tích hợp trí tuệ nhân tạo (AI): Ứng dụng AI vào việc gợi ý lộ trình học tập cá nhân hóa cho từng học viên.
* Hỗ trợ đa nền tảng: Mở rộng hệ thống để tương thích tốt hơn trên các thiết bị di động và các nền tảng khác.
* Mở rộng tính năng theo dõi: Nâng cao hệ thống phân tích dữ liệu học tập để cung cấp các báo cáo chi tiết hơn về hành vi và tiến độ học viên.
* Tăng cường bảo mật: Triển khai các cơ chế mã hóa dữ liệu và xác thực hai lớp (2FA) để bảo vệ người dùng và dữ liệu hệ thống.
* Mở API tích hợp: Cung cấp các API mở để tích hợp với các hệ thống bên thứ ba như các nền tảng học trực tuyến phổ biến hoặc CRM.

Với các hướng mở rộng này, hệ thống hứa hẹn sẽ trở thành một nền tảng quản lý học tập toàn diện, đáp ứng nhu cầu người dùng ngày càng đa dạng.

---
# Tài liệu tham khảo
* https://github.com/opendesigncasestudies/iLearn-IanSommerville?tab=readme-ov-file
* https://software-engineering-book.com/case-studies/ilearn/
* https://arxiv.org/pdf/1411.3948
* https://www.dropbox.com/scl/fi/ffls77bnutw9gmzo73ahq/Architecture-proposal.pdf?rlkey=oye4s9hldeweosuxwigsm2wpy&e=1&dl=0%2F
