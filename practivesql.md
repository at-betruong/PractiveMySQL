# 1. Tạo database như hình trên (sau khi tạo thì import database, sẽ gửi sau)
# 2. Thêm 1 dòng dữ liệu trong bất kỳ table nào
* INSERT INTO `category` VALUES ('3001', 'Category 1', 'Description 1');
# 3. Xoá và sửa 1 dòng dữ liệu trong bất kỳ table nào
* DELETE FROM user WHERE id = 1013 ;
# 4. Select 10 blog mới nhất đã active
* create
INSERT INTO  blog  VALUES (2005, 3005, 1006, 'title blog 5', 22, 1, 'chiec thuyen ngoai xa', '2018-06-29 12:30:00', '2018-06-30 06:00:00');
INSERT  INTO  blog  VALUES (2002, 3008, 1011, 'title blog 2', 33, 0, 'chiec thuyen ngoai xa', '2018-06-29 23:30:00', '2018-06-30 12:00:00');
INSERT  INTO  blog  VALUES (2003, 3001, 1009, 'title blog 3', 12, 1, 'chiec thuyen ngoai xa', '2018-06-29 11:30:00', '2018-06-30 22:00:00');
INSERT  INTO  blog  VALUES (2004, 3003, 1005, 'title blog 4', 13, 1, 'chiec thuyen ngoai xa', '2018-06-29 02:30:00', '2018-06-30 14:00:00');
INSERT INTO blog VALUES (2006, 3004, 1005, 'title blog 6', 33, 1, 'chiec thuyen ngoai xa', '2018-06-29 05:30:00', '2018-06-30 01:20:00');
INSERT INTO blog VALUES (2007, 3002, 1004, 'title blog 7', 14, 0, 'chiec thuyen ngoai xa', '2018-06-29 00:30:00', '2018-06-30 03:40:00');
INSERT  INTO  blog VALUES (2008, 3002, 1008, 'title blog 8', 41, 1, 'chiec thuyen ngoai xa', '2018-06-29 22:30:00', '2018-06-30 12:10:00');
INSERT  INTO  blog  VALUES (2009, 3007, 1010, 'title blog 9', 55, 1, 'chiec thuyen ngoai xa', '2018-06-29 21:30:00', '2018-06-30 01:00:00');
INSERT  INTO  blog  VALUES (2010, 3006, 1003, 'title blog 10', 22, 0, 'chiec thuyen ngoai xa', '2018-06-29 11:40:00', '2018-06-30 12:00:00');
INSERT  INTO  blog  VALUES (2011, 3003, 1003, 'title blog 11', 66, 1, 'chiec thuyen ngoai xa', '2018-06-29 03:00:00', '2018-06-30 11:00:00');
INSERT  INTO  blog  VALUES (2012, 3003, 1001, 'title blog 12', 56, 1, 'chiec thuyen ngoai xa', '2018-06-29 03:12:00', '2018-06-30 08:00:00');
INSERT  INTO  blog  VALUES (2013, 3007, 1007, 'title blog 13', 54, 1, 'chiec thuyen ngoai xa', '2018-06-29 03:09:00', '2018-06-30 07:00:00');
INSERT  INTO  blog  VALUES (2014, 3005, 1008, 'title blog 14', 76, 1, 'chiec thuyen ngoai xa', '2018-06-29 03:56:00', '2018-06-30 05:00:00');
INSERT  INTO  blog  VALUES (2015, 3004, 1009, 'title blog 15', 12, 1, 'chiec thuyen ngoai xa', '2018-06-29 03:22:00', '2018-06-30 03:00:00');
INSERT  INTO  blog  VALUES (2016, 3004, 1001, 'title blog 16', 20, 0, 'chiec thuyen ngoai xa', '2018-06-29 03:11:00', '2018-06-30 23:00:00');
INSERT  INTO  blog  VALUES (2017, 3002, 1001, 'title blog 17', 33, 1, 'chiec thuyen ngoai xa', '2018-06-29 03:05:00', '2018-06-30 12:00:00');
* truy vấn:
SELECT * FROM  blog 
WHERE  is_active =1 
ORDER BY  created_a t DESC
LIMIT 10;
# 5. Lấy 5 blog từ blog thứ 10
SELECT * FROM  blog 
LIMIT 10, 5;
# 6. Set is_active = 0 của user có id = 3 trong bảng user
UPDATE  blog  SET  is_active=0  WHERE  id=3;
# 7. Xoá tất cả comment của user = 2 trong blog = 5
* insert news
INSERT INTO news VALUES (4001, 3005, 'title new 1', 12, 1, 'content new 1', '2018-06-28 12:00:00', '2018-06-30 11:00:00');
INSERT INTO news VALUES (4002, 3006, 'title new 2', 22, 0, 'content new 2', '2018-06-28 03:30:00', '2018-06-30 05:00:00');
INSERT INTO news VALUES (4003, 3001, 'title new 3', 33, 0, 'content new 3', '2018-06-28 02:00:00', '2018-06-30 22:22:00');
INSERT INTO news VALUES (4004, 3004, 'title new 4', 99, 1, 'content new 4', '2018-06-28 13:00:00', '2018-06-30 11:40:00');
INSERT INTO news VALUES (4005, 3007, 'title new 5', 55, 1, 'content new 5', '2018-06-28 22:00:00', '2018-06-30 01:30:00');
INSERT INTO news VALUES (4006, 3003, 'title new 6', 22, 1, 'content new 6', '2018-06-28 20:00:00', '2018-06-30 10:11:00');
INSERT INTO news VALUES (4007, 3002, 'title new 7', 32, 1, 'content new 7', '2018-06-28 20:00:00', '2018-06-30 11:03:00');
INSERT INTO news VALUES (4008, 3005, 'title new 8', 11, 1, 'content new 8', '2018-06-28 03:47:00', '2018-06-30 11:34:00');
* insert comment
INSERT INTO comment VALUES (5007, 'blog', 2001, 1007, 'ok', '2018-06-30 06:00:00', '2018-06-30 06:00:00');
INSERT INTO comment VALUES (5002, 'news', 4003, 1003, 'ok', '2018-06-30 06:00:00', '2018-06-30 06:00:00');
INSERT INTO comment VALUES (5003, 'blog', 2007, 1002, 'ok', '2018-06-30 06:00:00', '2018-06-30 06:00:00');
INSERT INTO comment VALUES (5004, 'news', 4004, 1005, 'ok', '2018-06-30 06:00:00', '2018-06-30 06:00:00');
INSERT INTO comment VALUES (5005, 'news', 4001, 1001, 'ok', '2018-06-30 06:00:00', '2018-06-30 06:00:00');
INSERT INTO comment VALUES (5006, 'blog', 2005, 1002, 'ok', '2018-06-30 06:00:00', '2018-06-30 06:00:00');
* truy vấn: 
DELETE FROM comment 
WHERE target_table ='blog' AND target_id ='2005' AND user_id ='1002';

# 8. Lấy 3 blog bất kỳ (random)
SELECT * FROM blog
ORDER BY RAND()
LIMIT 3;
# 9. Lấy số lượng comment của các blog
SELECT target_table, target_id, COUNT(id) as SL FROM comment 
WHERE target_table='blog'
GROUP BY target_id, target_table;
# 10. Lấy Category có tồn tại blog hoặc news đã active (không được lặp lại category)
SELECT * FROM category
WHERE category.id IN (SELECT blog.category_id FROM blog WHERE blog.is_active =1)
		OR category.id IN (SELECT news.category_id FROM news WHERE news.is_active =1) ;
# 11. #Lấy tổng lượt view của từng category thông qua blog và news
CREATE TABLE  view_blog  SELECT  blog.category_id,  sum(view) as SL FROM  blog 
GROUP  BY  category_id;

CREATE  TABLE  view_news  SELECT  news.category_id,   sum(view) as SL  FROM  news 
GROUP BY  category_id;
    
SELECT  * FROM  view_blog  as  b  JOIN  view_news  as n  
ON  b.category_id  =  n.category_id;
# 12. Lấy blog được tạo bởi user mà user này không có bất kỳ comment ở blog
SELECT * FROM blog 
WHERE blog.user_id NOT IN (
	SELECT user.id FROM user JOIN comment 
	ON user.id = comment.user_id
	GROUP BY user.id); 
# 13. Lấy 5 blog mới nhất và số lượng comment cho từng blog
SELECT *, SL FROM blog JOIN 
(SELECT comment.target_id, COUNT(user_id) AS SL
	FROM comment
	GROUP BY comment.target_id) AS countcmt
ON blog.category_id =  countcmt.target_id
ORDER BY  blog.created_at DESC
LIMIT 5;

# 14. Lấy 3 User comment đầu tiên trong 5 blogs mới nhất
SELECT user.id, user.full_name, user.email, user.rank, user.is_active, user.created_at
FROM blog JOIN user ON blog.user_id = user.id JOIN comment ON user.id =  comment.user_id
GROUP BY user.id
ORDER BY blog.created_at DESC, comment.created_at DESC
LIMIT 3;

# 15. Update rank user = 2 khi tổng số lượng comment của user > 20
* Tạo bảng ‘amountcmt ’ truy vấn để đếm số comment của mỗi user_id
CREATE TABLE amountcmt AS 
	SELECT comment.user_id, COUNT(comment.id) AS SL 
	FROM comment
	GROUP BY comment.user_id;
*Thực hiện truy vấn theo đề ra
UPDATE user  JOIN amountcmt ON user.id = amountcmt.user_id 
set user.rank = 2 
WHERE amountcmt.SL > 20;
  
# 16. #Xoá comment mà nội dung comment có từ "fuck" hoặc "phức"
SELECT * FROM `comment` WHERE comment = 'fruck' AND comment = 'phức';

# 17. Select 10 blog mới nhất được tạo bởi các user active
SELECT * FROM blog JOIN user ON blog.user_id = user.id
WHERE user.is_active = '1'
ORDER BY  blog.created_at DESC
LIMIT 10

# 18. Lấy số lượng Blog active của user có id là 1,2,4
SELECT blog.user_id , count( blog.id) AS SL  FROM blog JOIN user ON blog.user_id = user.id
WHERE  user.id  IN (1,2,3)
GROUP BY blog.user_id;

# 19. Lấy 5 blog và 5 news của 1 category bất kỳ
SELECT * FROM blog JOIN news ON  blog.category_id =  news.category_id
GROUP BY blog.id, news.id
ORDER BY RAND()
LIMIT 5;

# 20. Lấy blog và news có lượt view nhiều nhất
* blog có view nhiều nhất
SELECT  *  FROM  blog
ORDER  BY  view  DESC
LIMIT 1;
* news có view nhiều nhất
SELECT  *  FROM  news
ORDER  BY  view DESC
LIMIT 1;

# 21. Lấy blog được tạo trong 3 ngày gần nhất
SELECT * FROM blog 
WHERE DATEDIFF(CURDATE(), blog.created_at) <3;

# 22. Lấy danh sách user đã comment trong 2 blog mới nhất
SELECT blog.user_id FROM blog 
WHERE blog.id IN (
    SELECT * FROM blog  
	ORDER BY blog.created_at DESC
    LIMIT 2;
	);

SELECT blog.user_id FROM blog 
WHERE blog.id  IN(
	SELECT  TOP 2 blog.id FROM blog  
	ORDER BY blog.created_at DESC
    )

# 23. Lấy 2 blog, 2 news mà user có id = 1 đã comment
SELECT * FROM blog JOIN news ON  blog.category_id =  news.category_id
WHERE blog.user_id = 1
LIMIT 2;

# 24. Lấy 1 blog và 1 news có số lượng comment nhiều nhất
* Tạo bảng lấy số lượng comment nhiều nhất của 1 blog
 CREATE TABLE max_cmt_news AS
 	SELECT comment.target_id, COUNT(comment.id) as SL FROM comment
	WHERE comment.target_table = 'blog' 
    GROUP BY comment.target_id
	LIMIT 1
* Tạo bảng lấy số lượng comment nhiều nhất của 1 news
 CREATE TABLE max_cmt_news AS
 	SELECT comment.target_id, COUNT(comment.id) as SL FROM comment
	WHERE comment.target_table = 'news' 
    GROUP BY comment.target_id
	LIMIT 1
* Truy vấn
SELECT * FROM blog 
WHERE blog.id IN (SELECT max_cmt_blog.target_id FROM max_cmt_blog);

SELECT * FROM news 
WHERE news.id IN (SELECT max_cmt_news.target_id FROM max_cmt_news);

# 25. Lấy 5 blog và 5 news mới nhất đã active
* 5 blog  mới nhất đã active
SELECT * FROM blog 
WHERE blog.is_active = 1
ORDER BY blog.created_at DESC
LIMIT 5;
* 5 news mới nhất đã active
SELECT * FROM  news
WHERE  is_active = 1
ORDER BY  created_at DESC
LIMIT 5;

# 26. Lấy nội dung comment trong blog và news của user id =1
SELECT comment FROM comment
WHERE comment.user_id =1;

# 27. Blog của user đang được user có id = 1 follow
SELECT blog.id FROM blog JOIN user 
ON blog.user_id = user.id JOIN follow ON user.id =  follow.from_user_id
WHERE follow.from_user_id =1;

# 28. Lấy số lượng user đang follow user = 1
SELECT  to_user_id,  COUNT(from_user_id)  as SL   FROM  follow
WHERE  to_user_id  = 1
GROUP  BY  to_user_id;

# 29. Lấy số lượng user 1 đang follow
SELECT  from_user_id,  COUNT(to_user_id)  as  SL   FROM  follow
WHERE  from_user_id  = 1
GROUP  BY  from_user_id;

# 30. Lấy 1 comment(id_comment,  comment) mới nhất và thông tin user của user đang được follow bởi user 1
SELECT user.id, user.full_name, user.email, user.rank, user.is_active, user.created_at, comment.id, comment.comment
FROM follow JOIN user ON follow.from_user_id = user.id
JOIN comment ON user.id =  comment.id
WHERE follow.from_user_id = 1
ORDER BY comment.created_at DESC
LIMIT 1


# 31. Hiển thị một chuổi "PHP Team " + ngày giờ hiện tại (Ex: PHP Team 2017-06-21 13:06:37)
SELECT STR('PHP Team ' + CURDATE() );
# 32. Tìm có tên(user.full_name) "Khiêu" và các thông tin trên blog của user này như: (blog.title, blog.view), title category(category) của blog này. Hiển thị theo output như bên dưới:

# 33. Liệt kê email user các user có tên(user.full_name) có chứa ký tự "Khi" theo danh sách như output bên dưới.


# 34. Tính điểm cho user có email là minh82@example.com trong bảng comment. Cách tính điểm:
 Trong bảng comment với taget_table = "blog" tính 1 điểm, taget_table = "news" tính 2 điểm.



