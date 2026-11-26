# RISING TEMPERATURE

```
Bảng: Weather

+---------------+---------+
| Tên cột       | Kiểu    |
+---------------+---------+
| id            | int     |
| recordDate    | date    |
| temperature   | int     |
+---------------+---------+
Cột id là khóa chính và có giá trị duy nhất trong bảng.
Không có hai dòng nào có cùng recordDate.
Bảng này lưu thông tin về nhiệt độ trong một ngày cụ thể.

Viết truy vấn SQL để tìm tất cả các `id` của những ngày có nhiệt độ cao hơn ngày trước đó (hôm qua).

Trả về kết quả theo thứ tự bất kỳ.

Ví dụ 1:

Dữ liệu đầu vào:
Bảng Weather:
+----+------------+-------------+
| id | recordDate | temperature |
+----+------------+-------------+
| 1  | 2015-01-01 | 10          |
| 2  | 2015-01-02 | 25          |
| 3  | 2015-01-03 | 20          |
| 4  | 2015-01-04 | 30          |
+----+------------+-------------+

Kết quả đầu ra:
+----+
| id |
+----+
| 2  |
| 4  |
+----+

Giải thích:
Vào ngày 2015-01-02, nhiệt độ cao hơn hôm trước (10 -> 25).
Vào ngày 2015-01-04, nhiệt độ cao hơn hôm trước (20 -> 30).
```

Code sql:

```sql
select w2.id from Weather as w1
join Weather as w2 on datediff(w2.recordDate,w1.recordDate)=1
where w2.temperature>w1.temperature;
```