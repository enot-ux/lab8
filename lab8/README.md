# Аналіз Світових Метеорологічних Даних за допомогою Java Streams та HTTP-запитів

## Огляд Проекту

Цей проект розроблено для вивчення та вдосконалення навичок студентів у використанні Java Streams для обробки та аналізу світових метеорологічних даних, отриманих через HTTP-запити до метеорологічного API.

### Основний клас: WeatherAnalysis

Проект містить основний клас `WeatherAnalysis`, що включає методи для взаємодії з метеорологічним API та проведення аналізу погодних умов.

### Розробка

#### Взаємодія з API та отримання даних

- `fetchDataFromApi(String apiUrl)`: Метод для виконання HTTP-запиту до метеорологічного API та отримання даних. Дані перетворюються у список об'єктів `WeatherData`.

#### Аналіз екстремальних погодних умов

- `findHottestStations(List<WeatherData> weatherDataList, int count)`: Знаходження 10 найгарячіших станцій за середньою температурою.
- `findColdestStations(List<WeatherData> weatherDataList, int count)`: Знаходження 10 найхолодніших станцій за середньою температурою.
- `findMostHumidStations(List<WeatherData> weatherDataList, int count)`: Знаходження 10 найвологіших станцій за середнім рівнем опадів.

#### Розпізнавання патернів

- `findStationsWithContinuousRain(List<WeatherData> weatherDataList, int days)`: Визначення станцій, на яких було більше 7 послідовних днів опадів.
- `findStationsWithTemperatureIncrease(List<WeatherData> weatherDataList, int days, double temperatureIncrease)`: Визначення станцій, на яких температура зросла на щонайменше 5°C протягом 5 послідовних днів.

#### Агрегація та підсумкова статистика

- `calculateMonthlyAverages(List<WeatherData> weatherDataList)`: Розрахунок середньої глобальної температури, вологості та рівня опадів для кожного місяця.
- `findMonthWithHighestWindSpeed(List<WeatherData> weatherDataList)`: Знаходження місяця з найвищою середньою швидкістю вітру.

#### Відображення результатів

 Використання додаткових бібліотек для візуалізації даних.

## Використання

1. Запустіть програму.
2. Введіть URL метеорологічного API.
3. Отримайте та проаналізуйте світові метеорологічні дані.
