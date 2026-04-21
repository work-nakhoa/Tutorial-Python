# Bài 11 - Dự Án Tổng Hợp: Quản Lý Điểm Học Sinh

## Mục tiêu

- Kết hợp kiến thức: biến, hàm, list, dict, vòng lặp, file JSON.
- Tạo một chương trình gần với nhu cầu thực tế.
- Rèn kỹ năng chia bài toán thành các bước nhỏ.

## Yêu cầu dự án

Viết chương trình quản lý điểm có các chức năng:

1. Thêm học sinh.
2. Nhập điểm Toán, Văn, Anh.
3. Tính điểm trung bình.
4. Xếp loại học lực.
5. In danh sách học sinh.
6. Lưu dữ liệu ra file JSON.
7. Đọc dữ liệu từ file JSON khi mở chương trình.

## Thiết kế dữ liệu

Mỗi học sinh là một `dict`:

```python
hoc_sinh = {
    "ten": "An",
    "toan": 8.0,
    "van": 7.5,
    "anh": 9.0
}
```

Toàn bộ lớp là một `list` chứa nhiều học sinh.

## Gợi ý các hàm cần có

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

```python
def in_thong_tin(hs):
    tb = tinh_diem_tb(hs["toan"], hs["van"], hs["anh"])
    loai = xep_loai(tb)
    print(f'{hs["ten"]}: TB={tb:.2f}, Xếp loại={loai}')
```

## Gợi ý menu chương trình

```text
1. Thêm học sinh
2. Xem danh sách
3. Lưu file JSON
4. Đọc file JSON
5. Thoát
```

## Mục tiêu chất lượng

- Chạy ổn định, không lỗi khi nhập sai đơn giản.
- Dữ liệu lưu đúng định dạng JSON.
- Tên hàm và biến rõ nghĩa.

## Nâng cấp thêm (khuyến khích)

- Tìm học sinh điểm trung bình cao nhất.
- Tìm học sinh theo tên.
- Sửa điểm của một học sinh.
- Xóa học sinh khỏi danh sách.

## Thử thách mini

Thêm chức năng thống kê:

- Số học sinh Giỏi, Khá, Trung bình, Yếu.
- Điểm trung bình cả lớp.
