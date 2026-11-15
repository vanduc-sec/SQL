# EMPLOYEES

```
Cho bảng employees gồm các thông tin

ID INT PRIMARY KEY
salary FLOAT
department_id INT

Hãy cập nhật lương (salary) tăng 10% của các nhân viên có department_id là 2
```

Code sql:

```sql
update employees
set salary=(salary)*1.1
where department_id=2;
```