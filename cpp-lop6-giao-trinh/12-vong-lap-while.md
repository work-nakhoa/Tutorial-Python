# Bài 12: Vòng lặp `while`

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu vòng lặp `while` dùng để làm gì.
* Biết khác nhau cơ bản giữa `for` và `while`.
* Viết được vòng lặp `while` đơn giản.
* Biết tránh lỗi vòng lặp vô hạn.
* Viết được chương trình nhập số cho đến khi nhập `0` thì dừng.
* Biết tính tổng các số được nhập vào.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi:

1. Vòng lặp dùng để làm gì?
2. Vòng lặp `for` thường dùng khi nào?
3. `i++` nghĩa là gì?
4. Muốn tính tổng từ `1` đến `n`, biến `tong` ban đầu bằng bao nhiêu?

Gợi ý trả lời:

```text
1. Vòng lặp dùng để lặp lại một công việc nhiều lần.
2. for thường dùng khi biết trước số lần lặp.
3. i++ nghĩa là tăng i lên 1.
4. tong ban đầu bằng 0.
```

Dẫn vào bài mới:

> Bài trước chúng ta học `for`, thường dùng khi biết trước số lần lặp.
> Hôm nay ta học `while`, thường dùng khi chưa biết trước sẽ lặp bao nhiêu lần.

---

# 3. Vòng lặp `while` là gì?

`while` nghĩa là **trong khi**.

Vòng lặp `while` sẽ lặp lại công việc **khi điều kiện còn đúng**.

Cấu trúc:

```cpp
while (dieu_kien) {
    // lệnh cần lặp
}
```

Giải thích:

```text
Nếu điều kiện đúng  → chạy lệnh trong while
Sau đó kiểm tra lại điều kiện
Nếu vẫn đúng       → tiếp tục chạy
Nếu sai            → dừng vòng lặp
```

---

# 4. Ví dụ đầu tiên với `while`

In các số từ `1` đến `5`.

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 1;

    while (i <= 5) {
        cout << i << " ";
        i++;
    }

    return 0;
}
```

Kết quả:

```text
1 2 3 4 5
```

Giải thích:

```text
Ban đầu i = 1
Nếu i <= 5 thì in i
Sau đó i tăng lên 1
Khi i = 6 thì điều kiện sai, vòng lặp dừng
```

---

# 5. So sánh `for` và `while`

| Vòng lặp | Thường dùng khi nào?       | Ví dụ                           |
| -------- | -------------------------- | ------------------------------- |
| `for`    | Biết trước số lần lặp      | In từ 1 đến 10                  |
| `while`  | Chưa biết trước số lần lặp | Nhập số đến khi nhập 0 thì dừng |

Ví dụ dùng `for`:

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << " ";
}
```

Ví dụ dùng `while`:

```cpp
int i = 1;

while (i <= 5) {
    cout << i << " ";
    i++;
}
```

Hai chương trình trên đều in:

```text
1 2 3 4 5
```

---

# 6. Ví dụ 2: Nhập số đến khi nhập 0 thì dừng

Đây là ví dụ quan trọng nhất của bài.

## Đề bài

Người dùng nhập số nguyên. Chương trình tiếp tục nhập cho đến khi người dùng nhập `0`.

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    while (n != 0) {
        cout << "Ban vua nhap: " << n << endl;

        cout << "Nhap n: ";
        cin >> n;
    }

    cout << "Ket thuc chuong trinh";

    return 0;
}
```

Ví dụ chạy:

```text
Nhap n: 5
Ban vua nhap: 5
Nhap n: 8
Ban vua nhap: 8
Nhap n: 3
Ban vua nhap: 3
Nhap n: 0
Ket thuc chuong trinh
```

Giải thích:

```text
Nếu n khác 0 thì tiếp tục lặp.
Nếu n bằng 0 thì dừng.
```

Điều kiện:

```cpp
n != 0
```

nghĩa là:

```text
n khác 0
```

---

# 7. Ví dụ 3: Tính tổng các số nhập vào

## Đề bài

Nhập nhiều số nguyên. Khi nhập `0` thì dừng. Tính tổng các số đã nhập, không tính số `0`.

## Phân tích

```text
Đầu vào:
- Các số nguyên nhập từ bàn phím

Điều kiện lặp:
- Lặp khi n != 0

Xử lý:
- Mỗi lần nhập số khác 0 thì cộng vào tổng

Đầu ra:
- Tổng các số đã nhập
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    while (n != 0) {
        tong = tong + n;

        cout << "Nhap n: ";
        cin >> n;
    }

    cout << "Tong la: " << tong;

    return 0;
}
```

Ví dụ chạy:

```text
Nhap n: 5
Nhap n: 7
Nhap n: 3
Nhap n: 0
Tong la: 15
```

Giải thích:

```text
tong ban đầu bằng 0
Nhập 5  → tong = 0 + 5 = 5
Nhập 7  → tong = 5 + 7 = 12
Nhập 3  → tong = 12 + 3 = 15
Nhập 0  → dừng
```

---

# 8. Ví dụ 4: Đếm số lượng số đã nhập

## Đề bài

Nhập nhiều số nguyên. Khi nhập `0` thì dừng. Đếm xem người dùng đã nhập bao nhiêu số khác `0`.

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int dem = 0;

    cout << "Nhap n: ";
    cin >> n;

    while (n != 0) {
        dem = dem + 1;

        cout << "Nhap n: ";
        cin >> n;
    }

    cout << "Ban da nhap " << dem << " so";

    return 0;
}
```

Ví dụ:

```text
Nhap n: 4
Nhap n: 9
Nhap n: 2
Nhap n: 0
Ban da nhap 3 so
```

---

# 9. Lỗi thường gặp với `while`

## Lỗi 1: Quên cập nhật biến

Sai:

```cpp
int i = 1;

while (i <= 5) {
    cout << i << " ";
}
```

Chương trình sẽ lặp mãi vì `i` luôn bằng `1`.

Đúng:

```cpp
int i = 1;

while (i <= 5) {
    cout << i << " ";
    i++;
}
```

---

## Lỗi 2: Điều kiện luôn đúng

Sai:

```cpp
while (true) {
    cout << "Lap mai";
}
```

Chương trình sẽ chạy mãi nếu không có lệnh dừng.

Với học sinh mới học, chưa nên dùng dạng này.

---

## Lỗi 3: Quên nhập lại dữ liệu trong vòng lặp

Sai:

```cpp
int n;
cin >> n;

while (n != 0) {
    cout << n;
}
```

Nếu `n` khác `0`, vòng lặp sẽ chạy mãi.

Đúng:

```cpp
int n;
cin >> n;

while (n != 0) {
    cout << n;

    cin >> n;
}
```

---

# 10. Hoạt động thực hành trên lớp

## Bài 1: In số từ 1 đến 5 bằng `while`

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 1;

    while (i <= 5) {
        cout << i << " ";
        i++;
    }

    return 0;
}
```

---

## Bài 2: Nhập số đến khi nhập 0 thì dừng

Yêu cầu:

```text
Nhập số nguyên.
Nếu số khác 0 thì in ra số đó.
Nếu nhập 0 thì dừng.
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    while (n != 0) {
        cout << "So vua nhap: " << n << endl;

        cout << "Nhap n: ";
        cin >> n;
    }

    cout << "Ket thuc";

    return 0;
}
```

---

## Bài 3: Tính tổng các số nhập vào

Yêu cầu:

```text
Nhập nhiều số.
Nhập 0 thì dừng.
In tổng các số đã nhập.
```

Gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    while (n != 0) {
        tong = tong + n;

        cout << "Nhap n: ";
        cin >> n;
    }

    cout << "Tong la: " << tong;

    return 0;
}
```

---

# 11. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

Vòng lặp `while` chạy khi nào?

A. Khi điều kiện sai
B. Khi điều kiện đúng
C. Khi chương trình kết thúc
D. Khi không có biến

Đáp án: **B**

---

## Bài 2: Điền từ còn thiếu

```text
while nghĩa là lặp lại trong khi điều kiện còn ______.
```

Đáp án:

```text
đúng
```

---

## Bài 3: Đoán kết quả

```cpp
int i = 1;

while (i <= 3) {
    cout << i << " ";
    i++;
}
```

Đáp án:

```text
1 2 3
```

---

## Bài 4: Tìm lỗi sai

```cpp
int i = 1;

while (i <= 5) {
    cout << i << " ";
}
```

Lỗi:

```text
Thiếu i++, nên vòng lặp có thể chạy mãi.
```

Sửa đúng:

```cpp
int i = 1;

while (i <= 5) {
    cout << i << " ";
    i++;
}
```

---

# 12. Bài tập về nhà

## Bài 1

Viết chương trình dùng `while` để in các số từ `1` đến `10`.

---

## Bài 2

Viết chương trình dùng `while` để in các số từ `10` về `1`.

Gợi ý:

```cpp
int i = 10;

while (i >= 1) {
    cout << i << " ";
    i--;
}
```

---

## Bài 3

Viết chương trình nhập nhiều số nguyên. Khi nhập `0` thì dừng. In tổng các số đã nhập.

---

## Bài 4

Viết chương trình nhập nhiều số nguyên. Khi nhập `0` thì dừng. Đếm xem đã nhập bao nhiêu số khác `0`.

---

# 13. Tóm tắt bài học

Học sinh cần nhớ:

```text
while dùng để lặp khi điều kiện còn đúng.

Cấu trúc:

while (dieu_kien) {
    // lệnh cần lặp
}

for thường dùng khi biết trước số lần lặp.
while thường dùng khi chưa biết trước số lần lặp.

Cẩn thận:
- Phải có cách làm điều kiện thay đổi.
- Nếu điều kiện luôn đúng, vòng lặp có thể chạy mãi.
```

Mẫu quan trọng:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    while (n != 0) {
        cout << "Ban vua nhap: " << n << endl;

        cout << "Nhap n: ";
        cin >> n;
    }

    cout << "Ket thuc";

    return 0;
}
```

---

# 14. Gợi ý thời lượng dạy 45 phút

| Phần                                | Thời lượng |
| ----------------------------------- | ---------: |
| Ôn bài cũ                           |     5 phút |
| Giới thiệu vòng lặp `while`         |     7 phút |
| Ví dụ in số từ 1 đến 5              |     7 phút |
| So sánh `for` và `while`            |     5 phút |
| Ví dụ nhập đến khi nhập 0           |    10 phút |
| Thực hành tính tổng các số nhập vào |     8 phút |
| Củng cố và giao bài tập             |     3 phút |

Tổng: **45 phút**.
