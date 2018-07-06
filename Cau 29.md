### Câu 29. Lấy số lượng user 1 đang follow
```
SELECT  from_user_id,  COUNT(to_user_id)  as  SL   FROM  follow
WHERE  from_user_id  = 1
GROUP  BY  from_user_id;
```
