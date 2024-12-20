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

## 3. Kết luận
- Báo cáo đã làm rõ **sự cần thiết** và lợi ích khi xây dựng hệ thống học tập số hóa mới thay thế hệ thống cũ.  
- Xác định các **yêu cầu chức năng** và **phi chức năng** để đảm bảo hệ thống có tính **linh hoạt, mở rộng và bảo mật cao**.  
- Mục tiêu xây dựng hệ thống học tập số iLearn có khả năng **tùy chỉnh, tích hợp** với các dịch vụ bên thứ ba và đáp ứng nhu cầu hiện đại của giáo dục.

