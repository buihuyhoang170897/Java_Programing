# Giọng văn: kể chuyện

### **Câu chuyện lập trình của tôi: Hành trình khám phá vòng lặp và những từ khóa quyền năng trong Java**

Chào bạn! Hôm nay, tôi sẽ kể cho bạn nghe một câu chuyện – câu chuyện về cuộc hành trình của tôi khi lần đầu tiên khám phá "vòng lặp" và những từ khóa kỳ diệu **`break`** và **`continue`** trong Java. Nghe có vẻ khô khan? Đừng lo, tôi hứa câu chuyện này vừa thú vị vừa giúp bạn hiểu rõ hơn về lập trình.

---

## **1. Lạc vào thế giới của vòng lặp**

Ngày xưa, khi mới học Java, tôi từng mơ ước: "Giá mà có cách để máy tính làm đi làm lại một việc mà mình không cần gõ mã hàng trăm lần!". Và rồi, tôi gặp **vòng lặp**, một phép màu làm thay đổi cách tôi nhìn thế giới lập trình.

### **1.1. Vòng lặp `for` – Người bạn ngăn nắp**
Lần đầu tiên, tôi làm quen với anh chàng `for`. Anh ấy giống như một người lính gác rất nguyên tắc: chỉ làm việc khi biết rõ mình phải làm gì và làm bao nhiêu lần.

Tôi nhớ bài tập đầu tiên với `for`:
- Thầy bảo: “Hãy in số từ 1 đến 10 lên màn hình”.
- Tôi cười: “Chuyện nhỏ!”.

Và đây là cách tôi viết:
```java
for (int i = 1; i <= 10; i++) {
    System.out.println("Số thứ: " + i);
}
```

Lần đầu chạy chương trình, những con số hiện lên đều tăm tắp. Tôi cảm giác như vừa điều khiển được một đoàn tàu vậy!

Nhưng chưa dừng lại ở đó. Một hôm, tôi thử nghiệm thêm:
- “Nếu muốn tỏ tình 100 lần thì sao nhỉ?”  
  Và thế là…
```java
for (int i = 1; i <= 100; i++) {
    System.out.println("Anh thích em lần thứ " + i);
}
```
Máy tính làm xong trong chớp mắt. Còn tôi? Chỉ biết cười hạnh phúc!

---

### **1.2. Vòng lặp `while` – Người bạn kiên nhẫn**
Một ngày nọ, tôi gặp `while`. Anh bạn này không giống `for` chút nào. `while` là kiểu người chỉ làm khi điều kiện cho phép. Kiểu như anh ấy sẽ hỏi:
- “Có chắc là mình nên làm không? Được thì làm, không thì thôi.”

Một hôm, tôi thử kiểm tra xem mình còn bao nhiêu tiền sau mỗi lần đi mua trà sữa. Và tôi đã viết:
```java
int tien = 20; // Có 20 nghìn trong túi
while (tien > 0) {
    System.out.println("Còn " + tien + " nghìn trong túi!");
    tien -= 5; // Mỗi lần tiêu 5k
}
```
Cứ mỗi lần chạy vòng lặp, tiền trong túi lại giảm dần. Khi tiền hết, `while` chào tạm biệt:
- “Thôi nhé, không còn lý do để tiếp tục đâu.”

---

### **1.3. Vòng lặp `do-while` – Làm trước, hỏi sau**
Lần cuối cùng trong hành trình vòng lặp, tôi gặp `do-while`. Cậu ấy thì khác hoàn toàn, kiểu như một người bạn táo bạo:
- “Cứ làm trước đi! Sai thì tính sau!”

Có lần, tôi đói bụng và nếm thử món ăn mới dù hơi ngờ vực. Điều đó làm tôi nghĩ đến `do-while`. Tôi viết:
```java
boolean ngonQua = false;
do {
    System.out.println("Ăn thử món này cái đã!");
    ngonQua = true; // Wow, ngon thật!
} while (!ngonQua);
```
Dù ban đầu hơi nghi ngờ, nhưng ít nhất món ăn đã được nếm thử. Hóa ra, làm trước đôi khi cũng là cách tốt!

---

## **2. Những từ khóa quyền năng: `break` và `continue`**

Lần nọ, trong khi làm việc với vòng lặp, tôi gặp một vấn đề lớn:
- “Nếu đang lặp mà mình muốn dừng giữa chừng thì làm sao?”

Và rồi, tôi phát hiện ra **`break`** và **`continue`**, hai từ khóa như siêu anh hùng đến giải cứu.

---

### **2.1. `break` – Người hùng dừng vòng lặp**
`break` giống như một nút thoát hiểm khẩn cấp. Khi bạn thấy không cần tiếp tục nữa, chỉ cần gọi `break`.

Có lần tôi tìm số chẵn đầu tiên trong dãy số từ 1 đến 10:
```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 == 0) {
        System.out.println("Số chẵn đầu tiên là: " + i);
        break; // Dừng ngay khi tìm thấy!
    }
}
```
`break` giúp tôi thoát khỏi vòng lặp ngay khi đạt được mục tiêu.

---

### **2.2. `continue` – Người bạn bỏ qua rắc rối**
`continue` thì khác. Nó không dừng vòng lặp, mà chỉ nói:
- “Lần này tạm bỏ qua, lần sau tiếp tục nhé!”

Ví dụ, tôi muốn in tất cả các số từ 1 đến 10, trừ những số chia hết cho 3:
```java
for (int i = 1; i <= 10; i++) {
    if (i % 3 == 0) {
        continue; // Bỏ qua các số chia hết cho 3
    }
    System.out.println(i);
}
```
Nhờ `continue`, tôi vẫn kiểm soát vòng lặp mà không cần quá nhiều điều kiện phức tạp.

---

## **Kết thúc câu chuyện**

Từ ngày gặp vòng lặp và hai từ khóa kỳ diệu này, tôi cảm thấy như mình có thêm siêu năng lực. Những bài toán lặp đi lặp lại không còn là ác mộng nữa. Và hơn hết, tôi hiểu rằng lập trình không chỉ là viết mã mà còn là tận hưởng niềm vui khám phá.

Bạn cũng vậy, hãy thử trải nghiệm và sáng tạo với vòng lặp nhé! Chắc chắn bạn sẽ tìm được câu chuyện của riêng mình. 🚀  