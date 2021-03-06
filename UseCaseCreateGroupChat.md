## Термины предметной области

Преподаватель

Студент

Пользователь — преподаватель или студент

Мобильное приложение

Веб-сайт

Приложение — мобильное приложение или веб-сайт

База данных

## Сценарий использования
# Создание общего чата

**Акторы:** пользователь.

**Цель:** пользователь создаёт общий чат для совместного общения нескольких пользователей.

**Предусловия:** пользователь зашёл в приложение, успешно авторизовался в нём, открыл список своих чатов.

**Сценарий:**

1. Пользователь нажимает кнопку "Создание нового чата" на верхней панели.
2. Приложение запрашивает список пользователей у бекенда.
3. Бекенд возвращает список пользователей, с которыми можно создать чат.
4. Приложение отображает список пользователей.
5. Пользователь нажимает кнопку "Создат групповой чат" на верхней панели.
6. Напротив каждого имени в списке появляется чекбокс.
7. Пользователь ставит галочку в чекбоксы напротив тех пользователей, которых он хочет добавить в общий чат.
8. Если выбрано больше одного пользователя, загорается кнопка "Готово"
9. Пользователь нажимает кнопку "Готово".
10. Приложение отправляет в бекенд запрос на создание нового чата.
11. Бекенд возвращает ответ успешного создания чата.
12. Приложение создаёт общий чат с выбранными пользователями.
13. Приложение открывает новое окно чата с выбранными пользователями.

**Результат:**

- Открывается окно общего чата с пользователями.
- В базу добавлен новый чат.
- Новый общий чат виден в списке чатов.
- В окне общего чата отображается переписка всех участников с момента начала.

**Альтернативы или исключения**

3а. Бекенд вернул пустой список.

3а1 Приложение выводит сообщение о том, что писать некому

6а. Нужного человека нет в списке пользователей.

6а1. Пользователь набирает телефон/никнейм/имя пользователя/адрес электронной почты в строке поиска.

6а2. Приложение запрашивает профиль пользователя у бекенда.

6а3. Бекенд возвращает профиль запрашиваемого пользователя.

6а4. Приложение отображает профиль найденного пользователя с чекбоксом напротив.

6а5. Пользователь ставит галочку в чекбокс, возврат к шагу №8

11а. Пользователь ограничил возможность создания чата с ним настройками приватности.

11а1. Приложение выводит сообщение о том, что невозможно создать приватный чат с выбранным пользователем

11б. Бекенд вернул код ошибки.

11б1. Приложение выводит сообщение с кодом ошибки и её пояснением.

6а3.1. Пользователь не найден.