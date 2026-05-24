# Bài 1: Lập trình là gì?

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Hiểu lập trình là gì.
* Biết chương trình máy tính là gì.
* Biết máy tính chỉ làm theo lệnh.
* Hiểu lập trình viên là người viết lệnh cho máy tính.
* Nhận biết một số ví dụ lập trình trong đời sống.
* Viết được chương trình C++ đầu tiên ở mức quan sát, chưa cần hiểu hết cú pháp.

---

# 2. Mở đầu bài học

Giáo viên hỏi học sinh:

> Các em có dùng điện thoại, máy tính, tivi thông minh hoặc robot hút bụi không?

Sau đó hỏi tiếp:

> Khi em bấm nút mở YouTube, vì sao điện thoại biết phải mở YouTube?
> Khi em chơi game, vì sao nhân vật biết chạy, nhảy, bắn?
> Khi em bấm máy tính tính `5 + 3`, vì sao máy tính biết kết quả là `8`?

Giải thích:

Máy tính không tự thông minh như con người. Máy tính làm được việc vì có người viết sẵn các **lệnh** cho nó.

Những lệnh đó được gọi là **chương trình**.

Việc viết các lệnh đó được gọi là **lập trình**.

---

# 3. Lập trình là gì?

## Khái niệm đơn giản

**Lập trình** là việc viết các câu lệnh để yêu cầu máy tính làm một công việc nào đó.

Ví dụ trong đời sống:

Khi mẹ bảo em:

```text
1. Lấy ly
2. Rót nước
3. Uống nước
```

Đây là một dãy hướng dẫn.

Trong lập trình cũng tương tự, ta viết các bước để máy tính làm theo.

Ví dụ:

```text
1. Nhập hai số
2. Cộng hai số đó
3. In kết quả ra màn hình
```

Đó chính là tư duy lập trình.

---

# 4. Máy tính có hiểu tiếng Việt không?

Máy tính không hiểu tiếng Việt như con người.

Nếu ta nói:

```text
Máy tính ơi, hãy cộng 2 số giúp tôi.
```

Máy tính không tự hiểu được.

Ta phải dùng một **ngôn ngữ lập trình** để viết lệnh.

Ví dụ trong C++:

```cpp
cout << 5 + 3;
```

Lệnh này yêu cầu máy tính in ra kết quả của phép tính `5 + 3`.

---

# 5. Ngôn ngữ lập trình là gì?

**Ngôn ngữ lập trình** là ngôn ngữ dùng để giao tiếp với máy tính.

Một số ngôn ngữ lập trình phổ biến:

| Ngôn ngữ   | Thường dùng để làm gì?              |
| ---------- | ----------------------------------- |
| C          | Lập trình hệ thống, nhúng, thiết bị |
| C++        | Học thuật toán, game, phần mềm      |
| Python     | AI, dữ liệu, tự động hóa            |
| JavaScript | Làm website                         |
| Java       | Ứng dụng, hệ thống lớn              |

Trong khóa học này, chúng ta học **C++ cơ bản**.

---

# 6. Vì sao học C++?

C++ là ngôn ngữ rất tốt để học tư duy lập trình.

Lý do:

* Giúp hiểu rõ cách máy tính xử lý lệnh.
* Phù hợp để học thuật toán.
* Dùng nhiều trong các kỳ thi lập trình.
* Có thể viết chương trình đơn giản, game nhỏ, bài toán tính toán.

Tuy nhiên, ở lớp 6, chúng ta chỉ học phần cơ bản, chưa học phần khó như con trỏ, bộ nhớ, hướng đối tượng phức tạp.

---

# 7. Chương trình máy tính là gì?

**Chương trình máy tính** là tập hợp nhiều câu lệnh được viết theo một thứ tự nhất định.

Ví dụ chương trình pha mì:

```text
1. Đun nước
2. Bóc gói mì
3. Cho mì vào tô
4. Đổ nước sôi
5. Chờ 3 phút
6. Ăn mì
```

Nếu làm sai thứ tự thì có thể không ra kết quả đúng.

Ví dụ:

```text
1. Ăn mì
2. Đổ nước sôi
3. Bóc gói mì
```

Thứ tự này sai.

Trong lập trình cũng vậy, máy tính sẽ chạy lệnh theo thứ tự từ trên xuống dưới.

---

# 8. Ví dụ chương trình C++ đầu tiên

Giáo viên cho học sinh xem chương trình sau:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao lop 6!";
    return 0;
}
```

Kết quả khi chạy:

```text
Xin chao lop 6!
```

Ở bài này, học sinh chưa cần hiểu hết từng dòng.

Chỉ cần hiểu:

| Dòng lệnh              | Ý nghĩa đơn giản                     |
| ---------------------- | ------------------------------------ |
| `#include <iostream>`  | Cho phép chương trình in ra màn hình |
| `using namespace std;` | Giúp viết lệnh ngắn hơn              |
| `int main()`           | Nơi chương trình bắt đầu chạy        |
| `cout`                 | Lệnh in ra màn hình                  |
| `return 0;`            | Kết thúc chương trình                |

Giáo viên nhấn mạnh:

> Hôm nay các em chỉ cần nhớ: `cout` dùng để in nội dung ra màn hình.

---

# 9. Giải thích bằng ví dụ dễ hiểu

Câu lệnh:

```cpp
cout << "Xin chao lop 6!";
```

Nghĩa là:

```text
Hãy in dòng chữ: Xin chao lop 6!
```

Nếu đổi thành:

```cpp
cout << "Toi dang hoc lap trinh";
```

Thì màn hình sẽ hiện:

```text
Toi dang hoc lap trinh
```

---

# 10. Hoạt động trên lớp

## Hoạt động 1: Máy tính làm theo lệnh

Giáo viên chọn một học sinh đóng vai “máy tính”.

Giáo viên ra lệnh:

```text
Đứng lên
Bước sang trái 1 bước
Giơ tay phải
Ngồi xuống
```

Sau đó hỏi cả lớp:

> Bạn ấy có tự làm việc khác ngoài lệnh không?

Kết luận:

Máy tính cũng vậy. Máy tính chỉ làm đúng những gì được lập trình.

---

## Hoạt động 2: Viết lệnh bằng lời

Yêu cầu học sinh viết các bước để làm một việc quen thuộc.

Ví dụ:

**Đánh răng**

```text
1. Lấy bàn chải
2. Lấy kem đánh răng
3. Làm ướt bàn chải
4. Đánh răng
5. Súc miệng
```

Sau đó giáo viên nói:

> Đây chính là cách suy nghĩ của lập trình viên: chia việc lớn thành nhiều bước nhỏ.

---

# 11. Bài tập trên lớp

## Bài 1

Sắp xếp các bước sau cho đúng để “mở máy tính và vào học lập trình”:

```text
A. Mở phần mềm lập trình
B. Bật máy tính
C. Viết chương trình
D. Chạy chương trình
```

---

## Bài 2

Em hãy viết các bước để máy tính tính tổng hai số.

Gợi ý đáp án:

```text
1. Nhập số thứ nhất
2. Nhập số thứ hai
3. Cộng hai số
4. In kết quả
```

---

## Bài 3

Quan sát chương trình sau và đoán kết quả:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Em thich hoc lap trinh";
    return 0;
}
```

Đáp án:

```text
Em thich hoc lap trinh
```

---

# 12. Bài tập thực hành

Học sinh sửa dòng chữ trong chương trình mẫu.

Chương trình mẫu:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Xin chao!";
    return 0;
}
```

Yêu cầu 1:

Đổi nội dung thành tên của em.

Ví dụ:

```cpp
cout << "Xin chao, em ten la Nam";
```

Yêu cầu 2:

In ra lớp của em.

Ví dụ:

```cpp
cout << "Em hoc lop 6A";
```

Yêu cầu 3:

In ra sở thích của em.

Ví dụ:

```cpp
cout << "Em thich choi bong da";
```

---

# 13. Lỗi thường gặp

## Lỗi 1: Quên dấu chấm phẩy

Sai:

```cpp
cout << "Xin chao"
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích:

Trong C++, nhiều câu lệnh phải kết thúc bằng dấu `;`.

---

## Lỗi 2: Quên dấu ngoặc kép

Sai:

```cpp
cout << Xin chao;
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích:

Khi in chữ, phải đặt chữ trong dấu ngoặc kép `" "`.

---

## Lỗi 3: Gõ sai chữ `cout`

Sai:

```cpp
count << "Xin chao";
```

Đúng:

```cpp
cout << "Xin chao";
```

Giải thích:

Máy tính rất nghiêm khắc. Gõ sai một chữ cũng có thể làm chương trình lỗi.

---

# 14. Câu hỏi củng cố cuối bài

Giáo viên hỏi:

1. Lập trình là gì?
2. Chương trình máy tính là gì?
3. Máy tính có tự hiểu ý muốn của con người không?
4. `cout` dùng để làm gì?
5. Vì sao cần viết lệnh đúng thứ tự?

Gợi ý trả lời:

1. Lập trình là viết lệnh cho máy tính.
2. Chương trình là tập hợp các câu lệnh.
3. Không, máy tính chỉ làm theo lệnh.
4. `cout` dùng để in ra màn hình.
5. Vì máy tính chạy lệnh theo thứ tự, sai thứ tự có thể sai kết quả.

---

# 16. Tóm tắt bài học

Trong bài học này, học sinh cần nhớ:

```text
Lập trình = viết lệnh cho máy tính
Chương trình = nhiều câu lệnh ghép lại
Máy tính = chỉ làm đúng theo lệnh
C++ = một ngôn ngữ lập trình
cout = lệnh in ra màn hình
```

---

# 17. Gợi ý thời lượng dạy

| Phần                        | Thời lượng |
| --------------------------- | ---------: |
| Mở đầu, đặt câu hỏi         |     5 phút |
| Giải thích lập trình là gì  |    10 phút |
| Ví dụ chương trình đầu tiên |    10 phút |
| Hoạt động đóng vai máy tính |    10 phút |
| Bài tập trên lớp            |    10 phút |
| Củng cố, giao bài tập       |     5 phút |

Tổng thời lượng: khoảng **45–50 phút**.
