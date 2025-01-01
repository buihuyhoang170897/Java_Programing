### **Ví dụ khác: Quản lý phương tiện giao thông**

Chương trình yêu cầu áp dụng đầy đủ 4 tính chất OOP để quản lý các loại phương tiện giao thông như xe hơi, xe máy, và xe tải.

---

### **Đề bài**

1. **Tính đóng gói (Encapsulation)**
    - Tạo một lớp `Vehicle` với các thuộc tính: tên xe (`name`), tốc độ (`speed`), số bánh xe (`wheels`).
    - Sử dụng **getter** và **setter** để truy cập và cập nhật các thuộc tính này.

2. **Tính kế thừa (Inheritance)**
    - Tạo các lớp con như `Car`, `Motorbike`, và `Truck` kế thừa từ lớp `Vehicle`.

3. **Tính đa hình (Polymorphism)**
    - Ghi đè phương thức `move()` để định nghĩa cách di chuyển riêng cho từng loại phương tiện.

4. **Tính trừu tượng (Abstraction)**
    - Lớp `Vehicle` phải là lớp trừu tượng, khai báo phương thức `move()` và `displayInfo()` là trừu tượng.

---

### **Giải pháp**

#### **1. Lớp trừu tượng `Vehicle`**
```java
abstract class Vehicle {
    private String name;
    private int speed;
    private int wheels;

    // Constructor
    public Vehicle(String name, int speed, int wheels) {
        this.name = name;
        this.speed = speed;
        this.wheels = wheels;
    }

    // Getter và Setter (Encapsulation)
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getSpeed() {
        return speed;
    }

    public void setSpeed(int speed) {
        this.speed = speed;
    }

    public int getWheels() {
        return wheels;
    }

    public void setWheels(int wheels) {
        this.wheels = wheels;
    }

    // Phương thức trừu tượng
    public abstract void move();           // Cách di chuyển
    public abstract void displayInfo();    // Hiển thị thông tin
}
```

#### **2. Lớp `Car` kế thừa từ `Vehicle`**
```java
class Car extends Vehicle {

    public Car(String name, int speed) {
        super(name, speed, 4); // Xe hơi luôn có 4 bánh
    }

    @Override
    public void move() {
        System.out.println(getName() + " di chuyển trên đường với tốc độ " + getSpeed() + " km/h.");
    }

    @Override
    public void displayInfo() {
        System.out.println("Xe hơi: " + getName() + ", Tốc độ: " + getSpeed() + " km/h, Số bánh: " + getWheels());
    }
}
```

#### **3. Lớp `Motorbike` kế thừa từ `Vehicle`**
```java
class Motorbike extends Vehicle {

    public Motorbike(String name, int speed) {
        super(name, speed, 2); // Xe máy luôn có 2 bánh
    }

    @Override
    public void move() {
        System.out.println(getName() + " lướt trên đường với tốc độ " + getSpeed() + " km/h.");
    }

    @Override
    public void displayInfo() {
        System.out.println("Xe máy: " + getName() + ", Tốc độ: " + getSpeed() + " km/h, Số bánh: " + getWheels());
    }
}
```

#### **4. Lớp `Truck` kế thừa từ `Vehicle`**
```java
class Truck extends Vehicle {
    private int loadCapacity; // Sức chứa hàng (tính bằng tấn)

    public Truck(String name, int speed, int loadCapacity) {
        super(name, speed, 6); // Xe tải thường có 6 bánh
        this.loadCapacity = loadCapacity;
    }

    public int getLoadCapacity() {
        return loadCapacity;
    }

    public void setLoadCapacity(int loadCapacity) {
        this.loadCapacity = loadCapacity;
    }

    @Override
    public void move() {
        System.out.println(getName() + " chở hàng với tốc độ " + getSpeed() + " km/h.");
    }

    @Override
    public void displayInfo() {
        System.out.println("Xe tải: " + getName() + ", Tốc độ: " + getSpeed() + " km/h, Số bánh: " + getWheels() + ", Sức chứa: " + loadCapacity + " tấn");
    }
}
```

#### **5. Lớp chính `TransportManagement`**
```java
public class TransportManagement {
    public static void main(String[] args) {
        // Tạo các phương tiện giao thông
        Vehicle car = new Car("Toyota Camry", 120);
        Vehicle motorbike = new Motorbike("Yamaha R15", 80);
        Truck truck = new Truck("Hino 500", 60, 15);

        // Hiển thị thông tin và cách di chuyển của từng phương tiện
        car.displayInfo();
        car.move();

        motorbike.displayInfo();
        motorbike.move();

        truck.displayInfo();
        truck.move();
    }
}
```

---

### **Đầu ra (Output)**

Chạy chương trình trên, kết quả sẽ là:

```
Xe hơi: Toyota Camry, Tốc độ: 120 km/h, Số bánh: 4
Toyota Camry di chuyển trên đường với tốc độ 120 km/h.
Xe máy: Yamaha R15, Tốc độ: 80 km/h, Số bánh: 2
Yamaha R15 lướt trên đường với tốc độ 80 km/h.
Xe tải: Hino 500, Tốc độ: 60 km/h, Số bánh: 6, Sức chứa: 15 tấn
Hino 500 chở hàng với tốc độ 60 km/h.
```

---

### **Phân tích tính chất OOP**
1. **Tính đóng gói (Encapsulation)**  
   Các thuộc tính trong lớp `Vehicle` được khai báo là **private**, và truy cập thông qua các phương thức **getter** và **setter**.

2. **Tính kế thừa (Inheritance)**  
   Các lớp `Car`, `Motorbike`, và `Truck` kế thừa từ lớp `Vehicle`, tái sử dụng các thuộc tính và phương thức chung.

3. **Tính đa hình (Polymorphism)**  
   Phương thức `move()` được ghi đè (overridden) trong các lớp con để định nghĩa cách di chuyển riêng biệt của từng phương tiện.

4. **Tính trừu tượng (Abstraction)**  
   Lớp `Vehicle` là lớp trừu tượng, cung cấp khung sườn chung cho các loại phương tiện và yêu cầu các lớp con triển khai cụ thể các phương thức `move()` và `displayInfo()`.

---

### **Mở rộng bài tập**
- Thêm các loại phương tiện khác như **xe đạp (Bicycle)**, **máy bay (Airplane)**.
- Thêm thuộc tính và phương thức như: **nhiên liệu tiêu thụ (fuelConsumption)** hoặc **loại động cơ (engineType)**.
- Sử dụng **ArrayList** để quản lý danh sách các phương tiện và hiển thị thông tin toàn bộ danh sách.

Nếu bạn muốn, tôi có thể mở rộng hoặc giải thích thêm bất kỳ phần nào! 😊