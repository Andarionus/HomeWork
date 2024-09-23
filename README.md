# АНАЛИЗ ДАННЫХ В РАЗРАБОТКЕ ИГР
Отчет по лабораторной работе #1 выполнил(а):
- Галимуллин Андрей Александрович
- РИ-230932
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 + Самостоятельная работа | * | 20 |

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
Ознакомиться с основными операторами зыка Python на примере реализации линейной регрессии.

## Задание 1
### Написать программу Hello World на Python с запуском в Jupiter Notebook
Ход работы:
- Скачан дистрибутив anaconda, запущен Jupiter Notebook. На скриншоте представленно выполнение программы Hello World на Python.

![изображение](https://github.com/user-attachments/assets/93db508d-5463-4e73-95fb-a80bbafb1471)


## Задание 2
###  Написать программу Hello World на C# с запуском на Unity.

- Так как типичного для компилятора C# простого вывода на кран сообщения с консоли в Unity не предусмотрено (или я просто чего-то не осознал), то мною был придуман следующий вариант.
![изображение](https://github.com/user-attachments/assets/e6b74527-8552-448f-9467-c192106e4ecd)
- Данный скрипт написан с подключением библиотеки UI с движка юнити, позволяет заменить любую фразу в  присоединённом объекте "текст" на Hello World. Так как Visual Studio подключен по иснтрукции с курса, написано всё на нём.
![изображение](https://github.com/user-attachments/assets/2570e84b-c0a3-42b9-8081-c911ca529c2e)
![изображение](https://github.com/user-attachments/assets/98b76340-d1b4-4eb1-8378-2e605a3d34f4)
![изображение](https://github.com/user-attachments/assets/80708ecf-0ada-4501-9532-00670eb9f53d)
- К данному скрипту присоединён объект "текст", что явялется частью интерактивного объекта "кнопка". При запуске сцены имеется возможность нажать на кнопку, которая по этому триггеру выводит рядом объект "текст". В этом случае выводится Hello World благодаря скрипту.


## Задание 3
### Оформить отчет в виде документации на github (markdown-разметка).
- Я так понимаю, успешность этого пункта выполняется по факту отправки формы, поэтому дальше перейдём к следующему пункту.


## Самостоятельная работа (слайд с лекции)
### ГеймДизайн игры SaveRTF (В чём цель игры, смысл?)

- Цель игры в SaveRTF заключается лишь в репетативном фарме кристаллов, падающих с боссов (встречающиеся через каждые 4 волны), ради получения доступа к следующей локации. Так как по сути нет ни сюжета, ни какой-либо другой завлекаловки (помимо острела одинаковых мобов), то весь смысл сводится к "челенджу" пройти как можно больше волн. В надежде, что на следующей локации ГеймДизайн окажется получше.

### Какую сущность(и) мы бы могли «обучить» ML-Agent-ом для того чтобы создать более качественный игровой опыт?

- На мой взгляд подходит несколько сущностей, которые можно было бы улучшить благодаря обучению ML-AGent-ом. Они перечислены ниже.
1) Зомби. Как от самого распространнёного противника, острелом которого занимается игрок большую часть времени, ожидается, что он будет как-то прогрессировать параллельно игроку. Но несмотря на то, что на более поздних волнах появляется усиленная версия ("ползующая", лишь двигается быстрее), сущности всё равно как и на первой волне имеют очень примитивный поиск пути до игрока. Что на первой волне они будут сбиваться в кучу, пытаясь догнать игрока, что на десятой. И чтобы сделать более качественный игровой опыт, можно было бы хотя бы усиленную версию обучить ML-AGent-ом в плане обособленного поиска пути до игра (хотя бы). Благодаря этому игрок начнёт хоть немного задумываться о позоционке (как в ближайших шутерных аналогах от первого лица (современный doom, destiny и тд.)), что должно хоть как-то разнообразить репетативный геймплей.
2) Боссы. Несмотря на разные текстуры, статлайн боссов остаётся одинаковым. Большая губка для пуль с совсем уж низкой скоростью и большим уроном за тычку. Ближайший аналог для этой сущности - это особенные заражённые из Left 4 dead, конкретно - танк. И он не медленно плетётся за персонажем игрока, представляя какую-то угрозу только если закончатся патроны и придётся использовать нож (хотя у меня и с ним получлось затыкать босса в SaveRTF). Так что помимо поиска пути, упомянутого выше, нужно применить ещё ряд каких-либо изменений. Чтобы босс выходил не в одиночестве, а в месте с волной, чтобы он мог хоть как-то атаковать из далека.
3) Магазин. Довольно быстро игрок понимает, что его между волнами насильно запирают в меню магазина, хоть он и всегда стоит в углу карты. Я бы предложил изменить его в сущность летающего дрона. Он бы либо курсировал по карте, либо и вовсе следовал за игроком (раз уж вы всё равно решили его запускать между волнами). Собственно этому его можно было бы также обучить ML-Agent-ом, чтобы игроку не приходилось бегать в процессе боя на другой край карты в попытки закупиться патронам.


## Выводы

Установлена Anaconda, попробовал писать на Python в новом компиляторе. Что же до Unity с Visual Studio, то они были установлены ещё в первом году обучения в университете, так что лишь немного попрактиковался с решением задания 2. На github заведён отдельны репозиторий для данного трека, на котором и реилизован этот отчёт о лабораторной работе. В виде эксперимента ознакомился с SaveRTF. помимо последнего пункта, узнал много чего важного и нового.

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
