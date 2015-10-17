Вопросы по Git
==============
> Как откатить patch?

Version control->Log
Правой кнопкой на нужной ревизии -> Reset Current Branch to Here
Soft- оставить все изменения, Hard - все затереть (в том числе локальные изменения)
![resetcurrentbranch](https://cloud.githubusercontent.com/assets/13649199/10559911/03be0a98-7503-11e5-98c6-eea3f062aba5.png)

<hr>
> Patch не накатывается (предлагает merge)

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

Сравнить содержимое можно скопировав содержимое из github в буфер:
![github_raw](https://cloud.githubusercontent.com/assets/13649199/10560413/52ec4e08-7513-11e5-8386-1c52eb55b5eb.png)

и следать Compare with clipboard в IDEA:
![compare_with_clipboard](https://cloud.githubusercontent.com/assets/13649199/10560411/4be3809a-7513-11e5-914e-94b4efb5b08e.png)
