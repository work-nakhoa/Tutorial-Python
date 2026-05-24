# Bài 10: Nhiều điều kiện với `if else if`

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu khi nào cần dùng `if else if`.
* Biết xử lý bài toán có nhiều trường hợp.
* Biết phân biệt `if`, `if else`, `if else if`.
* Biết dùng toán tử logic:

  * `&&`: và
  * `||`: hoặc
* Viết được chương trình:

  * Xếp loại điểm.
  * Kiểm tra số âm, dương, bằng 0.
  * Tìm số lớn nhất trong 3 số ở mức cơ bản.
  * Kiểm tra tháng thuộc mùa nào.
* Biết tránh lỗi sai thứ tự điều kiện.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. `if else` dùng để làm gì?
2. Phần `if` chạy khi nào?
3. Phần `else` chạy khi nào?
4. Có viết điều kiện sau `else` không?
5. Điều kiện kiểm tra số chẵn viết thế nào?
6. Muốn kiểm tra hai số bằng nhau dùng `=` hay `==`?

Gợi ý trả lời:

```text
1. if else dùng để xử lý hai trường hợp.
2. Phần if chạy khi điều kiện đúng.
3. Phần else chạy khi điều kiện sai.
4. Không viết điều kiện sau else.
5. n % 2 == 0
6. Dùng == để so sánh bằng nhau.
```

Giáo viên dẫn vào bài mới:

> Ở bài trước, chúng ta học `if else` để xử lý 2 trường hợp.
> Nhưng trong thực tế, có nhiều bài toán có hơn 2 trường hợp.
> Ví dụ điểm có thể là Giỏi, Khá, Trung bình hoặc Chưa đạt.
> Khi đó ta dùng `if else if`.

---

# 3. Vì sao cần `if else if`?

Ví dụ bài toán:

```text
Nhập điểm và xếp loại:

Từ 8 trở lên: Giỏi
Từ 6.5 trở lên: Khá
Từ 5 trở lên: Trung bình
Dưới 5: Chưa đạt
```

Bài này có 4 trường hợp.

Nếu chỉ dùng `if else`, ta chỉ xử lý được 2 trường hợp đơn giản:

```text
Đạt
Chưa đạt
```

Muốn xử lý nhiều trường hợp hơn, ta dùng:

```cpp
if
else if
else if
else
```

---

# 4. Cấu trúc `if else if`

Cấu trúc:

```cpp
if (dieu_kien_1) {
    // Chạy nếu điều kiện 1 đúng
} else if (dieu_kien_2) {
    // Chạy nếu điều kiện 1 sai và điều kiện 2 đúng
} else if (dieu_kien_3) {
    // Chạy nếu các điều kiện trên sai và điều kiện 3 đúng
} else {
    // Chạy nếu tất cả điều kiện trên đều sai
}
```

Giải thích đơn giản:

```text
Máy tính kiểm tra từ trên xuống dưới.

Nếu điều kiện 1 đúng → chạy phần 1 rồi bỏ qua các phần còn lại.
Nếu điều kiện 1 sai → kiểm tra điều kiện 2.
Nếu điều kiện 2 đúng → chạy phần 2 rồi bỏ qua các phần còn lại.
Nếu tất cả điều kiện đều sai → chạy phần else.
```

---

# 5. So sánh `if`, `if else`, `if else if`

| Câu lệnh     | Dùng khi nào?                | Ví dụ                           |
| ------------ | ---------------------------- | ------------------------------- |
| `if`         | Chỉ cần kiểm tra 1 điều kiện | Nếu điểm >= 5 thì in Đạt        |
| `if else`    | Có 2 trường hợp              | Chẵn hoặc lẻ                    |
| `if else if` | Có nhiều hơn 2 trường hợp    | Giỏi, Khá, Trung bình, Chưa đạt |

Ví dụ:

## Dùng `if`

```cpp
if (diem >= 5) {
    cout << "Dat";
}
```

## Dùng `if else`

```cpp
if (diem >= 5) {
    cout << "Dat";
} else {
    cout << "Chua dat";
}
```

## Dùng `if else if`

```cpp
if (diem >= 8) {
    cout << "Gioi";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 5) {
    cout << "Trung binh";
} else {
    cout << "Chua dat";
}
```

---

# 6. Ví dụ 1: Xếp loại điểm

## Đề bài

Nhập điểm. Xếp loại theo quy tắc:

```text
Điểm >= 8       → Giỏi
Điểm >= 6.5     → Khá
Điểm >= 5       → Trung bình
Điểm < 5        → Chưa đạt
```

## Phân tích

```text
Đầu vào:
- diem

Điều kiện:
- diem >= 8
- diem >= 6.5
- diem >= 5
- còn lại là dưới 5

Đầu ra:
- xếp loại học sinh
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 8) {
        cout << "Gioi";
    } else if (diem >= 6.5) {
        cout << "Kha";
    } else if (diem >= 5) {
        cout << "Trung binh";
    } else {
        cout << "Chua dat";
    }

    return 0;
}
```

## Ví dụ chạy chương trình

```text
Nhap diem: 9
Gioi
```

```text
Nhap diem: 7
Kha
```

```text
Nhap diem: 5.5
Trung binh
```

```text
Nhap diem: 4
Chua dat
```

---

# 7. Vì sao thứ tự điều kiện quan trọng?

Trong bài xếp loại điểm, ta viết:

```cpp
if (diem >= 8) {
    cout << "Gioi";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 5) {
    cout << "Trung binh";
} else {
    cout << "Chua dat";
}
```

Thứ tự này đúng vì kiểm tra từ điểm cao xuống điểm thấp.

Nếu viết sai thứ tự:

```cpp
if (diem >= 5) {
    cout << "Trung binh";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 8) {
    cout << "Gioi";
} else {
    cout << "Chua dat";
}
```

Nếu nhập điểm `9`, chương trình sẽ in:

```text
Trung binh
```

Vì `9 >= 5` đúng, máy tính chạy ngay phần đầu tiên và bỏ qua các phần sau.

Kết luận:

```text
Khi nhiều điều kiện có liên quan đến nhau, cần sắp xếp điều kiện đúng thứ tự.
```

---

# 8. Ví dụ 2: Kiểm tra số âm, dương, bằng 0

## Đề bài

Nhập một số nguyên `n`. Kiểm tra số đó là:

```text
Số dương
Số âm
Số bằng 0
```

## Phân tích

```text
Đầu vào:
- n

Điều kiện:
- n > 0     → số dương
- n < 0     → số âm
- còn lại   → bằng 0
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
    } else if (n < 0) {
        cout << "So am";
    } else {
        cout << "So bang 0";
    }

    return 0;
}
```

## Ví dụ

```text
Nhap n: 5
So duong
```

```text
Nhap n: -3
So am
```

```text
Nhap n: 0
So bang 0
```

---

# 9. Ví dụ 3: So sánh hai số

## Đề bài

Nhập hai số nguyên `a`, `b`. Kiểm tra:

```text
a lớn hơn b
a nhỏ hơn b
a bằng b
```

## Phân tích

```text
Đầu vào:
- a
- b

Điều kiện:
- a > b    → a lớn hơn b
- a < b    → a nhỏ hơn b
- còn lại  → a bằng b
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
        cout << "a lon hon b";
    } else if (a < b) {
        cout << "a nho hon b";
    } else {
        cout << "a bang b";
    }

    return 0;
}
```

## Ví dụ

```text
Nhap a: 8
Nhap b: 3
a lon hon b
```

```text
Nhap a: 2
Nhap b: 9
a nho hon b
```

```text
Nhap a: 5
Nhap b: 5
a bang b
```

---

# 10. Toán tử logic là gì?

Đôi khi một điều kiện cần kiểm tra nhiều ý cùng lúc.

Ví dụ:

```text
Điểm phải lớn hơn hoặc bằng 0 và nhỏ hơn hoặc bằng 10.
```

Điều kiện này có 2 phần:

```text
diem >= 0
diem <= 10
```

Ta cần cả hai điều kiện đều đúng.

Trong C++ dùng toán tử logic.

| Toán tử | Tên gọi | Ý nghĩa                   |      |                                      |
| ------- | ------- | ------------------------- | ---- | ------------------------------------ |
| `&&`    | Và      | Cả hai điều kiện đều đúng |      |                                      |
| `       |         | `                         | Hoặc | Chỉ cần một trong hai điều kiện đúng |

---

# 11. Toán tử `&&` — và

`&&` nghĩa là **và**.

Điều kiện dùng `&&` chỉ đúng khi **cả hai vế đều đúng**.

Ví dụ:

```cpp
if (diem >= 0 && diem <= 10) {
    cout << "Diem hop le";
}
```

Nghĩa là:

```text
Nếu điểm >= 0 và điểm <= 10 thì điểm hợp lệ.
```

Ví dụ:

| `diem` | `diem >= 0` | `diem <= 10` | Kết quả |
| -----: | ----------- | ------------ | ------- |
|      8 | Đúng        | Đúng         | Đúng    |
|     -1 | Sai         | Đúng         | Sai     |
|     12 | Đúng        | Sai          | Sai     |

Chương trình mẫu:

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 0 && diem <= 10) {
        cout << "Diem hop le";
    } else {
        cout << "Diem khong hop le";
    }

    return 0;
}
```

---

# 12. Toán tử `||` — hoặc

`||` nghĩa là **hoặc**.

Điều kiện dùng `||` đúng khi **ít nhất một điều kiện đúng**.

Ví dụ:

```cpp
if (ngay == 7 || ngay == 8) {
    cout << "Cuoi tuan";
}
```

Nghĩa là:

```text
Nếu ngày là 7 hoặc ngày là 8 thì là cuối tuần.
```

Ví dụ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int ngay;

    cout << "Nhap so ngay trong tuan: ";
    cin >> ngay;

    if (ngay == 7 || ngay == 8) {
        cout << "Cuoi tuan";
    } else {
        cout << "Ngay thuong";
    }

    return 0;
}
```

Lưu ý:

Ở ví dụ này giả sử:

```text
Thứ Bảy = 7
Chủ Nhật = 8
```

---

# 13. Ví dụ 4: Kiểm tra điểm hợp lệ rồi xếp loại

## Đề bài

Nhập điểm.

Nếu điểm nhỏ hơn 0 hoặc lớn hơn 10 thì in:

```text
Diem khong hop le
```

Ngược lại, xếp loại:

```text
>= 8      Giỏi
>= 6.5    Khá
>= 5      Trung bình
< 5       Chưa đạt
```

## Phân tích

```text
Đầu vào:
- diem

Điều kiện:
- diem < 0 hoặc diem > 10 → không hợp lệ
- diem >= 8              → Giỏi
- diem >= 6.5            → Khá
- diem >= 5              → Trung bình
- còn lại                → Chưa đạt
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem < 0 || diem > 10) {
        cout << "Diem khong hop le";
    } else if (diem >= 8) {
        cout << "Gioi";
    } else if (diem >= 6.5) {
        cout << "Kha";
    } else if (diem >= 5) {
        cout << "Trung binh";
    } else {
        cout << "Chua dat";
    }

    return 0;
}
```

## Ví dụ

```text
Nhap diem: 11
Diem khong hop le
```

```text
Nhap diem: 9
Gioi
```

```text
Nhap diem: 4
Chua dat
```

---

# 14. Ví dụ 5: Kiểm tra tháng thuộc mùa nào

Để đơn giản cho học sinh lớp 6, có thể quy ước:

```text
Mùa xuân: tháng 1, 2, 3
Mùa hè: tháng 4, 5, 6
Mùa thu: tháng 7, 8, 9
Mùa đông: tháng 10, 11, 12
```

## Đề bài

Nhập tháng. In ra mùa tương ứng.

## Phân tích

```text
Đầu vào:
- thang

Điều kiện:
- 1, 2, 3       → Mua xuan
- 4, 5, 6       → Mua he
- 7, 8, 9       → Mua thu
- 10, 11, 12    → Mua dong
- còn lại       → Thang khong hop le
```

## Cách 1: Dùng `&&`

```cpp
#include <iostream>
using namespace std;

int main() {
    int thang;

    cout << "Nhap thang: ";
    cin >> thang;

    if (thang >= 1 && thang <= 3) {
        cout << "Mua xuan";
    } else if (thang >= 4 && thang <= 6) {
        cout << "Mua he";
    } else if (thang >= 7 && thang <= 9) {
        cout << "Mua thu";
    } else if (thang >= 10 && thang <= 12) {
        cout << "Mua dong";
    } else {
        cout << "Thang khong hop le";
    }

    return 0;
}
```

## Ví dụ

```text
Nhap thang: 5
Mua he
```

```text
Nhap thang: 13
Thang khong hop le
```

---

# 15. Ví dụ 6: Tìm số lớn nhất trong 3 số

## Đề bài

Nhập ba số nguyên `a`, `b`, `c`. In ra số lớn nhất.

## Cách làm đơn giản cho lớp 6

Ta kiểm tra:

```text
Nếu a lớn hơn hoặc bằng b và a lớn hơn hoặc bằng c → a lớn nhất
Ngược lại nếu b lớn hơn hoặc bằng a và b lớn hơn hoặc bằng c → b lớn nhất
Ngược lại → c lớn nhất
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, c;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Nhap c: ";
    cin >> c;

    if (a >= b && a >= c) {
        cout << "So lon nhat la: " << a;
    } else if (b >= a && b >= c) {
        cout << "So lon nhat la: " << b;
    } else {
        cout << "So lon nhat la: " << c;
    }

    return 0;
}
```

## Ví dụ

```text
Nhap a: 5
Nhap b: 9
Nhap c: 3
So lon nhat la: 9
```

```text
Nhap a: 7
Nhap b: 7
Nhap c: 2
So lon nhat la: 7
```

---

# 16. Cách máy tính chạy `if else if`

Với đoạn code:

```cpp
if (diem >= 8) {
    cout << "Gioi";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 5) {
    cout << "Trung binh";
} else {
    cout << "Chua dat";
}
```

Nếu nhập `diem = 7`, máy tính làm như sau:

```text
Bước 1: Kiểm tra diem >= 8
7 >= 8 là sai

Bước 2: Kiểm tra diem >= 6.5
7 >= 6.5 là đúng

Bước 3: In "Kha"

Bước 4: Bỏ qua các phần còn lại
```

Kết luận:

```text
Trong chuỗi if else if, máy tính chỉ chạy một nhánh đầu tiên có điều kiện đúng.
```

---

# 17. Quy trình làm bài có nhiều điều kiện

Khi gặp bài toán có nhiều điều kiện, học sinh làm theo các bước:

```text
Bước 1: Đọc đề.
Bước 2: Liệt kê tất cả các trường hợp.
Bước 3: Viết điều kiện cho từng trường hợp.
Bước 4: Sắp xếp điều kiện theo thứ tự hợp lý.
Bước 5: Viết code bằng if else if.
Bước 6: Chạy thử mỗi trường hợp ít nhất một lần.
```

Ví dụ bài xếp loại điểm:

```text
Các trường hợp:
1. Điểm không hợp lệ
2. Giỏi
3. Khá
4. Trung bình
5. Chưa đạt

Điều kiện:
1. diem < 0 || diem > 10
2. diem >= 8
3. diem >= 6.5
4. diem >= 5
5. else
```

---

# 18. Lỗi thường gặp khi dùng `if else if`

## Lỗi 1: Sai thứ tự điều kiện

Sai:

```cpp
if (diem >= 5) {
    cout << "Trung binh";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 8) {
    cout << "Gioi";
}
```

Nếu nhập `9`, chương trình in `Trung binh`.

Đúng:

```cpp
if (diem >= 8) {
    cout << "Gioi";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 5) {
    cout << "Trung binh";
} else {
    cout << "Chua dat";
}
```

---

## Lỗi 2: Viết nhiều `if` riêng khi nên dùng `else if`

Ví dụ:

```cpp
if (diem >= 8) {
    cout << "Gioi";
}

if (diem >= 6.5) {
    cout << "Kha";
}

if (diem >= 5) {
    cout << "Trung binh";
}
```

Nếu nhập `9`, chương trình có thể in:

```text
GioiKhaTrung binh
```

Vì cả ba điều kiện đều đúng.

Nên dùng:

```cpp
if (diem >= 8) {
    cout << "Gioi";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 5) {
    cout << "Trung binh";
} else {
    cout << "Chua dat";
}
```

---

## Lỗi 3: Dùng sai toán tử logic

Sai:

```cpp
if (diem >= 0 || diem <= 10) {
    cout << "Diem hop le";
}
```

Điều kiện này gần như luôn đúng với nhiều số.

Đúng:

```cpp
if (diem >= 0 && diem <= 10) {
    cout << "Diem hop le";
}
```

Giải thích:

```text
Điểm hợp lệ khi vừa >= 0, vừa <= 10.
Vậy phải dùng &&.
```

---

## Lỗi 4: Quên điều kiện không hợp lệ

Ví dụ nhập tháng:

```cpp
if (thang >= 1 && thang <= 3) {
    cout << "Mua xuan";
} else if (thang >= 4 && thang <= 6) {
    cout << "Mua he";
} else if (thang >= 7 && thang <= 9) {
    cout << "Mua thu";
} else {
    cout << "Mua dong";
}
```

Nếu nhập `20`, chương trình vẫn in `Mua dong`, không hợp lý.

Đúng hơn:

```cpp
if (thang >= 1 && thang <= 3) {
    cout << "Mua xuan";
} else if (thang >= 4 && thang <= 6) {
    cout << "Mua he";
} else if (thang >= 7 && thang <= 9) {
    cout << "Mua thu";
} else if (thang >= 10 && thang <= 12) {
    cout << "Mua dong";
} else {
    cout << "Thang khong hop le";
}
```

---

## Lỗi 5: Dùng `=` thay vì `==`

Sai:

```cpp
if (thang = 1) {
    cout << "Thang 1";
}
```

Đúng:

```cpp
if (thang == 1) {
    cout << "Thang 1";
}
```

Nhắc lại:

```text
=  dùng để gán
== dùng để so sánh bằng nhau
```

---

# 19. Hoạt động thực hành 1: Xếp loại điểm

## Đề bài

Nhập điểm và xếp loại:

```text
>= 8      Gioi
>= 6.5    Kha
>= 5      Trung binh
< 5       Chua dat
```

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 8) {
        cout << "Gioi";
    } else if (diem >= 6.5) {
        cout << "Kha";
    } else if (diem >= 5) {
        cout << "Trung binh";
    } else {
        cout << "Chua dat";
    }

    return 0;
}
```

---

# 20. Hoạt động thực hành 2: Số âm, dương, bằng 0

## Đề bài

Nhập một số nguyên `n`. Kiểm tra:

```text
n > 0   → So duong
n < 0   → So am
n == 0  → So bang 0
```

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n > 0) {
        cout << "So duong";
    } else if (n < 0) {
        cout << "So am";
    } else {
        cout << "So bang 0";
    }

    return 0;
}
```

---

# 21. Hoạt động thực hành 3: So sánh hai số

## Đề bài

Nhập hai số `a`, `b`. In ra:

```text
a lon hon b
a nho hon b
a bang b
```

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
        cout << "a lon hon b";
    } else if (a < b) {
        cout << "a nho hon b";
    } else {
        cout << "a bang b";
    }

    return 0;
}
```

---

# 22. Hoạt động thực hành 4: Kiểm tra điểm hợp lệ

## Đề bài

Nhập điểm. Nếu điểm nằm trong khoảng từ `0` đến `10` thì in:

```text
Diem hop le
```

Ngược lại in:

```text
Diem khong hop le
```

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 0 && diem <= 10) {
        cout << "Diem hop le";
    } else {
        cout << "Diem khong hop le";
    }

    return 0;
}
```

---

# 23. Hoạt động thực hành 5: Kiểm tra tháng

## Đề bài

Nhập tháng. Nếu tháng từ 1 đến 12 thì in:

```text
Thang hop le
```

Ngược lại in:

```text
Thang khong hop le
```

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int thang;

    cout << "Nhap thang: ";
    cin >> thang;

    if (thang >= 1 && thang <= 12) {
        cout << "Thang hop le";
    } else {
        cout << "Thang khong hop le";
    }

    return 0;
}
```

---

# 24. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

`if else if` dùng khi nào?

A. Khi chỉ có một trường hợp
B. Khi có đúng hai trường hợp
C. Khi có nhiều trường hợp
D. Khi không cần điều kiện

Đáp án: **C**

---

## Bài 2: Chọn đáp án đúng

Toán tử `&&` có nghĩa là gì?

A. Hoặc
B. Và
C. Bằng nhau
D. Khác nhau

Đáp án: **B**

---

## Bài 3: Chọn đáp án đúng

Toán tử `||` có nghĩa là gì?

A. Hoặc
B. Và
C. Lớn hơn
D. Nhỏ hơn

Đáp án: **A**

---

## Bài 4: Đoán kết quả

```cpp
int n = -5;

if (n > 0) {
    cout << "So duong";
} else if (n < 0) {
    cout << "So am";
} else {
    cout << "So bang 0";
}
```

Đáp án:

```text
So am
```

---

## Bài 5: Đoán kết quả

```cpp
float diem = 7;

if (diem >= 8) {
    cout << "Gioi";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 5) {
    cout << "Trung binh";
} else {
    cout << "Chua dat";
}
```

Đáp án:

```text
Kha
```

---

## Bài 6: Đoán kết quả

```cpp
int thang = 13;

if (thang >= 1 && thang <= 12) {
    cout << "Hop le";
} else {
    cout << "Khong hop le";
}
```

Đáp án:

```text
Khong hop le
```

---

## Bài 7: Tìm lỗi sai

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem >= 5) {
        cout << "Trung binh";
    } else if (diem >= 6.5) {
        cout << "Kha";
    } else if (diem >= 8) {
        cout << "Gioi";
    } else {
        cout << "Chua dat";
    }

    return 0;
}
```

Lỗi:

```text
Thứ tự điều kiện sai. Phải kiểm tra điểm cao trước.
```

Sửa đúng:

```cpp
if (diem >= 8) {
    cout << "Gioi";
} else if (diem >= 6.5) {
    cout << "Kha";
} else if (diem >= 5) {
    cout << "Trung binh";
} else {
    cout << "Chua dat";
}
```

---

## Bài 8: Tìm lỗi sai

```cpp
if (diem >= 0 || diem <= 10) {
    cout << "Diem hop le";
}
```

Lỗi:

```text
Điểm hợp lệ cần đồng thời >= 0 và <= 10, nên phải dùng &&.
```

Sửa đúng:

```cpp
if (diem >= 0 && diem <= 10) {
    cout << "Diem hop le";
}
```

---

# 25. Bài tập thực hành

## Bài 1

Viết chương trình nhập điểm và xếp loại:

```text
>= 8      Gioi
>= 6.5    Kha
>= 5      Trung binh
< 5       Chua dat
```

---

## Bài 2

Viết chương trình nhập một số nguyên `n`. Kiểm tra:

```text
n > 0   So duong
n < 0   So am
n == 0  So bang 0
```

---

## Bài 3

Viết chương trình nhập hai số nguyên `a`, `b`. In ra:

```text
a lon hon b
a nho hon b
a bang b
```

---

## Bài 4

Viết chương trình nhập điểm. Nếu điểm nhỏ hơn 0 hoặc lớn hơn 10 thì in:

```text
Diem khong hop le
```

Ngược lại xếp loại:

```text
>= 8      Gioi
>= 6.5    Kha
>= 5      Trung binh
< 5       Chua dat
```

---

## Bài 5

Viết chương trình nhập tháng. Nếu tháng từ 1 đến 12 thì in:

```text
Thang hop le
```

Ngược lại in:

```text
Thang khong hop le
```

---

# 26. Bài tập nâng cao nhẹ

## Bài 1: Xếp loại học lực chi tiết

Nhập điểm trung bình và xếp loại:

```text
>= 9       Xuat sac
>= 8       Gioi
>= 6.5     Kha
>= 5       Trung binh
< 5        Yeu
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem trung binh: ";
    cin >> diem;

    if (diem >= 9) {
        cout << "Xuat sac";
    } else if (diem >= 8) {
        cout << "Gioi";
    } else if (diem >= 6.5) {
        cout << "Kha";
    } else if (diem >= 5) {
        cout << "Trung binh";
    } else {
        cout << "Yeu";
    }

    return 0;
}
```

---

## Bài 2: Tìm số lớn nhất trong 3 số

Nhập ba số nguyên `a`, `b`, `c`. In ra số lớn nhất.

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, c;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Nhap c: ";
    cin >> c;

    if (a >= b && a >= c) {
        cout << "So lon nhat la: " << a;
    } else if (b >= a && b >= c) {
        cout << "So lon nhat la: " << b;
    } else {
        cout << "So lon nhat la: " << c;
    }

    return 0;
}
```

---

## Bài 3: Kiểm tra mùa trong năm

Nhập tháng và in ra mùa theo quy ước:

```text
1, 2, 3       Mua xuan
4, 5, 6       Mua he
7, 8, 9       Mua thu
10, 11, 12    Mua dong
Khác          Thang khong hop le
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int thang;

    cout << "Nhap thang: ";
    cin >> thang;

    if (thang >= 1 && thang <= 3) {
        cout << "Mua xuan";
    } else if (thang >= 4 && thang <= 6) {
        cout << "Mua he";
    } else if (thang >= 7 && thang <= 9) {
        cout << "Mua thu";
    } else if (thang >= 10 && thang <= 12) {
        cout << "Mua dong";
    } else {
        cout << "Thang khong hop le";
    }

    return 0;
}
```

---

# 27. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. `if else if` dùng khi nào?
2. Máy tính kiểm tra các điều kiện trong `if else if` theo thứ tự nào?
3. Trong chuỗi `if else if`, máy tính có chạy nhiều nhánh cùng lúc không?
4. Toán tử `&&` có nghĩa là gì?
5. Toán tử `||` có nghĩa là gì?
6. Muốn kiểm tra điểm hợp lệ từ 0 đến 10, viết điều kiện thế nào?
7. Muốn kiểm tra điểm không hợp lệ, viết điều kiện thế nào?
8. Vì sao khi xếp loại điểm phải kiểm tra điểm cao trước?

Gợi ý trả lời:

```text
1. Dùng khi có nhiều trường hợp.
2. Từ trên xuống dưới.
3. Không. Chỉ chạy nhánh đúng đầu tiên.
4. && nghĩa là và.
5. || nghĩa là hoặc.
6. diem >= 0 && diem <= 10
7. diem < 0 || diem > 10
8. Vì nếu kiểm tra điểm thấp trước, điểm cao cũng thỏa điều kiện thấp và bị xếp sai.
```

---

# 28. Bài tập về nhà

## Bài 1

Viết chương trình nhập điểm Tin học và xếp loại:

```text
>= 8      Hoc tot
>= 6.5    Kha
>= 5      Dat
< 5       Can co gang
```

---

## Bài 2

Viết chương trình nhập một số nguyên `n`. Kiểm tra:

```text
n > 0   So duong
n < 0   So am
n == 0  So bang 0
```

---

## Bài 3

Viết chương trình nhập tháng. Nếu tháng không nằm trong khoảng 1 đến 12 thì in:

```text
Thang khong hop le
```

Nếu hợp lệ thì in mùa tương ứng:

```text
1, 2, 3       Mua xuan
4, 5, 6       Mua he
7, 8, 9       Mua thu
10, 11, 12    Mua dong
```

---

## Bài 4

Viết chương trình nhập ba số nguyên `a`, `b`, `c`. In ra số lớn nhất.

---

## Bài 5

Viết chương trình nhập điểm. Nếu điểm không hợp lệ thì in:

```text
Diem khong hop le
```

Nếu hợp lệ thì xếp loại:

```text
>= 9       Xuat sac
>= 8       Gioi
>= 6.5     Kha
>= 5       Trung binh
< 5        Yeu
```

---

# 29. Tóm tắt bài học

Học sinh cần nhớ:

```text
if else if dùng để xử lý nhiều trường hợp.

Cấu trúc:

if (dieu_kien_1) {
    // chạy nếu điều kiện 1 đúng
} else if (dieu_kien_2) {
    // chạy nếu điều kiện 2 đúng
} else if (dieu_kien_3) {
    // chạy nếu điều kiện 3 đúng
} else {
    // chạy nếu tất cả điều kiện trên đều sai
}

Máy tính kiểm tra từ trên xuống dưới.
Chỉ chạy nhánh đúng đầu tiên.

&& nghĩa là và.
|| nghĩa là hoặc.
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem < 0 || diem > 10) {
        cout << "Diem khong hop le";
    } else if (diem >= 8) {
        cout << "Gioi";
    } else if (diem >= 6.5) {
        cout << "Kha";
    } else if (diem >= 5) {
        cout << "Trung binh";
    } else {
        cout << "Chua dat";
    }

    return 0;
}
```

---

# 30. Gợi ý thời lượng dạy

| Phần                                   | Thời lượng |   |         |
| -------------------------------------- | ---------: | - | ------- |
| Ôn bài cũ                              |     5 phút |   |         |
| Giới thiệu `if else if`                |    10 phút |   |         |
| Ví dụ xếp loại điểm                    |    15 phút |   |         |
| Thứ tự điều kiện                       |    10 phút |   |         |
| Toán tử `&&`, `                        |            | ` | 15 phút |
| Ví dụ số âm, dương, bằng 0             |    10 phút |   |         |
| Thực hành xếp loại, tháng, số lớn nhất |    25 phút |   |         |
| Củng cố và giao bài tập                |     5 phút |   |         |

Tổng thời lượng: khoảng **95 phút**.
