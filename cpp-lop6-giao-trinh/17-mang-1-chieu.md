# Bài 17: Mảng một chiều trong C++

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu mảng là gì.
* Biết khi nào cần dùng mảng.
* Biết khai báo mảng một chiều.
* Biết truy cập phần tử trong mảng.
* Biết nhập và in các phần tử của mảng.
* Biết dùng vòng lặp để xử lý mảng.
* Viết được chương trình:

  * Nhập danh sách điểm.
  * Tính tổng các phần tử.
  * Tìm số lớn nhất.
  * Đếm số chẵn trong mảng.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. `string` dùng để lưu dữ liệu gì?
2. Muốn nhập họ tên có dấu cách dùng lệnh gì?
3. `.length()` dùng để làm gì?
4. Vòng lặp `for` dùng để làm gì?
5. Muốn kiểm tra số chẵn dùng điều kiện gì?

Gợi ý trả lời:

```text
1. string dùng để lưu chuỗi ký tự.
2. Dùng getline(cin, hoTen);
3. Dùng để lấy độ dài chuỗi.
4. Dùng để lặp lại công việc nhiều lần.
5. n % 2 == 0.
```

Dẫn vào bài mới:

> Nếu chỉ lưu một điểm số, ta có thể dùng một biến `diem`.
> Nhưng nếu cần lưu điểm của 30 học sinh thì sao?
> Ta không nên tạo 30 biến riêng lẻ.
> Lúc này ta dùng **mảng**.

---

# 3. Mảng là gì?

**Mảng** là một biến đặc biệt có thể lưu nhiều giá trị cùng kiểu dữ liệu.

Ví dụ:

```cpp
int diem[5];
```

Dòng trên tạo một mảng tên là `diem`, có thể lưu **5 số nguyên**.

Có thể hiểu mảng giống như một dãy chiếc hộp:

```text
diem[0]  diem[1]  diem[2]  diem[3]  diem[4]
```

Mỗi ô trong mảng lưu một giá trị.

---

# 4. Vì sao cần dùng mảng?

Nếu muốn lưu điểm của 5 học sinh, ta có thể viết:

```cpp
int diem1, diem2, diem3, diem4, diem5;
```

Nhưng cách này rất bất tiện.

Nếu có 30 học sinh thì phải tạo 30 biến.

Thay vào đó, ta dùng mảng:

```cpp
int diem[30];
```

Ưu điểm:

```text
- Code gọn hơn.
- Dễ nhập nhiều dữ liệu.
- Dễ dùng vòng lặp để xử lý.
- Dễ tính tổng, tìm lớn nhất, nhỏ nhất.
```

---

# 5. Khai báo mảng

Cấu trúc:

```cpp
kieu_du_lieu ten_mang[so_luong];
```

Ví dụ:

```cpp
int a[5];
float diem[10];
string ten[30];
```

Ý nghĩa:

| Câu lệnh          | Ý nghĩa                         |
| ----------------- | ------------------------------- |
| `int a[5];`       | Mảng `a` lưu 5 số nguyên        |
| `float diem[10];` | Mảng `diem` lưu 10 số thập phân |
| `string ten[30];` | Mảng `ten` lưu 30 chuỗi         |

---

# 6. Chỉ số của mảng

Trong C++, phần tử đầu tiên của mảng có chỉ số là `0`, không phải `1`.

Ví dụ:

```cpp
int a[5];
```

Mảng `a` có 5 phần tử:

```text
a[0]  a[1]  a[2]  a[3]  a[4]
```

Lưu ý:

```text
Mảng có 5 phần tử thì chỉ số chạy từ 0 đến 4.
Không có a[5].
```

Đây là điểm học sinh rất dễ nhầm.

---

# 7. Gán giá trị cho phần tử mảng

Ví dụ:

```cpp
int a[5];

a[0] = 10;
a[1] = 20;
a[2] = 30;
a[3] = 40;
a[4] = 50;
```

Sau đó:

```cpp
cout << a[0];
```

Kết quả:

```text
10
```

Chương trình đầy đủ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a[5];

    a[0] = 10;
    a[1] = 20;
    a[2] = 30;
    a[3] = 40;
    a[4] = 50;

    cout << a[0];

    return 0;
}
```

---

# 8. Khai báo mảng có giá trị ban đầu

Ta có thể khai báo và gán giá trị ngay:

```cpp
int a[5] = {10, 20, 30, 40, 50};
```

Khi đó:

```text
a[0] = 10
a[1] = 20
a[2] = 30
a[3] = 40
a[4] = 50
```

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a[5] = {10, 20, 30, 40, 50};

    cout << a[0] << endl;
    cout << a[1] << endl;
    cout << a[2];

    return 0;
}
```

Kết quả:

```text
10
20
30
```

---

# 9. In các phần tử của mảng bằng vòng lặp

Nếu muốn in 5 phần tử, không nên viết:

```cpp
cout << a[0];
cout << a[1];
cout << a[2];
cout << a[3];
cout << a[4];
```

Ta dùng vòng lặp:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a[5] = {10, 20, 30, 40, 50};

    for (int i = 0; i < 5; i++) {
        cout << a[i] << " ";
    }

    return 0;
}
```

Kết quả:

```text
10 20 30 40 50
```

Giải thích:

```text
i chạy từ 0 đến 4.
Mỗi lần lặp, chương trình in a[i].
```

---

# 10. Nhập mảng từ bàn phím

## Đề bài

Nhập 5 số nguyên vào mảng, sau đó in các số đó ra màn hình.

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int a[5];

    for (int i = 0; i < 5; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    cout << "Cac so vua nhap la: ";

    for (int i = 0; i < 5; i++) {
        cout << a[i] << " ";
    }

    return 0;
}
```

Ví dụ chạy:

```text
Nhap a[0]: 4
Nhap a[1]: 7
Nhap a[2]: 2
Nhap a[3]: 9
Nhap a[4]: 5
Cac so vua nhap la: 4 7 2 9 5
```

---

# 11. Nhập n phần tử của mảng

Thường ta cho người dùng nhập số lượng phần tử `n`.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int a[100];

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    cout << "Mang vua nhap la: ";

    for (int i = 0; i < n; i++) {
        cout << a[i] << " ";
    }

    return 0;
}
```

Lưu ý:

```text
int a[100];
```

nghĩa là ta tạo mảng tối đa 100 phần tử.

Khi nhập `n`, nên nhập `n <= 100`.

---

# 12. Tính tổng các phần tử trong mảng

## Đề bài

Nhập `n` số nguyên vào mảng. Tính tổng các phần tử.

## Phân tích

```text
Đầu vào:
- n
- mảng a gồm n số nguyên

Xử lý:
- tong = 0
- Duyệt từng phần tử a[i]
- Cộng a[i] vào tong

Đầu ra:
- tong
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int a[100];
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    for (int i = 0; i < n; i++) {
        tong = tong + a[i];
    }

    cout << "Tong la: " << tong;

    return 0;
}
```

Ví dụ:

```text
Nhap n: 4
Nhap a[0]: 3
Nhap a[1]: 5
Nhap a[2]: 2
Nhap a[3]: 10
Tong la: 20
```

---

# 13. Tìm số lớn nhất trong mảng

## Đề bài

Nhập `n` số nguyên vào mảng. Tìm số lớn nhất.

## Cách làm

* Giả sử phần tử đầu tiên là lớn nhất.
* Duyệt các phần tử còn lại.
* Nếu gặp phần tử lớn hơn `max`, cập nhật `max`.

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int a[100];

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    int max = a[0];

    for (int i = 1; i < n; i++) {
        if (a[i] > max) {
            max = a[i];
        }
    }

    cout << "So lon nhat la: " << max;

    return 0;
}
```

Ví dụ:

```text
Nhap n: 5
Nhap a[0]: 3
Nhap a[1]: 8
Nhap a[2]: 2
Nhap a[3]: 10
Nhap a[4]: 6
So lon nhat la: 10
```

---

# 14. Tìm số nhỏ nhất trong mảng

Tương tự tìm số lớn nhất.

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int a[100];

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    int min = a[0];

    for (int i = 1; i < n; i++) {
        if (a[i] < min) {
            min = a[i];
        }
    }

    cout << "So nho nhat la: " << min;

    return 0;
}
```

---

# 15. Đếm số chẵn trong mảng

## Đề bài

Nhập `n` số nguyên vào mảng. Đếm có bao nhiêu số chẵn.

## Phân tích

```text
Đầu vào:
- n
- mảng a

Xử lý:
- dem = 0
- Nếu a[i] % 2 == 0 thì tăng dem

Đầu ra:
- dem
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int a[100];
    int dem = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    for (int i = 0; i < n; i++) {
        if (a[i] % 2 == 0) {
            dem = dem + 1;
        }
    }

    cout << "Co " << dem << " so chan";

    return 0;
}
```

---

# 16. Tính tổng các số chẵn trong mảng

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int a[100];
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    for (int i = 0; i < n; i++) {
        if (a[i] % 2 == 0) {
            tong = tong + a[i];
        }
    }

    cout << "Tong cac so chan la: " << tong;

    return 0;
}
```

---

# 17. Ví dụ thực tế: Nhập điểm học sinh

## Đề bài

Nhập điểm của `n` học sinh. Tính điểm trung bình của cả lớp.

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    float diem[100];
    float tong = 0;
    float trungBinh;

    cout << "Nhap so hoc sinh: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap diem hoc sinh thu " << i + 1 << ": ";
        cin >> diem[i];
    }

    for (int i = 0; i < n; i++) {
        tong = tong + diem[i];
    }

    trungBinh = tong / n;

    cout << "Diem trung binh cua lop la: " << trungBinh;

    return 0;
}
```

Ví dụ:

```text
Nhap so hoc sinh: 3
Nhap diem hoc sinh thu 1: 8
Nhap diem hoc sinh thu 2: 7.5
Nhap diem hoc sinh thu 3: 9
Diem trung binh cua lop la: 8.16667
```

---

# 18. Lỗi thường gặp khi học mảng

## Lỗi 1: Nhầm chỉ số bắt đầu từ 1

Sai:

```cpp
for (int i = 1; i <= n; i++) {
    cin >> a[i];
}
```

Nếu dùng mảng kiểu C++, nên nhập từ `0` đến `n - 1`.

Đúng:

```cpp
for (int i = 0; i < n; i++) {
    cin >> a[i];
}
```

---

## Lỗi 2: Truy cập quá số phần tử

Sai:

```cpp
int a[5];
cout << a[5];
```

Mảng `a[5]` có các phần tử:

```text
a[0], a[1], a[2], a[3], a[4]
```

Không có `a[5]`.

---

## Lỗi 3: Quên khởi tạo biến tổng, biến đếm

Sai:

```cpp
int tong;
int dem;
```

Đúng:

```cpp
int tong = 0;
int dem = 0;
```

---

## Lỗi 4: Tìm max nhưng gán `max = 0`

Sai:

```cpp
int max = 0;
```

Nếu mảng toàn số âm, kết quả sẽ sai.

Đúng:

```cpp
int max = a[0];
```

---

## Lỗi 5: Nhập `n` lớn hơn kích thước mảng

Nếu khai báo:

```cpp
int a[100];
```

thì không nên nhập `n > 100`.

Có thể nhắc học sinh:

```text
Trong bài học này, chỉ nhập n từ 1 đến 100.
```

---

# 19. Hoạt động trên lớp

## Hoạt động 1: Nhập và in mảng

Yêu cầu:

```text
Nhập n số nguyên.
In lại các số vừa nhập.
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int a[100];

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    cout << "Mang vua nhap: ";

    for (int i = 0; i < n; i++) {
        cout << a[i] << " ";
    }

    return 0;
}
```

---

## Hoạt động 2: Tính tổng mảng

Yêu cầu:

```text
Nhập n số nguyên.
Tính tổng các số trong mảng.
```

Gợi ý:

```cpp
int tong = 0;

for (int i = 0; i < n; i++) {
    tong = tong + a[i];
}
```

---

## Hoạt động 3: Đếm số chẵn

Yêu cầu:

```text
Nhập n số nguyên.
Đếm có bao nhiêu số chẵn.
```

Gợi ý:

```cpp
int dem = 0;

for (int i = 0; i < n; i++) {
    if (a[i] % 2 == 0) {
        dem = dem + 1;
    }
}
```

---

# 20. Bài tập trên lớp

## Bài 1

Khai báo mảng `a` gồm 10 số nguyên.

Đáp án:

```cpp
int a[10];
```

---

## Bài 2

Mảng sau có bao nhiêu phần tử?

```cpp
int diem[30];
```

Đáp án:

```text
30 phần tử.
```

---

## Bài 3

Mảng `a[5]` có các chỉ số nào?

Đáp án:

```text
a[0], a[1], a[2], a[3], a[4]
```

---

## Bài 4

Đoạn code sau in ra gì?

```cpp
int a[3] = {5, 8, 2};

cout << a[1];
```

Đáp án:

```text
8
```

---

## Bài 5

Tìm lỗi sai:

```cpp
int a[5];

for (int i = 1; i <= 5; i++) {
    cin >> a[i];
}
```

Lỗi:

```text
Sai chỉ số mảng. Mảng 5 phần tử có chỉ số từ 0 đến 4.
```

Sửa đúng:

```cpp
for (int i = 0; i < 5; i++) {
    cin >> a[i];
}
```

---

# 21. Bài tập thực hành

## Bài 1

Nhập `n` số nguyên vào mảng. In lại mảng vừa nhập.

---

## Bài 2

Nhập `n` số nguyên vào mảng. Tính tổng các phần tử.

---

## Bài 3

Nhập `n` số nguyên vào mảng. Đếm số chẵn.

---

## Bài 4

Nhập `n` số nguyên vào mảng. Đếm số lẻ.

Gợi ý:

```cpp
if (a[i] % 2 != 0) {
    dem = dem + 1;
}
```

---

## Bài 5

Nhập `n` số nguyên vào mảng. Tìm số lớn nhất.

---

## Bài 6

Nhập `n` số nguyên vào mảng. Tìm số nhỏ nhất.

---

## Bài 7

Nhập điểm của `n` học sinh. Tính điểm trung bình.

---

# 22. Bài tập nâng cao nhẹ

## Bài 1: Tính tổng số dương trong mảng

Nhập `n` số nguyên. Tính tổng các số dương.

Gợi ý:

```cpp
if (a[i] > 0) {
    tong = tong + a[i];
}
```

---

## Bài 2: Đếm số âm trong mảng

Nhập `n` số nguyên. Đếm có bao nhiêu số âm.

Gợi ý:

```cpp
if (a[i] < 0) {
    dem = dem + 1;
}
```

---

## Bài 3: Đếm số chia hết cho 5

Nhập `n` số nguyên. Đếm có bao nhiêu số chia hết cho 5.

Gợi ý:

```cpp
if (a[i] % 5 == 0) {
    dem = dem + 1;
}
```

---

# 23. Câu hỏi củng cố

Giáo viên hỏi học sinh:

1. Mảng dùng để làm gì?
2. Mảng một chiều là gì?
3. Khai báo `int a[10];` nghĩa là gì?
4. Chỉ số đầu tiên của mảng trong C++ là mấy?
5. Mảng `a[5]` có phần tử `a[5]` không?
6. Muốn duyệt mảng `n` phần tử, vòng lặp thường viết thế nào?
7. Khi tính tổng mảng, biến `tong` ban đầu bằng bao nhiêu?
8. Khi tìm số lớn nhất, nên gán `max` ban đầu bằng gì?

Gợi ý trả lời:

```text
1. Mảng dùng để lưu nhiều giá trị cùng kiểu dữ liệu.
2. Là mảng gồm các phần tử xếp thành một dãy.
3. Tạo mảng a gồm 10 số nguyên.
4. Chỉ số đầu tiên là 0.
5. Không. Mảng a[5] có chỉ số từ 0 đến 4.
6. for (int i = 0; i < n; i++)
7. tong = 0.
8. max = a[0].
```

---

# 24. Bài tập về nhà

## Bài 1

Viết chương trình nhập `n` số nguyên vào mảng và in lại mảng.

## Bài 2

Viết chương trình nhập `n` số nguyên vào mảng và tính tổng các phần tử.

## Bài 3

Viết chương trình nhập `n` số nguyên vào mảng và đếm số chẵn.

## Bài 4

Viết chương trình nhập `n` số nguyên vào mảng và tìm số lớn nhất.

## Bài 5

Viết chương trình nhập điểm của `n` học sinh và tính điểm trung bình.

---

# 25. Tóm tắt bài học

Học sinh cần nhớ:

```text
Mảng dùng để lưu nhiều giá trị cùng kiểu dữ liệu.

Khai báo:
int a[100];

Phần tử đầu tiên:
a[0]

Mảng n phần tử có chỉ số:
0 đến n - 1

Duyệt mảng:
for (int i = 0; i < n; i++) {
    // xử lý a[i]
}

Tính tổng:
tong = tong + a[i];

Đếm số chẵn:
if (a[i] % 2 == 0) {
    dem = dem + 1;
}

Tìm lớn nhất:
max = a[0];
if (a[i] > max) {
    max = a[i];
}
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int a[100];
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap a[" << i << "]: ";
        cin >> a[i];
    }

    for (int i = 0; i < n; i++) {
        tong = tong + a[i];
    }

    cout << "Tong la: " << tong;

    return 0;
}
```

---

# 26. Gợi ý thời lượng dạy 60 phút

| Phần                   | Thời lượng |
| ---------------------- | ---------: |
| Ôn bài cũ              |     5 phút |
| Giới thiệu mảng        |     8 phút |
| Khai báo, chỉ số mảng  |    10 phút |
| Nhập và in mảng        |    10 phút |
| Tính tổng, đếm số chẵn |    12 phút |
| Tìm lớn nhất, nhỏ nhất |    10 phút |
| Củng cố, giao bài tập  |     5 phút |

Tổng: **60 phút**.
