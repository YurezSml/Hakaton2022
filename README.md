# Hackathon 2023 

><img align="right" width="110" height="110" src="https://user-images.githubusercontent.com/78375128/209393192-0b0016f6-a7ba-497d-a1e5-14df769c4816.png">
>
>## Команда «DataHunters»
>
>ШМЕЛЬКОВ Юрий, МАКЕЕВА Анастасия, ОЖЕРЕЛЬЕВ Виктор, КАРАГОДИН Николай, ПОНОМАРЕВ Глеб, БОГОМОЛОВ Алексей.

# Рекомендательный сервис для платформы Работа.ру.

## Описание датасета

В датасете содержится информация о пользователях платформы: идентификаторы пользователей(зарегитрированных/не зарегистрированных,), типы событий(просмотр вакансии, отклик и т.п), время события и временные метки.

Основная идея для цели использования датасета - основываясь на данных о взаимодействии пользователя с вакансией на платформе, разработать модель для рекомендации пользователю подобных вакансий, но ранее не просмотренных. 

## Структура датасета

Int64Index: 12212868 entries, 0 to 12292587
Data columns (total 9 columns):

| # | Column | Dtype |
|------|------|------|
| 0  | common_id       | int64   |
| 1  | event_date      | object  |
| 2  | event_timestamp | int64   |
| 3  | action_time     | int32   |
| 4  | vacancy_id_     | int64   |
| 5  | cookie_id_      | object  |
| 6  | user_id         | object |
| 7  | event_type      | object |
| 8  | rating          | int64   |
dtypes: int32(1), int64(4), object(4)\
memory usage: 885.2+ MB

## Методы сбора и обработки данных
Данные предоставлены компанией

## Описание ноутбуков

Ноутбуки разделены на три части: работа с данными и моделирование.

1. Ноутбук с поэтапной обработкой данных.
2. Три ноутбука с наработками по модели с использованием подхода для рекомендательных систем(svd).

Работа велась с помощью среды Jupyter Notebook.

## Структура репозитория

    ├── DataProcessing.ipynb                        # работа с данными
    ├── Model_RabotaRU.ipynb                        # моделирование
    ├── SVD_model_top80.ipynb                       # моделирование
    ├── baseline_model_with_precision5_v2.ipynb     # моделирование
    └── README.md                                   #Документация по проекту
