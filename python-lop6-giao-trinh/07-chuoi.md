# Bài 07 - Chuỗi Và Xử Lý Văn Bản Trong Python

## 1. Mục tiêu

- Hiểu chuỗi là gì.
- Biết truy cập ký tự, cắt chuỗi.
- Dùng được các hàm chuỗi phổ biến.
- Làm bài toán xử lý văn bản đơn giản.

## 2. Chuỗi cơ bản

```python
ten = "Nguyen Van A"
print(ten)
```

Chuỗi đặt trong dấu nháy đơn hoặc nháy kép.

## 3. Truy cập ký tự

```python
s = "Python"
print(s[0])   # P
print(s[1])   # y
print(s[-1])  # n
```

## 4. Cắt chuỗi (slicing)

```python
s = "Lap trinh Python"
print(s[0:3])   # Lap
print(s[4:10])  # trinh
print(s[:3])    # Lap
print(s[4:])    # trinh Python
```

## 5. Một số hàm chuỗi quan trọng

```python
s = "  python cơ bản  "
print(s.strip())                 # bỏ khoảng trắng đầu/cuối
print(s.upper())                 # viết hoa
print(s.lower())                 # viết thường
print(s.replace("cơ bản", "nâng cao"))
```

## 6. Tách và nối chuỗi

```python
mon = "Toán,Văn,Anh"
ds = mon.split(",")
print(ds)
```

```python
ho = "Nguyen"
ten = "An"
ho_ten = ho + " " + ten
print(ho_ten)
```

## 7. Kiểm tra trong chuỗi

```python
email = "abc@gmail.com"
if "@" in email:
    print("Email hợp lệ cơ bản")
else:
    print("Email chưa hợp lệ")
```

## 8. Độ dài chuỗi

```python
text = "Python"
print(len(text))  # 6
```

## 9. Lỗi thường gặp

1. Nhầm index bắt đầu từ 1 (thực tế bắt đầu từ 0).
2. Cắt sai biên chuỗi.
3. Quên xử lý khoảng trắng đầu/cuối.

## 10. Bài tập

### Mức 1

1. Nhập họ tên, in ra ký tự đầu tiên.
2. In độ dài chuỗi tên.

### Mức 2

1. Nhập chuỗi, in bản viết hoa và viết thường.
2. Nhập câu có dấu phẩy, tách thành list bằng `split(",")`.

### Mức 3

1. Kiểm tra email có `@` và `.` hay không.
2. Chuẩn hóa họ tên: bỏ khoảng trắng dư đầu/cuối, viết hoa chữ cái đầu mỗi từ.

## 11. Thử thách mini

Viết chương trình tạo username từ họ tên:

- Nhập họ tên.
- Chuẩn hóa chữ thường.
- Bỏ khoảng trắng thừa.
- Đổi khoảng trắng giữa các từ thành dấu `.`.

Ví dụ:

- Input: `  Nguyen   Van  An `
- Output: `nguyen.van.an`

## 12. Checklist

- [ ] Mình truy cập được ký tự theo index.
- [ ] Mình dùng được `strip`, `split`, `replace`.
- [ ] Mình làm được bài kiểm tra email cơ bản.
