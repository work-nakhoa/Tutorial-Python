# Bài 11 - Dự Án Tổng Hợp: Quản Lý Điểm Học Sinh

## 1. Mục tiêu

- Tổng hợp toàn bộ kiến thức đã học.
- Xây dựng chương trình có menu và lưu dữ liệu.
- Rèn kỹ năng chia bài toán thành module nhỏ.

## 2. Yêu cầu chức năng

Chương trình cần có:

1. Thêm học sinh.
2. Nhập điểm Toán, Văn, Anh.
3. Tính điểm trung bình.
4. Xếp loại học lực.
5. In danh sách học sinh.
6. Lưu dữ liệu JSON.
7. Đọc dữ liệu từ JSON.

## 3. Thiết kế dữ liệu

Mỗi học sinh:

```python
{
    "ten": "An",
    "toan": 8.0,
    "van": 7.5,
    "anh": 9.0
}
```

Danh sách lớp là `list` chứa nhiều học sinh.

## 4. Thiết kế hàm

```python
def tinh_diem_tb(toan, van, anh):
    return (toan + van + anh) / 3
```

```python
def xep_loai(tb):
    if tb >= 8:
        return "Giỏi"
    if tb >= 6.5:
        return "Khá"
    if tb >= 5:
        return "Trung bình"
    return "Yếu"
```

## 5. Menu mẫu

```text
1. Thêm học sinh
2. Xem danh sách
3. Lưu file JSON
4. Đọc file JSON
5. Thống kê
0. Thoát
```

## 6. Khung chương trình gợi ý

```python
import json

danh_sach = []

while True:
    print("\n=== QUẢN LÝ ĐIỂM ===")
    print("1. Thêm học sinh")
    print("2. Xem danh sách")
    print("3. Lưu JSON")
    print("4. Đọc JSON")
    print("0. Thoát")

    chon = input("Chọn: ")
    if chon == "0":
        break
```

## 7. Tiêu chí hoàn thành dự án

- Chạy ổn định, không crash khi nhập cơ bản.
- Dữ liệu lưu đúng và đọc lại được.
- Code có hàm rõ ràng.
- In kết quả dễ nhìn.

## 8. Nâng cấp khuyến khích

1. Tìm học sinh điểm TB cao nhất.
2. Tìm học sinh theo tên.
3. Sửa điểm và xóa học sinh.
4. In thống kê số học sinh theo xếp loại.

## 9. Bài tập dự án

### Mức 1

1. Hoàn thành chức năng thêm + xem danh sách.

### Mức 2

1. Thêm chức năng lưu/đọc JSON.

### Mức 3

1. Thêm thống kê và tìm kiếm.

## 10. Checklist

- [ ] Có menu hoạt động.
- [ ] Tính đúng điểm trung bình.
- [ ] Xếp loại đúng logic.
- [ ] Lưu và đọc JSON thành công.
- [ ] Có ít nhất 1 chức năng nâng cấp.
