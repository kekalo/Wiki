### <a href="http://jeeconf.com/archive/jeeconf-2013/materials/intellij-idea/">Эффективная работа с кодом в IntelliJ IDEA</a>

### <a href="http://info.javarush.ru/idea_help/2014/01/22/Руководство-пользователя-IntelliJ-IDEA-Отладчик-.html">Отладчик IntelliJ IDEA</a>

Ctrl+Shift+A:  справочник (поиск) по использованию горячих клавиш

### Деплой war в Tomcat (`Application Context` должен быть тот же, что и url приложения, деплоить надо `war exploded`)
![tomcat](https://cloud.githubusercontent.com/assets/975870/11599106/057932c4-9ad6-11e5-9e9e-fe9fd389532e.png)

###   Ошибки Spring: There is more than one bean / Coudln't autowire:
![spring_ctx](https://cloud.githubusercontent.com/assets/13649199/10559681/96b8bcca-74ff-11e5-8203-8d0d4cf1bd19.png)


Проверьте, что правильно выставлены профили Spring.
Проверьте - нет ли лишних бинов (или наоборот их не хватает) в Project Structure->Modules->Spring:

![spring-ctx2](https://cloud.githubusercontent.com/assets/13649199/10559730/4e60dea2-7500-11e5-8018-420e12fc7f5c.png)

<hr>
### Поставить кодировку UTF-8

Выставьте в Settings->File Encoding везде UTF-8.

Также можно сконвертировать файл в нужную кодировку внизу в строке статуса (View->Status Bar поднят).
![utf-8](https://cloud.githubusercontent.com/assets/13649199/10559841/e1b65654-7501-11e5-8913-d2b5b4e25087.png)

<hr>
### Поменять фонт по умолчанию (DejaVu):
- Скачиваете https://sourceforge.net/projects/dejavu/ и устанавливаете в систему
- Перегружаете IDEA
- В IDEA Settings нужно сделать схеме Save As с именем, отличным от Default:
![idea_fonts](https://cloud.githubusercontent.com/assets/11200258/11875035/b09d058c-a4f3-11e5-9d35-88e1b607c310.png)