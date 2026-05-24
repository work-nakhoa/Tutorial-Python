# Bài 8: Câu lệnh điều kiện `if`

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu điều kiện trong lập trình là gì.
* Biết câu lệnh `if` dùng để làm gì.
* Biết dùng các toán tử so sánh:

  * `>`
  * `<`
  * `>=`
  * `<=`
  * `==`
  * `!=`
* Biết viết chương trình kiểm tra một điều kiện đơn giản.
* Biết kết hợp `cin`, `cout`, biến, phép toán và `if`.
* Viết được chương trình kiểm tra điểm đạt, kiểm tra tuổi, kiểm tra số dương.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Khi giải bài toán lập trình, ta thường phân tích thành mấy phần?
2. Ba phần đó là gì?
3. Đổi km sang m dùng công thức gì?
4. Đổi phút sang giây dùng công thức gì?
5. Phép `%` dùng để làm gì?

Gợi ý trả lời:

```text
1. Ba phần.
2. Đầu vào, xử lý, đầu ra.
3. mét = km * 1000.
4. giây = phút * 60.
5. Phép % dùng để lấy số dư.
```

Giáo viên dẫn vào bài mới:

> Ở các bài trước, chương trình của chúng ta thường chạy từ trên xuống dưới và lệnh nào cũng được thực hiện.
> Hôm nay, chúng ta học cách để máy tính **chỉ thực hiện một lệnh khi điều kiện đúng**.
> Đó là câu lệnh `if`.

---

# 3. Điều kiện là gì?

## Giải thích đơn giản

**Điều kiện** là một câu hỏi có kết quả **đúng** hoặc **sai**.

Ví dụ trong đời sống:

```text
Nếu trời mưa thì mang áo mưa.
Nếu điểm từ 5 trở lên thì đạt.
Nếu em đủ 11 tuổi thì học lớp 6.
Nếu số chia hết cho 2 thì là số chẵn.
```

Mỗi câu đều có dạng:

```text
Nếu điều kiện đúng thì làm việc gì đó.
```

Ví dụ:

```text
Nếu trời mưa → mang áo mưa.
Nếu không mưa → không cần mang áo mưa.
```

Trong lập trình, ta dùng câu lệnh `if` để diễn tả kiểu suy nghĩ này.

---

# 4. Câu lệnh `if` là gì?

`if` là câu lệnh dùng để kiểm tra điều kiện.

Nếu điều kiện đúng, chương trình sẽ thực hiện lệnh bên trong `if`.

Nếu điều kiện sai, chương trình sẽ bỏ qua phần bên trong `if`.

Cấu trúc:

```cpp
if (dieu_kien) {
    // Lệnh sẽ chạy nếu điều kiện đúng
}
```

Ví dụ:

```cpp
if (tuoi >= 11) {
    cout << "Em co the hoc lop 6";
}
```

Nghĩa là:

```text
Nếu tuổi lớn hơn hoặc bằng 11
thì in ra: Em co the hoc lop 6
```

---

# 5. Ví dụ đầu tiên với `if`

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    if (tuoi >= 11) {
        cout << "Em co the hoc lop 6";
    }

    return 0;
}
```

Ví dụ chạy chương trình 1:

```text
Nhap tuoi: 12
Em co the hoc lop 6
```

Ví dụ chạy chương trình 2:

```text
Nhap tuoi: 10
```

Khi nhập `10`, chương trình không in gì thêm, vì điều kiện:

```cpp
tuoi >= 11
```

là sai.

Giáo viên giải thích:

> Câu lệnh trong `{ }` chỉ chạy khi điều kiện trong dấu `( )` đúng.

---

# 6. Toán tử so sánh

Để viết điều kiện, ta dùng các toán tử so sánh.

| Toán tử | Ý nghĩa           | Ví dụ    | Nghĩa là              |
| ------- | ----------------- | -------- | --------------------- |
| `>`     | Lớn hơn           | `a > b`  | a lớn hơn b           |
| `<`     | Nhỏ hơn           | `a < b`  | a nhỏ hơn b           |
| `>=`    | Lớn hơn hoặc bằng | `a >= b` | a lớn hơn hoặc bằng b |
| `<=`    | Nhỏ hơn hoặc bằng | `a <= b` | a nhỏ hơn hoặc bằng b |
| `==`    | Bằng nhau         | `a == b` | a bằng b              |
| `!=`    | Khác nhau         | `a != b` | a khác b              |

Giáo viên nhấn mạnh:

> Trong C++, kiểm tra bằng nhau dùng `==`, không phải `=`.

---

# 7. Phân biệt `=` và `==`

Đây là lỗi rất thường gặp.

## Dấu `=`

Dùng để **gán giá trị**.

Ví dụ:

```cpp
int tuoi = 11;
```

Nghĩa là:

```text
Gán giá trị 11 cho biến tuoi.
```

## Dấu `==`

Dùng để **so sánh bằng nhau**.

Ví dụ:

```cpp
if (tuoi == 11) {
    cout << "Em 11 tuoi";
}
```

Nghĩa là:

```text
Nếu tuổi bằng 11 thì in ra: Em 11 tuoi.
```

So sánh:

| Cách viết    | Ý nghĩa                          |
| ------------ | -------------------------------- |
| `tuoi = 11`  | Gán 11 vào biến `tuoi`           |
| `tuoi == 11` | Kiểm tra `tuoi` có bằng 11 không |

Giáo viên nên nhắc nhiều lần:

```text
Một dấu bằng = là gán.
Hai dấu bằng == là so sánh.
```

---

# 8. Ví dụ: Kiểm tra điểm đạt

Đề bài:

```text
Nhập điểm. Nếu điểm từ 5 trở lên thì in ra "Dat".
```

Phân tích:

```text
Đầu vào:
- diem

Xử lý:
- Nếu diem >= 5 thì in "Dat"

Đầu ra:
- Thông báo Dat nếu điều kiện đúng
```

Chương trình:

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

Ví dụ 1:

```text
Nhap diem: 8
Dat
```

Ví dụ 2:

```text
Nhap diem: 4
```

Vì `4 >= 5` là sai, nên chương trình không in chữ `Dat`.

---

# 9. Ví dụ: Kiểm tra số dương

Đề bài:

```text
Nhập một số nguyên. Nếu số đó lớn hơn 0 thì in ra "So duong".
```

Phân tích:

```text
Đầu vào:
- n

Xử lý:
- Nếu n > 0 thì in "So duong"

Đầu ra:
- Thông báo So duong nếu điều kiện đúng
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n > 0) {
        cout << "So duong";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap n: 7
So duong
```

Nếu nhập:

```text
Nhap n: -3
```

Chương trình không in thêm gì, vì `-3 > 0` là sai.

---

# 10. Ví dụ: Kiểm tra số bằng 0

Đề bài:

```text
Nhập một số nguyên. Nếu số đó bằng 0 thì in ra "So bang 0".
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n == 0) {
        cout << "So bang 0";
    }

    return 0;
}
```

Lưu ý quan trọng:

Đúng:

```cpp
if (n == 0)
```

Sai:

```cpp
if (n = 0)
```

Vì `=` là gán, không phải so sánh.

---

# 11. Ví dụ: Kiểm tra hai số bằng nhau

Đề bài:

```text
Nhập hai số nguyên a và b. Nếu hai số bằng nhau thì in ra "Hai so bang nhau".
```

Phân tích:

```text
Đầu vào:
- a
- b

Xử lý:
- Nếu a == b thì in "Hai so bang nhau"

Đầu ra:
- Thông báo nếu hai số bằng nhau
```

Chương trình:

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
        cout << "Hai so bang nhau";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap a: 5
Nhap b: 5
Hai so bang nhau
```

Nếu nhập `a = 5`, `b = 3`, chương trình không in gì thêm.

---

# 12. Ví dụ: Kiểm tra hai số khác nhau

Đề bài:

```text
Nhập hai số nguyên a và b. Nếu hai số khác nhau thì in ra "Hai so khac nhau".
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    if (a != b) {
        cout << "Hai so khac nhau";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap a: 5
Nhap b: 3
Hai so khac nhau
```

Giải thích:

```cpp
a != b
```

nghĩa là `a` khác `b`.

---

# 13. Ví dụ: Kiểm tra số chẵn bằng `%`

Đề bài:

```text
Nhập một số nguyên. Nếu số đó chia hết cho 2 thì in ra "So chan".
```

Nhắc lại:

```text
Một số chia hết cho 2 nếu số dư khi chia cho 2 bằng 0.
```

Tức là:

```cpp
n % 2 == 0
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n % 2 == 0) {
        cout << "So chan";
    }

    return 0;
}
```

Ví dụ 1:

```text
Nhap n: 8
So chan
```

Ví dụ 2:

```text
Nhap n: 7
```

Vì `7 % 2 == 0` là sai, chương trình không in chữ `So chan`.

Giáo viên nhấn mạnh:

> Đây là một ứng dụng rất quan trọng của phép `%`.

---

# 14. Câu lệnh trong `{ }`

Trong `if`, các lệnh nằm giữa `{` và `}` sẽ chạy nếu điều kiện đúng.

Ví dụ:

```cpp
if (diem >= 5) {
    cout << "Chuc mung!" << endl;
    cout << "Em da dat.";
}
```

Nếu `diem >= 5` đúng, cả hai dòng `cout` đều được chạy.

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

---

# 15. Nếu không có `{ }` thì sao?

Trong C++, nếu không có `{ }`, chỉ có **một lệnh ngay sau `if`** thuộc về `if`.

Ví dụ:

```cpp
if (diem >= 5)
    cout << "Chuc mung!" << endl;
    cout << "Em da dat.";
```

Dòng:

```cpp
cout << "Em da dat.";
```

sẽ luôn chạy, dù điểm có đạt hay không.

Vì vậy, với học sinh mới học, nên luôn viết `{ }`.

Nên viết:

```cpp
if (diem >= 5) {
    cout << "Chuc mung!" << endl;
    cout << "Em da dat.";
}
```

Quy tắc:

```text
Mới học thì luôn dùng { } cho câu lệnh if.
```

---

# 16. Quy trình viết bài có `if`

Khi gặp bài toán điều kiện, học sinh làm theo các bước:

```text
Bước 1: Đọc đề.
Bước 2: Xác định đầu vào.
Bước 3: Xác định điều kiện.
Bước 4: Viết câu lệnh if.
Bước 5: Viết lệnh cần chạy khi điều kiện đúng.
Bước 6: Chạy thử với dữ liệu đúng và dữ liệu sai.
```

Ví dụ:

```text
Đề bài: Nhập điểm, nếu điểm >= 5 thì in "Dat".
```

Phân tích:

```text
Đầu vào:
- diem

Điều kiện:
- diem >= 5

Nếu đúng:
- in "Dat"
```

Code:

```cpp
if (diem >= 5) {
    cout << "Dat";
}
```

---

# 17. Hoạt động thực hành 1: Kiểm tra tuổi

Đề bài:

```text
Nhập tuổi. Nếu tuổi lớn hơn hoặc bằng 11 thì in ra "Du tuoi hoc lop 6".
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    if (tuoi >= 11) {
        cout << "Du tuoi hoc lop 6";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap tuoi: 12
Du tuoi hoc lop 6
```

---

# 18. Hoạt động thực hành 2: Kiểm tra điểm

Đề bài:

```text
Nhập điểm. Nếu điểm lớn hơn hoặc bằng 5 thì in ra "Dat".
```

Code gợi ý:

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

---

# 19. Hoạt động thực hành 3: Kiểm tra số lớn hơn 100

Đề bài:

```text
Nhập một số nguyên. Nếu số đó lớn hơn 100 thì in ra "Lon hon 100".
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
    }

    return 0;
}
```

---

# 20. Hoạt động thực hành 4: Kiểm tra số chẵn

Đề bài:

```text
Nhập một số nguyên. Nếu số đó là số chẵn thì in ra "So chan".
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n % 2 == 0) {
        cout << "So chan";
    }

    return 0;
}
```

---

# 21. Hoạt động thực hành 5: Kiểm tra mật mã đơn giản

Đề bài:

```text
Nhập một số mật mã. Nếu mật mã bằng 1234 thì in ra "Dung mat ma".
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int matMa;

    cout << "Nhap mat ma: ";
    cin >> matMa;

    if (matMa == 1234) {
        cout << "Dung mat ma";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap mat ma: 1234
Dung mat ma
```

Nếu nhập số khác, chương trình không in gì thêm.

---

# 22. Lỗi thường gặp khi dùng `if`

## Lỗi 1: Dùng `=` thay vì `==`

Sai:

```cpp
if (n = 0) {
    cout << "So bang 0";
}
```

Đúng:

```cpp
if (n == 0) {
    cout << "So bang 0";
}
```

Giải thích:

```text
= là gán
== là so sánh bằng nhau
```

---

## Lỗi 2: Quên dấu ngoặc tròn `( )`

Sai:

```cpp
if n > 0 {
    cout << "So duong";
}
```

Đúng:

```cpp
if (n > 0) {
    cout << "So duong";
}
```

---

## Lỗi 3: Quên dấu ngoặc nhọn `{ }`

Không nên viết:

```cpp
if (diem >= 5)
    cout << "Dat";
```

Nên viết:

```cpp
if (diem >= 5) {
    cout << "Dat";
}
```

Lý do:

> Dùng `{ }` giúp code rõ ràng và tránh lỗi khi có nhiều lệnh.

---

## Lỗi 4: Viết điều kiện sai dấu

Ví dụ đề yêu cầu:

```text
Nếu điểm từ 5 trở lên thì đạt.
```

Sai:

```cpp
if (diem > 5) {
    cout << "Dat";
}
```

Vì điểm `5` cũng phải đạt.

Đúng:

```cpp
if (diem >= 5) {
    cout << "Dat";
}
```

---

## Lỗi 5: Quên dấu `;` sau lệnh bên trong `if`

Sai:

```cpp
if (n > 0) {
    cout << "So duong"
}
```

Đúng:

```cpp
if (n > 0) {
    cout << "So duong";
}
```

---

# 23. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

Câu lệnh `if` dùng để làm gì?

A. Nhập dữ liệu
B. In dữ liệu
C. Kiểm tra điều kiện
D. Kết thúc chương trình

Đáp án: **C**

---

## Bài 2: Chọn đáp án đúng

Toán tử nào dùng để kiểm tra hai giá trị bằng nhau?

A. `=`
B. `==`
C. `!=`
D. `>=`

Đáp án: **B**

---

## Bài 3: Điền từ còn thiếu

```text
Trong C++, dấu = dùng để ______ giá trị.
```

Đáp án:

```text
gán
```

---

## Bài 4: Điền từ còn thiếu

```text
Trong C++, dấu == dùng để ______ bằng nhau.
```

Đáp án:

```text
so sánh
```

---

## Bài 5: Đoán kết quả

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 10;

    if (n > 5) {
        cout << "Lon hon 5";
    }

    return 0;
}
```

Kết quả:

```text
Lon hon 5
```

---

## Bài 6: Đoán kết quả

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n = 3;

    if (n > 5) {
        cout << "Lon hon 5";
    }

    return 0;
}
```

Kết quả:

```text
Chương trình không in gì thêm.
```

Vì `3 > 5` là sai.

---

## Bài 7: Tìm lỗi sai

Chương trình sau sai ở đâu?

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n = 0) {
        cout << "So bang 0";
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
if (n == 0) {
    cout << "So bang 0";
}
```

---

## Bài 8: Tìm lỗi sai

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    if tuoi >= 11 {
        cout << "Du tuoi";
    }

    return 0;
}
```

Lỗi:

```text
Thiếu dấu ngoặc tròn quanh điều kiện.
```

Sửa đúng:

```cpp
if (tuoi >= 11) {
    cout << "Du tuoi";
}
```

---

# 24. Bài tập thực hành

## Bài 1

Viết chương trình nhập tuổi. Nếu tuổi lớn hơn hoặc bằng 11 thì in ra:

```text
Du tuoi hoc lop 6
```

---

## Bài 2

Viết chương trình nhập điểm. Nếu điểm lớn hơn hoặc bằng 5 thì in ra:

```text
Dat
```

---

## Bài 3

Viết chương trình nhập một số nguyên `n`. Nếu `n > 0` thì in ra:

```text
So duong
```

---

## Bài 4

Viết chương trình nhập một số nguyên `n`. Nếu `n == 0` thì in ra:

```text
So bang 0
```

---

## Bài 5

Viết chương trình nhập hai số nguyên `a`, `b`. Nếu hai số bằng nhau thì in ra:

```text
Hai so bang nhau
```

---

## Bài 6

Viết chương trình nhập hai số nguyên `a`, `b`. Nếu hai số khác nhau thì in ra:

```text
Hai so khac nhau
```

---

## Bài 7

Viết chương trình nhập một số nguyên `n`. Nếu `n` chia hết cho 2 thì in ra:

```text
So chan
```

Gợi ý:

```cpp
if (n % 2 == 0) {
    cout << "So chan";
}
```

---

# 25. Bài tập nâng cao nhẹ

## Bài 1: Kiểm tra đủ tiền mua đồ

Đề bài:

```text
Nhập giá món đồ và số tiền em có.
Nếu số tiền em có lớn hơn hoặc bằng giá món đồ thì in ra "Du tien mua".
```

Phân tích:

```text
Đầu vào:
- giaTien
- tienCo

Điều kiện:
- tienCo >= giaTien

Đầu ra:
- Du tien mua nếu điều kiện đúng
```

Code gợi ý:

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
    }

    return 0;
}
```

---

## Bài 2: Kiểm tra chia hết cho 5

Đề bài:

```text
Nhập một số nguyên n.
Nếu n chia hết cho 5 thì in ra "Chia het cho 5".
```

Gợi ý:

```cpp
if (n % 5 == 0) {
    cout << "Chia het cho 5";
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
    }

    return 0;
}
```

---

## Bài 3: Kiểm tra điểm tuyệt đối

Đề bài:

```text
Nhập điểm. Nếu điểm bằng 10 thì in ra "Diem tuyet doi".
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    float diem;

    cout << "Nhap diem: ";
    cin >> diem;

    if (diem == 10) {
        cout << "Diem tuyet doi";
    }

    return 0;
}
```

---

# 26. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. `if` dùng để làm gì?
2. Điều kiện trong `if` nằm trong dấu gì?
3. Các lệnh cần chạy khi điều kiện đúng nằm trong dấu gì?
4. Dấu `=` dùng để làm gì?
5. Dấu `==` dùng để làm gì?
6. Muốn kiểm tra `n` lớn hơn 0, viết điều kiện thế nào?
7. Muốn kiểm tra `n` bằng 0, viết điều kiện thế nào?
8. Muốn kiểm tra `n` chia hết cho 2, viết điều kiện thế nào?

Gợi ý trả lời:

```text
1. if dùng để kiểm tra điều kiện.
2. Điều kiện nằm trong dấu ngoặc tròn ( ).
3. Các lệnh nằm trong dấu ngoặc nhọn { }.
4. Dấu = dùng để gán giá trị.
5. Dấu == dùng để so sánh bằng nhau.
6. n > 0
7. n == 0
8. n % 2 == 0
```

---

# 27. Bài tập về nhà

## Bài 1

Viết chương trình nhập tuổi. Nếu tuổi lớn hơn hoặc bằng 6 thì in ra:

```text
Du tuoi vao lop 1
```

---

## Bài 2

Viết chương trình nhập điểm Tin học. Nếu điểm lớn hơn hoặc bằng 8 thì in ra:

```text
Hoc tot mon Tin
```

---

## Bài 3

Viết chương trình nhập một số nguyên. Nếu số đó nhỏ hơn 0 thì in ra:

```text
So am
```

---

## Bài 4

Viết chương trình nhập một số nguyên. Nếu số đó chia hết cho 10 thì in ra:

```text
Chia het cho 10
```

Gợi ý:

```cpp
n % 10 == 0
```

---

## Bài 5

Viết chương trình nhập mật mã. Nếu mật mã bằng `2026` thì in ra:

```text
Mo khoa thanh cong
```

---

# 28. Tóm tắt bài học

Học sinh cần nhớ:

```text
Câu lệnh if dùng để kiểm tra điều kiện.

Cấu trúc:

if (dieu_kien) {
    // lệnh chạy khi điều kiện đúng
}

Các toán tử so sánh:

>   lớn hơn
<   nhỏ hơn
>=  lớn hơn hoặc bằng
<=  nhỏ hơn hoặc bằng
==  bằng nhau
!=  khác nhau

=  dùng để gán giá trị
== dùng để so sánh bằng nhau
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    if (n > 0) {
        cout << "So duong";
    }

    return 0;
}
```

---

# 29. Gợi ý thời lượng dạy

| Phần                                | Thời lượng |
| ----------------------------------- | ---------: |
| Ôn bài cũ                           |     5 phút |
| Giới thiệu điều kiện và `if`        |    10 phút |
| Toán tử so sánh                     |    15 phút |
| Phân biệt `=` và `==`               |    10 phút |
| Ví dụ kiểm tra điểm, tuổi, số dương |    15 phút |
| Thực hành số chẵn với `%`           |    10 phút |
| Sửa lỗi thường gặp                  |    10 phút |
| Củng cố và giao bài tập             |     5 phút |

Tổng thời lượng: khoảng **80 phút**.
