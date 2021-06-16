# spbu_diploma - LaTeX шаблон для ВКР СПбГУ (2021)

### Свежее обновление (3.05.2020) - вариант со шрифтом Tempora, выглядит значительно лучше
### (и больше похож на привычный для дипломов Times New Roman)

## Cтруктура:

* spbudiploma.sty - стилевой файл. Не рекомендуется изменять.
* spbudiploma_tempora.sty - aльтернативный стилевой файл со шрифтом Tempora (Правильно рендерятся размеры, шрифт больше похож на Times)
* titlepage_example.tex - пример титульника, который необходимо изменить под себя и сохранить отдельно, например, в titlepage.tex, чтобы изменения в файлах этого репозитория не влияли на ваш проект.
* main_example.tex - пример основного файла. Рекомендуется создать свой main.tex, чтобы изменения в main_example.tex не влияли на ваш проект.
* [main_example.pdf](https://github.com/itonik/spbu_diploma/blob/master/main_example.pdf) - пример получившегося PDF файла
* [main_example_tempora.pdf](https://github.com/itonik/spbu_diploma/blob/master/main_example_tempora.pdf) - пример PDF со шрифтом Tempora

## Важные замечания:

* Формулы рекомендуется оформлять не `$$<...>$$`, а с помощью `\begin{equation}<...>\end{equation}`. Пример с нумерованными и ненумерованными формулами есть в `main_example.tex`.
* Напоминаю, что в тексте вместо "..." необходимо использовать «...». Существует проблема с "...", когда после второй квычки «съедается» проблел. Лечится с помощью `\space` после второй кавычки.

## Какие документы регламентируют верстку ВКР?
По каджому направлению (первые ссылки):
https://edu.spbu.ru/gia.html

Титульник: http://edu.spbu.ru/images/data/normativ_acts/local/20180703_6616_1.pdf
На этот документ ссылаются документы по направлениям

## Как этим пользоваться?
Склонировать репозиторий к себе на компьютер, или, если вы пользуетесь онлайн-редактором,
скачать себе zip-архив и загрузить его. И обязательно регулярно заглядывать в репозиторий.

(Опция для просвещенных).
Можно форкнуть репозиторий, в нем писать свой диплом и периодически синкать его
с этим репозиторием.
Приобщиться к тайному знанию можно, например,
[тут](https://help.github.com/en/articles/syncing-a-fork)

Рекомендую смысловые части разбивать на отдельные файлы и в main соединять их с помощью
`\input{<имя_файла>.tex}`. Посмотрите как подключается `titlepage.tex`, красота!

## Как структурировать диплом?
Диплом состоит из глав и параграфов. Для нас, глава - это `\section`, а параграф - это `\subsection`.
Также существуют **особые** главы - это "Введение", "Постановка задачи", "Обзор литературы",
"Выводы", "Заключение". Они обязательно присутствуют, не нумеруются и должны идти в том порядке, в
каком они идут в примере. Оформляются коммандой `\specialsection{<название_особой_главы>}`

## Хочу предложить изменение. Куда писать, что делать?
В issue, а еще лучше сделать pull-request.
