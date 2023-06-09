# Описание проекта

Сервис по продаже автомобилей с пробегом разрабатывает приложение, чтобы привлечь новых клиентов. В нём можно будет узнать рыночную стоимость своего автомобиля. 
Нужно построить модель, которая умеет её определять. Получены данные о технических характеристиках, комплектации и ценах других автомобилей.
Критерии, которые важны заказчику:
- качество предсказания;
- время обучения модели;
- время предсказания модели.

# Описание данных

Признаки:
- `DateCrawled` — дата скачивания анкеты из базы
- `VehicleType` — тип автомобильного кузова
- `RegistrationYear` — год регистрации автомобиля
- `Gearbox` — тип коробки передач
- `Power` — мощность (л. с.)
- `Model` — модель автомобиля
- `Kilometer` — пробег (км)
- `RegistrationMonth` — месяц регистрации автомобиля
- `FuelType` — тип топлива
- `Brand` — марка автомобиля
- `Repaired` — была машина в ремонте или нет
- `DateCreated` — дата создания анкеты
- `NumberOfPictures` — количество фотографий автомобиля
- `PostalCode` — почтовый индекс владельца анкеты (пользователя)
- `LastSeen` — дата последней активности пользователя
Целевой признак: 
- `Price` — цена (евро)

# Результат 

Во время работы с данными:
- избавился от выбросов
- избавился от лишних признаков
- избавился от пропусков
- провел кодировку категориальных признаков
- провел масштабирование признаков

Обучение моделей:
- обучил 4 модели
- подобрал гиперпараметры к ним
- замерил время выполнения ячеек
- сохранил качество предсказаний по метрике RMSE

Анализ моделей:
- проанализировал результаты всех моделей
- выбрал оптимальную, по всем критериям качества, модель
- сравнил модель со статичной


Оптимальной по всем критериям оказалась модель CatBoost с результатами:
- время обучения - 3 - 4 секунд
- время предсказания - менее секунды
- RMSE - 1714
- RMSE на итоговом тестировании - 1693
