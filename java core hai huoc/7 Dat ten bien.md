### **Đặt Tên Biến Trong Java: Đừng Biến "Biến" Thành Thảm Họa!**

Trong thế giới lập trình, tên biến giống như tên em bé – phải có ý nghĩa, dễ gọi và không gây nhầm lẫn. Đặt tên biến bừa bãi như `abc123` hay `xyz` chẳng khác gì tự đào hố chôn mình (và đồng đội). Hãy cùng tôi tìm hiểu **quy định đặt tên biến** sao cho chuẩn chỉnh mà không mất vui nhé!

---

### **1. Quy Tắc Vàng Khi Đặt Tên Biến**

#### **a. Bắt đầu bằng chữ cái hoặc dấu gạch dưới `_`**
Tên biến không được phép khởi đầu bằng số, ký tự đặc biệt hay icon cảm xúc (xin lỗi các fan emoji).
- **Được:** `name`, `_hiddenValue`.
- **Sai:** `123variable`, `@javaMaster`.

#### **b. Không chứa khoảng trắng hoặc ký tự đặc biệt (ngoại trừ `_`)**
Java không thích những biến như `my variable` – nó sẽ hiểu bạn vừa gõ nhầm. Dùng `_` thay vì khoảng trắng nhé!
- **Được:** `my_variable`, `total_sum`.
- **Sai:** `my variable`, `total#sum`.

#### **c. Không được trùng với từ khóa của Java**
Tên biến như `int`, `class`, hay `double` là cấm kỵ. Java cần những từ này để làm việc của nó, đừng “cướp” công cụ của Java!
- **Được:** `numberOfStudents`, `classRoom`.
- **Sai:** `int`, `class`.

#### **d. Phân biệt chữ hoa và chữ thường (case-sensitive)**
Biến `age` khác hoàn toàn với `Age`. Đừng để sự bất cẩn này làm bạn “khóc thét” khi debug.
- **Ví dụ:** `totalMarks` ≠ `TotalMarks`.

#### **e. Tên biến phải có ý nghĩa và mô tả rõ ràng**
Đừng dùng `x`, `y`, `z` trừ khi bạn đang viết phương trình toán học. Hãy đặt tên rõ ràng, giúp bạn và người đọc code hiểu ngay nó làm gì.
- **Tốt:** `studentScore`, `isCompleted`.
- **Tệ:** `data`, `temp`.

---

### **2. Theo Quy Tắc CamelCase Hoặc snake_case**

#### **CamelCase:**
Bắt đầu chữ cái đầu tiên viết thường, các từ tiếp theo viết hoa chữ cái đầu. Tên biến sẽ lên xuống như lưng lạc đà bướu đó!
- **Ví dụ:** `studentName`, `totalScore`.

#### **snake_case:**
Dùng dấu gạch dưới để phân cách giữa các từ. Tên biến sẽ nối nhau như con rắn 
- **Ví dụ:** `student_name`, `total_score`.

---

### **Kết Luận**

Hãy nhớ rằng **một cái tên biến đẹp là một cái tên không gây đau đầu**. Đừng ngại dành thêm chút thời gian để đặt tên rõ ràng và tuân theo quy tắc, bởi vì sau này, người đọc code của bạn (có thể là bạn của tương lai) sẽ cảm ơn bạn rất nhiều. **Code sạch, lòng thanh thản!** 🚀