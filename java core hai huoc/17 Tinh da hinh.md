### **Tính Đa Hình Trong Java: Khi Một Người Có Thể Đội Nhiều Mũ**

**Tính đa hình (Polymorphism)** là một trong những đặc trưng thú vị nhất của lập trình hướng đối tượng (OOP). Đa hình giống như việc bạn là một con người, nhưng trong các tình huống khác nhau, bạn có thể đóng nhiều vai trò khác nhau: **ở nhà là con ngoan, đi làm là nhân viên chăm chỉ, và tối về lại là game thủ “try hard”!**

Trong Java, tính đa hình cho phép một đối tượng **thay đổi hình dạng** để thực hiện các hành động khác nhau, tùy thuộc vào ngữ cảnh.

---

### **1. Đa Hình Là Gì?**

Hiểu nôm na, tính đa hình là khả năng một đối tượng có nhiều cách biểu hiện khác nhau. Có hai dạng chính:
1. **Đa hình tại thời điểm biên dịch (Compile-time Polymorphism):** Còn gọi là **Method Overloading** – tức là một phương thức nhưng có nhiều phiên bản khác nhau.
2. **Đa hình tại thời điểm chạy (Runtime Polymorphism):** Còn gọi là **Method Overriding** – tức là lớp con “tái định nghĩa” cách làm việc của phương thức lớp cha.

---

### **2. Đa Hình Tại Thời Điểm Biên Dịch – Method Overloading**

Bạn có thể tạo nhiều phương thức cùng tên, nhưng khác nhau về số lượng hoặc kiểu tham số. Java sẽ chọn đúng phương thức phù hợp dựa trên cách bạn gọi nó.

#### **Ví dụ Vui Vẻ:**
```java
class Calculator {
    // Cộng hai số
    int add(int a, int b) {
        return a + b;
    }

    // Cộng ba số
    int add(int a, int b, int c) {
        return a + b + c;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        System.out.println(calc.add(5, 10));       // Kết quả: 15
        System.out.println(calc.add(5, 10, 20));  // Kết quả: 35
    }
}
```
Ở đây, phương thức `add` có thể xử lý cả hai trường hợp: cộng 2 số hoặc cộng 3 số. Java "tự biết" bạn muốn gọi phiên bản nào.

---

### **3. Đa Hình Tại Thời Điểm Chạy – Method Overriding**

Lớp con có thể **ghi đè** (override) phương thức của lớp cha để cung cấp hành vi riêng. Đây là cách tính đa hình "nở rộ" khi bạn làm việc với kế thừa.

#### **Ví dụ Vui Vẻ:**
```java
class Animal {
    void sound() {
        System.out.println("Động vật phát ra âm thanh!");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Chó sủa: Gâu gâu!");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Mèo kêu: Meo meo!");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myDog = new Dog();
        Animal myCat = new Cat();

        myDog.sound(); // Kết quả: Chó sủa: Gâu gâu!
        myCat.sound(); // Kết quả: Mèo kêu: Meo meo!
    }
}
```
Ở đây, phương thức `sound` của lớp cha `Animal` bị lớp con `Dog` và `Cat` ghi đè, mỗi lớp con có cách “hát” riêng.

---

### **4. Lợi Ích Của Tính Đa Hình**

- **Giảm độ phức tạp:** Bạn chỉ cần nhớ tên phương thức chung, không cần tạo thêm hàng loạt tên khác nhau.
- **Tính linh hoạt:** Một đối tượng có thể thực hiện các hành động khác nhau tùy thuộc vào bối cảnh.
- **Tái sử dụng code:** Lớp cha định nghĩa khung sườn, lớp con tự do tùy chỉnh chi tiết.

---

### **5. Một Số Sai Lầm Hài Hước Khi Sử Dụng Đa Hình**

1. **Không ghi đúng cú pháp Override:**  
   Quên viết `@Override` khi ghi đè phương thức? Kết quả: chương trình vẫn chạy, nhưng bạn sẽ… "ngớ người" vì phương thức lớp cha bị gọi thay vì lớp con.

2. **Phương thức trong lớp cha không phải `public`:**  
   Lớp con sẽ không thể ghi đè được. Hãy nhớ: "Cha phải rộng lòng, con mới dễ tuỳ biến".

---

### **Kết Luận**

Tính đa hình là cách để Java giúp bạn **biến hóa** linh hoạt trong lập trình. Bạn có thể dùng chung một tên phương thức, nhưng hành vi của nó sẽ khác nhau tùy ngữ cảnh. **Đa hình không chỉ giúp code bạn đẹp hơn, mà còn giúp bạn trở thành coder "đa tài"!** 🚀