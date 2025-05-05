# DS_Analytical_Project_2025


# Intro

Привет, команда!

Этот проект — это ваш шанс проявить себя как настоящие аналитики данных. Мы не просто будем работать с цифрами и графиками, а создавать **реальные истории**, которые могут повлиять на важные решения. И это не просто еще одно задание — это ваша **карта в будущее**, которая поможет вам выделиться перед работодателями.

Почему это важно? Потому что в мире Data Science решают не только те, кто хорошо умеет работать с инструментами, но и те, кто может **самостоятельно решать реальные задачи**. Этот проект даст вам возможность доказать, что вы способны не только анализировать данные, но и находить инсайты, которые можно применить в бизнесе или других сферах. Ваши результаты — это часть вашего **портфолио**, которое будет полезно при поиске работы.

Кроме того, вы будете работать **в команде**, обмениваться идеями и учиться друг у друга. В Data Science умение работать с коллегами и коммуницировать результаты — важная часть работы, и этот проект даст вам практику в этом.

Не переживайте, если что-то будет сложно. Вместе мы справимся с любыми трудностями! Мы будем поддерживать друг друга на каждом шаге. Верьте в себя, в команду, и помните, что каждая ошибка — это просто шаг к успеху.

Вперед, команда! Результаты удивят вас!

--- 

# **Родмап для аналитического проекта по Data Science**

#### **1. Выбор датасета и тематики**

- **Задача**: Выбрать интересный и доступный датасет, подходящий для анализа.
- **Рекомендации**:
  - Оцените доступность данных (например, через платформы типа Kaggle, UCI Machine Learning Repository, или открытые данные).
  - Датасет должен быть достаточно объемным для того, чтобы можно было провести глубокий анализ, но не слишком сложным.
  - Примерные тематики: финансы, здравоохранение, маркетинг, спорт, социальные сети, экология, транспорт и т.д.
  - Отличной практикой является выбор темы, которая интересна именно Вам!
  - Также можно зпросить датасет у Нас (рынок авто, рынок недвижимости, данные по качеству воздуха, климату и погоде)
- **Результат**: Обоснованный выбор датасета и сформулированная тема для анализа.

---

#### **2. Первая очистка данных**

- **Задача**: Провести предварительный анализ и подготовку данных для дальнейшего анализа.
- **Шаги**:
  1. **Оценка пропущенных значений**:
     - Использовать методы, такие как `.isnull()`, `.sum()`, `info()` для анализа пропусков.
     - Оценить масштаб проблем и сделать первоначальные предположения касательно работы с пропусками (удаление, удаление колонок, заполнение, умное заполнение, ингорирование пропусков)
  2. **Удаление дубликатов**:
     - Использовать методы `.duplicated()` и `.drop_duplicates()`.
  3. **Проверка типов данных**:
     - Используйте `.dtypes`, `info()` для проверки типов данных.
     - Преобразуйте их в правильные типы (например, преобразование категориальных переменных в категориальные типы `category`, преобразование числовых значений в `float` или `int`).
  4. **Обработка аномалий**:
     - Используйте визуализации (например, boxplot, histograms) для выявления выбросов.
     - Предположить, как обрабатывать выбросы (удаление, замена или оставление).

- **Результат**: Чистые и подготовленные данные, готовые к анализу.

---

#### **3. Экспресс-анализ (Descriptive Analysis)**

- **Задача**: Провести начальную визуализацию и анализ для понимания структуры данных.
- **Шаги**:
  1. **Общие статистики**:
     - Для количественных признаков используйте методы `.describe()`, `.mean()`, `.std()`.
  2. **Построение графиков**:
     - **Гистограммы** (для изучения распределений количественных признаков).
     - **Boxplot** (для выявления выбросов).
     - **Плотности распределений** (с помощью `seaborn.kdeplot`) включая распределения по группам.
     - **Скаттер-плоты** (для исследования взаимозависимости количественных признаков).
     - **Парные графики (pairplot)** для выявления возможных связей между признаками.
     - **Графики для категориальных признаков**:
       - Столбчатые диаграммы для визуализации распределения категорий.
       - **Pie chart** для просмотра долей различных категорий.
  3. **Анализ взаимозависимостей**:
     - Построение корреляционных матриц для количественных признаков.
     - Использование scatter plot для отображения зависимостей между переменными.
     - Выявление корреляций между переменными (проверка на multicollinearity).
  4. **Анализ категориальных признаков**:
     - Оценка количества уникальных категорий, их частоты.
     - Проверка на дисбаланс классов в категориальных данных.
  
- **Результат**: Визуализированные данные, которые помогут выявить паттерны и аномалии в данных.

---

#### **4. Формулировка гипотез и вопросов**

- **Задача**: Сформулировать гипотезы и вопросы, которые можно проверить в процессе анализа.
- **Рекомендации**:
  - Гипотезы должны быть сформулированы на основе выводов из экспресс-анализа.
  - Например, гипотеза может быть такой: "Есть ли зависимость между уровнем дохода и удовлетворенностью клиентов?"
  - Вопросы могут быть как описательными, так и направленными на поиск причинно-следственных связей.
  
- **Результат**: Четкие гипотезы и вопросы, которые будут исследоваться в дальнейшем.

---

#### **5. Глубокий анализ и проверка гипотез**

- **Задача**: Использовать статистические методы для проверки гипотез и извлечения инсайтов.
- **Шаги**:
  1. **Тестирование гипотез**:
     - Применение статистических тестов, таких как t-test, ANOVA, Chi-Square, для проверки гипотез (если применимо).
     - Например, если гипотеза о разнице между группами, используйте t-test для независимых выборок.
  2. **Регрессионный анализ** (если применимо):
     - Оценка зависимости между переменными через линейную регрессию (для количественных признаков).
  3. **Кросс-табуляция и анализ категориальных данных**:
     - Использование кросс-табуляции для анализа связи между категориальными переменными.
  4. **Построение графиков для поддержки гипотез**:
     - Для каждой гипотезы подготовить графики, которые иллюстрируют результаты анализа.
  
- **Результат**: Проверенные гипотезы с соответствующими статистическими выводами и графиками.

---

#### **6. Формулировка инсайтов и подготовка отчета**

- **Задача**: Извлечь ключевые инсайты из данных и подготовить финальный отчет.
- **Шаги**:
  1. **Инсайты**:
     - На основе анализа данных сформулируйте ключевые выводы и инсайты.
     - Например, "Молодые люди чаще покупают продукт X, чем старшее поколение".
  2. **Подготовка отчета**:
     - Структура отчета:
       1. Введение (описание целей и задач анализа).
       2. Описание данных (источник, переменные, типы данных).
       3. Процесс очистки данных.
       4. Описание визуализаций и основных выводов.
       5. Обсуждение гипотез и выводов.
       6. Заключение (включая рекомендации, если это применимо).
  3. **Дашборд (по желанию)**:
     - Построить дашборд с ключевыми метриками и визуализациями с помощью таких инструментов как `Dash`, `Streamlit` или `Tableau`.
  
- **Результат**: Полный отчет с выводами и презентация для защиты.

---

#### **7. Презентация и защита проекта**

- **Задача**: Представить проект перед группой и преподавателем.
- **Шаги**:
  - Подготовить презентацию, в которой будет изложен весь процесс работы с данными: от выбора датасета до выводов и инсайтов.
  - Использовать графики и диаграммы для визуализации ключевых моментов.
  - Подготовить ответы на возможные вопросы.

- **Результат**: Презентация и успешная защита проекта.

---
# Временные рамки

<img width="581" alt="image" src="https://github.com/user-attachments/assets/079c2b6c-8c38-4649-823b-0e3cf16c35fa" />


# IQAir Dataset Bishkek

`QIair_Bishkek_data.csv`

### Описание датасета

Данный датасет содержит данные о качестве воздуха в Бишкеке, собранные на различных станциях мониторинга. Каждый ряд в датасете представляет собой информацию за один день по конкретной станции. Вот основные столбцы, которые присутствуют в данных:

1. **date** – дата измерений.
2. **min** – минимальное значение загрязнения воздуха за день.
3. **max** – максимальное значение загрязнения воздуха за день.
4. **median** – медианное значение загрязнения воздуха за день.
5. **q1** – первый квартиль (25-й процентиль) загрязнения воздуха.
6. **q3** – третий квартиль (75-й процентиль) загрязнения воздуха.
7. **stdev** – стандартное отклонение загрязнения воздуха.
8. **count** – количество измерений, сделанных в течение дня.
9. **station** – название станции мониторинга, с которой были собраны данные.
10. **latitude** – географическая широта станции.
11. **longitude** – географическая долгота станции.

### Пример данных

| **date**   | **min**  | **max**  | **median** | **q1**   | **q3**   | **stdev** | **count** | **station**      | **latitude** | **longitude** |
|------------|----------|----------|------------|----------|----------|-----------|-----------|------------------|--------------|---------------|
| 2019-12-13 | 15.16    | 255.77   | 34.53      | 21.03    | 98.56    | 83.69     | 193       | Кара-Балтинская  | 42.885263    | 74.554349     |
| 2019-12-14 | 6.75     | 70.45    | 25.34      | 14.08    | 47.86    | 18.56     | 175       | Кара-Балтинская  | 42.885263    | 74.554349     |
| 2019-12-15 | 32.54    | 769.79   | 155.93     | 96.87    | 478.88   | 221.72    | 572       | Кара-Балтинская  | 42.885263    | 74.554349     |

Эти данные позволяют анализировать изменения в уровне загрязнения воздуха в разных районах города и выявлять временные тренды и аномалии.


# Weather Data

### file: `open-meteo-42.85N74.53E760m.csv`

Данные собраны с использованием различных метеорологических инструментов, таких как метеостанции, спутники, радары и другие приборы, в том числе с автоматических метеостанций, которые записывают данные в реальном времени (ежечасно, ежедневно и т.д.). Временной интервал: 01.01.2018 - 02.05.2025. Наблюдения ежечасные.

[РЕСУРС и дока](https://open-meteo.com/en/docs/historical-weather-api?start_date=2018-01-01&end_date=2025-05-04&csv_coordinates=Bishkek&latitude=42.873&longitude=74.5895&hourly=temperature_2m,relative_humidity_2m,precipitation,apparent_temperature,rain,snow_depth,snowfall,surface_pressure,cloud_cover,cloud_cover_low,cloud_cover_mid,cloud_cover_high,wind_speed_10m,wind_speed_100m,wind_direction_10m,wind_direction_100m,wind_gusts_10m,dew_point_2m,pressure_msl&wind_speed_unit=ms)

Вы также можете скачать данные запустив код:

```bash
pip install openmeteo-requests
pip install requests-cache retry-requests numpy pandas
```

```python
import openmeteo_requests

import pandas as pd
import requests_cache
from retry_requests import retry

# Setup the Open-Meteo API client with cache and retry on error
cache_session = requests_cache.CachedSession('.cache', expire_after = -1)
retry_session = retry(cache_session, retries = 5, backoff_factor = 0.2)
openmeteo = openmeteo_requests.Client(session = retry_session)

# Make sure all required weather variables are listed here
# The order of variables in hourly or daily is important to assign them correctly below
url = "https://archive-api.open-meteo.com/v1/archive"
params = {
	"latitude": 42.873,
	"longitude": 74.5895,
	"start_date": "2018-01-01",
	"end_date": "2025-05-04",
	"hourly": ["temperature_2m", "relative_humidity_2m", "precipitation", "apparent_temperature", "rain", "snow_depth", "snowfall", "surface_pressure", "cloud_cover", "cloud_cover_low", "cloud_cover_mid", "cloud_cover_high", "wind_speed_10m", "wind_speed_100m", "wind_direction_10m", "wind_direction_100m", "wind_gusts_10m", "dew_point_2m", "pressure_msl"],
	"wind_speed_unit": "ms"
}
responses = openmeteo.weather_api(url, params=params)

# Process first location. Add a for-loop for multiple locations or weather models
response = responses[0]
print(f"Coordinates {response.Latitude()}°N {response.Longitude()}°E")
print(f"Elevation {response.Elevation()} m asl")
print(f"Timezone {response.Timezone()}{response.TimezoneAbbreviation()}")
print(f"Timezone difference to GMT+0 {response.UtcOffsetSeconds()} s")

# Process hourly data. The order of variables needs to be the same as requested.
hourly = response.Hourly()
hourly_temperature_2m = hourly.Variables(0).ValuesAsNumpy()
hourly_relative_humidity_2m = hourly.Variables(1).ValuesAsNumpy()
hourly_precipitation = hourly.Variables(2).ValuesAsNumpy()
hourly_apparent_temperature = hourly.Variables(3).ValuesAsNumpy()
hourly_rain = hourly.Variables(4).ValuesAsNumpy()
hourly_snow_depth = hourly.Variables(5).ValuesAsNumpy()
hourly_snowfall = hourly.Variables(6).ValuesAsNumpy()
hourly_surface_pressure = hourly.Variables(7).ValuesAsNumpy()
hourly_cloud_cover = hourly.Variables(8).ValuesAsNumpy()
hourly_cloud_cover_low = hourly.Variables(9).ValuesAsNumpy()
hourly_cloud_cover_mid = hourly.Variables(10).ValuesAsNumpy()
hourly_cloud_cover_high = hourly.Variables(11).ValuesAsNumpy()
hourly_wind_speed_10m = hourly.Variables(12).ValuesAsNumpy()
hourly_wind_speed_100m = hourly.Variables(13).ValuesAsNumpy()
hourly_wind_direction_10m = hourly.Variables(14).ValuesAsNumpy()
hourly_wind_direction_100m = hourly.Variables(15).ValuesAsNumpy()
hourly_wind_gusts_10m = hourly.Variables(16).ValuesAsNumpy()
hourly_dew_point_2m = hourly.Variables(17).ValuesAsNumpy()
hourly_pressure_msl = hourly.Variables(18).ValuesAsNumpy()

hourly_data = {"date": pd.date_range(
	start = pd.to_datetime(hourly.Time(), unit = "s", utc = True),
	end = pd.to_datetime(hourly.TimeEnd(), unit = "s", utc = True),
	freq = pd.Timedelta(seconds = hourly.Interval()),
	inclusive = "left"
)}

hourly_data["temperature_2m"] = hourly_temperature_2m
hourly_data["relative_humidity_2m"] = hourly_relative_humidity_2m
hourly_data["precipitation"] = hourly_precipitation
hourly_data["apparent_temperature"] = hourly_apparent_temperature
hourly_data["rain"] = hourly_rain
hourly_data["snow_depth"] = hourly_snow_depth
hourly_data["snowfall"] = hourly_snowfall
hourly_data["surface_pressure"] = hourly_surface_pressure
hourly_data["cloud_cover"] = hourly_cloud_cover
hourly_data["cloud_cover_low"] = hourly_cloud_cover_low
hourly_data["cloud_cover_mid"] = hourly_cloud_cover_mid
hourly_data["cloud_cover_high"] = hourly_cloud_cover_high
hourly_data["wind_speed_10m"] = hourly_wind_speed_10m
hourly_data["wind_speed_100m"] = hourly_wind_speed_100m
hourly_data["wind_direction_10m"] = hourly_wind_direction_10m
hourly_data["wind_direction_100m"] = hourly_wind_direction_100m
hourly_data["wind_gusts_10m"] = hourly_wind_gusts_10m
hourly_data["dew_point_2m"] = hourly_dew_point_2m
hourly_data["pressure_msl"] = hourly_pressure_msl

hourly_dataframe = pd.DataFrame(data = hourly_data)
print(hourly_dataframe)

```


