# Bài 01 - Làm Quen Với Python: In, Nhập Dữ Liệu, Biến, Comment

## 1. Vai trò của bài 01

Bài 01 là bài thực hành nền tảng đầu tiên của khóa học.  
Sau bài này, học sinh cần tự viết được chương trình tương tác đơn giản:

- Máy hỏi.
- Người dùng nhập.
- Chương trình in kết quả theo dữ liệu vừa nhập.

Đây là bước đầu để sang bài biến, kiểu dữ liệu và điều kiện.

## 2. Chuẩn đầu ra của bài 01

Sau khi học xong bài này, người học cần làm được:

1. Dùng `print()` để in chữ, số, biểu thức.
2. Dùng `input()` để lấy dữ liệu từ bàn phím.
3. Lưu dữ liệu nhập vào biến.
4. Dùng comment để ghi chú.
5. Tự viết chương trình "giới thiệu bản thân" có tương tác.

## 3. Kiến thức trọng tâm

## 3.1 Hàm `print()` - In dữ liệu ra màn hình

`print()` là lệnh xuất thông tin.

Ví dụ:

```python
print("Xin chào Python!")
print(2026)
print(2 + 3)
```

Kết quả:

- Dòng 1 in chuỗi.
- Dòng 2 in số.
- Dòng 3 in kết quả phép tính.

### 3.1.1 In nhiều giá trị cùng lúc

```python
ten = "Minh"
tuoi = 11
print("Tên:", ten, "- Tuổi:", tuoi)
```

### 3.1.2 Tham số `sep` và `end`

```python
print("Toán", "Văn", "Anh", sep=" | ")
print("Xin chào", end=" - ")
print("Mình là học sinh lớp 6")
```

Giải thích:

- `sep` là ký tự ngăn cách giữa các phần in.
- `end` là ký tự kết thúc sau mỗi lệnh `print`.

## 3.2 Hàm `input()` - Nhận dữ liệu từ người dùng

`input()` giúp chương trình "trò chuyện" với người dùng.

```python
ten = input("Nhập tên của bạn: ")
print("Xin chào", ten)
```

Lưu ý quan trọng:

- Dữ liệu nhận từ `input()` mặc định là chuỗi (`str`).
- Nếu nhập số để tính toán, cần ép kiểu (học kỹ ở bài 02).

Ví dụ sai thường gặp:

```python
tuoi = input("Nhập tuổi: ")
print(tuoi + 1)  # lỗi vì tuoi là chuỗi
```

Ví dụ đúng:

```python
tuoi = int(input("Nhập tuổi: "))
print(tuoi + 1)
```

## 3.3 Biến là nơi lưu dữ liệu

Biến giúp lưu thông tin để dùng lại.

```python
ten = "Lan"
lop = "6A"
print(ten, lop)
```

Nguyên tắc đặt tên biến:

- Không dấu, dễ hiểu.
- Không bắt đầu bằng số.
- Không đặt trùng từ khóa Python.

Ví dụ tốt:

- `ho_ten`
- `lop_hoc`
- `mon_yeu_thich`

Ví dụ nên tránh:

- `a`, `x1x2x3`
- `tên`, `lớp`

## 3.4 Comment - Ghi chú trong code

Comment giúp giải thích ý tưởng:

```python
# Đây là chương trình hỏi tên và lớp
ten = input("Tên bạn là gì? ")
lop = input("Bạn học lớp mấy? ")
print("Xin chào", ten, "lớp", lop)
```

Nên dùng comment khi:

- Ý tưởng khó.
- Cần nhắc việc chưa làm.
- Muốn người khác đọc hiểu nhanh.

## 4. Quy trình viết một chương trình nhỏ

Ví dụ bài toán:
"Hỏi tên và tuổi, rồi in lời chào."

Thực hiện theo 4 bước:

1. Xác định cần nhập gì.
2. Tạo biến nhận dữ liệu bằng `input()`.
3. Xử lý (nếu có).
4. In kết quả bằng `print()`.

Code:

```python
ten = input("Nhập tên: ")
tuoi = input("Nhập tuổi: ")
print("Xin chào", ten)
print("Năm nay bạn", tuoi, "tuổi.")
```

## 5. Ví dụ mẫu có giải thích kỹ

## Ví dụ 1 - Hồ sơ học sinh mini

```python
print("=== TẠO HỒ SƠ HỌC SINH ===")
ten = input("Nhập tên: ")
lop = input("Nhập lớp: ")
truong = input("Nhập tên trường: ")
so_thich = input("Nhập sở thích: ")

print("\n=== THÔNG TIN CỦA BẠN ===")
print("Tên:", ten)
print("Lớp:", lop)
print("Trường:", truong)
print("Sở thích:", so_thich)
```

Điểm hay của ví dụ:

- Có tiêu đề để chương trình dễ nhìn.
- Dùng biến rõ nghĩa.
- Dùng `\n` để xuống dòng tạo bố cục.

## Ví dụ 2 - Lời chào tùy biến

```python
ten = input("Tên bạn: ")
mon = input("Môn học bạn thích nhất: ")
print("Chào", ten + "!")
print("Thật tuyệt vì bạn thích môn", mon + ".")
```

## 6. Lỗi thường gặp và cách sửa

## 6.1 Quên dấu ngoặc đóng

Sai:

```python
print("Xin chào"
```

Sửa:

```python
print("Xin chào")
```

## 6.2 Quên dấu nháy

Sai:

```python
print("Hello)
```

Sửa:

```python
print("Hello")
```

## 6.3 Gõ sai tên biến

Sai:

```python
ten = input("Tên: ")
print(tên)  # sai vì khác ký tự
```

Sửa:

```python
ten = input("Tên: ")
print(ten)
```

## 6.4 Cộng chuỗi với số sai kiểu

Sai:

```python
tuoi = input("Tuổi: ")
print("Tuổi năm sau: " + tuoi + 1)
```

Sửa:

```python
tuoi = int(input("Tuổi: "))
print("Tuổi năm sau:", tuoi + 1)
```

## 7. Bài tập luyện tập theo cấp độ

## Mức 1 - Cơ bản

1. In 5 dòng giới thiệu bản thân.
2. In một câu động lực học tập bạn yêu thích.
3. In phép tính `7 + 8`, `9 * 6`.

## Mức 2 - Có tương tác

1. Nhập tên, in: `Chào mừng <tên> đến với lớp Python.`
2. Nhập tên trường và lớp, in thành một câu đầy đủ.
3. Nhập tên bạn thân, in lời chúc học tốt.

## Mức 3 - Tăng độ khó nhẹ

1. Nhập tên, tuổi, sở thích, in thành "thẻ thông tin".
2. Nhập năm sinh, in tuổi dự kiến vào năm 2026.
3. In menu đơn giản:
   - 1. Xem thông tin
   - 2. Cập nhật thông tin
   - 3. Thoát

## 8. Thử thách mini cuối bài

Viết chương trình "Phỏng vấn nhanh học sinh":

- Hỏi 5 thông tin:
  - Tên
  - Lớp
  - Trường
  - Môn học yêu thích
  - Ước mơ
- In báo cáo ngắn 5-6 dòng cho đẹp.
- Có tiêu đề đầu và cuối báo cáo.

Gợi ý định dạng:

```text
===== BÁO CÁO HỌC SINH =====
Tên: ...
Lớp: ...
...
===== KẾT THÚC =====
```

## 9. Đáp án tham khảo ngắn

### Bài mức 2, câu 1

```python
ten = input("Nhập tên: ")
print("Chào mừng", ten, "đến với lớp Python.")
```

### Bài mức 3, câu 1

```python
ten = input("Nhập tên: ")
tuoi = input("Nhập tuổi: ")
so_thich = input("Nhập sở thích: ")

print("=== THẺ THÔNG TIN ===")
print("Tên:", ten)
print("Tuổi:", tuoi)
print("Sở thích:", so_thich)
```

## 10. Tự đánh giá cuối bài

Đánh dấu `x` nếu bạn đã làm được:

- [ ] Mình biết dùng `print()` để in nhiều dạng dữ liệu.
- [ ] Mình biết dùng `input()` để nhận dữ liệu.
- [ ] Mình tạo được biến và dùng lại biến.
- [ ] Mình biết comment là gì.
- [ ] Mình đã làm ít nhất 3 bài tập.
- [ ] Mình tự sửa được ít nhất 1 lỗi khi chạy code.

Nếu còn dưới 4 dấu `x`, nên làm lại bài này thêm 1 buổi trước khi học bài 02.

## 11. Nhiệm vụ trước khi sang bài 02

1. Tạo file `bai_01_tong_hop.py` chứa chương trình phỏng vấn nhanh.
2. Chạy chương trình ít nhất 2 lần với dữ liệu khác nhau.
3. Ghi vào sổ tay 2 lỗi đã gặp và cách sửa.
