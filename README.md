# Hệ thống Quản trị Tri thức Doanh nghiệp (KMS) ứng dụng Drools Rule Engine
# 1. Giới thiệu dự án
Dự án tập trung xây dựng một Hệ thống Quản trị Tri thức (Knowledge Management System - KMS) nhằm giải quyết bài toán "lập trình cứng" (hard-code) các quy tắc nghiệp vụ trong doanh nghiệp. Bằng cách tách biệt hoàn toàn Logic ứng dụng và Logic nghiệp vụ, hệ thống cho phép các chuyên gia không cần am hiểu sâu về lập trình vẫn có thể tự điều chỉnh các chính sách, quy định của doanh nghiệp một cách linh hoạt thông qua ngôn ngữ luật Drools (DRL).
Các tính năng cốt lõi:
-Phân tách triệt để Logic nghiệp vụ và mã nguồn Java.
-Cơ chế cập nhật tri thức động (Hot-reload) không cần khởi động lại hệ thống.
-Hỗ trợ quản trị đa phân hệ: Nhân sự (HR), Sản xuất (Production), và Tài chính (Finance).
# 2. Cơ sở lí thuyết
Hệ thống được xây dựng dựa trên nền tảng của một Hệ chuyên gia (Expert System) tiêu chuẩn, bao gồm ba thành phần chính:
-Cơ sở tri thức (Knowledge Base): Lưu trữ dưới dạng các tập tin .drl chứa các quy tắc nghiệp vụ động.
-Bộ nhớ làm việc (Working Memory): Chứa các dữ kiện thực tế được định nghĩa qua các đối tượng DTO (EmployeeDTO, ProductionDTO, FinanceTransactionDTO).
-Bộ máy suy diễn (Inference Engine): Sử dụng thư viện Drools với giải thuật Rete nâng cao để thực hiện khớp mẫu (pattern matching) và suy diễn tiến (Forward Chaining).
# 3. Kiến trúc dự án
Dự án áp dụng kiến trúc phân lớp (Layered Architecture) kết hợp giao diện Master-Detail Dashboard để tối ưu hóa quản lý.
-Giao diện (UI Layer): Sử dụng thư viện FlatLaf để tạo giao diện hiện đại, trực quan cho các bảng điều khiển.
-Tầng xử lý (Service Layer): Tích hợp Drools Engine để điều phối phiên làm việc (KieSession) và kích hoạt các luật nghiệp vụ.
-Tầng dữ liệu (Data Layer): Lưu trữ thông tin thực thể trong cơ sở dữ liệu quan hệ và các tệp tin .drl độc lập, đảm bảo tính nhất quán và khả năng mở rộng.
# 4. Triển khai và Kết quả
Hệ thống triển khai thành công các quy tắc nghiệp vụ thực tế cho 03 phân hệ chính:
-Phân hệ Nhân sự: Tự động hóa quy trình xử lý kỷ luật và tính lương dựa trên chuyên cần.
-Phân hệ Sản xuất: Chẩn đoán và phân loại mức độ nghiêm trọng của lỗi sản phẩm thông qua thuộc tính độ ưu tiên (salience).
-Phân hệ Tài chính: Tự động hóa quy trình duyệt chi dựa trên các hạn mức tài chính linh hoạt.
-Cơ chế An toàn: Tích hợp lớp Validation để kiểm tra cú pháp luật DRL trước khi nạp vào hệ thống, đảm bảo ứng dụng không bị gián đoạn khi người dùng nhập sai quy tắc.
# 5. Tổng kết
Dự án đã đạt được các mục tiêu đề ra về việc xây dựng một hệ thống KMS linh hoạt, ổn định và có khả năng mở rộng. Trong tương lai, hệ thống hướng tới việc phát triển giao diện kéo - thả (Drag & Drop UI) để giúp người dùng cuối tiếp cận tri thức doanh nghiệp một cách tự động hóa và an toàn tuyệt đối mà không cần soạn thảo mã nguồn thủ công.
# Tài liệu tham khảo
-Drools Documentation 
-FlatLaf Library 
-Bài giảng môn Công nghệ tri thức - SGU
