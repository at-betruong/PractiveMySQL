### Câu 11. #Lấy tổng lượt view của từng category thông qua blog và news
```
SELECT category_id, SUM(SL) AS total_views FROM 
( 
	SELECT category_id, sum(view) as SL FROM blog 
	GROUP BY blog.category_id
	UNION ALL 
	SELECT category_id, sum(view) as SL FROM news
	GROUP BY news.category_id
) AS subtabl
GROUP BY category_id;
```
