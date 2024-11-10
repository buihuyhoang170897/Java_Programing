### Array là gì?

**Array** trong Java giống như một "khay trứng" với nhiều ô (hay còn gọi là "phần tử") giúp bạn lưu trữ các giá trị cùng loại. Nếu mỗi ô trứng trong khay đều chứa một quả trứng, thì trong `Array`, mỗi ô (index) sẽ chứa một giá trị nhất định. Điểm đặc biệt của `Array` là **kích thước cố định** – khi đã quyết định số lượng ô (kích thước) ban đầu, bạn không thể thay đổi nó nữa.

> Hãy tưởng tượng bạn có một `Array` chứa 10 phần tử, tức là giống như bạn có một khay trứng 10 ô. Nếu muốn thêm quả trứng thứ 11 thì… hơi tiếc là bạn không thể nhét thêm vào được, trừ khi tạo hẳn một khay trứng lớn hơn!

### Cú pháp khai báo Array

Bạn cần khai báo `Array` bằng cách xác định loại dữ liệu và số lượng phần tử. Dưới đây là cú pháp cơ bản:

```java
// Cách khai báo 1
int[] numbers = new int[5]; // Một mảng chứa 5 số nguyên

// Cách khai báo 2 (khai báo và khởi tạo cùng lúc)
int[] numbers = {1, 2, 3, 4, 5}; // Mảng chứa các số cụ thể
```

> Ở cách đầu tiên, bạn tạo một `Array` rỗng có 5 ô, tất cả đều là số 0 vì chưa gán giá trị gì. Ở cách thứ hai, bạn tạo `Array` với các số đã định sẵn.

### Truy cập và thay đổi phần tử trong Array

Trong `Array`, bạn có thể truy cập và thay đổi giá trị bằng cách chỉ định **vị trí (index)** của phần tử đó. Lưu ý rằng **index** bắt đầu từ 0 chứ không phải 1. Điều này có nghĩa là phần tử đầu tiên sẽ ở vị trí `0`, phần tử thứ hai là `1`, và cứ tiếp tục.

Ví dụ:
```java
int[] numbers = {1, 2, 3, 4, 5};
System.out.println(numbers[0]); // In ra 1, phần tử đầu tiên
System.out.println(numbers[4]); // In ra 5, phần tử cuối cùng
```

Bạn cũng có thể thay đổi giá trị của từng phần tử:

```java
numbers[0] = 10; // Đổi phần tử đầu tiên thành 10
numbers[4] = 50; // Đổi phần tử cuối cùng thành 50
System.out.println(numbers[0]); // In ra 10
System.out.println(numbers[4]); // In ra 50
```

### Một số phương pháp “đi chơi khắp mảng”!

Để xem qua tất cả phần tử trong `Array`, chúng ta có hai cách phổ biến:

#### a) Sử dụng vòng lặp `for` truyền thống

Vòng lặp `for` cho phép bạn lặp qua từng phần tử bằng cách dùng chỉ số (index):

```java
int[] numbers = {1, 2, 3, 4, 5};
for (int i = 0; i < numbers.length; i++) {
    System.out.println("Phần tử ở vị trí " + i + " là " + numbers[i]);
}
```

> **Giải thích**: `numbers.length` là độ dài của mảng, cho bạn biết số lượng phần tử trong mảng. Ở đây, vòng lặp `for` sẽ chạy từ `0` đến `4`, giúp bạn duyệt qua từng phần tử của `Array`.

#### b) Sử dụng vòng lặp `for-each`

Vòng lặp `for-each` là cách ngắn gọn để duyệt qua tất cả các phần tử mà không cần quan tâm đến chỉ số:

```java
int[] numbers = {1, 2, 3, 4, 5};
for (int num : numbers) {
    System.out.println("Phần tử: " + num);
}
```

> **Giải thích**: Cứ mỗi lần lặp, `num` sẽ nhận giá trị của từng phần tử trong `Array`. Đây là cách đọc `Array` rất tiện lợi!

### Một số lưu ý vui vẻ khi dùng Array

1. **Không được mở rộng**: `Array` cố định, không thêm hay bớt phần tử sau khi đã khai báo. Nếu bạn cần một `Array` lớn hơn, hãy tạo `Array` mới!

2. **IndexOutOfBoundsException**: Lỗi này xảy ra nếu bạn cố truy cập phần tử ngoài phạm vi `Array`. Ví dụ:
   ```java
   int[] numbers = {1, 2, 3};
   System.out.println(numbers[5]); // Lỗi: ArrayIndexOutOfBoundsException!
   ```

3. **Độ dài cố định**: `Array` có `.length` – số lượng phần tử trong mảng, dùng để kiểm tra kích thước của `Array`. Đây là điểm khác biệt so với các `List` (có `.size()`).

### Các phương thức và thao tác cơ bản với Array

Dưới đây là một số thao tác bạn thường làm với `Array`, từ cách truy cập phần tử, duyệt qua `Array`, đến tìm độ dài và nhiều hơn nữa!

#### 1. Truy cập phần tử trong Array

Bạn có thể truy cập vào từng phần tử trong `Array` bằng cách gọi `array[index]`. Chỉ cần biết số thứ tự là bạn sẽ biết phần tử đó chứa giá trị gì.

Ví dụ:
```java
int[] scores = {90, 85, 70, 95, 100};
System.out.println(scores[0]);  // In ra 90 - phần tử đầu tiên
System.out.println(scores[3]);  // In ra 95 - phần tử thứ 4
```

> **Lưu ý**: Nếu bạn thử `scores[5]` (vị trí thứ 6) thì sẽ gặp lỗi, vì `Array` này chỉ có 5 phần tử.

#### 2. Thay đổi giá trị của phần tử

Bạn có thể cập nhật giá trị của một phần tử trong `Array` bằng cách chỉ định `index` và gán giá trị mới cho nó.

Ví dụ:
```java
int[] scores = {90, 85, 70, 95, 100};
scores[2] = 75; // Thay đổi phần tử thứ 3 từ 70 thành 75
System.out.println(scores[2]); // In ra 75
```

> **Giải thích**: `scores[2] = 75;` cập nhật giá trị phần tử thứ 3 trong `Array` lên 75.

#### 3. Duyệt qua tất cả phần tử trong Array

Khi bạn muốn in ra hoặc thao tác với tất cả phần tử, dùng **vòng lặp** là cách nhanh nhất. Có hai cách duyệt `Array` phổ biến: dùng vòng lặp `for` và `for-each`.

- **Vòng lặp `for`**:

  ```java
  int[] scores = {90, 85, 75, 95, 100};
  for (int i = 0; i < scores.length; i++) {
      System.out.println("Điểm số tại vị trí " + i + " là: " + scores[i]);
  }
  ```
  > **Giải thích**: Vòng lặp `for` sẽ lặp từ `i = 0` đến `i = 4` (bằng `scores.length - 1`). Mỗi lần lặp sẽ in ra giá trị tại `scores[i]`.

- **Vòng lặp `for-each`**:

  ```java
  for (int score : scores) {
      System.out.println("Điểm số: " + score);
  }
  ```
  > **Giải thích**: Vòng lặp `for-each` giúp bạn duyệt qua tất cả phần tử mà không cần dùng `index`. Cứ mỗi lần lặp, `score` sẽ lấy giá trị của phần tử kế tiếp trong `Array`.

#### 4. Lấy độ dài của Array

Bạn có thể kiểm tra độ dài của `Array` (số phần tử) bằng thuộc tính `.length`. Độ dài này sẽ giúp bạn không gặp lỗi “vượt ranh giới” khi thao tác với `Array`.

Ví dụ:
```java
int[] scores = {90, 85, 75, 95, 100};
System.out.println("Số phần tử trong mảng: " + scores.length); // In ra 5
```

> **Giải thích**: `scores.length` trả về 5, nghĩa là `Array` này có 5 phần tử.

#### 5. Tìm giá trị lớn nhất hoặc nhỏ nhất trong Array (Cách thủ công)

Để tìm giá trị lớn nhất hoặc nhỏ nhất, bạn chỉ cần duyệt qua `Array` và so sánh từng phần tử để giữ lại giá trị mong muốn.

Ví dụ:
```java
int[] scores = {90, 85, 75, 95, 100};
int max = scores[0];  // Giả định phần tử đầu tiên là lớn nhất

for (int score : scores) {
    if (score > max) {
        max = score;
    }
}

System.out.println("Điểm số cao nhất là: " + max); // In ra 100
```

> **Giải thích**: Đầu tiên, ta giả định phần tử đầu tiên (`scores[0]`) là lớn nhất. Sau đó, duyệt qua từng `score` trong `Array`. Nếu tìm thấy `score` lớn hơn `max`, ta cập nhật `max` bằng `score` đó.

#### 6. Tạo mảng nhiều chiều (Array đa chiều)

Một `Array` nhiều chiều giống như một ma trận trong toán học, là “mảng của các mảng”. Mỗi hàng và mỗi cột đều có `index` riêng, giúp bạn lưu trữ dữ liệu theo dạng bảng.

Ví dụ:
```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
System.out.println(matrix[1][2]); // In ra 6
```

> **Giải thích**: `matrix[1][2]` đại diện cho phần tử tại hàng 2, cột 3 (vì `index` bắt đầu từ 0). Vậy nên kết quả là 6.

---

### Tóm lại về Array

- **Khai báo**: `Array` giúp bạn tạo một mảng chứa nhiều phần tử, nhưng kích thước phải cố định từ khi khai báo.
- **Truy cập bằng chỉ số**: Bạn có thể truy cập phần tử thông qua chỉ số, bắt đầu từ `0`.
- **Vòng lặp**: `for` và `for-each` là những cách nhanh nhất để duyệt qua `Array`.
- **Không thêm hay bớt được**: Nếu cần thêm phần tử, hãy chuyển sang dùng `List`.

`Array` là cấu trúc dữ liệu đơn giản, hiệu quả, và nhanh chóng – cực kỳ hữu ích khi bạn cần lưu trữ và truy cập một lượng lớn dữ liệu mà không cần thay đổi kích thước. Hãy bắt đầu khám phá `Array` và sử dụng nó một cách thông minh trong chương trình của mình nhé! 😄