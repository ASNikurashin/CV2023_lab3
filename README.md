# CV2023_lab3 
#  Классификация

Команда:
* Никурашин Алексей
* Горбунова Екатерина 
* Горцуева Александра
* Чернышев Артем
* Терешин Данил
  
## Датасет
Расположен в папке dataset, отдельная папка для каждого класса, который включает в себя изображения 5 различных классов цветков:
(тот же датасет на [Яндекс диске](https://disk.yandex.ru/d/r6AFbcgSAKzg0A) ) 
* buttercup - 318 изображений
* coreopsis -962 изображений
* daffodil - 814 изображений
* dandelion - 1021 изображений
* sunflower - 758 изображений
  
## Описание задачи
* Язык программирования - Python.
* При использовании нейронных сетей для классификации разрешено использовать любую библиотеку (PyTorch, TensorFlow, Keras и др.).
* Создать модель для классификация цветов и сохранить ее параметры в файл для дальнейшей проверки качества классификации во время занятия.
* Измерить время инференса модели при обработке одного изображения в секундах.
  
## Ограничения:
1. Запрещено использование готовых архитектур "из коробки" одной строчкой. В коде должны быть прописаны слои вашей модели.

## Метрики
**Метрика точности**
* Для расчета эффективности используется среднее значение метрики f1-score по всем 5 классам.
* пример расчета метрики из пакета sklearn представлен в файле evaluation.py

* F1-score вычисляется по следующей формуле:  F1 = 2 * (precision * recall) / (precision + recall).
* Точность (precision) измеряет, как много из предсказанных положительных классов действительно являются положительными. Она вычисляется как отношение числа верно предсказанных положительных классов к общему числу предсказанных положительных классов.
* Полнота (recall) измеряет, как много из всех положительных классов было правильно предсказано. Она вычисляется как отношение числа верно предсказанных положительных классов к общему числу фактических положительных классов.

## Baseline
* Модель - Resnet-18 , оптимизатор - SGD, lоss - кросс-энтропия, batch_size =16, количество эпох -20
* Предобработка изображений - только Resize до размера 224x224 пикселя
* Полученное значение метрики : 0.625
* Время инференса модели при обработке одного изображения: 13,39 мс (0,013 с)


| Ссылка на решение | Результат %| 
|-------------------|-----------|
| [ноутбук](https://colab.research.google.com/drive/1GEqhrpSFc_z5BXQPv6ZgoVvpgUcPiNKL#scrollTo=YA1mnnp7ipX_) | 0,84 |
| [ноутбук](https://colab.research.google.com/drive/1BMN4zeCy2Hbp66rpzKiw8-UZUfQiMv0f?usp=sharing) | 0,93 |
