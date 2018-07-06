### Câu 32. Tìm có tên(user.full_name) "Khiêu" và các thông tin trên blog của user này như: (blog.title, blog.view), title category(category) của blog này. Hiển thị theo output như bên dưới:

```
SELECT  user.full_name,  blog.title,  blog.view,  category.title
FROM  user  JOIN  blog  ON  user.id  =  blog.user_id
JOIN  category  ON  blog.category_id  =  category.id
WHERE  user.full_name  LIKE  '%Khiêu'; 
```
