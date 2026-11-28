# Tìm các lớp học đang được mở

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

Hãy viết truy vấn SQL để liệt kê tất cả các khóa học đang được giảng dạy (mở lớp) bởi các giảng viên. Mỗi khóa học cần hiển thị:

title

- -----------------------------------------

Machine Organization and Assembly Language

Introduction to Operating Systems

Introduction to Computer Communication Net

Code sql:

```sql
select c.title from Class c
join Teaches t on c.dept=t.dept and c.number=t.number;
```