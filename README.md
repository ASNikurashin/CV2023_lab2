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


| Методы   | Ссылка на решение | Результат | Скорость выполнения |
|----------|-------------------|-----------|---------------------|
| Sobel, morphological, threshold, findContours                | [ноутбук](https://colab.research.google.com/drive/1jLoLhwLoiuEl7kbHgRL-dhrnMXl-1vUr?usp=sharing)           | 0,9068 |1,6 С/Мп |
| Sobel, morphological, threshold, GaussianBlur, binary_closing| [ноутбук](https://colab.research.google.com/drive/1JobD_DqQEZG-Pp-Ig2LDvTboh7xykv3T#scrollTo=HBMzR7U74fTz) | 0,8380 |1,4 С/Мп |
| Laplacian, threshold, Morphological, GaussianBlur            | [ноутбук](https://colab.research.google.com/drive/1-fgFF5tkys7SLSuWoNv1q6PvDPCR2l3z?usp=sharing)           | 0,8188 |1,3 C/Мп |
