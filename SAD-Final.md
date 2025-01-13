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

# 1. Đăng nhập hệ thống

## Mô tả:
Người dùng nhập thông tin đăng nhập để xác thực và truy cập vào hệ thống iLearn. Sau khi xác thực thành công, người dùng sẽ được chuyển đến giao diện chính của hệ thống.

### Analysis Classes:
#### 1. Entity:
- **UserAccount**: Lớp này đại diện cho tài khoản người dùng trong hệ thống. Nó chứa thông tin về tên đăng nhập, mật khẩu đã mã hóa và vai trò của người dùng.
  - **Attributes**: username, passwordHash, role
  - **Methods**: validateCredentials(), getUserDetails()

#### 2. Boundary:
- **LoginUI**: Lớp này đại diện cho giao diện người dùng trong quá trình đăng nhập. Nó hiển thị trang đăng nhập, thu thập thông tin từ người dùng và hiển thị thông báo lỗi khi có sự cố.
  - **Methods**: displayLoginPage(), captureLoginInput(), displayErrorMessage(), LoginNotification()

#### 3. Control:
- **LoginController**: Lớp này kiểm soát luồng công việc của quá trình đăng nhập. Nó nhận yêu cầu từ giao diện người dùng, xác thực thông tin đăng nhập, tạo token phiên làm việc và ghi lại các lần đăng nhập.
  - **Methods**: handleLoginRequest(), verifyUser(), createSessionToken(), logLoginAttempt()
- **EncryptionService**: Cung cấp các phương thức để mã hóa và kiểm tra mật khẩu an toàn.
  - **Methods**: hashPassword(password), verifyPassword(password, hash)

### Responsibility:
1. **LoginUI**: Hiển thị giao diện đăng nhập và thu thập thông tin từ người dùng.
2. **ErrorNotification**: Thông báo lỗi cho người dùng khi đăng nhập thất bại.
3. **LoginController**: Xử lý luồng công việc đăng nhập, bao gồm xác thực thông tin người dùng và tạo phiên làm việc.
4. **UserAccount**: Đại diện cho tài khoản người dùng và lưu trữ thông tin xác thực.
5. **EncryptionService**: Cung cấp các phương thức để mã hóa và kiểm tra mật khẩu an toàn.

### Biểu đồ Sequence Diagram
![Login Sequence Diagram](https://www.planttext.com/plantuml/png/X9AzJiCm58LtFyLz0LuW0m8X10Z4GYknfeuLMwJNnRskoDo1WOc92QaHGWYaIY2nu0mTNF4UVW9U0INzeN_0wEISSpyVtwzojDEbs91jPopcf0qqkyAmbhQOn2Q74vqgR1unhf6CpYRdlSaX4uO994LvRThbN5kakNGVkSaxf3IU2TDJN31MoM1hUvOQGSFO77XmmmwaAjQGg51U8unlntrC0MNrXqtLbR4AYE1GXRAFG3AKDq0cndJ5iJRdjFuE9Fqxfa3gZn4hDupW89H31Rb_iHNfazra_T7FAATjJAzuPODxfCNvc7w-Xl9UGU8_C6KB5jZQHD4mmJqi1f0VABYGEhW7t0InLdy4vxxWTMjl7Dh13GakP73FbgrfDpCS1pSYkBGLoTLF5eipMiecwGSeWLUi35PpbXSWk493Hoh_Wf3vGHjwrGhmcMtnsVUapUk77zy6DyAbZU7I3r4oaNN52afTV2kuGls7CkcsvGiDMIZlvlfVLs-Y4fYm7O69RMVV0000__y30000)

### Biểu đồ Class Diagram
![Login Class Diagram](https://www.planttext.com/plantuml/png/P95DJWCn38NtEKMMiEWD8jIgLA8Ie8hI0vYCEnEHIGRRAHgXdem5H-8AAEbCwSyoxzd-dftVxvyf2v2arYlhWLbl66bcRKn1j34On4b_T_UbjDOwCLA05ikZ0-RFIDK3S5C4YlxWxC2x2WJdX5KU09vlRejJe-JvzoZWYhXN0_OnrYvibjgOjvWge2EpSjnvw8k_WXg7IHOwIOH5NeOkoQ0FvGkYI4_8_DzHIf-ZkAsp82w6A_my1g7eFP8snXuUOum6GkKFk1VyICWZS8VajdtUQan6289hP7OnlCPtpA1i-5YN_fa8jbtkF-8NmLBVvL1hf9spg8r9ulp9xHlWPZMS_0nz8kwLElk-oUHoCNMvw5YoMLvPkVqgc9fYg5Bh_m000F__0m00)

---

# 2. Đăng ký tài khoản

## Mô tả:
Người dùng tạo tài khoản mới để tham gia hệ thống iLearn. Người dùng sẽ cung cấp thông tin cá nhân, bao gồm tên, email, mật khẩu, và các thông tin cần thiết khác. Sau khi thông tin được xác thực và lưu trữ trong cơ sở dữ liệu, người dùng sẽ nhận thông báo thành công và có thể tiếp tục sử dụng hệ thống.

### Analysis Classes:
#### 1. Entity:
- **UserAccount**: Đại diện cho tài khoản người dùng với các thông tin cơ bản như tên, email, mật khẩu được mã hóa và vai trò trong hệ thống.
  - **Attributes**: name, email, passwordHash, role
  - **Methods**: validateCredentials(), getUserDetails()
- **DatabaseService**: Quản lý việc lưu trữ thông tin người dùng vào cơ sở dữ liệu.
  - **Methods**: saveUser(user: User), checkUserExists(email: String)

#### 2. Boundary:
- **RegistrationUI**: Đại diện cho giao diện người dùng để đăng ký tài khoản mới.
  - **Methods**: displayRegistrationPage(), captureRegistrationInput(), displayErrorMessage(), displaySuccessMessage()

#### 3. Control:
- **RegistrationController**: Quản lý luồng xử lý của quá trình đăng ký tài khoản.
  - **Methods**: handleRegistrationRequest(), validateUserData(), saveUserAccount(), sendConfirmationEmail()

### Responsibility:
1. **RegistrationUI**: Giao diện đăng ký tài khoản mới
2. **RegistrationController**: Xử lý luồng công việc trong quá trình đăng ký
3. **UserAccount**: Đại diện cho tài khoản người dùng và lưu trữ thông tin xác thực và thông tin đăng nhập
4. **DatabaseService**: Quản lý việc lưu trữ thông tin người dùng vào cơ sở dữ liệu và kiểm tra sự tồn tại của người dùng

### Biểu đồ Sequence Diagram
![Registration Sequence Diagram](https://www.planttext.com/plantuml/png/h9I_Rjim4CPtFiMDCf2yW8OYHHEq7PgXJO2kDCMAX6ag84z6CsV8qCdeqAbe3KyjODH3bue8EiZmU_09yWe1QRULPJb_a0hGGjnztzsFTxnslmyiKeFbK17Ai31mQhaX_QBK6JNdy9hdqgAXA0jz-fAmGgCfrCRnizMPuePmZHBFeyHJnefIuv-ZGugqJor_myr8Cav8Y87z9os355vvzmNGK9t3Ohouq3aCwYko6HNoGduABwHt5nfGUFS1tXLcs4pQPN4iV3Kx0nJrJvq3Ijr8WWJhxteF-91AjGT3NyqG1i9NtyfUHnNT759uxjrCTZiGqfrqczo8AfbHvA6ZG3Bf4QeG3htx0KfwTrd2OEKbl9kUWVBkaW303i4kA1iabNUVv9P04_oQeVBLfDaduShoZRhkNL1hGb9WWhD1S3jwBotQ95v9Bwg4ve_pvToxpnAo-bSSbdeAwDr73HYAYd7XQ-d2_YsSZuB5Rgd7q8IaMtpLq3rGn_R3DKzOJ8caMn2OMCxfVwAm7gY7SMXiVWedlfeKi1XxDvQ0eT2fpfiXa0XgHMl9xZRPcXHBHt4raj9oyq_X8Js_hISCT22jGItdPPZfhre02n0UEm3h_UZN4SVVf-PEY-OKd3GqjXAvpaZu3xZEmaj-0m00__y30000)

### Biểu đồ Class Diagram
![Registration Class Diagram](https://planttext.com/plantuml/png/V59BRi8m4Dtd55w61HT04QBGI6LHgG9nWAaz3LOTEvqPqwAAatNH8_KALKW0XtwMypxsUsD_VNpEM80arYxJ3fZL2YlBGY0s-CrI5SKyH6-0zjEfUi-KKiPous2VwXwWmdpKaXeQYOGfkVHDb8xjhILHe7jaFjjwOXsrHkOBTSX-IRK8NYWuXwIAeXzEuRRWZHjSlyANYDm7s86p1WGtZ7GB0XtAi3iYDrg7w7ifepUBu9yirSTpoXgiIoCb3bKKfHShvnrvg76YraBML-sChJa56c1-3MJkWBSfJi4DZAV02qA3NYmupaSJDG_18VXMKQ4Ssw20xSXslCHiQpu2unffPpN-Y7egdqT6wip32_GMzNCBbs-MXVD1bqHwoBBiwlECnzC_NcwWJ1wqTIIB_KzsLIoReJUnTjy0003__mC0)

## 3. Học viên tham gia khóa học

### Mô tả
- Học viên đăng ký và tham gia một khóa học trên hệ thống iLearn. Học viên sẽ chọn khóa học mong muốn từ danh sách các khóa học, hệ thống kiểm tra tình trạng khóa học (còn chỗ hay không), và nếu còn chỗ, học viên sẽ được thêm vào danh sách khóa học và nhận thông báo xác nhận.

### Luồng sự kiện chính
1. Học viên chọn khóa học muốn tham gia từ danh sách.
2. Hệ thống kiểm tra tình trạng khóa học (còn chỗ trống hay không).
3. Lưu thông tin học viên vào danh sách học viên tham gia khóa học.
4. Gửi thông báo xác nhận đến email hoặc thông báo trong hệ thống cho học viên.

### Luồng sự kiện phụ
- Nếu khóa học không còn chỗ trống:
  - Gợi ý các khóa học tương tự hoặc thêm học viên vào danh sách chờ (waitlist).
  - Gửi thông báo đến email hoặc trong hệ thống khi có chỗ trống.

### Biểu đồ luồng sự kiện
![dangkykhoahoc](https://www.planttext.com/plantuml/png/Z5ExJYCn5Etz5KUfe9WVI1558HAie2CIjUDuOsjd7EIvCuWIKIAAL5GhxIZQ1krAxACQ2r5ubV_m5-ml82U1p210T9PrNlTS-xzxwEV4BHLPohYWcKNd8BXhWLBxMzC1pt5CnKGQOgVSaXRwb1j2vqIEFncIzZCNSeKwaUCsOczMs5mUIrlg3MHzqqODEV4npzU0uO0njh53qekQw69F1NTjy4NvFnpnB90LmSqDIF4CKyrP12QzZG6wEDJ1NMOWoq7-Xr4W6-hAJ9iYR8DEUXWEqCN85kSeG_qzwlg_PWhIBLSs721fkenig1SeWxjurYVbA_sgo_Cu7s8ndX8E6nCB_zj0gE1k8ilDpPG1M4as8nqjxufcVBNT9Kh_ROO9DmgvhuHQyLzqiAyqZ0hrptUPQ2O5c4npsGhxR-uNKA5-e7NaRTIaz_ISqCL1t59iExYhfz1ZNysG1dUZto3j1xVGyFSGlXAjHq7Bk-MgpU1-lLhEIFdRxDt1Ojgls3dZcbATqowJPi8OwqipYH_a4G00__y30000)

### Lớp phân tích
- **Boundary:CourseManagementUI**
  - **Method**: displayForm(), captureInput(), notifyStatus()
- **Controller:CourseController**
  - **Method**: validateInput(), saveCourse(), listCourses(), notifyStatus()
- **Entity:Course**
  - **Attributes**: courseId: int, title: String, description: String, startDate: Date, endDate: Date
  - **Methods**: getDetails(), isAvailable(), enrollStudent(), removeStudent()

### Sơ đồ lớp
![dangkykhoahoc](https://www.planttext.com/plantuml/png/T991QiGm34NtFeMNaqKk44AOCaCXYwv23w34QX0uSh3bG2WzMHSzKgzGafYPJDfwOV3xihui-Vlpwnm4lCJ1AgKw2o7eYui-u0imz3WWoskjox9raGtukQhqkzBhCXH62_EpyyCfIwo3KQB7ciSeDyXEw6rk12I6KwO-7eqkZiKxQz7hikosmyvb0ai6v90om8JRzHko56H3uJ_d1HtSTLaY2ydzORdkLgKsXIQMn8J4Og4RySHzOWP3vsaKSdnGrfvUGR3GovueijcnL6AFSaK1ik6KFMJHciBJ16IXjRXehNCsASXBnng91baEciV1JRZJ9aTcQRfIVqmspwjVSqXnky7SevHIPsIp_9SV0000__y30000)

## 4. Giáo viên thêm bài học mới

### Mô tả
- Giáo viên tạo và đăng tải bài học mới lên hệ thống iLearn. Giáo viên nhập thông tin bài học, tải lên tài liệu (ví dụ: tài liệu học, video, hình ảnh) và hệ thống sẽ kiểm tra tính hợp lệ của tài liệu trước khi lưu trữ và thông báo thành công.

### Luồng sự kiện chính
1. Giáo viên chọn "Thêm bài học mới" trong giao diện quản lý khóa học.
2. Nhập thông tin bài học (tiêu đề, mô tả) và tải lên tài liệu hoặc video.
3. Hệ thống kiểm tra định dạng và kích thước tệp tải lên.
4. Lưu thông tin bài giảng và tài liệu liên quan vào cơ sở dữ liệu.
5. Hiển thị thông báo thành công cho giáo viên.

### Luồng sự kiện phụ
- Nếu tệp tải lên không hợp lệ, hệ thống sẽ hiển thị thông báo lỗi và yêu cầu thử lại.

### Biểu đồ luồng sự kiện
![Giáo viên thêm bài](https://www.planttext.com/plantuml/png/Z58zQnmn5EprAmRt9lqMnf0hOhAuoSAcSAFLofQmLdjejGSkGuehJ8fKATpSSONXuC15gbMHGi7_u_q2_uMWs_CNd4rKIM_cpSnxw27yEUuyTxvl3EF2jmw5v4991zwXO5NRsvgxAvIoEh5UkdCkP89A9bhhNMkGowvhxHVfPdg4SbPppolUIKmUBxp3XB42XqSeCtnK57vOd1qKAguRL76XaKe23OKRVNR0oiGiCdpI5BvRU4NX6kUjQs0L3Pifl8g_xGMyjY_QdmnEto5X5XVmDAmqJ5nR-8GOJM7UVvZfMhQZUPxXSp9lu1t7tvyKhgr2JSFINcmbBkD6A7XrVqVXHi1Jc4yP0m1kF8hqJ8QhAGo5-HP89q_Yampv_Lt_Ni3dL4-j4noEmRx6fHWNOM5sEWkh89BQQwSoGp6QL77PxYVkNVOkslukQJgv6_5ovBqrQV9tDAmme_3jbQYXy4l_VuOjVRkQgxZk8MYuJNDJsC3Gi1oLfAqPEvQsJj_v7m000F__0m00)

### Lớp phân tích
- **Boundary:TeacherUI**
  - **Method**: displayForm(), captureInput(), notifyStatus()
- **Controller:LessonController**
  - **Attributes**: title: String
  - **Methods**: validateInput(), saveLesson(), addLesson(), notifyStatus()
- **Entity:Lesson**
  - **Attributes**: fileName: String, format: String, size: int, description: String
  - **Methods**: validate(): boolean

### Sơ đồ lớp
![Addlesson](https://www.planttext.com/plantuml/png/P951IiKm48RtEKMMxU9Te8JoK10UY9kd1nYRgGwaapAPFAZYoLnu9AyWRP-jhLbbFYPy_qo-Fx-EIK4qTy4q0LAoJwT7XEOLnJft4pDxaA6kxRknq_6K-W33NPIkAA-iWLwpu8dxh0lagDGEPmNDgIYD-J1NmJsc5FasiaeC0SMvzRw8b3HWPSygn2yJIN31-ManAy3xJRqJZkW2WJpeacoNmJba9Lt7QodW0tHRSHkb0zrceJUiBB5EbSVK2FLAaMtrf-lNNfILVOun8F2OO5tmuL3_suRPWx5hPjOOSqJsur_z0000__y30000)

## 5: Gửi thông báo đến học viên

## Lớp phân tích

### **Boundary (Ranh giới)**

#### a. **NotificationUI**  
- **Mô tả**: Giao diện cho phép giáo viên hoặc quản trị viên gửi thông báo đến học viên.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `sendNotification()`  
  - `displayResult()`  

---

### **Control (Điều khiển)**

#### a. **NotificationController**  
- **Mô tả**: Điều phối các tác vụ liên quan đến việc gửi thông báo, xác thực người nhận, và lưu thông tin thông báo.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `sendNotification()`  
  - `validateRecipients()`  
  - `saveNotification()`  
  - `logNotification()`  

---

### **Entity (Thực thể)**

#### a. **UserStorage**  
- **Mô tả**: Quản lý và cung cấp thông tin về các học viên đủ điều kiện nhận thông báo.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `getValidRecipients()`  

#### b. **NotificationStorage**  
- **Mô tả**: Lưu trữ thông tin chi tiết về thông báo được gửi.  
- **Thuộc tính**:  
  - `title`  
  - `content`  
  - `createdAt`  
- **Phương thức**:  
  - `saveNotification()`  

#### c. **NotificationLogStorage**  
- **Mô tả**: Ghi lại trạng thái gửi thông báo và thời điểm gửi.  
- **Thuộc tính**:  
  - `sentAt`  
  - `status`  
- **Phương thức**:  
  - `saveLog()`  

---

## Trách nhiệm

### **NotificationUI**  
- Hiển thị giao diện nhập nội dung thông báo và kết quả gửi thông báo.  

### **NotificationController**  
- Điều phối quy trình gửi thông báo, xác minh người nhận, lưu thông tin, và ghi nhật ký.  

### **UserStorage**  
- Cung cấp danh sách người nhận hợp lệ.  

### **NotificationStorage**  
- Lưu trữ thông tin nội dung thông báo được tạo.  

### **NotificationLogStorage**  
- Ghi lại thông tin nhật ký gửi thông báo, bao gồm trạng thái và thời gian gửi.  

![markdown](https://www.planttext.com/plantuml/png/j5JBQjj05DtFLnoyiY4YUrDC-g1fgHieRZvWB4qrG-GxZcOKoBgBBahN9Oj2HEWc4CWYK90MMGZo7_C5_OKoikME4-Eqb2xlp3b7vzovkZ_hsprZUMwBMSPuR7MEthl2LHS4cxlwCqvKSqcxs5TDgHT53zpWQJ9Jz5xmM8gSJNL12SzFqJlGLdrGCRTAq-7h5lbiUSbYJJRNsJhe-U8m4taBNfPCa5Ns5Br38t9ChCvvAbg0FrZMAr2ejmOEBxQHnZfD5QKjPwpJ3ih2a8X6goWOua2wwceESlMPGb9G2YkR6qenRKgzWrYw-WlXgBaaYPFc79JUNRlwcm9v8h6LL3JgGcC88oW9ZVLdmXYU2eyGPBqk9nAPsK4kOZLNWgmPi4uW6eNzmH1lbAi_pc1ptjcpYkvxGJ_K2WMYDNClE4cOfepb0mNfweivCbT_Og6P3Vt74EExwoAq4pIECPvPxBlwIeN7E2uun8ohZ05OMLf_aSTOOST_Fx8dIeLCftxUgtBnaAL2sihr9qKS2sDsNtALYMJ0H6O4ngx-sY4ssXflqiyUi0Gbsn9Ftax-Ec_7-KzfDrXwDAldR4bAxIyqTVNPbh2l_23xKV4hwS_O_v3Qcrrz_4aKhMsx-swEN7LhSUnt9lfMDkSa4RS6fNRLZzZ3gkyMKrULQi3Odg34BzjV0000__y30000)

---
![markdown](https://www.planttext.com/plantuml/png/b5AzQiCm4Dxr54ScP_0BX602dG8cWqkwNwsh42Ww8vq39kJ9ElIH-Wf5BgLsek9qbExxFUdp_MCN1OFq9wTQXp72wi1YtsoBOjaVzolORb-vznh3K5LmKG1bgG008daznHRh3Om3RMFdS6WezawAzKPTLKxxYRq4Tev2ycY_JmzQdD5PZK8DjRQpv2Kcdv62PyfI79kx-zzWnqZXMJYWePI6l5YvwMj8NfBjt3FVRK4g6pAlLBDvGAncywDnztvbMVsz-3byEXbfixKiOBFz_y6PD5KxyZfzoIy0003__mC0)

---

## 6: Tạo nhóm học tập

## Lớp phân tích

### **Entity (Thực thể)**

#### a. **Group (Nhóm)**  
- **Mô tả**: Đại diện cho một nhóm học tập được tạo trên hệ thống.  
- **Thuộc tính**:  
  - `groupID`  
  - `groupName`  
  - `creatorID`  
  - `memberList`  
  - `creationDate`  
- **Phương thức**:  
  - `getGroupDetails()`  
  - `addMember(memberID)`  
  - `removeMember(memberID)`  

#### b. **Member (Thành viên)**  
- **Mô tả**: Đại diện cho người dùng trong nhóm học tập.  
- **Thuộc tính**:  
  - `memberID`  
  - `email`  
  - `name`  
  - `status`  
- **Phương thức**:  
  - `getMemberDetails()`  
  - `updateStatus(newStatus)`  

---

### **Boundary (Ranh giới)**

#### a. **GroupCreationUI**  
- **Mô tả**: Cung cấp giao diện để giáo viên hoặc học sinh tạo nhóm học tập.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `displayGroupForm()`  
  - `captureGroupDetails()`  
  - `showNotification()`  

---

### **Control (Điều khiển)**

#### a. **GroupController**  
- **Mô tả**: Điều phối các tương tác giữa giáo viên, hệ thống iLearn, cơ sở dữ liệu và các dịch vụ thông báo.  
- **Thuộc tính**: *(Chưa được liệt kê)*  
- **Phương thức**:  
  - `createGroup(groupDetails)`  
  - `inviteMembers(memberList)`  
  - `handleErrors(errorType)`  

---

### **Utility (Tiện ích)**

#### a. **NotificationService**  
- **Mô tả**: Gửi thông báo đến các thành viên được mời tham gia nhóm học tập.  
- **Thuộc tính**:  
  - `notifications`  
  - `recipientList`  
- **Phương thức**:  
  - `sendNotification(details)`  
  - `trackNotificationStatus()`  

---

## Trách nhiệm

### **GroupCreationUI**  
- Xử lý tương tác của người dùng để nhập thông tin và tạo nhóm học tập.  

### **GroupController**  
- Điều phối các quy trình tạo nhóm, mời thành viên, và xử lý lỗi.  

### **Group**  
- Đại diện và lưu trữ thông tin về nhóm học tập.  

### **Member**  
- Đại diện và lưu trữ thông tin về các thành viên trong nhóm.  

### **NotificationService**  
- Gửi thông báo đến các thành viên được mời tham gia nhóm học tập.  


![markdown](https://www.planttext.com/plantuml/png/h9D1Rjim44NtFCM7LkqY5_0Y26m5HXVnHie1nkJO9a2H1ZboexDbqIFr2WKfAX5Gjvjs8q2SDt_-V4e_ttyy9Q4eu-0KQGaHFPE-S0GbzFMeaz6mbtpKgMCOlQ4ueTd7C5vtaKbiyA_VcbpVxrwL3bvYS0imlpcE5L3inSg4fYMX8oKkv-rsfNm8OazM5-6Euytg6JfqIlLuUCnZi477ZhMWAHuOPLoZSktX4JqsQ6swEffmpXMSGXpMxSzUEDQQOI7hqjAyts63Abk0B-NPpjHNjTzbgjrc4tIh32J0r9rKk_tGARwGwCO6QTIQKpgDparLvT2LLRo1zJSh3B_QFcNHWOSZnwGENUOpNWAQGCSmIXrUcajFvVfFhWgdV8bt7CnnB65L00EdH6TUvzbTmlUF-jgcKkG4pp66Y0jvuwm_Bujx6XWsmOnNbt5M078od_UOPRaqBqDdvBUBdA5c9KmkCfa9_6QJf4QnD_VDl9GGmGDPbxtZb3-tV_ToN_SlHfRF7Zfupph7XnDPn__1p9-rPqDFx4t-rNy1003__mC0)

![markdown](https://www.planttext.com/plantuml/png/T5D1ReGm3BppYXpfWHz4QANILYkrUq5zW9Uukr53WXp3QbNrPJtqIVr2HG8KMCe5F7PcF3Rv-VhUUGRYjZP9KXdmNZoHQniX9LhMVCrpyP68_YcPj3s9Kv_U5xVO0MfSe1KXiAEnzbbxbYzO7v5oKOTt3yLa0OpnW7Qs3o9yGWxj5CYWZK_l8WnAHQ8qykoB8K5OkmvlSf-ZjvZvtznuP05Y3Tei4BkswXcuzLFFKMRLTDieO2n3PMhn4hzcpGMdzyCCNlT2ogDhhGAQzQcqRmnSG-cZeteahw3Xbd1hMFxiBWV7-arNWJczaNIMoHaJ1bF5u4ynB2KIZupQTfg7AKyoPx3Au0EH2zWaKG334JmAALlMPZ5r3zsIcP19umhiguQLpdZdbagaJbVR4cZLodt0cQ1wNt34nGI5U0MoRFXVOZmRKvRbwsrjrepUDvCR1f9fM9F24XhwsV8-IoSxjAg_qRy0003__mC0)


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


## 8. Phụ huynh theo dõi tiến độ học tập của học sinh  

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




## Các lớp phân tích  

### 1. Thực thể (Entity)  
- **Service**: Đại diện cho các dịch vụ được cấu hình.  
  - **Thuộc tính**:  
    - `serviceID`  
    - `name`  
    - `configurationOptions`  
  - **Phương thức**:  
    - `configure(options)`  

### 2. Biên (Boundary)  
- **ServiceUI**: Giao diện cấu hình dịch vụ.  
  - **Phương thức**:  
    - `displayServices()`  
    - `updateConfiguration()`  

### 3. Điều khiển (Control)  
- **ServiceController**: Quản lý các yêu cầu cấu hình dịch vụ.  
  - **Phương thức**:  
    - `getServiceList()`  
    - `updateServiceConfiguration(serviceID, options)`  

---

## Biểu đồ Sequence Diagram  
![Cấu hình dịch vụ](
https://www.planttext.com/plantuml/png/b92nIWCn6CVtFCNt0ds13bAee0vEMgZZDHSkWUkNaaiEEtVeK0IT7UmDHH2xEJM3G_eYtnFu2dAMzb8ugOu9-Vt_-V--_6Uli8cnRfopX5jjO508mqRQOPgOATm8Koek1bUCQxH6v_kR_kwO2yC4McKFJnch4w1prh1Ts3vkPvW1Ijgi9r26fGP9VWvMad_2h0sv9ly2cKeqf8hy787JPkL0XdUKa99VS0ab-HKxC550yxikt8KtLyEl3j849HIXugq93HGbTU7Mk2dSEzgiR1ImXw3Jtdh-vwhZsPUA_0n_n2pYkXP3VKd-0UFuscmzTJtPgRQnj9EYBiYlrP7cCVbdTK9F_qJTRuA6eU8xh5uRbYY1Xm_C_gd8oXg2KQZqSKnFOEh6-JS0003__mC0)


---

## Biểu đồ Class Diagram  

![Cấu hình dịch vụ](
https://www.planttext.com/plantuml/png/R8rD2i8m48NtESKixQ8t2ALGDmN1XVG0CHbB84rACX6AU38N7iahIF-jkXbctdlplTVZcGSIdc9Zc3GY13YXlsg9m7aaRJHrMNPZ001XDChzS5dHuB18Po-wZbwGTlROzZDi3DmbxCwszAe4piykAk4NljAXDQAR4c6N36fibI0iFal-y0fdoJjZq0FdSZncReqqfGuwq0QxVd_JVxcGfXdCVRDVbRs-o6kSvMXLRCmR003__mC0).





# 3. Các phần tử thiết kế trong hệ thống iLearn

## 3.1 Các lớp phân tích thành các phần tử thiết kế
| **Lớp Phân Tích**      | **Phần Tử Thiết Kế**        |
|---------------|---------------|
| LoginUI <br>ParentUI <br>TeacherUI <br>RegistrationUI <br>CourseManagementUI <br>GroupCreationUI <br>GroupJoinUI <br>ServiceUI <br>NotificationUI <br>ProgressController | User Subsystem<br> IUser Interface|
|   GroupController<br> JoinGroup <br> AddLesson | Group Subsystem<br>IGroupController Interface |
|  ServiceController <br> DatabaseService <br>EncryptionService | Service Subsystem<br>IService Interface|
| Parent <br> Teacher<br>Student<br>Member<br>UserAccount| UserAccount |
| Group  | Group  |
|Course  |  Course  |
| Lesson | Lesson  |
|NotificationLogStorage <br> NotificationStorage <br> NotificationController <br>UserStorage| Storage Subsystem <br>  IStorage Interface |
| LoginController  <br> RegistrationController  | IAuthentication Subsystem <br> IAUthentication Interface |


---

## 3.2 Các phẩn tử thiết kế thành các Owning-Package
| Design Element                        | Owning Package                           |
|---------------------------------------|------------------------------------------|
| LoginUI                               | Middleware::UI::Authentication           |
| RegistrationUI                        | Middleware::UI::Authentication           |
| CourseManagementUI                    | Applications::UI::Course Management      |
| TeacherUI                             | Applications::UI::Teacher Management     |
| ParentUI                              | Applications::UI::Parent Management      |
| NotificationUI                        | Middleware::UI::Notification             |
| GroupManagementUI SubSystem           | Applications::Group Management           |
| IGroupManagementUI Interface          | Applications::Group Management           |
| ServiceUI Subsystem                   | Business Services::UI::Service Management|
| IServiceUI Interface                  | Business Services::UI::Service Management|
| UserAccount                           | Applications::User Management            |
| Group                                 | Applications::Group Management           |
| Course                                | Applications::Course Management          |
| Lesson                                | Applications::Course Management          |
| Notification Subsystem                | Middleware::Notification                 |
| INotification Interface               | Middleware::Notification                 |
| UserStorage Subsystem                 | Middleware::Storage::User                |
| IUserStorage Interface                | Middleware::Storage::User                |
| DatabaseService Subsystem             | Middleware::Storage::Database            |
| IDatabaseService Interface            | Middleware::Storage::Database            |
| Login                                 | Middleware::Security::Authentication     |
| EncryptionService Subsystem           | Middleware::Security::Encryption         |
| IEncryptionService Interface          | Middleware::Security::Encryption         |
| Registration                          | Middleware::Security::Authentication     |
| Notification Subsystem                | Middleware::Notification                 |
| INotificationController Interface     | Middleware::Notification                 |
| Group Subsystem                       | Applications::Group Management           |
| IGroupController Interface            | Applications::Group Management           |
| Tracking                              | Applications::Tracking                   |
| Service Subsystem                     | Business Services::Service Management    |
| IService Interface                    | Business Services::Service Management    |
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
