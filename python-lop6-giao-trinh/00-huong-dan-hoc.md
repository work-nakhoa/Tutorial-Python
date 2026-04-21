# Bài 00 - Khởi Động Và Phương Pháp Học Python Đúng Cách

## 1. Bài này dùng để làm gì?

Đây là bài mở đầu của toàn bộ giáo trình.  
Mục tiêu của bài 00 không phải học nhiều cú pháp, mà là:

- Chuẩn bị đúng môi trường học.
- Học đúng phương pháp để đi đường dài.
- Biết tự xử lý lỗi cơ bản ngay từ đầu.

Nếu học sinh nắm chắc bài 00, các bài sau sẽ học nhanh hơn và ít nản hơn.

## 2. Chuẩn đầu ra của bài 00

Sau bài này, người học cần làm được:

1. Mở được trình soạn thảo và terminal.
2. Kiểm tra được Python đã cài đúng.
3. Chạy được file `.py` đầu tiên.
4. Hiểu quy trình học mỗi buổi.
5. Biết đọc lỗi cơ bản và tự sửa từng bước.

## 3. Chuẩn bị trước khi học

### 3.1 Thiết bị và phần mềm

- Máy tính có thể dùng ổn định 30-60 phút/buổi.
- Python 3.x.
- Trình soạn thảo code:
  - Gợi ý 1: VS Code.
  - Gợi ý 2: Thonny (nhẹ, dễ cho học sinh nhỏ tuổi).
- Bàn phím gõ tiếng Anh cơ bản.

### 3.2 Cấu trúc thư mục học tập (khuyên dùng)

Tạo cấu trúc như sau:

```text
python-lop6/
  bai-00/
    hello.py
    ghi-chu.md
  bai-01/
  bai-02/
```

Lợi ích:

- Dễ tìm file.
- Dễ xem tiến độ.
- Mỗi bài tách riêng, tránh rối.

### 3.3 Quy ước đặt tên file và biến

- Tên file dùng chữ thường, không dấu, ngăn cách bằng `_`.
- Ví dụ tốt: `bai_tap_01.py`.
- Ví dụ nên tránh: `Bài tập số 1.py`.

Tên biến cũng tương tự:

- Tốt: `diem_toan`, `ho_ten`.
- Nên tránh: `điểmToán`, `A`, `abcxyz`.

## 4. Kiểm tra cài đặt Python

Mở terminal và chạy:

```bash
python3 --version
```

Nếu hiện dạng `Python 3.x.x` là đạt.

Nếu máy bạn dùng lệnh `python` thay vì `python3`, thử thêm:

```bash
python --version
```

Ghi chú cho giáo viên/phụ huynh:

- Chỉ cần một trong hai lệnh chạy được ổn định là đủ dùng.
- Nên thống nhất một lệnh trên máy học sinh để tránh nhầm.

## 5. Chạy chương trình Python đầu tiên

Tạo file `hello.py`:

```python
print("Xin chào Python!")
print("Mình bắt đầu học lập trình.")
print("Mục tiêu: viết được chương trình nhỏ của riêng mình.")
```

Chạy file:

```bash
python3 hello.py
```

Kết quả mong đợi:

- In ra 3 dòng chữ đúng như trong code.
- Không báo lỗi đỏ ở terminal.

## 6. Quy trình học 1 buổi chuẩn (45-60 phút)

### 6.1 Cấu trúc buổi học

1. 5 phút: ôn bài cũ.
2. 15 phút: học khái niệm mới.
3. 20 phút: gõ ví dụ và tự sửa ví dụ.
4. 10 phút: làm bài tập ngắn.
5. 5-10 phút: tổng kết, ghi lỗi đã gặp.

### 6.2 Quy tắc 70/30

- 30% thời gian đọc/giải thích.
- 70% thời gian gõ code và chạy thật.

Nếu chỉ đọc mà không gõ, tốc độ tiến bộ sẽ rất chậm.

### 6.3 Sổ tay lỗi cá nhân

Mỗi lần gặp lỗi, ghi 3 dòng:

1. Lỗi gì?
2. Vì sao lỗi?
3. Sửa thế nào?

Sau 2-3 tuần, học sinh sẽ thấy lặp lại một số lỗi quen thuộc và sửa rất nhanh.

## 7. Cách đọc lỗi Python (mức cơ bản)

Khi chạy code lỗi, Python thường cho:

- Tên lỗi (ví dụ: `SyntaxError`, `NameError`).
- Số dòng lỗi.
- Gợi ý vị trí lỗi.

Ví dụ lỗi:

```python
print("Hello"
```

Kết quả thường gặp: `SyntaxError` vì thiếu dấu `)`.

### 7.1 6 lỗi phổ biến nhất cho người mới

1. `SyntaxError`: sai cú pháp (thiếu dấu ngoặc, thiếu dấu `:`).
2. `NameError`: dùng biến chưa khai báo hoặc gõ sai tên biến.
3. `IndentationError`: thụt đầu dòng sai.
4. `TypeError`: dùng sai kiểu dữ liệu (ví dụ cộng chuỗi với số).
5. `ValueError`: ép kiểu dữ liệu không hợp lệ.
6. `ModuleNotFoundError`: import thư viện chưa cài.

### 7.2 Quy trình sửa lỗi 4 bước

1. Đọc dòng cuối thông báo lỗi.
2. Nhảy đến đúng số dòng bị báo.
3. Sửa lỗi nhỏ nhất trước (dấu ngoặc, dấu `:`, tên biến).
4. Chạy lại ngay để kiểm tra.

Nguyên tắc:

- Không sửa 10 chỗ cùng lúc.
- Sửa từng lỗi một, chạy lại từng lần một.

## 8. Quy tắc viết code sạch từ ngày đầu

1. Mỗi dòng làm một việc rõ ràng.
2. Đặt tên biến có nghĩa.
3. Dùng comment khi ý tưởng khó hiểu.
4. Không viết code quá dài trong một file nhỏ.
5. Luôn kiểm tra kết quả sau mỗi thay đổi.

Ví dụ comment đúng:

```python
# Tính tổng điểm 3 môn
tong = toan + van + anh
```

Ví dụ comment không cần thiết:

```python
# Gán 5 cho a
a = 5
```

## 9. Mẫu ghi chú sau mỗi bài (dùng lại cho toàn khóa)

Bạn có thể tạo file `ghi_chu.md` với mẫu:

```md
# Ghi chú bài ...

## Mình đã học được gì?
- ...

## Lỗi mình đã gặp
- ...

## Cách mình sửa
- ...

## Mình còn chưa chắc chỗ nào?
- ...
```

Đây là kỹ năng tự học rất quan trọng.

## 10. Bài tập thực hành bài 00

### Mức 1 - Cơ bản

1. Tạo file `gioi_thieu.py`.
2. In 5 dòng:
   - Tên
   - Tuổi
   - Lớp
   - Trường
   - Mục tiêu học Python

### Mức 2 - Có nhập dữ liệu

Viết chương trình:

- Nhập tên.
- Nhập lớp.
- In: `Xin chào <tên>, chúc bạn học tốt ở lớp <lớp>.`

### Mức 3 - Cố tình tạo lỗi rồi sửa

1. Viết một dòng `print` thiếu dấu `)`.
2. Chạy để thấy lỗi.
3. Tự sửa lại.
4. Ghi lỗi và cách sửa vào sổ tay.

## 11. Đáp án tham khảo ngắn cho bài tập

### Bài mức 1

```python
print("Tên: Nguyễn Minh An")
print("Tuổi: 11")
print("Lớp: 6A")
print("Trường: THCS ...")
print("Mục tiêu: Viết được game đơn giản bằng Python")
```

### Bài mức 2

```python
ten = input("Nhập tên: ")
lop = input("Nhập lớp: ")
print("Xin chào", ten + ",", "chúc bạn học tốt ở lớp", lop + ".")
```

## 12. Checklist đánh giá cuối bài 00

Đánh dấu `x` nếu đã làm được:

- [ ] Mình kiểm tra được phiên bản Python.
- [ ] Mình tạo và chạy được file `.py`.
- [ ] Mình hiểu `print()` dùng để làm gì.
- [ ] Mình biết đọc số dòng trong thông báo lỗi.
- [ ] Mình có sổ tay ghi lỗi cá nhân.
- [ ] Mình hoàn thành ít nhất 2 bài tập thực hành.

Nếu còn dưới 4 dấu `x`, nên học lại bài 00 thêm 1 buổi trước khi qua bài 01.

## 13. Nhiệm vụ trước khi sang bài 01

1. Tạo thư mục bài 01.
2. Đảm bảo chạy được `hello.py` không lỗi.
3. Chuẩn bị tinh thần: bài 01 sẽ học nhập/xuất và làm chương trình tương tác đầu tiên.
