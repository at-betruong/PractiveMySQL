### Câu 19. Lấy 5 blog và 5 news của 1 category bất kỳ
```
SELECT * FROM blog JOIN news ON  blog.category_id =  news.category_id
GROUP BY blog.id, news.id
ORDER BY RAND()
LIMIT 5;
```
