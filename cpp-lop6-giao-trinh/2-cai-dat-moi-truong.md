# Bài 2: Cài đặt môi trường lập trình và chạy chương trình đầu tiên

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Biết môi trường lập trình là gì.
* Biết cần phần mềm nào để viết và chạy C++.
* Biết tạo file chương trình C++.
* Biết chạy chương trình C++ đầu tiên.
* Biết sửa nội dung trong lệnh `cout`.
* Nhận biết một số lỗi đơn giản khi chạy chương trình.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Lập trình là gì?
2. Chương trình máy tính là gì?
3. Máy tính có tự hiểu ý muốn của con người không?
4. Lệnh `cout` dùng để làm gì?

Gợi ý trả lời:

```text
1. Lập trình là viết lệnh cho máy tính.
2. Chương trình là tập hợp nhiều câu lệnh.
3. Không. Máy tính chỉ làm theo lệnh.
4. cout dùng để in nội dung ra màn hình.
```

Giáo viên dẫn vào bài mới:

> Ở bài trước, chúng ta đã biết lập trình là viết lệnh cho máy tính.
> Hôm nay, chúng ta sẽ học cách viết chương trình C++ thật sự và chạy nó trên máy tính.

---

# 3. Môi trường lập trình là gì?

## Giải thích đơn giản

**Môi trường lập trình** là nơi giúp chúng ta:

* Viết chương trình.
* Lưu chương trình.
* Chạy chương trình.
* Xem kết quả.
* Phát hiện lỗi.

Có thể giải thích cho học sinh như sau:

> Muốn viết văn, em cần vở và bút.
> Muốn vẽ tranh, em cần giấy và màu.
> Muốn lập trình, em cần phần mềm để viết và chạy chương trình.

Phần mềm đó gọi là **môi trường lập trình**.

---

# 4. Cần những gì để lập trình C++?

Để lập trình C++, ta thường cần 2 thứ:

| Thành phần           | Công dụng                               |
| -------------------- | --------------------------------------- |
| Trình soạn thảo code | Nơi viết chương trình                   |
| Trình biên dịch C++  | Giúp máy tính hiểu và chạy chương trình |

Giải thích đơn giản:

## Trình soạn thảo code

Là nơi ta gõ chương trình.

Ví dụ:

* VS Code
* Dev-C++
* Code::Blocks
* OnlineGDB
* Replit

## Trình biên dịch C++

Là công cụ dịch chương trình C++ sang dạng máy tính có thể hiểu.

Ví dụ dễ hiểu:

```text
Con người viết: cout << "Xin chao";
Máy tính cần: mã máy
Trình biên dịch sẽ giúp dịch từ C++ sang mã máy.
```

---

# 5. Nên dùng phần mềm nào cho lớp 6?

Với học sinh lớp 6, có thể chọn một trong hai cách.

## Cách 1: Dùng trình chạy online

Phù hợp nếu chưa muốn cài phần mềm.

Ví dụ:

* OnlineGDB
* Programiz C++ Compiler
* Replit

Ưu điểm:

* Không cần cài đặt.
* Mở trình duyệt là dùng được.
* Phù hợp cho buổi đầu.

Nhược điểm:

* Cần internet.
* Có thể bị chậm hoặc có quảng cáo.

---

## Cách 2: Dùng phần mềm trên máy tính

Phù hợp nếu học lâu dài.

Có thể dùng:

* Dev-C++
* Code::Blocks
* VS Code + trình biên dịch C++

Với lớp 6 mới học, giáo viên có thể dùng **Dev-C++** hoặc **Code::Blocks** cho dễ.

Nếu học sinh quen dùng máy tính hơn, có thể dùng **VS Code**.

---

# 6. Tên file C++ là gì?

Chương trình C++ thường được lưu trong file có đuôi:

```text
.cpp
```

Ví dụ:

```text
bai2.cpp
hello.cpp
xin_chao.cpp
```

Giáo viên giải thích:

> Giống như file Word thường có đuôi `.docx`,
> file ảnh có thể có đuôi `.jpg` hoặc `.png`,
> file C++ có đuôi `.cpp`.

---

# 7. Quy tắc đặt tên file

Nên đặt tên file:

* Không dấu tiếng Việt.
* Không có khoảng trắng.
* Dùng chữ thường.
* Có thể dùng dấu gạch dưới `_`.

Nên đặt:

```text
bai2.cpp
xin_chao.cpp
chuong_trinh_dau_tien.cpp
```

Không nên đặt:

```text
bài 2.cpp
xin chào.cpp
chương trình đầu tiên.cpp
```

Lý do:

> Tên file có dấu hoặc có khoảng trắng đôi khi gây lỗi hoặc khó chạy.

---

# 8. Chương trình C++ đầu tiên

Giáo viên cho học sinh gõ chương trình sau:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao lop 6!";
    return 0;
}
```

Kết quả khi chạy:

```text
Xin chao lop 6!
```

---

# 9. Giải thích từng phần trong chương trình

Ở bài này, học sinh chưa cần hiểu quá sâu. Chỉ cần hiểu đơn giản.

| Dòng lệnh              | Ý nghĩa đơn giản                |
| ---------------------- | ------------------------------- |
| `#include <iostream>`  | Cho phép dùng lệnh nhập xuất    |
| `using namespace std;` | Giúp viết lệnh ngắn hơn         |
| `int main()`           | Nơi chương trình bắt đầu chạy   |
| `{` và `}`             | Đánh dấu phần thân chương trình |
| `cout`                 | In nội dung ra màn hình         |
| `return 0;`            | Kết thúc chương trình           |

Giáo viên nhấn mạnh:

> Trong bài này, quan trọng nhất là các em biết chương trình bắt đầu ở `main` và `cout` dùng để in ra màn hình.

---

# 10. Cấu trúc cơ bản của chương trình C++

Giáo viên có thể cho học sinh ghi nhớ mẫu sau:

```cpp
#include <iostream>
using namespace std;

int main() {
    // Viết lệnh ở đây

    return 0;
}
```

Giải thích:

> Khi viết chương trình C++ cơ bản, các em có thể dùng mẫu này trước.
> Sau đó thay phần `// Viết lệnh ở đây` bằng lệnh mình muốn máy tính thực hiện.

---

# 11. Dấu chấm phẩy `;`

Trong C++, nhiều câu lệnh phải kết thúc bằng dấu:

```text
;
```

Ví dụ đúng:

```cpp
cout << "Xin chao";
return 0;
```

Ví dụ sai:

```cpp
cout << "Xin chao"
return 0
```

Giáo viên giải thích:

> Dấu `;` giống như dấu chấm trong câu văn.
> Nó báo cho máy tính biết câu lệnh đã kết thúc.

---

# 12. Dấu ngoặc kép `" "`

Khi muốn in chữ ra màn hình, ta đặt chữ trong dấu ngoặc kép:

```cpp
cout << "Xin chao";
```

Phần nằm trong `" "` sẽ được in ra màn hình.

Ví dụ:

```cpp
cout << "Toi dang hoc C++";
```

Kết quả:

```text
Toi dang hoc C++
```

Nếu quên dấu ngoặc kép, chương trình sẽ báo lỗi.

Sai:

```cpp
cout << Toi dang hoc C++;
```

Đúng:

```cpp
cout << "Toi dang hoc C++";
```

---

# 13. Chạy chương trình

Tùy phần mềm mà cách chạy khác nhau.

## Nếu dùng trình chạy online

Các bước:

```text
1. Mở trang chạy C++ online.
2. Chọn ngôn ngữ C++.
3. Gõ chương trình.
4. Bấm nút Run.
5. Xem kết quả ở màn hình Output.
```

## Nếu dùng Dev-C++ hoặc Code::Blocks

Các bước:

```text
1. Mở phần mềm.
2. Tạo file mới.
3. Gõ chương trình.
4. Lưu file với đuôi .cpp.
5. Bấm Compile & Run hoặc Run.
6. Xem kết quả.
```

## Nếu dùng VS Code

Các bước tổng quát:

```text
1. Mở VS Code.
2. Tạo file bai2.cpp.
3. Gõ chương trình.
4. Lưu file.
5. Chạy chương trình bằng nút Run hoặc terminal.
6. Xem kết quả.
```

Với học sinh lớp 6, giáo viên nên chuẩn bị sẵn môi trường trước để tránh mất quá nhiều thời gian cài đặt.

---

# 14. Hoạt động thực hành 1: Chạy chương trình mẫu

Yêu cầu học sinh gõ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao lop 6!";
    return 0;
}
```

Sau khi chạy, học sinh cần thấy kết quả:

```text
Xin chao lop 6!
```

Giáo viên kiểm tra:

* Học sinh có gõ đúng `#include <iostream>` không?
* Có gõ đúng `int main()` không?
* Có đủ dấu `{` và `}` không?
* Có dấu `;` sau lệnh `cout` không?
* Có dấu `;` sau `return 0` không?

---

# 15. Hoạt động thực hành 2: Đổi nội dung in ra màn hình

Yêu cầu học sinh sửa dòng:

```cpp
cout << "Xin chao lop 6!";
```

Thành:

```cpp
cout << "Em ten la An";
```

Hoặc:

```cpp
cout << "Hom nay em hoc lap trinh";
```

Ví dụ chương trình hoàn chỉnh:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Em ten la An";
    return 0;
}
```

Kết quả:

```text
Em ten la An
```

---

# 16. Hoạt động thực hành 3: In nhiều dòng

Để in nhiều dòng, ta có thể dùng `endl`.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao!" << endl;
    cout << "Em dang hoc C++" << endl;
    cout << "Lap trinh rat thu vi";

    return 0;
}
```

Kết quả:

```text
Xin chao!
Em dang hoc C++
Lap trinh rat thu vi
```

Giải thích:

```cpp
endl
```

có nghĩa là xuống dòng.

---

# 17. Hoạt động thực hành 4: Tự giới thiệu bản thân

Yêu cầu học sinh viết chương trình in ra 3 dòng:

```text
Ten cua em la ...
Em hoc lop ...
So thich cua em la ...
```

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Ten cua em la Nam" << endl;
    cout << "Em hoc lop 6A" << endl;
    cout << "So thich cua em la bong da";

    return 0;
}
```

Kết quả:

```text
Ten cua em la Nam
Em hoc lop 6A
So thich cua em la bong da
```

---

# 18. Lỗi thường gặp trong bài 2

## Lỗi 1: Quên dấu `;`

Sai:

```cpp
cout << "Xin chao"
```

Đúng:

```cpp
cout << "Xin chao";
```

Cách nhận biết:

* Chương trình báo lỗi.
* Thường lỗi xuất hiện ở dòng hiện tại hoặc dòng ngay sau đó.

---

## Lỗi 2: Viết sai `cout`

Sai:

```cpp
count << "Xin chao";
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích:

> Máy tính không đoán ý mình. Gõ sai một chữ cũng có thể lỗi.

---

## Lỗi 3: Quên dấu ngoặc kép

Sai:

```cpp
cout << Xin chao;
```

Đúng:

```cpp
cout << "Xin chao";
```

---

## Lỗi 4: Thiếu dấu `{` hoặc `}`

Sai:

```cpp
int main() 
    cout << "Xin chao";
    return 0;
}
```

Đúng:

```cpp
int main() {
    cout << "Xin chao";
    return 0;
}
```

Giải thích:

> Dấu `{` và `}` giống như cái hộp chứa các lệnh bên trong chương trình chính.

---

## Lỗi 5: Chưa lưu file

Một số phần mềm yêu cầu lưu file trước khi chạy.

Cách sửa:

```text
1. Bấm Save.
2. Đặt tên file có đuôi .cpp.
3. Chạy lại chương trình.
```

---

# 19. Bài tập trên lớp

## Bài 1: Điền từ còn thiếu

```text
File C++ thường có đuôi là ______.
```

Đáp án:

```text
.cpp
```

---

## Bài 2: Chọn đáp án đúng

Lệnh nào dùng để in nội dung ra màn hình?

A. `cin`
B. `cout`
C. `main`
D. `return`

Đáp án: **B**

---

## Bài 3: Sửa lỗi chương trình

Chương trình sau bị lỗi. Hãy sửa lại.

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao lop 6!"
    return 0;
}
```

Lỗi:

```text
Thiếu dấu ; sau dòng cout.
```

Chương trình đúng:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao lop 6!";
    return 0;
}
```

---

## Bài 4: Đoán kết quả

Chương trình sau in ra gì?

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "C++ rat thu vi";
    return 0;
}
```

Đáp án:

```text
C++ rat thu vi
```

---

## Bài 5: Viết chương trình

Viết chương trình in ra dòng chữ:

```text
Em dang hoc bai 2
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Em dang hoc bai 2";
    return 0;
}
```

---

# 20. Bài tập thực hành nâng cao nhẹ

## Bài 1

Viết chương trình in ra 2 dòng:

```text
Xin chao!
Toi la hoc sinh lop 6.
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao!" << endl;
    cout << "Toi la hoc sinh lop 6.";
    return 0;
}
```

---

## Bài 2

Viết chương trình in ra hình sau:

```text
*
**
***
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "*" << endl;
    cout << "**" << endl;
    cout << "***";
    return 0;
}
```

---

## Bài 3

Viết chương trình in ra khung tên:

```text
==========
Ten: Nam
Lop: 6A
==========
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "==========" << endl;
    cout << "Ten: Nam" << endl;
    cout << "Lop: 6A" << endl;
    cout << "==========";
    return 0;
}
```

---

# 21. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. Môi trường lập trình dùng để làm gì?
2. File C++ có đuôi gì?
3. Lệnh `cout` dùng để làm gì?
4. Khi in chữ, ta đặt chữ trong dấu gì?
5. Dấu `;` dùng để làm gì?
6. `endl` dùng để làm gì?

Gợi ý trả lời:

```text
1. Dùng để viết, lưu và chạy chương trình.
2. File C++ có đuôi .cpp.
3. cout dùng để in ra màn hình.
4. Đặt chữ trong dấu ngoặc kép " ".
5. Dấu ; dùng để kết thúc câu lệnh.
6. endl dùng để xuống dòng.
```

---

# 22. Bài tập về nhà

## Bài 1

Viết chương trình in ra tên của em.

Ví dụ kết quả:

```text
Ten cua em la An
```

---

## Bài 2

Viết chương trình in ra 3 dòng giới thiệu bản thân:

```text
Ten cua em la ...
Em hoc lop ...
Em thich ...
```

---

## Bài 3

Viết chương trình in ra hình sau:

```text
*****
*   *
*****
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "*****" << endl;
    cout << "*   *" << endl;
    cout << "*****";
    return 0;
}
```

---

# 23. Tóm tắt bài học

Học sinh cần nhớ:

```text
Môi trường lập trình giúp viết và chạy chương trình.
File C++ có đuôi .cpp.
Chương trình C++ bắt đầu chạy từ hàm main.
cout dùng để in ra màn hình.
Dấu ; dùng để kết thúc câu lệnh.
Dấu " " dùng để chứa chữ cần in.
endl dùng để xuống dòng.
```

---

# 24. Gợi ý thời lượng dạy

| Phần                              | Thời lượng |
| --------------------------------- | ---------: |
| Ôn bài cũ                         |     5 phút |
| Giới thiệu môi trường lập trình   |     7 phút |
| Tạo file và chạy chương trình mẫu |    10 phút |
| Giải thích chương trình đầu tiên  |     8 phút |
| Thực hành sửa nội dung `cout`     |    10 phút |
| Bài tập in nhiều dòng             |    10 phút |
| Củng cố và giao bài tập           |     5 phút |

Tổng thời lượng: khoảng **50–55 phút**.
