**BÁO CÁO GIỚI THIỆU SẢN PHẨM: ỨNG DỤNG TRỰC QUAN HÓA VÀ XỬ LÝ ĐỒ THỊ (GRAPH VISUALIZATION APP)**

Người thực hiện: Nguyễn Thị Thuỳ Linh

Vị trí ứng tuyển mục tiêu: Software Engineer Intern / Backend Developer / Data Structure & Algorithm Specialist

Ngôn ngữ sử dụng: Python (Tkinter, NetworkX, Matplotlib)

**1. TỔNG QUAN DỰ ÁN (PROJECT OVERVIEW)**

1.1. Đặt vấn đề & Động lực phát triển
Lý thuyết đồ thị (Graph Theory) là một trong những phần cốt lõi của Cấu trúc dữ liệu & Giải thuật và Toán rời rạc, có ứng dụng cực kỳ rộng rãi trong mạng xã hội, hệ thống định vị (GPS), tối ưu hóa mạng lưới vận chuyển và luồng dữ liệu. Tuy nhiên, việc hiểu và vận hành các thuật toán trên đồ thị qua các dòng code thuần (CLI) thường trừu tượng và khó tiếp cận.

Dự án Graph Visualization App được xây dựng nhằm giải quyết bài toán này thông qua việc cung cấp một công cụ trực quan hóa (GUI), giúp người dùng dễ dàng khởi tạo, quản lý cấu trúc đồ thị (vô hướng/có hướng) và theo dõi kết quả thực thi của các thuật toán kinh điển từ cơ bản đến nâng cao.

1.2. Giá trị cốt lõi sản phẩm mang lại
Tính trực quan cao: Chuyển đổi các ma trận, danh sách đỉnh/cạnh phức tạp thành giao diện đồ họa trực quan (Visual Presentation).

Hỗ trợ đa thuật toán: Tích hợp đầy đủ từ các thuật toán tìm kiếm, kiểm tra cấu trúc cơ bản cho đến tối ưu hóa cây khung, luồng cực đại và chu trình Euler.

Tính mở rộng (Scalability): Thiết kế modular rõ ràng giữa tầng xử lý logic đồ thị (networkx), tầng giao diện (tkinter) và tầng hiển thị (matplotlib), cho phép dễ dàng tích hợp thêm thuật toán mới.

**2. KIẾN TRÚC VÀ CÁC TÍNH NĂNG CHÍNH (FEATURES & ARCHITECTURE)**

Ứng dụng được chia làm hai phân hệ chức năng rõ rệt đáp ứng trọn vẹn từ các bài toán cơ bản đến phức tạp:

2.1. Phân hệ Cơ bản (Core Features)
Khởi tạo và Trực quan hóa Đồ thị (Graph Manipulation & Rendering): Hỗ trợ người dùng thêm đỉnh (Node), thêm cạnh (Edge) có trọng số một cách động. Tự động tính toán bố trí vị trí các đỉnh (spring_layout) để đồ thị không bị chồng chéo khi hiển thị qua Matplotlib.

Persistence Data (Lưu trữ dữ liệu): Xuất/Nhập cấu trúc đồ thị thông qua định dạng chuẩn JSON (node_link_data và node_link_graph). Giúp người dùng có thể tái sử dụng hoặc chia sẻ cấu trúc đồ thị đã thiết kế.

Thuật toán Tìm kiếm & Đường đi ngắn nhất:

Duyệt đồ thị theo chiều rộng (BFS) và chiều sâu (DFS), trả về cây duyệt đồ thị.

Tìm đường đi ngắn nhất (Shortest Path) tối ưu theo trọng số giữa 2 đỉnh bất kỳ.

Kiểm tra cấu trúc đặc biệt: Tích hợp bộ lọc kiểm tra đồ thị hai phía (Bipartite Graph Checking).

2.2. Phân hệ Nâng cao (Advanced Algorithms & Optimization)
Tối ưu hóa Cây khung nhỏ nhất (Minimum Spanning Tree - MST): Tích hợp hai thuật toán kinh điển Prim và Kruskal, hiển thị đồ thị kết quả tách biệt để phục vụ bài toán tối ưu chi phí mạng lưới (ví dụ: rải cáp quang, xây đường giao thông).

Tối ưu hóa Luồng (Network Flow): Triển khai thuật toán Ford-Fulkerson giúp tìm luồng cực đại (Maximum Flow) từ đỉnh phát (Source) đến đỉnh thu (Sink), ứng dụng trong tối ưu hóa băng thông mạng hoặc logistics.

Bài toán đồ thị Euler (Eulerian Path & Circuit): Tích hợp thuật toán Fleury và Hierholzer để tìm đường đi / chu trình Euler, giải quyết các bài toán tối ưu lộ trình di chuyển không lặp lại cạnh.

**3. CÔNG NGHỆ SỬ DỤNG VÀ TƯ DUY THIẾT KẾ (TECH STACK & DESIGN)**

3.1. Tech Stack
Ngôn ngữ chính: Python — Tận dụng thế mạnh về xử lý cấu trúc dữ liệu mạnh mẽ, mã nguồn ngắn gọn và tường minh.

Thư viện Engine Đồ thị: NetworkX — Một thư viện chuẩn công nghiệp dành cho việc nghiên cứu mạng lưới phức tạp, tối ưu hóa hiệu năng tính toán ma trận đồ thị.

Thư viện GUI: Tkinter — Thư viện xây dựng giao diện cửa sổ gọn nhẹ, không cài đặt phức tạp, giúp ứng dụng chạy mượt mà cross-platform (Windows, macOS, Linux).

Thư viện Data Visualization: Matplotlib — Chịu trách nhiệm render đồ thị, vẽ các node, edge và hiển thị trọng số một cách chính xác.

3.2. Tư duy thiết kế mã nguồn nổi bật
Event-Driven Programming (Lập trình hướng sự kiện): Hệ thống sử dụng mô hình bắt sự kiện thông qua các nút nhấn (Buttons) của Tkinter kết hợp các hộp thoại tương tác (Toplevel, messagebox) để nhận luồng dữ liệu từ người dùng mà không làm đơ (freeze) luồng chính của ứng dụng.

Loose Coupling (Liên kết lỏng lẻo): Tách biệt logic nhập liệu (simple_input), logic giải thuật (NetworkX) và logic hiển thị (draw_graph, draw_special). Điều này giúp mã nguồn dễ bảo trì; nếu sau này muốn thay đổi giao diện từ Tkinter sang Web (như Flask/React), phần lõi giải thuật hoàn toàn có thể giữ nguyên.

Exception Handling (Xử lý ngoại lệ chặt chẽ): Các hàm tính toán phức tạp như shortest_path hay Ford_Fulkerson đều được bọc trong các khối lệnh try - except nhằm bắt lỗi trường hợp đồ thị không liên thông hoặc không thỏa mãn điều kiện giải thuật, tránh việc ứng dụng bị crash đột ngột và nâng cao trải nghiệm người dùng (UX).

**4. ĐỊNH HƯỚNG PHÁT TRIỂN MỞ RỘNG (FUTURE IMPROVEMENTS)**

Nếu có thêm thời gian phát triển thương mại hoặc nâng cấp, dự án sẽ hướng tới:

Chuyển đổi Phương pháp biểu diễn đồ thị: Hiện thực hóa trọn vẹn việc chuyển đổi qua lại giữa Ma trận kề (Adjacency Matrix), Danh sách kề (Adjacency List) và Danh sách cạnh (Edge List) trực tiếp trên giao diện như yêu cầu mở rộng, giúp người học hiểu sâu hơn về cách lưu trữ dữ liệu trong bộ nhớ.

Hiệu ứng Step-by-Step Animation: Thay vì chỉ hiển thị kết quả cuối cùng, ứng dụng sẽ đổi màu các đỉnh/cạnh theo từng bước chạy của thuật toán (ví dụ: đỉnh đang xét màu đỏ, đỉnh đã duyệt màu xanh) để tăng tối đa tính giáo dục (Educational Value).

Nâng cấp UI/UX: Chuyển dịch lên các framework giao diện hiện đại hơn như CustomTkinter hoặc chuyển thành một ứng dụng Web tương tác bằng Streamlit / Dash để chạy trực tiếp trên trình duyệt mà không cần cài đặt môi trường Python.

**5. KẾT LUẬN**

Dự án Graph Visualization App không chỉ là một bài tập lớn môn Toán rời rạc, mà còn là minh chứng cho khả năng:

Chuyển đổi lý thuyết hàn lâm thành sản phẩm thực tế.

Làm chủ và kết hợp nhiều thư viện chuyên sâu trong Python.

Tư duy thiết kế giao diện hướng người dùng (User-centric) và tổ chức mã nguồn sạch (Clean Code).

Đây sẽ là nền tảng vững chắc để tôi tiếp tục phát triển các hệ thống phần mềm có tư duy giải thuật phức tạp hơn trong tương lai tại quý công ty.
