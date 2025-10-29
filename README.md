# Прогноз потребления газа котельной (ML)

**Цель**: Прогнозирование суточного потребления газа (`Vgas_m3`)  
**Период**: 2022–2024  
**Модель**: XGBoost (MAPE ~X.X% на 2024)  
**Прогноз**: 30 дней вперёд  

---
## Структура проекта
data/
├── raw/                → исходные .xlsx, .csv
├── processed/          → daily_merged.csv, daily_features.csv
notebooks/
├── 01_data_parsing.ipynb
├── 02_eda.ipynb
├── 03_feature_engineering.ipynb
├── 04_modeling.ipynb
├── 05_forecast_future.ipynb
models/
├── xgb_model.pkl
├── scaler.pkl
forecast_30_days.csv    → прогноз
requirements.txt
README.md## Структура проекта

---

## Как запустить
```bash
git clone https://github.com/ТВОЙ_ЮЗЕР/gas-consumption-forecast-ml.git
cd gas-consumption-forecast-ml
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook

Запусти по порядку: 01 → 02 → 03 → 04 → 05
Прогноз появится: forecast_30_days.csv

Результаты

XGBoost: MAE = X м³, MAPE = X.X%
Prophet: MAE = Y м³, MAPE = Y.Y%
Прогноз: +30 дней от последней даты

Автор: Кирилл_13
Дата: Октябрь 2025


---

### Шаг 4 — Пуш на GitHub

```powershell
git init
git add .
git commit -m "feat: полный ML-пайплайн прогноза газа"
git branch -M main
git remote add origin https://github.com/ТВОЙ_ЮЗЕР/gas-consumption-forecast-ml.git
git push -u origin main

ПРОЕКТ ЗАВЕРШЁН!
Ссылка на GitHub:
https://github.com/vasilijbereza123-maker/gas-consumption-forecast-ml