# Bài 19: Dự án nhỏ 3 — Quản lý điểm học sinh đơn giản

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Ôn lại biến, mảng, vòng lặp, điều kiện.
* Biết nhập điểm của nhiều học sinh.
* Biết tính điểm trung bình của lớp.
* Biết tìm điểm cao nhất, thấp nhất.
* Biết đếm số học sinh đạt.
* Biết viết một chương trình nhỏ có nhiều chức năng.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Mảng dùng để làm gì?
2. Mảng `diem[5]` có các chỉ số nào?
3. Muốn duyệt mảng `n` phần tử, vòng lặp viết thế nào?
4. Muốn tính tổng các phần tử trong mảng, biến `tong` ban đầu bằng bao nhiêu?
5. Muốn tìm số lớn nhất trong mảng, nên gán `max` ban đầu bằng gì?

Gợi ý trả lời:

```text
1. Mảng dùng để lưu nhiều giá trị cùng kiểu dữ liệu.
2. diem[0], diem[1], diem[2], diem[3], diem[4].
3. for (int i = 0; i < n; i++)
4. tong = 0.
5. max = a[0].
```

Dẫn vào bài mới:

> Hôm nay chúng ta sẽ làm một dự án nhỏ: **quản lý điểm học sinh**.
> Chương trình sẽ nhập điểm của nhiều học sinh, sau đó tính điểm trung bình, tìm điểm cao nhất và đếm số bạn đạt.

---

# 3. Ý tưởng dự án

Chương trình cần làm các việc sau:

```text
1. Nhập số lượng học sinh.
2. Nhập điểm từng học sinh.
3. In lại danh sách điểm.
4. Tính điểm trung bình.
5. Tìm điểm cao nhất.
6. Tìm điểm thấp nhất.
7. Đếm số học sinh đạt.
```

Ví dụ chạy chương trình:

```text
Nhap so hoc sinh: 4
Nhap diem hoc sinh thu 1: 8
Nhap diem hoc sinh thu 2: 6.5
Nhap diem hoc sinh thu 3: 4
Nhap diem hoc sinh thu 4: 9

===== KET QUA =====
Diem trung binh: 6.875
Diem cao nhat: 9
Diem thap nhat: 4
So hoc sinh dat: 3
```

Quy ước:

```text
Học sinh đạt nếu điểm >= 5.
```

---

# 4. Kiến thức cần dùng

| Kiến thức         | Dùng để làm gì?              |
| ----------------- | ---------------------------- |
| `float`           | Lưu điểm số                  |
| Mảng              | Lưu điểm của nhiều học sinh  |
| `for`             | Nhập và duyệt danh sách điểm |
| `if`              | Kiểm tra điểm đạt            |
| Biến `tong`       | Tính tổng điểm               |
| Biến `max`, `min` | Tìm điểm cao nhất, thấp nhất |
| Biến `demDat`     | Đếm số học sinh đạt          |

---

# 5. Phân tích bài toán

## Đề bài

Viết chương trình nhập điểm của `n` học sinh. Sau đó in ra điểm trung bình, điểm cao nhất, điểm thấp nhất và số học sinh đạt.

## Phân tích

```text
Đầu vào:
- n
- điểm của n học sinh

Xử lý:
- Dùng mảng diem để lưu điểm
- Tính tổng điểm
- Điểm trung bình = tổng điểm / n
- Tìm điểm cao nhất
- Tìm điểm thấp nhất
- Đếm số điểm >= 5

Đầu ra:
- Điểm trung bình
- Điểm cao nhất
- Điểm thấp nhất
- Số học sinh đạt
```

---

# 6. Bước 1: Nhập số lượng học sinh

Ta cần biến `n` để lưu số học sinh.

```cpp
int n;

cout << "Nhap so hoc sinh: ";
cin >> n;
```

Chương trình ban đầu:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "Nhap so hoc sinh: ";
    cin >> n;

    return 0;
}
```

---

# 7. Bước 2: Khai báo mảng điểm

Vì điểm có thể là số thập phân, ta dùng `float`.

```cpp
float diem[100];
```

Mảng này có thể lưu tối đa 100 điểm.

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    float diem[100];

    cout << "Nhap so hoc sinh: ";
    cin >> n;

    return 0;
}
```

Lưu ý:

> Trong bài này, học sinh nên nhập `n` từ 1 đến 100.

---

# 8. Bước 3: Nhập điểm từng học sinh

Ta dùng vòng lặp `for`.

```cpp
for (int i = 0; i < n; i++) {
    cout << "Nhap diem hoc sinh thu " << i + 1 << ": ";
    cin >> diem[i];
}
```

Giải thích:

```text
i chạy từ 0 đến n - 1.
diem[i] là điểm của học sinh thứ i + 1.
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    float diem[100];

    cout << "Nhap so hoc sinh: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap diem hoc sinh thu " << i + 1 << ": ";
        cin >> diem[i];
    }

    return 0;
}
```

---

# 9. Bước 4: In lại danh sách điểm

Sau khi nhập, ta có thể in lại điểm để kiểm tra.

```cpp
cout << "Danh sach diem: ";

for (int i = 0; i < n; i++) {
    cout << diem[i] << " ";
}
```

Chương trình:

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    float diem[100];

    cout << "Nhap so hoc sinh: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap diem hoc sinh thu " << i + 1 << ": ";
        cin >> diem[i];
    }

    cout << "Danh sach diem: ";

    for (int i = 0; i < n; i++) {
        cout << diem[i] << " ";
    }

    return 0;
}
```

---

# 10. Bước 5: Tính điểm trung bình

Cần tạo biến:

```cpp
float tong = 0;
float trungBinh;
```

Sau đó cộng tất cả điểm vào `tong`.

```cpp
for (int i = 0; i < n; i++) {
    tong = tong + diem[i];
}

trungBinh = tong / n;
```

Chương trình mẫu:

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

    cout << "Diem trung binh: " << trungBinh;

    return 0;
}
```

---

# 11. Bước 6: Tìm điểm cao nhất

Cách làm:

```text
1. Gán diemCaoNhat = diem[0].
2. Duyệt từ học sinh thứ 2 đến hết.
3. Nếu diem[i] > diemCaoNhat thì cập nhật diemCaoNhat.
```

Code:

```cpp
float diemCaoNhat = diem[0];

for (int i = 1; i < n; i++) {
    if (diem[i] > diemCaoNhat) {
        diemCaoNhat = diem[i];
    }
}
```

Ví dụ:

```text
Danh sách điểm: 7, 9, 5, 8
Ban đầu diemCaoNhat = 7
Gặp 9 lớn hơn 7 → diemCaoNhat = 9
Gặp 5 không lớn hơn 9 → giữ nguyên
Gặp 8 không lớn hơn 9 → giữ nguyên
Kết quả: 9
```

---

# 12. Bước 7: Tìm điểm thấp nhất

Tương tự điểm cao nhất.

```cpp
float diemThapNhat = diem[0];

for (int i = 1; i < n; i++) {
    if (diem[i] < diemThapNhat) {
        diemThapNhat = diem[i];
    }
}
```

---

# 13. Bước 8: Đếm số học sinh đạt

Quy ước:

```text
Học sinh đạt nếu điểm >= 5.
```

Ta tạo biến đếm:

```cpp
int demDat = 0;
```

Sau đó duyệt mảng:

```cpp
for (int i = 0; i < n; i++) {
    if (diem[i] >= 5) {
        demDat = demDat + 1;
    }
}
```

---

# 14. Chương trình hoàn chỉnh

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    float diem[100];

    float tong = 0;
    float trungBinh;
    float diemCaoNhat;
    float diemThapNhat;
    int demDat = 0;

    cout << "Nhap so hoc sinh: ";
    cin >> n;

    for (int i = 0; i < n; i++) {
        cout << "Nhap diem hoc sinh thu " << i + 1 << ": ";
        cin >> diem[i];
    }

    cout << endl;
    cout << "Danh sach diem: ";
    for (int i = 0; i < n; i++) {
        cout << diem[i] << " ";
    }

    for (int i = 0; i < n; i++) {
        tong = tong + diem[i];
    }

    trungBinh = tong / n;

    diemCaoNhat = diem[0];
    diemThapNhat = diem[0];

    for (int i = 1; i < n; i++) {
        if (diem[i] > diemCaoNhat) {
            diemCaoNhat = diem[i];
        }

        if (diem[i] < diemThapNhat) {
            diemThapNhat = diem[i];
        }
    }

    for (int i = 0; i < n; i++) {
        if (diem[i] >= 5) {
            demDat = demDat + 1;
        }
    }

    cout << endl;
    cout << endl;
    cout << "===== KET QUA =====" << endl;
    cout << "Diem trung binh: " << trungBinh << endl;
    cout << "Diem cao nhat: " << diemCaoNhat << endl;
    cout << "Diem thap nhat: " << diemThapNhat << endl;
    cout << "So hoc sinh dat: " << demDat << endl;

    return 0;
}
```

Ví dụ chạy:

```text
Nhap so hoc sinh: 4
Nhap diem hoc sinh thu 1: 8
Nhap diem hoc sinh thu 2: 6.5
Nhap diem hoc sinh thu 3: 4
Nhap diem hoc sinh thu 4: 9

Danh sach diem: 8 6.5 4 9

===== KET QUA =====
Diem trung binh: 6.875
Diem cao nhat: 9
Diem thap nhat: 4
So hoc sinh dat: 3
```

---

# 15. Phiên bản có kiểm tra điểm hợp lệ

Điểm hợp lệ là điểm từ `0` đến `10`.

Khi nhập điểm, nếu học sinh nhập sai, yêu cầu nhập lại.

```cpp
for (int i = 0; i < n; i++) {
    cout << "Nhap diem hoc sinh thu " << i + 1 << ": ";
    cin >> diem[i];

    while (diem[i] < 0 || diem[i] > 10) {
        cout << "Diem khong hop le. Nhap lai: ";
        cin >> diem[i];
    }
}
```

Có thể thay phần nhập điểm trong chương trình hoàn chỉnh bằng đoạn trên.

Giải thích:

```text
Nếu điểm nhỏ hơn 0 hoặc lớn hơn 10 thì bắt nhập lại.
Khi điểm hợp lệ, chương trình mới tiếp tục.
```

---

# 16. Phiên bản nâng cao: Đếm học sinh giỏi, khá, đạt, chưa đạt

Quy ước đơn giản:

```text
Giỏi: điểm >= 8
Khá: điểm >= 6.5 và < 8
Đạt: điểm >= 5 và < 6.5
Chưa đạt: điểm < 5
```

Code xử lý:

```cpp
int demGioi = 0;
int demKha = 0;
int demDat = 0;
int demChuaDat = 0;

for (int i = 0; i < n; i++) {
    if (diem[i] >= 8) {
        demGioi = demGioi + 1;
    } else if (diem[i] >= 6.5) {
        demKha = demKha + 1;
    } else if (diem[i] >= 5) {
        demDat = demDat + 1;
    } else {
        demChuaDat = demChuaDat + 1;
    }
}
```

In kết quả:

```cpp
cout << "So hoc sinh gioi: " << demGioi << endl;
cout << "So hoc sinh kha: " << demKha << endl;
cout << "So hoc sinh dat: " << demDat << endl;
cout << "So hoc sinh chua dat: " << demChuaDat << endl;
```

---

# 17. Lỗi thường gặp

## Lỗi 1: Nhập sai chỉ số mảng

Sai:

```cpp
for (int i = 1; i <= n; i++) {
    cin >> diem[i];
}
```

Đúng:

```cpp
for (int i = 0; i < n; i++) {
    cin >> diem[i];
}
```

Vì mảng trong C++ bắt đầu từ chỉ số `0`.

---

## Lỗi 2: Quên khởi tạo biến tổng

Sai:

```cpp
float tong;
```

Đúng:

```cpp
float tong = 0;
```

---

## Lỗi 3: Tìm điểm cao nhất nhưng gán bằng 0

Sai:

```cpp
float diemCaoNhat = 0;
```

Không nên làm vậy, vì cách tốt nhất là lấy điểm đầu tiên làm giá trị ban đầu.

Đúng:

```cpp
float diemCaoNhat = diem[0];
```

---

## Lỗi 4: Quên kiểm tra `n`

Nếu `n = 0`, chương trình không có học sinh nào để tính điểm trung bình hoặc tìm điểm cao nhất.

Ở mức cơ bản, giáo viên nhắc:

```text
Khi chạy chương trình, nhập n lớn hơn 0.
```

Có thể kiểm tra:

```cpp
if (n <= 0) {
    cout << "So hoc sinh khong hop le";
    return 0;
}
```

---

## Lỗi 5: Chia sai khi tính trung bình

Sai:

```cpp
trungBinh = tong;
```

Đúng:

```cpp
trungBinh = tong / n;
```

---

# 18. Hoạt động trên lớp

## Hoạt động 1: Phân tích dự án

Yêu cầu học sinh điền:

```text
Đầu vào:
- ...

Xử lý:
- ...

Đầu ra:
- ...
```

Đáp án gợi ý:

```text
Đầu vào:
- số học sinh n
- điểm của từng học sinh

Xử lý:
- nhập điểm vào mảng
- tính tổng điểm
- tính điểm trung bình
- tìm điểm cao nhất
- tìm điểm thấp nhất
- đếm số học sinh đạt

Đầu ra:
- danh sách điểm
- điểm trung bình
- điểm cao nhất
- điểm thấp nhất
- số học sinh đạt
```

---

## Hoạt động 2: Viết phần nhập điểm

Yêu cầu học sinh viết đoạn code nhập điểm của `n` học sinh.

Gợi ý:

```cpp
for (int i = 0; i < n; i++) {
    cout << "Nhap diem hoc sinh thu " << i + 1 << ": ";
    cin >> diem[i];
}
```

---

## Hoạt động 3: Viết phần tính trung bình

Gợi ý:

```cpp
float tong = 0;
float trungBinh;

for (int i = 0; i < n; i++) {
    tong = tong + diem[i];
}

trungBinh = tong / n;
```

---

## Hoạt động 4: Viết phần đếm học sinh đạt

Gợi ý:

```cpp
int demDat = 0;

for (int i = 0; i < n; i++) {
    if (diem[i] >= 5) {
        demDat = demDat + 1;
    }
}
```

---

# 19. Bài tập trên lớp

## Bài 1

Viết chương trình nhập điểm của `n` học sinh và in lại danh sách điểm.

---

## Bài 2

Viết chương trình nhập điểm của `n` học sinh và tính điểm trung bình.

---

## Bài 3

Viết chương trình nhập điểm của `n` học sinh và tìm điểm cao nhất.

---

## Bài 4

Viết chương trình nhập điểm của `n` học sinh và đếm số học sinh đạt.

Quy ước:

```text
Đạt nếu điểm >= 5.
```

---

## Bài 5

Ghép các bài trên thành một chương trình hoàn chỉnh.

Chương trình cần in:

```text
Diem trung binh
Diem cao nhat
Diem thap nhat
So hoc sinh dat
```

---

# 20. Bài tập thực hành nâng cao

## Bài 1: Kiểm tra điểm hợp lệ

Khi nhập điểm, nếu điểm nhỏ hơn `0` hoặc lớn hơn `10`, yêu cầu nhập lại.

Gợi ý:

```cpp
while (diem[i] < 0 || diem[i] > 10) {
    cout << "Diem khong hop le. Nhap lai: ";
    cin >> diem[i];
}
```

---

## Bài 2: Đếm học sinh chưa đạt

Đếm số học sinh có điểm nhỏ hơn `5`.

Gợi ý:

```cpp
if (diem[i] < 5) {
    demChuaDat = demChuaDat + 1;
}
```

---

## Bài 3: Đếm học sinh giỏi

Đếm số học sinh có điểm lớn hơn hoặc bằng `8`.

Gợi ý:

```cpp
if (diem[i] >= 8) {
    demGioi = demGioi + 1;
}
```

---

## Bài 4: Xếp loại cả lớp

Đếm số học sinh theo nhóm:

```text
Giỏi: >= 8
Khá: >= 6.5
Đạt: >= 5
Chưa đạt: < 5
```

---

# 21. Câu hỏi củng cố

Giáo viên hỏi học sinh:

1. Vì sao dự án này cần dùng mảng?
2. Vì sao điểm nên dùng kiểu `float`?
3. Muốn tính điểm trung bình cần những bước nào?
4. Muốn tìm điểm cao nhất, ban đầu nên gán `diemCaoNhat` bằng gì?
5. Muốn đếm học sinh đạt, điều kiện là gì?
6. Vì sao cần kiểm tra điểm hợp lệ?
7. Nếu nhập `n = 0` thì có vấn đề gì?

Gợi ý trả lời:

```text
1. Vì cần lưu điểm của nhiều học sinh.
2. Vì điểm có thể là số thập phân như 7.5, 8.25.
3. Tính tổng điểm rồi chia cho số học sinh.
4. Gán bằng diem[0].
5. diem[i] >= 5.
6. Vì điểm phải nằm trong khoảng 0 đến 10.
7. Không có dữ liệu để tính trung bình hoặc tìm điểm cao nhất.
```

---

# 22. Bài tập về nhà

## Bài 1

Viết chương trình nhập điểm của `n` học sinh và in lại danh sách điểm.

## Bài 2

Viết chương trình nhập điểm của `n` học sinh và tính điểm trung bình.

## Bài 3

Viết chương trình nhập điểm của `n` học sinh và tìm điểm cao nhất, thấp nhất.

## Bài 4

Viết chương trình nhập điểm của `n` học sinh và đếm:

```text
Số học sinh đạt
Số học sinh chưa đạt
```

## Bài 5

Viết chương trình quản lý điểm hoàn chỉnh gồm:

```text
- Nhập số học sinh
- Nhập điểm từng học sinh
- In danh sách điểm
- Tính điểm trung bình
- Tìm điểm cao nhất
- Tìm điểm thấp nhất
- Đếm học sinh đạt
- Đếm học sinh chưa đạt
```

---

# 23. Tóm tắt bài học

Học sinh cần nhớ:

```text
Dự án quản lý điểm dùng:

- Mảng để lưu điểm nhiều học sinh
- Vòng lặp để nhập và xử lý điểm
- Biến tong để tính tổng điểm
- trungBinh = tong / n
- diemCaoNhat = diem[0]
- diemThapNhat = diem[0]
- if để đếm học sinh đạt hoặc chưa đạt
```

Mẫu quan trọng:

```cpp
for (int i = 0; i < n; i++) {
    tong = tong + diem[i];

    if (diem[i] >= 5) {
        demDat = demDat + 1;
    }
}
```

Tìm điểm cao nhất:

```cpp
float diemCaoNhat = diem[0];

for (int i = 1; i < n; i++) {
    if (diem[i] > diemCaoNhat) {
        diemCaoNhat = diem[i];
    }
}
```

---

# 24. Gợi ý thời lượng dạy 60 phút

| Phần                             | Thời lượng |
| -------------------------------- | ---------: |
| Ôn bài cũ                        |     5 phút |
| Giới thiệu dự án quản lý điểm    |     5 phút |
| Phân tích đầu vào, xử lý, đầu ra |     7 phút |
| Viết phần nhập và in điểm        |    10 phút |
| Tính trung bình                  |    10 phút |
| Tìm cao nhất, thấp nhất          |    10 phút |
| Đếm học sinh đạt                 |     8 phút |
| Củng cố và giao bài tập          |     5 phút |

Tổng: **60 phút**.
