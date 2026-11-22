# [NORTHWIND V3] BÀI 9

Tìm nhân viên có họ (lastname) dài nhất.

![image.png](%5BNORTHWIND%20V3%5D%20B%C3%80I%209/image.png)

Code sql:

```sql
select employeeId,lastname,length(lastname) as NameLength
from Employee
order by NameLength desc
limit 1;
```