### Câu 13. Lấy 5 blog mới nhất và số lượng comment cho từng blog
```
SELECT blog.*,  SL FROM blog JOIN 
(SELECT comment.target_id, COUNT(user_id) AS SL
	FROM comment
	GROUP BY comment.target_id) AS countcmt
ON blog.category_id =  countcmt.target_id
ORDER BY  blog.created_at DESC
LIMIT 5;
```
