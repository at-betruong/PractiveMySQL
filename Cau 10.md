### Câu 10. Lấy Category có tồn tại blog hoặc news đã active (không được lặp lại category)
```
SELECT * FROM category
WHERE category.id IN (SELECT blog.category_id FROM blog WHERE blog.is_active =1)
		OR category.id IN (SELECT news.category_id FROM news WHERE news.is_active =1) ;
```
