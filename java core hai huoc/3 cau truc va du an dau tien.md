### **Giới Thiệu Cấu Trúc Dự Án Java & Viết Chương Trình “Hello World” Đầu Tiên**

Bạn đã sẵn sàng bắt đầu hành trình với Java chưa? Hãy tưởng tượng bạn đang chuẩn bị xây dựng ngôi nhà đầu tiên (chính là dự án Java), và việc đầu tiên bạn cần làm là hiểu rõ cấu trúc của nó. Sau đó, để ăn mừng việc này, chúng ta sẽ viết một chương trình “Hello World” – giống như treo biển “Ngôi nhà đã xong, mời ghé thăm”!

---

### **1. Cấu Trúc Dự Án Java: Hiểu Nhà Mình Có Gì**

Một dự án Java nhìn tưởng đơn giản, nhưng thật ra nó khá giống với một tủ đồ cá nhân: nếu không sắp xếp gọn gàng, bạn sẽ không bao giờ tìm thấy đôi tất mình cần. Vậy một dự án Java cơ bản bao gồm những gì?

#### **a. Thư Mục Chính**
Khi bạn tạo một dự án Java trong các IDE (ví dụ: IntelliJ IDEA hoặc Eclipse), nó sẽ tạo ra một cấu trúc thư mục như sau:

```
MyFirstProject/
├── src/
│   ├── Main.java
└── out/
```

- **`src/` (source):** Đây là nơi bạn sẽ viết code. Nghĩa là tất cả những gì bạn gõ gõ (như `System.out.println`) sẽ nằm ở đây. Đây cũng là trái tim của dự án.
- **`out/` (output):** Sau khi biên dịch, các file `.class` sẽ được lưu tại đây. Chúng là sản phẩm mà JVM có thể chạy.
- **File `.idea` hoặc `.project`:** Đây là các file do IDE tạo ra để quản lý dự án. Bạn không cần quan tâm trừ khi muốn “vọc vạch” sâu hơn.

#### **b. Tập Tin Java**
Tập tin Java quan trọng nhất mà bạn thường gặp có dạng **`TênLớp.java`**. Mỗi file là một lớp (class), và lớp này có thể chứa các phương thức (method) – như các chức năng bạn sẽ xây dựng.

Ví dụ, file `Main.java` cơ bản trông sẽ như thế này:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

- **`public class Main`:** Đây là định nghĩa lớp chính (giống như nhân vật chính của phim).
- **`public static void main`:** Đây là điểm bắt đầu của chương trình. Nếu thiếu dòng này, JVM sẽ không biết phải làm gì.

---

### **2. Viết Chương Trình “Hello World” Đầu Tiên**

Đây là khoảnh khắc mà mọi lập trình viên đều phải trải qua: viết một chương trình để máy tính in ra dòng chữ **“Hello, World!”**. Nghe thì đơn giản, nhưng nó là “nghi thức nhập môn” của bất kỳ ngôn ngữ nào.

#### **Bước 1: Tạo File Java**
Mở IDE của bạn, tạo một dự án mới và thêm một file tên là **`Main.java`** vào thư mục `src`.

#### **Bước 2: Viết Code**
Gõ đoạn code thần thánh này vào:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

#### **Bước 3: Chạy Chương Trình**
- Trong IDE, nhấn nút “Run” (hoặc phím tắt như `Shift + F10` trong IntelliJ IDEA).
- Nếu mọi thứ đều đúng, bạn sẽ thấy dòng chữ **“Hello, World!”** hiện ra trên màn hình console.
![helloWorldConsole.png](..%2Fpicture%2FhelloWorldConsole.png)
#### **Giải Thích code nè:**
- **`System.out.println`:** Đây là lệnh bảo Java in ra màn hình. Hãy coi nó là micro để bạn nói chuyện với thế giới.
- **Dấu ngoặc kép:** Bạn cần bao dòng chữ trong dấu ngoặc kép, nếu không Java sẽ nghĩ bạn đang gửi tín hiệu... ngoài hành tinh.

---

### **Lỗi “Cười Ra Nước Mắt” Mà Bạn Có Thể Gặp**

1. **Quên dấu chấm phẩy (`;`):** Java cực kỳ nhạy cảm với dấu chấm phẩy. Quên nó giống như bỏ bánh xe ra khỏi xe đạp vậy.
2. **Sai tên file hoặc tên lớp:** Nếu file bạn đặt tên là `Main.java`, thì lớp bên trong cũng phải là `Main`. Nhớ đồng bộ để tránh bị JVM “gắt”.
3. **Viết nhầm `println` thành `printIn`:** Không ai thoát khỏi lỗi này trong lần đầu, nhưng hãy nhớ chữ “ln” là viết tắt của “line”.

---

### **Kết Luận**

Chương trình “Hello World” đơn giản là bài học đầu tiên, nhưng nó mở ra cánh cửa lớn để bạn khám phá thế giới lập trình Java. Và cấu trúc dự án? Cứ tưởng là rắc rối, nhưng thật ra là cách để mọi thứ luôn ngăn nắp và dễ quản lý.

**Chúc bạn thành công với bước khởi đầu này! Cứ viết và chạy thử, và đừng quên: mỗi lỗi là một bài học thú vị!** 🚀