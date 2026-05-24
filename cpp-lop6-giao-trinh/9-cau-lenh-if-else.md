# Bài 9: Câu lệnh điều kiện `if else`

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu câu lệnh `if else` dùng để làm gì.
* Biết phân biệt `if` và `if else`.
* Biết viết chương trình xử lý 2 trường hợp: đúng và sai.
* Biết kiểm tra số chẵn/lẻ.
* Biết kiểm tra điểm đạt/chưa đạt.
* Biết kiểm tra số lớn hơn trong 2 số.
* Biết tránh lỗi nhầm `=` và `==`.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Câu lệnh `if` dùng để làm gì?
2. Điều kiện trong `if` nằm trong dấu gì?
3. Các lệnh chạy khi điều kiện đúng nằm trong dấu gì?
4. Dấu `=` dùng để làm gì?
5. Dấu `==` dùng để làm gì?
6. Điều kiện kiểm tra `n` chia hết cho 2 viết thế nào?

Gợi ý trả lời:

```text
1. if dùng để kiểm tra điều kiện.
2. Điều kiện nằm trong dấu ngoặc tròn ( ).
3. Các lệnh nằm trong dấu ngoặc nhọn { }.
4. Dấu = dùng để gán giá trị.
5. Dấu == dùng để so sánh bằng nhau.
6. n % 2 == 0
```

Giáo viên dẫn vào bài mới:

> Ở bài trước, chúng ta đã học `if`.
> Nếu điều kiện đúng thì chương trình làm một việc.
> Nhưng nếu điều kiện sai thì muốn chương trình làm việc khác thì sao?
> Hôm nay, chúng ta học câu lệnh `if else`.

---

# 3. Vấn đề của câu lệnh `if`

Ở bài trước, ta có chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 5) {
        cout << "Dat";
    }

    return 0;
}
```

Nếu nhập:

```text
8
```

Chương trình in:

```text
Dat
```

Nhưng nếu nhập:

```text
4
```

Chương trình không in gì cả.

Điều này chưa rõ ràng.

Ta muốn:

```text
Nếu điểm >= 5 thì in "Dat"
Ngược lại thì in "Chua dat"
```

Lúc này ta dùng `if else`.

---

# 4. `if else` là gì?

`if else` dùng để xử lý **hai trường hợp**:

```text
Nếu điều kiện đúng → làm việc A
Ngược lại → làm việc B
```

Cấu trúc:

```cpp
if (dieu_kien) {
    // Lệnh chạy khi điều kiện đúng
} else {
    // Lệnh chạy khi điều kiện sai
}
```

Ví dụ:

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

Nghĩa là:

```text
Nếu điểm lớn hơn hoặc bằng 5 thì in "Dat".
Ngược lại thì in "Chua dat".
```

---

# 5. So sánh `if` và `if else`

| Câu lệnh  | Ý nghĩa                                      |
| --------- | -------------------------------------------- |
| `if`      | Chỉ làm việc khi điều kiện đúng              |
| `if else` | Nếu đúng làm một việc, nếu sai làm việc khác |

Ví dụ dùng `if`:

```cpp
if (diem >= 5) {
    cout << "Dat";
}
```

Nếu điểm dưới 5, chương trình không in gì.

Ví dụ dùng `if else`:

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

Nếu điểm dưới 5, chương trình in:

```text
Chua dat
```

---

# 6. Ví dụ 1: Kiểm tra điểm đạt hay chưa đạt

## Đề bài

Nhập điểm. Nếu điểm từ 5 trở lên thì in `Dat`, ngược lại in `Chua dat`.

## Phân tích

```text
Đầu vào:
- diem

Điều kiện:
- diem >= 5

Nếu đúng:
- in "Dat"

Ngược lại:
- in "Chua dat"
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 5) {
        cout << "Dat";
    } else {
        cout << "Chua dat";
    }

    return 0;
}
```

## Ví dụ chạy chương trình

Trường hợp 1:

```text
Nhap diem: 8
Dat
```

Trường hợp 2:

```text
Nhap diem: 4
Chua dat
```

---

# 7. Ví dụ 2: Kiểm tra số chẵn hay số lẻ

## Nhắc lại

Một số nguyên chia cho 2:

```text
Nếu dư 0 → số chẵn
Nếu dư khác 0 → số lẻ
```

Điều kiện kiểm tra số chẵn:

```cpp
n % 2 == 0
```

## Đề bài

Nhập một số nguyên `n`. Kiểm tra số đó là số chẵn hay số lẻ.

## Phân tích

```text
Đầu vào:
- n

Điều kiện:
- n % 2 == 0

Nếu đúng:
- in "So chan"

Ngược lại:
- in "So le"
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n % 2 == 0) {
        cout << "So chan";
    } else {
        cout << "So le";
    }

    return 0;
}
```

## Ví dụ

```text
Nhap n: 8
So chan
```

```text
Nhap n: 7
So le
```

Giáo viên nhấn mạnh:

> Đây là bài rất quan trọng.
> Muốn kiểm tra số chẵn, ta dùng `n % 2 == 0`.

---

# 8. Ví dụ 3: Kiểm tra số dương hay không dương

## Đề bài

Nhập một số nguyên `n`. Nếu `n > 0` thì in `So duong`, ngược lại in `Khong phai so duong`.

## Phân tích

```text
Đầu vào:
- n

Điều kiện:
- n > 0

Nếu đúng:
- in "So duong"

Ngược lại:
- in "Khong phai so duong"
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n > 0) {
        cout << "So duong";
    } else {
        cout << "Khong phai so duong";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap n: 5
So duong
```

```text
Nhap n: -2
Khong phai so duong
```

```text
Nhap n: 0
Khong phai so duong
```

Giáo viên lưu ý:

> Ở bài này, `0` không được xem là số dương.

---

# 9. Ví dụ 4: Kiểm tra hai số bằng nhau hay khác nhau

## Đề bài

Nhập hai số nguyên `a`, `b`. Nếu hai số bằng nhau thì in `Bang nhau`, ngược lại in `Khac nhau`.

## Phân tích

```text
Đầu vào:
- a
- b

Điều kiện:
- a == b

Nếu đúng:
- in "Bang nhau"

Ngược lại:
- in "Khac nhau"
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    if (a == b) {
        cout << "Bang nhau";
    } else {
        cout << "Khac nhau";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap a: 6
Nhap b: 6
Bang nhau
```

```text
Nhap a: 6
Nhap b: 4
Khac nhau
```

---

# 10. Ví dụ 5: Tìm số lớn hơn trong hai số

## Đề bài

Nhập hai số nguyên `a`, `b`. In ra số lớn hơn.

## Phân tích

```text
Đầu vào:
- a
- b

Điều kiện:
- a > b

Nếu đúng:
- a lớn hơn

Ngược lại:
- b lớn hơn hoặc bằng a
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    if (a > b) {
        cout << "So lon hon la: " << a;
    } else {
        cout << "So lon hon la: " << b;
    }

    return 0;
}
```

Ví dụ:

```text
Nhap a: 9
Nhap b: 4
So lon hon la: 9
```

```text
Nhap a: 3
Nhap b: 7
So lon hon la: 7
```

Lưu ý:

Nếu nhập:

```text
a = 5
b = 5
```

Chương trình sẽ in:

```text
So lon hon la: 5
```

Vì `a > b` sai, chương trình chạy phần `else`.

Ở bài sau, khi học `else if`, ta có thể xử lý riêng trường hợp hai số bằng nhau.

---

# 11. Ví dụ 6: Kiểm tra đủ tiền mua đồ

## Đề bài

Nhập giá món đồ và số tiền em có. Nếu đủ tiền thì in `Du tien mua`, ngược lại in `Khong du tien`.

## Phân tích

```text
Đầu vào:
- giaTien
- tienCo

Điều kiện:
- tienCo >= giaTien

Nếu đúng:
- in "Du tien mua"

Ngược lại:
- in "Khong du tien"
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaTien;
    int tienCo;

    cout << "Nhap gia tien mon do: ";
    cin >> giaTien;

    cout << "Nhap so tien em co: ";
    cin >> tienCo;

    if (tienCo >= giaTien) {
        cout << "Du tien mua";
    } else {
        cout << "Khong du tien";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap gia tien mon do: 15000
Nhap so tien em co: 20000
Du tien mua
```

```text
Nhap gia tien mon do: 15000
Nhap so tien em co: 10000
Khong du tien
```

---

# 12. Ví dụ 7: Kiểm tra mật mã

## Đề bài

Nhập mật mã. Nếu mật mã bằng `1234` thì in `Dung mat ma`, ngược lại in `Sai mat ma`.

## Phân tích

```text
Đầu vào:
- matMa

Điều kiện:
- matMa == 1234

Nếu đúng:
- in "Dung mat ma"

Ngược lại:
- in "Sai mat ma"
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int matMa;

    cout << "Nhap mat ma: ";
    cin >> matMa;

    if (matMa == 1234) {
        cout << "Dung mat ma";
    } else {
        cout << "Sai mat ma";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap mat ma: 1234
Dung mat ma
```

```text
Nhap mat ma: 1111
Sai mat ma
```

---

# 13. Nhiều lệnh trong `if else`

Trong mỗi phần `if` hoặc `else`, ta có thể viết nhiều lệnh.

Ví dụ:

```cpp
if (diem >= 5) {
    cout << "Chuc mung!" << endl;
    cout << "Em da dat.";
} else {
    cout << "Rat tiec!" << endl;
    cout << "Em chua dat.";
}
```

Chương trình đầy đủ:

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 5) {
        cout << "Chuc mung!" << endl;
        cout << "Em da dat.";
    } else {
        cout << "Rat tiec!" << endl;
        cout << "Em chua dat.";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap diem: 8
Chuc mung!
Em da dat.
```

```text
Nhap diem: 4
Rat tiec!
Em chua dat.
```

---

# 14. Cách máy tính chạy `if else`

Với đoạn code:

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

Máy tính làm như sau:

```text
Bước 1: Kiểm tra diem >= 5
Bước 2: Nếu đúng, chạy phần if
Bước 3: Nếu sai, chạy phần else
Bước 4: Sau đó tiếp tục các lệnh phía dưới
```

Quan trọng:

```text
Trong if else, máy tính chỉ chạy một trong hai phần:
- hoặc phần if
- hoặc phần else
```

Không chạy cả hai phần cùng lúc.

---

# 15. Sơ đồ tư duy đơn giản

Có thể giải thích bằng lời:

```text
Nếu điều kiện đúng
    Làm việc A
Ngược lại
    Làm việc B
```

Ví dụ điểm:

```text
Nếu điểm >= 5
    In "Đạt"
Ngược lại
    In "Chưa đạt"
```

Ví dụ số chẵn/lẻ:

```text
Nếu n chia 2 dư 0
    In "Số chẵn"
Ngược lại
    In "Số lẻ"
```

---

# 16. Quy trình viết bài có `if else`

Khi làm bài có `if else`, học sinh làm theo 6 bước:

```text
Bước 1: Đọc đề bài.
Bước 2: Xác định dữ liệu cần nhập.
Bước 3: Xác định điều kiện.
Bước 4: Xác định việc cần làm nếu điều kiện đúng.
Bước 5: Xác định việc cần làm nếu điều kiện sai.
Bước 6: Viết code.
```

Ví dụ bài số chẵn/lẻ:

```text
Đề bài:
Nhập n. Kiểm tra n là số chẵn hay số lẻ.

Dữ liệu cần nhập:
- n

Điều kiện:
- n % 2 == 0

Nếu đúng:
- in "So chan"

Nếu sai:
- in "So le"
```

Code:

```cpp
if (n % 2 == 0) {
    cout << "So chan";
} else {
    cout << "So le";
}
```

---

# 17. Lỗi thường gặp khi dùng `if else`

## Lỗi 1: Viết điều kiện sau `else`

Sai:

```cpp
if (diem >= 5) {
    cout << "Dat";
} else (diem < 5) {
    cout << "Chua dat";
}
```

Đúng:

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

Giải thích:

> `else` nghĩa là “ngược lại”, nên không viết điều kiện ngay sau `else`.

---

## Lỗi 2: Dùng `=` thay vì `==`

Sai:

```cpp
if (matMa = 1234) {
    cout << "Dung mat ma";
} else {
    cout << "Sai mat ma";
}
```

Đúng:

```cpp
if (matMa == 1234) {
    cout << "Dung mat ma";
} else {
    cout << "Sai mat ma";
}
```

Nhắc lại:

```text
=  dùng để gán
== dùng để so sánh bằng nhau
```

---

## Lỗi 3: Quên dấu ngoặc nhọn `{ }`

Không nên viết:

```cpp
if (diem >= 5)
    cout << "Dat";
else
    cout << "Chua dat";
```

Nên viết:

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

Lý do:

> Dùng `{ }` giúp code rõ ràng hơn và tránh lỗi khi có nhiều lệnh.

---

## Lỗi 4: Đặt dấu `;` ngay sau `if`

Sai:

```cpp
if (diem >= 5);
{
    cout << "Dat";
}
else {
    cout << "Chua dat";
}
```

Đúng:

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

Giải thích:

> Không đặt dấu `;` ngay sau dòng `if (điều kiện)`.

---

## Lỗi 5: Sai điều kiện chẵn/lẻ

Sai:

```cpp
if (n % 2 = 0) {
    cout << "So chan";
} else {
    cout << "So le";
}
```

Đúng:

```cpp
if (n % 2 == 0) {
    cout << "So chan";
} else {
    cout << "So le";
}
```

Giải thích:

> Kiểm tra bằng nhau phải dùng `==`.

---

# 18. Hoạt động thực hành 1: Điểm đạt/chưa đạt

## Đề bài

Nhập điểm. Nếu điểm từ 5 trở lên thì in `Dat`, ngược lại in `Chua dat`.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 5) {
        cout << "Dat";
    } else {
        cout << "Chua dat";
    }

    return 0;
}
```

---

# 19. Hoạt động thực hành 2: Số chẵn/lẻ

## Đề bài

Nhập số nguyên `n`. Kiểm tra số đó là số chẵn hay số lẻ.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n % 2 == 0) {
        cout << "So chan";
    } else {
        cout << "So le";
    }

    return 0;
}
```

---

# 20. Hoạt động thực hành 3: Số lớn hơn trong hai số

## Đề bài

Nhập hai số nguyên `a`, `b`. In ra số lớn hơn.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    if (a > b) {
        cout << "So lon hon la: " << a;
    } else {
        cout << "So lon hon la: " << b;
    }

    return 0;
}
```

---

# 21. Hoạt động thực hành 4: Đủ tiền hay không đủ tiền

## Đề bài

Nhập giá món đồ và số tiền em có. Kiểm tra có đủ tiền mua hay không.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaTien, tienCo;

    cout << "Nhap gia tien mon do: ";
    cin >> giaTien;

    cout << "Nhap so tien em co: ";
    cin >> tienCo;

    if (tienCo >= giaTien) {
        cout << "Du tien mua";
    } else {
        cout << "Khong du tien";
    }

    return 0;
}
```

---

# 22. Hoạt động thực hành 5: Mật mã đúng/sai

## Đề bài

Nhập mật mã. Nếu mật mã bằng `2026` thì in `Mo khoa thanh cong`, ngược lại in `Sai mat ma`.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int matMa;

    cout << "Nhap mat ma: ";
    cin >> matMa;

    if (matMa == 2026) {
        cout << "Mo khoa thanh cong";
    } else {
        cout << "Sai mat ma";
    }

    return 0;
}
```

---

# 23. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

Câu lệnh `else` có nghĩa là gì?

A. Nếu
B. Ngược lại
C. Nhập dữ liệu
D. In dữ liệu

Đáp án: **B**

---

## Bài 2: Chọn đáp án đúng

Cấu trúc nào đúng?

A.

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

B.

```cpp
if diem >= 5 {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

C.

```cpp
if (diem >= 5) {
    cout << "Dat";
} else (diem < 5) {
    cout << "Chua dat";
}
```

Đáp án: **A**

---

## Bài 3: Điền từ còn thiếu

```text
Trong câu lệnh if else, nếu điều kiện đúng thì chạy phần ______, nếu sai thì chạy phần ______.
```

Đáp án:

```text
if, else
```

---

## Bài 4: Đoán kết quả

```cpp
int n = 8;

if (n % 2 == 0) {
    cout << "So chan";
} else {
    cout << "So le";
}
```

Đáp án:

```text
So chan
```

---

## Bài 5: Đoán kết quả

```cpp
int n = 9;

if (n % 2 == 0) {
    cout << "So chan";
} else {
    cout << "So le";
}
```

Đáp án:

```text
So le
```

---

## Bài 6: Đoán kết quả

```cpp
int a = 5;
int b = 10;

if (a > b) {
    cout << a;
} else {
    cout << b;
}
```

Đáp án:

```text
10
```

---

## Bài 7: Tìm lỗi sai

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n % 2 = 0) {
        cout << "So chan";
    } else {
        cout << "So le";
    }

    return 0;
}
```

Lỗi:

```text
Dùng = thay vì == trong điều kiện.
```

Sửa đúng:

```cpp
if (n % 2 == 0) {
    cout << "So chan";
} else {
    cout << "So le";
}
```

---

## Bài 8: Tìm lỗi sai

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 5) {
        cout << "Dat";
    } else (diem < 5) {
        cout << "Chua dat";
    }

    return 0;
}
```

Lỗi:

```text
Không viết điều kiện sau else.
```

Sửa đúng:

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

---

# 24. Bài tập thực hành

## Bài 1

Viết chương trình nhập điểm. Nếu điểm lớn hơn hoặc bằng `5` thì in:

```text
Dat
```

Ngược lại in:

```text
Chua dat
```

---

## Bài 2

Viết chương trình nhập một số nguyên `n`. Nếu `n` là số chẵn thì in:

```text
So chan
```

Ngược lại in:

```text
So le
```

---

## Bài 3

Viết chương trình nhập tuổi. Nếu tuổi lớn hơn hoặc bằng `11` thì in:

```text
Du tuoi hoc lop 6
```

Ngược lại in:

```text
Chua du tuoi hoc lop 6
```

---

## Bài 4

Viết chương trình nhập hai số nguyên `a`, `b`. In ra số lớn hơn.

Ví dụ:

```text
Nhap a: 8
Nhap b: 3
So lon hon la: 8
```

---

## Bài 5

Viết chương trình nhập giá món đồ và số tiền em có. Nếu đủ tiền thì in:

```text
Du tien mua
```

Ngược lại in:

```text
Khong du tien
```

---

## Bài 6

Viết chương trình nhập mật mã. Nếu mật mã bằng `2026` thì in:

```text
Mo khoa thanh cong
```

Ngược lại in:

```text
Sai mat ma
```

---

# 25. Bài tập nâng cao nhẹ

## Bài 1: Kiểm tra số chia hết cho 5

Đề bài:

```text
Nhập một số nguyên n.
Nếu n chia hết cho 5 thì in "Chia het cho 5".
Ngược lại in "Khong chia het cho 5".
```

Gợi ý:

```cpp
if (n % 5 == 0) {
    cout << "Chia het cho 5";
} else {
    cout << "Khong chia het cho 5";
}
```

Code đầy đủ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n % 5 == 0) {
        cout << "Chia het cho 5";
    } else {
        cout << "Khong chia het cho 5";
    }

    return 0;
}
```

---

## Bài 2: Kiểm tra số lớn hơn 100

Đề bài:

```text
Nhập một số nguyên n.
Nếu n lớn hơn 100 thì in "Lon hon 100".
Ngược lại in "Khong lon hon 100".
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n > 100) {
        cout << "Lon hon 100";
    } else {
        cout << "Khong lon hon 100";
    }

    return 0;
}
```

---

## Bài 3: Tìm số nhỏ hơn trong hai số

Đề bài:

```text
Nhập hai số nguyên a, b.
In ra số nhỏ hơn.
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    if (a < b) {
        cout << "So nho hon la: " << a;
    } else {
        cout << "So nho hon la: " << b;
    }

    return 0;
}
```

---

## Bài 4: Tính tiền thừa nếu đủ tiền

Đề bài:

```text
Nhập giá món đồ và số tiền em có.
Nếu đủ tiền thì in số tiền thừa.
Ngược lại in "Khong du tien".
```

Phân tích:

```text
Đầu vào:
- giaTien
- tienCo

Điều kiện:
- tienCo >= giaTien

Nếu đúng:
- tienThua = tienCo - giaTien
- in tienThua

Ngược lại:
- in "Khong du tien"
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaTien, tienCo;
    int tienThua;

    cout << "Nhap gia tien mon do: ";
    cin >> giaTien;

    cout << "Nhap so tien em co: ";
    cin >> tienCo;

    if (tienCo >= giaTien) {
        tienThua = tienCo - giaTien;
        cout << "Tien thua la: " << tienThua << " dong";
    } else {
        cout << "Khong du tien";
    }

    return 0;
}
```

---

# 26. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. `if else` dùng để làm gì?
2. Phần `if` chạy khi nào?
3. Phần `else` chạy khi nào?
4. Có viết điều kiện sau `else` không?
5. Muốn kiểm tra số chẵn, viết điều kiện gì?
6. Muốn kiểm tra hai số bằng nhau, dùng `=` hay `==`?
7. Trong `if else`, máy tính có chạy cả hai phần không?

Gợi ý trả lời:

```text
1. if else dùng để xử lý hai trường hợp đúng và sai.
2. Phần if chạy khi điều kiện đúng.
3. Phần else chạy khi điều kiện sai.
4. Không.
5. n % 2 == 0
6. Dùng ==
7. Không. Máy tính chỉ chạy một trong hai phần.
```

---

# 27. Bài tập về nhà

## Bài 1

Viết chương trình nhập một số nguyên. Nếu số đó là số chẵn thì in:

```text
So chan
```

Ngược lại in:

```text
So le
```

---

## Bài 2

Viết chương trình nhập điểm Tin học. Nếu điểm lớn hơn hoặc bằng `8` thì in:

```text
Hoc tot
```

Ngược lại in:

```text
Can co gang hon
```

---

## Bài 3

Viết chương trình nhập hai số nguyên `a`, `b`. In ra số lớn hơn.

---

## Bài 4

Viết chương trình nhập mật mã. Nếu mật mã bằng `12345` thì in:

```text
Dang nhap thanh cong
```

Ngược lại in:

```text
Sai mat ma
```

---

## Bài 5

Viết chương trình nhập số kẹo và số bạn.

Nếu số kẹo chia hết cho số bạn thì in:

```text
Chia deu
```

Ngược lại in:

```text
Khong chia deu
```

Gợi ý:

```cpp
if (keo % ban == 0) {
    cout << "Chia deu";
} else {
    cout << "Khong chia deu";
}
```

---

# 28. Tóm tắt bài học

Học sinh cần nhớ:

```text
if else dùng để xử lý hai trường hợp.

Cấu trúc:

if (dieu_kien) {
    // Chạy khi điều kiện đúng
} else {
    // Chạy khi điều kiện sai
}

else nghĩa là ngược lại.
Không viết điều kiện sau else.

Một số điều kiện thường gặp:

diem >= 5       kiểm tra điểm đạt
n % 2 == 0      kiểm tra số chẵn
a == b          kiểm tra hai số bằng nhau
a > b           kiểm tra a lớn hơn b
tienCo >= giaTien kiểm tra đủ tiền
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n % 2 == 0) {
        cout << "So chan";
    } else {
        cout << "So le";
    }

    return 0;
}
```

---

# 29. Gợi ý thời lượng dạy

| Phần                      | Thời lượng |
| ------------------------- | ---------: |
| Ôn bài cũ                 |     5 phút |
| Giới thiệu `if else`      |    10 phút |
| So sánh `if` và `if else` |    10 phút |
| Ví dụ điểm đạt/chưa đạt   |    10 phút |
| Ví dụ số chẵn/lẻ          |    15 phút |
| Ví dụ tìm số lớn hơn      |    10 phút |
| Thực hành và sửa lỗi      |    20 phút |
| Củng cố, giao bài tập     |     5 phút |

Tổng thời lượng: khoảng **85 phút**.
