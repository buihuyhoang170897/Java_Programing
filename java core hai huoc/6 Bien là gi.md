### **Biến Trong Java: Một Câu Chuyện Về Lưu Trữ Dữ Liệu**

Trong Java, **biến (variable)** giống như một cái hộp thần kỳ để bạn lưu trữ thông tin. Chúng là nền tảng cơ bản cho mọi chương trình Java.

---

### **1. Biến Là Gì?**

**Biến** là nơi lưu giữ dữ liệu tạm thời trong chương trình. Bạn có thể thay đổi giá trị của biến bất cứ lúc nào (trừ khi bạn chán và biến nó thành hằng số). Hãy tưởng tượng biến giống như một cái vali, bạn có thể mở ra, bỏ vào áo quần, hoặc lấy đồ ra tùy ý.

---

### **2. Cách Khai Báo Biến**

Khai báo biến trong Java rất đơn giản:
```java
<kiểu dữ liệu> <tên biến> = <giá trị>;
```

Ví dụ:
```java
int age = 25; // Biến số nguyên
String name = "Java"; // Biến chuỗi
// Khởi tạo sau khi khai báo
int height;
height = 180;
```
---

### **3. Cách Sử Dụng Biến**

Sau khi khai báo, bạn có thể gán giá trị mới hoặc sử dụng giá trị biến trong các phép toán:
```java
age = 30; // Gán giá trị mới
System.out.println("Tuổi của bạn là: " + age);
```

---

### **4. Phạm Vi Biến**

Phạm vi biến quyết định nơi bạn có thể sử dụng nó. Có 3 loại chính:

#### **a. Biến cục bộ (Local Variable):**
Khai báo trong phương thức và chỉ dùng được trong phương thức đó.
```java
void greet() {
    int x = 10; // Chỉ dùng trong greet()
}
```

#### **b. Biến toàn cục (Instance Variable):**
Khai báo trong lớp, ngoài các phương thức. Dùng cho mọi phương thức trong lớp.
```java
class Example {
    int globalVar = 100; // Biến toàn cục
}
```

#### **c. Biến tĩnh (Static Variable):**
Khai báo với từ khóa `static`, được chia sẻ bởi tất cả các đối tượng.
```java
static int sharedVar = 50;
```
Thêm ví dụ nè:
```java
public class ScopeExample {
// Biến toàn cục
int globalVar = 10;
static int staticVar = 20;

    public void method() {
        // Biến cục bộ
        int localVar = 30;
        System.out.println(localVar);
    }

    public static void main(String[] args) {
        ScopeExample obj = new ScopeExample();
        System.out.println(obj.globalVar);
        System.out.println(staticVar);
    }
}
```
---

### **5. Hằng Số**

Hằng số là biến nhưng không thay đổi giá trị, được khai báo bằng từ khóa **`final`**. Nó giống như một chiếc hộp được niêm phong kín.
```java
final double PI = 3.14159; // Giá trị cố định
PI = 3.14; // Sai! Hằng số không thể thay đổi.
```

#### **Ưu điểm của hằng số:**
- Đảm bảo giá trị luôn cố định.
- Làm code dễ đọc hơn (ai cũng hiểu `PI` là số pi, không thay đổi).

---

### **6. Kết Luận**

**Biến** là công cụ tuyệt vời để lưu trữ thông tin động, còn **hằng số** giúp bạn giữ những thứ bất biến. Hãy sử dụng chúng đúng cách để tránh “khóc thét” khi chương trình chạy sai!
