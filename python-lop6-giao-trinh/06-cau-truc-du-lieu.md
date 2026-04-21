# Bài 06 - Cấu Trúc Dữ Liệu Cơ Bản: List, Tuple, Dict, Set

## 1. Mục tiêu

- Phân biệt 4 cấu trúc dữ liệu phổ biến.
- Chọn đúng cấu trúc theo bài toán.
- Thực hiện thêm/sửa/xóa/truy cập dữ liệu.

## 2. Tổng quan

Python có nhiều cách lưu dữ liệu. 4 loại quan trọng nhất ở mức cơ bản:

1. `list` - danh sách có thứ tự, sửa được.
2. `tuple` - danh sách có thứ tự, không sửa được.
3. `dict` - dữ liệu dạng khóa:giá trị.
4. `set` - tập hợp, không trùng lặp.

## 3. List

```python
mon_hoc = ["Toán", "Văn", "Anh"]
print(mon_hoc[0])     # Toán
mon_hoc.append("Tin")
mon_hoc[1] = "Ngữ văn"
print(mon_hoc)
```

Các thao tác hay dùng:

- `append()` thêm cuối.
- `insert()` chèn theo vị trí.
- `remove()` xóa theo giá trị.
- `pop()` xóa theo vị trí.
- `len()` lấy độ dài.

## 4. Tuple

```python
toa_do = (10, 20)
print(toa_do[0])
```

Tuple thường dùng cho dữ liệu cố định:

- Ngày tháng.
- Tọa độ.
- Cặp giá trị không muốn thay đổi.

## 5. Dictionary (Dict)

```python
hoc_sinh = {
    "ten": "Lan",
    "lop": "6A",
    "diem_toan": 8.5
}

print(hoc_sinh["ten"])
hoc_sinh["diem_toan"] = 9.0
hoc_sinh["truong"] = "THCS ABC"
print(hoc_sinh)
```

## 6. Set

```python
ds = [1, 1, 2, 2, 3, 4]
tap = set(ds)
print(tap)  # {1, 2, 3, 4}
```

Set dùng tốt khi:

- Cần loại phần tử trùng.
- Cần kiểm tra tồn tại nhanh.

## 7. Ví dụ tổng hợp

```python
danh_sach_hoc_sinh = [
    {"ten": "An", "diem": 8.0},
    {"ten": "Bình", "diem": 7.5},
    {"ten": "Chi", "diem": 9.0}
]

for hs in danh_sach_hoc_sinh:
    print(hs["ten"], "-", hs["diem"])
```

## 8. Lỗi thường gặp

1. Truy cập index vượt quá độ dài list.
2. Truy cập dict bằng khóa không tồn tại.
3. Nhầm giữa `list` và `dict`.

## 9. Bài tập

### Mức 1

1. Tạo list 5 môn học yêu thích.
2. In phần tử đầu và cuối của list.

### Mức 2

1. Tạo dict thông tin 1 cuốn sách.
2. Cập nhật giá sách mới rồi in lại.

### Mức 3

1. Tạo list chứa 3 dict học sinh (tên + điểm).
2. In học sinh có điểm cao nhất.
3. Từ list số có trùng, dùng set để loại trùng.

## 10. Thử thách mini

Tạo chương trình quản lý danh sách việc cần làm (`todo`):

- Thêm việc.
- Xóa việc.
- In toàn bộ việc.

Gợi ý: dùng `list` để lưu các công việc.

## 11. Checklist

- [ ] Mình phân biệt rõ list/tuple/dict/set.
- [ ] Mình thao tác được với từng kiểu.
- [ ] Mình chọn đúng kiểu dữ liệu cho bài toán đơn giản.
