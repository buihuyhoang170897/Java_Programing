### 1. Collections là gì? Các loại cơ bản

**Collections** trong Java là một “kho tàng” những cách để lưu trữ và quản lý dữ liệu nhiều phần tử, giúp bạn gom nhóm, sắp xếp, và tìm kiếm dữ liệu một cách dễ dàng. Hãy tưởng tượng bạn có một “hộp dụng cụ” chứa đủ loại đồ đạc – từ hộp nhỏ chứa từng cái đinh vít đến hộp lớn chứa đầy công cụ, và thậm chí có cả ngăn kéo phân loại mọi thứ. Đó chính là bộ **Collections** trong Java!

Java có ba loại `Collections` chính thường dùng:

1. **List** – “Danh sách có thứ tự”  
   Đây là kiểu danh sách có thứ tự, nghĩa là phần tử nào vào trước sẽ có thứ tự cụ thể, bạn có thể truy cập theo thứ tự đó. Các `List` thường dùng như `ArrayList`, `LinkedList`, giúp bạn lưu trữ các phần tử có thể lặp lại (giống như danh sách khách mời – có thể có người trùng tên!).

2. **Set** – “Tập hợp không trùng lặp”  
   Set giống như một hộp mà các phần tử không bao giờ trùng nhau, bất kể bạn thêm đi thêm lại bao nhiêu lần! `Set` cực kỳ hữu dụng khi bạn muốn lưu trữ dữ liệu duy nhất và không cần thứ tự cụ thể, như các số vé của hội chợ (không ai muốn trùng vé chứ!).

3. **Map** – “Bảng tra cứu”  
   Map giống như một cuốn từ điển, với “từ” (key) và “nghĩa” (value). Bạn có thể tìm “nghĩa” chỉ bằng cách nhập “từ.” Một Map sẽ cho phép bạn lưu trữ dữ liệu thành các cặp `key-value`, rất tiện khi cần lưu dữ liệu kiểu tra cứu nhanh (như tìm số điện thoại qua tên!).

### 2. Array, List, Map và các phương thức cơ bản

#### a) Array – “Mảng cố định”

**Array** là một cách đơn giản và hiệu quả để lưu trữ nhiều giá trị cùng loại, nhưng có một điều kiện là: kích thước của mảng phải được cố định ngay từ đầu. Nghĩa là khi đã tạo `array` với 10 phần tử, bạn không thể tự dưng thêm phần tử thứ 11 vào đó!

Ví dụ:
```java
int[] numbers = {1, 2, 3, 4, 5};
System.out.println(numbers[0]); // In ra phần tử đầu tiên: 1
```

Một số thao tác cơ bản với `Array`:
- **Truy cập phần tử**: `array[index]` – Lấy giá trị của phần tử tại `index`.
- **Duyệt qua mảng**: Dùng vòng lặp `for` hoặc `for-each`.

```java
for (int number : numbers) {
    System.out.println(number);
}
```

#### b) List – “Danh sách linh động”

`List` là phiên bản “linh động” hơn của `Array`. Với `List`, bạn không cần lo về kích thước, vì bạn có thể thêm, xóa phần tử tùy thích! `ArrayList` là một loại `List` rất hay dùng vì khả năng quản lý các phần tử một cách linh hoạt.

Ví dụ:
```java
import java.util.ArrayList;

List<String> fruits = new ArrayList<>();
fruits.add("Táo");
fruits.add("Cam");
fruits.add("Xoài");
System.out.println(fruits.get(0)); // In ra: "Táo"
```

Một số phương thức cơ bản của `List`:
- **add(element)**: Thêm một phần tử vào `List`.
- **get(index)**: Lấy phần tử tại vị trí `index`.
- **remove(index)**: Xóa phần tử tại vị trí `index`.
- **size()**: Trả về số phần tử trong `List`.

Ví dụ tiếp:
```java
fruits.add("Dứa");
System.out.println(fruits.size());  // Kết quả: 4
fruits.remove(1);                   // Xóa phần tử tại vị trí 1 ("Cam")
System.out.println(fruits);         // In ra: [Táo, Xoài, Dứa]
```

#### c) Map – “Từ điển của dữ liệu”

Map là một loại “danh bạ điện thoại” thông minh. Ở đây, mỗi `key` chỉ có một `value` tương ứng, và mỗi `key` phải là duy nhất (không có chuyện trùng `key`). `HashMap` là một loại `Map` phổ biến giúp bạn dễ dàng lưu trữ và truy xuất dữ liệu.

Ví dụ:
```java
import java.util.HashMap;

Map<String, String> phoneBook = new HashMap<>();
phoneBook.put("Alice", "0123456789");
phoneBook.put("Bob", "0987654321");
System.out.println(phoneBook.get("Alice")); // In ra: "0123456789"
```

Một số phương thức cơ bản của `Map`:
- **put(key, value)**: Thêm một cặp `key-value` vào `Map`.
- **get(key)**: Trả về `value` của `key` đã cho.
- **remove(key)**: Xóa cặp `key-value` theo `key`.
- **containsKey(key)**: Kiểm tra xem `Map` có chứa `key` này không.

Ví dụ tiếp:
```java
phoneBook.put("Charlie", "0111222333");
System.out.println(phoneBook.containsKey("Bob"));   // Kết quả: true
phoneBook.remove("Alice");                          // Xóa Alice khỏi danh bạ
System.out.println(phoneBook);                      // In ra: {Bob=0987654321, Charlie=0111222333}
```

---

### Tóm lại

- `Array` giống như một dãy ghế cố định, bạn đã xếp đủ ghế thì thôi, không thêm không bớt.
- `List` là danh sách linh động, muốn thêm bớt bao nhiêu cũng được.
- `Map` như cuốn từ điển, bạn tra cứu `value` thông qua `key`.

Với bộ sưu tập này, bạn đã có trong tay tất cả các công cụ lưu trữ và quản lý dữ liệu đa dạng, từ dãy số đến danh sách dài, và cả bảng tra cứu nhanh. Hãy thử áp dụng và khám phá những tiềm năng của `Collections` nhé! 😄