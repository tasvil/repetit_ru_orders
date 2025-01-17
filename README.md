# repetit_ru_orders

Прогноз факта оплаты заказа
Разработана модель классификации, которая по имеющейся информации о клиенте и заявке будет предсказывать вероятность оплаты заявки клиентом. Метрика: ROC-AUC.

В ходе работы выполнены следующие шаги:

Проведен обзор данных, их объединение и предобработка, включая корректировку аномалий, обработку текстовых данных.

Проведен исследовательский анализ данных, выявлены закономерности и зависимости признаков в отношении таргета, изучена корреляция признаков.

Созданы новые признаки:
- Признаки на основе рейтингов и других количественных данных, которые показали различие для таргета на графиках;
- Признаки на основе текстовых данных purpose и add_info: провели их лемматизацию, трансформировали с помощью TF-IDF и затем с помощью TruncatedSVD извлекли уплотненные признаки.

В качестве модели выбрана CatBoost, подобраны гиперпараметры. После проведенного анализа важности признаков выбраны ТОП-25 признаков для обучения модели.

В результате работы достигнуты следующие показатели:

ROC AUC на тестовой выборке = 0.748
