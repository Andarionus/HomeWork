# АНАЛИЗ ДАННЫХ В РАЗРАБОТКЕ ИГР
Отчет по лабораторной работе #5 выполнил(а):
- Галимуллин Андрей Александрович
- РИ-230932
- Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Познакомиться с программными средствами для создания системы машинного обучения и ее интеграции в Unity.


## Задание 1
###  Поиск агентом объекта на сцене.

Ход работы:
- Был создан 3D проект на юнити, к нему при помощи anaconda prompt добавлен ML агент. На данной сцене проведены исследования обучения модели по поиску объекта.
![изображение](https://github.com/user-attachments/assets/2d7f0224-e6fd-43f3-8848-ed4a6f29138b)
1) При запуске сцены было проведено тестирование обучения модели. Анаконда промт сохранил результаты. Они были использованы для работы агента без запуска программы в промте.
![изображение](https://github.com/user-attachments/assets/25ab3d65-4169-4c50-916d-30479d11f074)
![изображение](https://github.com/user-attachments/assets/7d40a092-f20d-444c-aea8-45cf08b3c4d2)
![изображение](https://github.com/user-attachments/assets/2db5f5cc-8161-44e9-8623-cd066cc4ebd7)
![изображение](https://github.com/user-attachments/assets/9a2cc70d-1988-492c-be7c-6ae52f2a451c)
Обучение заняло приличное количество времени, однако модель с присоединённым файлом результатов теперь передвигается самостоательно, хоть и с небольшими ошибками (иногда объект всё же не вписывается траекторией своего движения и падает за пределы опытной зоны)
2) Были сделаны 3, 9 и 27 копий объекта для дальнейших исследований. 
![изображение](https://github.com/user-attachments/assets/8df8b248-c212-4053-95e5-92a7c3054030)
![изображение](https://github.com/user-attachments/assets/4583d7a0-7469-4d04-a2d0-ecef4f5bc6fd)
![изображение](https://github.com/user-attachments/assets/f9618fe6-c4c4-4fde-a66d-39d363eb1458)
![изображение](https://github.com/user-attachments/assets/7c321080-9a1c-4000-8c37-30481a4e928c)
Однако несмотря на большее количество обучаемых моделей, при большем количество записанных успешнных данных, модель всё равно продолжала периодически сваливаться с опытной зоны. Возможно с ещё большей частотой, чем при единичном обучении.
![изображение](https://github.com/user-attachments/assets/6ed0b80a-53c9-4cc1-892e-bdbdebfbe340)
![изображение](https://github.com/user-attachments/assets/1852f4be-c8bc-494a-8b7e-c12bd3f8ee2e)
3) По итогу было выяснено, что большее количество обучающихся моделей лишь ускоряют процесс обучения (по сравнению с 1 моделью, 27 выдадут за считанные секунды первый результат). В то же время это не влиет на качество самого обучения, что нужно конпенсировать более чёткими критериями обучения в скрипте (на мой взгляд, так можно было бы решить проблемы с физикой движения)


## Задание 2
###  Симулятор добычи ресурсов
Ход работы:
- В первую очередь был добавлен проект Unity ML-Agent_EconomicModel и привязано к нему пространство в промте. Ввиду низкой производительности (остуствие видеокарты от nvidia), количество обучающихся моделей было уменьшено (в данном случае обучались 4 и 8 моделей). Далее было произведено наблюдение за обучением модели и выгрузка графиков.
![изображение](https://github.com/user-attachments/assets/4a555504-2981-426b-b91d-edce8f38f825)
![изображение](https://github.com/user-attachments/assets/045e3153-df7c-4015-866e-46fd2a9f3807)
![изображение](https://github.com/user-attachments/assets/00f0867e-ddb9-4619-8a0a-b19b98aaf4b2)
![изображение](https://github.com/user-attachments/assets/8ac0d358-ba54-4e9b-a1e8-e5fdc04e67ac)
![изображение](https://github.com/user-attachments/assets/7953a284-d924-45ab-94f0-80c2de6ee1e8)
![изображение](https://github.com/user-attachments/assets/32c876c1-4874-408f-b485-b5dc8f835d4a)
Всё так же 8 моделей обучаются быстрее 4, результаты в графиках так же отличаются. Кроме того, был исследован скрипт файл передвижения и yaml файл для дальнейших заключений о работе модели.
#### Найдите внутри C# скрипта “коэффициент корреляции” и сделать выводы о том, как он влияет на обучение модели.
- Ближайшим аналогом “коэффициента корреляции” является переменная tempInf, в которой сохранется процентное изменение цены на золото между первым и вторым месяцем (tempInf = ((pricesMonth[1] - pricesMonth[0]) / pricesMonth[0]) * 100;). В моём понимании - с каждой разом модель должна приходить с золотом ниже некоторой границы, которая высчитывается как увеличенное количество золота за прошлый месяц на 6%. если условие удовлетворено, то агент получает положительное вознаграждение и сохраняет данную стратегию действий. В обратном же случае он получает отрицательное вознаграждение. Таким образом, переменная является критерием успешности выполнения задачи и помогает обучать модель оптимизировать свои действия для получения положительных вознаграждений и минимизации отрицательных. Переменная tempInf в данном контексте измеряет процентное изменение между ценами на золото в два разных месяца и может рассматриваться как нечто подобное коэффициенту корреляции, если рассматривать изменение как зависимость между двумя переменными (через tempInf считается, конечно, не статическая переменная, поэтому он ближе к темпу роста, чем к критерию Пирсона)






- Под сегментом таблицы "Средний урон" в столбик подсчитан "Разброс урона оружия" (справа от него среднее значение по строке). Ввиду того, что показатели в строке распределены не равномерно разброс может слегка отличаться от реального значения (+/- единица). Найден он был путём вычитания из макимального значения в строке среднего значения.
- Далее под сегментом таблицы "Средний урон" подсчитано среднеквадратическое отклонение урона для всего оружия, которое имеет в этом смылс (исключения - нож и пила). Используется формула из теории вероятности, представленная ниже.
- Попытка подсчёта вариативность отклика же вызвала некоторые трудности. В реалиях геймплея Save RTF вариативности в приципе не так много, что уж до реакции на события. ибо основная механика - стрельба, по каким-то причинам, не подвластна влиянию игрока. Игровой персонаж в любом случае начнёт стрелать из выбранного оружия, а мобы  не перестанут приходить. Проблемы однозначности прокачки я тоже рассматривал в предыдущей работе (хотя забег с макимальной скоростью и пилой показал, что с вампиризмом всё не так однозначно, но игрок в жизни через такой гринд без кода не пролезет). Единственный момент, который можно было бы как-то просчитать, так это экономический вопрос (когда и как игрок покупает новое оружие, например). Однако в этой части тоже есть проблема, что просто не позволит накопить достаточно валюты за забег для этого, описанна она была выше и в прошлой работе. Поэтому с данным пунктом затрудняюсь выдать какую-либо визуализацию.
![изображение](https://github.com/user-attachments/assets/534998d3-bca4-48ab-8da3-8c4354e02dff) ![scale_1200](https://github.com/user-attachments/assets/3b17b372-5f04-4605-8dda-dc839215a462)



## Задание 3
### Решение в 80+ баллов должно визуализировать данные из google-таблицы, и с помощью Python передавать переменные в проект Unity. В Python данные также должны быть визуализированы.

- В гугл таблице представлена диаграмма эффективности оружия в зависимости от дальности, детали которой были описаны выше. По ней видно, что оружие нуждается в определённом ребалансе, в том числе пила, которая в приципе выходит за рамки таблицы (по своей сути, можно было бы добавить механику из дума с добиваниями с помощью пилы (долго, не слишком эффективно, но даёт кадры неуязвимости и восстанавливает определённые ресурсы)).
- Далее был написан код на питоне, что вводит в гугл таблицу значения вероятности попадания оружия (для боллее быстрой обработки, переносится в работе лишь значения пистолета и огнемёта (для наглядной разницы)), диаграмма присутствует та же. Из гугл таблицы переменные передаются в проект на юнити, где в зависимости от шанса на попасть воспроизводятся разные звуковые файлы (при больше %50 попал, при меньше - промахнулся)
![изображение](https://github.com/user-attachments/assets/534998d3-bca4-48ab-8da3-8c4354e02dff) 
![изображение](https://github.com/user-attachments/assets/d7b5e28d-99e0-4341-ae80-fe24c1c36915)

![изображение](https://github.com/user-attachments/assets/16824b95-9e91-4112-b0ab-f6d8dba8729b)

![изображение](https://github.com/user-attachments/assets/6d034d03-5862-49d0-ab8a-ae0fbb02a047)


## Выводы

"Удивительный" опыт первой попытки как-то проанализировать оружие в Save RTF через геймплей, конечно, дал результаты похожие на то, что есть в коде, но в то же время были далековаты от правды и пестрели моими домыслами. Однако после публикации исходников таблица начала обретать свой финальный вид (бесконечный урон пилы, ребаланс и тд). Более подробно о ребалансе будет мною описано в задании 3*, а пока лишь добавлю, что была проведена работа с данными в гугл-шаблоне, а так же был написан код на питоне/С# для юнити, основанный на материалах предыдущего задания. И всё даже работает.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
