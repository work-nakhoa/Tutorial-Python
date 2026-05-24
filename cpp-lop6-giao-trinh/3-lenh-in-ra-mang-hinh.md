# Bài 3: Lệnh in ra màn hình `cout`

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu `cout` dùng để in nội dung ra màn hình.
* Biết in chữ, in số, in nhiều dòng.
* Biết dùng `endl` và `\n` để xuống dòng.
* Biết kết hợp nhiều nội dung trong một lệnh `cout`.
* Biết sửa một số lỗi thường gặp khi dùng `cout`.
* Tự viết được chương trình in thông tin cá nhân, thời khóa biểu, hình đơn giản bằng dấu `*`.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. File C++ thường có đuôi gì?
2. Chương trình C++ bắt đầu chạy từ đâu?
3. Lệnh `cout` dùng để làm gì?
4. Dấu `;` dùng để làm gì?
5. Khi in chữ, ta đặt chữ trong dấu gì?

Gợi ý trả lời:

```text
1. File C++ có đuôi .cpp.
2. Chương trình bắt đầu chạy từ hàm main.
3. cout dùng để in ra màn hình.
4. Dấu ; dùng để kết thúc câu lệnh.
5. Khi in chữ, ta đặt chữ trong dấu ngoặc kép " ".
```

Giáo viên dẫn vào bài mới:

> Ở bài trước, các em đã biết chạy chương trình C++ đầu tiên.
> Hôm nay, chúng ta sẽ học kỹ hơn về lệnh `cout`, tức là lệnh dùng để in nội dung ra màn hình.

---

# 3. `cout` là gì?

## Giải thích đơn giản

Trong C++, `cout` là lệnh dùng để **in nội dung ra màn hình**.

Ví dụ:

```cpp
cout << "Xin chao!";
```

Kết quả:

```text
Xin chao!
```

Giáo viên giải thích:

> Khi muốn máy tính hiển thị chữ, số hoặc kết quả ra màn hình, chúng ta dùng `cout`.

---

# 4. Cấu trúc cơ bản của lệnh `cout`

Cấu trúc:

```cpp
cout << noi_dung_can_in;
```

Ví dụ:

```cpp
cout << "Hom nay em hoc C++";
```

Kết quả:

```text
Hom nay em hoc C++
```

Trong đó:

| Thành phần             | Ý nghĩa                  |
| ---------------------- | ------------------------ |
| `cout`                 | Lệnh in ra màn hình      |
| `<<`                   | Đưa nội dung ra màn hình |
| `"Hom nay em hoc C++"` | Nội dung cần in          |
| `;`                    | Kết thúc câu lệnh        |

Giáo viên có thể nói:

> Các em có thể hiểu đơn giản là:
> `cout` nghĩa là “hãy in ra”, còn `<<` nghĩa là “nội dung này”.

---

# 5. Chương trình mẫu

Giáo viên cho học sinh gõ chương trình sau:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao lop 6!";
    return 0;
}
```

Kết quả:

```text
Xin chao lop 6!
```

Giáo viên nhắc lại:

> Trong bài này, chúng ta tập trung vào dòng:
>
> ```cpp
> cout << "Xin chao lop 6!";
> ```

---

# 6. In chữ ra màn hình

Khi muốn in chữ, ta đặt chữ trong dấu ngoặc kép `" "`.

Ví dụ:

```cpp
cout << "Em dang hoc lap trinh";
```

Kết quả:

```text
Em dang hoc lap trinh
```

Ví dụ chương trình hoàn chỉnh:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Em dang hoc lap trinh";
    return 0;
}
```

Giáo viên nhấn mạnh:

> Nội dung nào nằm trong dấu `" "` thì sẽ được in ra màn hình.

---

# 7. In số ra màn hình

Khi in số, ta có thể không cần đặt trong dấu ngoặc kép.

Ví dụ:

```cpp
cout << 123;
```

Kết quả:

```text
123
```

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << 2026;
    return 0;
}
```

Kết quả:

```text
2026
```

So sánh:

```cpp
cout << "123";
cout << 123;
```

Cả hai đều có thể in ra:

```text
123
```

Nhưng ý nghĩa khác nhau:

| Cách viết | Ý nghĩa        |
| --------- | -------------- |
| `"123"`   | Xem 123 là chữ |
| `123`     | Xem 123 là số  |

Ở bài này, học sinh chỉ cần nhớ:

> In chữ thì đặt trong `" "`.
> In số thì có thể không cần `" "`.

---

# 8. In phép tính ra màn hình

`cout` có thể in kết quả của phép tính.

Ví dụ:

```cpp
cout << 5 + 3;
```

Kết quả:

```text
8
```

Ví dụ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << 5 + 3;
    return 0;
}
```

Kết quả:

```text
8
```

Một số ví dụ khác:

```cpp
cout << 10 - 4;
cout << 6 * 2;
cout << 20 / 5;
```

Kết quả lần lượt là:

```text
6
12
4
```

Lưu ý cho giáo viên:

> Ở bài này chỉ giới thiệu nhẹ việc `cout` có thể in kết quả phép tính.
> Các phép toán sẽ được học kỹ hơn ở bài sau.

---

# 9. In chữ kèm số

Ta có thể in chữ và số trong cùng một câu lệnh bằng cách dùng nhiều dấu `<<`.

Ví dụ:

```cpp
cout << "Nam nay em " << 11 << " tuoi";
```

Kết quả:

```text
Nam nay em 11 tuoi
```

Giải thích:

```text
"Nam nay em "  → in chữ Nam nay em
11             → in số 11
" tuoi"        → in chữ tuoi
```

Ví dụ chương trình hoàn chỉnh:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Nam nay em " << 11 << " tuoi";
    return 0;
}
```

---

# 10. In nhiều dòng với `endl`

Nếu muốn xuống dòng, ta dùng `endl`.

Ví dụ:

```cpp
cout << "Dong 1" << endl;
cout << "Dong 2";
```

Kết quả:

```text
Dong 1
Dong 2
```

Chương trình mẫu:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao!" << endl;
    cout << "Em dang hoc C++" << endl;
    cout << "Hom nay la bai 3";

    return 0;
}
```

Kết quả:

```text
Xin chao!
Em dang hoc C++
Hom nay la bai 3
```

Giải thích:

> `endl` nghĩa là kết thúc dòng hiện tại và xuống dòng mới.

---

# 11. In nhiều dòng với `\n`

Ngoài `endl`, ta cũng có thể dùng `\n` để xuống dòng.

Ví dụ:

```cpp
cout << "Dong 1\nDong 2";
```

Kết quả:

```text
Dong 1
Dong 2
```

Chương trình mẫu:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao!\n";
    cout << "Em dang hoc C++\n";
    cout << "Day la bai 3";

    return 0;
}
```

Kết quả:

```text
Xin chao!
Em dang hoc C++
Day la bai 3
```

So sánh đơn giản:

| Cách xuống dòng | Ví dụ                         |
| --------------- | ----------------------------- |
| Dùng `endl`     | `cout << "Xin chao" << endl;` |
| Dùng `\n`       | `cout << "Xin chao\n";`       |

Với học sinh lớp 6, có thể cho học trước `endl`, sau đó giới thiệu thêm `\n`.

---

# 12. In nhiều nội dung trong một lệnh `cout`

Ta có thể viết:

```cpp
cout << "Ten: " << "Nam" << endl << "Lop: " << "6A";
```

Kết quả:

```text
Ten: Nam
Lop: 6A
```

Tuy nhiên, với học sinh mới học, nên viết dễ nhìn hơn:

```cpp
cout << "Ten: Nam" << endl;
cout << "Lop: 6A";
```

Giáo viên nhấn mạnh:

> Code dễ đọc thì dễ sửa lỗi hơn.

---

# 13. Quy tắc quan trọng khi dùng `cout`

Học sinh cần nhớ 5 quy tắc:

```text
1. Muốn in ra màn hình thì dùng cout.
2. Muốn in chữ thì đặt chữ trong dấu " ".
3. Mỗi câu lệnh thường kết thúc bằng dấu ;.
4. Muốn xuống dòng thì dùng endl hoặc \n.
5. Gõ đúng từng ký tự, vì máy tính không tự đoán lỗi.
```

---

# 14. Hoạt động thực hành 1: In lời chào

Yêu cầu học sinh viết chương trình in ra:

```text
Xin chao cac ban!
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao cac ban!";
    return 0;
}
```

---

# 15. Hoạt động thực hành 2: In thông tin cá nhân

Yêu cầu học sinh viết chương trình in ra 3 dòng:

```text
Ten: ...
Lop: ...
So thich: ...
```

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Ten: Nam" << endl;
    cout << "Lop: 6A" << endl;
    cout << "So thich: bong da";

    return 0;
}
```

Kết quả:

```text
Ten: Nam
Lop: 6A
So thich: bong da
```

---

# 16. Hoạt động thực hành 3: In thời khóa biểu

Yêu cầu học sinh viết chương trình in thời khóa biểu một ngày.

Ví dụ kết quả:

```text
Thoi khoa bieu thu Hai
Tiet 1: Toan
Tiet 2: Van
Tiet 3: Anh
Tiet 4: Tin hoc
```

Gợi ý chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Thoi khoa bieu thu Hai" << endl;
    cout << "Tiet 1: Toan" << endl;
    cout << "Tiet 2: Van" << endl;
    cout << "Tiet 3: Anh" << endl;
    cout << "Tiet 4: Tin hoc";

    return 0;
}
```

---

# 17. Hoạt động thực hành 4: In hình bằng dấu sao

Yêu cầu học sinh in hình tam giác:

```text
*
**
***
****
```

Gợi ý chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "*" << endl;
    cout << "**" << endl;
    cout << "***" << endl;
    cout << "****";

    return 0;
}
```

Giáo viên giải thích:

> Đây là cách đầu tiên để tạo hình bằng lập trình.
> Sau này khi học vòng lặp, chúng ta sẽ in hình này ngắn hơn.

---

# 18. Hoạt động thực hành 5: In khung tên

Yêu cầu học sinh in ra:

```text
================
Ten: An
Lop: 6A
================
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "================" << endl;
    cout << "Ten: An" << endl;
    cout << "Lop: 6A" << endl;
    cout << "================";

    return 0;
}
```

---

# 19. Lỗi thường gặp khi dùng `cout`

## Lỗi 1: Quên dấu `;`

Sai:

```cpp
cout << "Xin chao"
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích:

> Dấu `;` báo cho máy tính biết câu lệnh đã kết thúc.

---

## Lỗi 2: Quên dấu ngoặc kép

Sai:

```cpp
cout << Xin chao;
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích:

> Khi in chữ, phải đặt chữ trong dấu `" "`.

---

## Lỗi 3: Gõ sai `cout`

Sai:

```cpp
count << "Xin chao";
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích:

> `cout` phải viết đúng là c-o-u-t.

---

## Lỗi 4: Viết sai dấu `<<`

Sai:

```cpp
cout < "Xin chao";
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích:

> Sau `cout` phải là hai dấu bé hơn: `<<`.

---

## Lỗi 5: Dùng nhầm dấu nháy đơn

Sai:

```cpp
cout << 'Xin chao';
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích đơn giản:

> Khi in một câu hoặc một dòng chữ, ta dùng dấu ngoặc kép `" "`.
> Dấu nháy đơn `' '` sẽ học sau, dùng cho một ký tự.

---

# 20. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

Lệnh nào dùng để in ra màn hình?

A. `cin`
B. `cout`
C. `main`
D. `return`

Đáp án: **B**

---

## Bài 2: Điền từ còn thiếu

```text
Muốn in chữ trong C++, ta đặt chữ trong dấu ______.
```

Đáp án:

```text
ngoặc kép " "
```

---

## Bài 3: Đoán kết quả

Chương trình sau in ra gì?

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hoc C++ rat vui";
    return 0;
}
```

Đáp án:

```text
Hoc C++ rat vui
```

---

## Bài 4: Đoán kết quả

Chương trình sau in ra gì?

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << 10 + 5;
    return 0;
}
```

Đáp án:

```text
15
```

---

## Bài 5: Sửa lỗi chương trình

Chương trình sau bị lỗi. Hãy sửa lại:

```cpp
#include <iostream>
using namespace std;

int main() {
    count << "Xin chao";
    return 0;
}
```

Lỗi:

```text
Viết sai cout thành count.
```

Chương trình đúng:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao";
    return 0;
}
```

---

## Bài 6: Sửa lỗi chương trình

Chương trình sau bị lỗi. Hãy sửa lại:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Em hoc lop 6"
    return 0;
}
```

Lỗi:

```text
Thiếu dấu ; sau lệnh cout.
```

Chương trình đúng:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Em hoc lop 6";
    return 0;
}
```

---

# 21. Bài tập thực hành

## Bài 1

Viết chương trình in ra dòng chữ:

```text
Xin chao thay co va cac ban!
```

---

## Bài 2

Viết chương trình in ra 3 dòng:

```text
Em ten la ...
Em hoc lop ...
Em thich ...
```

---

## Bài 3

Viết chương trình in ra:

```text
Ket qua cua 7 + 8 la:
15
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Ket qua cua 7 + 8 la:" << endl;
    cout << 7 + 8;

    return 0;
}
```

---

## Bài 4

Viết chương trình in ra hình:

```text
*****
*****
*****
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "*****" << endl;
    cout << "*****" << endl;
    cout << "*****";

    return 0;
}
```

---

## Bài 5

Viết chương trình in ra hình:

```text
   *
  ***
 *****
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "   *" << endl;
    cout << "  ***" << endl;
    cout << " *****";

    return 0;
}
```

---

# 22. Bài tập nâng cao nhẹ

## Bài 1: In bảng thông tin

Viết chương trình in ra:

```text
====================
  THONG TIN HOC SINH
====================
Ten: An
Lop: 6A
Truong: THCS Hoa Binh
====================
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "====================" << endl;
    cout << "  THONG TIN HOC SINH" << endl;
    cout << "====================" << endl;
    cout << "Ten: An" << endl;
    cout << "Lop: 6A" << endl;
    cout << "Truong: THCS Hoa Binh" << endl;
    cout << "====================";

    return 0;
}
```

---

## Bài 2: In menu đơn giản

Viết chương trình in ra menu:

```text
===== MENU =====
1. Bat dau
2. Huong dan
3. Thoat
================
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "===== MENU =====" << endl;
    cout << "1. Bat dau" << endl;
    cout << "2. Huong dan" << endl;
    cout << "3. Thoat" << endl;
    cout << "================";

    return 0;
}
```

---

# 23. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. `cout` dùng để làm gì?
2. Khi in chữ, ta cần dùng dấu gì?
3. Dấu `;` có tác dụng gì?
4. Muốn xuống dòng, ta có thể dùng gì?
5. Lệnh nào đúng: `cout < "Hi";` hay `cout << "Hi";`?
6. Chương trình sau in ra gì?

```cpp
cout << 4 + 6;
```

Gợi ý trả lời:

```text
1. cout dùng để in ra màn hình.
2. Dùng dấu ngoặc kép " ".
3. Dấu ; dùng để kết thúc câu lệnh.
4. Dùng endl hoặc \n.
5. Đúng là cout << "Hi";
6. In ra 10.
```

---

# 24. Bài tập về nhà

## Bài 1

Viết chương trình in ra tên của em.

Ví dụ:

```text
Ten cua em la Lan
```

---

## Bài 2

Viết chương trình in ra 4 dòng giới thiệu bản thân:

```text
Xin chao!
Ten cua em la ...
Em hoc lop ...
Em thich ...
```

---

## Bài 3

Viết chương trình in ra thời khóa biểu ngày thứ Ba gồm ít nhất 5 tiết học.

Ví dụ:

```text
Thoi khoa bieu thu Ba
Tiet 1: Toan
Tiet 2: Van
Tiet 3: Anh
Tiet 4: Khoa hoc
Tiet 5: Tin hoc
```

---

## Bài 4

Viết chương trình in ra hình sau:

```text
*
**
***
****
*****
```

---

## Bài 5

Tìm lỗi trong chương trình sau và sửa lại:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << Hom nay em hoc C++;
    return 0;
}
```

Đáp án gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hom nay em hoc C++";
    return 0;
}
```

Lỗi là thiếu dấu ngoặc kép quanh nội dung cần in.

---

# 25. Tóm tắt bài học

Học sinh cần nhớ:

```text
cout dùng để in nội dung ra màn hình.
In chữ thì đặt trong dấu ngoặc kép " ".
In số thì có thể không cần dấu ngoặc kép.
Dấu << dùng để đưa nội dung ra màn hình.
Dấu ; dùng để kết thúc câu lệnh.
endl hoặc \n dùng để xuống dòng.
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Noi dung can in";
    return 0;
}
```

---

# 26. Gợi ý thời lượng dạy

| Phần                           | Thời lượng |
| ------------------------------ | ---------: |
| Ôn bài cũ                      |     5 phút |
| Giới thiệu `cout`              |     7 phút |
| In chữ, in số, in phép tính    |    10 phút |
| In nhiều dòng với `endl`, `\n` |    10 phút |
| Thực hành in thông tin cá nhân |    10 phút |
| Thực hành in hình bằng dấu sao |    10 phút |
| Củng cố và giao bài tập        |     5 phút |

Tổng thời lượng: khoảng **55–60 phút**.
