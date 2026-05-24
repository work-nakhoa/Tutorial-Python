# Bài 11: Vòng lặp `for`

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu vòng lặp là gì.
* Biết khi nào cần dùng vòng lặp.
* Biết cấu trúc vòng lặp `for`.
* Biết dùng biến đếm `i`.
* Biết in dãy số bằng vòng lặp.
* Biết tính tổng từ `1` đến `n`.
* Biết in bảng cửu chương.
* Biết tránh lỗi vòng lặp chạy sai số lần hoặc chạy vô hạn.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. `if else if` dùng khi nào?
2. Máy tính kiểm tra các điều kiện theo thứ tự nào?
3. Toán tử `&&` nghĩa là gì?
4. Toán tử `||` nghĩa là gì?
5. Điều kiện kiểm tra số chẵn là gì?
6. Điều kiện kiểm tra điểm hợp lệ từ 0 đến 10 là gì?

Gợi ý trả lời:

```text
1. Dùng khi có nhiều trường hợp.
2. Từ trên xuống dưới.
3. && nghĩa là và.
4. || nghĩa là hoặc.
5. n % 2 == 0
6. diem >= 0 && diem <= 10
```

Giáo viên dẫn vào bài mới:

> Ở các bài trước, nếu muốn in 10 dòng, chúng ta phải viết 10 câu lệnh `cout`.
> Cách đó rất dài và dễ sai.
> Hôm nay, chúng ta học **vòng lặp `for`**, giúp máy tính lặp lại một công việc nhiều lần.

---

# 3. Vòng lặp là gì?

**Vòng lặp** là cách để chương trình thực hiện một hoặc nhiều câu lệnh lặp đi lặp lại nhiều lần.

Ví dụ trong đời sống:

```text
Đánh răng:
- Chải răng nhiều lần

Tập thể dục:
- Nhảy dây 100 lần

Viết phạt:
- Viết câu "Em sẽ làm bài tập" 20 lần
```

Trong lập trình cũng vậy.

Ví dụ:

```text
In các số từ 1 đến 10
In bảng cửu chương
Tính tổng các số từ 1 đến n
In nhiều dòng dấu *
```

Nếu không có vòng lặp, ta phải viết rất nhiều dòng code.

---

# 4. Vì sao cần vòng lặp?

Giả sử muốn in các số từ 1 đến 5.

Nếu không dùng vòng lặp:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << 1 << endl;
    cout << 2 << endl;
    cout << 3 << endl;
    cout << 4 << endl;
    cout << 5 << endl;

    return 0;
}
```

Nếu muốn in từ 1 đến 100 thì sao?

Ta không nên viết 100 dòng `cout`.

Dùng vòng lặp `for`:

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 100; i++) {
        cout << i << endl;
    }

    return 0;
}
```

Kết luận:

```text
Vòng lặp giúp code ngắn hơn, dễ sửa hơn và lặp lại công việc nhanh hơn.
```

---

# 5. Vòng lặp `for` là gì?

`for` là vòng lặp thường dùng khi ta biết trước số lần cần lặp.

Ví dụ:

```text
In 10 lần
Lặp từ 1 đến 100
Lặp qua các số từ 1 đến n
In bảng cửu chương từ 1 đến 10
```

Cấu trúc:

```cpp
for (khoi_tao; dieu_kien; cap_nhat) {
    // lệnh cần lặp
}
```

Ví dụ:

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}
```

Kết quả:

```text
1
2
3
4
5
```

---

# 6. Giải thích cấu trúc `for`

Xét vòng lặp:

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}
```

Trong đó:

| Thành phần  | Ý nghĩa                         |
| ----------- | ------------------------------- |
| `int i = 1` | Tạo biến đếm `i`, bắt đầu từ 1  |
| `i <= 5`    | Điều kiện để vòng lặp còn chạy  |
| `i++`       | Sau mỗi lần lặp, tăng `i` lên 1 |
| `cout << i` | Lệnh được lặp lại               |

Giải thích bằng lời:

```text
Bắt đầu i = 1.
Nếu i <= 5 thì in i.
Sau đó tăng i lên 1.
Lặp lại cho đến khi i > 5 thì dừng.
```

---

# 7. Biến đếm `i`

Trong vòng lặp, ta thường dùng biến tên là `i`.

Ví dụ:

```cpp
for (int i = 1; i <= 10; i++) {
    cout << i << endl;
}
```

`i` là biến đếm.

Nó cho biết vòng lặp đang chạy ở lần thứ mấy hoặc đang đến số nào.

Giá trị của `i` thay đổi sau mỗi lần lặp:

```text
Lần 1: i = 1
Lần 2: i = 2
Lần 3: i = 3
...
Lần 10: i = 10
```

---

# 8. Ý nghĩa của `i++`

Câu lệnh:

```cpp
i++
```

có nghĩa là:

```text
Tăng i lên 1
```

Ví dụ:

```cpp
int i = 1;
i++;
```

Sau khi chạy `i++`, giá trị của `i` là:

```text
2
```

Có thể hiểu:

```cpp
i++;
```

giống với:

```cpp
i = i + 1;
```

Trong vòng lặp:

```cpp
for (int i = 1; i <= 5; i++)
```

`i++` giúp `i` tăng dần:

```text
1 → 2 → 3 → 4 → 5
```

---

# 9. Cách vòng lặp chạy từng bước

Ví dụ:

```cpp
for (int i = 1; i <= 3; i++) {
    cout << i << endl;
}
```

Máy tính chạy như sau:

```text
Bước 1: i = 1
Kiểm tra i <= 3 → đúng
In 1
Tăng i lên 2

Bước 2: i = 2
Kiểm tra i <= 3 → đúng
In 2
Tăng i lên 3

Bước 3: i = 3
Kiểm tra i <= 3 → đúng
In 3
Tăng i lên 4

Bước 4: i = 4
Kiểm tra i <= 3 → sai
Dừng vòng lặp
```

Kết quả:

```text
1
2
3
```

---

# 10. Ví dụ 1: In dòng chữ nhiều lần

## Đề bài

In dòng chữ `"Xin chao"` 5 lần.

## Nếu không dùng vòng lặp

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao" << endl;
    cout << "Xin chao" << endl;
    cout << "Xin chao" << endl;
    cout << "Xin chao" << endl;
    cout << "Xin chao" << endl;

    return 0;
}
```

## Dùng vòng lặp `for`

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        cout << "Xin chao" << endl;
    }

    return 0;
}
```

Kết quả:

```text
Xin chao
Xin chao
Xin chao
Xin chao
Xin chao
```

---

# 11. Ví dụ 2: In các số từ 1 đến 10

## Đề bài

In các số từ 1 đến 10.

## Chương trình

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

Kết quả:

```text
1 2 3 4 5 6 7 8 9 10
```

Giải thích:

```text
i bắt đầu từ 1.
Mỗi lần lặp in i.
Sau mỗi lần lặp, i tăng thêm 1.
Vòng lặp dừng khi i lớn hơn 10.
```

---

# 12. Ví dụ 3: In các số từ 1 đến n

## Đề bài

Nhập số nguyên `n`. In các số từ `1` đến `n`.

## Phân tích

```text
Đầu vào:
- n

Xử lý:
- Cho i chạy từ 1 đến n
- Mỗi lần in i

Đầu ra:
- Dãy số từ 1 đến n
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        cout << i << " ";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap n: 7
1 2 3 4 5 6 7
```

---

# 13. Ví dụ 4: In các số chẵn từ 2 đến 20

Có 2 cách làm.

## Cách 1: Tăng `i` thêm 2

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 2; i <= 20; i = i + 2) {
        cout << i << " ";
    }

    return 0;
}
```

Kết quả:

```text
2 4 6 8 10 12 14 16 18 20
```

## Cách 2: Dùng `if`

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 20; i++) {
        if (i % 2 == 0) {
            cout << i << " ";
        }
    }

    return 0;
}
```

Với học sinh mới học, giáo viên nên dạy **cách 1 trước** vì dễ hiểu hơn.

---

# 14. Ví dụ 5: In các số lẻ từ 1 đến 19

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 19; i = i + 2) {
        cout << i << " ";
    }

    return 0;
}
```

Kết quả:

```text
1 3 5 7 9 11 13 15 17 19
```

Giải thích:

```text
Bắt đầu từ 1.
Mỗi lần tăng thêm 2.
Nên ta được các số lẻ.
```

---

# 15. Ví dụ 6: In ngược từ 10 về 1

Vòng lặp không chỉ tăng lên, mà còn có thể giảm xuống.

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 10; i >= 1; i--) {
        cout << i << " ";
    }

    return 0;
}
```

Kết quả:

```text
10 9 8 7 6 5 4 3 2 1
```

Trong đó:

```cpp
i--
```

nghĩa là:

```text
Giảm i đi 1
```

Tương đương:

```cpp
i = i - 1;
```

---

# 16. Tính tổng từ 1 đến n

## Đề bài

Nhập số nguyên `n`. Tính tổng:

```text
1 + 2 + 3 + ... + n
```

Ví dụ:

```text
n = 5
Tổng = 1 + 2 + 3 + 4 + 5 = 15
```

## Phân tích

```text
Đầu vào:
- n

Xử lý:
- Tạo biến tong = 0
- Cho i chạy từ 1 đến n
- Mỗi lần cộng i vào tong

Đầu ra:
- tong
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

    for (int i = 1; i <= n; i++) {
        tong = tong + i;
    }

    cout << "Tong la: " << tong;

    return 0;
}
```

Ví dụ:

```text
Nhap n: 5
Tong la: 15
```

---

# 17. Giải thích biến `tong`

Trong chương trình:

```cpp
int tong = 0;
```

Ta tạo biến `tong` để lưu kết quả cộng dồn.

Trong vòng lặp:

```cpp
tong = tong + i;
```

Nghĩa là:

```text
Lấy tổng hiện tại cộng thêm i,
rồi lưu kết quả mới vào biến tong.
```

Nếu `n = 5`, quá trình như sau:

| Lần lặp | `i` | `tong = tong + i` | Giá trị mới của `tong` |
| ------: | --: | ----------------- | ---------------------: |
| Ban đầu |     |                   |                      0 |
|       1 |   1 | 0 + 1             |                      1 |
|       2 |   2 | 1 + 2             |                      3 |
|       3 |   3 | 3 + 3             |                      6 |
|       4 |   4 | 6 + 4             |                     10 |
|       5 |   5 | 10 + 5            |                     15 |

Kết quả cuối cùng:

```text
15
```

---

# 18. Tính tổng các số chẵn từ 1 đến n

## Đề bài

Nhập `n`. Tính tổng các số chẵn từ `1` đến `n`.

Ví dụ:

```text
n = 10
Các số chẵn: 2, 4, 6, 8, 10
Tổng = 30
```

## Cách 1: Cho `i` chạy qua các số chẵn

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 2; i <= n; i = i + 2) {
        tong = tong + i;
    }

    cout << "Tong cac so chan la: " << tong;

    return 0;
}
```

## Cách 2: Dùng `if`

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        if (i % 2 == 0) {
            tong = tong + i;
        }
    }

    cout << "Tong cac so chan la: " << tong;

    return 0;
}
```

Với lớp 6, giáo viên có thể dạy cách 1 trước, sau đó giới thiệu cách 2 để ôn lại `if`.

---

# 19. Bảng cửu chương

## Đề bài

Nhập số `n`. In bảng cửu chương của `n` từ `1` đến `10`.

Ví dụ:

```text
Nhap n: 5

5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
...
5 x 10 = 50
```

## Phân tích

```text
Đầu vào:
- n

Xử lý:
- Cho i chạy từ 1 đến 10
- Mỗi lần in n * i

Đầu ra:
- Bảng cửu chương của n
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= 10; i++) {
        cout << n << " x " << i << " = " << n * i << endl;
    }

    return 0;
}
```

Ví dụ:

```text
Nhap n: 3
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
3 x 6 = 18
3 x 7 = 21
3 x 8 = 24
3 x 9 = 27
3 x 10 = 30
```

---

# 20. In hình bằng dấu `*`

## Ví dụ 1: In 5 dấu sao trên một dòng

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        cout << "*";
    }

    return 0;
}
```

Kết quả:

```text
*****
```

---

## Ví dụ 2: In 5 dòng dấu sao

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        cout << "*" << endl;
    }

    return 0;
}
```

Kết quả:

```text
*
*
*
*
*
```

---

## Ví dụ 3: In một dòng có `n` dấu sao

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        cout << "*";
    }

    return 0;
}
```

Ví dụ:

```text
Nhap n: 8
********
```

---

# 21. Kết hợp `for` và `if`

Ta có thể dùng `if` bên trong vòng lặp.

Ví dụ: In các số từ 1 đến `n`, nhưng chỉ in số chia hết cho 3.

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        if (i % 3 == 0) {
            cout << i << " ";
        }
    }

    return 0;
}
```

Ví dụ:

```text
Nhap n: 15
3 6 9 12 15
```

Giải thích:

```text
Vòng lặp đi qua từng số từ 1 đến n.
Nếu số đó chia hết cho 3 thì in ra.
```

---

# 22. Đếm số lượng

Ngoài tính tổng, vòng lặp còn dùng để đếm.

## Đề bài

Nhập `n`. Đếm xem từ `1` đến `n` có bao nhiêu số chẵn.

Ví dụ:

```text
n = 10
Các số chẵn: 2, 4, 6, 8, 10
Có 5 số chẵn
```

## Chương trình

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int dem = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        if (i % 2 == 0) {
            dem = dem + 1;
        }
    }

    cout << "Co " << dem << " so chan";

    return 0;
}
```

Giải thích:

```cpp
int dem = 0;
```

Tạo biến đếm, ban đầu bằng 0.

```cpp
dem = dem + 1;
```

Mỗi khi gặp một số chẵn, tăng biến `dem` thêm 1.

Có thể viết ngắn hơn:

```cpp
dem++;
```

Nhưng với học sinh mới học, nên dùng:

```cpp
dem = dem + 1;
```

để dễ hiểu.

---

# 23. Quy trình làm bài có vòng lặp `for`

Khi làm bài có vòng lặp, học sinh nên làm theo các bước:

```text
Bước 1: Xác định cần lặp việc gì.
Bước 2: Xác định lặp từ đâu.
Bước 3: Xác định lặp đến đâu.
Bước 4: Xác định mỗi lần lặp thay đổi như thế nào.
Bước 5: Viết câu lệnh trong vòng lặp.
Bước 6: Chạy thử với số nhỏ.
```

Ví dụ bài:

```text
In các số từ 1 đến n.
```

Phân tích:

```text
Cần lặp việc gì?
- In số i

Lặp từ đâu?
- i = 1

Lặp đến đâu?
- i <= n

Mỗi lần thay đổi thế nào?
- i tăng thêm 1

Code:
for (int i = 1; i <= n; i++) {
    cout << i << " ";
}
```

---

# 24. Lỗi thường gặp khi dùng `for`

## Lỗi 1: Quên tăng biến đếm

Sai:

```cpp
for (int i = 1; i <= 5;) {
    cout << i << endl;
}
```

Vì `i` không tăng, vòng lặp có thể chạy mãi.

Đúng:

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}
```

---

## Lỗi 2: Điều kiện sai làm vòng lặp không chạy

Sai:

```cpp
for (int i = 1; i >= 5; i++) {
    cout << i << endl;
}
```

Vì ban đầu `i = 1`, điều kiện `i >= 5` là sai, nên vòng lặp không chạy.

Đúng:

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}
```

---

## Lỗi 3: Dùng sai dấu khi in ngược

Sai:

```cpp
for (int i = 10; i >= 1; i++) {
    cout << i << " ";
}
```

Vòng lặp này sai vì `i++` làm `i` tăng lên, trong khi muốn đi từ 10 về 1.

Đúng:

```cpp
for (int i = 10; i >= 1; i--) {
    cout << i << " ";
}
```

---

## Lỗi 4: Đặt dấu `;` ngay sau dòng `for`

Sai:

```cpp
for (int i = 1; i <= 5; i++);
{
    cout << i << endl;
}
```

Đúng:

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}
```

Giải thích:

> Không đặt dấu `;` ngay sau dòng `for`.

---

## Lỗi 5: Quên khởi tạo biến tổng

Sai:

```cpp
int tong;

for (int i = 1; i <= n; i++) {
    tong = tong + i;
}
```

Đúng:

```cpp
int tong = 0;

for (int i = 1; i <= n; i++) {
    tong = tong + i;
}
```

Giải thích:

> Khi tính tổng, phải cho tổng ban đầu bằng 0.

---

# 25. Hoạt động thực hành 1: In lời chào 5 lần

## Đề bài

In dòng chữ:

```text
Xin chao
```

5 lần.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        cout << "Xin chao" << endl;
    }

    return 0;
}
```

---

# 26. Hoạt động thực hành 2: In số từ 1 đến n

## Đề bài

Nhập `n`, in các số từ `1` đến `n`.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        cout << i << " ";
    }

    return 0;
}
```

---

# 27. Hoạt động thực hành 3: Tính tổng từ 1 đến n

## Đề bài

Nhập `n`, tính tổng từ `1` đến `n`.

## Code gợi ý

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

# 28. Hoạt động thực hành 4: In bảng cửu chương

## Đề bài

Nhập số `n`, in bảng cửu chương của `n`.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= 10; i++) {
        cout << n << " x " << i << " = " << n * i << endl;
    }

    return 0;
}
```

---

# 29. Hoạt động thực hành 5: Đếm số chẵn từ 1 đến n

## Đề bài

Nhập `n`, đếm có bao nhiêu số chẵn từ `1` đến `n`.

## Code gợi ý

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int dem = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        if (i % 2 == 0) {
            dem = dem + 1;
        }
    }

    cout << "Co " << dem << " so chan";

    return 0;
}
```

---

# 30. Bài tập trên lớp

## Bài 1: Chọn đáp án đúng

Vòng lặp `for` dùng để làm gì?

A. Nhập dữ liệu
B. In dữ liệu
C. Lặp lại một công việc nhiều lần
D. Kết thúc chương trình

Đáp án: **C**

---

## Bài 2: Chọn đáp án đúng

Trong câu lệnh sau, biến đếm là biến nào?

```cpp
for (int i = 1; i <= 10; i++) {
    cout << i;
}
```

A. `int`
B. `i`
C. `cout`
D. `return`

Đáp án: **B**

---

## Bài 3: Điền từ còn thiếu

```text
i++ nghĩa là tăng i lên ______.
```

Đáp án:

```text
1
```

---

## Bài 4: Đoán kết quả

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << " ";
}
```

Đáp án:

```text
1 2 3 4 5
```

---

## Bài 5: Đoán kết quả

```cpp
for (int i = 2; i <= 10; i = i + 2) {
    cout << i << " ";
}
```

Đáp án:

```text
2 4 6 8 10
```

---

## Bài 6: Đoán kết quả

```cpp
for (int i = 5; i >= 1; i--) {
    cout << i << " ";
}
```

Đáp án:

```text
5 4 3 2 1
```

---

## Bài 7: Tìm lỗi sai

```cpp
for (int i = 1; i <= 5;) {
    cout << i << endl;
}
```

Lỗi:

```text
Thiếu phần cập nhật i.
```

Sửa đúng:

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}
```

---

## Bài 8: Tìm lỗi sai

```cpp
int tong;

for (int i = 1; i <= 5; i++) {
    tong = tong + i;
}
```

Lỗi:

```text
Biến tong chưa được gán giá trị ban đầu.
```

Sửa đúng:

```cpp
int tong = 0;

for (int i = 1; i <= 5; i++) {
    tong = tong + i;
}
```

---

# 31. Bài tập thực hành

## Bài 1

Viết chương trình in dòng chữ:

```text
Em dang hoc vong lap
```

10 lần.

---

## Bài 2

Viết chương trình nhập `n`, in các số từ `1` đến `n`.

Ví dụ:

```text
Nhap n: 6
1 2 3 4 5 6
```

---

## Bài 3

Viết chương trình nhập `n`, in các số từ `n` về `1`.

Ví dụ:

```text
Nhap n: 5
5 4 3 2 1
```

Gợi ý:

```cpp
for (int i = n; i >= 1; i--) {
    cout << i << " ";
}
```

---

## Bài 4

Viết chương trình in các số chẵn từ `2` đến `50`.

---

## Bài 5

Viết chương trình in các số lẻ từ `1` đến `49`.

---

## Bài 6

Viết chương trình nhập `n`, tính tổng từ `1` đến `n`.

---

## Bài 7

Viết chương trình nhập `n`, tính tổng các số chẵn từ `1` đến `n`.

---

## Bài 8

Viết chương trình nhập một số `n`, in bảng cửu chương của `n`.

---

# 32. Bài tập nâng cao nhẹ

## Bài 1: Tính tổng các số lẻ từ 1 đến n

Đề bài:

```text
Nhập n. Tính tổng các số lẻ từ 1 đến n.
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int tong = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i = i + 2) {
        tong = tong + i;
    }

    cout << "Tong cac so le la: " << tong;

    return 0;
}
```

---

## Bài 2: Đếm số chia hết cho 3 từ 1 đến n

Đề bài:

```text
Nhập n. Đếm có bao nhiêu số chia hết cho 3 từ 1 đến n.
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int dem = 0;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        if (i % 3 == 0) {
            dem = dem + 1;
        }
    }

    cout << "Co " << dem << " so chia het cho 3";

    return 0;
}
```

---

## Bài 3: In các bội của 5 từ 1 đến n

Đề bài:

```text
Nhập n. In các số chia hết cho 5 từ 1 đến n.
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        if (i % 5 == 0) {
            cout << i << " ";
        }
    }

    return 0;
}
```

---

## Bài 4: Tính tích từ 1 đến n

Đề bài:

```text
Nhập n. Tính tích 1 x 2 x 3 x ... x n.
```

Ví dụ:

```text
n = 5
Tích = 1 x 2 x 3 x 4 x 5 = 120
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int tich = 1;

    cout << "Nhap n: ";
    cin >> n;

    for (int i = 1; i <= n; i++) {
        tich = tich * i;
    }

    cout << "Tich la: " << tich;

    return 0;
}
```

Giáo viên lưu ý:

```text
Khi tính tổng, giá trị ban đầu là 0.
Khi tính tích, giá trị ban đầu là 1.
```

---

# 33. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. Vòng lặp dùng để làm gì?
2. Vòng lặp `for` thường dùng khi nào?
3. Trong `for (int i = 1; i <= 10; i++)`, `i` bắt đầu bằng bao nhiêu?
4. Điều kiện dừng là gì?
5. `i++` nghĩa là gì?
6. `i--` nghĩa là gì?
7. Muốn tính tổng từ 1 đến n, biến `tong` ban đầu nên bằng bao nhiêu?
8. Muốn tính tích từ 1 đến n, biến `tich` ban đầu nên bằng bao nhiêu?
9. Điều kiện kiểm tra số chẵn là gì?
10. Muốn in bảng cửu chương của `n`, cần cho `i` chạy từ mấy đến mấy?

Gợi ý trả lời:

```text
1. Dùng để lặp lại một công việc nhiều lần.
2. Khi biết trước số lần lặp hoặc biết khoảng lặp.
3. i bắt đầu bằng 1.
4. i <= 10.
5. Tăng i lên 1.
6. Giảm i đi 1.
7. tong = 0.
8. tich = 1.
9. i % 2 == 0.
10. i chạy từ 1 đến 10.
```

---

# 34. Bài tập về nhà

## Bài 1

Viết chương trình in tên của em 10 lần.

---

## Bài 2

Viết chương trình nhập `n`, in các số từ `1` đến `n`.

---

## Bài 3

Viết chương trình nhập `n`, in các số từ `n` về `1`.

---

## Bài 4

Viết chương trình nhập `n`, tính tổng từ `1` đến `n`.

---

## Bài 5

Viết chương trình nhập `n`, tính tổng các số chẵn từ `1` đến `n`.

---

## Bài 6

Viết chương trình nhập `n`, tính tổng các số lẻ từ `1` đến `n`.

---

## Bài 7

Viết chương trình nhập `n`, in bảng cửu chương của `n`.

---

## Bài 8

Viết chương trình nhập `n`, đếm có bao nhiêu số chia hết cho `3` từ `1` đến `n`.

---

# 35. Tóm tắt bài học

Học sinh cần nhớ:

```text
Vòng lặp dùng để lặp lại một công việc nhiều lần.

Cấu trúc vòng lặp for:

for (khoi_tao; dieu_kien; cap_nhat) {
    // lệnh cần lặp
}

Ví dụ:

for (int i = 1; i <= 10; i++) {
    cout << i << " ";
}

i++ nghĩa là tăng i lên 1.
i-- nghĩa là giảm i đi 1.

Tính tổng:
int tong = 0;
tong = tong + i;

Tính tích:
int tich = 1;
tich = tich * i;
```

Mẫu chương trình cần nhớ:

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

# 36. Gợi ý thời lượng dạy

| Phần                    | Thời lượng |
| ----------------------- | ---------: |
| Ôn bài cũ               |     5 phút |
| Giới thiệu vòng lặp     |    10 phút |
| Cấu trúc vòng lặp `for` |    15 phút |
| In dãy số               |    15 phút |
| Tính tổng từ 1 đến n    |    15 phút |
| Bảng cửu chương         |    15 phút |
| Kết hợp `for` và `if`   |    15 phút |
| Thực hành và sửa lỗi    |    20 phút |
| Củng cố và giao bài tập |     5 phút |

Tổng thời lượng: khoảng **115 phút**.
