### Câu 34. Tính điểm cho user có email là minh82@example.com trong bảng comment. Cách tính điểm: Trong bảng comment với taget_table = "blog" tính 1 điểm, taget_table = "news" tính 2 điểm.
```
SELECT email, SUM(CASE target_table WHEN 'blog' THEN 1 ELSE 2 END) AS point 
FROM user JOIN comment ON user.id = comment.user_id 
WHERE email = 'minh82@example.com';
```
