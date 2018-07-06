### Câu 27. Blog của user đang được user có id = 1 follow
```
SELECT distinct blog.id FROM blog JOIN user 
ON blog.user_id = user.id JOIN follow ON user.id =  follow.from_user_id
WHERE follow.from_user_id =1;
```
