# SẢN PHẨM TÁI CHẾ VÀ ÍT BÉO

```
Bảng: Products

Column Name       Type

product_id              INT

low_fats                 VARCHAR

recyclable              VARCHAR

product_id là khóa chính (cột chứa giá trị duy nhất) cho bảng này.

low_fats là một VARCHARcó kiểu ('Y', 'N') trong đó 'Y' có nghĩa là sản phẩm này ít chất béo và 'N' có nghĩa là sản phẩm này không ít chất béo.

recyclable là một VARCHAR có kiểu ('Y', 'N') trong đó 'Y' có nghĩa là sản phẩm này có thể tái chế và 'N' có nghĩa là sản phẩm này không thể tái chế.

**Yêu cầu:**

Viết một truy vấn SQL để tìm các product_id của các sản phẩm vừa ít chất béo (low fat) và có thể tái chế (recyclable).

Trả về kết quả dưới dạng bảng như ví dụ sau.

**Ví dụ 1:**

Dữ liệu đầu vào:

Bảng Products:

product_id  low_fats recyclable

0                 Y             N

1                 Y             Y

2                 N             Y

3                 Y             Y

4                 N             N

Kết quả đầu ra:

product_id

1

3

Giải thích:

Chỉ có sản phẩm có product_id là 1 và 3 là cả hai: ít chất béo (low fat) và có thể tái chế (recyclable).
```

Code sql:

```sql
select product_id from Products
where low_fats="Y" and recyclable="Y";
```