# Bài 02 - Biến Và Kiểu Dữ Liệu Trong Python

## 1. Vai trò của bài 02

Bài này giúp học sinh hiểu cách Python lưu dữ liệu và phân biệt các kiểu dữ liệu cơ bản.  
Đây là nền tảng trước khi học điều kiện, vòng lặp, hàm và xử lý dữ liệu.

## 2. Chuẩn đầu ra

Sau bài này, người học cần làm được:

1. Khai báo biến đúng cách.
2. Đặt tên biến rõ nghĩa.
3. Phân biệt `int`, `float`, `str`, `bool`.
4. Dùng `type()` để kiểm tra kiểu dữ liệu.
5. Ép kiểu cơ bản bằng `int()`, `float()`, `str()`, `bool()`.

## 3. Biến là gì?

Biến là "hộp" lưu dữ liệu.

```python
ten = "An"
tuoi = 11
```

- `ten` là tên biến.
- `"An"` là giá trị.

## 4. Quy tắc đặt tên biến

- Dùng chữ thường, không dấu.
- Dùng `_` để ngăn cách từ.
- Không bắt đầu bằng số.
- Không dùng từ khóa (`if`, `for`, `class`, ...).

Ví dụ tốt:

- `ho_ten`
- `diem_toan`
- `nam_sinh`

Ví dụ chưa tốt:

- `a`, `b` (khó hiểu)
- `2ten` (sai)
- `điểm` (dễ lỗi)

## 5. Các kiểu dữ liệu cơ bản

## 5.1 `int` - số nguyên

```python
so_hoc_sinh = 45
```

## 5.2 `float` - số thực

```python
diem_trung_binh = 8.25
```

## 5.3 `str` - chuỗi ký tự

```python
ten_truong = "THCS Nguyễn Du"
```

## 5.4 `bool` - đúng/sai

```python
da_lam_bai_tap = True
```

## 6. Kiểm tra kiểu dữ liệu bằng `type()`

```python
ten = "Minh"
tuoi = 12
diem = 9.5
gioi_tinh_nam = True

print(type(ten))
print(type(tuoi))
print(type(diem))
print(type(gioi_tinh_nam))
```

## 7. Ép kiểu dữ liệu

## 7.1 Từ chuỗi sang số

```python
tuoi_text = "12"
tuoi_so = int(tuoi_text)
print(tuoi_so + 1)  # 13
```

## 7.2 Từ số sang chuỗi

```python
diem = 10
diem_text = str(diem)
print("Điểm của em là " + diem_text)
```

## 7.3 Ép kiểu `float`

```python
chieu_cao_text = "1.45"
chieu_cao = float(chieu_cao_text)
print(chieu_cao + 0.05)
```

## 8. Ví dụ tổng hợp

```python
ten = input("Nhập tên: ")
nam_sinh = int(input("Nhập năm sinh: "))
nam_hien_tai = 2026
tuoi = nam_hien_tai - nam_sinh

print("Xin chào", ten)
print("Năm nay bạn", tuoi, "tuổi")
print("Kiểu dữ liệu của tuổi là:", type(tuoi))
```

## 9. Lỗi thường gặp

1. Gõ sai tên biến.
2. Cộng chuỗi với số mà chưa ép kiểu.
3. Nhập chữ rồi ép `int()` gây `ValueError`.

Ví dụ lỗi:

```python
tuoi = int(input("Nhập tuổi: "))  # nếu nhập "mười hai" sẽ lỗi
```

## 10. Bài tập

### Mức 1

1. Tạo biến lưu tên, tuổi, lớp và in ra.
2. Tạo biến lưu điểm 3 môn (float) và in tổng điểm.

### Mức 2

1. Nhập năm sinh và tính tuổi năm 2026.
2. Nhập chiều cao (mét), cân nặng (kg), in câu giới thiệu.

### Mức 3

1. Nhập 2 số nguyên dưới dạng chuỗi, ép kiểu rồi tính tổng.
2. Nhập điểm 3 môn, tính điểm trung bình (làm tròn 2 chữ số).

## 11. Thử thách mini

Viết chương trình tạo "thẻ thông tin học sinh":

- Tên
- Lớp
- Năm sinh
- Chiều cao
- Sở thích

Yêu cầu:

- Dùng đúng kiểu dữ liệu.
- In đẹp, rõ từng dòng.

## 12. Đáp án tham khảo ngắn

```python
ten = input("Tên: ")
lop = input("Lớp: ")
nam_sinh = int(input("Năm sinh: "))
chieu_cao = float(input("Chiều cao (m): "))

tuoi = 2026 - nam_sinh

print("=== THẺ HỌC SINH ===")
print("Tên:", ten)
print("Lớp:", lop)
print("Tuổi:", tuoi)
print("Chiều cao:", chieu_cao, "m")
```

## 13. Checklist cuối bài

- [ ] Mình hiểu biến là gì.
- [ ] Mình phân biệt được 4 kiểu dữ liệu cơ bản.
- [ ] Mình dùng được `type()`.
- [ ] Mình ép kiểu được dữ liệu nhập từ bàn phím.
- [ ] Mình làm ít nhất 3 bài tập.
