# Bài 14: Phân tích bài toán lập trình

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Biết cách đọc và hiểu đề bài lập trình.
* Biết xác định **đầu vào**, **xử lý**, **đầu ra**.
* Biết viết phân tích trước khi code.
* Biết chuyển phân tích thành chương trình C++.
* Làm được các bài toán cơ bản như:

  * Tính diện tích hình chữ nhật.
  * Kiểm tra số chẵn/lẻ.
  * Tìm số lớn hơn trong 2 số.
  * Tính tổng từ 1 đến `n`.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Thuật toán là gì?
2. Vì sao cần viết thuật toán trước khi code?
3. Khi tính tổng từ `1` đến `n`, biến `tong` ban đầu bằng bao nhiêu?
4. Muốn kiểm tra số chẵn, ta dùng điều kiện gì?

Gợi ý trả lời:

```text
1. Thuật toán là các bước rõ ràng để giải quyết một vấn đề.
2. Để hiểu cách giải trước khi viết code.
3. tong = 0.
4. n % 2 == 0.
```

Dẫn vào bài mới:

> Ở bài trước, chúng ta đã học thuật toán là các bước giải quyết vấn đề.
> Hôm nay, chúng ta học cách **phân tích một bài toán lập trình** trước khi viết code.

---

# 3. Phân tích bài toán là gì?

**Phân tích bài toán** là việc đọc đề bài và trả lời 3 câu hỏi:

```text
1. Đầu vào là gì?
2. Cần xử lý như thế nào?
3. Đầu ra là gì?
```

Nói đơn giản:

| Thành phần | Ý nghĩa                  |
| ---------- | ------------------------ |
| Đầu vào    | Dữ liệu cần nhập         |
| Xử lý      | Công thức hoặc cách giải |
| Đầu ra     | Kết quả cần in ra        |

Ví dụ:

```text
Bài toán: Nhập hai số a, b. Tính tổng hai số.
```

Phân tích:

```text
Đầu vào:
- a
- b

Xử lý:
- tong = a + b

Đầu ra:
- tong
```

---

# 4. Vì sao cần phân tích trước khi code?

Nếu không phân tích, học sinh dễ bị:

```text
- Không biết cần tạo biến gì.
- Không biết cần nhập dữ liệu nào.
- Viết sai công thức.
- In thiếu kết quả.
- Code dài nhưng không đúng yêu cầu.
```

Giáo viên nhấn mạnh:

> Trước khi viết code, hãy hiểu bài toán trước.
> Code chỉ là bước cuối cùng sau khi đã biết cách giải.

---

# 5. Mẫu phân tích bài toán

Học sinh nên ghi nhớ mẫu sau:

```text
Bài toán: ...

Đầu vào:
- ...

Xử lý:
- ...

Đầu ra:
- ...
```

Ví dụ:

```text
Bài toán: Nhập chiều dài và chiều rộng hình chữ nhật. Tính diện tích.

Đầu vào:
- chieuDai
- chieuRong

Xử lý:
- dienTich = chieuDai * chieuRong

Đầu ra:
- dienTich
```

---

# 6. Ví dụ 1: Tính diện tích hình chữ nhật

## Đề bài

Nhập chiều dài và chiều rộng hình chữ nhật. Tính diện tích.

## Phân tích

```text
Đầu vào:
- dai
- rong

Xử lý:
- dienTich = dai * rong

Đầu ra:
- dienTich
```

## Code C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int dai, rong;
    int dienTich;

    cout << "Nhap chieu dai: ";
    cin >> dai;

    cout << "Nhap chieu rong: ";
    cin >> rong;

    dienTich = dai * rong;

    cout << "Dien tich la: " << dienTich;

    return 0;
}
```

Ví dụ chạy:

```text
Nhap chieu dai: 5
Nhap chieu rong: 3
Dien tich la: 15
```

---

# 7. Ví dụ 2: Tính chu vi hình chữ nhật

## Đề bài

Nhập chiều dài và chiều rộng hình chữ nhật. Tính chu vi.

## Phân tích

```text
Đầu vào:
- dai
- rong

Xử lý:
- chuVi = (dai + rong) * 2

Đầu ra:
- chuVi
```

## Code C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int dai, rong;
    int chuVi;

    cout << "Nhap chieu dai: ";
    cin >> dai;

    cout << "Nhap chieu rong: ";
    cin >> rong;

    chuVi = (dai + rong) * 2;

    cout << "Chu vi la: " << chuVi;

    return 0;
}
```

Lưu ý:

```cpp
chuVi = (dai + rong) * 2;
```

Phải có dấu ngoặc để cộng `dai + rong` trước, rồi mới nhân `2`.

---

# 8. Ví dụ 3: Kiểm tra số chẵn/lẻ

## Đề bài

Nhập một số nguyên `n`. Kiểm tra số đó là số chẵn hay số lẻ.

## Phân tích

```text
Đầu vào:
- n

Xử lý:
- Nếu n % 2 == 0 thì n là số chẵn
- Ngược lại n là số lẻ

Đầu ra:
- So chan hoặc So le
```

## Code C++

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

Ví dụ:

```text
Nhap n: 8
So chan
```

```text
Nhap n: 7
So le
```

---

# 9. Ví dụ 4: Tìm số lớn hơn trong 2 số

## Đề bài

Nhập hai số nguyên `a`, `b`. In ra số lớn hơn.

## Phân tích

```text
Đầu vào:
- a
- b

Xử lý:
- Nếu a > b thì số lớn hơn là a
- Ngược lại số lớn hơn là b

Đầu ra:
- Số lớn hơn
```

## Code C++

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

Lưu ý:

> Bài này chưa xử lý riêng trường hợp `a == b`.
> Nếu muốn đầy đủ hơn, có thể dùng `if else if`.

---

# 10. Ví dụ 5: So sánh hai số đầy đủ

## Đề bài

Nhập hai số nguyên `a`, `b`. Cho biết `a` lớn hơn, nhỏ hơn hay bằng `b`.

## Phân tích

```text
Đầu vào:
- a
- b

Xử lý:
- Nếu a > b thì in "a lon hon b"
- Nếu a < b thì in "a nho hon b"
- Ngược lại in "a bang b"

Đầu ra:
- Kết quả so sánh
```

## Code C++

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

# 11. Ví dụ 6: Tính tổng từ 1 đến n

## Đề bài

Nhập số nguyên `n`. Tính tổng:

```text
1 + 2 + 3 + ... + n
```

## Phân tích

```text
Đầu vào:
- n

Xử lý:
- Tạo tong = 0
- Cho i chạy từ 1 đến n
- Mỗi lần lặp: tong = tong + i

Đầu ra:
- tong
```

## Code C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        tong = tong + i;
    }

    cout << "Tong la: " << tong;

    return 0;
}
```

Ví dụ:

```text
Nhap n: 5
Tong la: 15
```

---

# 12. Ví dụ 7: Đếm số chẵn từ 1 đến n

## Đề bài

Nhập số nguyên `n`. Đếm xem từ `1` đến `n` có bao nhiêu số chẵn.

## Phân tích

```text
Đầu vào:
- n

Xử lý:
- Tạo dem = 0
- Cho i chạy từ 1 đến n
- Nếu i % 2 == 0 thì tăng dem lên 1

Đầu ra:
- dem
```

## Code C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int dem = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        if (i % 2 == 0) {
            dem = dem + 1;
        }
    }

    cout << "Co " << dem << " so chan";

    return 0;
}
```

Ví dụ:

```text
Nhap n: 10
Co 5 so chan
```

---

# 13. Các bước chuyển từ đề bài sang code

Khi gặp một đề bài, học sinh làm theo 5 bước:

```text
Bước 1: Đọc kỹ đề bài.
Bước 2: Xác định đầu vào.
Bước 3: Xác định cách xử lý.
Bước 4: Xác định đầu ra.
Bước 5: Viết code C++.
```

Ví dụ:

```text
Đề bài: Nhập tuổi. Nếu tuổi >= 11 thì in "Du tuoi", ngược lại in "Chua du tuoi".
```

Phân tích:

```text
Đầu vào:
- tuoi

Xử lý:
- Nếu tuoi >= 11 thì in "Du tuoi"
- Ngược lại in "Chua du tuoi"

Đầu ra:
- Thông báo kết quả
```

Code:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    if (tuoi >= 11) {
        cout << "Du tuoi";
    } else {
        cout << "Chua du tuoi";
    }

    return 0;
}
```

---

# 14. Lỗi thường gặp khi phân tích bài toán

## Lỗi 1: Nhầm đầu vào và đầu ra

Ví dụ đề bài:

```text
Nhập chiều dài, chiều rộng. Tính diện tích.
```

Sai:

```text
Đầu vào:
- dienTich
```

Đúng:

```text
Đầu vào:
- dai
- rong

Đầu ra:
- dienTich
```

---

## Lỗi 2: Thiếu bước xử lý

Sai:

```text
Đầu vào:
- dai
- rong

Đầu ra:
- dienTich
```

Thiếu phần xử lý.

Đúng:

```text
Xử lý:
- dienTich = dai * rong
```

---

## Lỗi 3: Viết công thức sai

Sai:

```cpp
chuVi = dai + rong * 2;
```

Đúng:

```cpp
chuVi = (dai + rong) * 2;
```

---

## Lỗi 4: Quên khởi tạo biến tổng hoặc biến đếm

Sai:

```cpp
int tong;
```

Đúng:

```cpp
int tong = 0;
```

Sai:

```cpp
int dem;
```

Đúng:

```cpp
int dem = 0;
```

---

# 15. Hoạt động trên lớp

## Hoạt động 1: Điền đầu vào, xử lý, đầu ra

Đề bài:

```text
Nhập cạnh hình vuông. Tính chu vi và diện tích.
```

Học sinh điền:

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
- canh

Xử lý:
- chuVi = canh * 4
- dienTich = canh * canh

Đầu ra:
- chuVi
- dienTich
```

---

## Hoạt động 2: Từ phân tích viết code

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int canh;
    int chuVi, dienTich;

    cout << "Nhap canh: ";
    cin >> canh;

    chuVi = canh * 4;
    dienTich = canh * canh;

    cout << "Chu vi la: " << chuVi << endl;
    cout << "Dien tich la: " << dienTich;

    return 0;
}
```

---

# 16. Bài tập trên lớp

## Bài 1

Phân tích bài toán sau:

```text
Nhập hai số a, b. Tính tích a * b.
```

Gợi ý:

```text
Đầu vào:
- a
- b

Xử lý:
- tich = a * b

Đầu ra:
- tich
```

---

## Bài 2

Phân tích bài toán sau:

```text
Nhập một số n. Kiểm tra n có chia hết cho 5 hay không.
```

Gợi ý:

```text
Đầu vào:
- n

Xử lý:
- Nếu n % 5 == 0 thì chia hết cho 5
- Ngược lại không chia hết cho 5

Đầu ra:
- Thông báo kết quả
```

---

## Bài 3

Phân tích và viết code:

```text
Nhập n. Tính tổng các số lẻ từ 1 đến n.
```

Gợi ý xử lý:

```cpp
if (i % 2 != 0) {
    tong = tong + i;
}
```

---

# 17. Bài tập thực hành

## Bài 1

Phân tích và viết code cho bài:

```text
Nhập số phút. Đổi sang số giây.
```

Gợi ý:

```text
giay = phut * 60
```

---

## Bài 2

Phân tích và viết code cho bài:

```text
Nhập giá một cây bút và số lượng bút. Tính tổng tiền.
```

Gợi ý:

```text
tongTien = giaBut * soLuong
```

---

## Bài 3

Phân tích và viết code cho bài:

```text
Nhập một số n. Nếu n > 0 thì in "So duong", nếu n < 0 thì in "So am", ngược lại in "So bang 0".
```

---

## Bài 4

Phân tích và viết code cho bài:

```text
Nhập n. Đếm xem từ 1 đến n có bao nhiêu số chia hết cho 3.
```

Gợi ý:

```cpp
if (i % 3 == 0) {
    dem = dem + 1;
}
```

---

# 18. Câu hỏi củng cố

Giáo viên hỏi học sinh:

1. Phân tích bài toán gồm mấy phần?
2. Đầu vào là gì?
3. Xử lý là gì?
4. Đầu ra là gì?
5. Vì sao cần phân tích trước khi code?
6. Khi tính tổng, biến `tong` ban đầu nên bằng bao nhiêu?
7. Khi đếm số lượng, biến `dem` ban đầu nên bằng bao nhiêu?

Gợi ý trả lời:

```text
1. Gồm 3 phần: đầu vào, xử lý, đầu ra.
2. Là dữ liệu cần nhập.
3. Là công thức hoặc cách giải.
4. Là kết quả cần in ra.
5. Để hiểu bài, tránh viết sai code.
6. tong = 0.
7. dem = 0.
```

---

# 19. Bài tập về nhà

## Bài 1

Phân tích bài toán:

```text
Nhập chiều dài và chiều rộng hình chữ nhật. Tính chu vi và diện tích.
```

## Bài 2

Phân tích và viết code:

```text
Nhập hai số a, b. In ra số lớn hơn.
```

## Bài 3

Phân tích và viết code:

```text
Nhập n. Tính tổng từ 1 đến n.
```

## Bài 4

Phân tích và viết code:

```text
Nhập n số nguyên. Đếm có bao nhiêu số chẵn.
```

---

# 20. Tóm tắt bài học

Học sinh cần nhớ:

```text
Phân tích bài toán gồm:

1. Đầu vào:
   Cần nhập dữ liệu gì?

2. Xử lý:
   Cần tính toán hoặc kiểm tra gì?

3. Đầu ra:
   Cần in kết quả gì?

Trước khi code, nên viết phân tích.
Phân tích tốt giúp code dễ hơn và ít sai hơn.
```

Mẫu cần nhớ:

```text
Bài toán: ...

Đầu vào:
- ...

Xử lý:
- ...

Đầu ra:
- ...
```

---

# 21. Gợi ý thời lượng dạy 45 phút

| Phần                           | Thời lượng |
| ------------------------------ | ---------: |
| Ôn bài cũ                      |     5 phút |
| Giới thiệu phân tích bài toán  |     7 phút |
| Mẫu đầu vào, xử lý, đầu ra     |     5 phút |
| Ví dụ diện tích, chẵn lẻ, tổng |    15 phút |
| Bài tập trên lớp               |    10 phút |
| Củng cố, giao bài tập          |     3 phút |

Tổng: **45 phút**.
