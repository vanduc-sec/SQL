# Consecutive number

**Bảng: Logs**

```
+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| id          | int     |
| num         | varchar |
+-------------+---------+
```

Trong SQL, ***id*** là khóa chính của bảng này.

***id*** là cột tự tăng (auto increment).

**Nhiệm vụ:**

Tìm tất cả các số xuất hiện ít nhất ba lần liên tiếp.

Trả về bảng kết quả theo thứ tự tăng dần các số.

**Ví dụ:**

Input: Logs table:

```
+----+-----+
| id | num |
+----+-----+
| 1  | 1   |
| 2  | 1   |
| 3  | 1   |
| 4  | 2   |
| 5  | 1   |
| 6  | 2   |
| 7  | 2   |
+----+-----+
```

Output:

```
+-----------------+
| ConsecutiveNums |
+-----------------+
| 1               |
+-----------------+
```

**Giải thích:**

- Số 1 xuất hiện liên tiếp ít nhất 3 lần (id 1, 2, 3).
- Các số khác không thỏa mãn điều kiện xuất hiện liên tiếp ít nhất 3 lần.

Code sql:

```sql
select distinct l1.num as ConsecutiveNums
from Logs l1 
join Logs l2 on l1.id=l2.id-1
join Logs l3 on l1.id=l3.id-2
where l1.num=l2.num and l2.num=l3.num
order by ConsecutiveNums asc;
```