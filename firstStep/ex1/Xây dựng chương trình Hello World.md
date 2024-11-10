# 1. Cách tạo Java Project trong IntelliJ
  - Bước 1: Mở IntelliJ và tạo dự án mới
    - Mở IntelliJ ( Nhớ là phải mở đúng IntelliJ nha, đừng mở Word rồi thắc mắc “Sao không thấy chỗ tạo project?” )
    - Nhấn vào “New Project” 
    - Đây là nơi bắt đầu cuộc hành trình của bạn. IntelliJ sẽ đưa bạn đến một cửa sổ đầy các lựa chọn như chọn ngôn ngữ, nền tảng, v.v.
  - Bước 2: Chọn Java
    -  Chọn ngôn ngữ Java – Dĩ nhiên rồi! Đừng chọn C++ hay Python nếu bạn không muốn có một cuộc phiêu lưu “lạc đường”.
       ( Thực ra bạn cũng không chọn đuợc ngôn ngữ khác :D ) 
    - Chọn JDK (Java Development Kit) 
    Đây là phần khiến nhiều người hoảng hốt. Nếu chưa có JDK, IntelliJ sẽ hỏi bạn có muốn tải về không. Tải luôn đi, đừng ngại.
  - Bước 3: Đặt tên cho Project
    - Nhập tên dự án – Hãy đặt tên thật “cool” nhưng có ý nghĩa nhé, ví dụ như “HelloWorld” hoặc “DựÁnĐầuTiênCủaTui”. 
    - Đừng đặt tên vô tri kiểu “Project1” – dễ gây hiểu lầm lắm. Đến lúc bạn muốn tìm lại thì phải mở tất cả project ra xem đó. Bài học xương máu tôi từng mắc phải :( 
  - Bước 4: Nhấn “Finish” và bắt đầu
   Finish – Chỉ cần nhấn nút này và IntelliJ sẽ làm phần còn lại. Xin chúc mừng, bạn đã tạo thành công dự án Java đầu tiên!
# 2. Giới thiệu cấu trúc dự án
   Giờ chúng ta nhìn vào “cấu trúc” của dự án. Đừng lo, nó chỉ là một vài thư mục mà bạn sẽ sớm “thân thuộc”.

- src (Source): Đây là trái tim của dự án, nơi chứa toàn bộ mã nguồn (code) của bạn. Tất cả những gì bạn code sẽ nằm trong thư mục này.

- Libraries: Là nơi IntelliJ tự động tìm và đưa các thư viện Java cần thiết vào. Bạn không cần phải đụng vào đây nhiều đâu – nếu thiếu gì, chỉ cần lên Google tìm thêm thư viện là được.

- External Libraries: Tóm lại là mọi thứ ngoài lề mà chương trình bạn cần để chạy, như Java JDK. Nó không phải là thứ bạn “mở ra” đọc mỗi ngày đâu, cứ để nó yên.

- Project Files: Chứa các tệp cấu hình dự án. Đây là phần ít quan trọng đối với người mới học, nên tốt nhất là bỏ qua!

### Vậy đó, không có gì phức tạp. Cứ nghĩ cấu trúc như căn phòng của bạn thôi: 
    - src là bàn học, 
    - Libraries là kệ sách,
    - và External Libraries là đồ dùng ngoài cửa hàng mà bạn chỉ dùng khi thật sự cần thiết.

# 3. Phát triển chương trình Hello World đầu tiên
   Đến phần hấp dẫn nhất: Hello World. Đây là bước mà mọi lập trình viên đều phải trải qua, như bài kiểm tra nhập môn vậy.

- Bước 1: Tạo lớp mới
  - Nhấn chuột phải vào src, chọn New → Java Class.
  - Đặt tên cho lớp là HelloWorld. Hãy chắc rằng lớp này có tên bắt đầu bằng chữ in hoa (IntelliJ sẽ nhắc nhở nếu bạn không làm đúng).
- Bước 2: Viết đoạn mã kinh điển
### Bây giờ, dán đoạn code sau vào lớp HelloWorld:
    public class HelloWorld {
    public static void main(String[] args) {s
    System.out.println("Hello, World!");}}


- Bước 3: Chạy chương trình
  - Click chuột phải vào mã và chọn Run 'HelloWorld.main()'.
  - IntelliJ sẽ làm tất cả các công đoạn còn lại, và nếu bạn thấy dòng chữ Hello, World! hiện lên trong cửa sổ console, xin chúc mừng! Bạn đã hoàn thành chương trình đầu tiên của mình.
## Giải thích mã:
- public class HelloWorld : Đây là nơi bạn khai báo lớp. Nó giống như khi bạn giới thiệu mình là ai với mọi người.
- public static void main(String[] args) : Đoạn này có thể xem như là "nút khởi động" của chương trình. Khi bạn nhấn chạy, máy tính sẽ “đọc” từ đây trước.
- System.out.println("Hello, World!"); : Dòng lệnh này yêu cầu máy tính in ra dòng chữ "Hello, World!" – không hơn không kém.

### Đến đây, bạn đã có một dự án Java trong IntelliJ với một chương trình “Hello World” đơn giản. Hãy tiếp tục khám phá các chức năng khác và tập viết thêm các chương trình phức tạp hơn. Chúc bạn sớm trở thành cao thủ Java nhé!