# Bài 01 - Làm Quen Với Python

## Mục tiêu

- Hiểu `print()` để in dữ liệu.
- Biết dùng `input()` để nhận dữ liệu từ bàn phím.
- Biết dùng comment để ghi chú code.

## Kiến thức trọng tâm

### 1. In dữ liệu bằng `print()`

```python
print("Xin chào!")
print(2026)
print("Mình đang học Python.")
```

Bạn có thể in:

- Chuỗi ký tự (đặt trong dấu nháy)
- Số nguyên, số thực
- Kết quả tính toán

### 2. Nhận dữ liệu bằng `input()`

```python
ten = input("Nhập tên của bạn: ")
print("Xin chào", ten)
```

Lưu ý:

- Giá trị từ `input()` luôn là chuỗi.
- Nếu cần số, phải ép kiểu: `int(...)` hoặc `float(...)`.

### 3. Comment để ghi chú

```python
# Đây là comment 1 dòng
print("Học Python vui lắm")
```

Comment giúp:

- Giải thích ý tưởng.
- Ghi việc cần làm.
- Người khác đọc code nhanh hơn.

## Ví dụ tổng hợp

```python
ten = input("Tên bạn là gì? ")
lop = input("Bạn học lớp mấy? ")

print("Chào bạn", ten)
print("Bạn đang học lớp", lop)
```

## Lỗi thường gặp

- Quên đóng dấu nháy.
- Quên dấu `)` trong `print()`.
- Gõ sai tên biến (ví dụ `ten` và `tên`).

## Bài tập

1. In ra 5 dòng bất kỳ về bản thân (tên, tuổi, sở thích...).
2. Viết chương trình nhập tên và in: `Chào mừng <tên> đến với Python!`
3. Viết chương trình nhập tên trường và lớp, sau đó in lại thành 1 câu đầy đủ.

## Thử thách mini

Viết chương trình hỏi:

- Tên
- Môn học yêu thích
- Món ăn yêu thích

Sau đó in: `Bạn <tên> thích môn <môn_học> và thích ăn <món_ăn>.`
