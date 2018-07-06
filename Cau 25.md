### Câu 25. $Lấy 5 blog và 5 news mới nhất đã active
* ** 5 blog  mới nhất đã active
```
SELECT * FROM blog 
WHERE blog.is_active = 1
ORDER BY blog.created_at DESC
LIMIT 5;
```

*  **5 news mới nhất đã active
```
SELECT * FROM  news
WHERE  is_active = 1
ORDER BY  created_at DESC
LIMIT 5;
```
