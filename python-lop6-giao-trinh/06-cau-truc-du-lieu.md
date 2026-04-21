# Bài 06 - Cấu Trúc Dữ Liệu: List, Tuple, Dict, Set

## Mục tiêu

- Phân biệt được 4 cấu trúc dữ liệu phổ biến.
- Biết khi nào dùng loại nào.
- Thực hiện thao tác thêm, sửa, xóa cơ bản.

## 1. List (Danh sách)

- Có thứ tự.
- Có thể thay đổi.
- Cho phép trùng lặp.

```python
mon_hoc = ["Toán", "Văn", "Anh"]
mon_hoc.append("Tin")
mon_hoc[0] = "Toán nâng cao"
print(mon_hoc)
```

## 2. Tuple (Bộ giá trị)

- Có thứ tự.
- Không thể thay đổi sau khi tạo.

```python
toa_do = (10, 20)
print(toa_do[0])  # 10
```

Dùng khi dữ liệu cố định, ví dụ tọa độ, ngày tháng không muốn sửa.

## 3. Dict (Từ điển)

- Dữ liệu dạng cặp `khóa: giá trị`.
- Truy cập nhanh theo khóa.

```python
hoc_sinh = {
    "ten": "Lan",
    "tuoi": 11,
    "lop": "6A"
}

print(hoc_sinh["ten"])
hoc_sinh["tuoi"] = 12
print(hoc_sinh)
```

## 4. Set (Tập hợp)

- Không có thứ tự cố định.
- Không chứa phần tử trùng.

```python
so = {1, 2, 2, 3}
print(so)  # {1, 2, 3}
```

## So sánh nhanh

- `list`: danh sách có thứ tự, sửa được.
- `tuple`: có thứ tự, không sửa được.
- `dict`: quản lý theo khóa.
- `set`: loại bỏ trùng lặp.

## Bài tập

1. Tạo list 5 món ăn yêu thích, in món thứ 2.
2. Thêm 1 món mới vào list.
3. Tạo dict thông tin 1 cuốn sách (tên, tác giả, giá).
4. Từ list `[1, 1, 2, 2, 3, 3, 4]`, dùng set để xóa trùng.

## Thử thách mini

Tạo danh sách 3 học sinh bằng `list` chứa `dict`, rồi in:

- Tên từng học sinh
- Điểm trung bình từng học sinh
