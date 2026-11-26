# [NORTHWIND V2] BÀI 1

```
Đếm số lượng khách hàng của mỗi thành phố, chỉ hiển thị những thành phố có từ 2 khách hàng trở lên.
```

![image.png](%5BNORTHWIND%20V2%5D%20B%C3%80I%201/image.png)

```
Output
+----------------+---------------+
| city           | CustomerCount |
+----------------+---------------+
| México D.F.    |             5 |
| London         |             6 |
| Madrid         |             3 |
| Buenos Aires   |             3 |
| Sao Paulo      |             4 |
| Nantes         |             2 |
| Lisboa         |             2 |
| Rio de Janeiro |             3 |
| Portland       |             2 |
| Paris          |             2 |
+----------------+---------------+
```

Code sql:

```sql
select city,count(custid ) as CustomerCount from Customer
group by city
having CustomerCount>=2;
```