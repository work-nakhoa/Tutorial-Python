# Bài 10 - Thuật Toán Cơ Bản Cho Học Sinh Lớp 6

## 1. Mục tiêu

- Hiểu tư duy thuật toán theo từng bước.
- Làm được bài toán tìm kiếm, đếm, sắp xếp cơ bản.
- Biết mô tả thuật toán trước khi code.

## 2. Thuật toán là gì?

Thuật toán là một dãy bước rõ ràng để giải quyết bài toán.

Ví dụ: "Tìm số lớn nhất trong danh sách"

1. Lấy số đầu tiên làm lớn nhất tạm thời.
2. Duyệt các số còn lại.
3. Nếu gặp số lớn hơn thì cập nhật.
4. Kết thúc, in kết quả.

## 3. Tìm max, min

```python
ds = [4, 9, 2, 7, 1]
max_value = ds[0]
min_value = ds[0]

for x in ds:
    if x > max_value:
        max_value = x
    if x < min_value:
        min_value = x

print("Max:", max_value)
print("Min:", min_value)
```

## 4. Tìm kiếm tuyến tính

```python
ds = [10, 20, 30, 40]
can_tim = 30
tim_thay = False

for x in ds:
    if x == can_tim:
        tim_thay = True
        break

print("Tìm thấy:", tim_thay)
```

## 5. Đếm phần tử thỏa điều kiện

```python
ds = [1, 2, 3, 4, 5, 6]
dem_chan = 0

for x in ds:
    if x % 2 == 0:
        dem_chan += 1

print(dem_chan)
```

## 6. Sắp xếp cơ bản

```python
ds = [5, 2, 9, 1]
ds.sort()
print(ds)  # tăng dần

ds.sort(reverse=True)
print(ds)  # giảm dần
```

## 7. Bài toán tổng hợp

```python
diem = [8, 7, 10, 6, 9]
tb = sum(diem) / len(diem)
print("Điểm TB:", round(tb, 2))
print("Cao nhất:", max(diem))
print("Thấp nhất:", min(diem))
```

## 8. Bài tập

### Mức 1

1. Tìm số lớn nhất trong list.
2. Tính tổng các số trong list.

### Mức 2

1. Đếm số chẵn và số lẻ trong list.
2. Kiểm tra một số có tồn tại trong list không.

### Mức 3

1. Nhập danh sách điểm, in max/min/tb.
2. Sắp xếp điểm giảm dần, in top 3 điểm cao nhất.

## 9. Thử thách mini

Viết chương trình phân tích điểm lớp:

- Nhập danh sách điểm.
- In số lượng điểm >= 8.
- In tỷ lệ học sinh đạt khá giỏi.

## 10. Checklist

- [ ] Mình mô tả được thuật toán bằng lời.
- [ ] Mình viết được thuật toán tìm max/min.
- [ ] Mình làm được bài tìm kiếm trong list.
