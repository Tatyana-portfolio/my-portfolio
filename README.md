# Портфолио: аналитик данных 
## Обо мне
Привет! Меня зовут Татьяна, я начинающий аналитик данных. В этом репозитории вы можете найти некоторые из моих проектов, выполненных во время обучения и практики.

## Навыки и технологии
- Инструменты анализа данных: SQL, Excel:
- Языки программирования и библиотеки: Python
- Системы управления базами данных: MySQL, PostgreSQL
- Средства визуализации данных: PowerBi

## Проекты
Проект 1: Калькулятор юнит-экономики онлайн-школы

Что нужно было сделать: 

Задача №1. На какую сумму мы могли бы увеличить расходы на основных сотрудников (Fixed costs / ФОТ) в апреле 2021 года при условии, что маржинальность в этом месяце не должна упасть ниже 11%?  
Задача №2. Какой станет маржинальность за март 2021, если доля бесплатных уроков в нем упадет на 10 процентных пунктов? При этом общее количество уроков не изменится — просто часть бесплатных уроков мы продадим за полную цену в 1200 ₽.  

Как решала:  Воспользовалась данными на листе «Свод». Допустим что маржинальность апреля 2021 года равна 11%, при этом выручка, ЗП учителей и CAC не изменились. Расчитала насколько больше ФОТ, чем был по факту в апреле 2021 года.  Воспользовалась листом classes и посчитала доли уроков разной цены в марте 2021 года.  Рассчитав долю бесплатных уроков (представила, что было бы, если бы их было на 10 процентных пунктов меньше, а уроков за 1200 рублей на то же количество уроков больше). Расчитала выручку.  Воспользовалась данными на листе «Свод». Увеличила текущий рассчитанный средний ретеншен (88,55%)  на 2 процентных пункта и пересчитала лайфтайм. Не меняя среднюю интенсивность и среднюю цену урока, пересчитала LTR. Для апреля 2021 год пересчитала долю расходов на привлечение %CAC при том, что сам CAC в абсолютном выражении останется прежним — на уровне 13140,72 ₽. Рассчитала новое значение маржинальности. На листе «Свод» подставила в март получившуюся рассчетную выручку. Рассчитала маржинальность

Ссылка на проект 
[Калькулятор юнит-экономики онлайн-школы.xlsx](https://github.com/Tatyana-portfolio/my-portfolio/files/12573046/-.-.xlsx)

Выводы (итоги):

Итог №1 Сумма на которую мы могли бы увеличить расходы на основных сотрудников (Fixed costs / ФОТ) в апреле 2021 года = 358596,32 руб.  
Итог №2 Маржинальность за март 2021 вырастет на 10%

### Проект 2: Калькулятор юнит-экономики онлайн-кинотеатра

Что нужно было сделать:

Задача №1. Визуализируйте количество фильмов и сериалов Netflix с агрегацией по году выхода.  
Задача №2. Получите наименования лучших 250 фильмов.  
Задача №3. У вас есть подписка на Netflix и вы хотите использовать ее самым эффективным образом — посмотреть все лучшие фильмы. Рассчитайте, сколько времени на это потребуется.  

Как решала: Создала сводную таблицу для подсчета количества фильмов и сериалов по годам (назвала столбец release_year).Визуализировала получившиеся числа с помощью диаграммы. Импортировала список лучших фильмов с сайта http://top250.info/charts/?2023/07/13. Создала копию столбца Rank & Title и очиститила ее так, чтобы вытащить только названия. С помощью ВПР() определитла, какие из лучших тайтлов с сайта IMDB (с помощью очищенных в прошлой задаче данных) есть на платформе Netflix (в датасете netflix_titles). Выделила из них только фильмы (для которых в поле type значение Movie). Вытащила данные о продолжительности таких фильмов, очистив столбец duration (продолжительность). Просуммировала продолжительность всех этих фильмов и перевела в часы.

Ссылка на проект [Калькулятор юнит-экономики онлайн кинотеатра.xlsx](https://github.com/Tatyana-portfolio/my-portfolio/files/12573902/-.xlsx)

Выводы (итоги):

Итог №1 Диаграмма с количеством фильмов и сериалов по годам.  
Итог №2 Столбец с названиями лучших 250 фильмов по версии IMDB.  
Итог №3 Посчитанное количество часов, которое придется потратить на просмотр лучших фильмов, доступных на Netflix.

Проект 3: Когортный анализ онлайн-кинотеатра с помощью SQL

Что нужно было сделать:

Задача №1 Вывести названия всех фильмов, в которых участвует Хоакин Феникс (Joaquin Phoenix) — победитель номинации за лучшую мужскую роль.  
Задача №2. Дать названия всех сериалов, в которых участвует Рене Зеллвегер (Renée Zellweger) — победительница номинации за лучшую женскую роль.  
Задача №3. Дать всю имеющуюся информацию о не слишком старых фильмах производства Netflix, которые сняли режиссеры пяти главных фильмов 2020 года по версии «КиноПоиска»: https://www.kinopoisk.ru/awards/oscar/2020/.  
Задача №4. Проверить, есть ли у Netflix фильмы, за игру в которых актеры получили «Оскар» в 2020 году.

Как решала:  
![ScreenShot 11 09 23](https://github.com/Tatyana-portfolio/my-portfolio/assets/144625847/2a743315-de83-4f34-93bb-209fb8111a4f)  
![ScreenShot (2) 11 09 23](https://github.com/Tatyana-portfolio/my-portfolio/assets/144625847/2a6947f7-561c-425a-b99e-6c2ad598b772)
![ScreenShot (3) 11 09 23](https://github.com/Tatyana-portfolio/my-portfolio/assets/144625847/f62952dd-12a2-4830-9ac3-87eca6a18b15)
![ScreenShot (4)11 09 23](https://github.com/Tatyana-portfolio/my-portfolio/assets/144625847/f1c660a2-03ce-4cb5-a831-19cbed20ea9a)

Выводы (итоги):

Итог №1 Вывела название всех фильмов, сериалов
Итог №2 Предоставила всю имеющуюся информацию о фильмах и сериалах.

Проект 4: Построение витрины для модели машинного обучения в банке

Что нужно было сделать: задача №1.

Как решала(-а): краткое описание решения (автореферат)

Ссылка на проект (ссылка должна содержать демонстративные материалы: скриншоты, таблички, запросы, код. Работодатель должен иметь возможность быстро посмотреть результаты работы)

Выводы (итоги):

Итог №1
Итог №2

Проект 5: Моделирование изменения балансов студентов

Что нужно было сделать:

Задача №1
Задача №2.
Как решала(-а): краткое описание решения (автореферат)

Ссылка на проект (ссылка должна содержать демонстративные материалы: скриншоты, таблички, запросы, код. Работодатель должен иметь возможность быстро посмотреть результаты работы)

Выводы (итоги):

Итог №1
Итог №2

Контактная информация
Email: zinnurova_t@inbox.ru
