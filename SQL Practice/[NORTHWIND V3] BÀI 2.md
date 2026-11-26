# [NORTHWIND V3] BÀI 2

Hiển thị tên khách hàng (contactName) dưới dạng viết hoa toàn bộ.

![image.png](%5BNORTHWIND%20V3%5D%20B%C3%80I%202/image.png)

Output:

```
+--------+--------------------------------+
| custId | ContactName_Upper              |
+--------+--------------------------------+
|      1 | ALLEN, MICHAEL                 |
|      2 | HASSALL, MARK                  |
|      3 | PEOPLES, JOHN                  |
|      4 | ARNDT, TORSTEN                 |
|      5 | HIGGINBOTHAM, TOM              |
|      6 | POLAND, CAROLE                 |
|      7 | BANSAL, DUSHYANT               |
|      8 | ILYINA, JULIA                  |
|      9 | RAGHA.........(continue)..........
```

Code sql:

```sql
select custId,upper(contactName) as ContactName_Upper from Customer
```