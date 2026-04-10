I. Lịch sử cập nhật
Thời gian
A*M, D
Thay đổi
Mô tả chi tiết
27/01/2026
A
1.0.1- HuyGT
Xây dựng tài liệu nghiệp vụ đầy đủ cho hệ thống SEHO Plus
18/3/2026
M
1.2.2- HuyGT
Mọi thông tin trong tài liệu được lấy từ Sandbox.
*A - Added M - Modified D - Deleted
# II. Yêu cầu phần mềm
## 1. Tổng quan yêu cầu
### 1.1 Context Diagram
### 1.2 Data flow diagram
### 1.2 User Requirements
#### 1.2.1 Actors
Hệ thống cho phép quản trị viên tự cấu hình ma trận phân quyền (Permission Matrix). Mỗi chức năng sẽ đi kèm với các hành động cụ thể. Quản trị viên có thể tạo ra các nhóm quyền (Role) và gán các chức năng trên hệ thống vào nhóm quyền đó, sau đó áp dụng nhóm quyền cho người dùng.
Actor
Description
1
Admin
Là người dùng có quyền hạn cao nhất trong hệ thống. Admin chịu trách nhiệm quản trị vận hành, thiết lập cấu hình hệ thống, quản lý danh mục dùng chung và đặc biệt là tự cấu hình ma trận phân quyền (Permission Matrix). Admin có khả năng khởi tạo các nhóm quyền (Roles), gán các chức năng/hành động tương ứng và chỉ định nhóm quyền đó cho từng người dùng cụ thể.
2
User
Là người dùng cuối (có thể bao gồm các vai trò nghiệp vụ như người vận hành, quản lý nhà máy, hoặc tùy theo Role được gán). User thực hiện các thao tác nghiệp vụ trên hệ thống dựa trên các chức năng đã được Admin phân quyền. Phạm vi truy cập dữ liệu và các hành động (Xem, Thêm, Sửa, Xóa) của User bị giới hạn nghiêm ngặt bởi Nhóm phân quyền mà họ đang gán.
#### 1.2.2 Use Cases
ID
Feature/Workflow
Use Case
Use Case Description
01
Login
Đăng nhập
Cho phép người dùng xác thực và truy cập vào các chức năng của hệ thống.
02
Logout
Đăng xuất
Cho phép người dùng đăng xuất khỏi hệ thống một cách an toàn, kết thúc phiên làm việc hiện tại và bảo vệ tài khoản khỏi truy cập trái phép.
03
Tài khoản
Đổi mật khẩu
Cho phép người dùng thay đổi mật khẩu hiện tại để tăng cường bảo mật tài khoản.
04
Tài khoản
Thông tin tài khoản
Cho phép người dùng xem chi tiết thông tin cá nhân hoặc thông tin tài khoản của mình.
05
Tài khoản
Tạo tài khoản mới
Cho phép Admin/Quản trị viên khởi tạo một tài khoản người dùng mới trong hệ thống.
06
Tài khoản
Cập nhật thông tin tài khoản
Cho phép người dùng hoặc Admin chỉnh sửa các thông tin chi tiết của tài khoản.
07
Phân quyền
Thêm nhóm quyền
Cho phép Admin tạo mới một nhóm quyền (Role) với các tập hợp chức năng/hành động khác nhau.
08
Phân quyền
Chỉnh sửa nhóm quyền
Cho phép Admin điều chỉnh tên, mô tả và các chức năng/hành động được gán cho một nhóm quyền hiện có.
09
Phân quyền
Xóa nhóm quyền
Cho phép Admin loại bỏ một nhóm quyền khỏi hệ thống (có thể kèm điều kiện không còn người dùng nào được gán).
10
Cấu hình (Cài đặt trạm)
Tạo trạm mới
Cho phép thiết lập thông tin cơ bản và vị trí cho một trạm quan trắc hoặc vận hành mới.
11
Cấu hình (Cài đặt trạm)
Lấy thông tin trạm
Cho phép truy xuất và hiển thị dữ liệu cấu hình chi tiết của một trạm.
12
Cấu hình (Cài đặt trạm)
Chỉnh sửa thông tin trạm
Cho phép cập nhật các thông số cấu hình của một trạm hiện có.
13
Cấu hình (Cài đặt trạm)
Ẩn/hiện trạm trên bản đồ
Cho phép bật hoặc tắt hiển thị vị trí của trạm trên giao diện bản đồ.
14
Cấu hình (Cài đặt cảm biến)
Cài đặt cảm biến
Cho phép thiết lập các thông số kỹ thuật và cấu hình đo lường cho một cảm biến mới.
15
Cấu hình (Cài đặt cảm biến)
Chỉnh sửa thông tin cảm biến
Cho phép cập nhật các thông số cấu hình của một cảm biến hiện có.
16
Cấu hình (Cài đặt cảm biến)
Xóa cảm biến
Cho phép loại bỏ một cảm biến khỏi danh sách cấu hình của hệ thống.
17
Cấu hình (Cài đặt giá)
Thêm mới bảng dữ liệu mùa
Cho phép Admin tạo bảng dữ liệu mùa mới để quản lý giá theo mùa.
18
Cấu hình (Cài đặt giá)
Chỉnh sửa bảng dữ liệu mùa
Cho phép Admin cập nhật thông tin trong bảng dữ liệu mùa hiện có.
19
Cấu hình (Cài đặt giá)
Khóa bảng dữ liệu mùa
Cho phép Admin khóa một bảng dữ liệu mùa, ngăn chặn mọi thay đổi.
20
Cấu hình (Cài đặt giá)
Tải lại dữ liệu mùa
Cho phép đồng bộ hoặc tải lại dữ liệu cho bảng dữ liệu mùa.
21
Cấu hình (Cài đặt giá)
Thêm bảng khung giờ
Cho phép Admin tạo bảng khung giờ mới để quản lý giá theo thời gian trong ngày.
22
Cấu hình (Cài đặt giá)
Chỉnh sửa dữ liệu khung giờ
Cho phép Admin cập nhật thông tin trong bảng dữ liệu khung giờ hiện có.
23
Cấu hình (Cài đặt giá)
Khóa dữ liệu khung giờ
Cho phép Admin khóa một bảng dữ liệu khung giờ, ngăn chặn mọi thay đổi.
24
Cấu hình (Cài đặt giá)
Sao chép dữ liệu khung giờ
Cho phép tạo bản sao của một bảng dữ liệu khung giờ hiện có.
25
Cấu hình (Cài đặt giá)
Thêm dữ liệu theo ngày
Cho phép thêm các thiết lập giá đặc biệt hoặc ngoại lệ theo từng ngày cụ thể.
26
Cấu hình (Cài đặt giá)
Tải lại dữ liệu khung giờ
Cho phép đồng bộ hoặc tải lại dữ liệu cho bảng dữ liệu khung giờ.
27
Cấu hình (Cài đặt giá)
Thêm vùng tính giá
Cho phép Admin định nghĩa một khu vực địa lý hoặc khu vực kinh doanh mới để áp dụng cơ chế tính giá riêng biệt.
28
Cấu hình (Cài đặt giá)
Chỉnh sửa vùng tính giá
Cho phép Admin cập nhật thông tin, ranh giới hoặc quy tắc của vùng tính giá.
29
Cấu hình (Cài đặt giá)
Thêm bảng giá
Cho phép Admin tạo một bảng giá mới với các mức giá và quy tắc cụ thể.
30
Cấu hình (Cài đặt giá)
Chỉnh sửa bảng giá
Cho phép Admin cập nhật các mức giá, điều kiện hoặc quy tắc trong bảng giá hiện có.
31
Cấu hình (Cài đặt giá)
Khóa bảng giá
Cho phép Admin khóa một bảng giá, ngăn chặn mọi thay đổi đối với các mức giá đã thiết lập.
32
Cấu hình (Cài đặt giá)
Thêm khung giờ và giá trị mới
Cho phép bổ sung một khung giờ mới cùng với mức giá tương ứng vào bảng giá.
33
Cấu hình (Bảng nội suy)
Cập nhật bảng nội suy
Cho phép Admin điều chỉnh dữ liệu trong bảng nội suy để tính toán các thông số không đo trực tiếp.
34
Cấu hình (Bảng nội suy)
Tải bảng nội suy xuống
Cho phép người dùng tải về tệp dữ liệu của bảng nội suy hiện tại.
35
Cấu hình (Cài đặt dự án)
Cập nhật thông tin thủy điện
Cho phép cập nhật các thông số kỹ thuật và quản lý của công trình thủy điện.
36
Cấu hình (Cài đặt dự án)
Cập nhật thông tin hồ chứa
Cho phép cập nhật các thông số vận hành và quản lý của hồ chứa.
37
Cấu hình (Cài đặt dự án)
Cập nhật dữ liệu xả lũ
Cho phép cập nhật thông tin và quy tắc liên quan đến dữ liệu xả lũ.
38
Cấu hình (Cài đặt dự án)
Cập nhật tuyến năng lượng
Cho phép điều chỉnh thông tin về các đường truyền/tuyến năng lượng trong dự án.
39
Cấu hình (Cài đặt dự án)
Cập nhật thông tin nhà máy
Cho phép cập nhật các thông số quản lý, vị trí và kỹ thuật của nhà máy điện.
40
Cấu hình (Cài đặt dự án)
Cập nhật thông tin vị trí đo
Cho phép điều chỉnh thông tin về các điểm đo lường trong hệ thống.
41
Cấu hình (Cài đặt dự án)
Cập nhật thông tin tổ máy
Cho phép cập nhật các thông số kỹ thuật và trạng thái của từng tổ máy phát điện.
42
Cấu hình (Cài đặt dự án)
Cập nhật thông tin cửa xả
Cho phép cập nhật thông số và quy tắc vận hành của các cửa xả.
43
Cấu hình (Cài đặt dự án)
Cập nhật thông tin lưu vực
Cho phép cập nhật các thông số địa lý và thủy văn của lưu vực.
44
Cấu hình (Cài đặt dự án)
Cập nhật cài đặt hiển thị
Cho phép tùy chỉnh các tham số hiển thị dữ liệu trên giao diện người dùng.
45
Cấu hình (Cài đặt dự án)
Ẩn/hiện thông số dự báo
Cho phép bật hoặc tắt hiển thị các thông số dự báo trên giao diện.
46
Cấu hình (Cài đặt dự án)
Ẩn/hiện mưa quan trắc
Cho phép bật hoặc tắt hiển thị dữ liệu mưa quan trắc được thu thập.
47
Cấu hình (Cài đặt dự án)
Ẩn/hiện mưa phân tích
Cho phép bật hoặc tắt hiển thị dữ liệu mưa đã được phân tích.
48
Cấu hình (Cài đặt dự án)
Ẩn/hiện mưa dự báo
Cho phép bật hoặc tắt hiển thị dữ liệu mưa dự báo.
49
Cấu hình (Cài đặt dự án)
Ẩn/hiện lưu lượng dự báo
Cho phép bật hoặc tắt hiển thị dữ liệu lưu lượng dự báo.
50
Cấu hình (Cấu hình cảnh báo)
Thêm mới cảnh báo
Cho phép Admin tạo một quy tắc cảnh báo mới dựa trên các ngưỡng và điều kiện.
51
Cấu hình (Cấu hình cảnh báo)
Chỉnh sửa cảnh báo
Cho phép Admin điều chỉnh ngưỡng, điều kiện hoặc thông tin của một cảnh báo hiện có.
52
Cấu hình (Cấu hình cảnh báo)
Xóa cảnh báo
Cho phép Admin loại bỏ một quy tắc cảnh báo không còn sử dụng.
53
Cấu hình (Cài đặt khác)
Cài đặt bảng nội suy cửa van
Cho phép thiết lập hoặc cập nhật bảng nội suy liên quan đến việc vận hành cửa van.
54
Báo cáo(Báo cáo pháp lý)
Tải dữ liệu báo cáo pháp lý theo mẫu
Cho phép tải dữ liệu về một tệp mẫu báo cáo pháp lý để người dùng theo dõi số liệu và sử dụng.
55
Báo cáo(Báo cáo pháp lý)
Tải dữ liệu báo cáo pháp lý về máy tính
Cho phép xuất dữ liệu báo cáo pháp lý đã tổng hợp về máy tính cá nhân.
56
Báo cáo(Báo cáo Sản lượng & Doanh thu)
Thiết lập kế hoạch sản lượng doanh thu năm
Cho phép người dùng nhập và lưu trữ các chỉ tiêu kế hoạch sản lượng và doanh thu cho cả năm.
57
Báo cáo(Báo cáo Sản lượng & Doanh thu)
Xuất báo cáo sản lượng doanh thu
Cho phép người dùng tạo và tải về báo cáo tổng hợp về sản lượng và doanh thu.
58
Báo cáo(Báo cáo Sản lượng & Doanh thu)
Cập nhật sản lượng thực tế
Cho phép nhập hoặc cập nhật dữ liệu sản lượng thực tế đã đạt được.
59
Báo cáo(Báo cáo Sản lượng & Doanh thu)
Cập nhật doanh thu thực tế
Cho phép nhập hoặc cập nhật dữ liệu doanh thu thực tế đã đạt được.
60
Báo cáo(Bảng dữ liệu)
Lấy dữ liệu bảng dữ liệu vận hành
Cho phép truy xuất và hiển thị dữ liệu vận hành chi tiết trong dạng bảng.
61
Báo cáo(Bảng dữ liệu)
Lấy dữ liệu sai số dự báo
Cho phép truy xuất và hiển thị các số liệu về sai số giữa giá trị dự báo và thực tế.
62
Báo cáo(Dashboard)
Dữ liệu mưa trung bình thực đo
Cho phép hiển thị giá trị mưa trung bình được đo lường thực tế trên Dashboard.
63
Báo cáo(Dashboard)
Dữ liệu trung bình lưới mưa
Cho phép hiển thị giá trị mưa trung bình tính toán theo phương pháp lưới trên Dashboard.
64
Báo cáo(Dashboard)
Thay đổi thời gian quan trắc dữ liệu
Cho phép người dùng tùy chỉnh khoảng thời gian để xem dữ liệu quan trắc.
65
Báo cáo(Dashboard)
Thay đổi khoảng thời gian dự báo
Cho phép người dùng tùy chỉnh khoảng thời gian cho các dữ liệu dự báo được hiển thị.
66
Báo cáo(Dashboard)
Tính bù
Cho phép thực hiện chức năng tính toán bù trừ dữ liệu (ví dụ: bù thiếu/sai số).
67
Báo cáo(Dashboard)
Đánh giá khuyến nghị (Phù hợp – Không phù hợp
Cho phép người dùng đưa ra nhận xét hoặc đánh giá về độ tin cậy/mức độ phù hợp của các khuyến nghị vận hành.
68
Báo cáo(Dashboard)
Truy cập nhanh trang truyền dữ liệu
Cho phép điều hướng trực tiếp đến giao diện quản lý truyền dữ liệu.
69
Báo cáo(Dashboard)
Truy cập nhanh kinh bản khuyến nghị
Cho phép điều hướng trực tiếp đến giao diện xem/chỉnh sửa các kịch bản khuyến nghị.
70
Báo cáo(Dashboard)
Truy cập nhanh kịch bản tùy chỉnh
Cho phép điều hướng trực tiếp đến giao diện quản lý các kịch bản tùy chỉnh của người dùng.
71
Báo cáo(Truyền dữ liệu)
Thêm mới đường truyền dữ liệu
Cho phép thiết lập một kết nối hoặc kênh mới để truyền nhận dữ liệu.
72
Báo cáo(Truyền dữ liệu)
Cài đặt đường truyền dữ liệu
Cho phép cấu hình các thông số kỹ thuật và quy tắc cho đường truyền dữ liệu.
73
Báo cáo(Truyền dữ liệu)
Truyền bù dữ liệu
Cho phép thực hiện việc truyền lại hoặc bù đắp dữ liệu bị thiếu/lỗi trong một khoảng thời gian nhất định.
74
Báo cáo(Truyền dữ liệu)
Lịch sử truyền dữ liệu
Cho phép xem lại nhật ký chi tiết về các giao dịch và trạng thái truyền dữ liệu đã thực hiện
75
Báo cáo(Truyền dữ liệu)
Xóa đường truyền dữ liệu
Cho phép Admin loại bỏ một đường truyền dữ liệu không còn sử dụng.
76
Báo cáo(Truyền dữ liệu)
Thêm yếu tố truyền
Cho phép bổ sung một thông số hoặc loại dữ liệu mới vào cấu hình đường truyền.
77
Báo cáo(Truyền dữ liệu)
Chỉnh sửa yếu tố truyền
Cho phép cập nhật các thông số của một yếu tố truyền dữ liệu hiện có.
78
Báo cáo(Truyền dữ liệu)
Xóa yếu tố truyền
Cho phép loại bỏ một thông số khỏi cấu hình truyền dữ liệu.
79
Báo cáo(Thời tiết & Dự báo)
Dữ liệu mưa
Cho phép người dùng xem dữ liệu chi tiết về lượng mưa theo thời gian và khu vực.
80
Báo cáo(Thời tiết & Dự báo)
Bản đồ radar
Cho phép hiển thị dữ liệu radar thời tiết trên bản đồ, theo dõi diễn biến mưa.
81
Báo cáo(Thời tiết & Dự báo)
Bản đồ bão
Cho phép hiển thị đường đi và thông tin dự báo về các cơn bão trên bản đồ.
82
Báo cáo(Thời tiết & Dự báo)
Chuyển hướng đến vị trí cơn bão
Cho phép tự động định vị và tập trung bản đồ vào vị trí hiện tại hoặc dự báo của cơn bão.
83
Báo cáo(Thời tiết & Dự báo)
Xem dữ liệu trạm trên bản đồ
Cho phép hiển thị các thông số đo được của trạm trực tiếp trên bản đồ.
84
Báo cáo(Thời tiết & Dự báo)
Chi tiết dữ liệu trạm
Cho phép người dùng xem bảng/biểu đồ dữ liệu chi tiết của một trạm cụ thể.
85
Báo cáo(Thời tiết & Dự báo)
Tùy chỉnh thời gian lấy dữ liệu trạm
Cho phép người dùng chọn khoảng thời gian mong muốn để truy xuất dữ liệu từ trạm.
86
Báo cáo(Thời tiết & Dự báo)
Tải xuống dữ liệu trạm
Cho phép người dùng xuất dữ liệu đã chọn từ trạm về máy tính cá nhân.
87
Báo cáo(Thời tiết & Dự báo)
Thông tin thêm bản đồ - Dự báo mưa 24h
Cho phép bật/tắt lớp hiển thị dự báo lượng mưa trong 24 giờ tiếp theo trên bản đồ.
88
Báo cáo(Thời tiết & Dự báo)
Thông tin thêm bản đồ - Bảng tổng hợp các trạm
Cho phép hiển thị bảng tổng hợp các thông tin chính từ tất cả các trạm.
89
Báo cáo(Thời tiết & Dự báo)
Thông tin thêm bản đồ - Tổng hợp dữ liệu trạm dạng bảng
Cho phép hiển thị bảng dữ liệu chi tiết tổng hợp từ các trạm.
90
Mô phỏng vận hành
Chạy mô phỏng
Cho phép người dùng thực hiện một kịch bản mô phỏng vận hành hệ thống.
91
Mô phỏng vận hành
Thiết lập lại mô phỏng
Cho phép người dùng đặt lại các thông số và điều kiện ban đầu của kịch bản mô phỏng.
92
Mô phỏng vận hành
Tải lên kịch bản mô phỏng
Cho phép người dùng tải lên một tệp kịch bản mô phỏng đã được chuẩn bị sẵn.
93
Mô phỏng vận hành
Lưu kết quả mô phỏng
Cho phép lưu trữ kết quả đầu ra của một lần chạy mô phỏng.
94
Mô phỏng vận hành
Xem chi tiết kết quả mô phỏng
Cho phép hiển thị chi tiết các số liệu và biểu đồ từ kết quả mô phỏng đã lưu.
95
Mô phỏng vận hành
Tải kết quả mô phỏng lên dashboard
Cho phép hiển thị kết quả mô phỏng đã lưu lên giao diện Dashboard để so sánh hoặc tham khảo.
96
Mô phỏng vận hành
Chỉnh sửa kịch bản khuyến nghị
Cho phép người dùng điều chỉnh các thông số trong kịch bản khuyến nghị vận hành.
97
Mô phỏng vận hành
Tải lên kịch bản công suất
Cho phép tải lên tệp dữ liệu kịch bản về công suất vận hành.
98
Mô phỏng vận hành
Tải lên kịch bản lưu lượng vào
Cho phép tải lên tệp dữ liệu kịch bản về lưu lượng nước/vật chất đầu vào.
99
Mô phỏng vận hành
Tải lên kịch bản lưu lượng xả
Cho phép tải lên tệp dữ liệu kịch bản về lưu lượng nước/vật chất xả ra.
100
Log
Xem log hệ thống
Cho phép truy cập và xem nhật ký hoạt động chi tiết của hệ thống.
101
Log
Lọc log trên hệ thống
Cho phép người dùng tìm kiếm và lọc nhật ký hoạt động theo các tiêu chí (thời gian, loại sự kiện, người dùng...).
102
N/A
Chuyển đổi giao diện sáng/tối
Cho phép người dùng chuyển đổi giữa chế độ hiển thị giao diện sáng (light mode) và tối (dark mode).
## 2. UseCase Specifications
### 2.1. Đăng nhập
Use Case ID:
01
Use Case Name:
Đăng nhập
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
(Tác động khác đến chức năng)
None
Description:
(Mô tả)
Cho phép người dùng hoặc Quản trị viên xác thực thông tin tài khoản và truy cập vào các chức năng của hệ thống.
Precondition:
(Điều kiện cần)
Người dùng có tài khoản hợp lệ.
Post-condition:
(Điều kiện đủ)
Người dùng truy cập thành công được chuyển tới Dashboard/trang mặc định theo phân quyền.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập vào trang Đăng nhập.
2. Hệ thống yêu cầu Tên đăng nhập và Mật khẩu.
3. Người dùng nhập thông tin và nhấn nút "Đăng nhập".
4. Hệ thống xác thực thông tin đăng nhập (BR-L01, BR-L02).
5. Nếu thông tin hợp lệ, hệ thống kiểm tra trạng thái tài khoản (BR-L03) và tạo phiên làm việc (Session) mới.
6. Hệ thống chuyển hướng người dùng đến giao diện Dashboard chính (hoặc trang mặc định).
Alternative Flows:
(Luồng phụ)
A1: Người dùng quên mật khẩu.
→ Hệ thống chuyển hướng người dùng đến chức năng Phục hồi mật khẩu (Xem UC 03).
Exceptions:
(Trường hợp
ngoại lệ)
- Tên đăng nhập hoặc Mật khẩu không chính xác.
→ Hệ thống hiển thị thông báo lỗi "Tên đăng nhập hoặc mật khẩu không đúng." (BR-L01).
- . Tài khoản bị khóa (inactive).
→ Hệ thống hiển thị thông báo lỗi "Tài khoản của bạn đã bị khóa. Vui lòng liên hệ Admin." (BR-L03).
Business Rules:
(Nghiệp vụ)
BR-L01: Phải xác thực cả Tên đăng nhập và Mật khẩu.
BR-L02: Mật khẩu phải được mã hóa khi truyền tải và lưu trữ.
BR-L03: Chỉ cho phép đăng nhập nếu tài khoản đang ở trạng thái Active.
### 2.2. Đăng xuất
Use Case ID:
02
Use Case Name:
Đăng xuất
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng đăng xuất khỏi hệ thống một cách an toàn, kết thúc phiên làm việc hiện tại và bảo vệ tài khoản khỏi truy cập trái phép.
Precondition:
(Điều kiện cần)
Người dùng đang ở trạng thái đã đăng nhập (phiên làm việc đang hoạt động).
Post-condition:
(Điều kiện đủ)
Phiên làm việc kết thúc, người dùng được chuyển về trang Đăng nhập.
Normal Flow:
(Luồng chính)
1. Người dùng nhấn vào nút "Đăng xuất" trên giao diện hệ thống.
2. Hệ thống hủy phiên làm việc (Session) hiện tại và xóa token xác thực liên quan.
3. Hệ thống chuyển hướng người dùng trở lại trang Đăng nhập.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Lỗi hệ thống khi hủy phiên làm việc.
→ Hệ thống cố gắng thực hiện lại và thông báo lỗi nếu không thành công.
Business Rules:
(Nghiệp vụ)
BR-LO01: Tất cả các dữ liệu phiên làm việc và token phải được hủy khi người dùng đăng xuất.
BR-LO02: Phiên làm việc sẽ tự động hết hạn nếu không hoạt động trong một khoảng thời gian nhất định (ví dụ: 360 phút).
### 2.3. Đổi mật khẩu
Use Case ID:
03
Use Case Name:
Đổi mật khẩu
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng (User/Admin) thay đổi mật khẩu hiện tại của tài khoản để tăng cường bảo mật.
Precondition:
(Điều kiện cần)
PRE01- Người dùng đã đăng nhập.
PRE02- Admin có quyền đặt lại mật khẩu
Post-condition:
(Điều kiện đủ)
Mật khẩu của tài khoản được cập nhật.
Normal Flow:
(Luồng chính)
1. Tại thanh menu của hệ thống người dùng chọn vào ảnh đại diện của mình sau đó chọn "Đổi mật khẩu".
2. Người dùng nhập: Mật khẩu cũ(mật khẩu hiện tại), Mật khẩu mới, Xác nhận mật khẩu mới.
3. Hệ thống xác thực Mật khẩu hiện tại (BR-CP01).
4. Hệ thống kiểm tra Mật khẩu mới và Xác nhận mật khẩu mới có khớp nhau và tuân thủ quy tắc nghiệp vụ (BR-01).
5. Nếu hợp lệ, hệ thống mã hóa và cập nhật mật khẩu mới vào cơ sở dữ liệu.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
<Trang quản lý tài khoản>
Exceptions:
(Trường hợp
ngoại lệ)
- Mật khẩu hiện tại không chính xác.
→ Hệ thống hiển thị thông báo lỗi "Mật khẩu hiện tại không đúng." (BR-CP01).
- Mật khẩu mới không đáp ứng quy tắc nghiệp vụ (BR-01).
→ Hệ thống hiển thị thông báo lỗi về quy tắc mật khẩu.
3. Mật khẩu mới và Xác nhận mật khẩu mới không khớp nhau.  → Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-01: Mật khẩu phải có ít nhất 8 ký tự, bao gồm chữ hoa, chữ thường và số.
BR-CP01: Phải xác thực mật khẩu hiện tại trước khi cho phép cập nhật.
### 2.4. Thông tin tài khoản
Use Case ID:
04
Use Case Name:
Thông tin tài khoản
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng xem chi tiết thông tin cá nhân hoặc thông tin tài khoản của mình. Đối với Admin, có thể xem thông tin tài khoản của người dùng khác.(BR-A01)
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập.
Post-condition:
(Điều kiện đủ)
Thông tin tài khoản được hiển thị.
Normal Flow:
(Luồng chính)
1. Tại thanh menu của hệ thống người dùng chọn vào ảnh đại diện của mình sau đó chọn “Thông tin tài khoản” hoặc Admin truy cập danh sách người dùng và chọn một tài khoản.
2. Hệ thống xác định tài khoản cần xem.
3. Hệ thống tải và hiển thị các thông tin chi tiết của tài khoản (Tài khoản, Họ và tên, Chức danh).
4. Người dùng xem thông tin.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Không tìm thấy thông tin tài khoản tương ứng.
→ Hệ thống hiển thị thông báo lỗi "Không tìm thấy thông tin tài khoản".
Business Rules:
(Nghiệp vụ)
BR-A01: User chỉ có thể xem thông tin cá nhân của chính mình. Admin có thể xem thông tin của tất cả User.
### 2.5. Tạo tài khoản mới
Use Case ID:
05
Use Case Name:
Tạo tài khoản mới
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin khởi tạo một tài khoản người dùng mới (ví dụ: nhân viên vận hành, quản lý) trong hệ thống, chỉ định các thông tin cơ bản và nhóm quyền (Role) ban đầu.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Tạo tài khoản".
Post-condition:
(Điều kiện đủ)
Một tài khoản người dùng mới được tạo với trạng thái hoạt động.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Quản lý Tài khoản" -> "Tạo tài khoản mới".
2. Admin nhập các thông tin bắt buộc: Tên đăng nhập, Mật khẩu, Họ và tên, Vai trò (Role).
3. Admin nhấn nút "Tạo tài khoản".
4. Hệ thống kiểm tra tính duy nhất của Username (BR-AC01) và quy tắc mật khẩu (BR-01).
5. Nếu hợp lệ, hệ thống tạo tài khoản mới.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Username đã tồn tại (BR-AC01).
→ Hệ thống hiển thị thông báo lỗi "Tên đăng nhập đã được sử dụng."
- Mật khẩu không đáp ứng quy tắc (BR-01).
→ Hệ thống hiển thị thông báo lỗi về quy tắc mật khẩu.
- Thiếu trường thông tin bắt buộc.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-AC01: Tên đăng nhập Username phải là duy nhất.
BR-01: Mật khẩu phải có ít nhất 8 ký tự, bao gồm chữ hoa, chữ thường và số.
BR-A02: Chỉ Admin mới có quyền tạo và quản lý tài khoản người dùng.
### 2.6. Cập nhật thông tin tài khoản
Use Case ID:
06
Use Case Name:
Cập nhật thông tin tài khoản
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
DES-1: Cho phép Người dùng cập nhật thông tin cá nhân của mình (không bao gồm cả vai trò và trạng thái).
DES-2: Admin chỉnh sửa thông tin tài khoản (bao gồm cả vai trò và trạng thái) của bất kỳ người dùng nào.
Precondition:
(Điều kiện cần)
Người dùng/Admin đã đăng nhập. Admin có quyền "Cập nhật thông tin tài khoản" của người khác.
Post-condition:
(Điều kiện đủ)
Thông tin tài khoản được cập nhật trong hệ thống.
Normal Flow:
(Luồng chính)
1. Tại thanh menu của hệ thống người dùng chọn vào ảnh đại diện của mình sau đó chọn “thông tin tài khoản”.
2. Hệ thống tải và hiển thị thông tin hiện tại.
3. Người dùng chỉnh sửa các trường thông tin cho phép.
4. Người dùng nhấn nút "Lưu".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-AC01, BR-A03) và cập nhật thông tin.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
1. Người dùng đăng nhập bằng tài khoản admin, tại Menu chọn vào Quản lý, sau đó chọn quản lý “Tài khoản”.
2. Hệ thống tải và hiển thị thông tin toàn bộ tài khoản hiện tại.
3. Người dùng chọn và chỉnh sửa các trường thông tin cho tài khoản cần sửa.
4. Người dùng nhấn nút "Lưu".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-AC01, BR-A03) và cập nhật thông tin.
6. Hệ thống hiển thị thông báo thành công.
Exceptions:
(Trường hợp
ngoại lệ)
- Username mới trùng với tài khoản khác (BR-AC01).
→ Hệ thống hiển thị thông báo lỗi.
- Thiếu trường thông tin bắt buộc.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-AC01: Tên đăng nhập (Email/Username) phải là duy nhất.
BR-A02: Chỉ Admin mới có quyền tạo và quản lý tài khoản người dùng.
BR-A03: User không có quyền thay đổi Role hoặc Trạng thái tài khoản của chính mình.
### 2.7. Thêm nhóm quyền
Use Case ID:
07
Use Case Name:
Thêm nhóm quyền
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin tạo mới một nhóm quyền (Role) với các tập hợp chức năng/hành động khác nhau trong hệ thống.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Thêm nhóm quyền".
Post-condition:
(Điều kiện đủ)
Một nhóm quyền mới được tạo và sẵn sàng để gán cho người dùng.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Quản lý”, chọn ”Phân quyền" -> "Thêm nhóm quyền".
2. Hệ thống hiển thị biểu mẫu tạo mới và danh sách các chức năng/hành động có thể gán.
3. Admin nhập: Tên nhóm quyền (bắt buộc), Cấp độ quyền (bắt buộc), Mô tả (nếu cần).
4. Admin chọn các Chức năng/Hành động (permissions) tương ứng từ ma trận phân quyền (Permission Matrix).
5. Admin nhấn nút "Tạo mới".
6. Hệ thống kiểm tra tính duy nhất của Tên nhóm quyền (BR-R01) và lưu Role mới.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Tên nhóm quyền đã tồn tại (BR-R01).
→ Hệ thống hiển thị lỗi và yêu cầu nhập lại tên khác.
- Thiếu trường thông tin bắt buộc (Tên nhóm quyền).
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-R01: Tên nhóm quyền phải là duy nhất trong hệ thống.
BR-A02: Chỉ Admin mới có quyền tạo, sửa, xóa nhóm quyền.
### 2.8. Chỉnh sửa nhóm quyền
Use Case ID:
08
Use Case Name:
Chỉnh sửa nhóm quyền
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin điều chỉnh tên, mô tả và các chức năng/hành động (permissions) được gán cho một nhóm quyền hiện có.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Chỉnh sửa nhóm quyền".
Post-condition:
(Điều kiện đủ)
Thông tin và/hoặc quyền hạn của nhóm quyền đã được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập "Quản lý” chọn “Phân quyền" và chọn một nhóm quyền để chỉnh sửa.
2. Hệ thống tải và hiển thị thông tin và các quyền hiện tại của Role đó.
3. Admin thực hiện điều chỉnh Tên nhóm quyền, Mô tả, hoặc thay đổi các quyền hạn.
4. Admin nhấn nút "Lưu".
5. Hệ thống kiểm tra tính hợp lệ và lưu thay đổi vào cơ sở dữ liệu.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Tên nhóm quyền mới trùng với tên nhóm quyền khác (BR-R01).
→ Hệ thống hiển thị lỗi.
- Lỗi hệ thống khi cập nhật.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-R01: Tên nhóm quyền phải là duy nhất trong hệ thống.
BR-A02: Chỉ Admin mới có quyền tạo, sửa, xóa nhóm quyền.
### 2.9. Xóa nhóm quyền
Use Case ID:
09
Use Case Name:
Xóa nhóm quyền
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin loại bỏ một nhóm quyền khỏi hệ thống.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Xóa nhóm quyền".
Post-condition:
(Điều kiện đủ)
Nhóm quyền được chọn đã bị xóa khỏi hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập "Quản lý” chọn“Phân quyền".
2. Admin chọn một nhóm quyền để xóa.
3. Hệ thống hiển thị hộp thoại xác nhận.
4. Admin xác nhận xóa.
5. Hệ thống kiểm tra xem có người dùng nào đang gán nhóm quyền này hay không (BR-R02).
6. Nếu không, hệ thống xóa nhóm quyền đó khỏi cơ sở dữ liệu.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Nhóm quyền đang được gán cho ít nhất một người dùng (BR-R02).
→ Hệ thống hiển thị thông báo lỗi và không cho phép xóa, yêu cầu Admin phải gỡ gán hoặc xóa người dùng trước.
Business Rules:
(Nghiệp vụ)
BR-R02: Không được phép xóa một nhóm quyền nếu có bất kỳ người dùng nào đang gán nhóm quyền đó.
BR-A02: Chỉ Admin mới có quyền tạo, sửa, xóa nhóm quyền.
### 2.10. Tạo trạm mới
Use Case ID:
10
Use Case Name:
Tạo trạm mới
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép thiết lập thông tin cơ bảncho một trạm quan trắc hoặc vận hành mới trong hệ thống.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình trạm".
Post-condition:
(Điều kiện đủ)
Một trạm mới được tạo và sẵn sàng để cấu hình cảm biến.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Thông tin trạm" -> "Tạo trạm mới".
2. Admin nhập các thông tin bắt buộc: Mã trạm (ví dụ: ST01), Tên trạm,Địa chỉ lắp trạm, Tỉnh, ,Loại trạm, Nguồn dữ liệu, Cổng lắp cảm biến, Tọa độ (vĩ độ, kinh độ), Dữ liệu cuối lúc, Ẩn hiện trên bản đồ(UC-2.13).
3. Admin nhấn nút "Tạo mới".
4. Hệ thống kiểm tra tính duy nhất của Mã trạm (BR-ST01) và tính hợp lệ của tọa độ.
5. Nếu hợp lệ, hệ thống tạo bản ghi trạm mới.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Mã trạm đã tồn tại (BR-ST01).
→ Hệ thống hiển thị lỗi và yêu cầu nhập lại mã khác.
- Không lấy được thông tin trạm(kết nối với trạm)
→ Hệ thống hiển thị thông báo lỗi.
- Thiếu trường thông tin bắt buộc.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-ST01: Mã trạm phải là duy nhất.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình trạm.
BR-ST02: Trạm mới phải được gán cho một trạm đang hoạt động thực tế và cụ thể.
### 2.11. Lấy thông tin trạm
Use Case ID:
11
Use Case Name:
Lấy thông tin trạm
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép kết nối trực tiếp đến trạm ngoài thực tế.
Precondition:
(Điều kiện cần)
Người dùng có quyền truy cập vào thông tin trạm (BR-ST03).
Post-condition:
(Điều kiện đủ)
Thông báo trạm đã kết nối thành công.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Thông tin trạm".
2. Người dùng chọn vào chức năng “Lấy thông tin trạm”.
3. Hệ thống truy xuất dữ liệu chi tiết của trạm (mã trạm, tọa độ, loại trạm, danh sách cảm biến).
4. Hệ thống hiển thị thông tin trạm trên màn hình.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Trạm không tồn tại.
→ Hệ thống hiển thị thông báo lỗi "Không tìm thấy thông tin trạm."
Business Rules:
(Nghiệp vụ)
### 2.13. Ẩn/Hiện trạm trên bản đồ
Use Case ID:
13
Use Case Name:
Ẩn/hiện trạm trên bản đồ
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bật hoặc tắt hiển thị vị trí của trạm trên giao diện bản đồ mà không xóa dữ liệu của trạm đó.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình trạm". Trạm đã tồn tại trong hệ thống.
Post-condition:
(Điều kiện đủ)
Trạng thái hiển thị của trạm trên bản đồ được thay đổi.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Thông tin trạm".
2. Admin chọn một trạm và thay đổi trạng thái Ẩn/Hiện thông qua nút gạt.
3. Hệ thống ghi nhận trạng thái hiển thị mới vào cơ sở dữ liệu.
4. Hệ thống cập nhật giao diện bản đồ.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
- Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình trạm.
BR-ST05: Việc ẩn trạm chỉ ảnh hưởng đến hiển thị trên bản đồ, không ảnh hưởng đến việc thu thập và lưu trữ dữ liệu của trạm đó.
### 2.14. Cài đặt cảm biến
Use Case ID:
14
Use Case Name:
Cài đặt cảm biến
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép thiết lập các thông số kỹ thuật, cấu hình đo lường, và gán cho một trạm cụ thể đối với một cảm biến mới.
Đối với mỗi cảm biến sẽ có cấu hình thông số kỹ thuật khác nhau:
1. Đo mưa: (Tên trạm, Cổng lắp cảm biến, Trọng số trạm đo)
2. Đo mực nước: (Tên trạm, Cổng lắp cảm biến, Vị trí đo mực nước, Tên vị trí đo, Cao độ cảm biến, Cách đo mực nước)
3. Đo công suất máy: (Tên trạm, Cổng lắp cảm biến, Tổ máy,Cao trình tâm turbine, Mực nước thượng,Mực nước hạ,Nguồn nước)
4. Đo độ mở cửa van: (Tên trạm, Cổng lắp cảm biến,Cửa van, Mực nước thượng, Mực nước hạ, Nguồn nước)
5. Đo lưu lượng tổ máy: (Tên trạm, Cổng lắp cảm biến, Tổ máy, Cao trình tâm turbine, Nguồn nước)
6. Đo lưu lượng cửa van (Tên trạm, Cổng lắp cảm biến, Cửa van, Vị trí đo, Nguồn nước)
7. Đo lưu lượng kênh xả (Trực tiếp) (Tên trạm, Cổng lắp cảm biến,Kênh xả:Vị trí đo, Nguồn nước)
8. Đo lưu lượng kênh xả (Gián tiếp) (Tên trạm, Cổng lắp cảm biến,Kênh xả:Vị trí đo, Nguồn nước)
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình cảm biến". Trạm tương ứng đã được tạo (Xem UC 10).
Post-condition:
(Điều kiện đủ)
Cảm biến mới được cấu hình và liên kết với trạm.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cấu hình cảm biến".
2. Admin chọn chức năng "Thêm cảm biến mới".
3. Admin nhập các thông tin tùy theo yêu cầu của từng loại cảm biến.
4. Admin nhấn nút "Cập nhật".
5. Hệ thống kiểm tra tính duy nhất của Mã cảm biến (BR-S01) và tính hợp lệ của dữ liệu.
6. Nếu hợp lệ, hệ thống tạo bản ghi cảm biến mới và liên kết với trạm.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Mã cảm biến đã tồn tại (BR-S01).  → Hệ thống hiển thị lỗi và yêu cầu nhập lại mã khác.  2. Thiếu trường thông tin bắt buộc.  → Hệ thống hiển thị thông báo lỗi.  3. Trạm liên kết không tồn tại.  → Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-S01: Mã cảm biến phải là duy nhất trên toàn hệ thống.  BR-A02: Chỉ Admin mới có quyền quản lý cấu hình cảm biến.  BR-S02: Ngưỡng cảnh báo phải là các giá trị số và tuân theo giới hạn kỹ thuật của loại cảm biến (ví dụ: <tự thêm nghiệp vụ>).
### 2.15. Chỉnh sửa thông tin cảm biến
Use Case ID:
15
Use Case Name:
Chỉnh sửa thông tin cảm biến
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật các thông số cấu hình, đơn vị đo, hoặc ngưỡng cảnh báo của một loại cảm biến hiện có.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Chỉnh sửa cảm biến". Cảm biến đã tồn tại.
Post-condition:
(Điều kiện đủ)
Thông tin cấu hình cảm biến được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cấu hình cảm biến".
2. Người dùng chọn một cảm biến và nhấn nút "Chỉnh sửa".
3. Hệ thống tải và hiển thị thông tin cảm biến hiện tại.
4. Admin chỉnh sửa các trường thông tin cho phép (ví dụ: Tên cảm biến, Ngưỡng cảnh báo, Đơn vị đo).
5. Admin nhấn nút "Lưu/Cập nhật".
6. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-S02, BR-S03) và cập nhật thông tin.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Ngưỡng cảnh báo mới không hợp lệ (BR-S02).
→ Hệ thống hiển thị lỗi.
- Cố gắng thay đổi trường Mã cảm biến mà không được phép (BR-S03).
→ Hệ thống hiển thị cảnh báo/lỗi.
Business Rules:
(Nghiệp vụ)
BR-S02: Ngưỡng cảnh báo phải tuân thủ giới hạn kỹ thuật.
BR-S03: Mã cảm biến (ID) không được phép thay đổi sau khi tạo.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình cảm biến.
### 2.16. Xóa cảm biến
Use Case ID:
16
Use Case Name:
Xóa cảm biến
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép loại bỏ một cảm biến khỏi danh sách cấu hình của hệ thống.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Xóa cảm biến". Cảm biến đã tồn tại.
Post-condition:
(Điều kiện đủ)
Cảm biến được xóa khỏi cấu hình hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cấu hình cảm biến".
2. Người dùng chọn một cảm biến và nhấn nút "Xóa".
3. Hệ thống hiển thị hộp thoại xác nhận.
4. Admin xác nhận xóa.
5. Hệ thống xóa cảm biến khỏi danh sách cấu hình và nếu cần, lưu trữ/đánh dấu dữ liệu lịch sử.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1.Cảm biến đang được sử dụng trong một báo cáo quan trọng hoặc quy tắc nghiệp vụ khác (BR-S05).
→ Hệ thống hiển thị cảnh báo và yêu cầu Admin gỡ liên kết trước khi xóa.
- Lỗi hệ thống khi xóa dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-S05: Không thể xóa cảm biến nếu nó đang là thành phần chính trong các tính toán hoặc mô hình dự báo.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình cảm biến.
### 2.17. Thêm mới bảng dữ liệu mùa
Use Case ID:
17
Use Case Name:
Thêm mới bảng dữ liệu mùa
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin tạo bảng dữ liệu mới để quản lý giá, tham số hoặc quy tắc khác nhau áp dụng theo mùa hoặc giai đoạn thời gian dài.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cài đặt giá".
Post-condition:
(Điều kiện đủ)
Một bảng dữ liệu mùa mới được tạo với các tham số khởi tạo.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cài đặt giá" -> "Bảng dữ liệu mùa" -> "Thêm mới".
2. Admin nhập các thông tin bắt buộc: Tên mùa, Thời gian bắt đầu và Thời gian kết thúc, và các tham số dữ liệu mùa (ví dụ: giá trị cơ sở, hệ số...).
3. Admin nhấn nút "Hoàn thành".
4. Hệ thống tạo bản ghi bảng dữ liệu mùa mới.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Thiếu trường thông tin bắt buộc.
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-P01: Khoảng thời gian áp dụng của các bảng dữ liệu mùa không được chồng lấn nhau.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.18. Chỉnh sửa bảng dữ liệu mùa
Use Case ID:
18
Use Case Name:
Chỉnh sửa bảng dữ liệu mùa
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin cập nhật thông tin trong bảng dữ liệu mùa hiện có (Tên, Thời gian, hoặc các tham số dữ liệu mùa).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng dữ liệu mùa đã tồn tại (Xem UC 19).
Post-condition:
(Điều kiện đủ)
Thông tin của bảng dữ liệu mùa được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Bảng dữ liệu mùa", chọn một bảng và nhấn nút "Chỉnh sửa".
2. Hệ thống tải và hiển thị thông tin bảng dữ liệu hiện tại.
3. Admin chỉnh sửa các trường thông tin cho phép.
4. Admin nhấn nút "Hoàn thành".
5. Hệ thống cập nhật thông tin.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi cập nhật dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-P01: Khoảng thời gian áp dụng của các bảng dữ liệu mùa không được chồng lấn nhau.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.19. Khóa bảng dữ liệu mùa
Use Case ID:
19
Use Case Name:
Khóa bảng dữ liệu mùa
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin khóa một bảng dữ liệu mùa, ngăn chặn mọi thay đổi sau khi bảng đã được phê duyệt và đưa vào sử dụng.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng dữ liệu mùa đã tồn tại.
Post-condition:
(Điều kiện đủ)
Bảng dữ liệu mùa được đánh dấu là trạng thái Khóa.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Dữ liệu mùa", chọn một bảng.
2. Admin nhấn nút "Khóa bảng dữ liệu".
3. Hệ thống cập nhật trạng thái của bảng dữ liệu mùa thành Đã Khóa (BR-P04).
4. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.20. Tải lại dữ liệu mùa
Use Case ID:
20
Use Case Name:
Tải lại dữ liệu mùa
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
Hệ thống nguồn dữ liệu (Data Source)
Description:
(Mô tả)
Cho phép đồng bộ hoặc tải lại dữ liệu cho bảng dữ liệu mùa, thường được dùng để áp dụng ngay lập tức các thay đổi về giá trị hoặc tải dữ liệu từ một nguồn ngoại vi.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá".
Post-condition:
(Điều kiện đủ)
Dữ liệu của bảng dữ liệu mùa được đồng bộ/tải lại thành công.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Dữ liệu mùa", chọn một bảng.
2. Admin nhấn nút "Tải lại dữ liệu".
3. Hệ thống tiến hành kết nối đến nguồn dữ liệu và thực hiện quá trình đồng bộ dữ liệu.
4. Hệ thống cập nhật bản ghi dữ liệu mùa.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
None.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.21. Thêm bảng khung giờ
Use Case ID:
21
Use Case Name:
Thêm bảng khung giờ
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin tạo bảng khung giờ mới để quản lý giá, tham số hoặc quy tắc khác nhau áp dụng theo thời gian trong ngày (ví dụ: giờ cao điểm, thấp điểm).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá".
Post-condition:
(Điều kiện đủ)
Một bảng khung giờ mới được tạo và sẵn sàng để nhập dữ liệu.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cài đặt giá" -> "Bảng khung giờ" -> "Thêm mới".
2. Admin nhập các thông tin bắt buộc: Tên bảng khung giờ, Chi tiết giá từng khung giờ, từng ngày trong tuần.
3. Admin nhấn nút "Hoàn thành".
4. Hệ thống hiển thị thông báo thêm mới thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Thiếu trường thông tin bắt buộc (Tên bảng).
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.22. Chỉnh sửa dữ liệu khung giờ
Use Case ID:
22
Use Case Name:
Chỉnh sửa dữ liệu khung giờ
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin cập nhật các khung giờ cụ thể và giá trị/tham số tương ứng trong một bảng dữ liệu khung giờ hiện có.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng khung giờ đã tồn tại.
Post-condition:
(Điều kiện đủ)
Các khung giờ và dữ liệu liên quan được cập nhật trong bảng.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Bảng khung giờ", chọn một bảng và nhấn nút "Chỉnh sửa dữ liệu".
2. Hệ thống tải và hiển thị danh sách các khung giờ hiện tại.
3. Admin thực hiện các thao tác: Thêm khung giờ mới (giờ bắt đầu/kết thúc), Sửa các giá trị hiện có, hoặc Xóa khung giờ.
4. Admin nhấn nút "Hoàn thành".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu: đảm bảo các khung giờ không chồng lấn nhau và bao phủ hết 24 giờ (BR-P07).
6. Hệ thống cập nhật dữ liệu khung giờ.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
A1: Sử dụng chức năng Sao chép dữ liệu khung giờ (UC 24) để tạo một bản sao sử dụng cho các ngày khác trong tuần.
Exceptions:
(Trường hợp
ngoại lệ)
1. Các khung giờ bị chồng lấn hoặc không bao phủ hết 24 giờ (BR-P07).
→ Hệ thống hiển thị lỗi và yêu cầu điều chỉnh.
2. Giá trị nhập vào không hợp lệ (ví dụ: giá trị âm) (BR-P09).
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-P07: Các khung giờ trong cùng một bảng không được chồng lấn và nên bao phủ hết 24 giờ trong một ngày.
BR-P09: Giá trị/Tham số trong khung giờ phải tuân thủ quy tắc nghiệp vụ (ví dụ: >0).
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.23. Khóa dữ liệu khung giờ
Use Case ID:
23
Use Case Name:
Khóa dữ liệu khung giờ
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin khóa một bảng dữ liệu khung giờ, ngăn chặn hệ thống tự động đưa bảng dữ liệu khung giờ vào tính toán.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng khung giờ đã tồn tại.
Post-condition:
(Điều kiện đủ)
Bảng dữ liệu khung giờ được đánh dấu là trạng thái Đã khóa.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Bảng khung giờ", chọn một bảng.
2. Admin nhấn nút "Khóa dữ liệu khung giờ".
3. Hệ thống cập nhật trạng thái của bảng khung giờ thành Đã khóa.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Bảng dữ liệu khung giờ đã ở trạng thái Locked.
→ Hệ thống hiển thị cảnh báo.
2. Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.24. Sao chép dữ liệu khung giờ
Use Case ID:
24
Use Case Name:
Sao chép dữ liệu khung giờ
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép tạo bản sao của một cột dữ liệu khung giờ trong ngày hiện có (bao gồm cả các khung giờ và giá trị bên trong) để làm cơ sở cho một cột mới cho ngày khác.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng khung giờ nguồn đã tồn tại.
Post-condition:
(Điều kiện đủ)
Một cột khung giờ mới được tạo ra với dữ liệu giống cột nguồn.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Bảng khung giờ".
2. Tại phần chỉnh sửa hoặc tạo mới bảng dữ liệu khung giờ, chọn một ngày và nhấn nút "Sao chép".
3. Hệ thống tự động điền các chi tiết (khung giờ, giá trị) từ cột nguồn.
4. Admin nhấn nút "Xác nhận ".
5. Hệ thống tạo bản ghi bảng khung giờ mới với trạng thái.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
None.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.25. Thêm dữ liệu theo ngày
Use Case ID:
25
Use Case Name:
Thêm dữ liệu theo ngày
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép thêm các thiết lập giá đặc biệt hoặc ngoại lệ theo từng ngày cụ thể, áp dụng thay thế cho bảng dữ liệu khung giờ mặc định.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá".
Post-condition:
(Điều kiện đủ)
Dữ liệu cấu hình đặc biệt cho một ngày cụ thể được lưu.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Dữ liệu theo ngày" -> "Thêm mới".
2. Admin nhập các thông tin bắt buộc: Ngày áp dụng, Loại ngoại lệ (ví dụ: Ngày lễ, Cuộc họp, Giá khẩn cấp).
3. Admin nhập các tham số cấu hình áp dụng cho ngày này (có thể là một bảng khung giờ khác, hoặc một giá trị cố định).
4. Admin nhấn nút "Lưu/Tạo mới".
5. Hệ thống kiểm tra tính duy nhất và tính hợp lệ của Ngày áp dụng.
6. Hệ thống tạo bản ghi cấu hình giá theo ngày.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Thiếu trường thông tin bắt buộc.
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.26. Tải lại dữ liệu khung giờ
Use Case ID:
26
Use Case Name:
Tải lại dữ liệu khung giờ
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
Hệ thống nguồn dữ liệu (Data Source)
Description:
(Mô tả)
Cho phép đồng bộ hoặc tải lại toàn bộ dữ liệu cho bảng khung giờ từ một nguồn bên ngoài, áp dụng cho bảng đã tạo (Xem UC 21).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng khung giờ đã tồn tại và chưa bị khóa.s
Post-condition:
(Điều kiện đủ)
Dữ liệu khung giờ của bảng được đồng bộ/tải lại thành công.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Bảng khung giờ", chọn một bảng.
2. Admin nhấn nút "Tải lại dữ liệu".
3. Hệ thống tiến hành kết nối và thực hiện quá trình đồng bộ dữ liệu, thay thế dữ liệu khung giờ hiện tại.
4. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
None.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.27. Thêm vùng tính giá
Use Case ID:
27
Use Case Name:
Thêm vùng tính giá
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin định nghĩa một khu vực địa lý hoặc khu vực kinh doanh mới để áp dụng cơ chế tính giá, quy tắc hoặc tham số riêng biệt.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá".
Post-condition:
(Điều kiện đủ)
Một vùng tính giá mới được tạo và sẵn sàng để áp dụng bảng giá.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cài đặt giá" -> "Vùng tính giá" -> "Thêm mới".
2. Admin nhập các thông tin bắt buộc: Tên Bảng.
4. Admin nhấn nút “Hoàn thành".
5. Hệ thống kiểm tra tính duy nhất của Mã vùng (BR-P14).
6. Hệ thống tạo bản ghi vùng tính giá mới.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Mã vùng tính giá đã tồn tại (BR-P14).
→ Hệ thống hiển thị lỗi.
2. Thiếu trường thông tin bắt buộc.
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-P14: Mã vùng tính giá phải là duy nhất.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.28. Chỉnh sửa vùng tính giá
Use Case ID:
28
Use Case Name:
Chỉnh sửa vùng tính giá
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin cập nhật thông tin (Tên, Mô tả), ranh giới hoặc quy tắc của vùng tính giá hiện có.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Vùng tính giá đã tồn tại.
Post-condition:
(Điều kiện đủ)
Thông tin và/hoặc ranh giới của vùng tính giá được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Vùng tính giá", chọn một vùng và nhấn nút "Chỉnh sửa".
2. Hệ thống tải và hiển thị thông tin vùng hiện tại.
3. Admin chỉnh sửa trường thông tin cho phép.
4. Admin nhấn nút "Hoàn thành".
5. Hệ thống kiểm tra tính hợp lệ của cập nhật.
6. Hệ thống cập nhật thông tin vùng tính giá.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Cố gắng thay đổi Mã vùng đã tồn tại.
→ Hệ thống hiển thị lỗi/cảnh báo.
2. Lỗi hệ thống khi cập nhật.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.29. Thêm bảng giá
Use Case ID:
29
Use Case Name:
Thêm bảng giá
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin tạo một bảng giá mới với các mức giá, quy tắc, và tham chiếu đến dữ liệu khung giờ/dữ liệu mùa cụ thể.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá".
Post-condition:
(Điều kiện đủ)
Một bảng giá mới được tạo và sẵn sàng để áp dụng cho Vùng/Trạm.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt giá" -> "Quản lý Bảng giá" -> "Thêm mới".
2. Admin nhập các thông tin bắt buộc: Tên bảng giá, Thời gian áp dụng, Vùng tính giá áp dụng.
4. Admin nhập các mức giátheo từng khung giờ chính.
5. Admin nhấn nút "Xác nhận".
6. Hệ thống kiểm tra tính duy nhất của Tên bảng giá (BR-P17).
7. Hệ thống tạo bản ghi bảng giá mới.
8. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Tên bảng giá đã tồn tại (BR-P17).
→ Hệ thống hiển thị lỗi.
2. Thiếu trường thông tin bắt buộc.
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-P17: Tên bảng giá phải là duy nhất.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.30. Chỉnh sửa bảng giá
Use Case ID:
30
Use Case Name:
Chỉnh sửa bảng giá
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin cập nhật các mức giá, điều kiện, quy tắc hoặc tham chiếu dữ liệu trong bảng giá hiện có.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng giá đã tồn tại và chưa bị khóa (Xem UC 31).
Post-condition:
(Điều kiện đủ)
Các thông số, mức giá, quy tắc trong bảng giá được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Quản lý Bảng giá", chọn một bảng và nhấn nút "Chỉnh sửa".
2. Hệ thống tải và hiển thị thông tin bảng giá hiện tại.
3. Admin chỉnh sửa các trường thông tin.
4. Admin nhấn nút "Xác nhận".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-P18, BR-P19).
6. Hệ thống cập nhật thông tin bảng giá.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
None.
Business Rules:
(Nghiệp vụ)
BR-P18: Mọi bảng giá phải tham chiếu đến ít nhất một nguồn dữ liệu giá.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.31. Khóa bảng giá
Use Case ID:
31
Use Case Name:
Khóa bảng giá
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin khóa một bảng giá, ngăn chặn mọi thay đổi đối với các mức giá đã thiết lập để đảm bảo tính ổn định và tuân thủ pháp lý.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng giá đã tồn tại.
Post-condition:
(Điều kiện đủ)
Bảng giá được đánh dấu là trạng thái Locked.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Quản lý Bảng giá", chọn một bảng.
2. Admin nhấn nút "Khóa bảng giá".
3. Hệ thống cập nhật trạng thái của bảng giá thành Locked.
4. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
2. Bảng giá đang được tham chiếu trong các tính toán quan trọng và không thể khóa.
→ Hệ thống hiển thị cảnh báo/lỗi.
3. Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.32. Thêm khung giờ và giá trị mới
Use Case ID:
32
Use Case Name:
Thêm khung giờ và giá trị mới
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bổ sung một khung giờ mới vào cấu hình bảng giá.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình giá". Bảng giá và thêm khung giờ.
Post-condition:
(Điều kiện đủ)
Một khung giờ mới được thêm vào bảng.
Normal Flow:
(Luồng chính)
1. Admin truy cập màn hình chỉnh sửa của Bảng giá/Bảng khung giờ (Xem UC 22, UC 30).
2. Admin chọn chức năng "Thêm khung giờ mới".
3. Admin chọn: Khung giờ, Mùa, và Giá trị/Tham số tương ứng.
4. Admin nhấn nút "Hoàn thành".
5. Hệ thống kiểm tra tính hợp lệ của khung giờ mới.
6. Hệ thống thêm khung giờ/giá trị mới vào cơ sở dữ liệu.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Giá trị/Tham số nhập vào không hợp lệ (BR-P09).
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-P09: Giá trị/Tham số quá lớn hoặc là số âm.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình giá.
### 2.33. Cập nhật bảng nội suy
Use Case ID:
33
Use Case Name:
Cập nhật bảng nội suy
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin điều chỉnh dữ liệu trong bảng nội suy (Interpolation Table) để tính toán các thông số không đo trực tiếp hoặc chuyển đổi giữa các đơn vị/tham số liên quan đến vật lý, thủy văn (ví dụ: chuyển đổi Mực nước - Dung tích hồ).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình bảng nội suy". Bảng nội suy đã tồn tại.
Post-condition:
(Điều kiện đủ)
Dữ liệu trong bảng nội suy được cập nhật và áp dụng vào hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Bảng nội suy".
2. Admin chọn một loại bảng nội suy cần cập nhật.
3. Hệ thống tải và hiển thị dữ liệu bảng nội suy hiện tại.
4. Admin tải lên một tệp dữ liệu mới (ví dụ: Excel/CSV).
5. Admin nhấn nút "Cập nhật".
6. Hệ thống kiểm tra tính hợp lệ của dữ liệu (đảm bảo tính liên tục- BR-IT01).
7. Hệ thống cập nhật dữ liệu bảng nội suy.
8. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
A1: Admin tải dữ liệu từ tệp lên.  → Hệ thống xử lý dữ liệu từ tệp. Nếu dữ liệu không hợp lệ, chuyển sang Exception 2.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu nhập/tải lên vi phạm quy tắc nội suy (BR-IT01).
→ Hệ thống hiển thị lỗi và yêu cầu điều chỉnh.
2. Lỗi đọc/tải tệp dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
3. Bảng nội suy đang được sử dụng trong một tính toán quan trọng và không thể sửa (BR-IT02).
→ Hệ thống hiển thị cảnh báo.
Business Rules:
(Nghiệp vụ)
BR-IT01: Dữ liệu nội suy phải đảm bảo tính hợp lý vật lý (ví dụ: Mực nước tăng thì Dung tích/Lưu lượng phải tăng).
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình bảng nội suy.
### 2.34. Tải bảng nội suy xuống
Use Case ID:
34
Use Case Name:
Tải bảng nội suy xuống
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng hoặc Admin tải về tệp dữ liệu của bảng nội suy hiện tại (ví dụ: dưới dạng Excel/CSV) để kiểm tra, lưu trữ hoặc sử dụng ngoại tuyến.
Precondition:
(Điều kiện cần)
Người dùng có quyền truy cập vào chức năng "Bảng nội suy". Bảng nội suy đã tồn tại.
Post-condition:
(Điều kiện đủ)
Tệp dữ liệu bảng nội suy được tải về máy tính của người dùng.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Bảng nội suy".
2. Người dùng chọn một bảng nội suy cụ thể.
3. Người dùng nhấn nút "Tải xuống".
4. Hệ thống truy xuất dữ liệu từ bảng nội suy.
5. Hệ thống chuyển đổi dữ liệu sang định dạng tệp yêu cầu (ví dụ: Excel).
6. Hệ thống gửi tệp đến trình duyệt của người dùng.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Bảng nội suy không có dữ liệu.
→ Hệ thống hiển thị cảnh báo.
2. Người dùng không có quyền tải xuống bảng này (BR-IT03).
→ Hệ thống chặn và hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-IT03: Chỉ những người dùng có quyền Xem mới được phép tải xuống bảng nội suy.
### 2.35. Cập nhật thông tin thủy điện
Use Case ID:
35
Use Case Name:
Cập nhật thông tin thủy điện
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật các thông số kỹ thuật và quản lý của công trình thủy điện (ví dụ: công suất lắp máy, công suất hữu ích, mức nước chết, mức nước dâng bình thường, v.v...).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Các thông số cấu hình thủy điện được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cài đặt dự án" tại phần "Thông tin thủy điện".
2. Hệ thống tải và hiển thị thông tin cấu hình hiện tại.
3. Admin chỉnh sửa các tham số kỹ thuật và quản lý.
4. Admin nhấn nút "Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu Mã thủy điện, tên thủy điện, khu vực.
6. Hệ thống cập nhật thông tin thủy điện.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu nhập vào vi phạm quy tắc cấu trúc nhập.
→ Hệ thống hiển thị lỗi và yêu cầu nhập lại.
2. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
### 2.36. Cập nhật thông tin hồ chứa
Use Case ID:
36
Use Case Name:
Cập nhật thông tin hồ chứa
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật các thông số vận hành và quản lý của hồ chứa (ví dụ: dung tích hữu ích, mực nước giới hạn trên/dưới, dung tích phòng lũ, v.v...).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Các thông số cấu hình hồ chứa được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Thông tin hồ chứa".
2. Hệ thống tải và hiển thị thông tin cấu hình hiện tại.
3. Admin chỉnh sửa các tham số vận hành và quản lý.
4. Admin nhấn nút "Lưu/Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (ví dụ: dung tích hồ phải đồng bộ với các điểm mực nước liên quan.
6. Hệ thống cập nhật thông tin hồ chứa.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu nhập vào sai cấu trúc.
→ Hệ thống hiển thị lỗi.
2. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
### 2.37. Cập nhật dữ liệu xả lũ
Use Case ID:
37
Use Case Name:
Cập nhật dữ liệu xả lũ
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật thông tin và quy tắc liên quan đến dữ liệu đánh giá cấp độ xả lũ (ví dụ: giá trị ngưỡng, chú thích ngưỡng)(BR-PRJ03).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Dữ liệu/Quy tắc xả lũ của hồ chứa được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" phần "Xả lũ".
2. Hệ thống tải và hiển thị quy tắc xả lũ(7 cấp độ lũ) hiện tại.
3. Admin chỉnh sửa các quy tắc xả lũ(7 cấp độ lũ) (ví dụ: Giá trị ngưỡng, Chú thích ngưỡng).
4. Admin nhấn nút "Cập nhật".
5. Hệ thống cập nhật dữ liệu xả lũ.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu nhập vào không hợp lệ (ví dụ: giá trị âm).
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-PRJ03: Quy tắc xả lũ phải tuân thủ nghiêm ngặt Quy trình vận hành hồ chứa liên hồ chứa do cơ quan có thẩm quyền ban hành.  BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
### 2.38. Cập nhật tuyến năng lượng
Use Case ID:
38
Use Case Name:
Cập nhật tuyến năng lượng
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép điều chỉnh thông tin về các đường truyền/tuyến năng lượng bao gồm kênh dẫn nước.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Thông tin tuyến năng lượng được cập nhật trong hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Tuyến năng lượng".
2. Hệ thống tải và hiển thị danh sách tuyến năng lượng hiện có.
3. Admin chọn một tuyến.
4. Admin nhấn nút "Cập nhật".
5. Hệ thống cập nhật thông tin.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Công suất tối đa nhập vào không tuân thủ quy chuẩn kỹ thuật (BR-PRJ04).  → Hệ thống hiển thị lỗi.  2. Lỗi hệ thống khi lưu trữ dữ liệu.  → Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-PRJ04: Công suất truyền tải tối đa phải là giá trị số dương và tuân thủ giới hạn thiết kế.  BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
### 2.39. Cập nhật thông tin nhà máy
Use Case ID:
39
Use Case Name:
Cập nhật thông tin nhà máy
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật các thông số quản lý, vị trí và kỹ thuật của nhà máy điện (ví dụ: tên nhà máy, vị trí, ngày thành lập, công suất lắp đặt, hệ số hiệu chỉnh, v.v...).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Thông tin nhà máy được cập nhật trong hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Thông tin nhà máy".
2. Hệ thống tải và hiển thị thông tin cấu hình hiện tại.
3. Admin chỉnh sửa các thông số quản lý và kỹ thuật.
4. Admin nhấn nút "Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu.
6. Hệ thống cập nhật thông tin nhà máy.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Thiếu trường thông tin bắt buộc.
→ Hệ thống hiển thị thông báo lỗi.
2. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
### 2.40. Cập nhật thông tin vị trí đo
Use Case ID:
40
Use Case Name:
Cập nhật thông tin vị trí đo
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép điều chỉnh thông tin về các điểm đo lường (Measurement Points) trong hệ thống (ví dụ: tên điểm đo, tọa độ chính xác, tham chiếu đến cảm biến, độ cao, v.v...).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án". Vị trí đo đã tồn tại.
Post-condition:
(Điều kiện đủ)
Thông tin vị trí đo được cập nhật trong hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Vị trí đo".
2. Hệ thống tải và hiển thị danh sách vị trí đo hiện tại.
3. Admin chọn một vị trí và chỉnh sửa các thông số: Tên điểm đo, Tọa độ, Độ cao.
4. Admin nhấn nút "Lưu/Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (ví dụ: tọa độ hợp lệ).
6. Hệ thống cập nhật thông tin.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Tọa độ nhập vào không hợp lệ.
→ Hệ thống hiển thị thông báo lỗi.
2. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
BR-PRJ05: Mọi Vị trí đo phải được liên kết đến một Trạm (UC 10) hoặc một Cảm biến (UC 14) cụ thể.
### 2.41. Cập nhật thông tin tổ máy
Use Case ID:
41
Use Case Name:
Cập nhật thông tin tổ máy
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật các thông số kỹ thuật và trạng thái của từng tổ máy phát điện (ví dụ: công suất định mức, hiệu suất, trạng thái vận hành).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Thông số và trạng thái của tổ máy được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Thông tin tổ máy".
2. Hệ thống tải và hiển thị danh sách tổ máy hiện tại.
3. Admin chọn một tổ máy và chỉnh sửa các thông số: Tên tổ máy, Loại tổ máy, Kiểu cửa, Bảng nội suy, Bảng nội suy phụ,Trạng thái(đang hoạt động, bảo trì),Giá trị mặc định.
4. Admin nhấn nút "Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-PRJ06).
6. Hệ thống cập nhật thông tin.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
### 2.42. Cập nhật thông tin cửa xả
Use Case ID:
42
Use Case Name:
Cập nhật thông tin cửa xả
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật thông số và quy tắc vận hành của các cửa xả bao gồm loại cửa, phương pháp xả, bảng nội suy, cao trình ngưỡng tràn, độ mở cực đại, ngưỡng tối đa, ngưỡng tối thiểu, giá trị mặc định trạng thái(đang hoạt động, bảo trì).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Thông số vận hành của cửa xả được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Thông tin cửa xả".
2. Hệ thống tải và hiển thị danh sách cửa xả hiện tại.
3. Admin chọn một cửa xả và chỉnh sửa các thông số: gồm loại cửa, phương pháp xả, bảng nội suy, cao trình ngưỡng tràn, độ mở cực đại, ngưỡng tối đa, ngưỡng tối thiểu, giá trị mặc định trạng thái(đang hoạt động, bảo trì).
4. Admin nhấn nút "Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-PRJ07).
6. Hệ thống cập nhật thông tin.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
### 2.43. Cập nhật thông tin lưu vực
Use Case ID:
43
Use Case Name:
Cập nhật thông tin lưu vực
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật các thông số địa lý và thủy văn của lưu vực cấp nước cho hồ chứa/nhà máy (ví dụ: diện tích lưu vực, hệ số dòng chảy, v.v...).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Thông số lưu vực được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Thông tin lưu vực".
2. Hệ thống tải và hiển thị thông tin cấu hình hiện tại.
3. Admin chỉnh sửa các thông số: Diện tích lưu vực, Hệ số dòng chảy.
4. Admin nhấn nút "Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (ví dụ: diện tích không được âm).
6. Hệ thống cập nhật thông tin.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu nhập vào không hợp lệ.
→ Hệ thống hiển thị thông báo lỗi.
2. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình dự án.
### 2.44. Cập nhật cài đặt hiển thị
Use Case ID:
44
Use Case Name:
Cập nhật cài đặt hiển thị
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép tùy chỉnh các tham số hiển thị dữ liệu trên giao diện người dùng, áp dụng cho toàn bộ dự án (Admin) hoặc cho tài khoản cá nhân (User).
Precondition:
(Điều kiện cần)
Người dùng/Admin đã đăng nhập.
Post-condition:
(Điều kiện đủ)
Các tham số hiển thị giao diện được cập nhật.
Normal Flow:
(Luồng chính)
1. Người dùng/Admin truy cập chức năng "Cài đặt" -> "Hiển thị".
2. Hệ thống tải và hiển thị các tùy chọn cấu hình hiện tại (ví dụ: Tham số cơ sở dữ liệu, Đơn vị mặc định, Bảng màu, Kích thước font chữ).
3. Người dùng/Admin chỉnh sửa các tùy chọn mong muốn.
4. Người dùng/Admin nhấn nút "Cập nhật".
5. Hệ thống lưu cấu hình mới (Cấu hình Admin ảnh hưởng toàn hệ thống, Cấu hình User chỉ ảnh hưởng tài khoản cá nhân - BR-PRJ08).
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-PRJ08: Cài đặt hiển thị của Admin được áp dụng làm mặc định cho toàn bộ hệ thống. Cài đặt của User được ưu tiên áp dụng cho tài khoản đó nếu có tùy chỉnh.
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình hiển thị mặc định của dự án.
### 2.45. Ẩn/hiện thông số dự báo
Use Case ID:
45
Use Case Name:
Ẩn/hiện thông số dự báo
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bật hoặc tắt hiển thị các thông số dự báo (Forecast Parameters) trên giao diện (ví dụ: Dự báo lưu lượng, Dự báo mực nước) để kiểm soát dữ liệu nào được công bố cho người dùng.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Trạng thái hiển thị của các thông số dự báo được thay đổi.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Cài đặt hiển thị".
2. Hệ thống hiển thị danh sách các thông số dự báo có thể tùy chỉnh.
3. Admin chọn (check-hiện) hoặc bỏ chọn (uncheck-ẩn) thông số dự báo.
4. Admin nhấn nút "Cập nhật".
5. Hệ thống cập nhật cấu hình hiển thị.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình hiển thị dự báo cho toàn bộ hệ thống.
### 2.46. Ẩn/hiện mưa quan trắc
Use Case ID:
46
Use Case Name:
Ẩn/hiện mưa quan trắc
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bật hoặc tắt hiển thị dữ liệu mưa quan trắc (đã được thu thập) trên giao diện bản đồ, báo cáo, hoặc Dashboard.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Trạng thái hiển thị của dữ liệu mưa quan trắc được thay đổi.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Cài đặt hiển thị".
2. Admin chọn (check) hoặc bỏ chọn (uncheck) tùy chọn Hiển thị Mưa quan trắc.
3. Admin nhấn nút "Cập nhật".
4. Hệ thống cập nhật cấu hình hiển thị.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình hiển thị dữ liệu mưa quan trắc cho toàn bộ hệ thống.
### 2.47. Ẩn/hiện mưa phân tích
Use Case ID:
47
Use Case Name:
Ẩn/hiện mưa phân tích
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bật hoặc tắt hiển thị dữ liệu mưa đã được phân tích/nội suy (Analyzed Rainfall) trên giao diện (thường là dữ liệu mưa lưới hoặc mưa đã được hiệu chỉnh).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Trạng thái hiển thị của dữ liệu mưa phân tích được thay đổi.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Cài đặt hiển thị".
2. Admin chọn (check) hoặc bỏ chọn (uncheck) tùy chọn Hiển thị Mưa phân tích.
3. Admin nhấn nút "Cập nhật".
4. Hệ thống cập nhật cấu hình hiển thị.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình hiển thị.
### 2.48. Ẩn/hiện mưa dự báo
Use Case ID:
48
Use Case Name:
Ẩn/hiện mưa dự báo
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bật hoặc tắt hiển thị dữ liệu mưa dự báo (Forecast Rainfall) trên giao diện.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Trạng thái hiển thị của dữ liệu mưa dự báo được thay đổi.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Cài đặt hiển thị".
2. Admin chọn (check) hoặc bỏ chọn (uncheck) tùy chọn Hiển thị Mưa dự báo.
3. Admin nhấn nút "Lưu/Cập nhật".
4. Hệ thống cập nhật cấu hình hiển thị.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình hiển thị.
### 2.49. Ẩn/hiện lưu lượng dự báo
Use Case ID:
49
Use Case Name:
Ẩn/hiện lưu lượng dự báo
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bật hoặc tắt hiển thị dữ liệu lưu lượng dự báo (Forecast Flow) trên giao diện.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình dự án".
Post-condition:
(Điều kiện đủ)
Trạng thái hiển thị của dữ liệu lưu lượng dự báo được thay đổi.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cài đặt dự án" -> "Cài đặt hiển thị".
2. Admin chọn (check) hoặc bỏ chọn (uncheck) tùy chọn Hiển thị Lưu lượng dự báo.
3. Admin nhấn nút "Cập nhật".
4. Hệ thống cập nhật cấu hình hiển thị.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi cập nhật trạng thái.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A02: Chỉ Admin mới có quyền quản lý cấu hình hiển thị.
### 2.50. Thêm mới cảnh báo
Use Case ID:
50
Use Case Name:
Thêm mới cảnh báo
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin tạo một quy tắc cảnh báo mới dựa trên các ngưỡng và điều kiện (ví dụ: nhiệt độ vượt quá X độ, lưu lượng giảm dưới Y m³/s).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình cảnh báo". Các thông số đo lường đã được định nghĩa trong hệ thống.
Post-condition:
(Điều kiện đủ)
Quy tắc cảnh báo mới được tạo, lưu trữ và kích hoạt trong hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cấu hình cảnh báo".
2. Admin chọn "Thêm mới cảnh báo".
3. Hệ thống hiển thị biểu mẫu nhập liệu.
4. Admin nhập các thông số: Tên cảnh báo, Mô tả, Thông số đo lường (Sensor/Tag), Ngưỡng (min/max), Điều kiện kích hoạt (>, <, =), Thời gian duy trì cảnh báo, và Phương thức thông báo (Email, SMS...).
5. Admin nhấn nút "Lưu".
6. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-CFG01).
7. Hệ thống lưu trữ quy tắc cảnh báo mới.
8. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu nhập vào không hợp lệ (ví dụ: ngưỡng không phải là số - BR-CFG01).
→ Hệ thống hiển thị lỗi và yêu cầu nhập lại.
Business Rules:
(Nghiệp vụ)
BR-CFG01: Tất cả các trường bắt buộc phải được điền đầy đủ và đúng định dạng (ví dụ: ngưỡng phải là số dương).
BR-CFG02: Chỉ Admin mới có quyền thêm mới, chỉnh sửa, xóa cảnh báo.
### 2.51. Chỉnh sửa cảnh báo
Use Case ID:
51
Use Case Name:
Chỉnh sửa cảnh báo
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin điều chỉnh ngưỡng, điều kiện hoặc các thông tin khác của một cảnh báo hiện có.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình cảnh báo". Cảnh báo cần chỉnh sửa đã tồn tại trong hệ thống.
Post-condition:
(Điều kiện đủ)
Thông tin của cảnh báo được cập nhật trong hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cấu hình cảnh báo".
2. Admin tìm kiếm và chọn cảnh báo cần chỉnh sửa.
3. Hệ thống tải thông tin chi tiết của cảnh báo.
4. Admin thay đổi các thông số cần thiết (ví dụ: điều chỉnh ngưỡng, thêm người nhận thông báo).
5. Admin nhấn nút "Cập nhật".
6. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-CFG01).
7. Hệ thống cập nhật thông tin cảnh báo.
8. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi cập nhật.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-CFG01: Tất cả các trường bắt buộc phải được điền đầy đủ và đúng định dạng.
BR-CFG02: Chỉ Admin mới có quyền thêm mới, chỉnh sửa, xóa cảnh báo.
### 2.52. Xóa cảnh báo
Use Case ID:
52
Use Case Name:
Xóa cảnh báo
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin loại bỏ một quy tắc cảnh báo không còn sử dụng khỏi hệ thống.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cấu hình cảnh báo". Cảnh báo cần xóa đã tồn tại.
Post-condition:
(Điều kiện đủ)
Quy tắc cảnh báo bị xóa vĩnh viễn khỏi hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cấu hình cảnh báo".
2. Admin tìm kiếm và chọn cảnh báo cần xóa.
3. Admin nhấn nút "Xóa".
4. Hệ thống hiển thị hộp thoại xác nhận (ví dụ: "Bạn có chắc chắn muốn xóa cảnh báo này không?").
5. Admin xác nhận xóa.
6. Hệ thống loại bỏ quy tắc cảnh báo.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống trong quá trình xóa.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-CFG02: Chỉ Admin mới có quyền thêm mới, chỉnh sửa, xóa cảnh báo.
### 2.53. Cài đặt bảng nội suy cửa van
Use Case ID:
53
Use Case Name:
Cài đặt bảng nội suy cửa van
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép thiết lập hoặc cập nhật bảng nội suy liên quan đến việc vận hành cửa van (ví dụ: Mối quan hệ giữa độ mở cửa van và lưu lượng xả).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Cài đặt khác".
Post-condition:
(Điều kiện đủ)
Bảng nội suy cửa van được cập nhật và áp dụng cho các tính toán vận hành.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Cấu hình" -> "Cài đặt khác".
2. Admin chọn "Cài đặt bảng nội suy cửa van".
3. Hệ thống hiển thị bảng dữ liệu nội suy hiện tại.
4. Admin thực hiện nhập liệu bằng cách tải tệp dữ liệu mới lên (ví dụ: Excel/CSV) để cập nhật (BR-CFG03).
5. Hệ thống kiểm tra cấu trúc/dữ liệu tệp và tính hợp lệ của dữ liệu.
6. Hệ thống lưu trữ bảng nội suy mới.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
A1: Tải bảng nội suy hiện tại xuống để chỉnh sửa.
Exceptions:
(Trường hợp
ngoại lệ)
1. Tệp dữ liệu tải lên sai cấu trúc hoặc định dạng (BR-CFG03).
→ Hệ thống hiển thị lỗi và yêu cầu tải lại.
2. Lỗi hệ thống khi lưu trữ.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-CFG03: Dữ liệu bảng nội suy phải tuân thủ cấu trúc định sẵn (ví dụ: cột độ mở, cột lưu lượng) và là giá trị số dương.
### 2.54. Tải dữ liệu báo cáo pháp lý theo mẫu
Use Case ID:
54
Use Case Name:
Tải dữ liệu báo cáo pháp lý theo mẫu
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép tải dữ liệu về một tệp mẫu báo cáo pháp lý đã được định dạng sẵn để người dùng theo dõi số liệu và sử dụng cho việc báo cáo lên cơ quan chức năng.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền "Truy cập báo cáo pháp lý" (BR-REP01). Mẫu báo cáo đã được định nghĩa trong hệ thống.
Post-condition:
(Điều kiện đủ)
Tệp báo cáo pháp lý theo mẫu (đã có dữ liệu) được tải về máy tính.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Báo cáo pháp lý".
2. Người dùng chọn loại mẫu báo cáo cần tải (ví dụ: Báo cáo Mực nước, Báo cáo Vận hành Thủy điện).
3. Người dùng chọn Khoảng thời gian (Ngày, Tháng, Quý, Năm) cần báo cáo.
4. Người dùng nhấn nút "Tải dữ liệu theo mẫu".
5. Hệ thống truy xuất dữ liệu liên quan trong khoảng thời gian đã chọn (BR-REP02).
6. Hệ thống chèn dữ liệu vào tệp mẫu đã định dạng (ví dụ: Excel, PDF) và gửi tệp đến trình duyệt của người dùng.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu trong khoảng thời gian đã chọn không đầy đủ (ví dụ: mất dữ liệu cảm biến).
→ Hệ thống hiển thị cảnh báo và tiếp tục xuất báo cáo với dữ liệu thiếu.
2. Người dùng không có quyền truy cập báo cáo này (BR-REP01).
→ Hệ thống chặn và hiển thị lỗi.
3. Lỗi tạo/xuất tệp báo cáo.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-REP01: Chỉ những người dùng có Role được phân quyền (ví dụ: Admin, Quản lý) mới có thể truy cập báo cáo pháp lý.
BR-REP02: Dữ liệu báo cáo pháp lý phải tuân thủ các chuẩn báo cáo.
### 2.55. Tải dữ liệu báo cáo pháp lý về máy tính
Use Case ID:
55
Use Case Name:
Tải dữ liệu báo cáo pháp lý về máy tính
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép xuất dữ liệu báo cáo pháp lý đã tổng hợp về máy tính cá nhân dưới dạng tệp dữ liệu thô (ví dụ: CSV) hoặc tệp tổng hợp không theo mẫu định sẵn.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền "Truy cập báo cáo pháp lý".
Post-condition:
(Điều kiện đủ)
Tệp dữ liệu báo cáo pháp lý (dạng thô hoặc tổng hợp) được tải về.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Báo cáo pháp lý".
2. Người dùng chọn Khoảng thời gian và Loại dữ liệu (ví dụ: Dữ liệu thô Mực nước).
3. Người dùng chọn định dạng xuất tệp (ví dụ: CSV, Excel).
4. Người dùng nhấn nút "Tải dữ liệu về máy tính".
5. Hệ thống truy xuất dữ liệu thô từ cơ sở dữ liệu (BR-REP02).
6. Hệ thống tạo tệp dữ liệu đã chọn và gửi đến trình duyệt.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Khoảng thời gian yêu cầu quá lớn, vượt quá giới hạn xuất dữ liệu (BR-REP03).
→ Hệ thống hiển thị cảnh báo và yêu cầu giới hạn lại khoảng thời gian.
2. Người dùng không có quyền (BR-REP01).
→ Hệ thống chặn.
3. Lỗi tạo/xuất tệp dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-REP01: Chỉ những người dùng có Role được phân quyền mới có thể truy cập báo cáo pháp lý.
BR-REP02: Dữ liệu báo cáo pháp lý phải tuân thủ các chuẩn báo cáo.
### 2.56. Thiết lập kế hoạch sản lượng doanh thu năm
Use Case ID:
56
Use Case Name:
Thiết lập kế hoạch sản lượng doanh thu năm
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng nhập và lưu trữ các chỉ tiêu kế hoạch sản lượng (ví dụ: MWh) và doanh thu (ví dụ: VNĐ) cho cả năm, thường được nhập theo từng tháng/quý.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Thiết lập kế hoạch sản lượng" (BR-REP04).
Post-condition:
(Điều kiện đủ)
Kế hoạch sản lượng và doanh thu năm được lưu trữ trong hệ thống.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Báo cáo Sản lượng & Doanh thu" -> "Thiết lập kế hoạch".
2. Người dùng chọn Năm cần thiết lập kế hoạch.
3. Hệ thống hiển thị biểu mẫu nhập liệu theo tháng cho Sản lượng và Doanh thu.
4. Người dùng nhập các chỉ tiêu kế hoạch vào từng trường (BR-REP05).
5. Người dùng nhấn nút "Lưu kế hoạch".
6. Hệ thống kiểm tra tính hợp lệ của dữ liệu (ví dụ: phải là số dương).
7. Hệ thống lưu trữ kế hoạch.
8. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
A1: Người dùng tải dữ liệu kế hoạch từ tệp lên.
→ Hệ thống xử lý dữ liệu từ tệp. Nếu dữ liệu không hợp lệ, chuyển sang Exception 2.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu nhập vào không hợp lệ (ví dụ: giá trị âm, thiếu trường - BR-REP05).
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-REP04: Chỉ Admin và các Role được cấp quyền (ví dụ: Quản lý) mới có thể thiết lập kế hoạch sản lượng/doanh thu.
BR-REP05: Sản lượng và Doanh thu kế hoạch phải là các giá trị số dương.
### 2.57. Xuất báo cáo sản lượng doanh thu
Use Case ID:
57
Use Case Name:
Xuất báo cáo sản lượng doanh thu
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng tạo và tải về báo cáo tổng hợp về sản lượng và doanh thu (bao gồm so sánh giữa Kế hoạch và Thực tế).
Precondition:
(Điều kiện cần)
Người dùng có quyền "Xem báo cáo sản lượng". Dữ liệu kế hoạch và thực tế (UC 56, 58, 59) đã được nhập.
Post-condition:
(Điều kiện đủ)
Tệp báo cáo tổng hợp sản lượng/doanh thu được tải về.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Báo cáo Sản lượng & Doanh thu".
2. Người dùng chọn Khoảng thời gian (Tháng, Quý, Năm) cần báo cáo.
3. Người dùng chọn định dạng xuất tệp (ví dụ: Excel, PDF).
4. Người dùng nhấn nút "Xuất báo cáo".
5. Hệ thống tổng hợp dữ liệu Kế hoạch, Thực tế và tính toán các chỉ số so sánh (Phần trăm hoàn thành, Sai số).
6. Hệ thống tạo tệp báo cáo với cấu trúc tổng hợp (BR-REP07) và gửi đến trình duyệt.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Không có dữ liệu Thực tế trong khoảng thời gian yêu cầu.
→ Hệ thống hiển thị cảnh báo và xuất báo cáo chỉ với dữ liệu Kế hoạch.
2. Lỗi hệ thống khi tổng hợp/xuất báo cáo.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-REP07: Báo cáo phải bao gồm các chỉ số Kế hoạch, Thực tế, và Chênh lệch/Phần trăm hoàn thành cho cả Sản lượng và Doanh thu.
### 2.58. Cập nhật sản lượng thực tế
Use Case ID:
58
Use Case Name:
Cập nhật sản lượng thực tế
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép nhập hoặc cập nhật dữ liệu sản lượng thực tế đã đạt được (ví dụ: tổng sản lượng điện hàng ngày/tháng) từ nguồn đo lường.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Cập nhật sản lượng thực tế" (BR-REP08).
Post-condition:
(Điều kiện đủ)
Dữ liệu sản lượng thực tế được ghi nhận vào hệ thống.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Báo cáo Sản lượng & Doanh thu".
2. Người dùng chọn Khoảng thời gian (Ngày/Tháng) cần cập nhật.
3. Người dùng nhập Giá trị Sản lượng thực tế (ví dụ: MWh).
4. Hệ thốngtự động kiểm tra tính hợp lệ của dữ và tự động lưu giá trị được nhập vào.
5. Hệ thống lưu trữ dữ liệu sản lượng thực tế (BR-REP09).
Alternative Flows:
(Luồng phụ)
A1: Sản lượng được nhập tự động từ Hệ thống SCADA/Đo đếm.
→ Hệ thống tự động thực hiện Bước 3, 4, 5.(chưa thực hiện được).
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-REP08: Chỉ người dùng được phân quyền mới có thể nhập dữ liệu thực tế.
### 2.59. Cập nhật doanh thu thực tế
Use Case ID:
59
Use Case Name:
Cập nhật doanh thu thực tế
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép nhập hoặc cập nhật dữ liệu doanh thu thực tế đã đạt được (ví dụ: tổng tiền thu được từ bán điện hàng tháng).
Precondition:
(Điều kiện cần)
Người dùng có quyền "Cập nhật doanh thu thực tế" (BR-REP08).
Post-condition:
(Điều kiện đủ)
Dữ liệu doanh thu thực tế được ghi nhận vào hệ thống.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Báo cáo Sản lượng & Doanh thu".
2. Người dùng chọn Khoảng thời gian (Tháng) cần cập nhật.
3. Người dùng nhập Giá trị Doanh thu thực tế (ví dụ: VNĐ).
4. Hệ thống kiểm tra tính hợp lệ của dữ liệu và tự động lưu.
5. Hệ thống lưu trữ dữ liệu doanh thu thực tế (BR-REP11).
Alternative Flows:
(Luồng phụ)
A1: Doanh thu được nhập tự động từ Hệ thống Kế toán.  → Hệ thống tự động thực hiện Bước 3, 4, 5.
Exceptions:
(Trường hợp
ngoại lệ)
3. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-REP08: Chỉ người dùng được phân quyền mới có thể nhập dữ liệu thực tế.
BR-REP10: Dữ liệu thực tế cho các kỳ báo cáo đã chốt không được phép cập nhật.
### 2.60. Lấy dữ liệu bảng dữ liệu vận hành
Use Case ID:
60
Use Case Name:
Lấy dữ liệu bảng dữ liệu vận hành
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép truy xuất và hiển thị dữ liệu vận hành chi tiết (Mực nước, Lưu lượng, Sản lượng, trạng thái tổ máy...) trong dạng bảng, phục vụ cho việc kiểm tra và đối chiếu số liệu.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền "Xem dữ liệu vận hành" (BR-REP12).
Post-condition:
(Điều kiện đủ)
Dữ liệu vận hành được hiển thị dưới dạng bảng trên giao diện.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Bảng dữ liệu".
2. Hệ thống hiển thị giao diện tùy chọn truy vấn.
3. Người dùng chọn Khoảng thời gian (Ngày, Giờ, Từ - Đến).
5. Người dùng nhấn nút "Xem dữ liệu" hoặc "Tải dữ liệu".
6. Hệ thống truy xuất dữ liệu từ CSDL theo các tiêu chí đã chọn.
7. Hệ thống hiển thị dữ liệu dưới dạng bảng có thể sắp xếp, lọc.
Alternative Flows:
(Luồng phụ)
A1: Người dùng chọn tùy chọn Tải dữ liệu (Export).
→ Hệ thống tạo tệp dữ liệu (Excel) và tự động tải về.
Exceptions:
(Trường hợp
ngoại lệ)
1. Khoảng thời gian truy vấn vượt quá giới hạn cho.
→ Hệ thống hiển thị lỗi và yêu cầu giới hạn lại.
2. Lỗi hệ thống khi truy xuất dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-REP12: Quyền truy cập vào dữ liệu vận hành phải được phân quyền chi tiết đến từng trạm đo.
### 2.61. Lấy dữ liệu sai số dự báo
Use Case ID:
61
Use Case Name:
Lấy dữ liệu sai số dự báo
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép truy xuất và hiển thị các số liệu về sai số (Error) giữa giá trị dự báo và giá trị thực tế đã quan trắc được, giúp đánh giá độ chính xác của mô hình dự báo.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Xem báo cáo sai số". Dữ liệu Dự báo và Thực đo đã tồn tại cho cùng một khoảng thời gian.
Post-condition:
(Điều kiện đủ)
Bảng dữ liệu sai số dự báo (bao gồm cả Thực tế, Dự báo, Sai số).
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Bảng dữ liệu” ->“Sai số dự báo".
2. Người dùng chọn Khoảng thời gian (Ngày, Tháng) cần phân tích.
3. Hệ thống tự động tổng hợp dữ liệu Dự báo và Thực tế tương ứng, và tính toán Sai số.
4. Hệ thống hiển thị kết quả dưới dạng bảng.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Không có dữ liệu Dự báo hoặc Thực tế trong khoảng thời gian (BR-REP16).
→ Hệ thống hiển thị cảnh báo và không tính toán sai số.
2. Lỗi hệ thống khi tính toán sai số.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
None.
### 2.62. Dữ liệu mưa trung bình thực đo
Use Case ID:
62
Use Case Name:
Dữ liệu mưa trung bình thực đo
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép hiển thị giá trị mưa trung bình được đo lường thực tế trên Dashboard (ví dụ: mưa trung bình lưu vực trong 24 giờ qua), cung cấp cái nhìn tổng quan về tình hình thủy văn.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập. Dữ liệu mưa quan trắc đã được thu thập.
Post-condition:
(Điều kiện đủ)
Giá trị mưa trung bình thực đo được hiển thị trên Dashboard.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập màn hình Dashboard.
2. Hệ thống xác định Khoảng thời gian tính toán mặc định (ví dụ: 24 giờ gần nhất).
3. Hệ thống truy xuất dữ liệu mưa từ các trạm quan trắc.
4. Hệ thống tính toán Mưa trung bình thực đo trên Lưu vực theo phương pháp được cấu hình.
5. Hệ thống hiển thị giá trị đã tính toán lênbiểu đồ trên Dashboard.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Thiếu dữ liệu mưa từ một số trạm quan trọng.
→ Hệ thống hiển thị cảnh báo về độ tin cậy của giá trị mưa trung bình (BR-DB02).
2. Lỗi hệ thống khi tính toán.
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
None.
### 2.63. Dữ liệu trung bình lưới mưa
Use Case ID:
63
Use Case Name:
Dữ liệu trung bình lưới mưa
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép hiển thị giá trị mưa trung bình tính toán theo phương pháp lưới trên Dashboard, thường dùng cho dữ liệu mưa phân tích hoặc mưa dự báo.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập. Dữ liệu mưa lưới đã được tính toán hoặc nhận được từ hệ thống ngoại vi.
Post-condition:
(Điều kiện đủ)
Giá trị mưa trung bình lưới mưa được hiển thị trên Dashboard.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập màn hình Dashboard.
2. Hệ thống xác định Khoảng thời gian tính toán mặc định.
3. Hệ thống truy xuất dữ liệu mưa lưới cho Lưu vực.
4. Hệ thống tính toán Mưa trung bình từ dữ liệu lưới trên khu vực Lưu vực.
5. Hệ thống hiển thị giá trị đã tính toán lên biểu đồ trên Dashboard.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu mưa lưới không tồn tại trong khoảng thời gian yêu cầu.
→ Hệ thống hiển thị giá trị N/A hoặc 0.
2. Lỗi hệ thống khi tính toán.
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-DB03: Phương pháp tính Mưa trung bình lưới phải được cấu hình cố định (ví dụ: <tự thêm nghiệp vụ: Tính trung bình có trọng số theo ô lưới>).
BR-DB04: Dữ liệu mưa lưới phải được cung cấp bởi hệ thống Mô hình Dự báo.
### 2.64. Thay đổi thời gian quan trắc dữ liệu
Use Case ID:
64
Use Case Name:
Thay đổi thời gian quan trắc dữ liệu
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng tùy chỉnh khoảng thời gian để xem dữ liệu quan trắc (Thực đo) trên Dashboard (ví dụ: thay đổi từ 24 giờ sang 7 ngày hoặc chọn một khoảng thời gian tùy chỉnh).
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập.
Post-condition:
(Điều kiện đủ)
Dữ liệu Dashboard được cập nhật theo khoảng thời gian mới.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Dashboard.
2. Người dùng chọn chức năng "Tùy chỉnh thời gian" (Time Picker).
3. Người dùng chọn một khoảng thời gian mới (ví dụ: 7 Ngày, 30 Ngày) hoặc nhập ngày bắt đầu và ngày kết thúc.
4. Hệ thống xác thực khoảng thời gian (BR-DB05).
5. Hệ thống truy xuất và tính toán lại tất cả các dữ liệu Thực đo (Mưa, Mực nước, v.v...) trên Dashboard theo khoảng thời gian mới.
6. Hệ thống làm mới biểu đồ.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Khoảng thời gian yêu cầu vượt quá giới hạn tối đa (BR-DB05).
→ Hệ thống hiển thị lỗi và yêu cầu giới hạn lại.
2. Lỗi hệ thống khi truy xuất/tính toán lại dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DB05: Khoảng thời gian tối đa được phép tùy chỉnh trên Dashboard để đảm bảo tốc độ tải trang.
BR-DB06: Việc thay đổi thời gian quan trắc không được ảnh hưởng đến các dữ liệu dự báo.
### 2.65. Thay đổi khoảng thời gian dự báo
Use Case ID:
65
Use Case Name:
Thay đổi khoảng thời gian dự báo
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng tùy chỉnh khoảng thời gian cho các dữ liệu dự báo được hiển thị trên Dashboard (ví dụ: xem dự báo 24 giờ, 72 giờ hoặc 7 ngày tới).
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập. Dữ liệu dự báo đã được tính toán.
Post-condition:
(Điều kiện đủ)
Dữ liệu dự báo trên Dashboard được cập nhật theo khoảng thời gian mới.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Dashboard.
2. Người dùng chọn chức năng "Tùy chỉnh khoảng dự báo".
3. Người dùng chọn một khoảng thời gian dự báo mới (ví dụ: 3h, 6h, 12h,…).
4. Hệ thống truy xuất và hiển thị dữ liệu Dự báo tương ứng theo khoảng thời gian mới (ví dụ: Biểu đồ dự báo Lưu lượng).
5. Hệ thống làm mới biểu đồ.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi truy xuất/hiển thị dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DB06: Việc thay đổi khoảng thời gian dự báo không được ảnh hưởng đến các dữ liệu quan trắc.
### 2.66. Tính bù
Use Case ID:
66
Use Case Name:
Tính bù
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép thực hiện chức năng tính toán bù trừ dữ liệu (ví dụ: bù thiếu/sai số) cho một khoảng thời gian nhất định, dựa trên dữ liệu từ các trạm lân cận hoặc các mô hình nội suy.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Tính bù dữ liệu" (BR-DB08). Dữ liệu gốc đang bị thiếu/lỗi trong một khoảng thời gian cần bù.
Post-condition:
(Điều kiện đủ)
Dữ liệu đã được tính bù và được sử dụng.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Tính bù dữ liệu" tại Bảng dữ liệu ở Dashboard.
3. Người dùng chọn Khoảng thời gian (Từ - Đến) dữ liệu bị thiếu/lỗi.
4. Hệ thống thực hiện tính toán bù dữ liệu.
5. Hệ thống tự động cập nhật biểu đồ trên trang dashboard.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Khoảng thời gian yêu cầu bù quá lớn, vượt quá giới hạn.
→ Hệ thống hiển thị lỗi.
2. Dữ liệu đầu vào cho việc tính bù cũng bị thiếu/lỗi.
→ Hệ thống hiển thị cảnh báo và không thể thực hiện bù.
3. Người dùng không có quyền.
→ Hệ thống chặn.
Business Rules:
(Nghiệp vụ)
BR-DB10: Giới hạn thời gian tối đa được phép tính bù là 7 ngày.
### 2.67. Đánh giá khuyến nghị (Phù hợp – Không phù hợp)
Use Case ID:
67
Use Case Name:
Đánh giá khuyến nghị (Phù hợp – Không phù hợp)
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng đưa ra nhận xét hoặc đánh giá về độ tin cậy/mức độ phù hợp của các khuyến nghị vận hành (ví dụ: đề xuất xả lũ, đề xuất phát điện) được tạo ra bởi hệ thống.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền "Đánh giá khuyến nghị”. Một Khuyến nghị vận hành đã được hệ thống tạo ra và hiển thị.
Post-condition:
(Điều kiện đủ)
Đánh giá của người dùng được ghi lại, sử dụng để cải tiến mô hình hoặc báo cáo.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Dashboard hoặc màn hình Khuyến nghị.
2. Người dùng xem một khuyến nghị cụ thể.
3. Người dùng chọn tùy chọn "Phù hợp" hoặc "Không phù hợp".
4. Hệ thống lưu trữ đánh giá cùng với ID khuyến nghị, ID người dùng và thời gian đánh giá.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi lưu trữ.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DB13: Khuyến nghị để đánh giá chất lượng Mô hình.
### 2.68. Truy cập nhanh trang truyền dữ liệu
Use Case ID:
68
Use Case Name:
Truy cập nhanh trang truyền dữ liệu
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép điều hướng trực tiếp đến giao diện quản lý truyền dữ liệu từ Dashboard, tiết kiệm thời gian tìm kiếm.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền truy cập Truyền dữ liệu (UC 71).
Post-condition:
(Điều kiện đủ)
Người dùng được chuyển đến màn hình Quản lý Truyền dữ liệu.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Dashboard.
2. Người dùng nhấn vào liên kết hoặc nút "Truyền dữ liệu" (ví dụ: trên một widget hiển thị trạng thái truyền dữ liệu).
3. Hệ thống xác thực quyền truy cập của người dùng.
4. Hệ thống chuyển hướng trình duyệt đến địa chỉ URL của chức năng Quản lý Truyền dữ liệu.
5. Hệ thống hiển thị thông báo thành công (tùy chọn).
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Người dùng không có quyền truy cập trang Truyền dữ liệu.
→ Hệ thống chặn và hiển thị lỗi "Bạn không có quyền truy cập trang này".
2. Lỗi chuyển hướng trang.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A01: Quyền truy cập phải tuân thủ phân quyền của người dùng.
### 2.69. Truy cập nhanh kinh bản khuyến nghị
Use Case ID:
69
Use Case Name:
Truy cập nhanh kịch bản khuyến nghị
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép điều hướng trực tiếp đến giao diện xem/chỉnh sửa các kịch bản khuyến nghị vận hành từ Dashboard.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền truy cập Kịch bản khuyến nghị (UC 96).
Post-condition:
(Điều kiện đủ)
Người dùng được chuyển đến màn hình Quản lý Kịch bản khuyến nghị.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Dashboard.
2. Người dùng nhấn vào liên kết"Kịch bản khuyến nghị".
3. Hệ thống xác thực quyền truy cập của người dùng.
4. Hệ thống chuyển hướng trình duyệt đến địa chỉ URL của chức năng Quản lý Kịch bản khuyến nghị.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Người dùng không có quyền truy cập trang Kịch bản khuyến nghị.
→ Hệ thống chặn và hiển thị lỗi.
2. Lỗi chuyển hướng trang.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A01: Quyền truy cập phải tuân thủ phân quyền của người dùng.
### 2.70. Truy cập nhanh kịch bản tùy chỉnh
Use Case ID:
70
Use Case Name:
Truy cập nhanh kịch bản tùy chỉnh
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép điều hướng trực tiếp đến giao diện quản lý các kịch bản mô phỏng tùy chỉnh của người dùng từ Dashboard.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền truy cập Kịch bản tùy chỉnh (UC 92, 97-99).
Post-condition:
(Điều kiện đủ)
Người dùng được chuyển đến màn hình Quản lý Kịch bản tùy chỉnh.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Dashboard.
2. Người dùng nhấn vào liên kết "Kịch bản tùy chỉnh".
3. Hệ thống xác thực quyền truy cập của người dùng.
4. Hệ thống chuyển hướng trình duyệt đến địa chỉ URL của chức năng Quản lý Kịch bản tùy chỉnh.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Người dùng không có quyền truy cập trang Kịch bản tùy chỉnh.
→ Hệ thống chặn và hiển thị lỗi.
2. Lỗi chuyển hướng trang.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-A01: Quyền truy cập phải tuân thủ phân quyền của người dùng.
### 2.71. Thêm mới đường truyền dữ liệu
Use Case ID:
71
Use Case Name:
Thêm mới đường truyền dữ liệu
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép thiết lập một kết nối hoặc kênh mới để truyền nhận dữ liệu giữa hệ thống hiện tại và một hệ thống/đơn vị bên ngoài.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Quản lý truyền dữ liệu" (BR-DT01).
Post-condition:
(Điều kiện đủ)
Một đường truyền dữ liệu mới được tạo và sẵn sàng để cấu hình chi tiết.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Báo cáo" -> "Truyền dữ liệu" -> "Thêm mới".
2. Admin nhập các thông tin bắt buộc: Tên tiến trình, Mẫu truyền, Thời khoảng(thời gian-khoảng cách mỗi điểm dữ liệu), Mã tỉnh, ký hiệu thủy điện, đường dẫn đơn vị tiếp nhận, tên đăng nhập, mật khẩu, thời gian trễ.
4. Admin nhấn nút "Hoàn thành".
5. Hệ thống tạo bản ghi đường truyền mới.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Thông số kết nối nhập vào không hợp lệ (ví dụ: định dạng IP sai).
→ Hệ thống hiển thị lỗi.
2. Lỗi hệ thống khi lưu trữ.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DT01: Chỉ Admin mới có quyền tạo và quản lý đường truyền dữ liệu.
BR-DT02: Tên đường truyền dữ liệu phải là duy nhất.
### 2.72. Cài đặt đường truyền dữ liệu
Use Case ID:
72
Use Case Name:
Cài đặt đường truyền dữ liệu
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cấu hình các thông số kỹ thuật và quy tắc cho đường truyền dữ liệu (ví dụ: tần suất truyền, định dạng tệp, cơ chế bảo mật, xử lý lỗi).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Quản lý truyền dữ liệu". Đường truyền đã được tạo (UC 71).
Post-condition:
(Điều kiện đủ)
Các thông số kỹ thuật và quy tắc của đường truyền được cập nhật.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Truyền dữ liệu", chọn một đường truyền và nhấn nút "Cài đặt".
2. Hệ thống hiển thị các tab/form cấu hình chi tiết.
3. Admin thiết lập các quy tắc: Tần suất truyền (ví dụ: 15 phút/lần), Định dạng dữ liệu (ví dụ: JSON, XML, Excel), Nguyên tắc đặt tên tệp (BR-DT04), Cơ chế xác thực, Cơ chế xử lý lỗi (ví dụ: thử lại N lần).
4. Admin nhấn nút "Lưu/Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của cấu hình (BR-DT04).
6. Hệ thống cập nhật cấu hình đường truyền.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Cấu hình tần suất truyền không hợp lệ (ví dụ: thời gian quá ngắn).
→ Hệ thống hiển thị lỗi.
2. Lỗi hệ thống khi lưu trữ cấu hình.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DT04: Định dạng và nguyên tắc đặt tên tệp phải tuân thủ yêu cầu của hệ thống đích.
BR-DT01: Chỉ Admin mới có quyền quản lý đường truyền dữ liệu.
### 2.73. Truyền bù dữ liệu
Use Case ID:
73
Use Case Name:
Truyền bù dữ liệu
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép thực hiện việc truyền lại hoặc bù đắp dữ liệu bị thiếu/lỗi trong một khoảng thời gian nhất định cho hệ thống đích.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Truyền bù dữ liệu" (BR-DT06). Đường truyền đã được cấu hình hợp lệ (UC 72). Dữ liệu bị thiếu/lỗi đã được xác định.
Post-condition:
(Điều kiện đủ)
Dữ liệu đã được truyền lại cho hệ thống đích.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Truyền bù dữ liệu".
2. Người dùng chọn Đường truyền dữ liệu cần bù.
3. Người dùng chọn Khoảng thời gian (Từ - Đến) và Loại dữ liệu cần truyền bù.
4. Người dùng nhấn nút "Thực hiện Truyền bù".
5. Hệ thống truy xuất dữ liệu trong khoảng thời gian đã chọn.
6. Hệ thống tiến hành đóng gói và truyền dữ liệu theo cấu hình đường truyền (BR-DT07).
7. Hệ thống theo dõi trạng thái truyền và ghi nhận vào Lịch sử truyền dữ liệu (UC 74).
8. Hệ thống hiển thị thông báo thành công hoặc thông báo lỗi nếu quá trình truyền thất bại.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Khoảng thời gian yêu cầu truyền bù quá lớn (BR-DT08).  → Hệ thống hiển thị lỗi và yêu cầu giới hạn lại.  2. Đường truyền không hoạt động/lỗi kết nối.  → Hệ thống hiển thị lỗi kết nối.  3. Lỗi xác thực quyền (BR-DT06).  → Hệ thống chặn.
Business Rules:
(Nghiệp vụ)
BR-DT06: Chỉ người dùng có quyền Vận hành/Admin mới được phép thực hiện truyền bù.  BR-DT07: Dữ liệu được truyền bù phải tuân thủ cấu hình định dạng của đường truyền.  BR-DT08: Giới hạn thời gian tối đa cho mỗi lần truyền bù là <tự thêm nghiệp vụ: 3 tháng>.
### 2.74. Lịch sử truyền dữ liệu
Use Case ID:
74
Use Case Name:
Lịch sử truyền dữ liệu
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép xem lại nhật ký chi tiết về các giao dịch và trạng thái truyền dữ liệu đã thực hiện (bao gồm cả truyền tự động và truyền bù), giúp theo dõi và kiểm soát chất lượng dữ liệu.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền "Xem lịch sử truyền dữ liệu" (BR-DT09).
Post-condition:
(Điều kiện đủ)
Nhật ký truyền dữ liệu được hiển thị trên giao diện.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Truyền dữ liệu" -> "Lịch sử truyền dữ liệu".
2. Hệ thống hiển thị danh sách các lần truyền dữ liệu.
3. Người dùng có thể Lọc theo các tiêu chí: Tên đường truyền, Khoảng thời gian.
4. Hệ thống truy xuất và hiển thị chi tiết nhật ký (Thời gian bắt đầu/kết thúc, Số lượng bản ghi).
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi truy xuất nhật ký.
→ Hệ thống hiển thị thông báo lỗi.
2. Người dùng cố gắng xem lịch sử truyền mà không có quyền (BR-DT09).
→ Hệ thống chặn.
Business Rules:
(Nghiệp vụ)
BR-DT09: Chỉ người dùng có quyền Vận hành/Admin mới được phép xem lịch sử truyền dữ liệu.
### 2.75. Xóa đường truyền dữ liệu
Use Case ID:
75
Use Case Name:
Xóa đường truyền dữ liệu
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin loại bỏ một đường truyền dữ liệu không còn sử dụng khỏi hệ thống.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Quản lý truyền dữ liệu". Đường truyền đã tồn tại.
Post-condition:
(Điều kiện đủ)
Đường truyền dữ liệu được chọn đã bị xóa khỏi cấu hình hệ thống.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Truyền dữ liệu", chọn một đường truyền và nhấn nút "Xóa".
2. Hệ thống hiển thị hộp thoại xác nhận.
3. Admin xác nhận xóa.
4. Hệ thống xóa đường truyền dữ liệu và các cấu hình liên quan (UC 72, 76, 77, 78).
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi xóa dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DT01: Chỉ Admin mới có quyền tạo và quản lý đường truyền dữ liệu.
### 2.76. Thêm yếu tố truyền
Use Case ID:
76
Use Case Name:
Thêm yếu tố truyền
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bổ sung một thông số hoặc loại dữ liệu mới (yếu tố truyền) vào cấu hình của một đường truyền dữ liệu cụ thể (ví dụ: thêm tham số "Mực nước dự báo 24h" vào đường truyền EVN).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Quản lý truyền dữ liệu". Đường truyền đã được tạo (UC 71).
Post-condition:
(Điều kiện đủ)
Một yếu tố truyền dữ liệu mới được thêm vào cấu hình đường truyền.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Truyền dữ liệu", chọn một đường truyền và vào màn hình "Quản lý yếu tố truyền".
2. Admin nhấn nút "Thêm mới yếu tố truyền".
3. Admin chọn Tham số/Cảm biến nguồn từ hệ thống (ví dụ: Mã cảm biến Mực nước Hồ).
4. Admin nhập Tên yếu tố truyền trên hệ thống đích (ví dụ: H_ho_TB) (BR-DT12).
5. Admin nhập Tham số chuyển đổi (nếu cần).
6. Admin nhấn nút "Lưu/Thêm".
7. Hệ thống kiểm tra tính duy nhất của yếu tố truyền trên đường truyền này.
8. Hệ thống cập nhật cấu hình đường truyền.
9. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Yếu tố truyền đã tồn tại trên đường truyền này (BR-DT12).
→ Hệ thống hiển thị lỗi.
2. Tham số nguồn không tồn tại.
→ Hệ thống hiển thị lỗi.
3. Lỗi hệ thống khi lưu trữ.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DT12: Mã/Tên yếu tố truyền trên hệ thống đích phải là duy nhất trong phạm vi một đường truyền.
BR-DT01: Chỉ Admin mới có quyền quản lý đường truyền dữ liệu.
### 2.77. Chỉnh sửa yếu tố truyền
Use Case ID:
77
Use Case Name:
Chỉnh sửa yếu tố truyền
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép cập nhật các thông số của một yếu tố truyền dữ liệu hiện có (ví dụ: thay đổi tham số nguồn, thay đổi tên yếu tố truyền trên hệ thống đích).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Quản lý truyền dữ liệu". Yếu tố truyền đã tồn tại.
Post-condition:
(Điều kiện đủ)
Thông số của yếu tố truyền được cập nhật trong cấu hình.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Truyền dữ liệu", chọn một đường truyền và vào màn hình "Quản lý yếu tố truyền".
2. Admin chọn một yếu tố truyền và nhấn nút "Chỉnh sửa".
3. Admin chỉnh sửa các thông số: Tham số nguồn, Tên yếu tố truyền trên hệ thống đích (BR-DT12), Tham số chuyển đổi.
4. Admin nhấn nút "Lưu/Cập nhật".
5. Hệ thống kiểm tra tính hợp lệ của dữ liệu (BR-DT12).
6. Hệ thống cập nhật cấu hình đường truyền.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Tên yếu tố truyền trên hệ thống đích bị trùng (BR-DT12).
→ Hệ thống hiển thị lỗi.
2. Tham số nguồn mới không tồn tại.
→ Hệ thống hiển thị lỗi.
3. Lỗi hệ thống khi lưu trữ.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DT12: Mã/Tên yếu tố truyền trên hệ thống đích phải là duy nhất trong phạm vi một đường truyền.
BR-DT01: Chỉ Admin mới có quyền quản lý đường truyền dữ liệu.
### 2.78. Xóa yếu tố truyền
Use Case ID:
78
Use Case Name:
Xóa yếu tố truyền
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép loại bỏ một thông số (yếu tố truyền) khỏi cấu hình truyền dữ liệu của một đường truyền cụ thể.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Quản lý truyền dữ liệu". Yếu tố truyền đã tồn tại.
Post-condition:
(Điều kiện đủ)
Yếu tố truyền được xóa khỏi cấu hình của đường truyền dữ liệu.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Truyền dữ liệu", chọn một đường truyền và vào màn hình "Quản lý yếu tố truyền".
2. Admin chọn một yếu tố truyền và nhấn nút "Xóa".
3. Hệ thống hiển thị hộp thoại xác nhận.
4. Admin xác nhận xóa.
5. Hệ thống kiểm tra xem yếu tố truyền có phải là yếu tố duy nhất đang được cấu hình hay không (BR-DT13).
6. Hệ thống xóa yếu tố truyền khỏi cấu hình.
7. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Yếu tố truyền là yếu tố duy nhất đang được cấu hình (BR-DT13).
→ Hệ thống hiển thị lỗi và không cho phép xóa, yêu cầu Admin phải thêm yếu tố khác hoặc xóa đường truyền.
2. Lỗi hệ thống khi xóa.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-DT13: Đường truyền dữ liệu phải có ít nhất 1 yếu tố truyền được cấu hình.
BR-DT01: Chỉ Admin mới có quyền quản lý đường truyền dữ liệu.
### 2.79. Dữ liệu mưa
Use Case ID:
79
Use Case Name:
Dữ liệu mưa
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng xem dữ liệu chi tiết về lượng mưa theo thời gian và khu vực dưới dạng bảng trên bản đồ.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền xem dữ liệu thời tiết. Dữ liệu mưa thực đo đã được thu thập.
Post-condition:
(Điều kiện đủ)
Dữ liệu mưa được hiển thị.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Báo cáo" -> "Thời tiết & Dự báo" Chọn biểu tượng "Mưa".
2. Hệ thống truy xuất dữ liệu mưa từ các trạm/lưới mưa.
3. Hệ thống hiển thị dữ liệu dưới dạng bảng và biểu đồ.
Alternative Flows:
(Luồng phụ)
A1: Người dùng chọn Tải xuống.
→ Hệ thống tạo tệp Excel/CSV với dữ liệu đã lọc và gửi đến trình duyệt.
Exceptions:
(Trường hợp
ngoại lệ)
1. Khoảng thời gian truy vấn không có dữ liệu mưa.
→ Hệ thống hiển thị thông báo "Không có dữ liệu".
2. Người dùng không có quyền truy cập dữ liệu của khu vực đã chọn.
→ Hệ thống chặn và hiển thị lỗi.
3. Lỗi hệ thống khi truy xuất dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-WF01: Dữ liệu mưa hiển thị phải được phân biệt rõ ràng giữa Mưa Thực đo và Mưa Phân tích/Dự báo (UC 46, 47, 48).
### 2.80. Bản đồ radar
Use Case ID:
80
Use Case Name:
Bản đồ radar
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép hiển thị dữ liệu radar thời tiết (thường là ảnh radar phản xạ) trên bản đồ, theo dõi diễn biến và cường độ mưa theo thời gian thực hoặc gần thời gian thực.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền xem bản đồ radar. Hệ thống có kết nối với nguồn dữ liệu radar.
Post-condition:
(Điều kiện đủ)
Lớp phủ dữ liệu radar được hiển thị trên bản đồ.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Thời tiết & Dự báo" -> "Bản đồ radar".
2. Hệ thống truy xuất ảnh radar mới nhất từ nguồn dữ liệu (BR-WF02).
3. Hệ thống hiển thị bản đồ địa lý với lớp phủ dữ liệu radar.
4. Người dùng có thể điều chỉnh Khoảng thời gian (dạng thanh trượt) để xem diễn biến mưa trong quá khứ gần nhất.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Không kết nối được với nguồn dữ liệu radar (BR-WF02).
→ Hệ thống hiển thị thông báo lỗi kết nối và không tải được lớp phủ radar.
2. Lỗi hệ thống khi hiển thị trên bản đồ.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-WF02: Dữ liệu radar phải được cập nhật định kỳ để đảm bảo tính thời gian thực.
### 2.81. Bản đồ bão
Use Case ID:
81
Use Case Name:
Bản đồ bão
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép hiển thị đường đi và thông tin dự báo về các cơn bão/áp thấp nhiệt đới hiện tại trên bản đồ.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền xem bản đồ bão. Hệ thống có kết nối với nguồn dữ liệu bão.
Post-condition:
(Điều kiện đủ)
Đường đi dự báo bão được hiển thị trên bản đồ.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Thời tiết & Dự báo" -> "Bản đồ bão".
2. Hệ thống truy xuất dữ liệu về các cơn bão/áp thấp nhiệt đới đang hoạt động.
3. Hệ thống hiển thị bản đồ địa lý với Vị trí hiện tại, Đường đi dự báo, Phạm vi ảnh hưởng của bão.
4. Người dùng có thể chọn một cơn bão cụ thể để xem chi tiết (tốc độ gió, áp suất).
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Không có cơn bão/áp thấp nhiệt đới nào đang hoạt động.
→ Hệ thống hiển thị thông báo "Không có thông tin bão đang hoạt động".
2. Lỗi kết nối với nguồn dữ liệu bão.
→ Hệ thống hiển thị thông báo lỗi.
3. Lỗi hệ thống khi hiển thị trên bản đồ.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-WF04: Dữ liệu bão phải được lấy từ nguồn tin.
BR-WF05: Đường đi dự báo phải có mốc thời gian rõ ràng (ví dụ: Dự báo 24h, 48h tới).
### 2.82. Chuyển hướng đến vị trí cơn bão
Use Case ID:
82
Use Case Name:
Chuyển hướng đến vị trí cơn bão
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép tự động định vị và tập trung bản đồ vào vị trí hiện tại hoặc dự báo của cơn bão.
Precondition:
(Điều kiện cần)
Người dùng đang xem Bản đồ bão (UC 81). Có ít nhất một cơn bão đang hoạt động.
Post-condition:
(Điều kiện đủ)
Bản đồ được phóng to và đặt tâm vào vị trí của cơn bão.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Bản đồ bão.
2. Người dùng nhấn vào chọn tên/điểm trên đường đi dự báo của bão.
3. Hệ thống xác định tọa độ của vị trí đã chọn (vị trí hiện tại của bão hoặc vị trí dự báo tại mốc thời gian).
4. Hệ thống điều chỉnh tâm bản đồ và mức độ phóng to (Zoom Level) sao cho cơn bão hiển thị rõ nhất.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi lấy tọa độ bão.
→ Hệ thống hiển thị lỗi và giữ nguyên bản đồ.
Business Rules:
(Nghiệp vụ)
BR-WF06: Mức độ phóng to mặc định khi chuyển hướng phải bao gồm toàn bộ phạm vi ảnh hưởng của bão.
### 2.83. Xem dữ liệu trạm trên bản đồ
Use Case ID:
83
Use Case Name:
Xem dữ liệu trạm trên bản đồ
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép hiển thị các thông số đo được của trạm (ví dụ: mực nước, lượng mưa) trực tiếp trên bản đồ dưới dạng.
Precondition:
(Điều kiện cần)
Người dùng đang xem bản đồ (ví dụ: Bản đồ tổng thể hệ thống). Dữ liệu trạm mới nhất đã có.
Post-condition:
(Điều kiện đủ)
Dữ liệu trạm mới nhất được hiển thị trên bản đồ.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập màn hình Bản đồ.
2. Hệ thống hiển thị các trạm quan trắc/vận hành dưới dạng các biểu tượng.
3. Người dùng di chuyển chuột Click vào biểu tượng một trạm.
4. Hệ thống truy xuất dữ liệu quan trắc gần nhất của trạm đó (BR-WF07).
5. Hệ thống hiển thị một pop-up/tooltip chứa các thông số chính (ví dụ: Mực nước hiện tại, Mưa 24h).
6. Người dùng nhấn vào pop-up để truy cập Chi tiết dữ liệu trạm (UC 84).
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Trạm không có dữ liệu mới nhất (ví dụ: trạm mất kết nối).
→ Pop-up vẫn hiển thị nhưng kèm cảnh báo "Mất dữ liệu".
2. Lỗi hệ thống khi truy xuất dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
None.
### 2.84. Chi tiết dữ liệu trạm
Use Case ID:
84
Use Case Name:
Chi tiết dữ liệu trạm
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng xem bảng/biểu đồ dữ liệu chi tiết của một trạm cụ thể trong một khoảng thời gian được chỉ định, phục vụ cho việc phân tích chuyên sâu.
Precondition:
(Điều kiện cần)
Người dùng đã đăng nhập và có quyền xem dữ liệu của trạm đó.
Post-condition:
(Điều kiện đủ)
Màn hình chi tiết dữ liệu (Biểu đồ/Bảng) của trạm được hiển thị.
Normal Flow:
(Luồng chính)
1. Người dùng nhấn vào biểu tượng trạm trên bản đồ hoặc chọn trạm từ danh sách.
2. Hệ thống hiển thị popup cho biết dữ liệu chi tiết trạm.
4. Hệ thống tải và hiển thị dữ liệu quan trắc của tất cả các cảm biến/tham số liên quan đến trạm đó trong khoảng thời gian mặc định.
5. Người dùng có thể tùy chỉnh khoảng thời gian xem (UC 85) và tải dữ liệu xuống (UC 86).
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Trạm không tồn tại.
→ Hệ thống hiển thị lỗi "Trạm không tồn tại".
2. Lỗi hệ thống khi truy xuất dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
3. Người dùng không có quyền truy cập trạm.
→ Hệ thống chặn.
Business Rules:
(Nghiệp vụ)
BR-A01: Quyền truy cập vào dữ liệu trạm phải tuân thủ phân quyền.
### 2.85. Tùy chỉnh thời gian lấy dữ liệu trạm
Use Case ID:
85
Use Case Name:
Tùy chỉnh thời gian lấy dữ liệu trạm
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng chọn khoảng thời gian mong muốn để xem dữ liệu chi tiết của trạm trên màn hình Chi tiết dữ liệu trạm (UC 84).
Precondition:
(Điều kiện cần)
Người dùng đang ở màn hình Chi tiết dữ liệu trạm (UC 84).
Post-condition:
(Điều kiện đủ)
Dữ liệu trạm được tải và hiển thị lại theo khoảng thời gian mới.
Normal Flow:
(Luồng chính)
1. Người dùng trên màn hình Chi tiết dữ liệu trạm.
2. Người dùng chọn chức năng Bộ chọn thời gian (Date Range Picker).
3. Người dùng chọn ngày/giờ Bắt đầu và Kết thúc hoặc chọn một khoảng thời gian sẵn có (ví dụ: Hôm qua, Tuần trước).
4. Hệ thống kiểm tra khoảng thời gian (BR-WF09).
6. Hệ thống truy xuất dữ liệu trạm trong khoảng thời gian mới.
7. Hệ thống cập nhật Biểu đồ và Bảng số liệu.
8. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Khoảng thời gian vượt quá giới hạn tối đa cho phép (BR-WF09).
→ Hệ thống hiển thị lỗi và yêu cầu giới hạn lại.
2. Khoảng thời gian không hợp lệ (ví dụ: Ngày bắt đầu sau Ngày kết thúc).
→ Hệ thống hiển thị lỗi.
3. Lỗi hệ thống khi truy xuất dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-WF09: Giới hạn truy vấn dữ liệu trạm tối đa cho mỗi lần.
BR-WF10: Khoảng thời gian phải được hợp lệ về mặt thứ tự thời gian.
### 2.86. Tải xuống dữ liệu trạm
Use Case ID:
86
Use Case Name:
Tải xuống dữ liệu trạm
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng xuất dữ liệu quan trắc đã chọn của trạm về máy tính cá nhân dưới dạng tệp (Excel/CSV).
Precondition:
(Điều kiện cần)
Người dùng đang ở màn hình Chi tiết dữ liệu trạm (UC 84). Đã chọn khoảng thời gian cần tải.
Post-condition:
(Điều kiện đủ)
Tệp dữ liệu trạm được tải về máy tính của người dùng.
Normal Flow:
(Luồng chính)
1. Người dùng trên màn hình Chi tiết dữ liệu trạm.
2. Người dùng chọn các Tham số cần tải xuống (ví dụ: Mực nước, Lưu lượng).
3. Người dùng chọn Định dạng xuất (Excel/CSV).
4. Người dùng nhấn nút "Tải xuống dữ liệu".
5. Hệ thống truy xuất dữ liệu thô/đã tổng hợp theo các tiêu chí (BR-WF11).
6. Hệ thống chuyển đổi dữ liệu thành tệp.
7. Hệ thống gửi tệp đến trình duyệt của người dùng.
8. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu truy xuất vượt quá giới hạn tải xuống tối đa (BR-WF11).
→ Hệ thống hiển thị lỗi.  2. Lỗi hệ thống khi tạo tệp. → Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-WF11: Giới hạn tối đa cho mỗi lần tải xuống là <tự thêm nghiệp vụ: 1 năm dữ liệu>.  BR-A01: Chỉ được phép tải dữ liệu của các trạm mà người dùng có quyền truy cập.
### 2.87. Thông tin thêm bản đồ - Dự báo mưa 24h
Use Case ID:
87
Use Case Name:
Thông tin thêm bản đồ - Dự báo mưa 24h
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép bật hoặc tắt lớp hiển thị dự báo lượng mưa trong 24 giờ tiếp theo (thường dưới dạng bản đồ màu) trên giao diện bản đồ.
Precondition:
(Điều kiện cần)
Người dùng đang xem Bản đồ. Dữ liệu dự báo mưa 24h đã được tính toán.
Post-condition:
(Điều kiện đủ)
Lớp phủ bản đồ dự báo mưa 24h được hiển thị hoặc ẩn đi.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Bản đồ.
2. Người dùng chọn tùy chọn "Dự báo mưa 24h" (ví dụ: trong thanh công cụ Lớp phủ bản đồ).
3. Hệ thống kiểm tra trạng thái Ẩn/Hiện mưa dự báo (UC 48).
4. Hệ thống truy xuất dữ liệu mưa dự báo 24h.
5. Hệ thống hiển thị lớp phủ bản đồ màu với cường độ mưa dự báo tương ứng.
6. Người dùng có thể ẩn lớp phủ bằng cách bỏ chọn.
7. Hệ thống hiển thị thông báo thành công (tùy chọn).
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Không có dữ liệu dự báo mưa 24h.
→ Hệ thống hiển thị cảnh báo và không tải lớp phủ.
2. Cấu hình hệ thống đang ẩn Mưa dự báo (UC 48).
→ Hệ thống hiển thị cảnh báo.
Business Rules:
(Nghiệp vụ)
BR-WF12: Lớp phủ Dự báo mưa 24h phải đồng bộ về thời gian và độ phân giải với dữ liệu dự báo gốc.
### 2.88. Thông tin thêm bản đồ - Bảng tổng hợp các trạm
Use Case ID:
88
Use Case Name:
Thông tin thêm bản đồ - Bảng tổng hợp các trạm
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép hiển thị một bảng tổng hợp các thông tin chính (Mực nước, Lượng mưa, Trạng thái) từ tất cả các trạm/cảm biến quan trọng trên một phần của giao diện bản đồ.
Precondition:
(Điều kiện cần)
Người dùng đang xem Bản đồ. Dữ liệu trạm mới nhất đã có.
Post-condition:
(Điều kiện đủ)
Bảng tổng hợp các trạm được hiển thị/ẩn trên giao diện.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Bản đồ.
2. Tại phần dự báo mưa,người dùng chọn tùy chọn "Bảng tổng hợp trạm".
3. Hệ thống truy xuất dữ liệu quan trắc gần nhất của tất cả các trạm quan trọng trong phạm vi xem bản đồ.
4. Hệ thống tổng hợp dữ liệu (ví dụ: chỉ lấy tham số Mực nước và Mưa 24h).
5. Hệ thống hiển thị một bảng tóm tắt/tổng hợp ở góc màn hình.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi truy xuất/tổng hợp dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
2. Không có trạm nào trong phạm vi xem bản đồ.
→ Hệ thống hiển thị bảng trống/cảnh báo.
Business Rules:
(Nghiệp vụ)
None.
### 2.89. Thông tin thêm bản đồ - Tổng hợp dữ liệu trạm dạng bảng
Use Case ID:
89
Use Case Name:
Thông tin thêm bản đồ - Tổng hợp dữ liệu trạm dạng bảng
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép hiển thị một bảng dữ liệu chi tiết hơn về các thông số quan trắc (Real-time data) trong phạm vi xem bản đồ, thường bao gồm nhiều tham số hơn so với Bảng tổng hợp các trạm (UC 88).
Precondition:
(Điều kiện cần)
Người dùng đang xem Bản đồ. Dữ liệu trạm mới nhất đã có.
Post-condition:
(Điều kiện đủ)
Bảng chi tiết dữ liệu trạm (dạng bảng) được hiển thị/ẩn trên giao diện.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập Bản đồ.
2. Người dùng chọn tùy chọn "Tổng hợp dữ liệu trạm dạng bảng" (ví dụ: trong thanh công cụ Lớp phủ bản đồ).
3. Hệ thống truy xuất dữ liệu quan trắc gần nhất của tất cả các tham số của tất cả các trạm trong phạm vi xem bản đồ.
4. Hệ thống hiển thị một bảng chi tiết (có thể cuộn) ở góc màn hình.
5. Người dùng có thể Sắp xếp/Lọc dữ liệu trong bảng.
6. Hệ thống hiển thị thông báo thành công (tùy chọn).
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi truy xuất/hiển thị dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
2. Số lượng dữ liệu quá lớn, gây chậm trễ tải trang (BR-WF14).
→ Hệ thống cảnh báo và giới hạn số lượng trạm hiển thị.
Business Rules:
(Nghiệp vụ)
None.
### 2.90. Chạy mô phỏng
Use Case ID:
90
Use Case Name:
Chạy mô phỏng
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng thực hiện một kịch bản mô phỏng vận hành hệ thống (ví dụ: mô phỏng xả lũ, mô phỏng phát điện) dựa trên các điều kiện đầu vào đã cấu hình.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Chạy mô phỏng" (BR-SIM01). Đã có một Kịch bản mô phỏng (Simulation Scenario) được tạo hoặc tải lên (UC 92, 97, 98, 99).
Post-condition:
(Điều kiện đủ)
Kết quả mô phỏng được tính toán và sẵn sàng để xem.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Mô phỏng vận hành".
2. Người dùng chọn Kịch bản mô phỏng cần chạy.
3. Người dùng chọn Thời điểm bắt đầu và Khoảng thời gian mô phỏng.
4. Người dùng nhấn nút "Chạy mô phỏng".
5. Hệ thống kiểm tra tính hợp lệ của Kịch bản và Điều kiện (BR-SIM02).
6. Hệ thống gửi Kịch bản và Điều kiện tới Hệ thống Mô hình.
7. Hệ thống Mô hình thực hiện tính toán.
8. Hệ thống nhận kết quả từ Mô hình và lưu trữ (UC 93).
9. Hệ thống hiển thị thông báo thành công và chuyển hướng đến Xem chi tiết kết quả mô phỏng (UC 94).
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Kịch bản mô phỏng không hợp lệ (BR-SIM02).
→ Hệ thống hiển thị lỗi.
2. Lỗi kết nối/lỗi tính toán từ Hệ thống Mô hình.
→ Hệ thống hiển thị lỗi Mô hình.
3. Người dùng cố gắng chạy mô phỏng vượt quá giới hạn tài nguyên (BR-SIM03).
→ Hệ thống chặn và hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-SIM01: Chỉ những người dùng được phân quyền mới được chạy mô phỏng.
BR-SIM02: Kịch bản mô phỏng phải có đủ dữ liệu đầu vào theo yêu cầu của Mô hình.
### 2.91. Thiết lập lại mô phỏng
Use Case ID:
91
Use Case Name:
Thiết lập lại mô phỏng
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng đặt lại các thông số và điều kiện ban đầu của kịch bản mô phỏng hiện tại, loại bỏ các thay đổi tạm thời đã thực hiện.
Precondition:
(Điều kiện cần)
Người dùng đang ở màn hình cấu hình kịch bản mô phỏng.
Post-condition:
(Điều kiện đủ)
Các thông số kịch bản mô phỏng được đưa về trạng thái gốc.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập màn hình cấu hình kịch bản.
2. Người dùng nhấn nút "Thiết lập lại mô phỏng" hoặc "Khôi phục mặc định".
3. Hệ thống hiển thị hộp thoại xác nhận.
4. Người dùng xác nhận thao tác.
5. Hệ thống khôi phục tất cả các tham số của kịch bản về giá trị gốc (hoặc giá trị mặc định của hệ thống) (BR-SIM04).
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi khôi phục dữ liệu gốc.
→ Hệ thống hiển thị lỗi.
2. Người dùng không có quyền (BR-SIM01).
→ Hệ thống chặn.
Business Rules:
(Nghiệp vụ)
BR-SIM04: Thao tác thiết lập lại chỉ áp dụng cho các tham số đầu vào của kịch bản đang được chỉnh sửa, không ảnh hưởng đến dữ liệu gốc của hệ thống.
BR-SIM01: Chỉ những người dùng được phân quyền mới được thao tác mô phỏng.
### 2.92. Tải lên kịch bản mô phỏng
Use Case ID:
92
Use Case Name:
Tải lên kịch bản mô phỏng
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép người dùng tải lên một tệp kịch bản mô phỏng đã được chuẩn bị sẵn (ví dụ: tệp Excel/CSV) để sử dụng làm điều kiện đầu vào cho chạy mô phỏng.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Tải lên kịch bản mô phỏng" (BR-SIM01). Tệp kịch bản phải tuân thủ định dạng yêu cầu (BR-SIM05).
Post-condition:
(Điều kiện đủ)
Dữ liệu kịch bản được tải lên và lưu trữ, sẵn sàng để sử dụng.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Quản lý Kịch bản" -> "Tải lên".
2. Người dùng chọn Loại kịch bản (ví dụ: Công suất, Lưu lượng vào) (UC 97, 98, 99) và nhấn nút "Chọn tệp".
3. Người dùng chọn tệp kịch bản từ máy tính.
4. Người dùng nhấn nút "Tải lên/Xử lý".
5. Hệ thống kiểm tra định dạng và tính hợp lệ của dữ liệu trong tệp (BR-SIM05).
6. Nếu hợp lệ, hệ thống lưu trữ dữ liệu kịch bản mới.
7. Hệ thống hiển thị thông báo thành công và tên kịch bản mới.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Tên kịch bản trong tệp đã tồn tại.
→ Hệ thống hỏi người dùng có muốn ghi đè lên kịch bản cũ không.
2. Tệp không đúng định dạng (BR-SIM05).
→ Hệ thống hiển thị lỗi định dạng tệp.
3. Dữ liệu trong tệp không hợp lệ (ví dụ: giá trị âm).
→ Hệ thống hiển thị lỗi và danh sách các lỗi dữ liệu.
Business Rules:
(Nghiệp vụ)
BR-SIM01: Chỉ những người dùng được phân quyền mới được tải lên kịch bản.
BR-SIM05: Tệp kịch bản phải là định dạng Excel/CSV và tuân thủ cấu trúc cột/hàng đã định nghĩa.
### 2.93. Lưu kết quả mô phỏng
Use Case ID:
93
Use Case Name:
Lưu kết quả mô phỏng
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép lưu trữ kết quả đầu ra của một lần chạy mô phỏng (do người dùng kích hoạt hoặc do Hệ thống Mô hình tự động lưu trữ).
Precondition:
(Điều kiện cần)
Quá trình mô phỏng đã hoàn thành và tạo ra kết quả đầu ra.
Post-condition:
(Điều kiện đủ)
Kết quả mô phỏng được lưu trữ và có thể truy vấn được (UC 94).
Normal Flow:
(Luồng chính)
1. Hệ thống Mô hình hoàn thành tính toán và gửi kết quả về Hệ thống Quản lý.
2. Hệ thống Quản lý tạo một ID kết quả (Result ID) duy nhất.
3. Hệ thống lưu trữ tất cả dữ liệu đầu ra mô phỏng (Biểu đồ, Bảng, Tóm tắt) và các tham số đầu vào của Kịch bản đã chạy (BR-SIM06).
4. Hệ thống hiển thị thông báo thành công (chỉ cho người dùng nếu thao tác được kích hoạt thủ công).
Alternative Flows:
(Luồng phụ)
A1: Người dùng chạy mô phỏng thủ công (UC 90) và chọn tùy chọn "Lưu kết quả" sau khi xem.
→ Người dùng đặt Tên kết quả và nhấn Lưu.
→ Hệ thống lưu kết quả.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi lưu trữ dữ liệu.
→ Hệ thống ghi lại Log lỗi (UC 100).
2. Dữ liệu kết quả quá lớn, vượt quá giới hạn lưu trữ.
→ Hệ thống cảnh báo và yêu cầu nén/giới hạn dữ liệu (BR-SIM07).
Business Rules:
(Nghiệp vụ)
BR-SIM08: Tên kết quả (nếu do người dùng đặt) phải là duy nhất.
### 2.94. Xem chi tiết kết quả mô phỏng
Use Case ID:
94
Use Case Name:
Xem chi tiết kết quả mô phỏng
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép hiển thị chi tiết các số liệu, biểu đồ, và tóm tắt từ một kết quả mô phỏng đã lưu.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Xem kết quả mô phỏng" (BR-SIM01). Kết quả mô phỏng đã được lưu trữ (UC 93).
Post-condition:
(Điều kiện đủ)
Các số liệu và biểu đồ chi tiết của kết quả mô phỏng được hiển thị.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Quản lý Kết quả Mô phỏng".
2. Người dùng chọn một kết quả mô phỏng từ danh sách (BR-SIM09).
3. Hệ thống tải và hiển thị giao diện chi tiết: Biểu đồ so sánh (Dự báo, Thực đo, Mô phỏng), Bảng số liệu chi tiết, Thông tin tóm tắt.
4. Người dùng có thể Tải kết quả lên Dashboard (UC 95).
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Kết quả mô phỏng không tồn tại/lỗi dữ liệu (BR-SIM09).
→ Hệ thống hiển thị lỗi.
2. Người dùng không có quyền truy cập kết quả này (BR-SIM01).
→ Hệ thống chặn.
Business Rules:
(Nghiệp vụ)
BR-SIM01: Chỉ những người dùng được phân quyền mới được xem kết quả.
### 2.95. Tải kết quả mô phỏng lên dashboard
Use Case ID:
95
Use Case Name:
Tải kết quả mô phỏng lên dashboard
Primary Actor:
User, Admin
Secondary Actors:
None
Description:
Cho phép hiển thị dữ liệu từ một kết quả mô phỏng đã lưu lên giao diện Dashboard (thường là biểu đồ chính) để so sánh trực tiếp với dữ liệu Thực đo hoặc Dự báo.
Precondition:
Người dùng đang xem chi tiết kết quả mô phỏng (UC 94).
Post-condition:
Lớp phủ dữ liệu Mô phỏng được thêm vào Dashboard.
Normal Flow:
1. Người dùng trên màn hình Chi tiết kết quả mô phỏng.
2. Người dùng nhấn nút "Tải lên Dashboard" hoặc "So sánh".
3. Hệ thống hiển thị hộp thoại xác nhận và tùy chọn Vị trí hiển thị (ví dụ: Biểu đồ chính Mực nước Hồ).
4. Người dùng xác nhận.
5. Hệ thống thêm lớp dữ liệu Mô phỏng tương ứng vào Dashboard.
6. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
None.
Exceptions:
1. Biểu đồ trên Dashboard đang bị đầy hoặc không cho phép thêm lớp dữ liệu Mô phỏng (BR-SIM10).
→ Hệ thống hiển thị lỗi.
2. Lỗi hệ thống khi thêm lớp dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
BR-SIM10: Chỉ được phép hiển thị tối đa 1kịch bản khuyến nghịtrên Dashboard.
BR-SIM11: Dữ liệu mô phỏng tải lên Dashboard phải có màu sắc/chú giải rõ ràng.
### 2.96. Chỉnh sửa kịch bản khuyến nghị
Use Case ID:
96
Use Case Name:
Chỉnh sửa kịch bản khuyến nghị
Primary Actor:
(Người dùng)
Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép Admin điều chỉnh các thông số/quy tắc cốt lõi trong kịch bản khuyến nghị vận hành (dành cho hệ thống tự động tạo khuyến nghị).
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Chỉnh sửa kịch bản khuyến nghị" (BR-SIM01).
Post-condition:
(Điều kiện đủ)
Kịch bản khuyến nghị được cập nhật và ảnh hưởng đến các khuyến nghị sau này.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Quản lý Kịch bản khuyến nghị" (UC 69).
2. Admin chọn kịch bản cần chỉnh sửa và nhấn nút "Chỉnh sửa".
3. Hệ thống hiển thị các tham số/quy tắc chi tiết (ví dụ: Hệ số ưu tiên phát điện, Giới hạn thay đổi mực nước).
4. Admin chỉnh sửa các giá trị.
5. Admin nhấn nút "Lưu/Cập nhật".
6. Hệ thống kiểm tra tính hợp lệ và cảnh báo về tác động của thay đổi (BR-SIM12).
7. Hệ thống cập nhật kịch bản khuyến nghị.
8. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Giá trị nhập vào vi phạm quy tắc logic (BR-SIM12).
→ Hệ thống hiển thị lỗi.
2. Lỗi hệ thống khi lưu trữ.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
(Nghiệp vụ)
BR-SIM01: Chỉ Admin mới có quyền chỉnh sửa kịch bản khuyến nghị.
BR-SIM12: Hệ thống phải lưu trữ lịch sử thay đổi của Kịch bản khuyến nghị (Audit Trail) và yêu cầu xác nhận lần 2 trước khi lưu.
### 2.97. Tải lên kịch bản công suất
Use Case ID:
97
Use Case Name:
Tải lên kịch bản công suất
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép tải lên tệp dữ liệu kịch bản về công suất vận hành (ví dụ: Biểu đồ Công suất theo giờ) để sử dụng làm đầu vào cho mô phỏng.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Tải lên kịch bản" (BR-SIM01). Tệp tuân thủ định dạng (BR-SIM05).
Post-condition:
(Điều kiện đủ)
Dữ liệu kịch bản công suất được lưu trữ.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Quản lý Kịch bản" -> "Tải lên Kịch bản Công suất".
2. Người dùng chọn tệp.
3. Hệ thống kiểm tra định dạng và tính hợp lệ của dữ liệu (ví dụ: công suất không vượt quá giới hạn tổ máy - BR-SIM13).
4. Hệ thống lưu trữ kịch bản.
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu công suất vượt quá giới hạn kỹ thuật (BR-SIM13).
→ Hệ thống hiển thị lỗi.
2. Tệp không đúng định dạng (BR-SIM05).
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-SIM01: Chỉ những người dùng được phân quyền mới được tải lên kịch bản.
BR-SIM05: Tệp phải là định dạng Excel/CSV và tuân thủ cấu trúc.
BR-SIM13: Giá trị công suất trong kịch bản không được vượt quá Tổng công suất lắp máy của Nhà máy.
### 2.98. Tải lên kịch bản lưu lượng vào
Use Case ID:
98
Use Case Name:
Tải lên kịch bản lưu lượng vào
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép tải lên tệp dữ liệu kịch bản về lưu lượng nước/vật chất đầu vào (Inflow) (ví dụ: Lưu lượng nước dự kiến chảy vào hồ) để sử dụng làm đầu vào cho mô phỏng.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Tải lên kịch bản" (BR-SIM01). Tệp tuân thủ định dạng (BR-SIM05).
Post-condition:
(Điều kiện đủ)
Dữ liệu kịch bản lưu lượng vào được lưu trữ.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Quản lý Kịch bản" -> "Tải lên Kịch bản Lưu lượng vào".  2. Người dùng chọn tệp.  3. Hệ thống kiểm tra định dạng và tính hợp lệ của dữ liệu (ví dụ: giá trị lưu lượng không âm - BR-SIM14).  4. Hệ thống lưu trữ kịch bản.  5. Hệ thống hiển thị thông báo thành công.  (Các bước chi tiết tương tự UC 92)
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Dữ liệu lưu lượng là giá trị âm (BR-SIM14). → Hệ thống hiển thị lỗi.  2. Tệp không đúng định dạng (BR-SIM05). → Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-SIM01: Chỉ những người dùng được phân quyền mới được tải lên kịch bản.  BR-SIM05: Tệp phải là định dạng Excel/CSV và tuân thủ cấu trúc.  BR-SIM14: Giá trị lưu lượng vào phải là giá trị không âm.
### 2.99. Tải lên kịch bản lưu lượng xả
Use Case ID:
99
Use Case Name:
Tải lên kịch bản lưu lượng xả
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép tải lên tệp dữ liệu kịch bản về lưu lượng nước/vật chất xả ra (Outflow) (ví dụ: Lưu lượng nước xả qua tổ máy và cửa xả) để sử dụng làm đầu vào cho mô phỏng.
Precondition:
(Điều kiện cần)
Người dùng có quyền "Tải lên kịch bản" (BR-SIM01). Tệp tuân thủ định dạng (BR-SIM05).
Post-condition:
(Điều kiện đủ)
Dữ liệu kịch bản lưu lượng xả được lưu trữ.
Normal Flow:
(Luồng chính)
1. Người dùng truy cập chức năng "Quản lý Kịch bản" -> "Tải lên Kịch bản Lưu lượng xả".
2. Người dùng chọn tệp.
3. Hệ thống kiểm tra định dạng và tính hợp lệ của dữ liệu (ví dụ: tổng lưu lượng xả không vượt quá giới hạn an toàn - BR-SIM15).
4. Hệ thống lưu trữ kịch bản.
5. Hệ thống hiển thị thông báo thành công.  (Các bước chi tiết tương tự UC 92)
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp ngoại lệ)
1. Dữ liệu lưu lượng xả vượt quá giới hạn an toàn (BR-SIM15).
→ Hệ thống hiển thị lỗi.
2. Tệp không đúng định dạng (BR-SIM05).
→ Hệ thống hiển thị lỗi.
Business Rules:
(Nghiệp vụ)
BR-SIM01: Chỉ những người dùng được phân quyền mới được tải lên kịch bản.
BR-SIM05: Tệp phải là định dạng Excel/CSV và tuân thủ cấu trúc.
BR-SIM15: Tổng lưu lượng xả trong kịch bản không được vượt quá Giới hạn xả lũ an toàn đã được cấu hình (UC 37).
### 2.100. Xem log hệ thống
Use Case ID:
100
Use Case Name:
Xem log hệ thống
Primary Actor:
(Người dùng)
User, Admin
Secondary Actors:
None
Description:
(Mô tả)
Cho phép truy cập và xem nhật ký hoạt động (Log) chi tiết của hệ thống (ví dụ: hoạt động đăng nhập, cảnh báo, lỗi, thay đổi cấu hình) để phục vụ cho mục đích kiểm tra và khắc phục sự cố.
Precondition:
(Điều kiện cần)
Admin đã đăng nhập và có quyền "Xem log hệ thống" (BR-LOG01).
Post-condition:
(Điều kiện đủ)
Danh sách các sự kiện log hệ thống được hiển thị.
Normal Flow:
(Luồng chính)
1. Admin truy cập chức năng "Log" -> "Xem log hệ thống".
2. Hệ thống truy vấn và hiển thị danh sách các bản ghi log mới nhất (BR-LOG02).
3. Mỗi bản ghi hiển thị: Thời gian, Mức độ (Level: Info, Warning, Error), Nguồn (Source), Mô tả chi tiết.
4. Admin có thể Lọc log theo nhiều tiêu chí (UC 101).
5. Hệ thống hiển thị thông báo thành công.
Alternative Flows:
(Luồng phụ)
None.
Exceptions:
(Trường hợp
ngoại lệ)
1. Lỗi hệ thống khi truy vấn cơ sở dữ liệu Log.
→ Hệ thống hiển thị thông báo lỗi.
2. Người dùng không có quyền (BR-LOG01).
→ Hệ thống chặn.
Business Rules:
(Nghiệp vụ)
BR-LOG01: Chỉ Admin mới có quyền truy cập log hệ thống.
BR-LOG02: Hệ thống phải ghi lại tất cả các hoạt động thay đổi cấu hình, cảnh báo cấp cao, và lỗi hệ thống.
BR-LOG03: Log phải được lưu trữ trong một kho lưu trữ an toàn trong vòng tối thiểu.
### 2.101. Lọc log trên hệ thống
Use Case ID:
101
Use Case Name:
Lọc log trên hệ thống
Primary Actor:
User, Admin
Secondary Actors:
None
Description:
Cho phép người dùng Admin tìm kiếm và lọc nhật ký hoạt động theo các tiêu chí (thời gian, loại sự kiện, mức độ, người dùng, v.v...) để dễ dàng tìm ra thông tin cần thiết.
Precondition:
Admin đang ở màn hình Xem log hệ thống (UC 100).
Post-condition:
Danh sách log được hiển thị lại theo tiêu chí lọc mới.
Normal Flow:
1. Admin trên màn hình Xem log hệ thống.
2. Admin nhập/chọn các tiêu chí lọc: Khoảng thời gian, Người dùng thực hiện, Từ khóa tìm kiếm (trong Mô tả).
3. Admin nhấn nút "Áp dụng lọc".
4. Hệ thống truy vấn cơ sở dữ liệu Log dựa trên các tiêu chí lọc đã nhập.
5. Hệ thống hiển thị kết quả log đã được lọc.
6. Hệ thống hiển thị thông báo thành công (tùy chọn).
Alternative Flows:
None.
Exceptions:
1. Tiêu chí lọc không hợp lệ.
→ Hệ thống hiển thị lỗi và yêu cầu nhập lại tiêu chí.
2. Lỗi hệ thống khi truy vấn cơ sở dữ liệu.
→ Hệ thống hiển thị thông báo lỗi.
Business Rules:
BR-LOG01: Chỉ Admin mới có quyền truy cập log hệ thống.
BR-LOG05: Các thao tác lọc và tìm kiếm phải được tối ưu hóa để trả về kết quả trong thời gian ngắn ngay cả khi truy vấn lượng dữ liệu lớn.
### 2.102. Chuyển đổi giao diện sáng/tối
Use Case ID:
102
Use Case Name:
Chuyển đổi giao diện sáng/tối
Primary Actor:
User, Admin
Secondary Actors:
None
Description:
Cho phép người dùng chuyển đổi giữa chế độ hiển thị giao diện sáng (light mode) và tối (dark mode) theo sở thích cá nhân.
Precondition:
Người dùng đã đăng nhập hoặc đang ở giao diện người dùng.
Post-condition:
Giao diện của ứng dụng được chuyển sang chế độ sáng hoặc tối.
Normal Flow:
1. Người dùng truy cập biểu tượng Chuyển đổi giao diện (ví dụ: biểu tượng mặt trăng/mặt trời) trên thanh công cụ.
2. Người dùng nhấn vào biểu tượng.
3. Hệ thống ngay lập tức chuyển đổi giao diện sang chế độ đối lập (ví dụ: từ Sáng sang Tối).
4. Hệ thống lưu trữ lựa chọn của người dùng trong cấu hình tài khoản (hoặc Local Storage) để áp dụng cho các lần truy cập sau (BR-OTH01).
5. Hệ thống hiển thị thông báo thành công (tùy chọn).
Alternative Flows:
None.
Exceptions:
1. Lỗi hệ thống khi chuyển đổi giao diện.
→ Hệ thống hiển thị lỗi và giữ nguyên chế độ hiện tại.
Business Rules:
BR-OTH01: Chế độ hiển thị phải được lưu trữ ở cấp độ người dùng để duy trì cài đặt qua các phiên làm việc.
BR-OTH02: Tất cả các thành phần giao diện phải tương thích với cả hai chế độ Sáng và Tối.
