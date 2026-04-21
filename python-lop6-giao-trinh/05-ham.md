# Bài 05 - Hàm Trong Python

## Mục tiêu

- Hiểu hàm là gì và lợi ích của hàm.
- Biết tạo hàm bằng `def`.
- Biết truyền tham số và nhận kết quả bằng `return`.

## Hàm là gì?

Hàm là một nhóm lệnh để làm một việc cụ thể.
Khi cần, ta gọi hàm thay vì viết lại code nhiều lần.

Lợi ích:

- Code ngắn gọn hơn.
- Dễ đọc và dễ sửa.
- Tái sử dụng nhiều lần.

## Tạo hàm đơn giản

```python
def chao():
    print("Xin chào!")

chao()
```

## Hàm có tham số

```python
def chao_ten(ten):
    print("Xin chào", ten)

chao_ten("Minh")
chao_ten("Lan")
```

## Hàm trả về kết quả

```python
def tong(a, b):
    return a + b

ket_qua = tong(3, 4)
print(ket_qua)
```

Nếu không dùng `return`, hàm chỉ in ra chứ không trả về dữ liệu để dùng tiếp.

## Ví dụ thực tế

```python
def tinh_diem_trung_binh(toan, van, anh):
    return (toan + van + anh) / 3

tb = tinh_diem_trung_binh(8, 7.5, 9)
print("Điểm trung bình:", tb)
```

## Lỗi thường gặp

- Quên dấu `:` sau `def`.
- Quên thụt đầu dòng trong thân hàm.
- Gọi hàm thiếu tham số.
- Nhầm giữa `print()` và `return`.

## Bài tập

1. Viết hàm tính chu vi hình chữ nhật.
2. Viết hàm kiểm tra số chẵn.
3. Viết hàm tính điểm trung bình 3 môn.
4. Viết hàm đổi từ độ C sang độ F.

## Thử thách mini

Viết chương trình có các hàm:

- `nhap_thong_tin_hoc_sinh()`
- `tinh_diem_trung_binh(...)`
- `xep_loai(...)`

Sau đó in kết quả xếp loại cho một học sinh.
