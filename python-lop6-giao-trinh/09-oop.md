# Bài 09 - Lập Trình Hướng Đối Tượng (OOP)

## Mục tiêu

- Hiểu `class` và `object`.
- Biết tạo thuộc tính và phương thức.
- Biết dùng hàm khởi tạo `__init__`.

## OOP là gì?

OOP giúp mô tả sự vật ngoài đời bằng code.

Ví dụ:

- Học sinh có: tên, lớp, tuổi (thuộc tính).
- Học sinh có thể: giới thiệu bản thân, tính điểm trung bình (phương thức).

## Khái niệm cơ bản

- `class`: bản thiết kế.
- `object`: đối tượng tạo ra từ `class`.
- `self`: đại diện cho chính đối tượng đang làm việc.

## Ví dụ cơ bản

```python
class HocSinh:
    def __init__(self, ten, lop):
        self.ten = ten
        self.lop = lop

    def gioi_thieu(self):
        print(f"Mình là {self.ten}, học lớp {self.lop}.")

hs1 = HocSinh("An", "6A")
hs1.gioi_thieu()
```

## Ví dụ 2: lớp Tài Khoản

```python
class TaiKhoan:
    def __init__(self, chu_tai_khoan, so_du):
        self.chu_tai_khoan = chu_tai_khoan
        self.so_du = so_du

    def nap_tien(self, so_tien):
        self.so_du += so_tien

    def rut_tien(self, so_tien):
        if so_tien <= self.so_du:
            self.so_du -= so_tien
        else:
            print("Không đủ số dư")

    def hien_thi(self):
        print(f"Tài khoản {self.chu_tai_khoan}: {self.so_du} VND")
```

## Lỗi thường gặp

- Quên tham số `self` trong phương thức.
- Gõ sai tên thuộc tính.
- Tạo object nhưng quên truyền đủ dữ liệu vào `__init__`.

## Bài tập

1. Tạo class `Sach` gồm tên sách, tác giả, giá.
2. Tạo class `TaiKhoan` có hàm `nap_tien`, `rut_tien`.
3. Tạo class `HocSinh` có hàm `tinh_diem_trung_binh`.
4. Tạo class `HinhChuNhat` có hàm tính diện tích, chu vi.

## Thử thách mini

Xây dựng class `QuanLyHocSinh` có:

- Danh sách học sinh
- Hàm thêm học sinh
- Hàm in toàn bộ danh sách
- Hàm tìm học sinh có điểm trung bình cao nhất
