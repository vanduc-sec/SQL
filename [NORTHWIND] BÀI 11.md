# [NORTHWIND] BÀI 11

Liệt kê những khách hàng có **`contactName**` có thứ tự từ điển lớn hơn `"Harani Canes"`

![image.png](%5BNORTHWIND%5D%20B%C3%80I%2011/image.png)

```
Expected Output:+--------+----------------+---------------------------+--------------------------------+----------------------------------------------+-----------------+---------------+------------+-------------+-----------------+--------+-------+-----------------+
| custId | companyName    | contactName               | contactTitle                   | address                                      | city            | region        | postalCode | country     | phone           | mobile | email | fax             |
.........(continue)..........
```

Code sql:

```sql
select * from Customer
where contactName > "Harani Canes";
```