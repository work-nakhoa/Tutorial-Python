# Bài 4: Biến và kiểu dữ liệu

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu biến là gì.
* Biết vì sao cần dùng biến trong lập trình.
* Biết khai báo biến trong C++.
* Biết một số kiểu dữ liệu cơ bản:

  * `int`
  * `float`
  * `double`
  * `char`
  * `string`
  * `bool`
* Biết gán giá trị cho biến.
* Biết in giá trị của biến ra màn hình bằng `cout`.
* Viết được chương trình lưu và in thông tin học sinh.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. `cout` dùng để làm gì?
2. Khi in chữ, ta đặt chữ trong dấu gì?
3. Muốn xuống dòng, ta dùng gì?
4. Dấu `;` dùng để làm gì?
5. Chương trình sau in ra gì?

```cpp
cout << "Xin chao lop 6";
```

Gợi ý trả lời:

```text
1. cout dùng để in ra màn hình.
2. Đặt chữ trong dấu ngoặc kép " ".
3. Dùng endl hoặc \n.
4. Dấu ; dùng để kết thúc câu lệnh.
5. In ra: Xin chao lop 6
```

Giáo viên dẫn vào bài mới:

> Ở bài trước, chúng ta đã biết cách in chữ và số ra màn hình.
> Hôm nay, chúng ta sẽ học cách lưu dữ liệu trong chương trình bằng **biến**.

---

# 3. Biến là gì?

## Giải thích đơn giản

**Biến** là nơi dùng để lưu trữ dữ liệu trong chương trình.

Có thể hiểu biến giống như một chiếc hộp.

Ví dụ:

```text
Hộp tên     → lưu tên học sinh
Hộp tuổi    → lưu tuổi học sinh
Hộp điểm    → lưu điểm học sinh
```

Trong lập trình, ta có thể tạo ra các “hộp” như vậy để lưu thông tin.

Ví dụ:

```cpp
int tuoi = 11;
```

Dòng này có nghĩa là:

```text
Tạo một biến tên là tuoi để lưu số 11.
```

---

# 4. Vì sao cần dùng biến?

Giáo viên đưa ví dụ:

Nếu muốn in tuổi của một học sinh, ta có thể viết:

```cpp
cout << 11;
```

Nhưng nếu nhiều chỗ trong chương trình đều cần dùng tuổi, viết số trực tiếp sẽ khó sửa.

Ví dụ:

```cpp
cout << "Tuoi cua em la ";
cout << 11;
```

Nếu sau này tuổi đổi thành `12`, ta phải đi sửa nhiều chỗ.

Thay vào đó, ta dùng biến:

```cpp
int tuoi = 11;
cout << "Tuoi cua em la " << tuoi;
```

Khi cần đổi tuổi, chỉ cần sửa:

```cpp
int tuoi = 12;
```

Kết luận:

> Biến giúp chương trình dễ đọc, dễ sửa và dễ sử dụng lại dữ liệu.

---

# 5. Cách khai báo biến trong C++

Cấu trúc khai báo biến:

```cpp
kieu_du_lieu ten_bien;
```

Ví dụ:

```cpp
int tuoi;
```

Nghĩa là:

```text
Tạo một biến tên là tuoi, dùng để lưu số nguyên.
```

Ta cũng có thể khai báo biến và gán giá trị ngay:

```cpp
int tuoi = 11;
```

Nghĩa là:

```text
Tạo biến tuoi và cho nó giá trị ban đầu là 11.
```

---

# 6. Kiểu dữ liệu là gì?

**Kiểu dữ liệu** cho biết biến sẽ lưu loại dữ liệu nào.

Ví dụ trong đời sống:

| Dữ liệu            | Loại dữ liệu  |
| ------------------ | ------------- |
| Tuổi               | Số nguyên     |
| Chiều cao          | Số thập phân  |
| Tên                | Chuỗi chữ     |
| Giới tính viết tắt | Một ký tự     |
| Đúng hoặc sai      | Giá trị logic |

Trong C++, mỗi biến cần có một kiểu dữ liệu.

---

# 7. Các kiểu dữ liệu cơ bản trong C++

## 7.1. Kiểu `int`

`int` dùng để lưu **số nguyên**.

Ví dụ:

```cpp
int tuoi = 11;
int soHocSinh = 35;
int namSinh = 2013;
```

Số nguyên là số không có phần thập phân.

Ví dụ số nguyên:

```text
1, 2, 10, 100, -5, 0
```

Ví dụ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi = 11;

    cout << "Tuoi cua em la: " << tuoi;

    return 0;
}
```

Kết quả:

```text
Tuoi cua em la: 11
```

---

## 7.2. Kiểu `float`

`float` dùng để lưu **số thập phân**.

Ví dụ:

```cpp
float diemToan = 8.5;
float chieuCao = 1.45;
```

Ví dụ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    float diemToan = 8.5;

    cout << "Diem Toan cua em la: " << diemToan;

    return 0;
}
```

Kết quả:

```text
Diem Toan cua em la: 8.5
```

---

## 7.3. Kiểu `double`

`double` cũng dùng để lưu số thập phân, nhưng có thể lưu chính xác hơn `float`.

Ví dụ:

```cpp
double diemTrungBinh = 8.75;
double canNang = 36.5;
```

Với học sinh lớp 6, giáo viên có thể giải thích đơn giản:

> `float` và `double` đều dùng để lưu số thập phân.
> Khi mới học, các em có thể dùng `float` cho dễ nhớ.

---

## 7.4. Kiểu `char`

`char` dùng để lưu **một ký tự**.

Ví dụ:

```cpp
char xepLoai = 'A';
char kyTu = 'K';
```

Lưu ý:

* `char` dùng dấu nháy đơn `' '`.
* `string` dùng dấu ngoặc kép `" "`.

Ví dụ đúng:

```cpp
char chuCai = 'A';
```

Ví dụ sai:

```cpp
char chuCai = "A";
```

Ví dụ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    char xepLoai = 'A';

    cout << "Xep loai: " << xepLoai;

    return 0;
}
```

Kết quả:

```text
Xep loai: A
```

---

## 7.5. Kiểu `string`

`string` dùng để lưu **chuỗi ký tự**, tức là nhiều chữ ghép lại.

Ví dụ:

```cpp
string ten = "Nam";
string lop = "6A";
string truong = "THCS Hoa Binh";
```

Ví dụ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    string ten = "Nam";

    cout << "Ten cua em la: " << ten;

    return 0;
}
```

Kết quả:

```text
Ten cua em la: Nam
```

Lưu ý:

> Khi dùng `string`, trong một số môi trường cần thêm dòng `#include <string>`.
> Nhưng với chương trình cơ bản dùng `iostream`, nhiều môi trường vẫn chạy được.
> Để chắc chắn, có thể viết như sau:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "Nam";

    cout << "Ten cua em la: " << ten;

    return 0;
}
```

---

## 7.6. Kiểu `bool`

`bool` dùng để lưu giá trị **đúng hoặc sai**.

Trong C++:

```text
true  = đúng
false = sai
```

Ví dụ:

```cpp
bool daLamBaiTap = true;
bool nghiHoc = false;
```

Ví dụ chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    bool daLamBaiTap = true;

    cout << daLamBaiTap;

    return 0;
}
```

Kết quả thường là:

```text
1
```

Giải thích đơn giản:

```text
true  thường được in ra là 1
false thường được in ra là 0
```

Ở bài này, chỉ cần học sinh biết `bool` dùng để lưu đúng/sai.

---

# 8. Bảng tóm tắt kiểu dữ liệu

| Kiểu dữ liệu | Dùng để lưu                | Ví dụ                    |
| ------------ | -------------------------- | ------------------------ |
| `int`        | Số nguyên                  | `int tuoi = 11;`         |
| `float`      | Số thập phân               | `float diem = 8.5;`      |
| `double`     | Số thập phân chính xác hơn | `double canNang = 36.5;` |
| `char`       | Một ký tự                  | `char loai = 'A';`       |
| `string`     | Chuỗi chữ                  | `string ten = "Nam";`    |
| `bool`       | Đúng hoặc sai              | `bool dat = true;`       |

---

# 9. Gán giá trị cho biến

Sau khi tạo biến, ta có thể gán giá trị cho biến.

Ví dụ:

```cpp
int tuoi;
tuoi = 11;
```

Hai dòng trên có nghĩa là:

```text
Tạo biến tuoi.
Gán giá trị 11 cho biến tuoi.
```

Ta cũng có thể viết gọn:

```cpp
int tuoi = 11;
```

Hai cách dưới đây có ý nghĩa giống nhau:

Cách 1:

```cpp
int tuoi;
tuoi = 11;
```

Cách 2:

```cpp
int tuoi = 11;
```

---

# 10. Thay đổi giá trị của biến

Biến có thể thay đổi giá trị trong quá trình chạy chương trình.

Ví dụ:

```cpp
int tuoi = 11;
cout << tuoi << endl;

tuoi = 12;
cout << tuoi;
```

Kết quả:

```text
11
12
```

Giải thích:

Ban đầu biến `tuoi` có giá trị `11`.

Sau đó ta gán lại:

```cpp
tuoi = 12;
```

Nên giá trị mới của `tuoi` là `12`.

Giáo viên nhấn mạnh:

> Biến giống như một chiếc hộp.
> Khi bỏ giá trị mới vào hộp, giá trị cũ sẽ được thay thế.

---

# 11. In biến ra màn hình

Muốn in giá trị của biến, ta dùng `cout`.

Ví dụ:

```cpp
int tuoi = 11;
cout << tuoi;
```

Kết quả:

```text
11
```

Lưu ý quan trọng:

Nếu viết:

```cpp
cout << "tuoi";
```

Kết quả là:

```text
tuoi
```

Nếu viết:

```cpp
cout << tuoi;
```

Kết quả là giá trị của biến:

```text
11
```

So sánh:

| Câu lệnh          | Kết quả                    |
| ----------------- | -------------------------- |
| `cout << "tuoi";` | In chữ `tuoi`              |
| `cout << tuoi;`   | In giá trị của biến `tuoi` |

---

# 12. Ví dụ hoàn chỉnh: In thông tin học sinh

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "Nam";
    int tuoi = 11;
    string lop = "6A";
    float diemToan = 8.5;

    cout << "THONG TIN HOC SINH" << endl;
    cout << "Ten: " << ten << endl;
    cout << "Tuoi: " << tuoi << endl;
    cout << "Lop: " << lop << endl;
    cout << "Diem Toan: " << diemToan;

    return 0;
}
```

Kết quả:

```text
THONG TIN HOC SINH
Ten: Nam
Tuoi: 11
Lop: 6A
Diem Toan: 8.5
```

---

# 13. Quy tắc đặt tên biến

Tên biến nên:

* Dễ hiểu.
* Không có dấu tiếng Việt.
* Không có khoảng trắng.
* Không bắt đầu bằng số.
* Không trùng với từ khóa của C++.
* Nên dùng chữ thường hoặc kiểu viết dễ đọc.

Ví dụ tên biến tốt:

```cpp
int tuoi;
string ten;
float diemToan;
int soHocSinh;
```

Ví dụ tên biến không nên dùng:

```cpp
int t;
string a;
float x;
```

Vì khó hiểu.

Ví dụ tên biến sai:

```cpp
int 1tuoi;
string ho ten;
float điểm;
```

Lý do:

| Tên biến sai | Vì sao sai?               |
| ------------ | ------------------------- |
| `1tuoi`      | Bắt đầu bằng số           |
| `ho ten`     | Có khoảng trắng           |
| `điểm`       | Có dấu tiếng Việt, dễ lỗi |
| `int`        | Trùng từ khóa C++         |

---

# 14. Phân biệt dấu `=` trong lập trình

Trong C++, dấu `=` có nghĩa là **gán giá trị**.

Ví dụ:

```cpp
int tuoi = 11;
```

Nghĩa là:

```text
Gán giá trị 11 cho biến tuoi.
```

Không nên hiểu là “tuổi bằng 11” như toán học hoàn toàn.

Ví dụ:

```cpp
tuoi = 12;
```

Nghĩa là:

```text
Đưa giá trị 12 vào biến tuoi.
```

Học sinh có thể hiểu:

```text
Bên phải đưa vào bên trái.
```

Ví dụ:

```cpp
tuoi = 11;
```

Nghĩa là đưa `11` vào biến `tuoi`.

---

# 15. Hoạt động thực hành 1: Tạo biến tuổi

Yêu cầu học sinh viết chương trình:

* Tạo biến `tuoi`.
* Gán giá trị `11`.
* In tuổi ra màn hình.

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi = 11;

    cout << "Tuoi cua em la: " << tuoi;

    return 0;
}
```

Kết quả:

```text
Tuoi cua em la: 11
```

---

# 16. Hoạt động thực hành 2: Tạo biến tên và lớp

Yêu cầu học sinh viết chương trình:

* Tạo biến `ten`.
* Tạo biến `lop`.
* In tên và lớp ra màn hình.

Gợi ý:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "Lan";
    string lop = "6A";

    cout << "Ten: " << ten << endl;
    cout << "Lop: " << lop;

    return 0;
}
```

Kết quả:

```text
Ten: Lan
Lop: 6A
```

---

# 17. Hoạt động thực hành 3: Thông tin học sinh

Yêu cầu học sinh tạo các biến:

```text
ten
tuoi
lop
diemToan
```

Sau đó in ra màn hình.

Gợi ý:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "Minh";
    int tuoi = 11;
    string lop = "6B";
    float diemToan = 9.0;

    cout << "===== THONG TIN =====" << endl;
    cout << "Ten: " << ten << endl;
    cout << "Tuoi: " << tuoi << endl;
    cout << "Lop: " << lop << endl;
    cout << "Diem Toan: " << diemToan << endl;
    cout << "====================";

    return 0;
}
```

---

# 18. Hoạt động thực hành 4: Thay đổi giá trị biến

Yêu cầu học sinh quan sát chương trình và đoán kết quả:

```cpp
#include <iostream>
using namespace std;

int main() {
    int diem = 8;

    cout << "Diem ban dau: " << diem << endl;

    diem = 10;

    cout << "Diem sau khi sua: " << diem;

    return 0;
}
```

Kết quả:

```text
Diem ban dau: 8
Diem sau khi sua: 10
```

Câu hỏi cho học sinh:

> Vì sao dòng thứ hai in ra 10 chứ không phải 8?

Gợi ý trả lời:

```text
Vì biến diem đã được gán giá trị mới là 10.
```

---

# 19. Lỗi thường gặp khi dùng biến

## Lỗi 1: Dùng biến khi chưa khai báo

Sai:

```cpp
tuoi = 11;
cout << tuoi;
```

Đúng:

```cpp
int tuoi = 11;
cout << tuoi;
```

Giải thích:

> Trước khi dùng biến, phải tạo biến trước.

---

## Lỗi 2: Gán sai kiểu dữ liệu

Sai:

```cpp
int ten = "Nam";
```

Đúng:

```cpp
string ten = "Nam";
```

Giải thích:

> `int` dùng cho số nguyên, không dùng để lưu tên.

---

## Lỗi 3: Quên dấu ngoặc kép với `string`

Sai:

```cpp
string ten = Nam;
```

Đúng:

```cpp
string ten = "Nam";
```

Giải thích:

> Chuỗi chữ phải đặt trong dấu `" "`.

---

## Lỗi 4: Dùng dấu ngoặc kép khi in biến

Không sai cú pháp, nhưng sai ý nghĩa.

Ví dụ:

```cpp
int tuoi = 11;

cout << "tuoi";
```

Kết quả:

```text
tuoi
```

Muốn in giá trị của biến, phải viết:

```cpp
cout << tuoi;
```

Kết quả:

```text
11
```

---

## Lỗi 5: Đặt tên biến có khoảng trắng

Sai:

```cpp
int diem toan = 9;
```

Đúng:

```cpp
int diemToan = 9;
```

Hoặc:

```cpp
int diem_toan = 9;
```

---

# 20. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

Biến dùng để làm gì?

A. In ra màn hình
B. Lưu trữ dữ liệu
C. Xóa chương trình
D. Tắt máy tính

Đáp án: **B**

---

## Bài 2: Nối kiểu dữ liệu với ý nghĩa

| Kiểu dữ liệu | Ý nghĩa         |
| ------------ | --------------- |
| `int`        | A. Chuỗi chữ    |
| `float`      | B. Số nguyên    |
| `string`     | C. Số thập phân |
| `char`       | D. Một ký tự    |

Đáp án:

```text
int    → B
float  → C
string → A
char   → D
```

---

## Bài 3: Điền từ còn thiếu

```text
Kiểu int dùng để lưu ______.
```

Đáp án:

```text
số nguyên
```

---

## Bài 4: Đoán kết quả

Chương trình sau in ra gì?

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi = 11;
    cout << tuoi;
    return 0;
}
```

Đáp án:

```text
11
```

---

## Bài 5: Đoán kết quả

Chương trình sau in ra gì?

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "An";
    cout << "Xin chao " << ten;
    return 0;
}
```

Đáp án:

```text
Xin chao An
```

---

## Bài 6: Tìm lỗi sai

Chương trình sau sai ở đâu?

```cpp
#include <iostream>
using namespace std;

int main() {
    int ten = "Nam";
    cout << ten;
    return 0;
}
```

Lỗi:

```text
Biến ten dùng để lưu chữ, nên phải dùng kiểu string, không phải int.
```

Sửa đúng:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "Nam";
    cout << ten;
    return 0;
}
```

---

# 21. Bài tập thực hành

## Bài 1

Viết chương trình tạo biến `tuoi` có giá trị `11`, sau đó in ra:

```text
Tuoi cua em la 11
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi = 11;

    cout << "Tuoi cua em la " << tuoi;

    return 0;
}
```

---

## Bài 2

Viết chương trình tạo biến:

```text
ten
lop
```

Sau đó in ra:

```text
Ten: Lan
Lop: 6A
```

Gợi ý:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "Lan";
    string lop = "6A";

    cout << "Ten: " << ten << endl;
    cout << "Lop: " << lop;

    return 0;
}
```

---

## Bài 3

Viết chương trình tạo các biến:

```text
ten
tuoi
lop
diemTinHoc
```

Sau đó in ra thông tin học sinh.

Ví dụ kết quả:

```text
Ten: Minh
Tuoi: 11
Lop: 6B
Diem Tin hoc: 9.5
```

---

## Bài 4

Viết chương trình tạo biến `soA = 10`, `soB = 5`, sau đó in ra:

```text
So thu nhat: 10
So thu hai: 5
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int soA = 10;
    int soB = 5;

    cout << "So thu nhat: " << soA << endl;
    cout << "So thu hai: " << soB;

    return 0;
}
```

---

## Bài 5

Quan sát chương trình và đoán kết quả:

```cpp
#include <iostream>
using namespace std;

int main() {
    int so = 3;

    cout << so << endl;

    so = 7;

    cout << so;

    return 0;
}
```

Đáp án:

```text
3
7
```

---

# 22. Bài tập nâng cao nhẹ

## Bài 1: Thẻ học sinh

Viết chương trình tạo các biến:

```text
ten
lop
truong
tuoi
```

Sau đó in ra mẫu:

```text
====================
    THE HOC SINH
====================
Ten: An
Tuoi: 11
Lop: 6A
Truong: THCS Hoa Binh
====================
```

Gợi ý:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "An";
    int tuoi = 11;
    string lop = "6A";
    string truong = "THCS Hoa Binh";

    cout << "====================" << endl;
    cout << "    THE HOC SINH" << endl;
    cout << "====================" << endl;
    cout << "Ten: " << ten << endl;
    cout << "Tuoi: " << tuoi << endl;
    cout << "Lop: " << lop << endl;
    cout << "Truong: " << truong << endl;
    cout << "====================";

    return 0;
}
```

---

## Bài 2: Thông tin môn học

Viết chương trình tạo các biến:

```text
monHoc
diem
dat
```

Trong đó:

```cpp
string monHoc = "Tin hoc";
float diem = 8.5;
bool dat = true;
```

In ra:

```text
Mon hoc: Tin hoc
Diem: 8.5
Dat: 1
```

Gợi ý:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string monHoc = "Tin hoc";
    float diem = 8.5;
    bool dat = true;

    cout << "Mon hoc: " << monHoc << endl;
    cout << "Diem: " << diem << endl;
    cout << "Dat: " << dat;

    return 0;
}
```

Giáo viên giải thích:

```text
Dat: 1 nghĩa là true, tức là đúng.
```

---

# 23. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. Biến là gì?
2. Biến dùng để làm gì?
3. Kiểu `int` dùng để lưu dữ liệu gì?
4. Kiểu `float` dùng để lưu dữ liệu gì?
5. Kiểu `string` dùng để lưu dữ liệu gì?
6. Muốn in giá trị của biến `tuoi`, viết `cout << tuoi;` hay `cout << "tuoi";`?
7. Tên biến có được chứa khoảng trắng không?

Gợi ý trả lời:

```text
1. Biến là nơi lưu trữ dữ liệu.
2. Biến dùng để lưu dữ liệu để chương trình sử dụng.
3. int dùng để lưu số nguyên.
4. float dùng để lưu số thập phân.
5. string dùng để lưu chuỗi chữ.
6. Viết cout << tuoi;
7. Không được chứa khoảng trắng.
```

---

# 24. Bài tập về nhà

## Bài 1

Viết chương trình tạo biến:

```text
ten
tuoi
```

Sau đó in ra:

```text
Xin chao, em ten la ...
Nam nay em ... tuoi
```

---

## Bài 2

Viết chương trình tạo biến:

```text
monHoc
diem
```

Ví dụ:

```cpp
string monHoc = "Toan";
float diem = 9.5;
```

Sau đó in ra:

```text
Mon hoc: Toan
Diem: 9.5
```

---

## Bài 3

Tìm lỗi sai trong chương trình sau và sửa lại:

```cpp
#include <iostream>
using namespace std;

int main() {
    string ten = Nam;
    cout << ten;
    return 0;
}
```

Gợi ý:

```text
Chuỗi chữ Nam phải đặt trong dấu ngoặc kép.
```

Sửa đúng:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "Nam";
    cout << ten;
    return 0;
}
```

---

## Bài 4

Tìm lỗi sai trong chương trình sau và sửa lại:

```cpp
#include <iostream>
using namespace std;

int main() {
    int diem toan = 10;
    cout << diem toan;
    return 0;
}
```

Gợi ý:

```text
Tên biến không được có khoảng trắng.
```

Sửa đúng:

```cpp
#include <iostream>
using namespace std;

int main() {
    int diemToan = 10;
    cout << diemToan;
    return 0;
}
```

---

## Bài 5

Viết chương trình in ra bảng thông tin cá nhân của em, có sử dụng ít nhất 4 biến.

Ví dụ:

```text
===== THONG TIN CA NHAN =====
Ten: An
Tuoi: 11
Lop: 6A
So thich: Ve tranh
=============================
```

---

# 25. Tóm tắt bài học

Học sinh cần nhớ:

```text
Biến dùng để lưu dữ liệu trong chương trình.

Cách khai báo biến:
kieu_du_lieu ten_bien = gia_tri;

Một số kiểu dữ liệu:
int    → số nguyên
float  → số thập phân
double → số thập phân chính xác hơn
char   → một ký tự
string → chuỗi chữ
bool   → đúng hoặc sai

Muốn in giá trị biến:
cout << ten_bien;
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten = "Nam";
    int tuoi = 11;

    cout << "Ten: " << ten << endl;
    cout << "Tuoi: " << tuoi;

    return 0;
}
```

---

# 26. Gợi ý thời lượng dạy

| Phần                         | Thời lượng |
| ---------------------------- | ---------: |
| Ôn bài cũ                    |     5 phút |
| Giới thiệu biến              |    10 phút |
| Kiểu dữ liệu cơ bản          |    15 phút |
| In biến bằng `cout`          |    10 phút |
| Quy tắc đặt tên biến         |     8 phút |
| Thực hành thông tin học sinh |    15 phút |
| Củng cố và giao bài tập      |     5 phút |

Tổng thời lượng: khoảng **65–70 phút**.
