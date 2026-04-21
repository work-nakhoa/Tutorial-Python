# Bài 10 - Thuật Toán Cơ Bản

## Mục tiêu

- Hiểu thuật toán là gì.
- Biết cách giải bài toán theo từng bước.
- Làm quen với tìm kiếm và sắp xếp cơ bản.

## Thuật toán là gì?

Thuật toán là một chuỗi bước rõ ràng để giải quyết một vấn đề.

Ví dụ bài toán:

- Tìm số lớn nhất trong danh sách.
- Tìm một số có tồn tại trong danh sách hay không.
- Sắp xếp danh sách điểm tăng dần/giảm dần.

## 1. Tìm giá trị lớn nhất trong list

```python
ds = [4, 9, 2, 7, 1]
max_value = ds[0]

for x in ds:
    if x > max_value:
        max_value = x

print(max_value)
```

Ý tưởng:

1. Tạm coi phần tử đầu là lớn nhất.
2. Duyệt lần lượt các phần tử còn lại.
3. Nếu thấy số lớn hơn thì cập nhật.

## 2. Tìm kiếm tuyến tính

```python
ds = [10, 20, 30, 40]
can_tim = 30
tim_thay = False

for x in ds:
    if x == can_tim:
        tim_thay = True
        break

print(tim_thay)
```

## 3. Sắp xếp đơn giản

```python
ds = [5, 2, 9, 1]
ds.sort()
print(ds)  # [1, 2, 5, 9]
```

Sắp xếp giảm dần:

```python
ds.sort(reverse=True)
print(ds)
```

## Bài tập

1. Tìm số nhỏ nhất trong list.
2. Kiểm tra một số có nằm trong list hay không.
3. Sắp xếp list điểm theo thứ tự giảm dần.
4. Đếm xem trong list có bao nhiêu số chẵn.

## Thử thách mini

Nhập một danh sách điểm từ bàn phím, sau đó:

- In điểm cao nhất
- In điểm thấp nhất
- In điểm trung bình
- In danh sách đã sắp xếp tăng dần
