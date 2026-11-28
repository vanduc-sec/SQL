# Liệt kê 2 khóa học theo tên giảng viên (sắp xếp theo tên giảm dần)

Bạn có 3 bảng sau:

1. **Bảng Class:**
- Chứa thông tin về các khóa học.
- Cấu trúc:
- dept (VARCHAR(6)): Mã phòng ban của khóa học.
- number (INTEGER): Số hiệu khóa học.
- title (VARCHAR(75)): Tiêu đề khóa học.
1. **Bảng Instructor:**
- Chứa thông tin về giảng viên.
- Cấu trúc:
- username (VARCHAR(8)): Tên tài khoản giảng viên.
- fname (VARCHAR(50)): Tên của giảng viên.
- lname (VARCHAR(50)): Họ của giảng viên.
- started_on (CHAR(10)): Ngày bắt đầu làm việc của giảng viên.
1. **Bảng Teaches:**
- Chứa thông tin về việc giảng viên dạy khóa học nào.
- Cấu trúc:
- username (VARCHAR(8)): Tên tài khoản giảng viên.
- dept (VARCHAR(6)): Mã phòng ban của khóa học.
- number (INTEGER): Số hiệu khóa học.

**Yêu cầu:**

- - Liệt kê 2 khóa học theo họ giảng viên (sắp xếp theo lname giảm dần)

Ví dụ output

![image.png](<Liệt kê 2 khóa học theo tên giảng viên (sắp xếp theo tên giảm dần)/image.png>)

Code sql:

```sql
select i.username,t.dept,t.number from Instructor i
join Teaches t on i.username=t.username
order by i.lname desc
limit 2;
```