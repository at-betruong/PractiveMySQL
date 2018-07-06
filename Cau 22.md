### Câu 22. $Lấy danh sách user đã comment trong 2 blog mới nhất
```
SELECT blog.user_id FROM blog 
WHERE blog.id IN (
    SELECT * FROM blog
	ORDER BY blog.created_at DESC
    LIMIT 2;
	);
```

```
SELECT blog.user_id FROM blog 
WHERE blog.id  IN(
	SELECT  TOP 2 blog.id FROM blog
	ORDER BY blog.created_at DESC
    )
```
