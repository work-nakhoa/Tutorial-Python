# Bài 6: Các phép toán cơ bản trong C++

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Biết các phép toán cơ bản trong C++.
* Biết dùng `+`, `-`, `*`, `/`, `%`.
* Biết nhập dữ liệu rồi tính toán.
* Biết lưu kết quả phép tính vào biến.
* Biết phân biệt chia thường `/` và chia lấy dư `%`.
* Biết viết chương trình tính chu vi, diện tích hình vuông, hình chữ nhật.
* Biết chú ý thứ tự ưu tiên phép toán.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. `cin` dùng để làm gì?
2. `cout` dùng để làm gì?
3. Muốn nhập tuổi vào biến `tuoi`, viết thế nào?
4. Muốn nhập hai số `a`, `b`, viết thế nào?
5. Chương trình sau làm gì?

```cpp
int a, b;
cin >> a >> b;
cout << a + b;
```

Gợi ý trả lời:

```text
1. cin dùng để nhập dữ liệu từ bàn phím.
2. cout dùng để in dữ liệu ra màn hình.
3. cin >> tuoi;
4. cin >> a >> b;
5. Nhập hai số a, b rồi in ra tổng của chúng.
```

Giáo viên dẫn vào bài mới:

> Ở bài trước, chúng ta đã biết nhập dữ liệu từ bàn phím.
> Hôm nay, chúng ta sẽ học cách dùng C++ để tính toán như một chiếc máy tính.

---

# 3. Phép toán trong C++ là gì?

Trong lập trình, **phép toán** là cách để máy tính tính toán dữ liệu.

Ví dụ:

```cpp
cout << 5 + 3;
```

Kết quả:

```text
8
```

Hoặc:

```cpp
int a = 10;
int b = 4;

cout << a - b;
```

Kết quả:

```text
6
```

---

# 4. Các phép toán cơ bản

Trong C++, các phép toán cơ bản gồm:

| Phép toán   | Ký hiệu trong C++ | Ví dụ    | Kết quả |
| ----------- | ----------------: | -------- | ------: |
| Cộng        |               `+` | `5 + 3`  |     `8` |
| Trừ         |               `-` | `5 - 3`  |     `2` |
| Nhân        |               `*` | `5 * 3`  |    `15` |
| Chia        |               `/` | `10 / 2` |     `5` |
| Chia lấy dư |               `%` | `10 % 3` |     `1` |

Giáo viên nhấn mạnh:

> Trong C++, phép nhân không viết là `x` mà viết là `*`.
> Phép chia viết là `/`.

---

# 5. Phép cộng `+`

Phép cộng dùng để cộng hai giá trị.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int b = 3;

    cout << "Tong la: " << a + b;

    return 0;
}
```

Kết quả:

```text
Tong la: 8
```

Có thể lưu kết quả vào biến:

```cpp
int tong = a + b;
cout << tong;
```

Ví dụ đầy đủ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int b = 3;
    int tong = a + b;

    cout << "Tong la: " << tong;

    return 0;
}
```

---

# 6. Phép trừ `-`

Phép trừ dùng để lấy số này trừ số khác.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int b = 4;

    cout << "Hieu la: " << a - b;

    return 0;
}
```

Kết quả:

```text
Hieu la: 6
```

Ví dụ có nhập dữ liệu:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Hieu la: " << a - b;

    return 0;
}
```

---

# 7. Phép nhân `*`

Trong C++, phép nhân dùng dấu:

```cpp
*
```

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 6;
    int b = 4;

    cout << "Tich la: " << a * b;

    return 0;
}
```

Kết quả:

```text
Tich la: 24
```

Lưu ý:

Sai:

```cpp
cout << a x b;
```

Đúng:

```cpp
cout << a * b;
```

---

# 8. Phép chia `/`

Trong C++, phép chia dùng dấu:

```cpp
/
```

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 20;
    int b = 5;

    cout << "Thuong la: " << a / b;

    return 0;
}
```

Kết quả:

```text
Thuong la: 4
```

Ví dụ nhập dữ liệu:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Thuong la: " << a / b;

    return 0;
}
```

---

# 9. Lưu ý quan trọng về chia số nguyên

Nếu cả hai số đều là `int`, C++ sẽ chia theo kiểu số nguyên.

Ví dụ:

```cpp
cout << 5 / 2;
```

Kết quả:

```text
2
```

Không phải `2.5`.

Vì `5` và `2` đều là số nguyên, nên C++ lấy phần nguyên.

Nếu muốn ra kết quả thập phân, dùng `float` hoặc `double`.

```cpp
#include <iostream>
using namespace std;

int main() {
    float a = 5;
    float b = 2;

    cout << a / b;

    return 0;
}
```

Kết quả:

```text
2.5
```

Giáo viên nhấn mạnh:

> Nếu muốn chia ra số thập phân, nên dùng `float` hoặc `double`.

---

# 10. Phép chia lấy dư `%`

Phép `%` dùng để lấy **số dư** của phép chia.

Ví dụ:

```cpp
cout << 10 % 3;
```

Vì:

```text
10 chia 3 được 3, dư 1
```

Nên kết quả là:

```text
1
```

Một số ví dụ:

| Biểu thức | Giải thích     | Kết quả |
| --------- | -------------- | ------: |
| `10 % 3`  | 10 chia 3 dư 1 |     `1` |
| `8 % 2`   | 8 chia 2 dư 0  |     `0` |
| `7 % 2`   | 7 chia 2 dư 1  |     `1` |
| `15 % 4`  | 15 chia 4 dư 3 |     `3` |

Ví dụ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int b = 3;

    cout << "So du la: " << a % b;

    return 0;
}
```

Kết quả:

```text
So du la: 1
```

Lưu ý:

> Phép `%` thường dùng với số nguyên `int`.

---

# 11. Ứng dụng `%`: Kiểm tra số chẵn, số lẻ

Một số chia cho 2:

* Nếu dư `0` thì là số chẵn.
* Nếu dư `1` thì là số lẻ.

Ví dụ:

```cpp
8 % 2 = 0
7 % 2 = 1
```

Ở bài này chưa học `if`, nên chỉ cần cho học sinh quan sát kết quả.

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap mot so: ";
    cin >> n;

    cout << "So du khi chia cho 2 la: " << n % 2;

    return 0;
}
```

Ví dụ chạy chương trình:

```text
Nhap mot so: 8
So du khi chia cho 2 la: 0
```

Hoặc:

```text
Nhap mot so: 7
So du khi chia cho 2 la: 1
```

Giáo viên nói:

> Sau này khi học câu lệnh `if`, chúng ta sẽ dùng `%` để kiểm tra số chẵn, số lẻ.

---

# 12. Tính toán với biến

Ta có thể dùng biến để tính toán.

Ví dụ:

```cpp
int a = 10;
int b = 5;

int tong = a + b;
int hieu = a - b;
int tich = a * b;
int thuong = a / b;
```

Chương trình đầy đủ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int b = 5;

    cout << "Tong: " << a + b << endl;
    cout << "Hieu: " << a - b << endl;
    cout << "Tich: " << a * b << endl;
    cout << "Thuong: " << a / b << endl;

    return 0;
}
```

Kết quả:

```text
Tong: 15
Hieu: 5
Tich: 50
Thuong: 2
```

---

# 13. Nhập hai số và tính đủ 4 phép toán

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Tong: " << a + b << endl;
    cout << "Hieu: " << a - b << endl;
    cout << "Tich: " << a * b << endl;
    cout << "Thuong: " << a / b << endl;
    cout << "So du: " << a % b;

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap a: 10
Nhap b: 3
Tong: 13
Hieu: 7
Tich: 30
Thuong: 3
So du: 1
```

Giáo viên lưu ý:

> Không nên nhập `b = 0` khi đang làm phép chia, vì không thể chia cho 0.

---

# 14. Không được chia cho 0

Trong toán học, ta không chia cho 0.

Trong C++ cũng vậy.

Sai:

```cpp
int a = 10;
int b = 0;

cout << a / b;
```

Chương trình có thể bị lỗi.

Giáo viên nhắc:

```text
Không nhập số chia là 0.
Ví dụ với a / b thì b không được bằng 0.
Ví dụ với a % b thì b không được bằng 0.
```

---

# 15. Thứ tự ưu tiên phép toán

C++ tính toán gần giống toán học.

Thứ tự cơ bản:

```text
1. Trong ngoặc ()
2. Nhân *, chia /, chia lấy dư %
3. Cộng +, trừ -
```

Ví dụ:

```cpp
cout << 2 + 3 * 4;
```

Kết quả:

```text
14
```

Vì máy tính làm:

```text
3 * 4 = 12
2 + 12 = 14
```

Nếu muốn cộng trước, dùng dấu ngoặc:

```cpp
cout << (2 + 3) * 4;
```

Kết quả:

```text
20
```

Vì máy tính làm:

```text
2 + 3 = 5
5 * 4 = 20
```

Giáo viên nhấn mạnh:

> Khi công thức phức tạp, nên dùng dấu ngoặc để rõ ràng và tránh sai.

---

# 16. Ví dụ: Tính chu vi hình chữ nhật

Công thức:

```text
Chu vi = (dài + rộng) * 2
```

Chương trình:

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

    cout << "Chu vi hinh chu nhat la: " << chuVi;

    return 0;
}
```

Ví dụ:

```text
Nhap chieu dai: 5
Nhap chieu rong: 3
Chu vi hinh chu nhat la: 16
```

---

# 17. Ví dụ: Tính diện tích hình chữ nhật

Công thức:

```text
Diện tích = dài * rộng
```

Chương trình:

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

    cout << "Dien tich hinh chu nhat la: " << dienTich;

    return 0;
}
```

Ví dụ:

```text
Nhap chieu dai: 5
Nhap chieu rong: 3
Dien tich hinh chu nhat la: 15
```

---

# 18. Ví dụ: Tính chu vi và diện tích hình vuông

Hình vuông có một cạnh là `canh`.

Công thức:

```text
Chu vi = canh * 4
Diện tích = canh * canh
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int canh;

    cout << "Nhap canh hinh vuong: ";
    cin >> canh;

    cout << "Chu vi hinh vuong la: " << canh * 4 << endl;
    cout << "Dien tich hinh vuong la: " << canh * canh;

    return 0;
}
```

Ví dụ:

```text
Nhap canh hinh vuong: 6
Chu vi hinh vuong la: 24
Dien tich hinh vuong la: 36
```

---

# 19. Ví dụ: Đổi giờ sang phút

Một giờ có 60 phút.

Công thức:

```text
Số phút = số giờ * 60
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int gio;
    int phut;

    cout << "Nhap so gio: ";
    cin >> gio;

    phut = gio * 60;

    cout << gio << " gio = " << phut << " phut";

    return 0;
}
```

Ví dụ:

```text
Nhap so gio: 2
2 gio = 120 phut
```

---

# 20. Ví dụ: Đổi ngày sang giờ

Một ngày có 24 giờ.

Công thức:

```text
Số giờ = số ngày * 24
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int ngay;
    int gio;

    cout << "Nhap so ngay: ";
    cin >> ngay;

    gio = ngay * 24;

    cout << ngay << " ngay = " << gio << " gio";

    return 0;
}
```

Ví dụ:

```text
Nhap so ngay: 3
3 ngay = 72 gio
```

---

# 21. Quy trình giải bài toán tính toán

Khi gặp bài toán tính toán, học sinh làm theo các bước:

```text
Bước 1: Đọc đề bài.
Bước 2: Xác định cần nhập gì.
Bước 3: Xác định cần tính gì.
Bước 4: Viết công thức.
Bước 5: Chuyển công thức thành code C++.
Bước 6: In kết quả.
```

Ví dụ bài toán:

```text
Nhập chiều dài và chiều rộng, tính diện tích hình chữ nhật.
```

Phân tích:

```text
Cần nhập: dài, rộng
Cần tính: diện tích
Công thức: diện tích = dài * rộng
Code: dienTich = dai * rong;
```

---

# 22. Hoạt động thực hành 1: Tính tổng hai số

Yêu cầu học sinh nhập hai số nguyên rồi in tổng.

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Tong la: " << a + b;

    return 0;
}
```

---

# 23. Hoạt động thực hành 2: Tính chu vi hình chữ nhật

Yêu cầu học sinh nhập chiều dài, chiều rộng rồi tính chu vi.

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int dai, rong;

    cout << "Nhap chieu dai: ";
    cin >> dai;

    cout << "Nhap chieu rong: ";
    cin >> rong;

    cout << "Chu vi la: " << (dai + rong) * 2;

    return 0;
}
```

---

# 24. Hoạt động thực hành 3: Tính diện tích hình chữ nhật

Yêu cầu học sinh nhập chiều dài, chiều rộng rồi tính diện tích.

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int dai, rong;

    cout << "Nhap chieu dai: ";
    cin >> dai;

    cout << "Nhap chieu rong: ";
    cin >> rong;

    cout << "Dien tich la: " << dai * rong;

    return 0;
}
```

---

# 25. Hoạt động thực hành 4: Tính tuổi từ năm sinh

Yêu cầu học sinh nhập năm sinh, sau đó tính tuổi gần đúng.

Ví dụ dùng năm hiện tại là `2026`.

Công thức:

```text
Tuổi = 2026 - năm sinh
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int namSinh;
    int tuoi;

    cout << "Nhap nam sinh: ";
    cin >> namSinh;

    tuoi = 2026 - namSinh;

    cout << "Tuoi cua em la: " << tuoi;

    return 0;
}
```

Ví dụ:

```text
Nhap nam sinh: 2014
Tuoi cua em la: 12
```

---

# 26. Hoạt động thực hành 5: Tính số dư

Yêu cầu học sinh nhập hai số nguyên `a`, `b`, sau đó in ra số dư của `a` chia cho `b`.

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "So du la: " << a % b;

    return 0;
}
```

Ví dụ:

```text
Nhap a: 17
Nhap b: 5
So du la: 2
```

---

# 27. Lỗi thường gặp

## Lỗi 1: Dùng sai dấu nhân

Sai:

```cpp
cout << a x b;
```

Đúng:

```cpp
cout << a * b;
```

---

## Lỗi 2: Dùng sai dấu chia

Sai:

```cpp
cout << a : b;
```

Đúng:

```cpp
cout << a / b;
```

---

## Lỗi 3: Quên dấu ngoặc trong công thức

Sai:

```cpp
chuVi = dai + rong * 2;
```

Nếu `dai = 5`, `rong = 3`, kết quả sẽ là:

```text
5 + 3 * 2 = 11
```

Đúng:

```cpp
chuVi = (dai + rong) * 2;
```

Kết quả đúng:

```text
(5 + 3) * 2 = 16
```

---

## Lỗi 4: Chia số nguyên nhưng muốn ra số thập phân

Ví dụ:

```cpp
int a = 5;
int b = 2;
cout << a / b;
```

Kết quả:

```text
2
```

Nếu muốn ra `2.5`, dùng `float`:

```cpp
float a = 5;
float b = 2;
cout << a / b;
```

---

## Lỗi 5: Chia cho 0

Sai:

```cpp
int a = 10;
int b = 0;

cout << a / b;
```

Không được chia cho `0`.

---

# 28. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

Trong C++, phép nhân dùng ký hiệu nào?

A. `x`
B. `*`
C. `:`
D. `#`

Đáp án: **B**

---

## Bài 2: Chọn đáp án đúng

Trong C++, phép chia dùng ký hiệu nào?

A. `:`
B. `\`
C. `/`
D. `|`

Đáp án: **C**

---

## Bài 3: Điền từ còn thiếu

```text
Phép % dùng để lấy ______ của phép chia.
```

Đáp án:

```text
số dư
```

---

## Bài 4: Đoán kết quả

```cpp
cout << 7 + 3 * 2;
```

Đáp án:

```text
13
```

Giải thích:

```text
3 * 2 = 6
7 + 6 = 13
```

---

## Bài 5: Đoán kết quả

```cpp
cout << (7 + 3) * 2;
```

Đáp án:

```text
20
```

Giải thích:

```text
7 + 3 = 10
10 * 2 = 20
```

---

## Bài 6: Đoán kết quả

```cpp
cout << 10 % 3;
```

Đáp án:

```text
1
```

---

## Bài 7: Tìm lỗi sai

Chương trình sau sai ở đâu?

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int b = 3;

    cout << a x b;

    return 0;
}
```

Lỗi:

```text
Trong C++, phép nhân phải dùng dấu *.
```

Sửa đúng:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int b = 3;

    cout << a * b;

    return 0;
}
```

---

# 29. Bài tập thực hành

## Bài 1

Viết chương trình nhập hai số nguyên `a`, `b`, sau đó in ra:

```text
Tong: ...
Hieu: ...
Tich: ...
Thuong: ...
```

---

## Bài 2

Viết chương trình nhập cạnh hình vuông, sau đó tính:

```text
Chu vi hinh vuong
Dien tich hinh vuong
```

---

## Bài 3

Viết chương trình nhập chiều dài và chiều rộng hình chữ nhật, sau đó tính:

```text
Chu vi hinh chu nhat
Dien tich hinh chu nhat
```

---

## Bài 4

Viết chương trình nhập số giờ, sau đó đổi ra số phút.

Ví dụ:

```text
Nhap so gio: 4
4 gio = 240 phut
```

---

## Bài 5

Viết chương trình nhập số ngày, sau đó đổi ra số giờ.

Ví dụ:

```text
Nhap so ngay: 5
5 ngay = 120 gio
```

---

## Bài 6

Viết chương trình nhập một số nguyên `n`, sau đó in ra số dư khi `n` chia cho `2`.

Ví dụ:

```text
Nhap n: 9
So du khi chia cho 2 la: 1
```

---

# 30. Bài tập nâng cao nhẹ

## Bài 1: Tính tổng tiền mua hàng

Bài toán:

```text
Nhập giá một quyển vở.
Nhập số lượng vở.
Tính tổng tiền cần trả.
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaVo;
    int soLuong;
    int tongTien;

    cout << "Nhap gia mot quyen vo: ";
    cin >> giaVo;

    cout << "Nhap so luong vo: ";
    cin >> soLuong;

    tongTien = giaVo * soLuong;

    cout << "Tong tien can tra la: " << tongTien;

    return 0;
}
```

---

## Bài 2: Chia kẹo

Bài toán:

```text
Có n cái kẹo chia đều cho m bạn.
Hỏi mỗi bạn được bao nhiêu cái kẹo và còn dư bao nhiêu cái?
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int keo, ban;

    cout << "Nhap so keo: ";
    cin >> keo;

    cout << "Nhap so ban: ";
    cin >> ban;

    cout << "Moi ban duoc: " << keo / ban << " cai keo" << endl;
    cout << "Con du: " << keo % ban << " cai keo";

    return 0;
}
```

Ví dụ:

```text
Nhap so keo: 17
Nhap so ban: 5
Moi ban duoc: 3 cai keo
Con du: 2 cai keo
```

---

## Bài 3: Đổi tiền đơn giản

Bài toán:

```text
Một món đồ có giá x đồng.
Em đưa y đồng.
Hỏi cần trả lại bao nhiêu tiền?
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaTien;
    int tienDua;
    int tienThua;

    cout << "Nhap gia tien mon do: ";
    cin >> giaTien;

    cout << "Nhap so tien dua: ";
    cin >> tienDua;

    tienThua = tienDua - giaTien;

    cout << "Tien thua la: " << tienThua;

    return 0;
}
```

---

# 31. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. Trong C++, phép cộng dùng ký hiệu gì?
2. Trong C++, phép trừ dùng ký hiệu gì?
3. Trong C++, phép nhân dùng ký hiệu gì?
4. Trong C++, phép chia dùng ký hiệu gì?
5. Phép `%` dùng để làm gì?
6. `10 % 3` bằng bao nhiêu?
7. `5 / 2` với kiểu `int` cho kết quả bao nhiêu?
8. Vì sao công thức chu vi hình chữ nhật cần viết `(dai + rong) * 2`?

Gợi ý trả lời:

```text
1. Dùng dấu +
2. Dùng dấu -
3. Dùng dấu *
4. Dùng dấu /
5. Dùng để lấy số dư
6. Bằng 1
7. Bằng 2
8. Vì cần cộng dài và rộng trước, rồi mới nhân 2.
```

---

# 32. Bài tập về nhà

## Bài 1

Viết chương trình nhập hai số nguyên `a`, `b`, sau đó in ra:

```text
Tong: ...
Hieu: ...
Tich: ...
```

---

## Bài 2

Viết chương trình nhập cạnh hình vuông, sau đó tính chu vi và diện tích.

---

## Bài 3

Viết chương trình nhập chiều dài và chiều rộng hình chữ nhật, sau đó tính chu vi và diện tích.

---

## Bài 4

Viết chương trình nhập số phút, sau đó đổi ra số giây.

Gợi ý:

```text
1 phút = 60 giây
Số giây = số phút * 60
```

---

## Bài 5

Viết chương trình nhập số kẹo và số bạn. Tính:

```text
Mỗi bạn được bao nhiêu cái kẹo?
Còn dư bao nhiêu cái kẹo?
```

Gợi ý:

```cpp
cout << keo / ban;
cout << keo % ban;
```

---

# 33. Tóm tắt bài học

Học sinh cần nhớ:

```text
Các phép toán cơ bản trong C++:

+  cộng
-  trừ
*  nhân
/  chia
%  chia lấy dư

Thứ tự ưu tiên:
1. Dấu ngoặc ()
2. Nhân, chia, chia lấy dư
3. Cộng, trừ

Không được chia cho 0.
Muốn chia ra số thập phân, dùng float hoặc double.
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    cout << "Tong: " << a + b << endl;
    cout << "Hieu: " << a - b << endl;
    cout << "Tich: " << a * b << endl;
    cout << "Thuong: " << a / b << endl;
    cout << "So du: " << a % b;

    return 0;
}
```

---

# 34. Gợi ý thời lượng dạy

| Phần                     | Thời lượng |
| ------------------------ | ---------: |
| Ôn bài cũ                |     5 phút |
| Giới thiệu phép toán     |    10 phút |
| Cộng, trừ, nhân, chia    |    15 phút |
| Chia lấy dư `%`          |    10 phút |
| Thứ tự ưu tiên phép toán |    10 phút |
| Thực hành bài hình học   |    15 phút |
| Củng cố và giao bài tập  |     5 phút |

Tổng thời lượng: khoảng **70 phút**.
