# Các Từ Khóa Cơ Bản trong Java
Java có nhiều từ khóa quan trọng, mỗi từ khóa định nghĩa cấu trúc và hành vi của chương trình. Đây là danh sách các từ khóa cơ bản của Java cùng với một giải thích ngắn gọn về từng từ:
- public: Được sử dụng để chỉ ra rằng lớp, phương thức hoặc biến có thể được truy cập từ bất kỳ đâu.

Ví dụ: public class MyClass {}
- private: Chỉ có thể truy cập trong lớp hiện tại, không thể truy cập từ ngoài lớp.

Ví dụ: private int age;
- protected: Truy cập được trong lớp hiện tại, lớp kế thừa và cùng package.

Ví dụ: protected void method() {}
- static: Chỉ ra rằng phương thức hoặc biến thuộc về lớp, không phải đối tượng.

Ví dụ: static int count = 0;
- final: Lớp không thể bị kế thừa, phương thức không thể bị ghi đè, và biến không thể thay đổi giá trị.

Ví dụ: final int MAX = 100;
- void: Chỉ ra rằng phương thức không trả về giá trị.

Ví dụ: public void printMessage() {}
- this: Tham chiếu đến đối tượng hiện tại.

Ví dụ: this.name = name;
- super: Tham chiếu đến lớp cha, dùng để gọi constructor hoặc phương thức của lớp cha.

Ví dụ: super();
- int, double, boolean, v.v.: Các kiểu dữ liệu nguyên thủy.

Ví dụ: int num = 5;, boolean isActive = true;
- new: Dùng để tạo đối tượng mới từ lớp.

Ví dụ: Car myCar = new Car();
- abstract: Dùng để khai báo lớp hoặc phương thức trừu tượng, phải được kế thừa hoặc ghi đè trong lớp con.

Ví dụ: abstract void draw();
- interface: Khai báo một interface, định nghĩa các phương thức mà các lớp implement phải có.

Ví dụ: interface Drawable { void draw(); }
- try, catch, finally: Được sử dụng để xử lý ngoại lệ.

Ví dụ:
try {
int result = 10 / 0;
} catch (ArithmeticException e) {
System.out.println("Error");
}
- if, else, switch, case: Các cấu trúc điều kiện.

Ví dụ: if (x > 0) { ... }
- for, while, do: Các cấu trúc lặp.

Ví dụ: for (int i = 0; i < 10; i++) { ... }
- return: Dùng để trả về giá trị từ phương thức.

Ví dụ: return sum;
- continue, break: Dùng để điều khiển luồng của vòng lặp.

Ví dụ: continue;, break;
- import: Dùng để nhập các lớp hoặc gói từ thư viện khác.

Ví dụ: import java.util.Scanner;
- package: Khai báo gói cho lớp, giúp tổ chức mã nguồn.

Ví dụ: package com.example;
- instanceof: Kiểm tra kiểu của đối tượng.

Ví dụ: if (obj instanceof String) { ... }
- synchronized: Dùng để đồng bộ hóa các phương thức trong môi trường đa luồng.

Ví dụ: synchronized void method() { ... }
- enum: Dùng để khai báo kiểu dữ liệu liệt kê (enumeration).

Ví dụ: enum Day { MONDAY, TUESDAY, ... }
- throw, throws: Dùng để ném ngoại lệ.

Ví dụ: throw new Exception("Error");

Những từ khóa này là những thành phần cơ bản cần thiết để xây dựng chương trình Java hiệu quả. Biết cách sử dụng các từ khóa sẽ giúp bạn hiểu cách Java được tạo ra và viết mã nguồn sạch, dễ bảo trì.