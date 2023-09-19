# Примеры SQL-запросов


Задание:

Составьте сводную таблицу и выведите среднюю сумму инвестиций для стран, в которых есть стартапы, зарегистрированные в 2011, 2012 и 2013 годах. Данные за каждый год должны быть в отдельном поле. Отсортируйте таблицу по среднему значению инвестиций за 2011 год от большего к меньшему.

SQL-запрос:
```sql
SELECT a.country_code,
       a.avg_funding_2011,
       b.avg_funding_2012,
       c.avg_funding_2013
FROM
    (SELECT country_code,
           AVG(funding_total)  AS avg_funding_2011
    FROM company
    WHERE EXTRACT(YEAR FROM CAST(founded_at AS timestamp)) = 2011
    GROUP BY country_code) AS a
INNER JOIN 
        (SELECT country_code,
               AVG(funding_total)  AS avg_funding_2012
        FROM company
        WHERE EXTRACT(YEAR FROM CAST(founded_at AS timestamp)) = 2012
        GROUP BY country_code) AS b ON a.country_code = b.country_code
INNER JOIN 
        (SELECT country_code,
               AVG(funding_total)  AS avg_funding_2013
        FROM company
        WHERE EXTRACT(YEAR FROM CAST(founded_at AS timestamp)) = 2013
        GROUP BY country_code) AS c ON a.country_code = c.country_code        
ORDER BY a.avg_funding_2011 DESC; 
```

Задание:

Выгрузите таблицу, в которую войдут названия компаний из категории social, получившие финансирование с 2010 по 2013 год включительно. Проверьте, что сумма инвестиций не равна нулю. Выведите также номер месяца, в котором проходил раунд финансирования.

SQL-запрос:
```sql
SELECT c.name,
       f.month
FROM        
    (SELECT company_id,
           EXTRACT(MONTH FROM CAST(funded_at AS timestamp)) AS month
    FROM funding_round
    WHERE EXTRACT(YEAR FROM CAST(funded_at AS timestamp)) BETWEEN 2010 AND 2013) AS f
INNER JOIN company AS c ON f.company_id=c.id    
WHERE c.category_code = 'social'
```   