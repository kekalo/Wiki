Git
==============

### <a href="http://info.javarush.ru/idea_help/2014/02/14/Руководство-пользователя-IntelliJ-IDEA-Основы-работы-с-системами-контроля-версий-.html">Основы работы с системами контроля версий в IntelliJ IDEA</a>

- **Напоминаю, что патчи вы накатываете только в ветку `master`, а cвой код пишете только в ветках `HWxx`.
Модификация кода в ветке master только через патчи в материалах урока (Apply Patch), иначе придется мержить код.  Все патчи объязательны и применяются по порядку. Если при применении патча предлагается мержд, cмотрите: [Patch не накатывается (предлагает merge)](##patch-%D0%BD%D0%B5-%D0%BD%D0%B0%D0%BA%D0%B0%D1%82%D1%8B%D0%B2%D0%B0%D0%B5%D1%82%D1%81%D1%8F-%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%B0%D0%B3%D0%B0%D0%B5%D1%82-merge)
.**

- **Делать Apply Patch лучше по одному непосредственно перед видео на эту тему - тогда при просмотре вы сразу сможете отслеживать изменения кода проекта.**

- **Правило**: Перед каждым изменением проверяйте что меняется: Ctrl+D по всем файлам ченджлиста.
Если только пробелы - делайте revert.

## Как вести проект (у себя в локальном проекте):
#### Вступительное занятие:
- apply patch `Prepare_to_HW0.patch`
- git commit/push

#### Домашнее задание HW0:
- создать ветку HW0: в IDEA внизу справа `+ New Branch ->HW0`
![new_branch](https://cloud.githubusercontent.com/assets/13649199/13717279/8fcf7a42-e7f1-11e5-862f-b1fd3e302666.png)
- выполняете Домашнее Задание (HW0), git commit/push
- выполняете HW0 Optional, git commit/push

#### Урок 1:
- перключаемся на master:  в IDEA внизу справа `Local Branches -> master -> checkout`
- apply HW0/HW0-Optional/Lesson01 pathes,  git commit/push

#### Домашнее задание HW1:
- создать ветку HW1: в IDEA внизу справа `+ New Branch ->HW1`
- выполняете HW1, git commit/push
- выполняете HW1 Optional, git commit/push

#### Урок 2:
- перключаемся на master:  в IDEA внизу справа `Local Branches -> master -> checkout`
- apply HW1/HW1-Optional/Lesson02 pathes,  git commit/push
- ...

Так должна выглядеть ваш Version Control -> Log:
![branch](https://cloud.githubusercontent.com/assets/13649199/13716918/15c2a456-e7ef-11e5-9db2-8f2db69ff1e3.png)

## Как откатить patch?

Version control -> Log
Правой кнопкой на нужной ревизии -> `Reset Current Branch to Here`
`Soft`- оставить все изменения, `Hard` - все затереть (в том числе локальные изменения)
![resetcurrentbranch](https://cloud.githubusercontent.com/assets/13649199/10559911/03be0a98-7503-11e5-98c6-eea3f062aba5.png)

<hr>
## Patch не накатывается (предлагает merge)

Вероятнее всего Ваша ветка master не соответствует моей.
Нужно сравнить проблемный файл:

посмотреть содержимое файла для определенной версии в IDEA можно
через Git->History на файле:
![idea_history](https://cloud.githubusercontent.com/assets/13649199/10560189/9f6b6046-750b-11e5-863e-6084cdeeb3ed.png)
или на истории изменений Version Control->Log
![idea_revision](https://cloud.githubusercontent.com/assets/13649199/10560200/e585d67e-750b-11e5-865c-a9485c68435f.png)
и двойном щелчке на файле.

Сравнивать можно в github с текущей версией проекта либо с соответствующей ревизией:
![github_revision](https://cloud.githubusercontent.com/assets/13649199/10560234/347dbeda-750d-11e5-8b03-a1b62b94166d.png)

<hr>
Сравнить содержимое можно скопировав содержимое из github в буфер:
![github_raw](https://cloud.githubusercontent.com/assets/13649199/10560439/304104e2-7514-11e5-9aea-16bf2466da83.png)

и следать Compare with clipboard в IDEA:
![compare_with_clipboard](https://cloud.githubusercontent.com/assets/13649199/10560411/4be3809a-7513-11e5-914e-94b4efb5b08e.png)

Если ваш файл совпадает с тем, что в репозитории и патч все равно не накатывается, напришите мне в личку- имя файла, номер патча и проблемные строки, я поправлю патч. Картинок с вашими ошибками слать НЕ НАДО, учимся грамотно определять и описывать проблему.