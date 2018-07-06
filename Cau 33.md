### Câu 33. $Liệt kê email user các user có tên(user.full_name) có chứa ký tự "Khi" theo danh sách như output bên dưới.

```
SELECT CONCAT(user.full_name) FROM user
WHERE user.full_name LIKE '%Khi%'
```
