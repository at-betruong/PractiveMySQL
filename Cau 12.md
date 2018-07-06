### Câu 12. Lấy blog được tạo bởi user mà user này không có bất kỳ comment ở blog
```
SELECT * FROM blog 
WHERE blog.user_id NOT IN (
	SELECT user.id FROM user JOIN comment 
	ON user.id = comment.user_id
	GROUP BY user.id); 
```
