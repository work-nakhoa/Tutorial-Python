# Bài 7: Bài tập ứng dụng phép toán

## 1. Mục tiêu bài học

Sau bài học này, học sinh có thể:

* Biết áp dụng phép toán vào bài toán thực tế.
* Biết phân tích bài toán thành: đầu vào, xử lý, đầu ra.
* Biết chuyển công thức toán học thành code C++.
* Viết được chương trình đổi đơn vị đơn giản.
* Viết được chương trình tính tiền, tính tuổi, tính chu vi, diện tích.
* Biết kiểm tra kết quả bằng ví dụ nhỏ.

---

# 2. Ôn lại bài cũ

Giáo viên hỏi học sinh:

1. Trong C++, phép cộng dùng ký hiệu gì?
2. Phép nhân dùng ký hiệu gì?
3. Phép chia dùng ký hiệu gì?
4. Phép `%` dùng để làm gì?
5. Kết quả của `10 % 3` là bao nhiêu?
6. Vì sao công thức chu vi hình chữ nhật cần viết `(dai + rong) * 2`?

Gợi ý trả lời:

```text
1. Phép cộng dùng dấu +
2. Phép nhân dùng dấu *
3. Phép chia dùng dấu /
4. Phép % dùng để lấy số dư
5. 10 % 3 = 1
6. Vì cần cộng dài và rộng trước, rồi mới nhân 2
```

Giáo viên dẫn vào bài mới:

> Ở bài trước, chúng ta đã học các phép toán trong C++.
> Hôm nay, chúng ta sẽ dùng các phép toán đó để giải những bài toán gần gũi trong đời sống.

---

# 3. Khi gặp bài toán lập trình, cần làm gì?

Khi gặp một bài toán, học sinh không nên viết code ngay.

Trước tiên cần suy nghĩ theo 3 phần:

```text
1. Đầu vào: Cần nhập dữ liệu gì?
2. Xử lý: Cần tính toán như thế nào?
3. Đầu ra: Cần in kết quả gì?
```

Ví dụ bài toán:

```text
Nhập chiều dài và chiều rộng hình chữ nhật. Tính diện tích.
```

Phân tích:

```text
Đầu vào:
- chiều dài
- chiều rộng

Xử lý:
- diện tích = chiều dài * chiều rộng

Đầu ra:
- diện tích hình chữ nhật
```

Code:

```cpp
#include <iostream>
using namespace std;

int main() {
    int dai, rong;
    int dienTich;

    cout << "Nhap chieu dai: ";
    cin >> dai;

    cout << "Nhap chieu rong: ";
    cin >> rong;

    dienTich = dai * rong;

    cout << "Dien tich la: " << dienTich;

    return 0;
}
```

---

# 4. Mẫu phân tích bài toán

Giáo viên cho học sinh ghi nhớ mẫu sau:

```text
Bài toán: ...

Đầu vào:
- ...

Xử lý:
- ...

Đầu ra:
- ...
```

Ví dụ:

```text
Bài toán: Nhập số giờ, đổi sang số phút.

Đầu vào:
- số giờ

Xử lý:
- số phút = số giờ * 60

Đầu ra:
- số phút
```

---

# 5. Bài toán 1: Đổi km sang m

## Đề bài

Nhập số kilomet, đổi sang mét.

Biết rằng:

```text
1 km = 1000 m
```

## Phân tích

```text
Đầu vào:
- soKm

Xử lý:
- soMet = soKm * 1000

Đầu ra:
- soMet
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int soKm;
    int soMet;

    cout << "Nhap so km: ";
    cin >> soKm;

    soMet = soKm * 1000;

    cout << soKm << " km = " << soMet << " m";

    return 0;
}
```

## Ví dụ chạy chương trình

```text
Nhap so km: 3
3 km = 3000 m
```

---

# 6. Bài toán 2: Đổi m sang cm

## Đề bài

Nhập số mét, đổi sang centimet.

Biết rằng:

```text
1 m = 100 cm
```

## Phân tích

```text
Đầu vào:
- soMet

Xử lý:
- soCm = soMet * 100

Đầu ra:
- soCm
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int soMet;
    int soCm;

    cout << "Nhap so met: ";
    cin >> soMet;

    soCm = soMet * 100;

    cout << soMet << " m = " << soCm << " cm";

    return 0;
}
```

## Ví dụ

```text
Nhap so met: 5
5 m = 500 cm
```

---

# 7. Bài toán 3: Đổi giờ sang phút

## Đề bài

Nhập số giờ, đổi sang số phút.

Biết rằng:

```text
1 giờ = 60 phút
```

## Phân tích

```text
Đầu vào:
- gio

Xử lý:
- phut = gio * 60

Đầu ra:
- phut
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int gio;
    int phut;

    cout << "Nhap so gio: ";
    cin >> gio;

    phut = gio * 60;

    cout << gio << " gio = " << phut << " phut";

    return 0;
}
```

## Ví dụ

```text
Nhap so gio: 2
2 gio = 120 phut
```

---

# 8. Bài toán 4: Đổi phút sang giây

## Đề bài

Nhập số phút, đổi sang số giây.

Biết rằng:

```text
1 phút = 60 giây
```

## Phân tích

```text
Đầu vào:
- phut

Xử lý:
- giay = phut * 60

Đầu ra:
- giay
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int phut;
    int giay;

    cout << "Nhap so phut: ";
    cin >> phut;

    giay = phut * 60;

    cout << phut << " phut = " << giay << " giay";

    return 0;
}
```

## Ví dụ

```text
Nhap so phut: 4
4 phut = 240 giay
```

---

# 9. Bài toán 5: Đổi ngày sang giờ

## Đề bài

Nhập số ngày, đổi sang số giờ.

Biết rằng:

```text
1 ngày = 24 giờ
```

## Phân tích

```text
Đầu vào:
- ngay

Xử lý:
- gio = ngay * 24

Đầu ra:
- gio
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int ngay;
    int gio;

    cout << "Nhap so ngay: ";
    cin >> ngay;

    gio = ngay * 24;

    cout << ngay << " ngay = " << gio << " gio";

    return 0;
}
```

## Ví dụ

```text
Nhap so ngay: 7
7 ngay = 168 gio
```

---

# 10. Bài toán 6: Tính tuổi từ năm sinh

## Đề bài

Nhập năm sinh, tính tuổi gần đúng.

Ví dụ lấy năm hiện tại là `2026`.

## Phân tích

```text
Đầu vào:
- namSinh

Xử lý:
- tuoi = 2026 - namSinh

Đầu ra:
- tuoi
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int namSinh;
    int tuoi;

    cout << "Nhap nam sinh: ";
    cin >> namSinh;

    tuoi = 2026 - namSinh;

    cout << "Tuoi cua em la: " << tuoi;

    return 0;
}
```

## Ví dụ

```text
Nhap nam sinh: 2014
Tuoi cua em la: 12
```

Giáo viên lưu ý:

> Đây là tuổi gần đúng. Muốn tính tuổi chính xác cần biết thêm tháng và ngày sinh. Ở bài này chỉ cần tính đơn giản bằng năm.

---

# 11. Bài toán 7: Tính tổng tiền mua vở

## Đề bài

Nhập giá một quyển vở và số lượng vở. Tính tổng tiền cần trả.

## Phân tích

```text
Đầu vào:
- giaVo
- soLuong

Xử lý:
- tongTien = giaVo * soLuong

Đầu ra:
- tongTien
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaVo;
    int soLuong;
    int tongTien;

    cout << "Nhap gia mot quyen vo: ";
    cin >> giaVo;

    cout << "Nhap so luong vo: ";
    cin >> soLuong;

    tongTien = giaVo * soLuong;

    cout << "Tong tien can tra la: " << tongTien << " dong";

    return 0;
}
```

## Ví dụ

```text
Nhap gia mot quyen vo: 8000
Nhap so luong vo: 5
Tong tien can tra la: 40000 dong
```

---

# 12. Bài toán 8: Tính tiền thừa

## Đề bài

Một món đồ có giá `giaTien` đồng. Em đưa `tienDua` đồng. Tính số tiền thừa.

## Phân tích

```text
Đầu vào:
- giaTien
- tienDua

Xử lý:
- tienThua = tienDua - giaTien

Đầu ra:
- tienThua
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaTien;
    int tienDua;
    int tienThua;

    cout << "Nhap gia tien mon do: ";
    cin >> giaTien;

    cout << "Nhap so tien em dua: ";
    cin >> tienDua;

    tienThua = tienDua - giaTien;

    cout << "Tien thua la: " << tienThua << " dong";

    return 0;
}
```

## Ví dụ

```text
Nhap gia tien mon do: 15000
Nhap so tien em dua: 20000
Tien thua la: 5000 dong
```

Giáo viên lưu ý:

> Bài này chưa dùng điều kiện `if`, nên tạm thời giả sử số tiền đưa luôn lớn hơn hoặc bằng giá tiền.

---

# 13. Bài toán 9: Chia kẹo

## Đề bài

Có `keo` cái kẹo chia đều cho `ban` bạn. Hỏi mỗi bạn được bao nhiêu cái và còn dư bao nhiêu cái?

## Phân tích

```text
Đầu vào:
- keo
- ban

Xử lý:
- moiBan = keo / ban
- conDu = keo % ban

Đầu ra:
- số kẹo mỗi bạn nhận được
- số kẹo còn dư
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int keo;
    int ban;
    int moiBan;
    int conDu;

    cout << "Nhap so keo: ";
    cin >> keo;

    cout << "Nhap so ban: ";
    cin >> ban;

    moiBan = keo / ban;
    conDu = keo % ban;

    cout << "Moi ban duoc: " << moiBan << " cai keo" << endl;
    cout << "Con du: " << conDu << " cai keo";

    return 0;
}
```

## Ví dụ

```text
Nhap so keo: 17
Nhap so ban: 5
Moi ban duoc: 3 cai keo
Con du: 2 cai keo
```

Giáo viên nhấn mạnh:

> Đây là ví dụ rất hay để hiểu phép chia `/` và phép chia lấy dư `%`.

---

# 14. Bài toán 10: Tính điểm trung bình

## Đề bài

Nhập điểm Toán, Văn, Anh. Tính điểm trung bình.

## Phân tích

```text
Đầu vào:
- toan
- van
- anh

Xử lý:
- trungBinh = (toan + van + anh) / 3

Đầu ra:
- trungBinh
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    float toan, van, anh;
    float trungBinh;

    cout << "Nhap diem Toan: ";
    cin >> toan;

    cout << "Nhap diem Van: ";
    cin >> van;

    cout << "Nhap diem Anh: ";
    cin >> anh;

    trungBinh = (toan + van + anh) / 3;

    cout << "Diem trung binh la: " << trungBinh;

    return 0;
}
```

## Ví dụ

```text
Nhap diem Toan: 8
Nhap diem Van: 9
Nhap diem Anh: 7
Diem trung binh la: 8
```

Lưu ý:

```cpp
trungBinh = (toan + van + anh) / 3;
```

Phải có dấu ngoặc để cộng 3 điểm trước, rồi mới chia cho 3.

---

# 15. Bài toán 11: Tính chu vi và diện tích hình chữ nhật

## Đề bài

Nhập chiều dài và chiều rộng hình chữ nhật. Tính chu vi và diện tích.

## Phân tích

```text
Đầu vào:
- dai
- rong

Xử lý:
- chuVi = (dai + rong) * 2
- dienTich = dai * rong

Đầu ra:
- chuVi
- dienTich
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int dai, rong;
    int chuVi, dienTich;

    cout << "Nhap chieu dai: ";
    cin >> dai;

    cout << "Nhap chieu rong: ";
    cin >> rong;

    chuVi = (dai + rong) * 2;
    dienTich = dai * rong;

    cout << "Chu vi hinh chu nhat la: " << chuVi << endl;
    cout << "Dien tich hinh chu nhat la: " << dienTich;

    return 0;
}
```

## Ví dụ

```text
Nhap chieu dai: 6
Nhap chieu rong: 4
Chu vi hinh chu nhat la: 20
Dien tich hinh chu nhat la: 24
```

---

# 16. Bài toán 12: Tính chu vi và diện tích hình vuông

## Đề bài

Nhập cạnh hình vuông. Tính chu vi và diện tích.

## Phân tích

```text
Đầu vào:
- canh

Xử lý:
- chuVi = canh * 4
- dienTich = canh * canh

Đầu ra:
- chuVi
- dienTich
```

## Chương trình mẫu

```cpp
#include <iostream>
using namespace std;

int main() {
    int canh;
    int chuVi, dienTich;

    cout << "Nhap canh hinh vuong: ";
    cin >> canh;

    chuVi = canh * 4;
    dienTich = canh * canh;

    cout << "Chu vi hinh vuong la: " << chuVi << endl;
    cout << "Dien tich hinh vuong la: " << dienTich;

    return 0;
}
```

## Ví dụ

```text
Nhap canh hinh vuong: 5
Chu vi hinh vuong la: 20
Dien tich hinh vuong la: 25
```

---

# 17. Cách kiểm tra chương trình đúng hay sai

Sau khi viết chương trình, học sinh nên tự thử với số nhỏ.

Ví dụ bài tính diện tích hình chữ nhật:

```text
dai = 5
rong = 3
dienTich = 5 * 3 = 15
```

Nếu chương trình in ra `15`, có thể đúng.

Ví dụ bài chia kẹo:

```text
keo = 17
ban = 5

17 chia 5 được 3, dư 2
```

Nếu chương trình in:

```text
Moi ban duoc: 3
Con du: 2
```

thì đúng.

Giáo viên nhấn mạnh:

> Lập trình viên không chỉ viết code, mà còn phải biết kiểm tra code.

---

# 18. Quy trình làm bài tập ứng dụng

Khi làm bài tập ứng dụng phép toán, học sinh có thể làm theo mẫu:

```text
Bước 1: Đọc kỹ đề.
Bước 2: Gạch chân dữ liệu cần nhập.
Bước 3: Viết công thức.
Bước 4: Tạo biến.
Bước 5: Nhập dữ liệu bằng cin.
Bước 6: Tính toán.
Bước 7: In kết quả bằng cout.
Bước 8: Chạy thử với ví dụ nhỏ.
```

---

# 19. Hoạt động thực hành 1: Phân tích bài toán

Giáo viên đưa đề:

```text
Nhập số phút, đổi sang số giây.
```

Yêu cầu học sinh điền:

```text
Đầu vào:
- ...

Xử lý:
- ...

Đầu ra:
- ...
```

Đáp án gợi ý:

```text
Đầu vào:
- phut

Xử lý:
- giay = phut * 60

Đầu ra:
- giay
```

---

# 20. Hoạt động thực hành 2: Viết code từ phân tích

Từ phân tích ở hoạt động 1, học sinh viết code:

```cpp
#include <iostream>
using namespace std;

int main() {
    int phut;
    int giay;

    cout << "Nhap so phut: ";
    cin >> phut;

    giay = phut * 60;

    cout << phut << " phut = " << giay << " giay";

    return 0;
}
```

---

# 21. Hoạt động thực hành 3: Tự phân tích rồi viết code

Giáo viên đưa đề:

```text
Nhập số ngày, đổi sang số giờ.
```

Học sinh tự làm theo mẫu:

```text
Đầu vào:
Xử lý:
Đầu ra:
```

Đáp án gợi ý:

```text
Đầu vào:
- ngay

Xử lý:
- gio = ngay * 24

Đầu ra:
- gio
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int ngay;
    int gio;

    cout << "Nhap so ngay: ";
    cin >> ngay;

    gio = ngay * 24;

    cout << ngay << " ngay = " << gio << " gio";

    return 0;
}
```

---

# 22. Hoạt động thực hành 4: Tính tiền mua hàng

Đề bài:

```text
Nhập giá một cây bút và số lượng bút. Tính tổng tiền.
```

Phân tích:

```text
Đầu vào:
- giaBut
- soLuong

Xử lý:
- tongTien = giaBut * soLuong

Đầu ra:
- tongTien
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaBut;
    int soLuong;
    int tongTien;

    cout << "Nhap gia mot cay but: ";
    cin >> giaBut;

    cout << "Nhap so luong but: ";
    cin >> soLuong;

    tongTien = giaBut * soLuong;

    cout << "Tong tien can tra la: " << tongTien << " dong";

    return 0;
}
```

---

# 23. Hoạt động thực hành 5: Chia bánh

Đề bài:

```text
Có n cái bánh chia đều cho m bạn.
Hỏi mỗi bạn được bao nhiêu cái bánh và còn dư bao nhiêu cái?
```

Phân tích:

```text
Đầu vào:
- banh
- ban

Xử lý:
- moiBan = banh / ban
- conDu = banh % ban

Đầu ra:
- moiBan
- conDu
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int banh;
    int ban;
    int moiBan;
    int conDu;

    cout << "Nhap so banh: ";
    cin >> banh;

    cout << "Nhap so ban: ";
    cin >> ban;

    moiBan = banh / ban;
    conDu = banh % ban;

    cout << "Moi ban duoc: " << moiBan << " cai banh" << endl;
    cout << "Con du: " << conDu << " cai banh";

    return 0;
}
```

---

# 24. Lỗi thường gặp trong bài tập ứng dụng

## Lỗi 1: Không phân tích đề trước khi code

Học sinh thường đọc đề xong viết ngay, dẫn đến sai biến hoặc sai công thức.

Cách sửa:

```text
Luôn viết:
Đầu vào
Xử lý
Đầu ra
```

---

## Lỗi 2: Quên tạo biến lưu kết quả

Sai:

```cpp
cin >> dai;
cin >> rong;
cout << dienTich;
```

Biến `dienTich` chưa được tạo và chưa được tính.

Đúng:

```cpp
int dienTich;
dienTich = dai * rong;
cout << dienTich;
```

---

## Lỗi 3: Sai công thức do thiếu dấu ngoặc

Sai:

```cpp
chuVi = dai + rong * 2;
```

Đúng:

```cpp
chuVi = (dai + rong) * 2;
```

---

## Lỗi 4: Dùng sai kiểu dữ liệu

Ví dụ tính điểm trung bình mà dùng `int`:

```cpp
int toan, van, anh;
int trungBinh;
```

Nếu điểm có phần thập phân thì không phù hợp.

Nên dùng:

```cpp
float toan, van, anh;
float trungBinh;
```

---

## Lỗi 5: Nhầm `/` và `%`

Ví dụ chia kẹo:

```cpp
moiBan = keo % ban;
conDu = keo / ban;
```

Sai ý nghĩa.

Đúng:

```cpp
moiBan = keo / ban;
conDu = keo % ban;
```

Giải thích:

```text
/ dùng để lấy phần chia được
% dùng để lấy phần còn dư
```

---

# 25. Bài tập trên lớp

## Bài 1: Điền phân tích

Đề bài:

```text
Nhập số km, đổi sang mét.
```

Điền:

```text
Đầu vào:
- ...

Xử lý:
- ...

Đầu ra:
- ...
```

Đáp án:

```text
Đầu vào:
- soKm

Xử lý:
- soMet = soKm * 1000

Đầu ra:
- soMet
```

---

## Bài 2: Chọn công thức đúng

Tính chu vi hình chữ nhật với `dai`, `rong`.

A. `chuVi = dai + rong * 2;`
B. `chuVi = dai * rong;`
C. `chuVi = (dai + rong) * 2;`
D. `chuVi = dai + rong;`

Đáp án: **C**

---

## Bài 3: Chọn công thức đúng

Tính diện tích hình chữ nhật với `dai`, `rong`.

A. `dienTich = dai + rong;`
B. `dienTich = dai * rong;`
C. `dienTich = (dai + rong) * 2;`
D. `dienTich = dai - rong;`

Đáp án: **B**

---

## Bài 4: Đoán kết quả

```cpp
int keo = 17;
int ban = 5;

cout << keo / ban << endl;
cout << keo % ban;
```

Đáp án:

```text
3
2
```

---

## Bài 5: Tìm lỗi sai

```cpp
#include <iostream>
using namespace std;

int main() {
    int dai, rong;
    int chuVi;

    cout << "Nhap dai: ";
    cin >> dai;

    cout << "Nhap rong: ";
    cin >> rong;

    chuVi = dai + rong * 2;

    cout << "Chu vi la: " << chuVi;

    return 0;
}
```

Lỗi:

```text
Công thức chu vi thiếu dấu ngoặc.
```

Sửa đúng:

```cpp
chuVi = (dai + rong) * 2;
```

---

# 26. Bài tập thực hành

## Bài 1

Viết chương trình nhập số km, đổi sang mét.

Ví dụ:

```text
Nhap so km: 4
4 km = 4000 m
```

---

## Bài 2

Viết chương trình nhập số mét, đổi sang centimet.

Ví dụ:

```text
Nhap so met: 7
7 m = 700 cm
```

---

## Bài 3

Viết chương trình nhập số giờ, đổi sang phút.

Ví dụ:

```text
Nhap so gio: 5
5 gio = 300 phut
```

---

## Bài 4

Viết chương trình nhập số phút, đổi sang giây.

Ví dụ:

```text
Nhap so phut: 3
3 phut = 180 giay
```

---

## Bài 5

Viết chương trình nhập năm sinh, tính tuổi gần đúng.

Ví dụ:

```text
Nhap nam sinh: 2013
Tuoi cua em la: 13
```

---

## Bài 6

Viết chương trình nhập giá một cây bút và số lượng bút. Tính tổng tiền cần trả.

Ví dụ:

```text
Nhap gia mot cay but: 5000
Nhap so luong but: 4
Tong tien can tra la: 20000 dong
```

---

## Bài 7

Viết chương trình nhập số kẹo và số bạn. Tính mỗi bạn được bao nhiêu cái kẹo và còn dư bao nhiêu cái.

Ví dụ:

```text
Nhap so keo: 20
Nhap so ban: 6
Moi ban duoc: 3 cai keo
Con du: 2 cai keo
```

---

# 27. Bài tập nâng cao nhẹ

## Bài 1: Tính tiền sau khi mua nhiều loại đồ

Đề bài:

```text
Nhập giá bút và số lượng bút.
Nhập giá vở và số lượng vở.
Tính tổng tiền cần trả.
```

Gợi ý công thức:

```text
tongTien = giaBut * soBut + giaVo * soVo
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int giaBut, soBut;
    int giaVo, soVo;
    int tongTien;

    cout << "Nhap gia mot cay but: ";
    cin >> giaBut;

    cout << "Nhap so luong but: ";
    cin >> soBut;

    cout << "Nhap gia mot quyen vo: ";
    cin >> giaVo;

    cout << "Nhap so luong vo: ";
    cin >> soVo;

    tongTien = giaBut * soBut + giaVo * soVo;

    cout << "Tong tien can tra la: " << tongTien << " dong";

    return 0;
}
```

---

## Bài 2: Đổi tổng số giây sang phút và giây

Đề bài:

```text
Nhập tổng số giây. Hỏi được bao nhiêu phút và còn dư bao nhiêu giây?
```

Ví dụ:

```text
125 giây = 2 phút 5 giây
```

Phân tích:

```text
Đầu vào:
- tongGiay

Xử lý:
- phut = tongGiay / 60
- giay = tongGiay % 60

Đầu ra:
- phut
- giay
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tongGiay;
    int phut;
    int giay;

    cout << "Nhap tong so giay: ";
    cin >> tongGiay;

    phut = tongGiay / 60;
    giay = tongGiay % 60;

    cout << tongGiay << " giay = " << phut << " phut " << giay << " giay";

    return 0;
}
```

---

## Bài 3: Đổi tổng số phút sang giờ và phút

Đề bài:

```text
Nhập tổng số phút. Hỏi được bao nhiêu giờ và còn dư bao nhiêu phút?
```

Ví dụ:

```text
135 phút = 2 giờ 15 phút
```

Phân tích:

```text
Đầu vào:
- tongPhut

Xử lý:
- gio = tongPhut / 60
- phut = tongPhut % 60

Đầu ra:
- gio
- phut
```

Code gợi ý:

```cpp
#include <iostream>
using namespace std;

int main() {
    int tongPhut;
    int gio;
    int phut;

    cout << "Nhap tong so phut: ";
    cin >> tongPhut;

    gio = tongPhut / 60;
    phut = tongPhut % 60;

    cout << tongPhut << " phut = " << gio << " gio " << phut << " phut";

    return 0;
}
```

---

# 28. Câu hỏi củng cố cuối bài

Giáo viên hỏi học sinh:

1. Khi gặp bài toán lập trình, ta nên phân tích thành mấy phần?
2. Ba phần đó là gì?
3. Đầu vào nghĩa là gì?
4. Xử lý nghĩa là gì?
5. Đầu ra nghĩa là gì?
6. Đổi km sang m dùng công thức gì?
7. Đổi giờ sang phút dùng công thức gì?
8. Chia kẹo đều cho các bạn cần dùng hai phép toán nào?
9. Vì sao cần chạy thử chương trình với ví dụ nhỏ?

Gợi ý trả lời:

```text
1. Ba phần.
2. Đầu vào, xử lý, đầu ra.
3. Dữ liệu cần nhập.
4. Công thức hoặc cách tính.
5. Kết quả cần in ra.
6. mét = km * 1000.
7. phút = giờ * 60.
8. Dùng / và %.
9. Để kiểm tra chương trình có đúng không.
```

---

# 29. Bài tập về nhà

## Bài 1

Viết phân tích và code cho bài:

```text
Nhập số ngày, đổi sang số giờ.
```

Mẫu phân tích:

```text
Đầu vào:
Xử lý:
Đầu ra:
```

---

## Bài 2

Viết phân tích và code cho bài:

```text
Nhập số mét, đổi sang centimet.
```

---

## Bài 3

Viết chương trình nhập giá một quyển sách và số lượng sách. Tính tổng tiền.

---

## Bài 4

Viết chương trình nhập số bánh và số bạn. Tính mỗi bạn được bao nhiêu cái bánh và còn dư bao nhiêu cái.

---

## Bài 5

Viết chương trình nhập chiều dài, chiều rộng hình chữ nhật. Tính chu vi và diện tích.

---

# 30. Tóm tắt bài học

Học sinh cần nhớ:

```text
Khi giải bài toán lập trình, cần phân tích:

Đầu vào  → Cần nhập gì?
Xử lý    → Tính như thế nào?
Đầu ra   → In kết quả gì?

Một số công thức thường dùng:

mét = km * 1000
cm = mét * 100
phút = giờ * 60
giây = phút * 60
giờ = ngày * 24
tuổi = năm hiện tại - năm sinh

Chia đều:
mỗi người nhận = tổng / số người
còn dư = tổng % số người
```

Mẫu chương trình cần nhớ:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;
    int ketQua;

    cout << "Nhap a: ";
    cin >> a;

    cout << "Nhap b: ";
    cin >> b;

    ketQua = a * b;

    cout << "Ket qua la: " << ketQua;

    return 0;
}
```

---

# 31. Gợi ý thời lượng dạy

| Phần                               | Thời lượng |
| ---------------------------------- | ---------: |
| Ôn bài cũ                          |     5 phút |
| Giới thiệu cách phân tích bài toán |    10 phút |
| Làm mẫu bài đổi đơn vị             |    15 phút |
| Làm mẫu bài tính tiền, chia kẹo    |    15 phút |
| Thực hành theo nhóm                |    20 phút |
| Sửa lỗi thường gặp                 |    10 phút |
| Củng cố và giao bài tập            |     5 phút |

Tổng thời lượng: khoảng **80 phút**.
