### Câu 15. Update rank user = 2 khi tổng số lượng comment của user > 20
 * **Tạo bảng `amountcmt` truy vấn để đếm số comment của mỗi user_id
```
CREATE TABLE amountcmt AS 
	SELECT comment.user_id, COUNT(comment.id) AS SL 
	FROM comment
	GROUP BY comment.user_id;
```
 *  **Thực hiện truy vấn :
```
UPDATE user  JOIN amountcmt ON user.id = amountcmt.user_id 
set user.rank = 2 
WHERE amountcmt.SL > 20;
```
