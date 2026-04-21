# Bài 04 - Vòng Lặp Trong Python (`for`, `while`)

## 1. Mục tiêu

- Hiểu bản chất vòng lặp.
- Dùng đúng `for` và `while`.
- Biết `break`, `continue`.
- Giải các bài toán lặp phổ biến.

## 2. Khi nào cần vòng lặp?

Khi phải làm lại một công việc nhiều lần:

- In số từ 1 đến 100.
- Tính tổng nhiều số.
- Duyệt từng phần tử trong danh sách.

## 3. Vòng lặp `for`

`for` dùng khi biết trước số lần lặp hoặc duyệt theo dãy.

```python
for i in range(1, 6):
    print("Lần:", i)
```

`range(1, 6)` tạo dãy: 1, 2, 3, 4, 5.

## 4. Vòng lặp `while`

`while` dùng khi lặp theo điều kiện.

```python
n = 1
while n <= 5:
    print(n)
    n += 1
```

Lưu ý:

- Phải cập nhật biến điều kiện (`n += 1`), nếu không sẽ lặp vô hạn.

## 5. `break` và `continue`

### 5.1 `break`

Thoát vòng lặp ngay lập tức.

```python
for i in range(1, 10):
    if i == 5:
        break
    print(i)
```

### 5.2 `continue`

Bỏ qua lần lặp hiện tại.

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

## 6. Ví dụ thực tế

### 6.1 Tính tổng từ 1 đến n

```python
n = int(input("Nhập n: "))
tong = 0

for i in range(1, n + 1):
    tong += i

print("Tổng =", tong)
```

### 6.2 In bảng cửu chương 2

```python
for i in range(1, 11):
    print("2 x", i, "=", 2 * i)
```

### 6.3 Kiểm tra đăng nhập tối đa 3 lần

```python
so_lan = 0
while so_lan < 3:
    mat_khau = input("Nhập mật khẩu: ")
    if mat_khau == "123456":
        print("Đăng nhập thành công")
        break
    so_lan += 1
    print("Sai mật khẩu")

if so_lan == 3:
    print("Bạn đã nhập sai quá 3 lần")
```

## 7. Lỗi thường gặp

1. Quên cập nhật biến trong `while`.
2. Dùng sai biên của `range`.
3. Thụt đầu dòng sai trong thân vòng lặp.
4. Đặt `break` nhầm vị trí.

## 8. Bài tập

### Mức 1

1. In các số từ 1 đến 20.
2. In các số chẵn từ 2 đến 30.

### Mức 2

1. Tính tổng từ 1 đến `n`.
2. Tính giai thừa của `n` (`n!`).

### Mức 3

1. In bảng cửu chương từ 2 đến 9.
2. Đếm số chữ số của một số nguyên dương.

## 9. Thử thách mini

Viết trò chơi đoán số:

- Máy tạo số bí mật từ 1 đến 20.
- Người dùng đoán tối đa 5 lần.
- Báo "lớn hơn" hoặc "nhỏ hơn" sau mỗi lần đoán sai.

## 10. Đáp án tham khảo ngắn

```python
tong = 0
for i in range(1, 101):
    tong += i
print(tong)
```

## 11. Checklist cuối bài

- [ ] Mình phân biệt được `for` và `while`.
- [ ] Mình dùng được `break`, `continue`.
- [ ] Mình viết được bài tính tổng từ 1 đến n.
- [ ] Mình làm ít nhất 3 bài tập.
