# Bài 13: Thuật toán là gì?

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu thuật toán là gì.
* Biết thuật toán là các bước giải quyết một vấn đề.
* Biết viết thuật toán bằng lời trước khi viết code.
* Biết phân tích bài toán theo các bước rõ ràng.
* Biết chuyển thuật toán đơn giản thành chương trình C++.
* Áp dụng được thuật toán cho các bài: tính tổng, kiểm tra chẵn lẻ, tìm số lớn nhất.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Vòng lặp dùng để làm gì?
2. `for` thường dùng khi nào?
3. `while` thường dùng khi nào?
4. Muốn kiểm tra số chẵn, ta viết điều kiện gì?
5. Muốn tính tổng nhiều số, biến `tong` ban đầu bằng bao nhiêu?

Gợi ý trả lời:

```text
1. Vòng lặp dùng để lặp lại một công việc nhiều lần.
2. for thường dùng khi biết trước số lần lặp.
3. while thường dùng khi chưa biết trước số lần lặp.
4. n % 2 == 0.
5. tong = 0.
```

Dẫn vào bài mới:

> Trước khi viết code, lập trình viên thường phải nghĩ xem bài toán cần giải như thế nào.
> Các bước giải bài toán đó gọi là **thuật toán**.

---

# 3. Thuật toán là gì?

**Thuật toán** là một dãy các bước rõ ràng để giải quyết một vấn đề.

Ví dụ trong đời sống:

## Thuật toán đánh răng

```text
1. Lấy bàn chải.
2. Lấy kem đánh răng.
3. Làm ướt bàn chải.
4. Chải răng.
5. Súc miệng.
6. Rửa bàn chải.
```

## Thuật toán nấu mì

```text
1. Đun nước.
2. Cho mì vào tô.
3. Cho gia vị vào.
4. Đổ nước sôi vào tô.
5. Chờ 3 phút.
6. Ăn mì.
```

Giáo viên kết luận:

> Thuật toán không chỉ có trong lập trình.
> Trong đời sống hằng ngày, khi ta làm việc theo từng bước, đó cũng là một dạng thuật toán.

---

# 4. Thuật toán trong lập trình

Trong lập trình, thuật toán là các bước để máy tính giải một bài toán.

Ví dụ bài toán:

```text
Nhập hai số a và b. Tính tổng hai số.
```

Thuật toán:

```text
1. Nhập a.
2. Nhập b.
3. Tính tong = a + b.
4. In tong.
```

Chuyển thành code C++:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;
    int tong;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    tong = a + b;

    cout << "Tong la: " << tong;

    return 0;
}
```

---

# 5. Vì sao cần học thuật toán?

Học thuật toán giúp học sinh:

```text
1. Biết suy nghĩ trước khi code.
2. Biết chia bài toán lớn thành nhiều bước nhỏ.
3. Code ít sai hơn.
4. Dễ tìm lỗi hơn.
5. Giải được nhiều bài toán khó hơn sau này.
```

Giáo viên nhấn mạnh:

> Viết code không phải là gõ lệnh ngay.
> Trước tiên phải hiểu cách giải bài toán.

---

# 6. Mẫu viết thuật toán đơn giản

Khi gặp bài toán lập trình, học sinh nên làm theo mẫu:

```text
Bài toán: ...

Đầu vào:
- ...

Xử lý:
- Bước 1: ...
- Bước 2: ...
- Bước 3: ...

Đầu ra:
- ...
```

Ví dụ:

```text
Bài toán: Nhập một số n, kiểm tra n là số chẵn hay số lẻ.

Đầu vào:
- n

Xử lý:
- Nếu n chia 2 dư 0 thì n là số chẵn.
- Ngược lại n là số lẻ.

Đầu ra:
- So chan hoặc So le.
```

---

# 7. Ví dụ 1: Thuật toán tính tổng hai số

## Đề bài

Nhập hai số nguyên `a`, `b`. Tính tổng hai số.

## Thuật toán

```text
1. Nhập a.
2. Nhập b.
3. Tính tong = a + b.
4. In tong.
```

## Code C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, tong;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    tong = a + b;

    cout << "Tong la: " << tong;

    return 0;
}
```

---

# 8. Ví dụ 2: Thuật toán kiểm tra số chẵn lẻ

## Đề bài

Nhập một số nguyên `n`. Kiểm tra số đó là số chẵn hay số lẻ.

## Thuật toán

```text
1. Nhập n.
2. Nếu n chia 2 dư 0 thì in "So chan".
3. Ngược lại in "So le".
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

---

# 9. Ví dụ 3: Thuật toán tính tổng từ 1 đến n

## Đề bài

Nhập số nguyên `n`. Tính tổng:

```text
1 + 2 + 3 + ... + n
```

## Thuật toán

```text
1. Nhập n.
2. Cho tong = 0.
3. Cho i chạy từ 1 đến n.
4. Mỗi lần lặp, cộng i vào tong.
5. In tong.
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

---

# 10. Ví dụ 4: Thuật toán tìm số lớn hơn trong 2 số

## Đề bài

Nhập hai số nguyên `a`, `b`. In ra số lớn hơn.

## Thuật toán

```text
1. Nhập a.
2. Nhập b.
3. Nếu a > b thì in a.
4. Ngược lại in b.
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

> Nếu `a` và `b` bằng nhau, chương trình vẫn in ra `b`.
> Bài nâng cao có thể xử lý riêng trường hợp bằng nhau.

---

# 11. Ví dụ 5: Thuật toán tìm số lớn nhất trong 3 số

## Đề bài

Nhập ba số nguyên `a`, `b`, `c`. Tìm số lớn nhất.

## Thuật toán

```text
1. Nhập a, b, c.
2. Gán max = a.
3. Nếu b > max thì max = b.
4. Nếu c > max thì max = c.
5. In max.
```

## Code C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b, c;
    int max;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Nhap c: ";
    cin >> c;

    max = a;

    if (b > max) {
        max = b;
    }

    if (c > max) {
        max = c;
    }

    cout << "So lon nhat la: " << max;

    return 0;
}
```

Giải thích:

```text
Ban đầu xem a là số lớn nhất.
Nếu b lớn hơn max thì cập nhật max.
Nếu c lớn hơn max thì cập nhật max.
Cuối cùng max là số lớn nhất.
```

---

# 12. Ví dụ 6: Thuật toán nhập n số và tính tổng

## Đề bài

Nhập `n`. Sau đó nhập `n` số nguyên. Tính tổng các số đó.

## Thuật toán

```text
1. Nhập n.
2. Cho tong = 0.
3. Lặp từ i = 1 đến n:
   - Nhập x.
   - Cộng x vào tong.
4. In tong.
```

## Code C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int n, x;
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        cout << "Nhap so thu " << i << ": ";
        cin >> x;

        tong = tong + x;
    }

    cout << "Tong la: " << tong;

    return 0;
}
```

---

# 13. Hoạt động trên lớp

## Hoạt động 1: Sắp xếp thuật toán

Giáo viên đưa các bước bị xáo trộn:

```text
A. In kết quả.
B. Nhập a.
C. Tính tong = a + b.
D. Nhập b.
```

Yêu cầu học sinh sắp xếp đúng để tính tổng hai số.

Đáp án:

```text
B → D → C → A
```

---

## Hoạt động 2: Viết thuật toán bằng lời

Đề bài:

```text
Nhập điểm. Nếu điểm >= 5 thì in "Dat", ngược lại in "Chua dat".
```

Học sinh viết thuật toán:

```text
1. Nhập điểm.
2. Nếu điểm >= 5 thì in "Dat".
3. Ngược lại in "Chua dat".
```

---

## Hoạt động 3: Chuyển thuật toán thành code

Từ thuật toán trên, học sinh viết code:

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

# 14. Lỗi thường gặp khi viết thuật toán

## Lỗi 1: Bỏ sót bước nhập dữ liệu

Sai:

```text
1. Tính tong = a + b.
2. In tong.
```

Thiếu bước nhập `a`, `b`.

Đúng:

```text
1. Nhập a.
2. Nhập b.
3. Tính tong = a + b.
4. In tong.
```

---

## Lỗi 2: Sai thứ tự bước

Sai:

```text
1. In tổng.
2. Nhập a.
3. Nhập b.
4. Tính tổng.
```

Đúng:

```text
1. Nhập a.
2. Nhập b.
3. Tính tổng.
4. In tổng.
```

---

## Lỗi 3: Thuật toán chưa rõ ràng

Chưa rõ:

```text
Tính toán rồi in ra.
```

Rõ ràng hơn:

```text
1. Nhập a.
2. Nhập b.
3. Tính tong = a + b.
4. In tong.
```

---

# 15. Bài tập trên lớp

## Bài 1

Viết thuật toán nhập hai số `a`, `b` và tính hiệu `a - b`.

Gợi ý:

```text
1. Nhập a.
2. Nhập b.
3. Tính hieu = a - b.
4. In hieu.
```

---

## Bài 2

Viết thuật toán nhập chiều dài, chiều rộng hình chữ nhật và tính diện tích.

Gợi ý:

```text
1. Nhập chiều dài.
2. Nhập chiều rộng.
3. Tính diện tích = chiều dài * chiều rộng.
4. In diện tích.
```

---

## Bài 3

Viết thuật toán kiểm tra một số có chia hết cho 5 hay không.

Gợi ý:

```text
1. Nhập n.
2. Nếu n % 5 == 0 thì in "Chia het cho 5".
3. Ngược lại in "Khong chia het cho 5".
```

---

## Bài 4

Viết thuật toán tính tổng từ `1` đến `n`.

Gợi ý:

```text
1. Nhập n.
2. Cho tong = 0.
3. Lặp i từ 1 đến n:
   - tong = tong + i.
4. In tong.
```

---

# 16. Bài tập thực hành

## Bài 1

Viết thuật toán và code cho bài:

```text
Nhập hai số a, b. Tính tích a * b.
```

## Bài 2

Viết thuật toán và code cho bài:

```text
Nhập một số n. Kiểm tra n là số chẵn hay số lẻ.
```

## Bài 3

Viết thuật toán và code cho bài:

```text
Nhập n. Tính tổng các số chẵn từ 1 đến n.
```

## Bài 4

Viết thuật toán và code cho bài:

```text
Nhập ba số a, b, c. Tìm số lớn nhất.
```

---

# 17. Câu hỏi củng cố

Giáo viên hỏi học sinh:

1. Thuật toán là gì?
2. Vì sao cần viết thuật toán trước khi code?
3. Một thuật toán tốt cần như thế nào?
4. Khi tính tổng từ 1 đến n, vì sao cần biến `tong`?
5. Khi tìm số lớn nhất trong 3 số, vì sao có thể gán `max = a` ban đầu?

Gợi ý trả lời:

```text
1. Thuật toán là các bước rõ ràng để giải quyết một vấn đề.
2. Để hiểu cách giải trước khi viết code, giúp code ít sai hơn.
3. Cần rõ ràng, đúng thứ tự, không thiếu bước.
4. Để lưu kết quả cộng dồn.
5. Vì ta tạm xem a là số lớn nhất, rồi so sánh với b và c.
```

---

# 18. Bài tập về nhà

## Bài 1

Viết thuật toán cho bài:

```text
Nhập tuổi. Nếu tuổi >= 11 thì in "Du tuoi hoc lop 6", ngược lại in "Chua du tuoi".
```

## Bài 2

Viết thuật toán cho bài:

```text
Nhập n. In các số từ 1 đến n.
```

## Bài 3

Viết thuật toán và code cho bài:

```text
Nhập n. Tính tổng từ 1 đến n.
```

## Bài 4

Viết thuật toán và code cho bài:

```text
Nhập n số nguyên. Đếm có bao nhiêu số chẵn.
```

---

# 19. Tóm tắt bài học

Học sinh cần nhớ:

```text
Thuật toán là các bước rõ ràng để giải quyết một vấn đề.

Khi làm bài lập trình:
1. Đọc đề.
2. Xác định đầu vào.
3. Viết các bước xử lý.
4. Xác định đầu ra.
5. Chuyển thuật toán thành code.

Một thuật toán tốt cần:
- Rõ ràng
- Đúng thứ tự
- Không thiếu bước
- Có thể thực hiện được
```

Mẫu cần nhớ:

```text
Bài toán: ...

Đầu vào:
- ...

Xử lý:
1. ...
2. ...
3. ...

Đầu ra:
- ...
```

---

# 20. Gợi ý thời lượng dạy 45 phút

| Phần                          | Thời lượng |
| ----------------------------- | ---------: |
| Ôn bài cũ                     |     5 phút |
| Giới thiệu thuật toán         |     7 phút |
| Ví dụ đời sống và lập trình   |     8 phút |
| Mẫu phân tích thuật toán      |     5 phút |
| Ví dụ tính tổng, chẵn lẻ, max |    12 phút |
| Bài tập trên lớp              |     5 phút |
| Củng cố, giao bài tập         |     3 phút |

Tổng: **45 phút**.
