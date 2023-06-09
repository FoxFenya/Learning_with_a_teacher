# Проект "Отток клиентов"
*Спринт обучение с учителем.*

## Постановка задачи
Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.

1. Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Модель потсроить на основе исторических данных о поведении клиентов и расторжении договоров с банком.
2. Необходимо найти модель с предельно большим значением F1-меры (метрика должна быть доведена до 0.59). Проверить F1-меру на тестовой выборке.
3. Измерерить AUC-ROC, сравнить её значение с F1-мерой.

Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

Для анализа были использованы модели:
- DecisionTreeClassifier (в качестве сплитера используется метод рандом)
- LogisticRegression
- RandomForestClassifier

## Этапы решения задачи

1. Загрузить и изучить файл с данными.
2. Исследовать баланс классов.
3. Выделить обещающую, валидационную и тестовую выборки из данных.
4. Обучить модели без учёта дисбаланса классов.
5. Сбалансировать классы и обучить модель, учитывая дисбаланс классов. Выбрать лучшую модель.
6. Проверить выбранную модель на тестовой выборке.

## Результат
Лучше всего с поставленной задачей справляется метод "Случайный лес" (RandomForestClassifier). Модель стабильно себя ведет как на валидационной так и на тестовой выборках и показывает результаты высокой точности. Можно с уверенностью сказать, что модель подходить для решения поставленной задачи.