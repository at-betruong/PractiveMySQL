### $Câu 14. Lấy 3 User comment đầu tiên trong 5 blogs mới nhất
```
SELECT cmt.user_id, cmt.created_at FROM comment as cmt
JOIN  (SELECT id  FROM blog ORDER BY blog.created_at DESC LIMIT 5) AS SUBQR
ON cmt.target_id = SUBQR.id
ORDER BY cmt.created_at DESC
LIMIT 3;
```
