# Реферат
## по курсу "Логическое программирование"

### студент: Кондратьев Е. А.

## ТЕМА Как научить младшую сестру/брата логическому программированию

## Результат проверки


| Преподаватель     | Дата         |  Оценка       |
|-------------------|--------------|---------------|
| Сошников Д.В. |              |               |
| Левинская М.А.|              |               |

> *Комментарии проверяющих (обратите внимание, что более подробные комментарии возможны непосредственно в репозитории по тексту программы)*

## Как научить младшую сестру/брата логическому программированию

Как вообще чему-нибудь научить ребенка? Конечно, заинтересовать, как игра или по-другому. Но на практике это реализовать не так-то просто. Предмет изучения нужно адаптировать под ребенка, возможно, придется пожертвовать некоторыми деталями и рассказать их позже. Но главное - превратить обучение в игру, и вы всегда можете усложнять ее правила по мере взросления. Изложение материала должно быть интересным, рассказанным простыми понятными словами и подкрепленным теми же примерами, которые понятны ребенку.

## Prolog
Для начала давайте определимся, кто такие программисты, зачем они пишут программы и какое отношение к этому имеют язык программирования и логика. Программист - это человек, который пишет для компьютера какие-то инструкции, называемые программами. Он сообщает компьютеру, что и как делать. У компьютеров есть языки, на которых написаны программы, точно так же, как у людей есть разные языки, на которых они говорят. Программы помогают компьютеру с помощью логики прийти к правильному выводу и показать его программисту. Одна из основных задач логики - понять, как прийти к выводу из любых рассуждений и получить верные, правильные знания о том, о чем мы думаем и о чем рассуждаем. Логическое программирование - это способ создания программ, которые помогают нам что-то выяснить на основе имеющихся у нас фактов. Его особенность заключается в том, что мы не указываем компьютеру, как он должен что-то делать. Компьютер должен во всем разобраться. Мы только пишем правила, по которым он должен это понимать.

Люди говорят на разных языках, например, мы говорим по-русски, но основной логический язык программирования - Пролог. Когда мы «говорим» на языке Пролог, для нас важно соблюдать некоторые правила, как и во всех других языках. В программе есть объекты, между ними существует связь, и компьютер должен им соответствовать. Мы увидим, какие объекты и отношения есть ниже на примерах. Количество операторов в программе не ограничено. Все имена и связи пишутся строчными буквами. Если имя объекта начинается со строчной буквы, то этот объект имеет известное значение, то есть является константой. Имена переменных в Прологе начинаются с заглавной буквы. Переменная может быть объектом, не имеющим значения, но при выполнении программы переменная принимает заданное значение и использует его для получения результата. Если в записи имени есть пробелы, их необходимо заменить знаком подчеркивания (_). Также у нас всегда есть возможность написать пояснение - комментарий к нашей программе, для этого нужно написать его после символа %, если комментарий занимает не более строки. Давайте посмотрим на пример написания комментария, констант (имен объектов) и отношений.

```prolog
% комментарий
гулять(дима, парк) % Утверждение: Дима гуляет в парке
```
Дима и Парк - константы, которые мы написали маленькими буквами, прогулка - это отношения. Первым делом записываем отношение, а затем в скобках и через запятую список объектов, которые на него ссылаются. И в конце мы всегда ставим точку. То, что Дима гуляет по парку, - факт. Факты и правила - это утверждения, из которых состоят программные данные. А цель - это то, что мы хотим узнать из программы. В Prolog есть внутренние процедуры для сопоставления целей с фактами и правилами, чтобы доказать (или вычислить) эти цели. Давайте посмотрим на пример переменной, факта и цели.
```prolog
гулять(дима,лес). % Факт: Дима гуляет в лесу
гулять(дима,парк). % факт: Дима гуляет в парке
гулять(дима,Что). % Цель: где гуляет дима? 
```
Переменные могут быть объектами как в утверждениях, так и в подцелях. Переменная для этой цели - Что. Когда программа пытается сопоставить эту цель с фактами или правилами программы, переменная Что не имеет значения, такие переменные называются свободными переменными. 
Когда свободная переменная целевого объекта Что совпадает с соответствующим объектом лес, значение Что становится лес. Теперь переменные Важные яблоки. Всякий раз, когда неназначенная переменная сопоставляется с константой, она получает значение этой константы. Переменная снова становится свободной, т.е. неназначенной, когда соответствие не удается или цель оценивается успешно. В прологе на экран выводится сообщение 'Что = лес; Что = парк' и что внутренняя процедура нашла все (или только) объекты, соответствующие цели. В логическом программировании используются такие слова, как если и или нет, равно / не равно. Например, если идет дождь, нужно взять с собой зонт. Маша и Лена дружат. Едем в зоопарк или в кино. Не девочка - мальчик. Пять кукол равны пяти платьям, но восемь кукол уже не равны. Также, например, можно делать такие вещи, как «цикл» - я ем мороженное, пока они не закончатся. Это действие, которое происходит до определенного момента. В нашем случае - пока не закончатся мороженное.

## Пример обучающего задания:

У тебя в классе есть 2 девушки, Аня и Катя, которые дружат. То есть они подруги. Запишем это, чтобы было лучше видно:

Аня девушка,
Катя девушка,
Аня дружит с Машей.
Значит Аня и Катя подруги. (важный вопрос: есть ли разница Катя дружит с Катей и Аня дружит с Машей)

Так же это можно записать так, как понятно компьютеру:
```prolog
девушка(аня).
девушка(катя).
друзья(аня, катя).
```
Как видно, разницы почти нет, но это еще не все. Надо записать, что Катя и Аня не просто друзья, а подруги. Это означает, что они обе девушки.
```prolog
подруги(катя,аня):-
    девушка(катя),
    девушка(аня),
    друзья(катя,аня).
% или
подруги(аня,катя):-
    девушка(катя),
    девушка(аня),
    друзья(аня,катя).
```

Вот так мы сказали компьютеру, что Аня и Катя девушки, и то, что они подруги.
То что они подруги, это прекрасно, но каждый раз описывать подруг таким образом немного неудобно, но компьютер позволяет нам быть ленивыми.

```prolog
подруги(Человек1,Человек2):-
    девушка(Человек1),
    девушка(Человек2),
    дружба(Человек1,Человек2).
```
Таким образом, подругами могут быть только 2 девушки, которые дружат. То же самое можно сказать словами: если Человек1 - девушка, а Человек2 - девушка, и если Человек1 дружит с Человек2, то они подруги. В этом примере мы видим, как можно задавать программе условия, которые нас интересуют. Программа сама будет логически обрабатывать полученную информацию и выдавать нам готовый результат. 

## Как научить?

Самое главное помнить о том, что обучать придется именно ребенка, а не взрослого человека или хотя бы подростка. Именно из-за того важно постараться не излагать исключительно сухие факты.

Постарайтесь красочно объяснить ребенку, что программировать интересно. Не говорите о его пользе в будущем, а именно заинтересуйте, для этого важно самому увлечься этой темой. Можно объяснить то, что благодаря логическому программированию, можно лучше изучить окружающий мир, узнать что-то новое.
Определите, что такое программирование в целом, особенно если ребенок ничего о нем не знает. 
Необходимо показать несколько элементарных примеров программ, чтобы ребенок занимался не только теорией. А после освоения теоретической базы пусть сам напишет самую простую программу.
И, конечно же, хвалите его за успех.

## Итог
Итак, в заключение хотелось бы отметить, что прежде чем начать преподавать кому-либо какой-либо предмет, важно сначала самому вникнуть в него и попытаться разобраться со всех сторон. А если нужно научить ребенка, то стоит удвоить усилия, так как всегда нужно помнить, что дети воспринимают информацию иначе, чем взрослые. Важнейшим критерием является их заинтересованность в процессе обучения, а этого можно добиться только в том случае, если вы сами интересуетесь предметом и можете правильно его преподнести. Имея такую основу, в будущем ребенок сможет самостоятельно изучить этот предмет, а также лучше понять, как описывать то, что его окружает. Он также узнает немного о программировании в целом и сможет улучшить свои логические навыки.

## Источники
1. [Обучение детей программированию](https://habr.com/ru/post/438278/)
2. [Prolog — удивительный язык программирования](https://habr.com/ru/post/124636/)
3. [Основы Prolog](https://www.sibsau.ru/sveden/edufiles/144224/)
