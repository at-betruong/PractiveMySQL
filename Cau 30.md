### Câu 30. Lấy 1 comment(id_comment,  comment) mới nhất và thông tin user của user đang được follow bởi user 1
```
SELECT user.* , comment.id, comment.comment
FROM follow JOIN user ON follow.from_user_id = user.id
JOIN comment ON user.id =  comment.id
WHERE follow.from_user_id = 1
ORDER BY comment.created_at DESC
LIMIT 1
```
