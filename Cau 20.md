### Câu 20. $Lấy blog và news có lượt view nhiều nhất
*  **Blog có view nhiều nhất
```
(SELECT  id, title  FROM  blog
ORDER  BY  view  DESC
LIMIT 1)
union all
(SELECT  id, title  FROM  news
ORDER  BY  view DESC
LIMIT 1);
```
