# kiselev_opendata_final_project
Message analysis of three big russian IT internship related communities

Ссылка на случай, если загрузка файлов из бакета не сработает: https://drive.google.com/drive/folders/1cIXZLhCjPKxslS8NaUK4wyrUGEvaQ474?usp=sharing 


## Описание работы

**Этап 0: Подгрузка файлов**
- Гет запросом получены файлы с Yandex object storage 

**Этап 1: Создание единого датафрейма** (это часть из домашней работы №2)
- Были объединены данные из трех телеграм-чатов: "Поступашки", "Яндекс алгоритмы" и "Питон помощь".
- Выполнена предобработка данных:
- Cложные сообщения из нескольких dict блоков были преобразованы в читаемый текст.
- Добавлены столбцы с количеством реакций и списком реакций для каждого сообщения.


**Этап 2: Exploratory Data Analysis**
- Вычислены средние, медианные и максимальные значения длины сообщений.
- Построена сводная таблица для анализа длины сообщений и количества реакций по каналам.
- Определено количество редактированных сообщений и их доля в общем объеме.

- Построена сводная таблица для анализа пользователей с большим количеством отправленных сообщений.
- Найден пользователь с наибольшей активностью (10% всех сообщений).
- Проанализирована осмысленность его сообщений (и по контексту, и по соотношению уникальных текстов сообщений)


**Этап 3: Визуализация данных**
- Построены графики активности для "топового пользователя".
- Проанализировано соотношение между объемом текстов и количеством реакций у "топового пользователя". Дополнительно построена корреляционная матрица для параметров. Результаты пользователя сопоставлены с общими по датасету. 
- Построены графики активности для сообществ. Выявлены пики активности в марте-апреле, сентябре и на рубеже года, что может быть связано с циклами стажировок или запуском курсов.
- Проанализированы аномальные объемы сообщества "Питон помощь": средняя длина сообщений вдвое меньше, чем в других каналах, что указывает на флуд.
- Построена круговая диаграмма с распределением объема сообщений между сообществами в выборке


**Выводы**
- Пользователь с наибольшей активностью вероятнее всего – реальный человек, а не бот, что подтверждается анализом его сообщений.
- Пики активности в каналах совпадают с периодами, связанными с образовательными или карьерными циклами.
- Канал "Питон помощь" выделяется сравнительно большим объемом сообщений, но низкой средней длиной, что указывает на его менее профессиональный характер.
