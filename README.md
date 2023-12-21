# Laba_2_Docker_Compose
Задание
С помощью Docker-compose развернуть среду из 4 контейнеров.
Контейнер 1. PostgreSQL
Контейнер 2. Spark – master
Контейнер 3. Spark – worker1
Контейнер 4. Spark – worker2
Источник данных – файл house_prices.csv
Схема обработки данных и взаимодействия контейнеров:
1) «Контейнер 1. PostgreSQL» запускается и создает (подключается к существующей) БД.
2) В БД подгружаются данные из файла house_prices.csv в соответствующую таблицу.
3) «Контейнер 2. Spark – master» имеет возможность подключения к БД.
4) Контейнеры 2, 3 и 4 настроены как кластер Spark.
5) Приложение PySpark в виде файла my_spark.py загружено в «Контейнер 2. Spark – master». Его
задача:
Из данных house_prices вывести информацию: Средние стоимости квартир и домов в
зависимости от района и количества комнат.

Результат работы:

* Запущенные контейнеры
  
<img width="340" alt="docker_compose_work" src="https://github.com/Daria-Krylova/Laba_2_Docker_Compose/assets/55152528/3277463f-5459-49a2-98f2-69d43bc09933">

* Результат работы приложения
  
<img width="469" alt="docker_2_table" src="https://github.com/Daria-Krylova/Laba_2_Docker_Compose/assets/55152528/09f189a8-7828-4118-9e75-62cd0cbee19e">
