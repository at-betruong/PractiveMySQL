### Câu 18. Lấy số lượng Blog active của user có id là 1,2,4
```
SELECT blog.user_id , count( blog.id) AS SL  FROM blog JOIN user ON blog.user_id = user.id
WHERE  user.id  IN (1,2,3)
GROUP BY blog.user_id;
```
