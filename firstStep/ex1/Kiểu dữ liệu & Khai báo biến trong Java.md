# 1. Kiểu dữ liệu là gì? Có các loại nào và đặc điểm mỗi loại
####   Kiểu dữ liệu là cách mà máy tính hiểu và quản lý dữ liệu bạn đưa vào chương trình, giúp nó biết cách lưu trữ và thao tác với các giá trị này. Nói cách khác, kiểu dữ liệu giống như “nhãn mác” cho từng loại dữ liệu để máy biết phải “đối xử” ra sao.

Dưới đây là các kiểu dữ liệu phổ biến trong Java (cũng tương tự với nhiều ngôn ngữ khác):

# 1. Kiểu dữ liệu nguyên thủy (Primitive Types)
   Trong Java, kiểu dữ liệu nguyên thủy là những kiểu dữ liệu có sẵn, không phải là đối tượng và không chứa các phương thức. 
#####    Java có 8 kiểu dữ liệu nguyên thủy cơ bản, được chia thành 4 nhóm chính: 
- kiểu số nguyên
- kiểu số thực
- kiểu ký tự  
- kiểu luận lý

## A. Kiểu số nguyên (Integer Types)
Dùng để lưu trữ các giá trị số nguyên không có phần thập phân. 
#### Có 4 kiểu số nguyên chính:

### - byte

  - Kích thước: 1 byte (8 bit)
  - Phạm vi giá trị: từ -128 đến 127
  - Sử dụng: Thường dùng để tiết kiệm bộ nhớ trong các trường hợp số nguyên nhỏ, đặc biệt là khi có mảng lớn mà giá trị các phần tử không lớn.
#### Ví dụ:
    byte age = 25;
### - short

  - Kích thước: 2 byte (16 bit)
  - Phạm vi giá trị: từ -32,768 đến 32,767
  - Sử dụng: Dùng khi cần số nguyên có phạm vi lớn hơn byte nhưng vẫn cần tiết kiệm bộ nhớ hơn int.
#### Ví dụ:
    short populationOfVillage = 15000;
### - int

  - Kích thước: 4 byte (32 bit)
  - Phạm vi giá trị: từ -2,147,483,648 đến 2,147,483,647
  - Sử dụng: Đây là kiểu số nguyên được dùng phổ biến nhất cho các giá trị số trong Java.
#### Ví dụ: 
    int distance = 5000;
### - long

- Kích thước: 8 byte (64 bit)
- Phạm vi giá trị: từ -9,223,372,036,854,775,808 đến 9,223,372,036,854,775,807
- Sử dụng: Dùng cho các số nguyên rất lớn mà int không đủ khả năng lưu trữ.
#### Ví dụ:
    long globalPopulation = 7800000000L; 
(Chú ý: Số long cần có hậu tố L để phân biệt với int)
## B. Kiểu số thực (Floating-point Types)
Dùng để lưu trữ các giá trị số thực (có phần thập phân). Có 2 kiểu số thực:

### float

- Kích thước: 4 byte (32 bit)
- Độ chính xác: Khoảng 6-7 chữ số thập phân
- Sử dụng: Dùng khi không yêu cầu độ chính xác cao hoặc cần tiết kiệm bộ nhớ hơn double.
#### Ví dụ:
    float pi = 3.14159f; 
(Chú ý: Số float cần có hậu tố f)
### double

- Kích thước: 8 byte (64 bit)
- Độ chính xác: Khoảng 15 chữ số thập phân
- Sử dụng: Dùng phổ biến trong tính toán có yêu cầu độ chính xác cao.
#### Ví dụ:
    double e = 2.718281828459;
Lưu ý: Do bản chất của số thực (floating-point), các phép tính với float và double có thể gặp vấn đề về độ chính xác, đặc biệt là khi so sánh các giá trị rất nhỏ.

## C. Kiểu ký tự (Character Type)
### char
- Kích thước: 2 byte (16 bit)
- Phạm vi giá trị: Dùng mã Unicode để biểu diễn ký tự, có thể biểu diễn các ký tự từ '\u0000' đến '\uffff' (tức là từ 0 đến 65,535).
- Sử dụng: Lưu trữ một ký tự đơn lẻ, chẳng hạn chữ cái, chữ số hoặc ký tự đặc biệt.
#### Ví dụ:
    char letter = 'A';
Mã Unicode giúp char có thể biểu diễn được các ký tự của nhiều ngôn ngữ khác nhau, không chỉ các ký tự ASCII (chữ cái, số, dấu câu, v.v.).

## D. Kiểu luận lý (Boolean Type)
### boolean
- Kích thước: Không xác định cụ thể (thông thường 1 bit)
- Giá trị: Chỉ có hai giá trị true hoặc false
- Sử dụng: Dùng cho các điều kiện logic và kiểm tra đúng/sai. Là kiểu dữ liệu quan trọng trong các biểu thức điều kiện như if, while, và for.
#### Ví dụ:
    boolean isJavaFun = true;
Lưu ý: Không giống các ngôn ngữ khác, trong Java, boolean không được dùng để đại diện cho số 0 và 1. Điều này giúp tránh sai sót khi so sánh các điều kiện và biểu thức logic.


## 2. Kiểu dữ liệu đối tượng (Reference Types)
   - String: Chuỗi ký tự, ví dụ "Hello, World!". Đây không phải là kiểu nguyên thủy nhưng rất hay dùng.
   - Array: Mảng, dùng để lưu trữ nhiều giá trị cùng kiểu, ví dụ: [1, 2, 3].
   - Classes: Java là ngôn ngữ hướng đối tượng, nên bạn có thể tạo ra các lớp (class) với các thuộc tính và phương thức riêng. Các lớp tự tạo này cũng được xem là một kiểu dữ liệu.
# 2. Biến là gì? Cách khai báo biến
   Biến là “chiếc hộp” mà bạn tạo ra trong chương trình để lưu trữ dữ liệu, giúp bạn có thể sử dụng và truy cập dữ liệu đó bất cứ lúc nào.

Cách khai báo biến
Cú pháp khai báo biến: kiểu_dữ_liệu tên_biến = giá_trị;

#### Ví dụ:
    int age = 20;           // Khai báo biến nguyên kiểu int
    double pi = 3.14159;    // Khai báo biến số thực kiểu double
    String name = "Alice";  // Khai báo biến chuỗi kiểu String
#### Bạn có thể khai báo biến mà không cần gán giá trị ngay:

    int count;              // Chỉ khai báo biến count, chưa gán giá trị
    count = 5;              // Gán giá trị sau đó
# 3. Quy định đặt tên biến trong lập trình và 2 quy tắc chuẩn hóa về Coding Convention
   Đặt tên biến là một kỹ năng cần thiết để viết mã sạch và dễ đọc. Đặt tên biến sao cho rõ nghĩa sẽ giúp bạn (và người khác) dễ hiểu mã nguồn hơn. Có một số quy định phổ biến khi đặt tên biến:

#### Quy tắc đặt tên biến
   - Tên biến chỉ bao gồm chữ cái (A-Z, a-z), chữ số (0-9), và dấu gạch dưới (_).
   - Tên biến không được bắt đầu bằng số (ví dụ: 2count là không hợp lệ).
   - Không sử dụng từ khóa (keywords) của Java như class, public, void, int, v.v., làm tên biến.
   - Cẩn thận với chữ hoa và thường – age và Age là hai biến khác nhau.
#### 2 Quy tắc chuẩn hóa về Coding Convention
- Camel Case: Dùng camelCase cho tên biến và tên hàm. Camel là lạc đà nên tên biến sẽ giống phần lưng của chú lạc đà. Giông Quy tắc này bắt đầu từ chữ thường, còn các từ tiếp theo sẽ viết hoa chữ cái đầu.
Ví dụ: firstName, totalScore, isAvailable.
- Biến phải rõ nghĩa: Tên biến phải diễn tả được mục đích của nó. Tránh đặt tên biến vô nghĩa như a, b, x1, tmp nếu có thể.
Thay vì int n = 20;, hãy đặt int maxUserCount = 20; để rõ ràng rằng biến này dùng cho số lượng người dùng tối đa.
# Tóm tắt
- Kiểu dữ liệu là cách máy tính hiểu và quản lý dữ liệu.
- Biến là "chiếc hộp" chứa dữ liệu, có thể khai báo và sử dụng để lưu trữ các giá trị.
- Quy tắc đặt tên biến: Nên tuân theo chuẩn Camel Case và tên biến cần có ý nghĩa rõ ràng.
#### Vậy là bạn đã có cái nhìn cơ bản về kiểu dữ liệu, cách khai báo biến, và quy tắc đặt tên biến trong lập trình Java! Giờ bạn chỉ cần ghi nhớ và luyên tập theo quy tắc này thôi