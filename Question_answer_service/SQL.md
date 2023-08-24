# Примеры SQL-запросов


Задание:

Сколько в среднем очков получает пост каждого пользователя?

SQL-запрос:
``` sql
SELECT title,
       user_id,
       score,
       ROUND(AVG(score) OVER (PARTITION BY user_id)) AS avg_score
FROM stackoverflow.posts
WHERE title IS NOT NULL 
AND NOT score = 0;
```

Задание:

Посчитайте ежедневный прирост новых пользователей в ноябре 2008 года. Сформируйте таблицу с полями:
- номер дня;
- число пользователей, зарегистрированных в этот день;
- сумму пользователей с накоплением.

SQL-запрос:
``` sql
WITH  cnt_users AS
        (SELECT EXTRACT(DAY FROM creation_date) AS num_day,
               COUNT(id) AS cnt_us
        FROM stackoverflow.users
        WHERE EXTRACT(MONTH FROM creation_date) = 11 
         AND EXTRACT(YEAR FROM creation_date) = 2008
        GROUP BY num_day)
SELECT num_day,
       cnt_us,
       SUM(cnt_us) OVER (ORDER BY num_day)
FROM cnt_users;       
```
    
Задание:

Для каждого пользователя, который написал хотя бы один пост, найдите интервал между регистрацией и временем создания первого поста. Отобразите:
- идентификатор пользователя;
- разницу во времени между регистрацией и первым постом.

SQL-запрос:
```sql
WITH first_date AS
    (SELECT DISTINCT user_id,
           FIRST_VALUE(creation_date) OVER(PARTITION BY user_id ORDER BY creation_date) AS first_post
    FROM stackoverflow.posts)
SELECT user_id,
       first_post - creation_date
FROM first_date AS fd 
LEFT JOIN stackoverflow.users AS us ON fd.user_id=us.id;
```