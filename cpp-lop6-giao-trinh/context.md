Dưới đây là một **khung giáo trình C/C++ cơ bản cho học sinh lớp 6**, phù hợp với học sinh mới bắt đầu lập trình. Nên ưu tiên **C++ cơ bản** thay vì C thuần, vì C++ dễ dạy hơn với `cin`, `cout`, `string`.

## Mục tiêu giáo trình

Sau khóa học, học sinh có thể:

* Hiểu lập trình là gì.
* Viết chương trình C++ đơn giản.
* Biết dùng biến, kiểu dữ liệu, nhập xuất.
* Biết dùng điều kiện `if`, vòng lặp `for`, `while`.
* Biết xử lý bài toán cơ bản bằng tư duy thuật toán.
* Làm được một số chương trình nhỏ: máy tính mini, đoán số, bảng cửu chương, quản lý điểm đơn giản.

---

# Giáo trình C/C++ cơ bản cho lớp 6

## Phần 1: Làm quen với lập trình

### Bài 1: Lập trình là gì?

Nội dung:

* Máy tính hiểu lệnh như thế nào?
* Chương trình là gì?
* Ngôn ngữ lập trình là gì?
* C, C++ là gì?
* Ví dụ chương trình đầu tiên.

Bài tập:

* Kể tên 3 phần mềm/app mà em dùng hằng ngày.
* Theo em, app đó cần những lệnh gì?

---

### Bài 2: Cài đặt môi trường lập trình

Nội dung:

* Cài VS Code hoặc Dev-C++.
* Cài compiler C++.
* Tạo file `.cpp`.
* Chạy chương trình đầu tiên.

Chương trình mẫu:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao lop 6!";
    return 0;
}
```

Bài tập:

* In ra tên của em.
* In ra lớp của em.
* In ra 3 dòng giới thiệu bản thân.

---

## Phần 2: Nhập xuất và biến

### Bài 3: Lệnh in ra màn hình `cout`

Nội dung:

* `cout` là gì?
* In chữ, in số.
* Xuống dòng bằng `endl` hoặc `\n`.
* Lỗi thường gặp khi thiếu dấu `;`.

Bài tập:

* In thời khóa biểu 1 ngày.
* In một bài thơ ngắn.
* In hình tam giác bằng dấu `*`.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "*\n";
    cout << "**\n";
    cout << "***\n";
    return 0;
}
```

---

### Bài 4: Biến và kiểu dữ liệu

Nội dung:

* Biến là gì?
* Các kiểu dữ liệu cơ bản:

  * `int`: số nguyên
  * `float`, `double`: số thập phân
  * `char`: một ký tự
  * `string`: chuỗi ký tự
  * `bool`: đúng/sai
* Cách đặt tên biến.

Bài tập:

* Tạo biến lưu tuổi, chiều cao, điểm toán.
* In thông tin học sinh ra màn hình.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi = 11;
    string ten = "Nam";

    cout << "Ten: " << ten << endl;
    cout << "Tuoi: " << tuoi << endl;

    return 0;
}
```

---

### Bài 5: Nhập dữ liệu với `cin`

Nội dung:

* Nhập số nguyên.
* Nhập số thập phân.
* Nhập chuỗi đơn giản.
* Kết hợp `cin` và `cout`.

Bài tập:

* Nhập tên và tuổi, sau đó in ra lời chào.
* Nhập 2 số và in ra tổng.
* Nhập điểm toán, văn, anh và tính điểm trung bình.

Ví dụ:

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

## Phần 3: Toán tử và biểu thức

### Bài 6: Các phép toán cơ bản

Nội dung:

* Cộng `+`
* Trừ `-`
* Nhân `*`
* Chia `/`
* Chia lấy dư `%`
* Thứ tự ưu tiên phép toán.

Bài tập:

* Tính chu vi, diện tích hình chữ nhật.
* Tính chu vi, diện tích hình vuông.
* Tính số phút từ số giờ nhập vào.
* Kiểm tra một số chia cho 2 dư bao nhiêu.

---

### Bài 7: Bài tập ứng dụng phép toán

Nội dung:

* Phân tích bài toán.
* Xác định đầu vào, đầu ra.
* Viết công thức.
* Chuyển công thức thành code.

Bài tập:

* Đổi km sang m.
* Đổi ngày sang giờ.
* Tính tổng tiền mua hàng.
* Tính tuổi từ năm sinh.

---

## Phần 4: Câu lệnh điều kiện

### Bài 8: Điều kiện `if`

Nội dung:

* Điều kiện đúng/sai.
* Câu lệnh `if`.
* Toán tử so sánh:

  * `>`
  * `<`
  * `>=`
  * `<=`
  * `==`
  * `!=`

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tuoi;
    cin >> tuoi;

    if (tuoi >= 11) {
        cout << "Em da hoc lop 6";
    }

    return 0;
}
```

Bài tập:

* Nhập tuổi, kiểm tra có đủ 11 tuổi không.
* Nhập điểm, nếu điểm từ 5 trở lên thì in “Đạt”.
* Nhập số, kiểm tra số dương.

---

### Bài 9: Điều kiện `if else`

Nội dung:

* Khi đúng làm gì, khi sai làm gì.
* Cấu trúc `if else`.
* Lỗi nhầm `=` và `==`.

Bài tập:

* Kiểm tra số chẵn/lẻ.
* Kiểm tra điểm đạt/chưa đạt.
* Kiểm tra số lớn hơn trong 2 số.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
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

### Bài 10: Nhiều điều kiện `if else if`

Nội dung:

* Xử lý nhiều trường hợp.
* Xếp loại điểm.
* Kết hợp điều kiện với `&&`, `||`.

Bài tập:

* Nhập điểm, xếp loại:

  * > = 8: Giỏi
  * > = 6.5: Khá
  * > = 5: Trung bình
  * < 5: Chưa đạt
* Nhập tháng, in ra mùa đơn giản.
* Nhập số, kiểm tra âm/dương/bằng 0.

---

## Phần 5: Vòng lặp

### Bài 11: Vòng lặp `for`

Nội dung:

* Khi nào cần lặp?
* Cấu trúc `for`.
* Biến đếm.
* In dãy số.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 10; i++) {
        cout << i << " ";
    }

    return 0;
}
```

Bài tập:

* In các số từ 1 đến 100.
* In các số chẵn từ 2 đến 50.
* In bảng cửu chương của số nhập vào.
* Tính tổng từ 1 đến n.

---

### Bài 12: Vòng lặp `while`

Nội dung:

* Khác nhau giữa `for` và `while`.
* Lặp khi điều kiện còn đúng.
* Tránh vòng lặp vô hạn.

Bài tập:

* Nhập số cho đến khi nhập số 0 thì dừng.
* Tính tổng các số nhập vào.
* Đếm có bao nhiêu số đã nhập.

---

### Bài 13: Bài tập luyện vòng lặp

Nội dung:

* Kết hợp vòng lặp và điều kiện.
* Tìm số lớn nhất, nhỏ nhất.
* Đếm số chẵn, số lẻ.

Bài tập:

* Nhập n số, tính tổng.
* Nhập n số, đếm số chẵn.
* In hình chữ nhật bằng dấu `*`.
* In tam giác sao.

---

## Phần 6: Tư duy thuật toán cơ bản

### Bài 14: Thuật toán là gì?

Nội dung:

* Thuật toán là các bước giải quyết vấn đề.
* Ví dụ thuật toán đánh răng, nấu mì, đi học.
* Viết thuật toán bằng lời trước khi code.

Bài tập:

* Viết các bước tính điểm trung bình.
* Viết các bước kiểm tra số chẵn/lẻ.
* Viết các bước tìm số lớn nhất trong 3 số.

---

### Bài 15: Phân tích bài toán lập trình

Nội dung:

* Đầu vào là gì?
* Đầu ra là gì?
* Cách xử lý ở giữa.
* Chạy thử bằng ví dụ nhỏ.

Mẫu phân tích:

```text
Bài toán: Nhập 2 số, in số lớn hơn.

Đầu vào: a, b
Xử lý:
- Nếu a > b thì in a
- Ngược lại in b
Đầu ra: số lớn hơn
```

Bài tập:

* Tính diện tích hình chữ nhật.
* Kiểm tra học sinh đạt hay chưa.
* Tính tổng từ 1 đến n.
* Tìm số lớn nhất trong 3 số.

---

## Phần 7: Hàm cơ bản

### Bài 16: Hàm là gì?

Nội dung:

* Hàm giúp chia nhỏ chương trình.
* Hàm có sẵn: `main`.
* Hàm tự viết.
* Hàm không trả về giá trị `void`.
* Hàm có trả về giá trị `int`, `double`.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

void xinChao() {
    cout << "Xin chao!";
}

int main() {
    xinChao();
    return 0;
}
```

Bài tập:

* Viết hàm in lời chào.
* Viết hàm tính tổng 2 số.
* Viết hàm kiểm tra chẵn/lẻ.

---

## Phần 8: Chuỗi ký tự cơ bản

### Bài 17: Làm việc với `string`

Nội dung:

* Chuỗi là gì?
* Khai báo `string`.
* Nhập chuỗi.
* Nối chuỗi.
* Độ dài chuỗi với `.length()`.

Bài tập:

* Nhập họ tên và in lời chào.
* Đếm số ký tự trong tên.
* Ghép họ và tên.
* Kiểm tra tên có dài hơn 10 ký tự không.

---

## Phần 9: Mảng cơ bản

### Bài 18: Mảng một chiều

Nội dung:

* Mảng là gì?
* Khi nào dùng mảng?
* Khai báo mảng.
* Truy cập phần tử.
* Duyệt mảng bằng vòng lặp.

Ví dụ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a[5] = {1, 2, 3, 4, 5};

    for (int i = 0; i < 5; i++) {
        cout << a[i] << " ";
    }

    return 0;
}
```

Bài tập:

* Nhập 5 điểm và in ra.
* Tính tổng các phần tử trong mảng.
* Tìm số lớn nhất trong mảng.
* Đếm số chẵn trong mảng.

---

## Phần 10: Mini project

### Bài 19: Dự án nhỏ 1 — Máy tính mini

Chức năng:

* Nhập 2 số.
* Chọn phép toán `+`, `-`, `*`, `/`.
* In kết quả.

Kiến thức dùng:

* `cin`, `cout`
* Biến
* `if else`
* Phép toán

---

### Bài 20: Dự án nhỏ 2 — Trò chơi đoán số

Chức năng:

* Máy có một số bí mật.
* Người chơi nhập số đoán.
* Chương trình báo lớn hơn, nhỏ hơn hoặc đúng.
* Cho đoán nhiều lần.

Kiến thức dùng:

* `while`
* `if else`
* Biến đếm

---

### Bài 21: Dự án nhỏ 3 — Quản lý điểm học sinh đơn giản

Chức năng:

* Nhập số lượng học sinh.
* Nhập điểm từng học sinh.
* Tính điểm trung bình.
* Tìm điểm cao nhất.
* Đếm số bạn đạt.

Kiến thức dùng:

* Mảng
* Vòng lặp
* Điều kiện
* Biến tổng

---

# Gợi ý chia thời lượng

Nếu học trong **12 buổi**, có thể chia như sau:

| Buổi | Nội dung                                               |
| ---- | ------------------------------------------------------ |
| 1    | Lập trình là gì, cài môi trường, chương trình đầu tiên |
| 2    | `cout`, biến, kiểu dữ liệu                             |
| 3    | `cin`, phép toán                                       |
| 4    | Bài tập phép toán, phân tích đầu vào/đầu ra            |
| 5    | `if`, `if else`                                        |
| 6    | `else if`, toán tử logic                               |
| 7    | Vòng lặp `for`                                         |
| 8    | Vòng lặp `while`                                       |
| 9    | Bài tập vòng lặp, in hình sao                          |
| 10   | Hàm cơ bản                                             |
| 11   | Mảng cơ bản                                            |
| 12   | Mini project tổng kết                                  |

Nếu học trong **20 buổi**, có thể dạy chậm hơn, mỗi bài một buổi, thêm nhiều bài tập thực hành và trò chơi nhỏ.

---

# Nên dạy C hay C++ cho lớp 6?

Nên dạy **C++ cơ bản**.

Lý do:

* `cout`, `cin` dễ hiểu hơn `printf`, `scanf`.
* Có `string` dễ dùng hơn mảng ký tự trong C.
* Học sinh lớp 6 chưa cần học con trỏ, cấp phát bộ nhớ, struct phức tạp.
* Vẫn giữ được tư duy thuật toán giống C.

Nên tránh ở giai đoạn đầu:

* Con trỏ.
* Cấp phát động.
* OOP phức tạp.
* Template.
* File.
* Đệ quy khó.
* Các thuật toán nâng cao.

---

# Lộ trình kiến thức đề xuất

```text
In ra màn hình
→ Biến
→ Nhập dữ liệu
→ Phép toán
→ Điều kiện
→ Vòng lặp
→ Hàm
→ Chuỗi
→ Mảng
→ Project nhỏ
```

Với lớp 6, mục tiêu quan trọng nhất không phải là học thật nhiều cú pháp, mà là giúp học sinh hình thành tư duy:

```text
Bài toán cần gì?
Dữ liệu vào là gì?
Cần xử lý như thế nào?
Kết quả ra là gì?
```

Đây là nền tảng tốt để sau này học C++, Python, Scratch, Arduino hoặc lập trình thi đấu.
