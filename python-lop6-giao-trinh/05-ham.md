# Bài 05 - Hàm Trong Python

## 1. Mục tiêu

- Hiểu vì sao cần hàm.
- Viết hàm bằng `def`.
- Dùng tham số và `return`.
- Chia chương trình lớn thành nhiều hàm nhỏ.

## 2. Hàm là gì?

Hàm là một khối lệnh làm một nhiệm vụ cụ thể, có thể gọi lại nhiều lần.

Lợi ích:

- Giảm lặp code.
- Dễ đọc.
- Dễ sửa lỗi.

## 3. Cú pháp cơ bản

```python
def chao():
    print("Xin chào")

chao()
```

## 4. Hàm có tham số

```python
def chao_ten(ten):
    print("Xin chào", ten)

chao_ten("Lan")
chao_ten("Minh")
```

## 5. Hàm trả về kết quả

```python
def tong(a, b):
    return a + b

ket_qua = tong(3, 5)
print(ket_qua)
```

`return` giúp lấy kết quả để dùng tiếp.

## 6. Phân biệt `print()` và `return`

- `print()`: chỉ in ra màn hình.
- `return`: trả giá trị về nơi gọi hàm.

## 7. Ví dụ thực tế

```python
def tinh_diem_tb(toan, van, anh):
    return (toan + van + anh) / 3

def xep_loai(tb):
    if tb >= 8:
        return "Giỏi"
    if tb >= 6.5:
        return "Khá"
    return "Trung bình"

tb = tinh_diem_tb(8, 7.5, 9)
print("Điểm TB:", tb)
print("Xếp loại:", xep_loai(tb))
```

## 8. Phạm vi biến (mức cơ bản)

Biến tạo trong hàm thường chỉ dùng trong hàm.

```python
def vi_du():
    x = 10
    print(x)
```

`x` bên trong hàm không dùng trực tiếp bên ngoài được.

## 9. Lỗi thường gặp

1. Quên dấu `:` sau `def`.
2. Quên thụt đầu dòng trong thân hàm.
3. Gọi hàm thiếu tham số.
4. Trả về sai kiểu dữ liệu so với mục tiêu.

## 10. Bài tập

### Mức 1

1. Viết hàm in lời chào.
2. Viết hàm cộng 2 số.

### Mức 2

1. Viết hàm kiểm tra số chẵn.
2. Viết hàm tính chu vi hình chữ nhật.

### Mức 3

1. Viết hàm tính điểm trung bình 3 môn.
2. Viết hàm xếp loại học lực.
3. Dùng 2 hàm trên để xử lý 1 học sinh.

## 11. Thử thách mini

Viết chương trình quản lý 1 học sinh bằng các hàm:

- `nhap_thong_tin()`
- `tinh_diem_tb()`
- `xep_loai()`
- `in_bao_cao()`

## 12. Đáp án tham khảo ngắn

```python
def la_so_chan(n):
    return n % 2 == 0

print(la_so_chan(8))
```

## 13. Checklist

- [ ] Mình tự viết được hàm có tham số.
- [ ] Mình dùng được `return`.
- [ ] Mình hiểu khác nhau giữa `print` và `return`.
- [ ] Mình chia được một bài toán thành 2-3 hàm nhỏ.
