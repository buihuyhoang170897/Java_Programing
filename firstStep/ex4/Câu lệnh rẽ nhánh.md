

### 1. Cấu trúc `If` và `If/Else` (ElseIf)

Cấu trúc `if` và `if/else` là kiểu như bạn đang phân vân: "Nếu điều này đúng thì làm gì? Nếu không thì sao?" Đây là một trong những công cụ giúp bạn ra quyết định khi lập trình, kiểu như bạn đang chơi trò **đoán đúng/sai** với máy tính.

#### `if`
Cấu trúc `if` đơn giản là kiểm tra một điều kiện. Nếu điều kiện **đúng** (`true`), đoạn mã bên trong `if` sẽ được thực hiện. Nếu **sai** (`false`), Java sẽ lướt qua và bỏ qua phần mã đó như chưa từng tồn tại.

Cú pháp:
```java
if (điều kiện) {
    // Việc cần làm nếu điều kiện đúng
}
```

Ví dụ:
```java
int temperature = 30;
if (temperature > 25) {
    System.out.println("Trời nóng quá, đi uống trà sữa thôi!");
}
```
> **Giải thích**: Nếu nhiệt độ lớn hơn 25 độ, bạn sẽ được phép “đi uống trà sữa”!

#### `if/else`
Cấu trúc `if/else` mở rộng ra một chút. Nó sẽ kiểm tra điều kiện `if` trước, nếu **đúng** thì thực hiện lệnh trong `if`, nếu **sai** thì sẽ nhảy vào `else` để thực hiện phần khác.

Cú pháp:
```java
if (điều kiện) {
    // Việc cần làm nếu điều kiện đúng
} else {
    // Việc cần làm nếu điều kiện sai
}
```

Ví dụ:
```java
int temperature = 20;
if (temperature > 30) {
    System.out.println("Trời nóng quá, đi uống trà sữa thôi!");
} else {
    System.out.println("Trời mát mà, khỏi cần uống trà sữa!");
}
```
> **Giải thích**: Nếu nhiệt độ không quá 30 độ, thì bạn cần 1 chiếc điều hòa và khỏi cần đi đâu cho mệt!

#### `if/else if/else`
Khi có nhiều điều kiện để kiểm tra, bạn có thể dùng `else if` để thêm vào các lựa chọn khác. Cứ như bạn đang lập kế hoạch: "Nếu không phải thế này, thì có phải thế kia không? Nếu cũng không phải, thì là gì nhỉ?"

Cú pháp:
```java
if (điều kiện 1) {
    // Thực hiện khi điều kiện 1 đúng
} else if (điều kiện 2) {
    // Thực hiện khi điều kiện 2 đúng
} else {
    // Thực hiện khi tất cả các điều kiện đều sai
}
```

Ví dụ:
```java
int temperature = 15;
if (temperature > 25) {
    System.out.println("Trời nóng quá, đi uống trà sữa thôi!");
} else if (temperature > 15) {
    System.out.println("Thời tiết tuyệt vời, đi dạo chơi thôi!");
} else {
    System.out.println("Lạnh quá rồi, ở nhà uống cà phê nóng vậy!");
}
```
> **Giải thích**: Bạn có một chuỗi lựa chọn, phụ thuộc vào nhiệt độ mà chương trình sẽ "tư vấn" hoạt động phù hợp.

---

### 2. Cấu trúc `Switch-Case`

Khi bạn có quá nhiều trường hợp để kiểm tra bằng `if/else if`, `switch-case` xuất hiện như một người hùng giúp mã ngắn gọn hơn và dễ đọc hơn. Đây là cấu trúc bạn dùng khi có nhiều trường hợp, và mỗi trường hợp có một "hành động" khác nhau.

#### Cú pháp của `switch-case`
```java
switch (biểu_thức) {
    case giá_trị_1:
        // Việc cần làm nếu biểu thức có giá trị là giá_trị_1
        break;
    case giá_trị_2:
        // Việc cần làm nếu biểu thức có giá trị là giá_trị_2
        break;
    ...
    default:
        // Việc cần làm nếu không có giá trị nào khớp
}
```

> **Chú ý**: `break` dùng để kết thúc từng `case`, ngăn chương trình chạy tiếp các `case` khác dù không phù hợp. Nếu quên `break`, chương trình sẽ "lọt" xuống các `case` tiếp theo, gây ra những kết quả khó hiểu!

#### Ví dụ `switch-case`
Hãy tưởng tượng bạn vào quán cafe và đang chọn thức uống, nhưng tùy chọn có vẻ hơi nhiều. `switch-case` sẽ là cách nhanh nhất để xử lý!

```java
String drink = "trà sữa";

switch (drink) {
    case "trà sữa":
        System.out.println("Bạn đã chọn trà sữa!");
        break;
    case "cà phê":
        System.out.println("Bạn đã chọn cà phê!");
        break;
    case "nước ép":
        System.out.println("Bạn đã chọn nước ép!");
        break;
    default:
        System.out.println("Xin lỗi, chúng tôi không có món này!");
}
```
> **Giải thích**: Chương trình sẽ kiểm tra giá trị của `drink`. Nếu là `"trà sữa"`, `"cà phê"`, hoặc `"nước ép"`, nó sẽ in ra món bạn chọn. Nếu không khớp với giá trị nào, `default` sẽ xử lý và thông báo món bạn chọn không có.

#### Khi nào nên dùng `switch-case`?
- Khi bạn có nhiều trường hợp cần kiểm tra, và mỗi trường hợp là một giá trị cụ thể.
- Khi bạn muốn mã ngắn gọn và dễ đọc hơn so với `if/else if`.

---

### Tóm lại

Vậy là chúng ta đã có hai "công cụ ra quyết định" cực hữu ích: `if/else` để xử lý các điều kiện đơn giản hoặc phức tạp, và `switch-case` để quản lý nhiều lựa chọn một cách ngắn gọn, rõ ràng hơn. Hãy thử thực hành với các cấu trúc này nhé!