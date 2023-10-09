# CV2023_lab2
Команда:
* Никурашин Алексей
* Горбунова Екатерина 
* Горцуева Александра
* Чернышев Артем
* Терешин Данил

#  Задача поиска объекта на изображении по шаблону
## Датасет
Расположен в папке datset

Включает в себя:
* 36 различных изображений
* 36 паттернов 

## Описание задачи
* Язык программирования - `Python`
* Метод поиска по шаблону должен быть реализован при помощи ключевых точек
* Маской является четырёхугольник 

* В файле `cv_lab2.ipynb` реализовать функцию `matchTemplate()`

## Метрики
**Метрика точности**
* В качестве метрики оценки результата используется IoU (Intersection over Union)

![image_2023-09-17_20-47-39](https://learnopencv.com/wp-content/uploads/2022/12/feature-image-iou-1-1024x292.jpg)

## Baseline
* IoU вычисляется для каждого изображения, затем определяется среднее значение
* Нами было получено значение метрики, равное 0.109
* Если использовать вместо значения метрики детектора всю картинку, то средние значение IoU будет 0.05


| Методы   | Ссылка на решение | Результат |
|----------|-------------------|-----------|
| SIFT, BFmatcher, bounding box(perspectiveTransform) | [ноутбук](https://colab.research.google.com/drive/1y9YbXHIKaEBJSr307Py4fYpkMHYHXRYB?usp=sharing)                           | 0,2760 |
| SIFT, BFmatcher                                     | [ноутбук](https://colab.research.google.com/drive/1TsclE90lUuy-jvIUs7UlAM17kaWzmReB?usp=sharing)                           | 0,6763 |
| MatchTemplate                                       | [ноутбук](https://colab.research.google.com/drive/1Hc45NxvEdC1FmbQlSfieAQYj1bHz82xN?hl=ru#scrollTo=DOAwwF7sSchd)           | 0,1115 |
