# [NORTHWIND] BÀI 4

Liệt kê những khách hàng sống tại thành phố London và có mã khách hàng là số chẵn

![image.png](%5BNORTHWIND%5D%20B%C3%80I%204/image.png)

Code sql:

```sql
select * from Customer
where city="London" and custId%2=0;
```