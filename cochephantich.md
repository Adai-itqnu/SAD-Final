# Cơ chế phân tích

## 1. Persistency (Tính bền vững):
* Áp dụng: Hệ thống iLearn yêu cầu lưu trữ dữ liệu người dùng, dịch vụ, các nhóm hợp tác, và tài liệu học tập một cách lâu dài. Các dịch vụ như dữ liệu xác thực, dữ liệu cấu hình và dữ liệu học tập phải được duy trì ngay cả khi hệ thống tắt.
* Ví dụ: Dữ liệu của các nhóm học tập, tài liệu, và các cài đặt dịch vụ cấu hình có thể được lưu trữ trong cơ sở dữ liệu hoặc hệ thống lưu trữ bền vững để đảm bảo tính liên tục của quá trình học.
## 2. Communication (Giao tiếp - IPC và RPC):
* Áp dụng: iLearn cần một cơ chế giao tiếp giữa các dịch vụ để cho phép dịch vụ tích hợp như xác thực, quản lý khóa học và dịch vụ chia sẻ tài liệu giao tiếp với nhau. Điều này có thể sử dụng RPC để gọi các chức năng từ xa, ví dụ: các dịch vụ xác thực hoặc API quản lý khóa học có thể được gọi từ các dịch vụ khác.
* Ví dụ: Dịch vụ xác thực có thể được gọi bởi các dịch vụ ứng dụng khác (như VLE) để xác minh người dùng.
## 3. Message Routing (Định tuyến thông điệp):
* Áp dụng: Để các dịch vụ trong iLearn có thể tương tác với nhau, cần có một cơ chế định tuyến thông điệp giữa các dịch vụ tích hợp và dịch vụ độc lập.
* Ví dụ: Một dịch vụ xác thực có thể định tuyến thông điệp đến các dịch vụ khác để chia sẻ thông tin về người dùng đã đăng nhập.
## 4. Distribution (Phân phối):
* Áp dụng: Hệ thống iLearn yêu cầu khả năng phân phối dữ liệu và các dịch vụ (như tài liệu học tập, thông tin nhóm) qua nhiều hệ thống, có thể là dữ liệu phân tán giữa các khu vực hoặc nền tảng khác nhau.
* Ví dụ: Dịch vụ như gói năng suất (MS Office 365) có thể được tích hợp và phân phối cho các nhóm người dùng khác nhau, mỗi nhóm có thể sử dụng các dịch vụ khác nhau tùy vào yêu cầu học tập.
## 5. Transaction Management (Quản lý giao dịch):
* Áp dụng: Để đảm bảo rằng các thay đổi (chẳng hạn như việc thay đổi cài đặt cấu hình hoặc quyền truy cập vào các dịch vụ) được thực hiện một cách an toàn và có thể khôi phục nếu có lỗi, quản lý giao dịch là cần thiết.
* Ví dụ: Khi người dùng thay đổi cấu hình của nhóm học hoặc cấu hình dịch vụ, các thay đổi cần phải đảm bảo tính toàn vẹn (ACID).
## 6. Security (Bảo mật):
* Áp dụng: Hệ thống iLearn phải đảm bảo tính bảo mật, bao gồm xác thực người dùng, bảo vệ dữ liệu học tập và các thông tin cá nhân của người dùng khỏi truy cập trái phép.
* Ví dụ: Cơ chế xác thực người dùng phải đảm bảo rằng chỉ những người dùng có quyền mới có thể truy cập vào các dịch vụ và tài liệu học tập.
## 7. Error Detection/Handling/Reporting (Phát hiện lỗi, xử lý lỗi và báo cáo lỗi):
* Áp dụng: Cần có cơ chế để phát hiện và xử lý lỗi khi một dịch vụ không hoạt động như mong muốn, chẳng hạn như lỗi trong dịch vụ xác thực hoặc trong việc chia sẻ tài liệu giữa các nhóm.
* Ví dụ: Khi dịch vụ xác thực gặp sự cố, hệ thống phải phát hiện lỗi và thông báo cho người dùng hoặc quản trị viên về vấn đề này.
## 8. Redundancy (Dư thừa):
* Áp dụng: Để tăng tính sẵn sàng của hệ thống và giảm thiểu sự gián đoạn, các dịch vụ quan trọng trong hệ thống iLearn, như dịch vụ xác thực hoặc lưu trữ dữ liệu, có thể được xây dựng với khả năng dự phòng hoặc dư thừa.
* Ví dụ: Dữ liệu người dùng có thể được sao lưu hoặc lưu trữ trên các hệ thống khác nhau để đảm bảo rằng hệ thống vẫn hoạt động khi có sự cố với một hệ thống lưu trữ.
## 9. Legacy Interface (Giao diện kế thừa):
* Áp dụng: Hệ thống iLearn cần phải hỗ trợ các giao diện kế thừa, đặc biệt là khi tích hợp các công cụ hoặc dịch vụ có sẵn từ bên ngoài (ví dụ: MS Office 365) hoặc các công cụ học tập cũ mà các trường học đang sử dụng.
* Ví dụ: iLearn có thể hỗ trợ giao diện với các công cụ học tập cũ như Moodle hoặc Blackboard, đảm bảo sự tương thích khi chuyển đổi sang hệ thống mới.
## 10. Process Control and Synchronization (Kiểm soát và đồng bộ hóa tiến trình):
* Áp dụng: Hệ thống iLearn phải đảm bảo rằng các tiến trình hoặc dịch vụ hoạt động đồng bộ để tránh xung đột, đặc biệt khi nhiều dịch vụ cố gắng truy cập hoặc thay đổi dữ liệu cùng một lúc.
* Ví dụ: Khi nhiều người dùng đang truy cập vào cùng một tài liệu học tập hoặc nhóm học, hệ thống cần đồng bộ hóa để tránh các xung đột.
## 11. Information Exchange, Format Conversion (Trao đổi thông tin, chuyển đổi định dạng):
* Áp dụng: iLearn sẽ cần trao đổi dữ liệu và tài liệu giữa các dịch vụ, đồng thời có khả năng chuyển đổi định dạng tài liệu để tương thích với các công cụ khác nhau (ví dụ: từ tài liệu Google Drive sang MS Office).
* Ví dụ: Chuyển đổi tài liệu giữa các định dạng như DOCX, PDF, hoặc Google Docs



# Kiến trúc đề xuất

* Kiến trúc nhiều lớp
