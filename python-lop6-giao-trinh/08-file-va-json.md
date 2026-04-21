# Bài 08 - Làm Việc Với File Và JSON

## 1. Mục tiêu

- Đọc và ghi file text.
- Hiểu chế độ mở file (`r`, `w`, `a`).
- Lưu và đọc dữ liệu JSON bằng Python.

## 2. Vì sao cần lưu file?

Nếu chỉ lưu trong biến, khi tắt chương trình dữ liệu sẽ mất.  
Lưu file giúp:

- Giữ dữ liệu lâu dài.
- Mở lại ở lần chạy sau.
- Chia sẻ dữ liệu với chương trình khác.

## 3. Đọc và ghi file text

## 3.1 Ghi mới file (`w`)

```python
with open("nhat_ky.txt", "w", encoding="utf-8") as f:
    f.write("Hôm nay học Python.\n")
    f.write("Mình đã học về file.\n")
```

## 3.2 Đọc file (`r`)

```python
with open("nhat_ky.txt", "r", encoding="utf-8") as f:
    noi_dung = f.read()
    print(noi_dung)
```

## 3.3 Ghi nối tiếp (`a`)

```python
with open("nhat_ky.txt", "a", encoding="utf-8") as f:
    f.write("Dòng này được thêm vào cuối file.\n")
```

## 4. JSON là gì?

JSON là định dạng dữ liệu dạng văn bản, rất phổ biến.

Ví dụ JSON:

```json
{
  "ten": "An",
  "lop": "6A",
  "diem": 8.5
}
```

## 5. Làm việc với JSON trong Python

## 5.1 Ghi JSON

```python
import json

hoc_sinh = {
    "ten": "An",
    "lop": "6A",
    "diem": 8.5
}

with open("hoc_sinh.json", "w", encoding="utf-8") as f:
    json.dump(hoc_sinh, f, ensure_ascii=False, indent=2)
```

## 5.2 Đọc JSON

```python
import json

with open("hoc_sinh.json", "r", encoding="utf-8") as f:
    data = json.load(f)

print(data["ten"])
```

## 6. Ví dụ tổng hợp

```python
import json

danh_sach = [
    {"ten": "An", "toan": 8.0},
    {"ten": "Bình", "toan": 7.5}
]

with open("diem_toan.json", "w", encoding="utf-8") as f:
    json.dump(danh_sach, f, ensure_ascii=False, indent=2)

with open("diem_toan.json", "r", encoding="utf-8") as f:
    ds_doc = json.load(f)

for hs in ds_doc:
    print(hs["ten"], hs["toan"])
```

## 7. Lỗi thường gặp

1. Quên `encoding="utf-8"` khi có tiếng Việt.
2. Mở sai chế độ file (`r` khi file chưa tồn tại).
3. JSON sai cấu trúc do sửa tay không đúng.

## 8. Bài tập

### Mức 1

1. Tạo file `ghi_chu.txt`, ghi 3 dòng.
2. Đọc lại file và in ra màn hình.

### Mức 2

1. Lưu thông tin 1 học sinh vào `hoc_sinh.json`.
2. Đọc JSON và in lại thông tin.

### Mức 3

1. Lưu list 5 học sinh vào JSON.
2. Đọc file và in học sinh có điểm cao nhất.

## 9. Thử thách mini

Xây dựng chương trình "Sổ điểm mini":

- Nhập nhiều học sinh.
- Lưu ra `so_diem.json`.
- Mở lại và in báo cáo danh sách điểm.

## 10. Checklist

- [ ] Mình đọc/ghi được file text.
- [ ] Mình hiểu khác nhau giữa `w` và `a`.
- [ ] Mình lưu/đọc được dữ liệu JSON.
- [ ] Mình làm được bài lưu danh sách học sinh.
