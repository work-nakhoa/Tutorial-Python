# Bài 04 - Vòng Lặp `for` Và `while`

## Mục tiêu

- Hiểu khi nào dùng `for`, khi nào dùng `while`.
- Biết lặp để giải bài toán tính tổng, in bảng cửu chương.
- Dùng được `break` và `continue`.

## Vì sao cần vòng lặp?

Nếu phải in số từ 1 đến 100 mà viết 100 dòng `print()` thì rất mất thời gian.
Vòng lặp giúp lặp lại công việc tự động.

## Vòng lặp `for`

Dùng khi biết trước số lần lặp.

```python
for i in range(1, 6):
    print("Lần thứ", i)
```

Giải thích:

- `range(1, 6)` tạo dãy: 1, 2, 3, 4, 5.
- Số cuối là 6 nhưng không được lấy.

## Vòng lặp `while`

Dùng khi chưa biết trước số lần lặp, chỉ biết điều kiện dừng.

```python
n = 1
while n <= 5:
    print(n)
    n += 1
```

Lưu ý cực quan trọng:

- Nếu quên `n += 1`, vòng lặp có thể chạy mãi (vòng lặp vô hạn).

## `break` và `continue`

### `break` - thoát vòng lặp ngay

```python
for i in range(1, 10):
    if i == 5:
        break
    print(i)
```

### `continue` - bỏ qua lần lặp hiện tại

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

## Ví dụ: tính tổng từ 1 đến n

```python
n = int(input("Nhập n: "))
tong = 0

for i in range(1, n + 1):
    tong += i

print("Tổng là:", tong)
```

## Bài tập

1. In các số từ 1 đến 20.
2. In các số chẵn từ 2 đến 30.
3. Tính tổng từ 1 đến `n` (nhập từ bàn phím).
4. In bảng cửu chương từ 2 đến 5.

## Thử thách mini

Viết chương trình:

- Nhập mật khẩu.
- Nếu nhập sai quá 3 lần thì dừng và in thông báo.
- Nếu đúng thì in `"Đăng nhập thành công"`.
