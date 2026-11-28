# Các khóa học cấp độ 400 (4xx) của CSE đang mở là gì

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

- - Các khóa học cấp độ 400 (4xx) của CSE đang mở là gì?

dept    number   title

- --------- ---------- ---------------------------------

CSE     451     Introduction to Operating Systems

CSE     461     Introduction to Computer Communic

Code sql:

```sql
select dept,number,title from Class
where dept="CSE" and number>=400 and number<500;
```