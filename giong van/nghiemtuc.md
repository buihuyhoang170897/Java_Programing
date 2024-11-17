# Giọng văn: Nghiêm túc

### **Hướng dẫn tổng hợp kiến thức: Vòng lặp và từ khóa trong Java**

Java cung cấp các công cụ mạnh mẽ để xử lý các tác vụ lặp lại, giúp lập trình viên tiết kiệm thời gian và tối ưu hóa chương trình. Bài viết này sẽ tổng hợp những kiến thức quan trọng nhất về vòng lặp trong Java (*Loops*) và hai từ khóa hữu ích **`break`** và **`continue`**.

---

## **1. Vòng lặp trong Java – Công cụ tái sử dụng hiệu quả**

Vòng lặp trong Java được sử dụng để thực thi một khối mã lệnh nhiều lần, dựa trên một điều kiện nhất định. Java hỗ trợ ba loại vòng lặp chính: **`for`**, **`while`**, và **`do-while`**.

### **1.1. Vòng lặp `for` – Lặp khi biết rõ số lần**
Vòng lặp `for` được sử dụng khi bạn biết trước số lần lặp cần thực hiện.

#### Cú pháp:
```java
for (khởi_tạo; điều_kiện; cập_nhật) {
    // Khối mã lệnh được thực thi
}
```
- **Khởi tạo**: Đặt giá trị ban đầu cho biến điều khiển.
- **Điều kiện**: Kiểm tra xem vòng lặp có tiếp tục không.
- **Cập nhật**: Thay đổi giá trị biến điều khiển sau mỗi lần lặp.

#### Ví dụ:
```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Lần lặp thứ: " + i);
}
```
Kết quả in ra:
```
Lần lặp thứ: 1  
Lần lặp thứ: 2  
Lần lặp thứ: 3  
Lần lặp thứ: 4  
Lần lặp thứ: 5  
```

---

### **1.2. Vòng lặp `while` – Lặp khi điều kiện đúng**
Vòng lặp `while` kiểm tra điều kiện trước mỗi lần lặp. Nó rất hữu ích khi bạn không biết trước số lần lặp, nhưng biết điều kiện cần để tiếp tục.

#### Cú pháp:
```java
while (điều_kiện) {
    // Khối mã lệnh được thực thi
}
```

#### Ví dụ:
```java
int count = 1;
while (count <= 5) {
    System.out.println("Lần lặp thứ: " + count);
    count++;
}
```
Kết quả tương tự như vòng lặp `for`, nhưng cách viết linh hoạt hơn.

---

### **1.3. Vòng lặp `do-while` – Lặp ít nhất một lần**
Khác với `while`, vòng lặp `do-while` luôn chạy ít nhất một lần, kể cả khi điều kiện sai ngay từ đầu, vì nó kiểm tra điều kiện **sau khi thực hiện khối mã**.

#### Cú pháp:
```java
do {
    // Khối mã lệnh được thực thi
} while (điều_kiện);
```

#### Ví dụ:
```java
int count = 1;
do {
    System.out.println("Lần lặp thứ: " + count);
    count++;
} while (count <= 5);
```
Kết quả tương tự, nhưng khác biệt ở chỗ `do-while` đảm bảo khối mã được thực hiện ít nhất một lần.

---

## **2. Từ khóa `break` và `continue` – Quyền kiểm soát vòng lặp**

Khi làm việc với vòng lặp, bạn có thể cần dừng vòng lặp đột ngột hoặc bỏ qua một số lần lặp nhất định. Đây là lúc hai từ khóa **`break`** và **`continue`** phát huy tác dụng.

### **2.1. Từ khóa `break` – Dừng vòng lặp ngay lập tức**
`break` được sử dụng để thoát khỏi vòng lặp, bất kể điều kiện còn đúng hay không.

#### Ví dụ:
Tìm số chẵn đầu tiên từ 1 đến 10:
```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 == 0) {
        System.out.println("Số chẵn đầu tiên là: " + i);
        break; // Thoát khỏi vòng lặp
    }
}
```
Kết quả:
```
Số chẵn đầu tiên là: 2
```

---

### **2.2. Từ khóa `continue` – Bỏ qua lần lặp hiện tại**
`continue` được dùng để bỏ qua khối mã còn lại trong vòng lặp và tiếp tục với lần lặp tiếp theo.

#### Ví dụ:
In tất cả các số từ 1 đến 10, nhưng bỏ qua số chia hết cho 3:
```java
for (int i = 1; i <= 10; i++) {
    if (i % 3 == 0) {
        continue; // Bỏ qua số chia hết cho 3
    }
    System.out.println(i);
}
```
Kết quả:
```
1  
2  
4  
5  
7  
8  
10  
```

---

## **So sánh giữa các vòng lặp**

| Đặc điểm           | `for`                        | `while`                  | `do-while`                 |
|--------------------|------------------------------|--------------------------|----------------------------|
| **Kiểm tra điều kiện** | Trước mỗi lần lặp            | Trước mỗi lần lặp         | Sau khi thực hiện khối mã  |
| **Số lần lặp tối thiểu** | Có thể là 0                  | Có thể là 0               | Ít nhất 1 lần              |
| **Sử dụng phổ biến**   | Khi biết rõ số lần lặp       | Khi không biết trước số lần | Khi cần thực thi ít nhất một lần |

---

## **Kết luận**

- **Vòng lặp `for`** phù hợp khi bạn biết rõ số lần lặp.
- **Vòng lặp `while`** thích hợp khi điều kiện là yếu tố quyết định.
- **Vòng lặp `do-while`** hữu ích khi bạn muốn đảm bảo khối mã chạy ít nhất một lần.
- **Từ khóa `break`** giúp dừng vòng lặp khi đạt được mục tiêu.
- **Từ khóa `continue`** giúp bỏ qua những lần lặp không cần thiết.

Hiểu rõ cách hoạt động và áp dụng chúng, bạn sẽ dễ dàng xử lý các bài toán phức tạp hơn trong lập trình Java. Hãy thử viết mã và khám phá những ứng dụng thú vị ngay hôm nay! 🚀