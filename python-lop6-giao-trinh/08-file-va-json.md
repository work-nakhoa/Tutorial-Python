# Bài 08 - Làm Việc Với File Và JSON

## Mục tiêu

- Biết đọc và ghi file văn bản.
- Hiểu JSON là gì và dùng để lưu dữ liệu.
- Biết lưu/đọc dữ liệu học sinh bằng JSON.

## Vì sao cần file?

Nếu chỉ lưu dữ liệu trong biến, tắt chương trình là mất.
File giúp lưu dữ liệu lâu dài để lần sau mở lại.

## Ghi file text

```python
with open("ghi_chu.txt", "w", encoding="utf-8") as f:
    f.write("Hôm nay học Python.\n")
    f.write("Mình đã học về file.\n")
```

Giải thích:

- `"w"`: ghi mới (xóa nội dung cũ nếu có).
- `encoding="utf-8"`: lưu tiếng Việt có dấu.

## Đọc file text

```python
with open("ghi_chu.txt", "r", encoding="utf-8") as f:
    noi_dung = f.read()
    print(noi_dung)
```

## Ghi thêm vào file

```python
with open("ghi_chu.txt", "a", encoding="utf-8") as f:
    f.write("Dòng này được thêm vào cuối file.\n")
```

## JSON là gì?

JSON là định dạng dữ liệu rất phổ biến, dễ đọc, dễ trao đổi.

Ví dụ dữ liệu JSON:

```json
{
  "ten": "Minh",
  "lop": "6A",
  "diem_python": 9
}
```

## Lưu dict vào JSON

```python
import json

du_lieu = {
    "ten": "Minh",
    "lop": "6A",
    "diem_python": 9
}

with open("hoc_sinh.json", "w", encoding="utf-8") as f:
    json.dump(du_lieu, f, ensure_ascii=False, indent=2)
```

## Đọc JSON

```python
import json

with open("hoc_sinh.json", "r", encoding="utf-8") as f:
    data = json.load(f)

print(data["ten"])
```

## Bài tập

1. Tạo file `nhat_ky.txt` và ghi 3 dòng.
2. Đọc lại file vừa tạo và in ra màn hình.
3. Lưu thông tin học sinh vào file JSON.
4. Đọc file JSON và in tên học sinh, lớp.

## Thử thách mini

Tạo danh sách 3 học sinh (list chứa dict), lưu vào `danh_sach_hoc_sinh.json`, rồi đọc lại và in ra theo định dạng đẹp.
