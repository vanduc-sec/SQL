# CUSTOMER PLACING THE LARGEST NUMBER OF ORDERS

```
Bảng: Orders

+-----------------+----------+
| Tên cột         | Kiểu     |
+-----------------+----------+
| order_number    | int      |
| customer_number | int      |
+-----------------+----------+

order_number là khóa chính (giá trị duy nhất) của bảng này.
Bảng này lưu thông tin về mã đơn hàng và mã khách hàng đã đặt hàng.

Yêu cầu:
Viết truy vấn SQL để **tìm customer_number của khách hàng đặt nhiều đơn hàng nhất**.

Giả sử các bộ test được tạo sao cho **chỉ có duy nhất một khách hàng có số đơn hàng nhiều nhất**.

Ví dụ:

Input:
Bảng Orders:
+--------------+-----------------+
| order_number | customer_number |
+--------------+-----------------+
| 1            | 1               |
| 2            | 2               |
| 3            | 3               |
| 4            | 3               |
+--------------+-----------------+

Output:
+-----------------+
| customer_number |
+-----------------+
| 3               |
+-----------------+

Giải thích:
Khách hàng có customer_number = 3 có 2 đơn hàng, nhiều hơn khách 1 và 2 (mỗi người chỉ có 1 đơn hàng), nên kết quả là 3.
```

Code sql:

```sql
select customer_number from Orders
group by customer_number 
order by count(order_number) desc
limit 1;
```