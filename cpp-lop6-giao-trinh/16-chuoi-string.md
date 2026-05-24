# Bài 16: Làm việc với chuỗi `string`

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu chuỗi ký tự là gì.
* Biết khai báo biến kiểu `string`.
* Biết nhập và in chuỗi đơn giản.
* Biết nối chuỗi.
* Biết lấy độ dài chuỗi bằng `.length()`.
* Biết so sánh chuỗi cơ bản.
* Viết được chương trình nhập tên, lớp, sở thích và in thông tin học sinh.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Hàm là gì?
2. `void` nghĩa là gì?
3. Hàm `main()` có vai trò gì?
4. Muốn gọi hàm `xinChao`, ta viết thế nào?
5. Lệnh `return` dùng để làm gì?

Gợi ý trả lời:

```text
1. Hàm là nhóm câu lệnh thực hiện một công việc cụ thể.
2. void nghĩa là hàm không trả về giá trị.
3. main() là nơi chương trình bắt đầu chạy.
4. xinChao();
5. return dùng để trả kết quả từ hàm.
```

Dẫn vào bài mới:

> Ở các bài trước, chúng ta đã dùng `string` để lưu tên, lớp, môn học.
> Hôm nay, chúng ta học kỹ hơn cách làm việc với chuỗi ký tự trong C++.

---

# 3. Chuỗi là gì?

**Chuỗi** là một dãy các ký tự ghép lại với nhau.

Ví dụ:

```text
"Nam"
"Lop 6A"
"Xin chao cac ban"
"Lap trinh C++"
```

Trong C++, ta dùng kiểu dữ liệu `string` để lưu chuỗi.

Ví dụ:

```cpp
string ten = "Nam";
string lop = "6A";
string cauChao = "Xin chao cac ban";
```

Giáo viên giải thích:

> Nếu `char` dùng để lưu một ký tự, thì `string` dùng để lưu nhiều ký tự.

So sánh:

```cpp
char chuCai = 'A';
string ten = "An";
```

| Kiểu dữ liệu | Dùng để lưu | Dấu dùng |
| ------------ | ----------- | -------- |
| `char`       | Một ký tự   | `' '`    |
| `string`     | Nhiều ký tự | `" "`    |

---

# 4. Khai báo biến kiểu `string`

Để dùng `string`, ta nên thêm thư viện:

```cpp
#include <string>
```

Mẫu chương trình:

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

Kết quả:

```text
Nam
```

---

# 5. In chuỗi ra màn hình

Ví dụ:

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

Giáo viên nhấn mạnh:

> Muốn in giá trị của biến chuỗi, không đặt tên biến trong dấu ngoặc kép.

Đúng:

```cpp
cout << ten;
```

Sai ý nghĩa:

```cpp
cout << "ten";
```

Vì dòng trên sẽ in ra chữ `ten`, không phải giá trị trong biến `ten`.

---

# 6. Nhập chuỗi bằng `cin`

Ví dụ:

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

Ví dụ chạy:

```text
Nhap ten: An
Xin chao An
```

Lưu ý:

> `cin >> ten;` chỉ nhập được một từ, không nhập được chuỗi có dấu cách.

Ví dụ nếu nhập:

```text
Nguyen Van An
```

thì biến `ten` chỉ nhận:

```text
Nguyen
```

---

# 7. Nhập chuỗi có dấu cách bằng `getline`

Nếu muốn nhập họ tên đầy đủ, ta dùng `getline`.

Ví dụ:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string hoTen;

    cout << "Nhap ho ten: ";
    getline(cin, hoTen);

    cout << "Ho ten cua em la: " << hoTen;

    return 0;
}
```

Ví dụ chạy:

```text
Nhap ho ten: Nguyen Van An
Ho ten cua em la: Nguyen Van An
```

Giải thích:

```cpp
getline(cin, hoTen);
```

có nghĩa là nhập cả dòng chữ từ bàn phím và lưu vào biến `hoTen`.

---

# 8. Lưu ý khi dùng `cin` trước `getline`

Nếu trước đó có dùng `cin`, rồi sau đó dùng `getline`, có thể gặp lỗi `getline` bị bỏ qua.

Ví dụ dễ lỗi:

```cpp
int tuoi;
string hoTen;

cin >> tuoi;
getline(cin, hoTen);
```

Cách sửa đơn giản là thêm:

```cpp
cin.ignore();
```

Ví dụ đầy đủ:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    int tuoi;
    string hoTen;

    cout << "Nhap tuoi: ";
    cin >> tuoi;

    cin.ignore();

    cout << "Nhap ho ten: ";
    getline(cin, hoTen);

    cout << "Ten: " << hoTen << endl;
    cout << "Tuoi: " << tuoi;

    return 0;
}
```

Với học sinh lớp 6, giáo viên có thể giải thích ngắn:

> Khi dùng `cin` nhập số trước, rồi dùng `getline` nhập chữ có dấu cách, ta thêm `cin.ignore();` ở giữa.

---

# 9. Nối chuỗi

Ta có thể dùng dấu `+` để nối chuỗi.

Ví dụ:

```cpp
string ho = "Nguyen";
string ten = "An";
string hoTen = ho + " " + ten;
```

Chương trình đầy đủ:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ho = "Nguyen";
    string ten = "An";
    string hoTen = ho + " " + ten;

    cout << hoTen;

    return 0;
}
```

Kết quả:

```text
Nguyen An
```

Ví dụ khác:

```cpp
string cauChao = "Xin chao " + ten;
```

---

# 10. Độ dài chuỗi với `.length()`

Ta có thể dùng `.length()` để biết chuỗi có bao nhiêu ký tự.

Ví dụ:

```cpp
string ten = "Nam";

cout << ten.length();
```

Kết quả:

```text
3
```

Chương trình đầy đủ:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string ten;

    cout << "Nhap ten: ";
    cin >> ten;

    cout << "Ten cua em co " << ten.length() << " ky tu";

    return 0;
}
```

Ví dụ chạy:

```text
Nhap ten: Minh
Ten cua em co 4 ky tu
```

Lưu ý:

> Khoảng trắng cũng được tính là một ký tự nếu dùng `getline`.

Ví dụ:

```text
An Binh
```

có 7 ký tự gồm cả khoảng trắng.

---

# 11. So sánh chuỗi đơn giản

Ta có thể dùng `==` để kiểm tra hai chuỗi có giống nhau không.

Ví dụ:

```cpp
string matKhau;

cout << "Nhap mat khau: ";
cin >> matKhau;

if (matKhau == "abc123") {
    cout << "Dung mat khau";
} else {
    cout << "Sai mat khau";
}
```

Chương trình đầy đủ:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string matKhau;

    cout << "Nhap mat khau: ";
    cin >> matKhau;

    if (matKhau == "abc123") {
        cout << "Dung mat khau";
    } else {
        cout << "Sai mat khau";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap mat khau: abc123
Dung mat khau
```

---

# 12. Ví dụ hoàn chỉnh: Thông tin học sinh

## Đề bài

Nhập họ tên, lớp, sở thích của học sinh. Sau đó in ra bảng thông tin.

## Chương trình

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string hoTen;
    string lop;
    string soThich;

    cout << "Nhap ho ten: ";
    getline(cin, hoTen);

    cout << "Nhap lop: ";
    getline(cin, lop);

    cout << "Nhap so thich: ";
    getline(cin, soThich);

    cout << endl;
    cout << "===== THONG TIN HOC SINH =====" << endl;
    cout << "Ho ten: " << hoTen << endl;
    cout << "Lop: " << lop << endl;
    cout << "So thich: " << soThich << endl;
    cout << "Do dai ho ten: " << hoTen.length() << " ky tu" << endl;
    cout << "==============================";

    return 0;
}
```

Ví dụ chạy:

```text
Nhap ho ten: Nguyen Van An
Nhap lop: 6A
Nhap so thich: Bong da

===== THONG TIN HOC SINH =====
Ho ten: Nguyen Van An
Lop: 6A
So thich: Bong da
Do dai ho ten: 13 ky tu
==============================
```

---

# 13. Kết hợp `string` với hàm

Ta có thể dùng `string` làm tham số của hàm.

Ví dụ:

```cpp
#include <iostream>
#include <string>
using namespace std;

void xinChao(string ten) {
    cout << "Xin chao " << ten;
}

int main() {
    string ten;

    cout << "Nhap ten: ";
    cin >> ten;

    xinChao(ten);

    return 0;
}
```

Ví dụ chạy:

```text
Nhap ten: Lan
Xin chao Lan
```

---

# 14. Lỗi thường gặp

## Lỗi 1: Quên `#include <string>`

Nên viết:

```cpp
#include <iostream>
#include <string>
using namespace std;
```

---

## Lỗi 2: Quên dấu ngoặc kép khi gán chuỗi

Sai:

```cpp
string ten = Nam;
```

Đúng:

```cpp
string ten = "Nam";
```

---

## Lỗi 3: Dùng `cin` để nhập họ tên đầy đủ

Nếu viết:

```cpp
cin >> hoTen;
```

và nhập:

```text
Nguyen Van An
```

thì chỉ nhận:

```text
Nguyen
```

Muốn nhập cả họ tên, dùng:

```cpp
getline(cin, hoTen);
```

---

## Lỗi 4: In nhầm tên biến thành chữ

Sai ý nghĩa:

```cpp
cout << "ten";
```

Đúng:

```cpp
cout << ten;
```

---

## Lỗi 5: Quên `cin.ignore()` khi dùng `cin` trước `getline`

Nếu nhập số trước rồi nhập chuỗi có dấu cách, nên dùng:

```cpp
cin.ignore();
```

Ví dụ:

```cpp
cin >> tuoi;
cin.ignore();
getline(cin, hoTen);
```

---

# 15. Hoạt động trên lớp

## Hoạt động 1: Nhập và in tên

Yêu cầu:

```text
Nhập tên học sinh.
In ra lời chào.
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

## Hoạt động 2: Nhập họ tên đầy đủ

Yêu cầu:

```text
Nhập họ tên đầy đủ.
In ra họ tên.
```

Gợi ý:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string hoTen;

    cout << "Nhap ho ten: ";
    getline(cin, hoTen);

    cout << "Ho ten: " << hoTen;

    return 0;
}
```

---

## Hoạt động 3: Đếm số ký tự trong tên

Yêu cầu:

```text
Nhập tên.
In ra số ký tự của tên.
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

    cout << "Ten co " << ten.length() << " ky tu";

    return 0;
}
```

---

# 16. Bài tập trên lớp

## Bài 1

Viết chương trình nhập tên và in:

```text
Xin chao ...
```

---

## Bài 2

Viết chương trình nhập họ tên đầy đủ và in lại họ tên đó.

---

## Bài 3

Viết chương trình nhập tên, sau đó in ra số ký tự trong tên.

---

## Bài 4

Viết chương trình nhập họ và tên riêng, sau đó ghép thành họ tên đầy đủ.

Gợi ý:

```cpp
string hoTen = ho + " " + ten;
```

---

## Bài 5

Viết chương trình nhập mật khẩu. Nếu mật khẩu bằng `"lop6"` thì in:

```text
Dang nhap thanh cong
```

Ngược lại in:

```text
Sai mat khau
```

---

# 17. Bài tập thực hành

## Bài 1: Thẻ học sinh

Nhập:

```text
Họ tên
Lớp
Trường
```

In ra:

```text
===== THE HOC SINH =====
Ho ten: ...
Lop: ...
Truong: ...
========================
```

---

## Bài 2: Giới thiệu bản thân

Nhập:

```text
Họ tên
Tuổi
Sở thích
```

Sau đó in ra:

```text
Xin chao, em ten la ...
Nam nay em ... tuoi
So thich cua em la ...
```

Gợi ý nếu nhập tuổi bằng `cin` rồi nhập sở thích bằng `getline`, cần dùng:

```cpp
cin.ignore();
```

---

## Bài 3: Kiểm tra tên

Nhập tên. Nếu tên là `"An"` thì in:

```text
Xin chao An
```

Ngược lại in:

```text
Xin chao ban
```

---

## Bài 4: Độ dài họ tên

Nhập họ tên đầy đủ. In ra độ dài của họ tên.

Gợi ý:

```cpp
hoTen.length()
```

---

# 18. Câu hỏi củng cố

Giáo viên hỏi học sinh:

1. `string` dùng để lưu dữ liệu gì?
2. Chuỗi ký tự đặt trong dấu gì?
3. `cin >> ten;` nhập được họ tên có dấu cách không?
4. Muốn nhập cả dòng có dấu cách dùng lệnh gì?
5. `.length()` dùng để làm gì?
6. Dùng dấu nào để nối chuỗi?
7. Muốn so sánh hai chuỗi bằng nhau, dùng toán tử gì?

Gợi ý trả lời:

```text
1. string dùng để lưu chuỗi ký tự.
2. Đặt trong dấu ngoặc kép " ".
3. Không. cin chỉ nhập một từ.
4. Dùng getline(cin, ten);
5. Dùng để lấy độ dài chuỗi.
6. Dùng dấu +.
7. Dùng ==.
```

---

# 19. Bài tập về nhà

## Bài 1

Viết chương trình nhập tên của em và in lời chào.

## Bài 2

Viết chương trình nhập họ tên đầy đủ bằng `getline`, sau đó in ra họ tên.

## Bài 3

Viết chương trình nhập tên, in ra số ký tự của tên.

## Bài 4

Viết chương trình nhập họ và tên riêng, sau đó ghép thành họ tên đầy đủ.

## Bài 5

Viết chương trình nhập mật khẩu. Nếu mật khẩu là `"cpp123"` thì in `Dung mat khau`, ngược lại in `Sai mat khau`.

---

# 20. Tóm tắt bài học

Học sinh cần nhớ:

```text
string dùng để lưu chuỗi ký tự.

Khai báo:
string ten = "Nam";

Nhập một từ:
cin >> ten;

Nhập cả dòng:
getline(cin, hoTen);

Nối chuỗi:
hoTen = ho + " " + ten;

Lấy độ dài chuỗi:
ten.length();

So sánh chuỗi:
if (matKhau == "abc123")
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string hoTen;

    cout << "Nhap ho ten: ";
    getline(cin, hoTen);

    cout << "Ho ten: " << hoTen << endl;
    cout << "Do dai: " << hoTen.length();

    return 0;
}
```

---

# 21. Gợi ý thời lượng dạy 60 phút

| Phần                        | Thời lượng |
| --------------------------- | ---------: |
| Ôn bài cũ                   |     5 phút |
| Giới thiệu `string`         |     8 phút |
| Khai báo, nhập, in chuỗi    |    10 phút |
| `getline` và `cin.ignore()` |    10 phút |
| Nối chuỗi, `.length()`      |    10 phút |
| Thực hành thẻ học sinh      |    14 phút |
| Củng cố, giao bài tập       |     3 phút |

Tổng: **60 phút**.
