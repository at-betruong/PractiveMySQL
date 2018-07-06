### Câu 21. Lấy blog được tạo trong 3 ngày gần nhất
```
SELECT * FROM blog 
WHERE DATEDIFF(CURRENT_TIMESTAMP, blog.created_at) <3;
```
