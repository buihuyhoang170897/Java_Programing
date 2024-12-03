### **Thao Tác Với Excel Trong Java: Biến Coder Thành Nhà Quản Lý Dữ Liệu**

Bạn đang làm việc với Java và sếp bất ngờ giao cho bạn một file Excel đầy dữ liệu? Đừng hoảng! Java không chỉ viết code, in "Hello, World!", mà còn có thể làm Excel "nhảy múa" như một trợ lý văn phòng thứ thiệt.

Hãy cùng khám phá cách thao tác với file Excel trong Java một cách đơn giản và, dĩ nhiên, đầy hài hước!

---

### **1. Làm Sao Java Làm Việc Được Với Excel?**

Java sử dụng một thư viện mạnh mẽ tên là **Apache POI** để thao tác với file Excel. Thư viện này giúp bạn:
- Đọc dữ liệu từ file Excel.
- Ghi dữ liệu vào file Excel.
- Tạo mới một file Excel từ đầu.

---

### **2. Cài Đặt Apache POI**

Trước khi bắt đầu, bạn cần thêm thư viện Apache POI vào dự án. Nếu đang dùng Maven, chỉ cần thêm đoạn này vào file `pom.xml`:
```xml
<dependency>
    <groupId>org.apache.poi</groupId>
    <artifactId>poi-ooxml</artifactId>
    <version>5.3.0</version> <!-- Đảm bảo dùng phiên bản mới nhất -->
</dependency>
```

---

### **3. Đọc File Excel**

Đọc file Excel trong Java giống như mở một cuốn sổ tay. Mỗi sheet trong Excel là một trang, và mỗi ô (cell) chứa thông tin cần đọc.

#### **Ví dụ Đọc File Excel:**
```java
import org.apache.poi.ss.usermodel.*;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;

public class ReadExcel {
    public static void main(String[] args) {
        try {
            FileInputStream fis = new FileInputStream(new File("data.xlsx")); // File Excel
            Workbook workbook = new XSSFWorkbook(fis); // Mở workbook
            Sheet sheet = workbook.getSheetAt(0); // Lấy sheet đầu tiên

            for (Row row : sheet) { // Duyệt qua từng dòng
                for (Cell cell : row) { // Duyệt qua từng ô trong dòng
                    System.out.print(cell.toString() + "\t"); // In nội dung
                }
                System.out.println(); // Xuống dòng
            }
            workbook.close(); // Đừng quên đóng file!
        } catch (IOException e) {
            System.out.println("Lỗi: Không thể đọc file Excel!");
            e.printStackTrace();
        }
    }
}
```

#### **Kết Quả:**
Nếu file `data.xlsx` chứa bảng điểm, bạn sẽ thấy dữ liệu được in ra console như một ma trận thần kỳ.

---

### **4. Ghi Dữ Liệu Vào File Excel**

Muốn tạo mới hoặc cập nhật file Excel? Java cũng làm được với Apache POI.

#### **Ví dụ Ghi File Excel:**
```java
import org.apache.poi.ss.usermodel.*;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;
import java.io.FileOutputStream;
import java.io.IOException;

public class WriteExcel {
    public static void main(String[] args) {
        try {
            Workbook workbook = new XSSFWorkbook(); // Tạo workbook mới
            Sheet sheet = workbook.createSheet("Bảng Điểm"); // Tạo sheet mới

            // Tạo dòng đầu tiên (header)
            Row header = sheet.createRow(0);
            header.createCell(0).setCellValue("Tên");
            header.createCell(1).setCellValue("Điểm");

            // Thêm dữ liệu
            Row row1 = sheet.createRow(1);
            row1.createCell(0).setCellValue("Nguyễn Văn A");
            row1.createCell(1).setCellValue(90);

            Row row2 = sheet.createRow(2);
            row2.createCell(0).setCellValue("Trần Thị B");
            row2.createCell(1).setCellValue(85);

            // Ghi file ra đĩa
            FileOutputStream fos = new FileOutputStream("output.xlsx");
            workbook.write(fos);
            fos.close();
            workbook.close();
            System.out.println("Đã ghi dữ liệu vào file Excel thành công!");
        } catch (IOException e) {
            System.out.println("Lỗi: Không thể ghi file Excel!");
            e.printStackTrace();
        }
    }
}
```

#### **Kết Quả:**
File `output.xlsx` sẽ chứa bảng điểm đẹp như trong mơ.

---

### **5. Xóa Dữ Liệu hoặc Sửa Dữ Liệu**

Để sửa, bạn chỉ cần tìm đúng dòng và ô rồi cập nhật giá trị mới. Xóa dữ liệu? Đơn giản là xóa nội dung trong ô đó:
```java
row.getCell(1).setCellValue(""); // Xóa dữ liệu trong ô
```

---

### **6. Lưu Ý Khi Làm Việc Với Excel**

1. **Chọn đúng định dạng file:**
    - File `.xlsx` dùng `XSSFWorkbook`.
    - File `.xls` dùng `HSSFWorkbook`.

2. **Đóng tài nguyên sau khi dùng:**
    - `workbook.close()` và `file.close()` rất quan trọng để tránh rò rỉ tài nguyên.

3. **Cẩn thận với đường dẫn:**  
   Đảm bảo đường dẫn file đúng, hoặc dùng đường dẫn tuyệt đối nếu file không nằm cùng thư mục với mã.

---

### **7. Kết Luận**

Thao tác với file Excel trong Java không quá khó, chỉ cần bạn "kết bạn" với Apache POI. Hãy tưởng tượng bạn là "chuyên gia Excel hóa", vừa đọc, vừa ghi, vừa làm đẹp file dữ liệu một cách chuyên nghiệp.

**Mẹo nhỏ:** Đừng quên kiểm tra dữ liệu đầu vào, và nếu sếp giao quá nhiều file Excel, hãy yêu cầu... thêm lương! 🚀