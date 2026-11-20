# ĐẤT NƯỚC LỚN

```
table World

+-------------+---------+
| Column Name | Type    |
+-------------+---------+
| name        | varchar |
| continent   | varchar |
| area        | int     |
| population  | int     |
| gdp         | bigint  |
+-------------+---------+
name là khóa chính (cột chứa giá trị duy nhất) cho bảng này.
Mỗi hàng trong bảng này cung cấp thông tin về tên quốc gia, châu lục mà quốc gia đó thuộc về,
diện tích, dân số và giá trị GDP của quốc gia.

Một quốc gia được coi là lớn nếu:
- Quốc gia có diện tích ít nhất là ba triệu (tức là 3000000 km²), hoặc
- Quốc gia có dân số ít nhất là hai mươi lăm triệu (tức là 25000000).
Viết một giải pháp để tìm tên (`name`), dân số (`population`) và diện tích (`area`) của các quốc gia lớn.

Định dạng kết quả giống ví dụ sau.
Example 1:
Input:
World table:
+-------------+-----------+---------+------------+--------------+
| name        | continent | area    | population | gdp          |
+-------------+-----------+---------+------------+--------------+
| Afghanistan | Asia      | 652230  | 25500100   | 20343000000  |
| Albania     | Europe    | 28748   | 2831741    | 12960000000  |
| Algeria     | Africa    | 2381741 | 37100000   | 188681000000 |
| Andorra     | Europe    | 468     | 78115      | 3712000000   |
| Angola      | Africa    | 1246700 | 20609294   | 100990000000 |
+-------------+-----------+---------+------------+--------------+
Output:
+-------------+------------+---------+
| name        | population | area    |
+-------------+------------+---------+
| Afghanistan | 25500100   | 652230  |
| Algeria     | 37100000   | 2381741 |
+-------------+------------+---------+
```

Code sql:

```agda
select name,population,area from World
where area>=3000000 or population>=25000000;
```