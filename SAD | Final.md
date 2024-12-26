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

