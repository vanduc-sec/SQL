# [NORTHWIND V3] BÀI 14

Nhân viên có nhiều đơn hàng nhất mỗi năm

![image.png](%5BNORTHWIND%20V3%5D%20B%C3%80I%2014/image.png)

```
Output:
+------------+-----------+--------------+-----------+------------+
| employeeId | firstname | lastname     | OrderYear | OrderCount |
+------------+-----------+--------------+-----------+------------+
|          4 | Yael      | Peled        |      2006 |         31 |
|          1 | Sara      | Davis        |      2006 |         26 |
|          8 | Maria     | Cameron      |      2006 |         19 |
|          3 | Judy      | Lew          |      2006 |         18 |
|          2 | Don       | Funk.........(continue)..........
```

Code sql:

```sql
select e.employeeId,e.firstname,e.lastname,
        year(s.orderDate) as OrderYear,
        count(s.orderid) as OrderCount
from Employee e
join SalesOrder as s on e.employeeId = s.employeeId 
group by e.employeeId,e.firstname,e.lastname,year(s.orderDate)
order by OrderYear asc,OrderCount desc;
```