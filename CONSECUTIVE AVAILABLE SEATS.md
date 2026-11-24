# CONSECUTIVE AVAILABLE SEATS

**Bảng: Cinema**

```
+-------------+------+
| Tên cột     | Kiểu dữ liệu |
+-------------+------+
| seat_id     | int  |
| free        | bool |
+-------------+------+
seat_id là một cột tự động tăng cho bảng này.
Mỗi hàng của bảng này cho biết ghế thứ i có còn trống hay không. 1 có nghĩa là ghế trống, trong khi 0 có nghĩa là đã có người ngồi.
Viết một giải pháp để tìm tất cả các ghế trống liên tiếp trong rạp chiếu phim.
Trả về bảng kết quả được sắp xếp theo seat_id theo thứ tự tăng dần.
Các bộ kiểm tra được tạo sao cho có nhiều hơn hai ghế liên tiếp còn trống.
```

---

```
Ví dụ 1:
Input:
Bảng Cinema:
+---------+------+
| seat_id | free |
+---------+------+
| 1       | 1    |
| 2       | 0    |
| 3       | 1    |
| 4       | 1    |
| 5       | 1    |
+---------+------+
Output:
+---------+
| seat_id |
+---------+
| 3       |
| 4       |
| 5       |
+---------+
```

Code sql:

```sql
select distinct c1.seat_id from Cinema c1
join Cinema c2 on abs(c1.seat_id-c2.seat_id)=1
where c1.free=1 and c2.free=1
order by c1.seat_id
```