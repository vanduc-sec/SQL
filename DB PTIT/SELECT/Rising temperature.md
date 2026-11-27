# Rising temperature

**Bảng: Weather**

![image.png](Rising%20temperature/image.png)

- id là cột có giá trị duy nhất trong bảng này.
- Không có hai hàng nào có cùng giá trị recordDate.
- Bảng chứa thông tin về nhiệt độ (temperature) vào một ngày cụ thể (recordDate).

**Yêu cầu:**

Viết một giải pháp để tìm tất cả các id của các ngày có nhiệt độ cao hơn so với ngày trước đó (hôm qua).

Trả về bảng kết quả với thứ tự bất kỳ.

### Ví dụ:

**Đầu vào:**

**Bảng Weather:**

![image.png](Rising%20temperature/image%201.png)

**Đầu ra:**

![image.png](Rising%20temperature/image%202.png)

**Giải thích:**

- Ngày 2015-01-02 (ID = 2): Nhiệt độ 25 cao hơn ngày trước đó (2015-01-01, nhiệt độ = 10).
- Ngày 2015-01-04 (ID = 4): Nhiệt độ 30 cao hơn ngày trước đó (2015-01-03, nhiệt độ = 20).
- Ngày 2015-01-03 (ID = 3): Nhiệt độ 20 không cao hơn ngày trước đó (2015-01-02, nhiệt độ = 25).

Code sql:

```sql
select w2.id from Weather w1
join Weather w2 on datediff(day,w1.recordDate,w2.recordDate)=1
where w2.temperature>w1.temperature;
```