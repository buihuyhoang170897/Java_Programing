### **Tính Đóng Gói (Encapsulation) Trong Java: Giấu Bí Mật, Nhưng Vẫn Cho Xem Qua Cửa Sổ**

Trong lập trình hướng đối tượng (OOP), **tính đóng gói (encapsulation)** chính là nghệ thuật "giấu đồ nhưng không giấu kỹ". Nó cho phép bạn giấu các dữ liệu quan trọng của một lớp (như thông tin cá nhân) và chỉ cung cấp những gì cần thiết cho người ngoài thông qua các "cửa sổ" an toàn.

---

### **1. Tính Đóng Gói Là Gì?**

Tính đóng gói giống như việc bạn cất tiền trong két sắt:
- **Dữ liệu (biến)** được bảo vệ bên trong két (khai báo với từ khóa `private`).
- Nếu ai muốn "xem tiền", bạn đưa họ **chìa khóa hợp lệ** – đó chính là các phương thức **`getter`** và **`setter`**.

#### **Cú pháp cơ bản của đóng gói:**
1. Khai báo các biến của lớp với từ khóa `private` để không ai "nghịch dại".
2. Tạo các phương thức `getter` và `setter` để truy cập hoặc chỉnh sửa dữ liệu.

#### **Ví dụ Vui Vẻ:**
```java
class Person {
    private String name; // Biến "bí mật"
    private int age;

    // Phương thức getter
    public String getName() {
        return name;
    }

    // Phương thức setter
    public void setName(String newName) {
        this.name = newName;
    }
}
```

#### **Cách sử dụng:**
```java
public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        person.setName("Nguyễn Văn Java"); // Đặt giá trị
        System.out.println(person.getName()); // Lấy giá trị
    }
}
```
**Kết quả:**
```
Nguyễn Văn Java
```

---

### **Tại Sao Cần Đóng Gói?**

- **Bảo vệ dữ liệu:** Tránh người ngoài "đụng chạm" lung tung.
- **Dễ bảo trì:** Nếu muốn thay đổi logic xử lý, chỉ cần sửa trong các phương thức, không phải đụng đến toàn bộ code.
- **Tạo điều kiện kiểm soát:** Bạn có thể kiểm tra hoặc điều kiện hóa dữ liệu trước khi lưu.

Ví dụ, bạn không muốn tuổi của ai đó được đặt là -5? Chỉ cần thêm logic vào setter:
```java
public void setAge(int newAge) {
    if (newAge > 0) {
        this.age = newAge;
    } else {
        System.out.println("Tuổi không hợp lệ!");
    }
}
```

---

### **2. Access Modifier – Bộ Phận Bảo Vệ Siêu Nhân**

**Access Modifier** là các "vệ sĩ" quyết định ai được quyền truy cập vào các biến và phương thức. Có 4 loại chính:

#### **a. Private (`private`):**
- Chỉ cho phép truy cập **trong chính lớp đó**.
- Giống như két sắt chỉ bạn mới mở được.

#### **b. Default (Không ghi gì):**
- Truy cập được **trong cùng package**.
- Như việc hàng xóm thân cận vẫn có thể mượn cây kéo của bạn.

#### **c. Protected (`protected`):**
- Truy cập được trong cùng package và **lớp con** (kể cả khác package).
- Đây là "ưu đãi đặc biệt" cho lớp con, như kiểu "bà con thân thiết".

#### **d. Public (`public`):**
- Mọi nơi đều truy cập được.
- Giống như bạn bật chế độ công khai trên Facebook: ai cũng có thể xem.

#### **Bảng Tóm Tắt:**
| **Modifier** | **Cùng Lớp** | **Cùng Package** | **Lớp Con (khác package)** | **Ngoài Package** |
|--------------|--------------|------------------|----------------------------|-------------------|
| `private`    | ✔            | ✘                | ✘                          | ✘                 |
| `Default`    | ✔            | ✔                | ✘                          | ✘                 |
| `protected`  | ✔            | ✔                | ✔                          | ✘                 |
| `public`     | ✔            | ✔                | ✔                          | ✔                 |

---

### **Kết Luận**

Tính đóng gói là cách bạn bảo vệ dữ liệu khỏi bị phá hoại lung tung, còn **access modifier** chính là lớp bảo mật giúp bạn kiểm soát "ai được vào, ai phải đứng ngoài". Kết hợp chúng, bạn sẽ làm chủ dữ liệu như một coder chuyên nghiệp. **Nhớ nhé: dữ liệu là vàng, hãy giữ nó cẩn thận!** 🚀