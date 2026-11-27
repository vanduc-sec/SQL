# Recycle and low fat product

**Bảng: Products**

![image.png](Recycle%20and%20low%20fat%20product/image.png)

- product_id là khóa chính (cột chứa các giá trị duy nhất) của bảng này.
- low_fats là kiểu ENUM với các giá trị ('Y', 'N'), trong đó 'Y' nghĩa là sản phẩm ít béo và 'N' nghĩa là không ít béo.
- recyclable là kiểu ENUM với các giá trị ('Y', 'N'), trong đó 'Y' nghĩa là sản phẩm có thể tái chế và 'N' nghĩa là không thể tái chế.

**Nhiệm vụ:**

Viết một giải pháp để tìm các ID của sản phẩm vừa ít béo vừa có thể tái chế. Trả về bảng kết quả với thứ tự bất kỳ.

### Ví dụ:

**Đầu vào:**

**Bảng Products:**

![image.png](Recycle%20and%20low%20fat%20product/image%201.png)

**Đầu ra:**

![image.png](Recycle%20and%20low%20fat%20product/image%202.png)

**Giải thích:**

Chỉ có các sản phẩm với ID là 1 và 3 thỏa mãn điều kiện vừa ít béo (low_fats = 'Y') vừa có thể tái chế (recyclable = 'Y').

Code sql:

```sql
select product_id from Products
where low_fats='y' and recyclable='y';
```