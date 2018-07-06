### Câu 24. $Lấy 1 blog và 1 news có số lượng comment nhiều nhất
*  **Tạo bảng lấy số lượng comment nhiều nhất của 1 blog
```
CREATE TABLE max_cmt_news AS
 	SELECT comment.target_id, COUNT(comment.id) as SL FROM comment
	WHERE comment.target_table = 'blog' 
    GROUP BY comment.target_id
	LIMIT 1
```

* **Tạo bảng lấy số lượng comment nhiều nhất của 1 news

```
CREATE TABLE max_cmt_news AS
    SELECT comment.target_id, COUNT(comment.id) as SL FROM comment
    WHERE comment.target_table = 'news' 
    GROUP BY comment.target_id
    LIMIT 1
* **Truy vấn
```
SELECT * FROM blog 
WHERE blog.id IN (SELECT max_cmt_blog.target_id FROM max_cmt_blog);
```

```
SELECT * FROM news 
WHERE news.id IN (SELECT max_cmt_news.target_id FROM max_cmt_news);
```
