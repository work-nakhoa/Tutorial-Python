# Bài 03 - Toán Tử Và Câu Lệnh Điều Kiện

## Mục tiêu

- Biết dùng toán tử để tính toán.
- Hiểu cách so sánh giá trị.
- Viết được chương trình rẽ nhánh bằng `if`, `elif`, `else`.

## Toán tử số học

```python
a = 10
b = 3

print(a + b)  # 13
print(a - b)  # 7
print(a * b)  # 30
print(a / b)  # 3.333...
print(a % b)  # 1 (phần dư)
print(a // b) # 3 (chia lấy phần nguyên)
```

## Toán tử so sánh

- `>` lớn hơn
- `<` nhỏ hơn
- `>=` lớn hơn hoặc bằng
- `<=` nhỏ hơn hoặc bằng
- `==` bằng nhau
- `!=` khác nhau

## Toán tử logic

- `and`: và
- `or`: hoặc
- `not`: phủ định

```python
tuoi = 12
co_the_thi = tuoi >= 11 and tuoi <= 15
print(co_the_thi)  # True
```

## Câu lệnh điều kiện

```python
diem = 8

if diem >= 9:
    print("Xuất sắc")
elif diem >= 7:
    print("Khá")
else:
    print("Cần cố gắng")
```

## Ví dụ thực tế: kiểm tra số chẵn/lẻ

```python
n = int(input("Nhập một số nguyên: "))

if n % 2 == 0:
    print("Đây là số chẵn")
else:
    print("Đây là số lẻ")
```

## Lỗi thường gặp

- Dùng `=` thay vì `==` trong điều kiện.
- Quên dấu `:` ở cuối dòng `if`, `elif`, `else`.
- Thụt đầu dòng không đúng.

## Bài tập

1. Nhập nhiệt độ, in `"Nóng"` nếu > 30, ngược lại in `"Mát"`.
2. Nhập một số, kiểm tra là số chẵn hay lẻ.
3. Nhập điểm, xếp loại: Giỏi/Khá/Trung bình/Yếu.
4. Nhập 2 số, in số lớn hơn.

## Thử thách mini

Viết chương trình kiểm tra năm nhuận đơn giản:

- Chia hết cho 4 thì tạm coi là năm nhuận.
- Nếu không chia hết cho 4 thì không nhuận.
