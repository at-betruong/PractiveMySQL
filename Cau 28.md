### Câu 28. Lấy số lượng user đang follow user = 1
```
SELECT  to_user_id,  COUNT(from_user_id)  as SL   FROM  follow
WHERE  to_user_id  = 1
GROUP  BY  to_user_id;
```
