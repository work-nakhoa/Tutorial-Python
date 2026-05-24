# Bài 15: Hàm cơ bản trong C++

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu hàm là gì.
* Biết vì sao cần dùng hàm.
* Biết tạo hàm đơn giản trong C++.
* Biết gọi hàm trong chương trình.
* Biết hàm không trả về giá trị với `void`.
* Biết hàm có tham số.
* Biết hàm có trả về giá trị với `int`.
* Viết được chương trình dùng hàm để tính tổng, in lời chào, kiểm tra số chẵn lẻ.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Phân tích bài toán gồm mấy phần?
2. Đầu vào là gì?
3. Xử lý là gì?
4. Đầu ra là gì?
5. Khi tính tổng, biến `tong` ban đầu bằng bao nhiêu?

Gợi ý trả lời:

```text
1. Gồm 3 phần: đầu vào, xử lý, đầu ra.
2. Đầu vào là dữ liệu cần nhập.
3. Xử lý là công thức hoặc cách giải.
4. Đầu ra là kết quả cần in ra.
5. tong = 0.
```

Dẫn vào bài mới:

> Khi chương trình dài hơn, nếu viết tất cả trong `main()` thì code sẽ khó đọc.
> Hôm nay chúng ta học **hàm**, giúp chia chương trình thành nhiều phần nhỏ hơn.

---

# 3. Hàm là gì?

**Hàm** là một nhóm câu lệnh dùng để thực hiện một công việc cụ thể.

Ví dụ trong đời sống:

```text
Công việc: Pha nước cam

Có thể chia thành các bước:
1. Lấy ly.
2. Cắt cam.
3. Vắt cam.
4. Thêm đường.
5. Khuấy đều.
```

Trong lập trình, ta có thể gom các bước đó thành một “hàm”.

Ví dụ trong C++:

```cpp
void xinChao() {
    cout << "Xin chao cac ban!";
}
```

Hàm này có nhiệm vụ in lời chào.

---

# 4. Vì sao cần dùng hàm?

Hàm giúp chương trình:

```text
1. Dễ đọc hơn.
2. Dễ sửa hơn.
3. Tránh viết lại code nhiều lần.
4. Chia bài toán lớn thành nhiều phần nhỏ.
```

Ví dụ nếu cần in lời chào nhiều lần, thay vì viết:

```cpp
cout << "Xin chao!" << endl;
cout << "Xin chao!" << endl;
cout << "Xin chao!" << endl;
```

Ta có thể tạo hàm:

```cpp
void xinChao() {
    cout << "Xin chao!" << endl;
}
```

Sau đó gọi hàm nhiều lần:

```cpp
xinChao();
xinChao();
xinChao();
```

---

# 5. Hàm `main()` là gì?

Từ những bài đầu, chúng ta đã luôn viết:

```cpp
int main() {
    // Các lệnh trong chương trình
    return 0;
}
```

`main()` cũng là một hàm.

Điểm quan trọng:

```text
Chương trình C++ bắt đầu chạy từ hàm main().
```

Các hàm khác muốn chạy thì phải được gọi trong `main()` hoặc trong một hàm khác.

---

# 6. Hàm không trả về giá trị `void`

## Cấu trúc

```cpp
void tenHam() {
    // Các lệnh của hàm
}
```

Trong đó:

| Thành phần | Ý nghĩa                  |
| ---------- | ------------------------ |
| `void`     | Hàm không trả về giá trị |
| `tenHam`   | Tên của hàm              |
| `{ }`      | Chứa các lệnh của hàm    |

---

# 7. Ví dụ 1: Hàm in lời chào

## Chương trình

```cpp
#include <iostream>
using namespace std;

void xinChao() {
    cout << "Xin chao cac ban!" << endl;
}

int main() {
    xinChao();

    return 0;
}
```

## Kết quả

```text
Xin chao cac ban!
```

Giải thích:

```text
1. Ta tạo hàm xinChao().
2. Trong main(), ta gọi hàm bằng câu lệnh xinChao();
3. Khi được gọi, hàm xinChao() sẽ chạy lệnh cout bên trong nó.
```

---

# 8. Gọi hàm nhiều lần

Ta có thể gọi một hàm nhiều lần.

```cpp
#include <iostream>
using namespace std;

void xinChao() {
    cout << "Xin chao!" << endl;
}

int main() {
    xinChao();
    xinChao();
    xinChao();

    return 0;
}
```

Kết quả:

```text
Xin chao!
Xin chao!
Xin chao!
```

---

# 9. Ví dụ 2: Hàm in thông tin lớp học

```cpp
#include <iostream>
using namespace std;

void thongTinLop() {
    cout << "Lop: 6A" << endl;
    cout << "Mon hoc: Lap trinh C++" << endl;
    cout << "Chu de: Ham co ban" << endl;
}

int main() {
    thongTinLop();

    return 0;
}
```

Kết quả:

```text
Lop: 6A
Mon hoc: Lap trinh C++
Chu de: Ham co ban
```

---

# 10. Hàm có tham số

## Tham số là gì?

**Tham số** là dữ liệu đưa vào hàm để hàm sử dụng.

Ví dụ:

```cpp
void xinChao(string ten) {
    cout << "Xin chao " << ten << endl;
}
```

Ở đây, `ten` là tham số.

Khi gọi hàm:

```cpp
xinChao("Nam");
```

Hàm sẽ in:

```text
Xin chao Nam
```

---

# 11. Ví dụ 3: Hàm chào theo tên

```cpp
#include <iostream>
#include <string>
using namespace std;

void xinChao(string ten) {
    cout << "Xin chao " << ten << endl;
}

int main() {
    xinChao("Nam");
    xinChao("Lan");
    xinChao("An");

    return 0;
}
```

Kết quả:

```text
Xin chao Nam
Xin chao Lan
Xin chao An
```

Giải thích:

```text
Cùng một hàm xinChao(),
nhưng mỗi lần truyền tên khác nhau,
kết quả in ra cũng khác nhau.
```

---

# 12. Hàm có nhiều tham số

Một hàm có thể nhận nhiều tham số.

Ví dụ:

```cpp
void inTong(int a, int b) {
    cout << "Tong la: " << a + b << endl;
}
```

Chương trình đầy đủ:

```cpp
#include <iostream>
using namespace std;

void inTong(int a, int b) {
    cout << "Tong la: " << a + b << endl;
}

int main() {
    inTong(3, 5);
    inTong(10, 20);

    return 0;
}
```

Kết quả:

```text
Tong la: 8
Tong la: 30
```

---

# 13. Hàm có trả về giá trị

Ngoài hàm `void`, ta có thể viết hàm **trả về kết quả**.

Ví dụ:

```cpp
int tinhTong(int a, int b) {
    return a + b;
}
```

Giải thích:

| Thành phần      | Ý nghĩa                |
| --------------- | ---------------------- |
| `int`           | Hàm trả về số nguyên   |
| `tinhTong`      | Tên hàm                |
| `int a, int b`  | Hai tham số            |
| `return a + b;` | Trả về kết quả `a + b` |

---

# 14. Ví dụ 4: Hàm tính tổng hai số

```cpp
#include <iostream>
using namespace std;

int tinhTong(int a, int b) {
    return a + b;
}

int main() {
    int ketQua;

    ketQua = tinhTong(4, 6);

    cout << "Tong la: " << ketQua;

    return 0;
}
```

Kết quả:

```text
Tong la: 10
```

Ta cũng có thể viết ngắn hơn:

```cpp
cout << "Tong la: " << tinhTong(4, 6);
```

---

# 15. So sánh hàm `void` và hàm có `return`

| Loại hàm | Đặc điểm                          | Ví dụ            |
| -------- | --------------------------------- | ---------------- |
| `void`   | Làm việc gì đó, không trả kết quả | In lời chào      |
| `int`    | Trả về một số nguyên              | Tính tổng hai số |

Ví dụ hàm `void`:

```cpp
void xinChao() {
    cout << "Xin chao!";
}
```

Ví dụ hàm trả về `int`:

```cpp
int tinhTong(int a, int b) {
    return a + b;
}
```

---

# 16. Ví dụ 5: Hàm kiểm tra số chẵn

Có thể viết hàm kiểm tra số chẵn bằng kiểu `bool`.

```cpp
#include <iostream>
using namespace std;

bool laSoChan(int n) {
    return n % 2 == 0;
}

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (laSoChan(n)) {
        cout << "So chan";
    } else {
        cout << "So le";
    }

    return 0;
}
```

Giải thích:

```text
Hàm laSoChan(n) trả về true nếu n là số chẵn.
Nếu không, trả về false.
```

Nếu muốn đơn giản hơn cho học sinh, giáo viên có thể dùng hàm `void`:

```cpp
#include <iostream>
using namespace std;

void kiemTraChanLe(int n) {
    if (n % 2 == 0) {
        cout << "So chan";
    } else {
        cout << "So le";
    }
}

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    kiemTraChanLe(n);

    return 0;
}
```

---

# 17. Quy tắc đặt tên hàm

Tên hàm nên:

```text
- Không có dấu tiếng Việt.
- Không có khoảng trắng.
- Không bắt đầu bằng số.
- Dễ hiểu.
```

Tên hàm tốt:

```cpp
xinChao()
tinhTong()
kiemTraChanLe()
inBangCuuChuong()
```

Tên hàm không nên dùng:

```cpp
a()
ham1()
xuly()
```

Tên hàm sai:

```cpp
tinh tong()
1ham()
kiểmTra()
```

---

# 18. Lỗi thường gặp khi dùng hàm

## Lỗi 1: Quên gọi hàm

Sai:

```cpp
#include <iostream>
using namespace std;

void xinChao() {
    cout << "Xin chao!";
}

int main() {
    return 0;
}
```

Chương trình không in gì vì chưa gọi hàm.

Đúng:

```cpp
int main() {
    xinChao();
    return 0;
}
```

---

## Lỗi 2: Quên dấu `;` khi gọi hàm

Sai:

```cpp
xinChao()
```

Đúng:

```cpp
xinChao();
```

---

## Lỗi 3: Hàm có kiểu `int` nhưng quên `return`

Sai:

```cpp
int tinhTong(int a, int b) {
    a + b;
}
```

Đúng:

```cpp
int tinhTong(int a, int b) {
    return a + b;
}
```

---

## Lỗi 4: Gọi hàm sai số lượng tham số

Hàm:

```cpp
void inTong(int a, int b) {
    cout << a + b;
}
```

Sai:

```cpp
inTong(5);
```

Đúng:

```cpp
inTong(5, 3);
```

---

# 19. Hoạt động trên lớp

## Hoạt động 1: Viết hàm in lời chào

Yêu cầu:

```text
Viết hàm xinChao() để in ra "Xin chao lop 6".
Gọi hàm trong main().
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

void xinChao() {
    cout << "Xin chao lop 6";
}

int main() {
    xinChao();

    return 0;
}
```

---

## Hoạt động 2: Viết hàm tính tổng

Yêu cầu:

```text
Viết hàm tinhTong(a, b) trả về tổng của a và b.
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int tinhTong(int a, int b) {
    return a + b;
}

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Tong la: " << tinhTong(a, b);

    return 0;
}
```

---

## Hoạt động 3: Viết hàm kiểm tra chẵn lẻ

Yêu cầu:

```text
Viết hàm kiemTraChanLe(n).
Nếu n chẵn thì in "So chan", ngược lại in "So le".
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

void kiemTraChanLe(int n) {
    if (n % 2 == 0) {
        cout << "So chan";
    } else {
        cout << "So le";
    }
}

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    kiemTraChanLe(n);

    return 0;
}
```

---

# 20. Bài tập trên lớp

## Bài 1

Viết hàm:

```cpp
void inTen()
```

để in tên của em ra màn hình.

---

## Bài 2

Viết hàm:

```cpp
void inLoiChao()
```

để in:

```text
Xin chao cac ban!
```

Sau đó gọi hàm 3 lần trong `main()`.

---

## Bài 3

Viết hàm:

```cpp
int tinhTong(int a, int b)
```

trả về tổng hai số.

---

## Bài 4

Viết hàm:

```cpp
int tinhTich(int a, int b)
```

trả về tích hai số.

---

## Bài 5

Viết hàm:

```cpp
void kiemTraChanLe(int n)
```

để kiểm tra số chẵn lẻ.

---

# 21. Bài tập thực hành

## Bài 1: Hàm tính hiệu

Viết hàm:

```cpp
int tinhHieu(int a, int b)
```

trả về `a - b`.

---

## Bài 2: Hàm tính diện tích hình chữ nhật

Viết hàm:

```cpp
int tinhDienTich(int dai, int rong)
```

trả về diện tích hình chữ nhật.

Gợi ý:

```cpp
return dai * rong;
```

---

## Bài 3: Hàm tính chu vi hình chữ nhật

Viết hàm:

```cpp
int tinhChuVi(int dai, int rong)
```

trả về chu vi hình chữ nhật.

Gợi ý:

```cpp
return (dai + rong) * 2;
```

---

## Bài 4: Hàm kiểm tra điểm đạt

Viết hàm:

```cpp
void kiemTraDiem(float diem)
```

Nếu điểm `>= 5` thì in `Dat`, ngược lại in `Chua dat`.

---

# 22. Câu hỏi củng cố

Giáo viên hỏi học sinh:

1. Hàm là gì?
2. Vì sao cần dùng hàm?
3. Chương trình C++ bắt đầu chạy từ hàm nào?
4. `void` nghĩa là gì?
5. Muốn gọi hàm `xinChao`, viết thế nào?
6. Hàm `int tinhTong(int a, int b)` trả về kiểu dữ liệu gì?
7. Lệnh `return` dùng để làm gì?

Gợi ý trả lời:

```text
1. Hàm là nhóm câu lệnh thực hiện một công việc cụ thể.
2. Để chương trình dễ đọc, dễ sửa, tránh viết lặp lại code.
3. Chương trình bắt đầu từ hàm main().
4. void nghĩa là hàm không trả về giá trị.
5. xinChao();
6. Trả về kiểu int.
7. return dùng để trả kết quả từ hàm.
```

---

# 23. Bài tập về nhà

## Bài 1

Viết chương trình có hàm `xinChao()` để in:

```text
Xin chao lop 6
```

Gọi hàm trong `main()`.

---

## Bài 2

Viết hàm `tinhTong(int a, int b)` trả về tổng hai số. Nhập `a`, `b` từ bàn phím rồi in kết quả.

---

## Bài 3

Viết hàm `tinhDienTich(int dai, int rong)` trả về diện tích hình chữ nhật.

---

## Bài 4

Viết hàm `kiemTraChanLe(int n)` để kiểm tra số chẵn lẻ.

---

# 24. Tóm tắt bài học

Học sinh cần nhớ:

```text
Hàm là một nhóm câu lệnh dùng để làm một công việc cụ thể.

Cấu trúc hàm không trả về giá trị:

void tenHam() {
    // lệnh
}

Cấu trúc hàm có trả về giá trị:

int tenHam() {
    return giaTri;
}

Gọi hàm:

tenHam();

Hàm giúp:
- Code gọn hơn
- Dễ đọc hơn
- Dễ sửa hơn
- Tránh viết lại code nhiều lần
```

Mẫu quan trọng:

```cpp
#include <iostream>
using namespace std;

int tinhTong(int a, int b) {
    return a + b;
}

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Tong la: " << tinhTong(a, b);

    return 0;
}
```

---

# 25. Gợi ý thời lượng dạy 60 phút

| Phần                                  | Thời lượng |
| ------------------------------------- | ---------: |
| Ôn bài cũ                             |     5 phút |
| Giới thiệu hàm                        |     8 phút |
| Hàm `void`                            |    10 phút |
| Hàm có tham số                        |    10 phút |
| Hàm có trả về giá trị                 |    12 phút |
| Thực hành viết hàm tính tổng, chẵn lẻ |    12 phút |
| Củng cố, giao bài tập                 |     3 phút |

Tổng: **60 phút**.
