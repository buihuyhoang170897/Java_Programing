### **Cấu Trúc If và If/Else Trong Java: Mở Cửa Cho Logic**

Trong thế giới lập trình Java, **if** và **if/else** chính là những “kẻ phán xét” tối cao. Chúng giúp bạn kiểm tra mọi điều kiện để đưa ra quyết định: "Nếu đúng thì làm cái này, nếu sai thì làm cái kia". Đơn giản, dễ hiểu, nhưng cũng tiềm ẩn nhiều tình huống hài hước nếu bạn viết sai logic.

---

### **1. If Là Gì?**

Cấu trúc **if** giống như việc bạn đặt câu hỏi: "Nếu điều này đúng, thì tôi làm gì?". Nếu câu trả lời là “đúng” (true), đoạn mã trong khối **if** sẽ được thực hiện. Nếu “sai” (false), Java sẽ… phớt lờ bạn.

#### **Cú pháp:**
```java
if (điều_kiện) {
    // Mã lệnh thực thi nếu điều kiện đúng
}
```

#### **Ví dụ:**
```java
int age = 20;
if (age >= 18) {
    System.out.println("Bạn đủ tuổi lấy vợ");
}
```
- Ở đây, Java kiểm tra xem tuổi (`age`) có lớn hơn hoặc bằng 18 không. Nếu có, Java in ra dòng thông báo. Nếu bạn 17 tuổi? Xin lỗi, Java không nói gì cả.

---

### **2. If/Else: Đưa Ra Lựa Chọn**

**If/Else** giống như một câu hỏi có hai lựa chọn. Nếu điều kiện đúng, thực hiện khối **if**. Nếu sai, chuyển sang thực hiện khối **else**.

#### **Cú pháp:**
```java
if (điều_kiện) {
    // Mã lệnh thực thi nếu điều kiện đúng
} else {
    // Mã lệnh thực thi nếu điều kiện sai
}
```

#### **Ví dụ:**
```java
int score = 75;
if (score >= 50) {
    System.out.println("Bạn đã đậu kỳ thi!");
} else {
    System.out.println("Rất tiếc, bạn đã trượt!");
}
```
- Ở đây, nếu điểm số (`score`) >= 50, Java chúc mừng bạn. Nếu điểm < 50, Java an ủi bạn (một cách hơi… phũ).

---

### **3. Else If: Kiểm Tra Nhiều Điều Kiện**

Đôi khi bạn cần kiểm tra không chỉ một, mà nhiều điều kiện khác nhau. **Else if** sẽ giúp bạn xử lý những tình huống phức tạp hơn.

#### **Cú pháp:**
```java
if (điều_kiện_1) {
    // Mã lệnh thực thi nếu điều kiện_1 đúng
} else if (điều_kiện_2) {
    // Mã lệnh thực thi nếu điều kiện_2 đúng
} else {
    // Mã lệnh thực thi nếu tất cả điều kiện đều sai
}
```

#### **Ví dụ:**
```java
int temperature = 30;

if (temperature > 35) {
    System.out.println("Trời nóng như đổ lửa!");
} else if (temperature > 25) {
    System.out.println("Trời mát mẻ, đi chơi thôi!");
} else {
    System.out.println("Lạnh rồi, ở nhà ôm chăn đi!");
}
```
- Ở đây, Java kiểm tra từng điều kiện theo thứ tự:
    - Nếu nhiệt độ > 35, in "Trời nóng".
    - Nếu không, kiểm tra xem nhiệt độ > 25 không, rồi in "Trời mát".
    - Nếu cả hai đều sai, Java in "Lạnh rồi".

---

### **4. Những Sai Lầm Phổ Biến Khi Dùng If/Else**

- **Quên dấu ngoặc nhọn:**
```java
if (age > 18)
    System.out.println("Đủ tuổi!"); 
System.out.println("Thật tuyệt!"); 
```
- Cả hai câu lệnh trên đều chạy dù `age <= 18`. Bạn muốn điều kiện áp dụng cho nhiều câu lệnh? Phải có dấu ngoặc `{}` nhé!

- **Điều kiện không chính xác:**
```java
if (age = 18) { // Dùng dấu '=' thay vì '=='
    System.out.println("Chúc mừng bạn 18 tuổi!");
}
```
- Kết quả? **Lỗi**! Vì dấu `=` là toán tử gán, không phải so sánh.

---

### **5. Kết Luận**

**If**, **if/else**, và **else if** là những người bạn thân của lập trình viên khi viết logic. Nhưng nhớ sử dụng chúng một cách cẩn thận, nếu không, bạn có thể tự đưa mình vào một mớ bòng bong logic sai lầm.

**Lời khuyên:** Hãy đọc kỹ điều kiện trước khi chạy chương trình. Vì không ai muốn thấy dòng in ra: “Chúc mừng bạn đỗ đại học!” khi bạn chỉ có… 3 điểm đâu! 😂