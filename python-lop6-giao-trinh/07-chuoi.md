# Bài 07 - Chuỗi Và Xử Lý Văn Bản

## Mục tiêu

- Nắm được cách truy cập ký tự trong chuỗi.
- Biết cắt chuỗi, nối chuỗi, tách chuỗi.
- Dùng được các hàm xử lý chuỗi thông dụng.

## Chuỗi là gì?

Chuỗi là một dãy ký tự, ví dụ `"Python"`, `"Lớp 6A"`.

```python
ten = "Nguyen Van A"
print(ten)
```

## Truy cập ký tự và cắt chuỗi

```python
ten = "Nguyen Van A"
print(ten[0])      # N
print(ten[0:6])    # Nguyen
print(ten[-1])     # A
```

## Một số hàm hữu ích

```python
s = "  python cơ bản  "
print(s.strip())                   # bỏ khoảng trắng đầu/cuối
print(s.upper())                   # viết hoa
print(s.lower())                   # viết thường
print(s.replace("cơ bản", "nâng cao"))
```

## Tách và nối chuỗi

```python
mon = "Toán,Văn,Anh"
danh_sach = mon.split(",")
print(danh_sach)
```

```python
ho = "Nguyen"
ten = "An"
ho_ten = ho + " " + ten
print(ho_ten)
```

## Kiểm tra chuỗi

```python
email = "abc@gmail.com"
if "@" in email:
    print("Email hợp lệ cơ bản")
else:
    print("Email chưa đúng")
```

## Bài tập

1. Nhập họ tên, in ra họ tên viết hoa.
2. Đếm số ký tự trong một chuỗi (không tính khoảng trắng đầu cuối).
3. Kiểm tra email có chứa ký tự `@` hay không.
4. Nhập một câu và thay từ `"Python"` thành `"Lập trình Python"`.

## Thử thách mini

Viết chương trình nhập họ và tên riêng, sau đó in:

- Họ tên đầy đủ
- Độ dài họ tên
- Chữ cái đầu tiên của tên riêng
