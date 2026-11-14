# FIND CUSTOMER REFEREE

```
Bảng: Customer

+-------------+---------+
| Tên cột     | Kiểu    |
+-------------+---------+
| id          | int     |
| name        | varchar |
| referee_id  | int     |
+-------------+---------+

Trong SQL, `id` là khóa chính của bảng này.
Mỗi dòng thể hiện một khách hàng với id, tên, và id của người đã giới thiệu khách hàng đó (referee_id).

Yêu cầu:
Viết truy vấn SQL để **tìm tên các khách hàng không được giới thiệu bởi khách hàng có id = 2**.

Trả về kết quả theo thứ tự bất kỳ.

Ví dụ:

Input:
Bảng Customer:
+----+------+------------+
| id | name | referee_id |
+----+------+------------+
| 1  | Will | null       |
| 2  | Jane | null       |
| 3  | Alex | 2          |
| 4  | Bill | null       |
| 5  | Zack | 1          |
| 6  | Mark | 2          |
+----+------+------------+

Output:
+------+
| name |
+------+
| Will |
| Jane |
| Bill |
| Zack |
+------+
```

Code sql:

```sql
select name from Customer
where referee_id != 2 or referee_id is null;
```