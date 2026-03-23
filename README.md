# E-SHOP-CLOTHING-2008- Xử lý dữ liệu

## 1. Mục đích

Tài liệu này ghi lại quá trình đổi tên các biến trong bộ dữ liệu *e-shop clothing 2008*.
Mục tiêu là chuẩn hóa tên biến để thuận tiện cho việc phân tích và xây dựng mô hình trong R.

---

## 2. Lý do đổi tên

Tên biến ban đầu trong bộ dữ liệu có:

* Khoảng trắng
* Ký tự đặc biệt
* Tên dài, khó sử dụng

Những vấn đề này có thể:

* Gây lỗi cú pháp trong R
* Làm code khó đọc và khó bảo trì

Vì vậy, các biến được đổi sang dạng ngắn gọn, không dấu cách và dễ sử dụng hơn.

---

## 3. Chi tiết đổi tên

Các biến được đổi tên như sau:

| Tên ban đầu             | Tên sau khi đổi |
| ----------------------- | --------------- |
| session ID              | sessionid       |
| page 1 (main category)  | page1           |
| page 2 (clothing model) | page2           |
| model photography       | model_photo     |
| price 2                 | price2          |

---

## 4. Thực hiện trong R

Quá trình đổi tên được thực hiện bằng hàm `rename()` trong thư viện **dplyr**:

```r id="v3l8kp"
e_shop_clothing_2008 <- e_shop_clothing_2008 |>
  rename(
    sessionid = `session ID`,
    page1 = `page 1 (main category)`,
    page2 = `page 2 (clothing model)`,
    model_photo = `model photography`,
    price2 = `price 2`
  )
```

---

## 5. Lợi ích

Sau khi đổi tên:

* Code trở nên rõ ràng và dễ đọc hơn
* Tránh lỗi khi gọi tên biến
* Dễ dàng thao tác và phân tích dữ liệu
* Thuận tiện khi làm việc nhóm

---

## 6. Kết luận

Việc đổi tên biến là một bước tiền xử lý quan trọng trong phân tích dữ liệu.
Bước này giúp nâng cao chất lượng code, giảm lỗi và hỗ trợ quá trình phân tích được hiệu quả hơn.
