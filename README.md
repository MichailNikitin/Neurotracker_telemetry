# Решение 2-х кейсов хакатона от Нейротехнолоджи


# Кейс 1: Анализ и кластеризация данных

## Описание
В этом кейсе мы анализируем данные, связанные с различными физиологическими показателями, такими как пульс, частота дыхания, уровень глюкозы и т.д. Целью является подготовка данных, анализ аномалий и кластеризация для выявления групп схожих наблюдений.

## Подготовка данных
1. **Выбор столбцов:**
   - Оставили только следующие столбцы: `'AvgPulse'`, `'Breath'`, `'EDA'`, `'Glucose'`, `'Oxygenation'`, `'Pulse'`, `'Steps'`, `'Temperature'`.
   - Убрали все NaN значения.

2. **Группировка по времени:**
   - Сгруппировали данные по времени и объединили по среднему значению.

## Анализ данных
### Быстрый просмотр:
- **Breath:** Частота дыхания, измеряется раз в 5 минут.
- **EDA:** Электродермальная активность, измеряет уровень возбуждения нервной системы через сопротивление кожи.
- **AvgPulse:** В данных присутствуют аномалии.
- **Breath и Glucose:** Нормальные значения.

### Кластеризация
Для кластеризации оставили следующие признаки: `'AvgPulse'`, `'Glucose'`, `'Oxygenation'`, `'Pulse'`, `'Temperature'`, так как остальные признаки были одинаковыми.

#### Подбор количества кластеров для KMeans:
1. **Понижение размерности:**
   - Использовали PCA (Principal Component Analysis) для понижения размерности до 2 признаков из 5 для упрощения визуализации.

2. **Выбор модели:**
   - По 3 метрикам наилучшей моделью оказалась KMeans с 4 кластерами.

### Визуализация


## Использованные библиотеки
- `pandas` для работы с данными.
- `numpy` для числовых операций.
- `scikit-learn` для PCA и KMeans.
- `matplotlib` для визуализации.

## Установка
1. Клонируйте репозиторий:
   ```sh
   git clone https://github.com/MichailNikitin/Neurotracker_telemetry.git


 # Кейс 2: Анализ данных акселерометров для выявления падений

## Описание
В этом кейсе мы создаем датасет из значений акселерометров с нейротрекеров, где человек упал и лежал неподвижно 30 секунд. Целью является выделение биомаркеров, которые указывают на падение.

## Подготовка данных
1. **Сбор данных:**
   - Собрали данные акселерометров с нейротрекеров, где человек упал и лежал неподвижно 30 секунд.

2. **Предобработка данных:**
   - Убрали NaN значения.
   - Нормализовали данные для улучшения качества анализа.

## Анализ данных
### Выделение биомаркеров:
- **Акселерометры:** Данные акселерометров использовались для выявления падений.
- **Биомаркеры:** Мы выделили биомаркеры, которые указывают на падение, такие как резкое изменение ускорения и последующая неподвижность.

### Визуализация:
- **Графики:** Построили графики для визуализации данных акселерометров и выделенния биомаркеров.

## Использованные библиотеки
- `pandas` для работы с данными.
- `numpy` для числовых операций.
- `matplotlib` для визуализации.

## Установка
1. Клонируйте репозиторий:
   ```sh
   git clone https://github.com/MichailNikitin/Neurotracker_telemetry.git
