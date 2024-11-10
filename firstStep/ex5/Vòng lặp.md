

### 1. Java Loops (Vòng lặp `For`, `While`, `Do-While`)

Trong lập trình, vòng lặp giống như khi bạn nhờ máy tính lặp lại một công việc nhiều lần. Nếu bạn muốn "đếm từ 1 đến 10" hoặc "làm điều gì đó 100 lần," thì vòng lặp chính là trợ thủ đắc lực để giúp bạn làm điều đó mà không cần viết lại cùng một đoạn mã đến 100 lần.

Java có ba loại vòng lặp chính: `for`, `while`, và `do-while`. Mỗi loại có cách dùng riêng, và chúng đều giúp bạn "làm đi làm lại" một nhiệm vụ nào đó. Hãy cùng khám phá nào!

#### a) Vòng lặp `for`
Vòng lặp `for` giống như việc bạn lập kế hoạch "chính xác" về số lần muốn lặp. Bạn quy định từ đầu rằng: “Đếm từ 1 đến 10 và kết thúc!”. `for` cực kỳ phù hợp khi bạn biết chính xác số lần lặp.

Cú pháp:
```java
for (khởi_tạo; điều_kiện; cập_nhật) {
    // Thực hiện công việc trong vòng lặp
}
```

Ví dụ:
```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Lặp lần thứ: " + i);
}
```
> **Giải thích**: `int i = 1` khởi tạo biến đếm `i` bằng 1. Vòng lặp sẽ tiếp tục khi `i <= 5`, và sau mỗi lần lặp, `i++` tăng `i` lên 1. Kết quả là chương trình sẽ in ra "Lặp lần thứ: 1" cho đến "Lặp lần thứ: 5".

#### b) Vòng lặp `while`
`while` giống như việc bạn nói: "Cứ lặp lại khi nào điều kiện còn đúng." Với `while`, chương trình sẽ kiểm tra điều kiện **trước** mỗi lần lặp. Nếu điều kiện sai ngay từ đầu, thì `while` sẽ... lờ nó đi luôn.

Cú pháp:
```java
while (điều_kiện) {
    // Thực hiện công việc trong vòng lặp
}
```

Ví dụ:
```java
int count = 1;
while (count <= 5) {
    System.out.println("Lặp lần thứ: " + count);
    count++;
}
```
> **Giải thích**: Ở đây, khi `count` vẫn nhỏ hơn hoặc bằng 5, vòng lặp sẽ in ra số lần lặp. Sau đó, `count++` tăng `count` lên 1 cho đến khi điều kiện sai và vòng lặp dừng lại.

#### c) Vòng lặp `do-while`
Vòng lặp `do-while` giống như câu nói: “Cứ làm trước rồi tính sau!”. `do-while` đảm bảo rằng vòng lặp sẽ thực hiện **ít nhất một lần** trước khi kiểm tra điều kiện. Đây là lựa chọn khi bạn muốn thực hiện vòng lặp ít nhất một lần, bất kể điều kiện ban đầu là gì.

Cú pháp:
```java
do {
    // Thực hiện công việc trong vòng lặp
} while (điều_kiện);
```

Ví dụ:
```java
int count = 1;
do {
    System.out.println("Lặp lần thứ: " + count);
    count++;
} while (count <= 5);
```
> **Giải thích**: `do-while` sẽ in ra "Lặp lần thứ: 1" và tiếp tục cho đến khi `count` lớn hơn 5. Khác với `while`, `do-while` sẽ luôn chạy ít nhất một lần, ngay cả khi điều kiện sai ngay từ đầu.

---

### 2. Từ khóa `break` và `continue`
Khi làm việc với vòng lặp, có lúc bạn sẽ muốn… "ngắt" hoặc "nhảy qua" một vòng lặp nào đó. Đó là lúc `break` và `continue` phát huy tác dụng!

#### Từ khóa `break`
`break` là cách bạn nói với vòng lặp: “Dừng lại! Hãy kết thúc ngay lập tức!” Khi gặp `break`, Java sẽ kết thúc vòng lặp tại vị trí hiện tại và "thoát" ra khỏi vòng lặp đó.

Cú pháp sử dụng `break`:
```java
for (int i = 1; i <= 10; i++) {
    if (i == 5) {
        break; // Dừng vòng lặp khi i đạt giá trị 5
    }
    System.out.println("Giá trị i: " + i);
}
```
> **Giải thích**: Vòng lặp sẽ in ra giá trị của `i` từ 1 đến 4, nhưng khi `i` bằng 5, `break` sẽ ngắt vòng lặp và không in ra gì thêm.

#### Từ khóa `continue`
`continue` giống như nói: “Bỏ qua lần này đi! Chạy tiếp vòng sau nhé!” Khi gặp `continue`, Java sẽ bỏ qua phần mã còn lại trong vòng lặp và **nhảy ngay sang lần lặp tiếp theo**.

Cú pháp sử dụng `continue`:
```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue; // Bỏ qua lần lặp khi i là 3
    }
    System.out.println("Giá trị i: " + i);
}
```
> **Giải thích**: Khi `i` là 3, `continue` sẽ khiến vòng lặp bỏ qua và không in ra giá trị 3. Kết quả là in ra các giá trị `1, 2, 4, 5` mà không có 3.

---

### Tóm lại

Với các vòng lặp và từ khóa `break`/`continue`, bạn sẽ có thể “quay vòng” trong chương trình của mình một cách thông minh. Hãy thử thực hành để nắm chắc cách sử dụng nhé vì bạn sẽ dungf nó rất nhiều đó !