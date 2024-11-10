

### 1. String là gì?

**String** là kiểu dữ liệu mà các lập trình viên rất yêu thích khi muốn… nói chuyện với máy tính! Nó là "chuỗi ký tự" – hiểu đơn giản là những đoạn văn bản, câu chữ từ vài ký tự đến nguyên cả cuốn tiểu thuyết. Bạn đã từng viết "Hello, World!" trong chương trình đầu tiên của mình nên bạn đã dùng `String` rồi đấy!

Trong Java, `String` là **immutable** – tức là không thể thay đổi sau khi đã tạo. Điều này có nghĩa là, mỗi lần bạn “chỉnh sửa” chuỗi, Java sẽ lén tạo ra một chuỗi mới và để lại chuỗi cũ trong bộ nhớ. Vậy nên nếu bạn cần thao tác nhiều với chuỗi, hãy cẩn thận để không biến bộ nhớ thành… bãi chiến trường nhé!

Ví dụ tạo `String`:
```java
String greeting = "Hello, Java!";
```

---

### 2. Các phương thức cơ bản làm việc với String

Dưới đây là bộ sưu tập các chiêu thức cực kỳ hữu ích khi bạn cần "biến hóa" với `String` trong Java. Hãy cùng xem qua từng chiêu nhé!

#### a) `length()`
Giống như đếm số kí tự trong câu, `length()` cho bạn biết độ dài của chuỗi.

```java
String message = "Hello, Java!";
int length = message.length(); // Kết quả: 11
```
> *"Hello, Java!"* có 11 ký tự, đếm cả dấu cách và dấu chấm than nhé!

#### b) `charAt(int index)`
Hàm `charAt` giúp bạn lấy ra từng ký tự trong chuỗi. Cần ký tự ở vị trí nào, cứ gọi `charAt(index)` là được. Nhớ rằng vị trí bắt đầu từ 0 nhé!

```java
String name = "Alice";
char firstChar = name.charAt(0); // Kết quả: 'A'
```
> Cần chữ "A"? Cứ nhờ `charAt(0)`, vì Java đếm từ 0, không phải từ 1!
##### [Remind] Cái gì quan trọng cần nhắc lại 3 lần `charAt(0)` vị trí bắt đầu từ 0 nhé!
#### c) `substring(int beginIndex, int endIndex)`
Muốn cắt một đoạn từ chuỗi? `substring` sẽ giúp bạn lấy phần bạn cần từ `beginIndex` đến `endIndex` (nhưng không tính `endIndex` đâu nha). Nó cũng bắt đầu từ vị trí 0 nhé

```java
String text = "Hello, world!";
String sub = text.substring(0, 5); // Kết quả: "Hello"
```
> *"Hello"* tách ra từ *"Hello, world!"* đấy!

#### d) `contains(CharSequence s)`
Muốn biết chuỗi có "chứa" đoạn nào không? `contains` là câu hàm kiểm tra xem có chuỗi con bạn muốn tìm không.

```java
String text = "Hello, world!";
boolean hasWorld = text.contains("world"); // Kết quả: true
```
> *"world"* nằm trong *"Hello, world!"* nên kết quả là *true*.

#### e) `toLowerCase()` và `toUpperCase()`
Biến chuỗi thành chữ thường hoặc chữ hoa! Dùng khi bạn muốn đồng nhất cách viết (hoặc hét thật to!).

```java
String name = "Alice";
String lowerName = name.toLowerCase(); // Kết quả: "alice"
String upperName = name.toUpperCase(); // Kết quả: "ALICE"
```

#### f) `trim()`
Chuỗi của bạn có bị "dính bụi" với những dấu cách thừa đầu đuôi không? `trim` sẽ giúp bạn "dọn dẹp sạch sẽ".

```java
String messyText = "   Hello   ";
String cleanText = messyText.trim(); // Kết quả: "Hello"
```
> Gọn gàng, tinh tươm rồi nhé!

#### g) `replace(CharSequence target, CharSequence replacement)`
Khi bạn muốn thay một đoạn nào đó trong chuỗi bằng một đoạn khác, `replace` sẽ giúp bạn đổi "vũ khí" nhanh gọn.

```java
String text = "Hello, world!";
String newText = text.replace("world", "Java"); // Kết quả: "Hello, Java!"
```
> *"world"* đã biến thành *"Java"*!

#### h) `equals(Object anotherString)` và `equalsIgnoreCase(String anotherString)`
So sánh chuỗi với nhau. `equals` để kiểm tra chính xác từng ký tự, `equalsIgnoreCase` thì… thoải mái hơn, không cần quan tâm chữ hoa chữ thường.

```java
String name1 = "Alice";
String name2 = "alice";
boolean isEqual = name1.equals(name2); // Kết quả: false
boolean isEqualIgnoreCase = name1.equalsIgnoreCase(name2); // Kết quả: true
```
> `equalsIgnoreCase` giống như việc bỏ qua câu nệ chữ hoa, chữ thường ấy!

#### i) `indexOf(String str)`
Tìm xem chuỗi con xuất hiện lần đầu ở đâu trong chuỗi chính. Nếu không có thì trả về `-1`.

```java
String text = "Hello, world!";
int index = text.indexOf("world"); // Kết quả: 7
```
> `"world"` bắt đầu từ vị trí số 7!

#### j) `isEmpty()`
Muốn kiểm tra xem chuỗi có trống không (tức là không có ký tự nào), `isEmpty` sẽ giúp bạn.

```java
String emptyText = "";
boolean isEmpty = emptyText.isEmpty(); // Kết quả: true
```
> Chuỗi không có gì, thì tất nhiên là *true* rồi!

---

### Tóm lại

Vậy là bạn đã có những vũ khí cơ bản với `String` trong Java! Những phương thức này sẽ giúp bạn xử lý chuỗi nhanh chóng và linh hoạt hơn rất nhiều. Chúc bạn vui vẻ với `String` và nhớ là… đừng ngại thử tìm hiểu thêm các hàm mới của `String` nhé! 😄