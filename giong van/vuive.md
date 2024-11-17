# Giọng văn: Vui vẻ, thân thiện
### **Hướng dẫn cho người mới bắt đầu: Vòng lặp trong Java và từ khóa Break/Continue**



## **1. Vòng lặp trong Java – Phép màu cho việc lặp đi lặp lại!**

Bạn đã bao giờ muốn máy tính làm gì đó nhiều lần mà không phải gõ đi gõ lại chưa? Ví dụ như đếm số, kiểm tra từng phần tử trong một danh sách dài, hay in ra lời nhắn yêu thương 100 lần? Đây chính là nơi vòng lặp phát huy công dụng tuyệt vời!

### **1.1. Vòng lặp `for` – Cỗ máy đếm cực kỳ chính xác!**
Vòng lặp `for` giống như một người bạn thích sự chính xác và trật tự. Khi bạn biết mình cần lặp bao nhiêu lần, hãy dùng `for`.

Cú pháp cơ bản trông thế này:
```java
for (int i = 0; i < 10; i++) {
    System.out.println("Đây là lần lặp thứ: " + i);
}
```
- **`int i = 0`**: Bắt đầu từ số 0.
- **`i < 10`**: Lặp khi **i** nhỏ hơn 10.
- **`i++`**: Sau mỗi lần lặp, tăng **i** lên 1.

**Ví dụ vui**: In lời tỏ tình 5 lần.
```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Anh thích em lần thứ " + i);
}
```

---

### **1.2. Vòng lặp `while` – Người bạn kiên nhẫn, làm khi còn điều kiện!**
Vòng lặp `while` là người bạn hơi "nguyên tắc": nó chỉ làm khi điều kiện còn đúng.

Cú pháp trông như sau:
```java
int count = 0;
while (count < 5) {
    System.out.println("Lặp lần thứ: " + count);
    count++;
}
```
Ở đây, vòng lặp kiểm tra **count < 5** trước khi chạy. Nếu đúng, nó tiếp tục. Sai là... thôi, không làm nữa!

**Ví dụ vui**: Đếm tiền trong túi (giả sử có 10k).
```java
int tien = 10;
while (tien > 0) {
    System.out.println("Còn " + tien + " nghìn trong túi!");
    tien -= 2; // Mỗi lần tiêu 2k
}
```

---

### **1.3. Vòng lặp `do-while` – Làm trước, hỏi sau!**
Nếu `while` là người nguyên tắc, thì `do-while` là kiểu "thôi cứ làm cái đã, tính sau!".

Cú pháp:
```java
int count = 0;
do {
    System.out.println("Lặp lần thứ: " + count);
    count++;
} while (count < 5);
```
Khác biệt là **`do-while` chạy ít nhất một lần**, ngay cả khi điều kiện sai.

**Ví dụ vui**: Nếm thử món ăn dù hơi nghi ngờ.
```java
boolean ngonQua = false;
do {
    System.out.println("Nếm thử món này cái đã!");
    ngonQua = true; // Ai ngờ, ngon thật!
} while (!ngonQua);
```

---

## **2. Từ khóa `break` và `continue` – Quyền năng làm chủ vòng lặp!**

Khi dùng vòng lặp, đôi lúc bạn muốn "bẻ lái" theo ý mình. Hai từ khóa **`break`** và **`continue`** sẽ giúp bạn:

### **2.1. `break` – Dừng vòng lặp ngay lập tức**
Khi gặp **`break`**, Java sẽ nói: *"Thôi, dừng ở đây thôi, không lặp nữa!"*.

Ví dụ: Dừng lại khi tìm thấy số chẵn đầu tiên trong dãy số.
```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 == 0) {
        System.out.println("Số chẵn đầu tiên là: " + i);
        break; // Không cần kiểm tra thêm!
    }
}
```

---

### **2.2. `continue` – Bỏ qua, nhưng không dừng hẳn!**
Ngược lại, **`continue`** giống như nói: *"Bỏ qua lần này, lặp tiếp lần sau nhé!"*.

Ví dụ: Bỏ qua số chia hết cho 3, in các số khác.
```java
for (int i = 1; i <= 10; i++) {
    if (i % 3 == 0) {
        continue; // Bỏ qua các số chia hết cho 3
    }
    System.out.println(i);
}
```

---

## **Kết luận**
Vòng lặp và từ khóa `break`/`continue` là những công cụ mạnh mẽ, giúp bạn tối ưu hóa chương trình và xử lý dữ liệu dễ dàng. Hãy thực hành để làm quen và áp dụng vào những bài toán thú vị nhé! 🚀

*Bây giờ thì... code thôi nào! 🎉*