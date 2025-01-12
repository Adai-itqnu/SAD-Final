8. Phụ huynh theo dõi tiến độ học tập của học sinh
Mô tả:

    Quá trình phụ huynh theo dõi tiến độ học tập của học sinh qua hệ thống iLearn. Sau khi đăng nhập, phụ huynh có thể xem thông tin về điểm số, bài tập, tình trạng tham gia lớp học và nhận xét từ giáo viên của học sinh. Hệ thống cũng cho phép tải xuống báo cáo học tập hoặc liên hệ với giáo viên nếu cần.

Các tác nhân:

    Phụ huynh: Người theo dõi tiến độ học tập của học sinh.
    Hệ thống iLearn: Cung cấp thông tin về học sinh cho phụ huynh.
    Học sinh: Người mà phụ huynh theo dõi tiến độ học tập.
    Giáo viên: Cung cấp nhận xét và thông tin về học sinh.

Mục tiêu:

    Cung cấp thông tin chi tiết về tiến độ học tập của học sinh cho phụ huynh.
    Tạo điều kiện cho phụ huynh theo dõi các yếu tố quan trọng như điểm số, bài tập, và sự tham gia lớp học của học sinh.
    Cung cấp báo cáo học tập và liên hệ với giáo viên khi cần thiết.

Cơ chế phân tích:

    Tính bền vững (Persistency): Lưu trữ dữ liệu về điểm số, bài tập và các nhận xét trong cơ sở dữ liệu.
    Phát hiện lỗi (Error Detection/Handling/Reporting): Hiển thị thông báo lỗi nếu không truy xuất được dữ liệu.
    Bảo mật (Security): Xác thực phụ huynh trước khi cho phép truy cập dữ liệu học sinh.

Luồng sự kiện chính:

    Phụ huynh đăng nhập vào hệ thống bằng tài khoản đã được cấp.
    Phụ huynh chọn chức năng "Theo dõi tiến độ học tập".
    Hệ thống hiển thị danh sách các con của phụ huynh (nếu có nhiều hơn một học sinh).
    Phụ huynh chọn học sinh muốn theo dõi.
    Hệ thống hiển thị: Điểm số của học sinh theo môn học. Danh sách bài tập đã nộp/chưa nộp. Tình trạng tham gia lớp học (đi học đầy đủ, đi trễ, nghỉ học). Nhận xét từ giáo viên.
    Nếu cần, phụ huynh tải xuống báo cáo học tập hoặc nhấn nút "Liên hệ giáo viên".

Luồng sự kiện phụ:

    Nếu không có dữ liệu: Hệ thống hiển thị thông báo, hướng dẫn phụ huynh liên hệ với giáo viên.
    Nếu có lỗi kết nối: Hệ thống hiển thị "Không thể kết nối đến máy chủ. Vui lòng thử lại sau."

Biểu đồ luồng sự kiện:

Theo Doi Tien Do Hoc Tap
