# INVALID TWEETS

```
Table: Tweets

+----------------+---------+
| Column Name    | Type    |
+----------------+---------+
| tweet_id       | int     |
| content        | varchar |
+----------------+---------+
tweet_id là khóa chính (cột chứa giá trị duy nhất) cho bảng này.
`content` bao gồm các ký tự trên bàn phím tiếng Anh Mỹ và không chứa các ký tự đặc biệt khác.
Bảng này chứa tất cả các tweet trong một ứng dụng mạng xã hội.
Viết một giải pháp để tìm các `tweet_id` của những tweet không hợp lệ.
Một tweet được coi là không hợp lệ nếu số ký tự trong nội dung (`content`) của tweet lớn hơn 15.

Định dạng kết quả giống ví dụ sau.
Example 1:

Input:
Tweets table:
+----------+-----------------------------------+
| tweet_id | content                           |
+----------+-----------------------------------+
| 1        | Let us Code                       |
| 2        | More than fifteen chars are here! |
+----------+-----------------------------------+
Output:
+----------+
| tweet_id |
+----------+
| 2        |
+----------+
Giải thích:
Tweet 1 có độ dài = 11. Đây là 1 tweet hợp lệ.
Tweet 2 có độ dài = 33. Đây là 1 tweet không hợp lệ.
```

Code sql:

```sql
select tweet_id from Tweets
where char_length(content)>15;
```