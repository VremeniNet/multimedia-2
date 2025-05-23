## Лабораторные работы по курсу "Методы, средства и технологии мультимедиа"


Студент: Желанов Даниил Вячеславович

Группа: М8О-410Б-21

---

## Лабораторная работа №6: Проведение исследований с моделями классификации

| Модель                         | Accuracy  | F-score  |
| -----------------------------  | --------- | --------------- |
| ResNet-18                      | 0.903     | 0.903           |
| ResNet-18 (улучшенный бейзлайн)  | 0.960     | 0.958           |
| ViT        | **0.938** | **0.937**       |
| ViT (улучшенный бейзлайн)        | 0.945     | 0.944           |
| Самостоятельная имплементация CNN           | 0.628     | 0.623           |
| Самостоятельная имплементация CNN (улучшенный бейзлайн)          | 0.647     | 0.637           |
| Самостоятельная имплементация transformer           | 0.630     | 0.622           |
| Самостоятельная имплементация transformer (улучшенный бейзлайн)          | 0.785     | 0.785           |


**Вывод:** Таким образом, модель ViT продемонстрировала наивысшие показатели точности, незначительно опередив ResNet-18 с улучшенным бейзлайном. Это подтверждает эффективность трансформеров в задачах компьютерного зрения, особенно при использовании предобученных весов. Улучшение бейзлайна сработало неравномерно: для ResNet-18 оно дало ощутимый прирост качества, подтверждая, что классические свёрточные сети неплохо реагируют на умеренные аугментации и корректировку гиперпараметров, для ViT же трансформации, напротив, разрушили позиционные зависимости, что привело к резкому падению метрик. Имплементированные модели показали удовлетворительные результаты, которые можно улучшить, увеличив количество эпох


---

## Лабораторная работа №7: Проведение исследований моделями семантической сегментации

| Модель                                                        | **Val IoU** | **Val Acc** |
| ------------------------------------------------------------- | :---------: | :---------: |
| UNet                                                          |    0.760    |    0.891    |
| UNet (улучшенный бейзлайн)                                    |  **0.776**  |  **0.893**  |
| Самостоятельная имплементация алгоритма                       |    0.691    |    0.854    |
| Самостоятельная имплементация алгоритма (улучшенный бейзлайн) |    0.672    |    0.831    |

**Вывод:** Таким образом, предобученная модель UNet с энкодером ResNet-34 показала достаточное качество сегментации, а улучшение бейзлайна позволило повысить точность без усложнения архитектуры. Свёрточная сеть, обученная с нуля, уступила предобученной модели UNet, но ее можно улучшить, увеличив количество эпох

---
## Лабораторная работа №8: Проведение исследований моделями обнаружения и распознавания объектов

| Модель                                | Precision | Recall | mAP@0.5 | mAP@0.5:0.95 |
|---------------------------------------|:---------:|:------:|:------:|:-------------:|
| YOLOv8 (предобученная)                | 0.704     | 0.687  | 0.701  | 0.465         |
| YOLOv8 (улучшенный бейзлайн)          | 0.719     | 0.703  | 0.716  | 0.478         |
| Самостоятельная реализация YOLO      | 0.526     | 0.508  | 0.514  | 0.309         |
| Реализация YOLO (улучшенный бейзлайн) | 0.542     | 0.551  | 0.536  | 0.332         |

**Вывод:** наилучшие результаты показала предобученная YOLOv11 с улучшенным бейзлайном. Улучшение бейзлайна позволило не только повысить точность и полноту, но и обеспечить более высокое среднее значение точности по различным уровням IoU. Собственная имплементация, несмотря на более низкие значения метрик по сравнению с предобученной моделью, продемонстрировала положительную динамику после применения улучшенного бейзлайна. Также все метрики можно еще улучшить, увеличив количество эпох.


