# CẬP NHẬT LƯƠNG

```sql
có 2 bảng: Employees và Departments. 
Bạn cần cập nhật mức lương của các nhân viên dựa trên thông tin từ bảng Departments. Cụ thể:
Nếu một nhân viên làm việc trong phòng "Sales", tăng mức lương của họ lên 10%.
Nếu một nhân viên làm việc trong phòng "HR", tăng mức lương của họ lên 5%.
Nếu nhân viên làm việc trong các phòng ban khác, không thay đổi mức lương.

Bảng Employees:
Column Name            Type
emp_id                 INT
emp_name               VARCHAR
salary                 DECIMAL
dept_id                INT

Bảng Departments:
Column Name          Type
dept_id              INT
dept_name            VARCHAR

Cột emp_id trong bảng Employees là khóa chính.
Cột dept_id trong bảng Employees là khóa ngoại tham chiếu đến bảng Departments (cột dept_id).

Yêu cầu:
Cập nhật mức lương của nhân viên dựa trên phòng ban họ làm việc.
Chú ý chỉ viết 1 câu lệnh UPDATE
```

Code sql:

```sql
update Employees
join Departments on Employees.dept_id=Departments.dept_id
set Employees.salary= case
    when Departments.dept_name="Sales" then 1.1*Employees.salary
    when Departments.dept_name="HR" then 1.05*Employees.salary
end
where Departments.dept_name in ("Sales","HR");
```