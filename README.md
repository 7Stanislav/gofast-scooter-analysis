# 🛴 GoFast Scooter Service Data Analysis / Исследование сервиса аренды самокатов GoFast

## Description / Описание
**EN:**  
This project was carried out in the role of a data analyst for *GoFast*, a popular scooter rental service.  
The goal was to analyze user and trip data to identify behavioral patterns, compare performance between subscription types, and test business hypotheses.  
The insights are aimed at developing recommendations for business growth, tariff optimization, and marketing strategies.  

GoFast offers two tariff plans:  
- **Free plan**  
  - No monthly fee  
  - 8 RUB per minute  
  - 50 RUB start fee  
- **Ultra plan**  
  - 199 RUB per month  
  - 6 RUB per minute  
  - No start fee  

**RU:**  
Данный проект выполнен в роли аналитика популярного сервиса аренды самокатов GoFast.  
Цель исследования — анализ данных о пользователях и их поездках для выявления паттернов поведения, сравнения показателей разных типов подписок и проверки бизнес-гипотез.  
Результаты помогут сформулировать рекомендации для роста бизнеса, оптимизации тарифов и маркетинговых стратегий.  

Сервис GoFast предлагает два тарифных плана:  
- **Без подписки (Free)**  
  - Абонентская плата: отсутствует  
  - 8 рублей за минуту  
  - 50 рублей за старт  
- **С подпиской Ultra**  
  - 199 рублей в месяц  
  - 6 рублей за минуту  
  - старт бесплатно  

---

## Dataset / Используемые данные
**EN:**  
The project uses three CSV files:  
- `users_go.csv` — user data (ID, name, age, city, subscription type)  
- `rides_go.csv` — trip data (user ID, distance, duration, date)  
- `subscriptions_go.csv` — tariff details (plan type, cost per minute, start fee, monthly fee)  

**RU:**  
В проекте используются три CSV-файла:  
- `users_go.csv` — информация о пользователях (ID, имя, возраст, город, тип подписки)  
- `rides_go.csv` — данные о поездках (ID пользователя, расстояние, длительность, дата)  
- `subscriptions_go.csv` — детали тарифных планов (тип подписки, стоимость минуты, стоимость старта, абонентская плата)  

---

## Research Workflow / Ход исследования
**EN:**  
1. **Initial Data Analysis** — load, check types, missing values, duplicates  
2. **Data Preprocessing** —  
   - Convert `date` to datetime  
   - Create `month` column  
   - Round trip duration upward (`duration_ceil`)  
   - Remove anomalies (very short rides)  
3. **Merging Data** — combine user, rides, and subscription info into one dataset  
4. **Exploratory Data Analysis (EDA)** —  
   - Distribution of age and cities  
   - Ride frequency and duration  
   - Comparison of user behavior by subscription type  
5. **Revenue Calculation** — monthly revenue per user by plan rules  
6. **Hypothesis Testing** — statistical tests to compare groups  
7. **Conclusions & Recommendations**  

**RU:**  
1. **Первичный анализ** — загрузка, проверка типов, пропусков, дубликатов  
2. **Предобработка данных** —  
   - преобразование `date` в формат даты  
   - создание столбца месяца  
   - округление длительности поездки вверх (`duration_ceil`)  
   - удаление аномалий (короткие поездки)  
3. **Объединение данных** — слияние таблиц пользователей, поездок и тарифов  
4. **EDA (исследовательский анализ)** —  
   - распределение возраста и городов  
   - частота и длительность поездок  
   - сравнение показателей подписчиков и неплательщиков  
5. **Подсчёт выручки** — расчет помесячной выручки  
6. **Проверка гипотез** — сравнение групп по статистике  
7. **Общий вывод и рекомендации**  

---

## Key Findings & Recommendations / Ключевые выводы и рекомендации
**EN:**  
- **User behavior:** Ultra subscribers take longer trips and cover more distance, while Free users often make short rides.  
- **Revenue:** Ultra subscribers generate more predictable monthly revenue due to the subscription fee, despite cheaper rides.  
- **Free plan users:** revenue depends strongly on number of rides.  
- **Hypothesis tests:** confirmed statistically significant differences between groups.  

**Recommendations:**  
- Strengthen marketing for Ultra subscriptions (discounts, referral bonuses).  
- Optimize Free plan with incentives to upgrade.  
- Encourage longer trips (loyalty programs).  
- Continue monitoring anomalies (very short or long trips).  

**RU:**  
- **Поведение пользователей:** Ultra-подписчики совершают более длинные поездки и проезжают большее расстояние; Free — чаще короткие.  
- **Выручка:** Ultra обеспечивает более предсказуемый доход благодаря абонентской плате.  
- **Free:** доход зависит от числа поездок.  
- **Гипотезы:** подтверждены статистические различия в поведении и выручке.  

**Рекомендации:**  
- Усилить маркетинг Ultra (акции, бонусы).  
- Оптимизировать Free (мотивировать к переходу на подписку).  
- Стимулировать длинные поездки (система лояльности).  
- Продолжать мониторинг аномалий.  

---

## Technologies / Используемые технологии
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- SciPy  
- Jupyter Notebook  

---

## How to Run / Как запустить проект
**EN:**  
1. Clone repository:  
   ```
   git clone https://github.com/7Stanislav/gofast-scooter-analysis
   ```  
2. Install dependencies:  
   ```
   pip install pandas numpy matplotlib seaborn scipy
   ```  
3. Data files `users_go.csv`, `rides_go.csv`, `subscriptions_go.csv` are included in the repo.  
4. Open `project.ipynb` in Jupyter Notebook/Lab.  
5. Run all cells.  

**RU:**  
1. Клонируйте репозиторий:  
   ```
   git clone https://github.com/7Stanislav/gofast-scooter-analysis
   ```  
2. Установите зависимости:  
   ```
   pip install pandas numpy matplotlib seaborn scipy
   ```  
3. Файлы `users_go.csv`, `rides_go.csv`, `subscriptions_go.csv` уже есть в репозитории.  
4. Откройте `project.ipynb` в Jupyter Notebook или JupyterLab.  
5. Запустите все ячейки по порядку.  
