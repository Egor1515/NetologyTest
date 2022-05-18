
# Предусловия к каждому тесту: 
Перед выполнением тестов должен быть осуществлен переход к форме регистрации.
## Валидные данные для всех полей
1. **Ввод мужского имени**
* Ввести имя "Егор"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
2. **Ввод женского имени**
* Ввести имя "Ольга"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
3. **Ввод имени с непонятным родом**
* Ввести имя "Саша"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно, на почту приходи письмо с пометкой "Уважаемый(ая)"
4. **Ввод распространенного имени**
* Ввести имя "Михаил"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
5. **Ввод редкого имени**
* Ввести имя "Спартак"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
6. **Ввод двойного имени**
* Ввести имя "Анна - Мария"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
7. **Ввод длинного имени**
*  Ввести имя "Пантелеймон"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
8. **Ввод короткого имени**
* Ввести имя "Ян"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
9. **Ввод составного имени**
*  Ввести имя "Канело Сауль"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
10. **Ввод иностранного имени**
* Ввести имя "Джеймс"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
11. **Ввод краткой формы имени**
* Ввести имя "Коля"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно"
12. **Ввод уменьшительной формы имени**
* Ввести имя "Олечка"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
13. **Ввод имени с буквой Ё**
* Ввести имя "Пётр"
* Ожидаемый результат: Поле подсвечивается зеленым, значение - валидно
14. **Ввод имени с опечаткой**
* Ввести имя "Олга"
* Ожидаемый результат: Клиент автоматически исправляет орфографическую ошибку
15. **Ввод имени с пробелом в начале**
* Ввести значение " Егор"
* Ожидаемый результат: Пробелы стираются автоматически, значение валидно
16. **Ввод имени с пробелом в середине**
* Ввести значение "Ег ор"
* Ожидаемый результат: Пробелы стираются автоматически, значение валидно
17. **Ввод имени с пробелом в конце**
* Ввести значение "Егор "
* Ожидаемый результат: Пробелы стираются автоматически, значение валидно
18. **Ввод валидного телефона**
* Ввести номер в формате "+9(999)999-99-99
* Ожидаемый результат : Поле подсвечивается зеленым, значение валидно
## Перечень автоматизируемых сценариев
1. **Авторизация с валидными данными**
* Ввести "Андрей" в поле Имя
* Ввести "+9 (999) 999-99-99" в поле Телефон
* Нажать кнопку "Записаться"
* Ожидаемый результат: На почту высылается письмо об успешной регистрации, на странице записи поп-ап об успехе записи
2. **Отправка пустой формы** 
* Опустошить поля формы(если они заполнены автоматически)
* Нажать кнопку "Записаться"
* Ожидаемый результат: Оба поля формы подсвечиваются красным, выдавая ошибку, запись не проходит
3. **Запись на консультацию**
* Заполнить поля своими данными
* Нажать на кнопку "Получить консультацию"
* Ожидаемый результат: Появляется поп-ап с дальнейшими инструкциями
4. **Валидация со стороны клиента, поле Имя**
* Опустошить поле Имя
* Ожидаемый результат: Поле подсвечивается красным, вылетает поп-ап с подсказкой "Обязательно поле"
5. **Валидация со стороны клиента, поле Телефон**
* Опустошить поле Телефон
* Ожидаемый результат: Поле подсвечивается красным, вылетает поп-ап с подсказкой "Обязательно поле"
6. **Вход для уже зарегистрированного пользователя**
* Нажать на кнопку "Войти"(Внизу формы регистрации)
* Ожидаемый результат: Открывается окно для ввода логина и пароля
7. **Очистка формы при обновлении страницы**
* Заполнить поля формы
* Нажать "Обновить страницу"
* Ожидаемый результат: Страница перезагружается, данные в форме регистрации НЕ сохраняются
8. **Ввод промокода** 
* Нажать на "У меня есть промокод"(Слева от формы регистрации)
* Ожидаемый результат: Открывается окно для ввода промокода
9. **Пользовательское соглашение** 
* Нажать на "Пользовательского соглашения"(внизу формы регистрации)
* Ожидаемый результат: Открывается окно со всей информацией об соглашении сторон
### Валидация поля Имя
1. **Ввод имени из двух букв в поле Имя**
* Ввести имя из одной буквы в поле Имя
* Ожидаемые результат: Поле Имя подсвечено красным, значение невалидно
2. **Ввод имени на английском**
* Ввести имя "Ben"
* Ожидаемый результат: Поле подсвечивается красным, значение - невалидно
3. **Ввод имени на английской раскладке**
* Ввести имя "Jkmuf"
* Ожидаемый результат:Клиент предлагает автоматически перевести имя на русскую раскладку
4. **Ввод цифр в поле имя**
* Ввести значение "123"
* Ожидаемый результат: Ошибка "Должно состоять из букв"
5. **Ввод символов в поле имя**
* Ввести значение "!"№!"№
* Ожидаемый результат: Ошибка "Должно состоять из букв"
### Валидация поля Телефон
1. **Ввод невалидного номера в поле Телефон** 
* Ввести номер "-123123123123"
* Ожидаемый результат: Поле подсвечивается красным, ошибка: "Номер в формате +9 (999) 999-99-99"
2. **Ввод букв в поле Телефон** 
* Ввести в поле Телефон значение "йцу"
* Ожидаемый результат: Поле подсвечивается красным, ошибка: "Номер в формате +9 (999) 999-99-99"
3. **Ввод символов в поле Телефон** 
* Ввести в поле Телефон значение "!"№
* Ожидаемый результат: Поле подсвечивается красным, ошибка: "Номер в формате +9 (999) 999-99-99"
### Кроссбраузерность 
1. **Уменьшение расширения браузера** 
* Уменьшить разрешение страницы перетягивая угол браузера к центру
* Ожидаемый результат: Верстка не едет, данные отображены правильно, функционал продолжает работать
2. **Установка расширения для Телефонов** 
* Открыть "Инструмент разработчика" (F12)
* Нажать на изображение планшета с телефоном (Слева от вкладки "Элементы") 
* Ожидаемый результат: Верстка не едет, данные отображены правильно, функционал продолжает работать
3. **Переворот страницы в расширении для Телефонов** 
* Открыть "Инструмент разработчика" (F12)
* Нажать на изображение планшета с телефоном (Слева от вкладки "Элементы")
* Перевернуть экран, нажать на значок "Повернуть"(Слева от изображения планшета с телефоном)
* Ожидаемый результат: Верстка не едет, данные отображены правильно, функционал продолжает работать
### Горячие клавиши
1. **Отправка формы клавишей Enter** 
* Заполнить форму валидными данными
* Нажать на клавишу "Enter"
* Ожидаемый результат: Форма отправляется
2. **Навигация с помощью табуляции** 
* Поставить курсор в поле Имя
* Заполнить Его
* Нажать на клавишу Tab
* Ожидаемый результат: Курсор переходит на следующую строку, можно продолжать ввод
3. **Закрытие поп-апов с помощью Escape** 
* Заполнить форму валидными данными
* Нажать на клавишу "Получить консультацию"
* Во всплывшем окне для продолжения нажать на Escape
* Ожидаемый результат: Окно закрывается, пользователь попадает обратно на форму регистрации

### Перечень используемых инструментов с обоснованием выбора

* Selenide - позволяет не хранить драйвер, а так же эффективен и прост в использовании
* junit4,Junit5,TestNG(Для написания авто-тестов и запуска) 
* Среда разработки(В нашем случае IDEA) - Ее функциональность и интеллект)
* Интеграция CI git actions - находится под рукой, проста в настройке.
* Инструменты репортинга, т.к: Allure - красочно и по факту, проста в подключении(в отличие от ReportPortal) и картина репорта полная
* Rest Assured(библиотека для тестирования REST Api)
* Язык программирования Java, версия 11 - причиной является LTS версия и возможность работать с постоянно обновляющимся обеспечением 

#### Перечень и описание возможных рисков при автоматизации

* Хардкод данных пользователя. Можем столкнуться с тем, что не будут проверены все сценарии и граничные значения
* Изменение требований в процессе(повлечет за собой большое количество проблем и затрат)
* Некорректно составленные тестовые сценарии, неправильно описаны шаги для автоматизации

##### Перечень необходимых специалистов для автоматизации

* Команда Тестировщиков: автоматизаторов - Для непосредственно написания тестов, мануальных- для составления тест-кейсов и сценариев

##### Перечень необходимых данных

* Тест-кейсы и сценарии для автоматизации
* Все данные для авторизации(логин, пароль, push-сообщения, и тд)
* Разрешение на автоматизацию от лица компании
* План о примерном представлении изменений после проведения автоматизации(стоит ли оно того?)
* Доступ к актуальным данным(для того, чтобы тестировать сам продукт и реальных пользователей)


##### Интервальная оценка с учётом рисков (в часах)

* 7 часов
