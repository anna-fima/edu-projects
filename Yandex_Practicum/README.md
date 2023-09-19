# Проекты по курсу "Аналитик Данных"

В этом репозитории собраны проекты, выполненные мной в ходе прохождения курса "Аналитик данных" от Яндекс Практикума.

Обучаясь на данном курсе и работая над проектами,  я освоила основы Python (и его основные библиотеки pandas, numpy, matplotlib, seaborn),
 SQL, Tableau, научилась профессионально работать с данными - обрабатывать данные, уточнять задачи, выдвигать и проверять гипотезы,
 исследовать данные, визуализировать и формулировать выводы.

| Название проекта | Описание проекта | Навыки и инструменты |
| :--------------- | :--------------- | :--------------- |
| [Анализ данных сервиса "Яндекс Музыка" - сравнение поведения пользователей двух городов](Music_big_cities) | Сравнение музыкальных предпочтений пользователей Яндекс.Музыка в Москве и Санкт-Петербурге в зависимости от дня недели и времени | Python, pandas | 
| [Исследование платежеспособности клиентов на основе данных кредитного отдела банка](Credit_repayment_for_bank) | Исследование влияния семейного положения, количества детей клиента и других факторов на погашение кредита в срок на основе статистики платежеспособности клиентов, предоставленной кредитным отделом банка | Python, pandas |
| [Анализ рынка недвижимости - продажа квартир в Санкт-Петербурге](Real_estate_market_analysis) | На основе данных сервиса Яндекс Недвижимость проанализирован архив объявлений по продаже квартир в Санкт-Петербурге, изучены и определены параметры, позволяющие спрогнозировать рыночную стоимость квартиры | Python, pandas, numpy, matplotlib |
| [Анализ и определение выгодного тарифа для телеком-компании](Profitable_tariff_for_telecom_company) | Анализ поведения клиентов и определение оптимального тарифа на основе данных клиентов оператора сотовой связи. Проверены статистические гипотезы на основе имеющихся данных  | Python, pandas, numpy, matplotlib, scipy.stats |
| [Анализ закономерностей, определяющих успешность игр](Successful_game) | Используя исторические данные о продажах компьютерных игр, оценки пользователей и экспертов, жанры и платформы, выявлены закономерности, определяющие успешность игры. Выбран актуальный период для анализа. Составлены портреты пользователей каждого региона. Проверены гипотезы  | Python, pandas, numpy, matplotlib, scipy.stats |
| [Исследование данных об инвестиции венчурных фондов в компании-стартапы](Investment_funds) | Проанализировать данные о фондах и инвестициях и написать запросы к базе с помощью SQL | SQL |
| [Анализ бизнес-показателей приложения Procrastinate Pro+](ProcrastinatePRO_app_analysis) | Проанализированы бизнес-показатели развлекательного приложения Procrastinate Pro+, определены причины неэффективности привлечения пользователей и сделаны рекомендации рекламному отделу. Рассчитаны различные метрики, использован когортный анализ: LTV, CAC, Retention rate, DAU, WAU, MAU  | Python, pandas, numpy, matplotlib, когортый анализ, продуктовые метрики|
| [Проверка гипотез по увеличению выручки в интернет-магазине — оценить результаты A/B теста](AB_test) | Проведена приоритизация гипотез по фреймворкам ICE и RICE. Проведен анализ результатов A/B-теста, построила графики кумулятивной выручки, среднего чека, конверсии по группам, а затем посчитал статистическую значимость различий конверсий и средних чеков по сырым и очищенным данным. На основании анализа мной было принято решение о нецелесообразности дальнейшего проведения теста | Python, pandas, numpy, matplotlib, A/B-тестирование, проверка статистических гипотез|
| [Исследования рынка общепита в Москве для принятия решения об открытии нового заведения](Catering_market_analysis) | Подготовлено исследование рынка на основе открытых данных о заведениях общественного питания Москвы, визуализированы полученные данные. На основе данных выбрано место для открытия нового заведения | Python, pandas, numpy, matplotlib, seaborn, plotly|
| [Анализ пользовательского поведения в мобильном приложении](Mobile_application) | Построила воронку продаж, исследовала путь пользователей до покупки. Проанализировала результаты A/B-теста введения новых шрифтов. Сравнила 2 контрольных группы между собой, убедилась в правильном разделении трафика, а затем сравнила с тестовой группой. Выявлено, что новый шрифт значительно не повлияет на поведение пользователей. | Python, pandas, numpy, matplotlib, plotly,  А/В тестирование, проверка статистических гипотез|
| [Анализ сервиса вопросов и ответов по программированию](Question_answer_service) | Написала SQL-запросы для подсчёта требуемых значений и метрик | SQL, PostgreSQL |
| [Анализ взаимодействия пользователей с карточками Яндекс.Дзен](Tableau_dashboard) | Подготовлен интерактивный дашборд на основе данных о взаимодействии пользователей с карточками. Для создания дашбордов использован BI-инструмент Tableau | Tableau|
| [Прогноз оттока клиентов в сети фитнес-центров](Gym_churn) | Спрогнозировала вероятность оттока в следующем месяце для каждго клиента, для этого построила модель бинарной классификации и выбрали наиболее удачный алгоритм "логистическая регрессия". С помощью кластеризации выделила 5 наиболее ярких групп клиентов и охарактеризовала их основные свойства. Проанализировала признаки, наиболее сильно влияющие на отток | Python, pandas, seaborn, matplotlib, sklearn|
| [Выявление профилей потребления](E_commerce_profiles) | Проанализировала товары магазина, сделала категоризацию, выделив 8 категорий товаров, провела кластеризацию клиентов по количеству заказов, среднему чеку и среднему числу наименований в заказе и выделила 4 кластера покупателей, нашла приоритетные категории товаров для каждого клиента и посмотрела на распределение приоритетных категорий в каждом кластере, на основании этих выводов сделала персонализированные предложения для клиентов, проверила статистические гипотезы  | Python, pandas, seaborn, matplotlib, sklearn, scipy, plotly|
