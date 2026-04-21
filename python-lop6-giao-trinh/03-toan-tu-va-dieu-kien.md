# Bài 03 - Toán Tử Và Câu Lệnh Điều Kiện

## 1. Mục tiêu bài học

- Dùng được toán tử số học và so sánh.
- Hiểu và viết đúng cấu trúc `if`, `elif`, `else`.
- Giải được các bài toán rẽ nhánh cơ bản.

## 2. Toán tử số học

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3
print(a % b)   # 1
```

## 3. Toán tử so sánh

- `>` lớn hơn
- `<` nhỏ hơn
- `>=` lớn hơn hoặc bằng
- `<=` nhỏ hơn hoặc bằng
- `==` bằng nhau
- `!=` khác nhau

## 4. Toán tử logic

- `and`: cả hai điều kiện cùng đúng.
- `or`: chỉ cần một điều kiện đúng.
- `not`: đảo ngược đúng/sai.

```python
tuoi = 12
print(tuoi >= 10 and tuoi <= 15)  # True
```

## 5. Cấu trúc điều kiện `if`

```python
diem = 8.0

if diem >= 9:
    print("Xuất sắc")
elif diem >= 7:
    print("Khá")
elif diem >= 5:
    print("Trung bình")
else:
    print("Cần cố gắng")
```

## 6. Ví dụ thực tế

### 6.1 Kiểm tra số chẵn/lẻ

```python
n = int(input("Nhập số nguyên: "))

if n % 2 == 0:
    print("Số chẵn")
else:
    print("Số lẻ")
```

### 6.2 So sánh hai số

```python
a = float(input("Nhập a: "))
b = float(input("Nhập b: "))

if a > b:
    print("a lớn hơn b")
elif a < b:
    print("a nhỏ hơn b")
else:
    print("a bằng b")
```

## 7. Lỗi thường gặp

1. Dùng `=` thay vì `==` trong điều kiện.
2. Quên dấu `:` sau `if`.
3. Thụt đầu dòng không đồng nhất.
4. Điều kiện chồng chéo sai thứ tự.

## 8. Mẹo viết điều kiện tốt

- Viết từ trường hợp đặc biệt đến chung.
- Tránh viết điều kiện quá dài trong một dòng.
- Tách thành nhiều biến logic nếu cần.

## 9. Bài tập

### Mức 1

1. Nhập nhiệt độ, in `"Nóng"` nếu > 30, ngược lại in `"Mát"`.
2. Nhập số nguyên, kiểm tra chẵn/lẻ.

### Mức 2

1. Nhập điểm, xếp loại theo 4 mức.
2. Nhập tuổi, kiểm tra có đủ điều kiện tham gia CLB (10-15 tuổi) hay không.

### Mức 3

1. Nhập 3 số, in ra số lớn nhất.
2. Viết chương trình tính tiền vé:
   - Dưới 6 tuổi: miễn phí
   - 6-12 tuổi: 50%
   - Trên 12 tuổi: 100%

## 10. Thử thách mini

Viết chương trình đăng nhập đơn giản:

- Tên đăng nhập đúng là `admin`.
- Mật khẩu đúng là `123456`.
- Nếu sai một trong hai, báo "Đăng nhập thất bại".

## 11. Đáp án tham khảo ngắn

```python
user = input("Tên đăng nhập: ")
pwd = input("Mật khẩu: ")

if user == "admin" and pwd == "123456":
    print("Đăng nhập thành công")
else:
    print("Đăng nhập thất bại")
```

## 12. Checklist

- [ ] Mình dùng được toán tử so sánh.
- [ ] Mình viết đúng `if/elif/else`.
- [ ] Mình phân biệt `=` và `==`.
- [ ] Mình làm được bài xếp loại học lực.
