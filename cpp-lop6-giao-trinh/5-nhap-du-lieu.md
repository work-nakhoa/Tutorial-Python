# Bài 5: Nhập dữ liệu với `cin`

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu `cin` dùng để nhập dữ liệu từ bàn phím.
* Biết nhập số nguyên, số thập phân, chuỗi đơn giản.
* Biết kết hợp `cout` và `cin`.
* Biết lưu dữ liệu người dùng nhập vào biến.
* Viết được chương trình nhập tên, tuổi, điểm và in ra màn hình.
* Viết được chương trình nhập 2 số và tính tổng đơn giản.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Biến dùng để làm gì?
2. Kiểu `int` dùng để lưu dữ liệu gì?
3. Kiểu `float` dùng để lưu dữ liệu gì?
4. Kiểu `string` dùng để lưu dữ liệu gì?
5. Muốn in giá trị biến `tuoi`, ta viết thế nào?

Gợi ý trả lời:

```text
1. Biến dùng để lưu dữ liệu.
2. int dùng để lưu số nguyên.
3. float dùng để lưu số thập phân.
4. string dùng để lưu chuỗi chữ.
5. cout << tuoi;
```

Giáo viên dẫn vào bài mới:

> Ở bài trước, chúng ta đã biết tạo biến và gán giá trị sẵn trong chương trình.
> Ví dụ: `int tuoi = 11;`
> Nhưng nếu muốn người dùng tự nhập tuổi từ bàn phím thì sao?
> Hôm nay, chúng ta sẽ học lệnh `cin`.

---

# 3. `cin` là gì?

Trong C++, `cin` dùng để **nhập dữ liệu từ bàn phím**.

Ví dụ:

```cpp
int tuoi;
cin >> tuoi;
```

Nghĩa là:

```text
Máy tính chờ người dùng nhập tuổi từ bàn phím.
Sau đó lưu giá trị vừa nhập vào biến tuoi.
```

So sánh đơn giản:

| Lệnh   | Công dụng                |
| ------ | ------------------------ |
| `cout` | In dữ liệu ra màn hình   |
| `cin`  | Nhập dữ liệu từ bàn phím |

Giáo viên có thể nói:

> `cout` là máy tính nói với mình.
> `cin` là mình nhập dữ liệu cho máy tính.

---

# 4. Cấu trúc cơ bản của `cin`

Cấu trúc:

```cpp
cin >> ten_bien;
```

Ví dụ:

```cpp
int tuoi;
cin >> tuoi;
```

Trong đó:

| Thành phần | Ý nghĩa                           |
| ---------- | --------------------------------- |
| `cin`      | Lệnh nhập dữ liệu                 |
| `>>`       | Đưa dữ liệu từ bàn phím vào biến  |
| `ten_bien` | Biến dùng để lưu dữ liệu nhập vào |
| `;`        | Kết thúc câu lệnh                 |

Lưu ý quan trọng:

```cpp
cout << "Nhap tuoi: ";
cin >> tuoi;
```

Dòng `cout` dùng để nhắc người dùng cần nhập gì.

Nếu chỉ viết:

```cpp
cin >> tuoi;
```

Thì chương trình vẫn chạy, nhưng học sinh có thể không biết phải nhập gì.

---

# 5. Chương trình nhập tuổi

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi cua em: ";
    cin >> tuoi;

    cout << "Tuoi cua em la: " << tuoi;

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap tuoi cua em: 11
Tuoi cua em la: 11
```

Giải thích từng bước:

```text
1. Tạo biến tuoi để lưu tuổi.
2. In ra dòng nhắc: Nhap tuoi cua em:
3. Người dùng nhập số tuổi.
4. Chương trình lưu số đó vào biến tuoi.
5. In tuổi ra màn hình.
```

---

# 6. Nhập số nguyên với `int`

Kiểu `int` dùng để nhập số nguyên.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int so;

    cout << "Nhap mot so nguyen: ";
    cin >> so;

    cout << "So vua nhap la: " << so;

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap mot so nguyen: 25
So vua nhap la: 25
```

Bài tập nhỏ:

Viết chương trình nhập năm sinh rồi in ra năm sinh.

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int namSinh;

    cout << "Nhap nam sinh: ";
    cin >> namSinh;

    cout << "Nam sinh cua em la: " << namSinh;

    return 0;
}
```

---

# 7. Nhập số thập phân với `float`

Kiểu `float` dùng để nhập số thập phân.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    float diemToan;

    cout << "Nhap diem Toan: ";
    cin >> diemToan;

    cout << "Diem Toan cua em la: " << diemToan;

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap diem Toan: 8.5
Diem Toan cua em la: 8.5
```

Giáo viên nhắc học sinh:

> Điểm số như `8.5`, `9.25`, `7.75` là số thập phân, nên dùng `float` hoặc `double`.

---

# 8. Nhập chuỗi đơn giản với `string`

Kiểu `string` dùng để nhập chữ.

Ví dụ:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten;

    cout << "Nhap ten cua em: ";
    cin >> ten;

    cout << "Xin chao " << ten;

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap ten cua em: Nam
Xin chao Nam
```

Lưu ý quan trọng:

Với `cin >> ten;`, chương trình chỉ nhập được **một từ**.

Ví dụ nếu nhập:

```text
Nguyen Van Nam
```

Thì biến `ten` chỉ nhận:

```text
Nguyen
```

Với học sinh lớp 6, bài này chỉ cần nhập tên một từ như:

```text
Nam
Lan
An
Minh
```

Nhập họ tên đầy đủ có dấu cách sẽ học sau bằng `getline`.

---

# 9. Kết hợp `cout` và `cin`

Thông thường, khi nhập dữ liệu, ta nên dùng `cout` để hỏi trước.

Ví dụ không nên viết:

```cpp
int tuoi;
cin >> tuoi;
```

Vì người dùng không biết cần nhập gì.

Nên viết:

```cpp
int tuoi;

cout << "Nhap tuoi: ";
cin >> tuoi;
```

Kết luận:

```text
cout dùng để hỏi hoặc thông báo.
cin dùng để nhận dữ liệu người dùng nhập.
```

---

# 10. Nhập nhiều dữ liệu

Ta có thể nhập nhiều biến.

Ví dụ nhập tên và tuổi:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten;
    int tuoi;

    cout << "Nhap ten: ";
    cin >> ten;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    cout << "Xin chao " << ten << endl;
    cout << "Nam nay em " << tuoi << " tuoi";

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap ten: An
Nhap tuoi: 11
Xin chao An
Nam nay em 11 tuoi
```

---

# 11. Nhập hai số và tính tổng

Đây là bài toán rất quan trọng.

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap so thu nhat: ";
    cin >> a;

    cout << "Nhap so thu hai: ";
    cin >> b;

    cout << "Tong hai so la: " << a + b;

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap so thu nhat: 5
Nhap so thu hai: 7
Tong hai so la: 12
```

Giải thích:

```text
1. Tạo hai biến a và b.
2. Nhập giá trị cho a.
3. Nhập giá trị cho b.
4. Tính a + b.
5. In kết quả ra màn hình.
```

Giáo viên nhấn mạnh:

> `a + b` là phép tính giữa hai biến.
> Máy tính sẽ lấy giá trị đang lưu trong `a` và `b` để cộng lại.

---

# 12. Nhập ba điểm và tính điểm trung bình

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    float toan, van, anh;
    float trungBinh;

    cout << "Nhap diem Toan: ";
    cin >> toan;

    cout << "Nhap diem Van: ";
    cin >> van;

    cout << "Nhap diem Anh: ";
    cin >> anh;

    trungBinh = (toan + van + anh) / 3;

    cout << "Diem trung binh la: " << trungBinh;

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap diem Toan: 8
Nhap diem Van: 7
Nhap diem Anh: 9
Diem trung binh la: 8
```

Giải thích:

```text
Diem trung binh = (Toan + Van + Anh) / 3
```

Lưu ý:

Nên có dấu ngoặc:

```cpp
(toan + van + anh) / 3
```

Nếu không có dấu ngoặc:

```cpp
toan + van + anh / 3
```

Thì máy sẽ chia `anh / 3` trước, kết quả có thể sai.

---

# 13. Nhập nhiều biến trên một dòng

Có thể nhập nhiều biến bằng một câu lệnh:

```cpp
cin >> a >> b;
```

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap hai so: ";
    cin >> a >> b;

    cout << "Tong la: " << a + b;

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap hai so: 3 4
Tong la: 7
```

Người dùng có thể nhập:

```text
3 4
```

Hoặc nhập từng dòng:

```text
3
4
```

Cả hai cách đều được.

Tuy nhiên, với học sinh mới học, nên nhập từng biến riêng để dễ hiểu:

```cpp
cout << "Nhap a: ";
cin >> a;

cout << "Nhap b: ";
cin >> b;
```

---

# 14. So sánh `cout <<` và `cin >>`

Học sinh thường nhầm hai dấu này.

| Lệnh   | Dấu dùng | Ý nghĩa                          |
| ------ | -------- | -------------------------------- |
| `cout` | `<<`     | Đưa dữ liệu ra màn hình          |
| `cin`  | `>>`     | Đưa dữ liệu từ bàn phím vào biến |

Mẹo nhớ:

```text
cout <<  dữ liệu đi ra màn hình
cin  >>  dữ liệu đi vào biến
```

Ví dụ:

```cpp
cout << "Nhap tuoi: ";
cin >> tuoi;
```

---

# 15. Chương trình hoàn chỉnh: Thông tin học sinh

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten;
    string lop;
    int tuoi;
    float diemTin;

    cout << "Nhap ten: ";
    cin >> ten;

    cout << "Nhap lop: ";
    cin >> lop;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    cout << "Nhap diem Tin hoc: ";
    cin >> diemTin;

    cout << endl;
    cout << "===== THONG TIN HOC SINH =====" << endl;
    cout << "Ten: " << ten << endl;
    cout << "Lop: " << lop << endl;
    cout << "Tuoi: " << tuoi << endl;
    cout << "Diem Tin hoc: " << diemTin << endl;
    cout << "==============================";

    return 0;
}
```

Ví dụ khi chạy:

```text
Nhap ten: Nam
Nhap lop: 6A
Nhap tuoi: 11
Nhap diem Tin hoc: 9.5

===== THONG TIN HOC SINH =====
Ten: Nam
Lop: 6A
Tuoi: 11
Diem Tin hoc: 9.5
==============================
```

---

# 16. Quy trình làm bài nhập dữ liệu

Khi gặp bài có nhập dữ liệu, học sinh nên làm theo 4 bước:

```text
Bước 1: Xác định cần nhập gì.
Bước 2: Tạo biến phù hợp.
Bước 3: Dùng cout để hỏi.
Bước 4: Dùng cin để nhập.
Bước 5: Xử lý và in kết quả.
```

Ví dụ bài toán:

```text
Nhập hai số, in ra tổng.
```

Phân tích:

```text
Cần nhập: a, b
Kiểu dữ liệu: int
Xử lý: a + b
Kết quả: tổng hai số
```

Code:

```cpp
int a, b;
cout << "Nhap a: ";
cin >> a;
cout << "Nhap b: ";
cin >> b;
cout << "Tong la: " << a + b;
```

---

# 17. Hoạt động thực hành 1: Nhập tên

Yêu cầu học sinh viết chương trình nhập tên rồi in lời chào.

Kết quả mẫu:

```text
Nhap ten: Lan
Xin chao Lan
```

Gợi ý:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten;

    cout << "Nhap ten: ";
    cin >> ten;

    cout << "Xin chao " << ten;

    return 0;
}
```

---

# 18. Hoạt động thực hành 2: Nhập tuổi

Yêu cầu học sinh viết chương trình nhập tuổi rồi in ra:

```text
Nam nay em ... tuoi
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    cout << "Nam nay em " << tuoi << " tuoi";

    return 0;
}
```

---

# 19. Hoạt động thực hành 3: Nhập hai số

Yêu cầu học sinh nhập hai số nguyên rồi in ra:

```text
Tong la: ...
```

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

# 20. Hoạt động thực hành 4: Nhập điểm

Yêu cầu học sinh nhập điểm Toán, Văn, Anh rồi tính điểm trung bình.

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    float toan, van, anh;
    float trungBinh;

    cout << "Nhap diem Toan: ";
    cin >> toan;

    cout << "Nhap diem Van: ";
    cin >> van;

    cout << "Nhap diem Anh: ";
    cin >> anh;

    trungBinh = (toan + van + anh) / 3;

    cout << "Diem trung binh la: " << trungBinh;

    return 0;
}
```

---

# 21. Lỗi thường gặp khi dùng `cin`

## Lỗi 1: Dùng sai dấu với `cin`

Sai:

```cpp
cin << tuoi;
```

Đúng:

```cpp
cin >> tuoi;
```

Giải thích:

> `cin` phải dùng dấu `>>`.

---

## Lỗi 2: Dùng sai dấu với `cout`

Sai:

```cpp
cout >> "Nhap tuoi: ";
```

Đúng:

```cpp
cout << "Nhap tuoi: ";
```

Giải thích:

> `cout` phải dùng dấu `<<`.

---

## Lỗi 3: Chưa khai báo biến

Sai:

```cpp
cout << "Nhap tuoi: ";
cin >> tuoi;
```

Đúng:

```cpp
int tuoi;

cout << "Nhap tuoi: ";
cin >> tuoi;
```

Giải thích:

> Muốn nhập dữ liệu vào biến, phải tạo biến trước.

---

## Lỗi 4: Nhập sai kiểu dữ liệu

Ví dụ chương trình yêu cầu:

```cpp
int tuoi;
cin >> tuoi;
```

Nhưng người dùng nhập:

```text
muoi mot
```

Chương trình có thể bị lỗi hoặc không chạy đúng.

Đúng là nên nhập:

```text
11
```

Giáo viên nhắc học sinh:

> Biến kiểu `int` thì nhập số nguyên.
> Biến kiểu `float` thì nhập số thập phân.
> Biến kiểu `string` thì nhập chữ.

---

## Lỗi 5: Nhập họ tên có dấu cách bằng `cin`

Ví dụ:

```cpp
string ten;
cin >> ten;
```

Nếu nhập:

```text
Nguyen Van Nam
```

Chương trình chỉ lấy:

```text
Nguyen
```

Ở bài này, chỉ cần nhập tên một từ.

Sau này có thể học:

```cpp
getline(cin, ten);
```

Nhưng chưa cần học sâu ở bài này.

---

# 22. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

Lệnh nào dùng để nhập dữ liệu từ bàn phím?

A. `cout`
B. `cin`
C. `main`
D. `return`

Đáp án: **B**

---

## Bài 2: Điền từ còn thiếu

```text
cin dùng để ______ dữ liệu từ bàn phím.
```

Đáp án:

```text
nhập
```

---

## Bài 3: Chọn câu lệnh đúng

Muốn nhập giá trị vào biến `tuoi`, ta viết:

A. `cin << tuoi;`
B. `cout >> tuoi;`
C. `cin >> tuoi;`
D. `cout << tuoi;`

Đáp án: **C**

---

## Bài 4: Đoán kết quả

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Gia tri cua a la: " << a;

    return 0;
}
```

Nếu người dùng nhập:

```text
9
```

Kết quả là:

```text
Nhap a: 9
Gia tri cua a la: 9
```

---

## Bài 5: Tìm lỗi sai

Chương trình sau sai ở đâu?

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout >> "Nhap tuoi: ";
    cin << tuoi;

    return 0;
}
```

Lỗi:

```text
cout dùng sai dấu.
cin dùng sai dấu.
```

Sửa đúng:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    return 0;
}
```

---

# 23. Bài tập thực hành

## Bài 1

Viết chương trình nhập tên, sau đó in ra:

```text
Xin chao ...
```

Ví dụ:

```text
Nhap ten: An
Xin chao An
```

---

## Bài 2

Viết chương trình nhập tuổi, sau đó in ra:

```text
Em ... tuoi
```

Ví dụ:

```text
Nhap tuoi: 11
Em 11 tuoi
```

---

## Bài 3

Viết chương trình nhập hai số nguyên `a`, `b`, sau đó in ra:

```text
Tong la: ...
```

Ví dụ:

```text
Nhap a: 4
Nhap b: 6
Tong la: 10
```

---

## Bài 4

Viết chương trình nhập hai số nguyên `a`, `b`, sau đó in ra:

```text
Hieu la: ...
```

Gợi ý:

```cpp
cout << "Hieu la: " << a - b;
```

---

## Bài 5

Viết chương trình nhập điểm Toán và điểm Văn, sau đó tính điểm trung bình.

Ví dụ:

```text
Nhap diem Toan: 8
Nhap diem Van: 9
Diem trung binh: 8.5
```

Gợi ý:

```cpp
trungBinh = (toan + van) / 2;
```

---

# 24. Bài tập nâng cao nhẹ

## Bài 1: Thông tin học sinh nhập từ bàn phím

Viết chương trình nhập:

```text
ten
lop
tuoi
diemTinHoc
```

Sau đó in ra bảng:

```text
===== THONG TIN HOC SINH =====
Ten: ...
Lop: ...
Tuoi: ...
Diem Tin hoc: ...
==============================
```

Gợi ý:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten, lop;
    int tuoi;
    float diemTinHoc;

    cout << "Nhap ten: ";
    cin >> ten;

    cout << "Nhap lop: ";
    cin >> lop;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    cout << "Nhap diem Tin hoc: ";
    cin >> diemTinHoc;

    cout << "===== THONG TIN HOC SINH =====" << endl;
    cout << "Ten: " << ten << endl;
    cout << "Lop: " << lop << endl;
    cout << "Tuoi: " << tuoi << endl;
    cout << "Diem Tin hoc: " << diemTinHoc << endl;
    cout << "==============================";

    return 0;
}
```

---

## Bài 2: Tính chu vi hình chữ nhật

Viết chương trình nhập chiều dài và chiều rộng, sau đó tính chu vi hình chữ nhật.

Công thức:

```text
Chu vi = (dai + rong) * 2
```

Gợi ý:

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

---

## Bài 3: Tính diện tích hình chữ nhật

Viết chương trình nhập chiều dài và chiều rộng, sau đó tính diện tích hình chữ nhật.

Công thức:

```text
Dien tich = dai * rong
```

Gợi ý:

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

---

# 25. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. `cin` dùng để làm gì?
2. `cout` dùng để làm gì?
3. `cin` dùng dấu `>>` hay `<<`?
4. `cout` dùng dấu `>>` hay `<<`?
5. Muốn nhập tuổi vào biến `tuoi`, viết câu lệnh gì?
6. Với `cin >> ten;`, nếu nhập `Nguyen Van Nam` thì biến `ten` nhận gì?
7. Muốn nhập điểm số 8.5 thì nên dùng kiểu dữ liệu nào?

Gợi ý trả lời:

```text
1. cin dùng để nhập dữ liệu từ bàn phím.
2. cout dùng để in ra màn hình.
3. cin dùng dấu >>.
4. cout dùng dấu <<.
5. cin >> tuoi;
6. Chỉ nhận Nguyen.
7. Dùng float hoặc double.
```

---

# 26. Bài tập về nhà

## Bài 1

Viết chương trình nhập tên của em rồi in ra:

```text
Xin chao ...
```

---

## Bài 2

Viết chương trình nhập tuổi và lớp, sau đó in ra:

```text
Em hoc lop ...
Nam nay em ... tuoi
```

---

## Bài 3

Viết chương trình nhập hai số nguyên `a`, `b`, sau đó in ra:

```text
Tong: ...
Hieu: ...
```

Gợi ý:

```cpp
cout << "Tong: " << a + b << endl;
cout << "Hieu: " << a - b;
```

---

## Bài 4

Viết chương trình nhập 3 điểm: Toán, Văn, Anh. Sau đó tính điểm trung bình.

---

## Bài 5

Tìm lỗi sai trong chương trình sau và sửa lại:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout >> "Nhap tuoi: ";
    cin << tuoi;

    cout << "Tuoi cua em la: " << tuoi;

    return 0;
}
```

Gợi ý sửa đúng:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    cout << "Tuoi cua em la: " << tuoi;

    return 0;
}
```

---

# 27. Tóm tắt bài học

Học sinh cần nhớ:

```text
cin dùng để nhập dữ liệu từ bàn phím.
cout dùng để in dữ liệu ra màn hình.

cout dùng dấu <<
cin dùng dấu >>

Muốn nhập dữ liệu:
1. Tạo biến
2. Dùng cout để hỏi
3. Dùng cin để nhập
4. In kết quả bằng cout
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    cout << "Tuoi cua em la: " << tuoi;

    return 0;
}
```

---

# 28. Gợi ý thời lượng dạy

| Phần                                | Thời lượng |
| ----------------------------------- | ---------: |
| Ôn bài cũ                           |     5 phút |
| Giới thiệu `cin`                    |    10 phút |
| Nhập số nguyên, số thập phân, chuỗi |    15 phút |
| Kết hợp `cout` và `cin`             |    10 phút |
| Nhập hai số và tính tổng            |    10 phút |
| Thực hành thông tin học sinh        |    15 phút |
| Củng cố và giao bài tập             |     5 phút |

Tổng thời lượng: khoảng **70 phút**.
