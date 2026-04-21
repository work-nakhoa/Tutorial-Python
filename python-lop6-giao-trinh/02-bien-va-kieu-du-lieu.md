# Bài 02 - Biến Và Kiểu Dữ Liệu

## Mục tiêu

- Hiểu biến là gì và cách đặt tên biến.
- Nắm 4 kiểu dữ liệu cơ bản: `int`, `float`, `str`, `bool`.
- Biết ép kiểu dữ liệu cơ bản.

## Biến là gì?

Biến giống như một chiếc hộp để lưu thông tin.
Mỗi biến có:

- Tên biến
- Giá trị
- Kiểu dữ liệu

```python
ten = "An"
tuoi = 11
diem_toan = 8.5
hoc_gioi = True
```

## Quy tắc đặt tên biến

- Nên dùng chữ thường và dấu gạch dưới: `diem_toan`.
- Không bắt đầu bằng số.
- Không dùng từ khóa Python như `if`, `for`, `class`.
- Đặt tên dễ hiểu, không quá ngắn kiểu `a`, `b` (trừ ví dụ đơn giản).

## Các kiểu dữ liệu cơ bản

```python
so_nguyen = 25          # int
so_thuc = 3.14          # float
chuoi = "Python"        # str
dung_sai = False        # bool
```

## Kiểm tra kiểu dữ liệu

```python
print(type(so_nguyen))
print(type(so_thuc))
print(type(chuoi))
print(type(dung_sai))
```

## Ép kiểu dữ liệu

```python
tuoi_text = "12"
tuoi_so = int(tuoi_text)
print(tuoi_so + 1)  # 13
```

```python
diem = 8
diem_text = str(diem)
print("Điểm của bạn là " + diem_text)
```

## Lỗi thường gặp

```python
# Sai: cộng chuỗi với số
# print("Tuổi của bạn là " + 12)

# Đúng:
print("Tuổi của bạn là", 12)
print("Tuổi của bạn là " + str(12))
```

## Bài tập

1. Tạo biến lưu tên trường, lớp, số bạn thân.
2. Nhập năm sinh, tính tuổi hiện tại (giả sử năm hiện tại là 2026).
3. Nhập điểm 3 môn (Toán, Văn, Anh) dạng `float`, in ra từng kiểu dữ liệu.

## Thử thách mini

Viết chương trình nhập:

- Tên
- Năm sinh
- Chiều cao (mét)

Sau đó in một câu đầy đủ, ví dụ:
`Bạn Minh sinh năm 2014, cao 1.45m.`
