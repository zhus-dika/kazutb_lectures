## План лабораторных работ

| Занятие | Тема | Самостоятельно | На занятии | Домашнее задание / сдача | Дедлайн |
|---:|---|---|---|---|---|
| **1** | Табличные данные (Polars) | Изучить ноутбук: https://github.com/esokolov/ml-course-hse/blob/master/2025-fall/seminars/sem01-polars.ipynb | Разбор ключевых операций Polars: чтение данных, фильтрация, join, groupby/agg, типы данных | Выполнить ноутбук: https://github.com/esokolov/ml-course-hse/tree/master/2025-fall/homework-practice/homework-practice-01-tabular (сдать ноутбук + результаты ячеек) | **через 2 недели после занятия 1** |
| **2** | Визуализация (Charts) + сбор данных (альтернативный трек) | Изучить ноутбук: https://github.com/esokolov/ml-course-hse/blob/master/2025-fall/seminars/sem02-charts.ipynb | 1) Разбор графиков из ноутбука. 2) Постановка задачи по сбору данных **без полного EDA** (сбор + таблица + минимальные проверки качества) | **Лаб 2 (сбор данных из локальных HTML):** выбрать сайт/тему (космос/медицина/наука и т.д.), сохранить *Save As* **3 страницы** листинга и **10 страниц** объектов, распарсить локально, собрать таблицу (≥1000 строк, ≥15 столбцов, ≥5 информативных), приложить код + таблицу | **через 2 недели после занятия 2** |
| **3** | Скоро появится | — | — | — | — |
| **4** | Скоро появится | — | — | — | — |
| **5** | Скоро появится | — | — | — | — |
| **6** | Скоро появится | — | — | — | — |
| **7** | Скоро появится | — | — | — | — |
| **8** | Скоро появится | — | — | — | — |

## Лабораторная №2: Сбор данных из открытых источников (Open Data / API)

### Цель
Научиться **находить**, **законно использовать**, **программно получать** и **собирать** датасет из открытых источников (API/порталы/репозитории), приводить его к **табличному виду** и документировать процесс.

### Алгоритм выполнения (шаги)
1) Выбрать тему + сформулировать исследовательский вопрос.  
2) Найти открытый источник данных, проверить лицензию/условия использования.  
3) Спроектировать таблицу: что является строкой (страна-год, объект, станция-день и т.п.).  
4) Реализовать скачивание: запросы, пагинация, параметры, сохранение raw.  
5) Нормализовать данные: привести к таблице (flat), типы, даты, единицы измерения.  
6) Очистить: пропуски, дубликаты, выбросы (минимум — отчёт по пропускам).  
7) Сделать базовый анализ/EDA: 2–3 графика или группировки + краткие выводы.  
8) Документировать: schema + data dictionary + ограничения/смещения.

---

### Варианты (выберите 1 или придумайте сами)

1) Космические данные
Примеры: астероиды/экзопланеты/миссии/объекты наблюдений.  
Рекомендуемые источники:
- NASA Open APIs: https://api.nasa.gov/
- NASA Exoplanet Archive API: https://exoplanetarchive.ipac.caltech.edu/docs/program_interfaces.html
- JPL Small-Body Database API: https://ssd-api.jpl.nasa.gov/doc/sbdb.html

2) Экология и климат
Примеры: погода, качество воздуха, климатические ряды, наблюдения по станциям.  
Рекомендуемые источники:
- OpenAQ (Air Quality): https://docs.openaq.org/
- NOAA Climate Data Online API: https://www.ncdc.noaa.gov/cdo-web/webservices/getstarted
- Open-Meteo (Weather API): https://open-meteo.com/

3) Медицина и общественное здоровье
Только агрегированные показатели (страна/регион/год), без персональных данных.  
Рекомендуемые источники:
- WHO GHO OData API: https://www.who.int/data/gho/info/gho-odata-api
- CDC Open Data (Socrata каталог): https://data.cdc.gov/
- Документация Socrata API (если используешь CDC): https://dev.socrata.com/

4) Экономика и социальные индикаторы
Показатели по странам/регионам/годам (индикаторы развития, демография и т.п.).  
Рекомендуемые источники:
- World Bank Indicators API: https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-about-the-indicators-api-documentation
- OECD API (страница-пояснение): https://www.oecd.org/en/data/insights/data-explainers/2024/09/api.html
- Казахстан (портал открытых данных): https://data.egov.kz/

5) Транспорт и мобильность
Поездки/расписания/маршруты/нагрузка по времени и географии.  
Рекомендуемые источники:
- NYC TLC Trip Record Data: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page
- OpenStreetMap (как скачать данные): https://wiki.openstreetmap.org/wiki/Downloading_data

6) Научные публикации и библиометрия
Метаданные статей/препринтов: год, темы, авторы, журнал и т.п.  
Рекомендуемые источники:
- Crossref REST API: https://www.crossref.org/documentation/retrieve-metadata/rest-api/
- OpenAlex API (Works): https://docs.openalex.org/api-entities/works
- arXiv API (User Manual): https://info.arxiv.org/help/api/user-manual.html
- PLOS Search API: https://api.plos.org/text-and-data-mining.html

7) Новости и события
События/упоминания/динамика по времени и регионам.  
Рекомендуемые источники:
- GDELT Project: https://www.gdeltproject.org/

8) Энергетика и устойчивое развитие
Потребление/производство энергии, доля ВИЭ, выбросы и т.п.  
Рекомендуемые источники:
- Our World in Data — Energy (репозиторий): https://github.com/owid/energy-data
- Data.gov (каталог открытых датасетов США): https://catalog.data.gov/
