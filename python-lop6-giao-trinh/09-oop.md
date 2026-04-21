# Bài 09 - Lập Trình Hướng Đối Tượng (OOP)

## 1. Mục tiêu

- Hiểu `class` và `object`.
- Tạo thuộc tính, phương thức.
- Dùng `__init__` để khởi tạo dữ liệu.
- Áp dụng OOP vào bài toán quản lý đơn giản.

## 2. Khái niệm cơ bản

- `class`: bản thiết kế.
- `object`: đối tượng tạo từ class.
- `self`: đại diện cho đối tượng hiện tại.

## 3. Ví dụ đầu tiên

```python
class HocSinh:
    def __init__(self, ten, lop):
        self.ten = ten
        self.lop = lop

    def gioi_thieu(self):
        print(f"Mình là {self.ten}, học lớp {self.lop}")

hs1 = HocSinh("An", "6A")
hs1.gioi_thieu()
```

## 4. Thuộc tính và phương thức

- Thuộc tính: dữ liệu của object (`ten`, `lop`).
- Phương thức: hành động của object (`gioi_thieu`).

## 5. Ví dụ thực tế: Tài khoản

```python
class TaiKhoan:
    def __init__(self, chu_tai_khoan, so_du=0):
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
        print(f"{self.chu_tai_khoan}: {self.so_du} VND")
```

## 6. Lỗi thường gặp

1. Quên `self` trong định nghĩa phương thức.
2. Gọi phương thức sai tên.
3. Truy cập thuộc tính chưa tồn tại.

## 7. Bài tập

### Mức 1

1. Tạo class `Sach` có thuộc tính tên, tác giả, giá.
2. Viết phương thức in thông tin sách.

### Mức 2

1. Tạo class `HocSinh` có điểm 3 môn.
2. Viết phương thức tính điểm trung bình.

### Mức 3

1. Tạo class `QuanLyHocSinh` chứa list học sinh.
2. Có phương thức thêm học sinh, in danh sách, tìm điểm cao nhất.

## 8. Thử thách mini

Làm chương trình quản lý thư viện mini:

- Thêm sách.
- Hiển thị sách.
- Tìm sách theo tên.

## 9. Checklist

- [ ] Mình hiểu class/object.
- [ ] Mình dùng được `__init__`.
- [ ] Mình viết được ít nhất 1 class có 2 phương thức.
