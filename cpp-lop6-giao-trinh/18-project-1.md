# Bài 18: Dự án nhỏ 1 — Máy tính mini

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Ôn lại biến, nhập xuất, phép toán.
* Biết dùng `if else if` để xử lý nhiều lựa chọn.
* Biết viết chương trình máy tính mini.
* Biết nhập 2 số và chọn phép toán.
* Biết xử lý các phép:

  * Cộng
  * Trừ
  * Nhân
  * Chia
* Biết tránh lỗi chia cho `0`.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Mảng dùng để làm gì?
2. `cin` dùng để làm gì?
3. `cout` dùng để làm gì?
4. Câu lệnh `if else if` dùng khi nào?
5. Trong C++, phép nhân viết bằng ký hiệu gì?
6. Trong C++, phép chia viết bằng ký hiệu gì?

Gợi ý trả lời:

```text
1. Mảng dùng để lưu nhiều giá trị cùng kiểu dữ liệu.
2. cin dùng để nhập dữ liệu.
3. cout dùng để in dữ liệu.
4. if else if dùng khi có nhiều trường hợp.
5. Phép nhân dùng dấu *.
6. Phép chia dùng dấu /.
```

Dẫn vào bài mới:

> Hôm nay chúng ta sẽ làm một chương trình nhỏ giống máy tính bỏ túi.
> Người dùng nhập hai số, chọn phép toán, chương trình sẽ in ra kết quả.

---

# 3. Ý tưởng dự án

Chương trình máy tính mini sẽ làm các việc sau:

```text
1. Nhập số thứ nhất.
2. Nhập số thứ hai.
3. Hiển thị menu phép toán.
4. Người dùng chọn phép toán.
5. Chương trình tính kết quả.
6. In kết quả ra màn hình.
```

Ví dụ khi chạy:

```text
Nhap so thu nhat: 10
Nhap so thu hai: 5

===== MAY TINH MINI =====
1. Cong
2. Tru
3. Nhan
4. Chia
Chon phep tinh: 1

Ket qua: 15
```

---

# 4. Kiến thức cần dùng

Dự án này dùng lại các kiến thức đã học:

| Kiến thức          | Dùng để làm gì?     |
| ------------------ | ------------------- |
| `int`, `float`     | Lưu số              |
| `cin`              | Nhập dữ liệu        |
| `cout`             | In dữ liệu          |
| `+`, `-`, `*`, `/` | Tính toán           |
| `if else if`       | Xử lý lựa chọn      |
| `if`               | Kiểm tra chia cho 0 |

---

# 5. Phân tích bài toán

## Đề bài

Viết chương trình máy tính mini. Người dùng nhập hai số, sau đó chọn phép toán cộng, trừ, nhân hoặc chia. Chương trình in ra kết quả.

## Phân tích

```text
Đầu vào:
- soA
- soB
- luaChon

Xử lý:
- Nếu luaChon == 1 thì tính soA + soB
- Nếu luaChon == 2 thì tính soA - soB
- Nếu luaChon == 3 thì tính soA * soB
- Nếu luaChon == 4 thì tính soA / soB
- Nếu chia thì cần kiểm tra soB có bằng 0 không

Đầu ra:
- Kết quả phép tính
```

---

# 6. Bước 1: Nhập hai số

Trước tiên, ta cho người dùng nhập hai số.

```cpp
#include <iostream>
using namespace std;

int main() {
    float soA, soB;

    cout << "Nhap so thu nhat: ";
    cin >> soA;

    cout << "Nhap so thu hai: ";
    cin >> soB;

    return 0;
}
```

Ở đây dùng `float` để có thể nhập số thập phân như `8.5`, `3.2`.

---

# 7. Bước 2: Hiển thị menu phép toán

Sau khi nhập hai số, ta hiển thị menu:

```cpp
cout << "===== MAY TINH MINI =====" << endl;
cout << "1. Cong" << endl;
cout << "2. Tru" << endl;
cout << "3. Nhan" << endl;
cout << "4. Chia" << endl;
```

Chương trình đầy đủ hơn:

```cpp
#include <iostream>
using namespace std;

int main() {
    float soA, soB;

    cout << "Nhap so thu nhat: ";
    cin >> soA;

    cout << "Nhap so thu hai: ";
    cin >> soB;

    cout << endl;
    cout << "===== MAY TINH MINI =====" << endl;
    cout << "1. Cong" << endl;
    cout << "2. Tru" << endl;
    cout << "3. Nhan" << endl;
    cout << "4. Chia" << endl;

    return 0;
}
```

---

# 8. Bước 3: Nhập lựa chọn

Ta cần thêm biến `luaChon`.

```cpp
int luaChon;

cout << "Chon phep tinh: ";
cin >> luaChon;
```

Ví dụ:

```cpp
int luaChon;

cout << "Chon phep tinh: ";
cin >> luaChon;
```

Nếu người dùng nhập:

```text
1
```

thì chương trình hiểu là chọn phép cộng.

---

# 9. Bước 4: Xử lý lựa chọn bằng `if else if`

Ta dùng `if else if` để xử lý từng trường hợp.

```cpp
if (luaChon == 1) {
    cout << "Ket qua: " << soA + soB;
} else if (luaChon == 2) {
    cout << "Ket qua: " << soA - soB;
} else if (luaChon == 3) {
    cout << "Ket qua: " << soA * soB;
} else if (luaChon == 4) {
    cout << "Ket qua: " << soA / soB;
} else {
    cout << "Lua chon khong hop le";
}
```

Giải thích:

```text
luaChon == 1  → cộng
luaChon == 2  → trừ
luaChon == 3  → nhân
luaChon == 4  → chia
Khác 1,2,3,4  → lựa chọn không hợp lệ
```

---

# 10. Chương trình hoàn chỉnh phiên bản 1

```cpp
#include <iostream>
using namespace std;

int main() {
    float soA, soB;
    int luaChon;

    cout << "Nhap so thu nhat: ";
    cin >> soA;

    cout << "Nhap so thu hai: ";
    cin >> soB;

    cout << endl;
    cout << "===== MAY TINH MINI =====" << endl;
    cout << "1. Cong" << endl;
    cout << "2. Tru" << endl;
    cout << "3. Nhan" << endl;
    cout << "4. Chia" << endl;

    cout << "Chon phep tinh: ";
    cin >> luaChon;

    if (luaChon == 1) {
        cout << "Ket qua: " << soA + soB;
    } else if (luaChon == 2) {
        cout << "Ket qua: " << soA - soB;
    } else if (luaChon == 3) {
        cout << "Ket qua: " << soA * soB;
    } else if (luaChon == 4) {
        cout << "Ket qua: " << soA / soB;
    } else {
        cout << "Lua chon khong hop le";
    }

    return 0;
}
```

Ví dụ chạy:

```text
Nhap so thu nhat: 10
Nhap so thu hai: 5

===== MAY TINH MINI =====
1. Cong
2. Tru
3. Nhan
4. Chia
Chon phep tinh: 3
Ket qua: 50
```

---

# 11. Vấn đề khi chia cho 0

Trong toán học, không được chia cho `0`.

Ví dụ:

```text
10 / 0
```

là không hợp lệ.

Vì vậy, khi người dùng chọn phép chia, ta cần kiểm tra:

```cpp
if (soB == 0) {
    cout << "Khong the chia cho 0";
} else {
    cout << "Ket qua: " << soA / soB;
}
```

---

# 12. Chương trình hoàn chỉnh phiên bản 2

Phiên bản này có kiểm tra chia cho `0`.

```cpp
#include <iostream>
using namespace std;

int main() {
    float soA, soB;
    int luaChon;

    cout << "Nhap so thu nhat: ";
    cin >> soA;

    cout << "Nhap so thu hai: ";
    cin >> soB;

    cout << endl;
    cout << "===== MAY TINH MINI =====" << endl;
    cout << "1. Cong" << endl;
    cout << "2. Tru" << endl;
    cout << "3. Nhan" << endl;
    cout << "4. Chia" << endl;

    cout << "Chon phep tinh: ";
    cin >> luaChon;

    if (luaChon == 1) {
        cout << "Ket qua: " << soA + soB;
    } else if (luaChon == 2) {
        cout << "Ket qua: " << soA - soB;
    } else if (luaChon == 3) {
        cout << "Ket qua: " << soA * soB;
    } else if (luaChon == 4) {
        if (soB == 0) {
            cout << "Khong the chia cho 0";
        } else {
            cout << "Ket qua: " << soA / soB;
        }
    } else {
        cout << "Lua chon khong hop le";
    }

    return 0;
}
```

Ví dụ chạy 1:

```text
Nhap so thu nhat: 10
Nhap so thu hai: 2

===== MAY TINH MINI =====
1. Cong
2. Tru
3. Nhan
4. Chia
Chon phep tinh: 4
Ket qua: 5
```

Ví dụ chạy 2:

```text
Nhap so thu nhat: 10
Nhap so thu hai: 0

===== MAY TINH MINI =====
1. Cong
2. Tru
3. Nhan
4. Chia
Chon phep tinh: 4
Khong the chia cho 0
```

---

# 13. Phiên bản dùng ký tự phép toán

Ngoài cách chọn số `1`, `2`, `3`, `4`, ta có thể cho người dùng nhập ký tự phép toán như `+`, `-`, `*`, `/`.

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    float a, b;
    char phepTinh;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Nhap phep tinh (+, -, *, /): ";
    cin >> phepTinh;

    if (phepTinh == '+') {
        cout << "Ket qua: " << a + b;
    } else if (phepTinh == '-') {
        cout << "Ket qua: " << a - b;
    } else if (phepTinh == '*') {
        cout << "Ket qua: " << a * b;
    } else if (phepTinh == '/') {
        if (b == 0) {
            cout << "Khong the chia cho 0";
        } else {
            cout << "Ket qua: " << a / b;
        }
    } else {
        cout << "Phep tinh khong hop le";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap a: 8
Nhap b: 4
Nhap phep tinh (+, -, *, /): /
Ket qua: 2
```

---

# 14. Nên dạy phiên bản nào?

Với học sinh lớp 6, nên dạy theo thứ tự:

```text
1. Phiên bản chọn số: 1, 2, 3, 4
2. Sau đó giới thiệu phiên bản chọn ký tự: +, -, *, /
```

Vì phiên bản chọn số dễ hiểu hơn khi mới học `if else if`.

---

# 15. Lỗi thường gặp

## Lỗi 1: Dùng `=` thay vì `==`

Sai:

```cpp
if (luaChon = 1) {
    cout << soA + soB;
}
```

Đúng:

```cpp
if (luaChon == 1) {
    cout << soA + soB;
}
```

Nhắc lại:

```text
=  dùng để gán
== dùng để so sánh
```

---

## Lỗi 2: Quên xử lý chia cho 0

Sai:

```cpp
cout << soA / soB;
```

Nếu `soB = 0`, chương trình có thể lỗi.

Đúng:

```cpp
if (soB == 0) {
    cout << "Khong the chia cho 0";
} else {
    cout << soA / soB;
}
```

---

## Lỗi 3: Nhầm dấu phép toán

Sai:

```cpp
cout << soA x soB;
```

Đúng:

```cpp
cout << soA * soB;
```

Sai:

```cpp
cout << soA : soB;
```

Đúng:

```cpp
cout << soA / soB;
```

---

## Lỗi 4: Không có trường hợp lựa chọn sai

Nên luôn có phần:

```cpp
else {
    cout << "Lua chon khong hop le";
}
```

Để xử lý khi người dùng nhập sai lựa chọn.

---

# 16. Hoạt động trên lớp

## Hoạt động 1: Phân tích dự án

Yêu cầu học sinh điền:

```text
Đầu vào:
- ...

Xử lý:
- ...

Đầu ra:
- ...
```

Đáp án gợi ý:

```text
Đầu vào:
- soA
- soB
- luaChon

Xử lý:
- 1: cộng
- 2: trừ
- 3: nhân
- 4: chia
- Nếu chia cho 0 thì báo lỗi

Đầu ra:
- kết quả phép tính hoặc thông báo lỗi
```

---

## Hoạt động 2: Viết menu

Yêu cầu học sinh viết đoạn code in menu:

```text
===== MAY TINH MINI =====
1. Cong
2. Tru
3. Nhan
4. Chia
```

Gợi ý:

```cpp
cout << "===== MAY TINH MINI =====" << endl;
cout << "1. Cong" << endl;
cout << "2. Tru" << endl;
cout << "3. Nhan" << endl;
cout << "4. Chia" << endl;
```

---

## Hoạt động 3: Hoàn thiện chương trình

Giáo viên cho khung code và học sinh điền phần còn thiếu.

```cpp
#include <iostream>
using namespace std;

int main() {
    float soA, soB;
    int luaChon;

    cout << "Nhap so thu nhat: ";
    cin >> soA;

    cout << "Nhap so thu hai: ";
    cin >> soB;

    cout << "1. Cong" << endl;
    cout << "2. Tru" << endl;
    cout << "3. Nhan" << endl;
    cout << "4. Chia" << endl;

    cout << "Chon phep tinh: ";
    cin >> luaChon;

    // Hoc sinh viet if else if o day

    return 0;
}
```

---

# 17. Bài tập trên lớp

## Bài 1

Viết chương trình nhập hai số `a`, `b`, sau đó in:

```text
Tong: ...
Hieu: ...
Tich: ...
Thuong: ...
```

Chưa cần menu.

---

## Bài 2

Viết menu sau bằng `cout`:

```text
===== MENU =====
1. Cong
2. Tru
3. Nhan
4. Chia
```

---

## Bài 3

Viết chương trình nhập hai số và một lựa chọn.

Nếu lựa chọn là `1` thì in tổng.

Nếu lựa chọn là `2` thì in hiệu.

---

## Bài 4

Hoàn thiện máy tính mini với 4 phép toán:

```text
1. Cong
2. Tru
3. Nhan
4. Chia
```

---

## Bài 5

Thêm kiểm tra chia cho `0`.

Nếu người dùng chọn phép chia và số thứ hai bằng `0`, in:

```text
Khong the chia cho 0
```

---

# 18. Bài tập thực hành nâng cao nhẹ

## Bài 1: Máy tính mini dùng ký tự

Viết chương trình nhập:

```text
a
b
phepTinh
```

Trong đó `phepTinh` là một trong các ký tự:

```text
+
-
*
/
```

Sau đó in kết quả.

---

## Bài 2: Máy tính diện tích

Viết chương trình có menu:

```text
1. Tinh dien tich hinh vuong
2. Tinh dien tich hinh chu nhat
3. Tinh chu vi hinh vuong
4. Tinh chu vi hinh chu nhat
```

Người dùng chọn chức năng, sau đó nhập dữ liệu cần thiết và in kết quả.

Gợi ý công thức:

```text
Dien tich hinh vuong = canh * canh
Chu vi hinh vuong = canh * 4
Dien tich hinh chu nhat = dai * rong
Chu vi hinh chu nhat = (dai + rong) * 2
```

---

# 19. Câu hỏi củng cố

Giáo viên hỏi học sinh:

1. Dự án máy tính mini cần những đầu vào nào?
2. Vì sao cần dùng `if else if`?
3. Khi chọn phép cộng, điều kiện là gì?
4. Khi chọn phép chia, cần kiểm tra điều gì?
5. Vì sao không được chia cho `0`?
6. Dấu `=` và `==` khác nhau thế nào?
7. Nếu người dùng nhập lựa chọn `5`, chương trình nên làm gì?

Gợi ý trả lời:

```text
1. Cần nhập hai số và lựa chọn phép toán.
2. Vì có nhiều phép toán để chọn.
3. luaChon == 1.
4. Kiểm tra số thứ hai có bằng 0 không.
5. Vì trong toán học không thể chia cho 0.
6. = là gán, == là so sánh.
7. In "Lua chon khong hop le".
```

---

# 20. Bài tập về nhà

## Bài 1

Viết chương trình máy tính mini có menu:

```text
1. Cong
2. Tru
3. Nhan
4. Chia
```

Người dùng nhập hai số và chọn phép toán.

---

## Bài 2

Thêm kiểm tra chia cho `0` vào bài 1.

---

## Bài 3

Viết máy tính mini dùng ký tự phép toán:

```text
+
-
*
/
```

Ví dụ:

```text
Nhap a: 10
Nhap b: 5
Nhap phep tinh: *
Ket qua: 50
```

---

## Bài 4

Viết chương trình menu hình học:

```text
1. Chu vi hinh vuong
2. Dien tich hinh vuong
3. Chu vi hinh chu nhat
4. Dien tich hinh chu nhat
```

---

# 21. Tóm tắt bài học

Học sinh cần nhớ:

```text
Dự án máy tính mini dùng các kiến thức:

- Biến để lưu số
- cin để nhập dữ liệu
- cout để in kết quả
- if else if để xử lý lựa chọn
- Phép toán +, -, *, /
- if để kiểm tra chia cho 0
```

Mẫu xử lý lựa chọn:

```cpp
if (luaChon == 1) {
    cout << "Ket qua: " << soA + soB;
} else if (luaChon == 2) {
    cout << "Ket qua: " << soA - soB;
} else if (luaChon == 3) {
    cout << "Ket qua: " << soA * soB;
} else if (luaChon == 4) {
    if (soB == 0) {
        cout << "Khong the chia cho 0";
    } else {
        cout << "Ket qua: " << soA / soB;
    }
} else {
    cout << "Lua chon khong hop le";
}
```

---

# 22. Gợi ý thời lượng dạy 60 phút

| Phần                                | Thời lượng |
| ----------------------------------- | ---------: |
| Ôn bài cũ                           |     5 phút |
| Giới thiệu dự án máy tính mini      |     5 phút |
| Phân tích đầu vào, xử lý, đầu ra    |     8 phút |
| Viết chương trình phiên bản chọn số |    15 phút |
| Xử lý chia cho 0                    |     7 phút |
| Thực hành hoàn thiện chương trình   |    15 phút |
| Củng cố và giao bài tập             |     5 phút |

Tổng: **60 phút**.
