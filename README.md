## Домашняя работа "Тестирование web-страницы вклада "Накопилка"

### Варианты автоматизируемых сценариев

#### - Вариант входа 1.
    1. Открыть сайт по адресу https://alfabank.ru/
    2. Навести курсор на пункт меню "Вклады"
    3. На выпавшем меню кликнуть на пункт "Накопилка"
    4. На окрывшейся странице нажать кнопку "Заполнить заявку"
    5. Заполнить необходимые пункты
    6. Нажать кнопку "Мы перезвоним"
#### - Вариант входа 2.
    1. Открыть сайт по адресу https://alfabank.ru/
    2. Нажать на пункт меню "Вклады"
    3. На открывшейся странице нажать на кнопку "Архивные счета и депозиты" 
    4. На окрывшейся странице нажать на пункт "Накопилка"
    5.  На окрывшейся странице нажать кнопку "Заполнить заявку"
    6. Заполнить необходимые пункты
    7. Нажать кнопку "Мы перезвоним"

### Общая часть для обоих вариантов:
    1. Позитивный сценарий: 
        - Заполнение полей: имя - кирилицей, телефон - коректный номер телефона, проставленный чекбокс в пункте "Я согласен".
        Ожидаемый результат - открытие следующей страницы.

    2. Негативные сценарии:
        
        2.1. Отправка пустой анкеты.
        Ожидаемый результат  - сообщение "Укажите имя".
        
        2.2. Тесты по  графе "Имя"
        
        - Отправка анкеты без имени: имя - незаполенено, телефон - коректный номер телефона, проставленный чекбокс в пункте "Я согласен".
        Ожидаемый результат  - сообщение "Укажите имя".
        - Отправка анкеты с именем написаным латиницей: имя - Petr, телефон - коректный номер телефона, проставленный чекбокс в пункте "Я согласен".
        Ожидаемый результат  - сообщение "Имя должно быть написано кирилицей".
        - Отправка анкеты с именем написаным цифрами: имя - 71688888, телефон - коректный номер телефона, проставленный чекбокс в пункте "Я согласен".
        Ожидаемый результат  - сообщение "Имя должно быть написано кирилицей".

        2.3. Тесты по графе "Телефон"
        
        - Отправка анкеты без номера телефона: имя - заполенено, телефон - не заполнен, проставленный чекбокс в пункте "Я согласен".
        Ожидаемый результат  - сообщение "Проверьте, пожалуйста, номер телефона".
        - Отправка анкеты с номером телефона из одной цифры: имя - заполенено, телефон - указана одна цифра, проставленный чекбокс в пункте "Я согласен".
        Ожидаемый результат  - сообщение "Проверьте, пожалуйста, номер телефона".
        - Отправка анкеты с некорректным номером телефона: имя - заполенено, телефон - номер из 11 цифр, проставленный чекбокс в пункте "Я согласен".
        Ожидаемый результат  - сообщение "Проверьте, пожалуйста, номер телефона".

        2.4. Тест по чекбоксу.

        - Заполнение полей: имя - кирилицей, телефон - коректный номер телефона, не проставлен чекбокс в пункте "Я согласен".
        Ожидаемый результат - сообщение "Не заполнен пункт о согласии на обработку лчиных данных.".




#### Используемы инструменты
    1. Github - хранение кода
    2. Junit - платформа для написания автотестов
    3. Gradle - система управления зависимостями
    4. Chrome - DeveloperTools - нахождение элементов CSS.
    5. Java - язык програмирования.
    6. Selenium/ Selenide - инструменты автоматизации браузеров.
    7. Allure - инструмент для репортинга

#### Перечень необходимых разрешений/данных/доступов
Автоматизированое тестирование публичного сайта это "табу". Необходимо письменное разрешение для тестирования.
Запросить тестовый jar-файл или доступ к тестовой СУБД (не верю что такой нет =) )

#### Риски автоматизации
1. Трата лишнего времени и средств. Конкретно в этом задании, на мой взгляд, нет необходимости  тестирования попадания на страницу заявки.  Считаю, что необходимо только автотестирование заполнения и отправки заявки.
2. Невозможность автоматизации - так как необходимо провести тестирование публичного сайта, то без разрешения это невозможно сделать.
3. Возможные ложные срабатывания тестов, если будут ошибки в тестах.
4. Единственным верным результатом тестироания будет успешное открытие следующей страницы.
5. Риск паданеия тестов при изменении структуры сайта.
6. Сложность нахождения селекторов для написания тестов.

#### Перечень необходимых специалистов для автоматизации
Для данной задачи, на мой взгляд, хватит одного тестировщика автомотизатора.

#### Интервальная оценка с учётом рисков (в часах)
Сложный вопрос для меня, так как опыта можно сказать, что нет. Думаю мне для решения данной задачи понадобилось бы 10-12 часов в данный момент.