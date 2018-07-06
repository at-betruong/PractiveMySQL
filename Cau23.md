### Câu 23. Lấy 2 blog, 2 news mà user có id = 1 đã comment
```
SELECT * FROM blog JOIN news ON  blog.category_id =  news.category_id
WHERE blog.user_id = 1
LIMIT 2;
```
