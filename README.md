Дипломный проект профессии «Python-разработчик: расширенный курс»
Backend-приложение для автоматизации закупок
Цель дипломного проекта
Создадите и настроите проект по автоматизации закупок в розничной сети, проработаете модели данных, импорт товаров, API views.

Вам нужно:

разработать backend для сервиса заказа товаров,
усовершенствовать навыки работы с Django ORM через проработку моделей товаров и связанных сущностей,
реализовать импорт и экспорт товаров,
внедрить систему управления заказами,
оптимизировать методы с использованием асинхронности,
освоить работу со сторонними библиотеками и фреймворками,
подготовить документацию к проекту,
использовать AI инструменты для решения задач.
Чеклист готовности к работе над проектом
Изучить материалы лекции подготовки к дипломной работе.
Подготовить компьютер или виртуальную машину с ОС Linux или MacOS (не рекомендуем использовать Windows).
Установить IDE с поддержкой Python: Pycharm, VS Code или др.
Установить версию Python 3.10 или более позднюю.
Установить AI-плагин из списка:
Machinet,
Codeium,
Tabnine,
Amazon Сodewhisperer,
Mutable.AI,
Google Duet-AI.
Инструкция к работе над проектом
Общее описание приложения
Приложение предназначено для автоматизации закупок в розничной сети через REST API.

Внимание! Все взаимодействие с приложением ведется через API запросы. Реализация фронтенд-приложения возможна только по желанию обучающегося

Пользователи сервиса:

Клиент (покупатель):
делает ежедневные закупки по каталогу, в котором представлены товары от нескольких поставщиков,
в одном заказе можно указать товары от разных поставщиков,
пользователь может авторизироваться, регистрироваться и восстанавливать пароль через API.
Поставщик:
через API информирует сервис об обновлении прайса,
может включать и отключать приём заказов,
может получать список оформленных заказов (с товарами из его прайса).
Задача
Необходимо разработать backend-часть сервиса заказа товаров для розничных сетей на Django Rest Framework.

Базовая часть:

разработка сервиса под готовую спецификацию (API),
возможность добавления настраиваемых полей (характеристик) товаров,
импорт товаров,
отправка накладной на email администратора (для исполнения заказа),
отправка заказа на email клиента (подтверждение приёма заказа).
Продвинутая часть (необязательная к выполнению, не влияет на получение зачёта):

экспорт товаров,
админка заказов (проставление статуса заказа и уведомление клиента),
выделение медленных методов в отдельные асинхронные функции (email, импорт, экспорт).
Обратите внимание!

В репозитории приведён готовый пример с базовой частью проекта. Вы можете работать с проектом, выбрав один из двух вариантов:

разработать свою версию, исходя из текстового описания базовой части проекта,
взять за основу пример из репозитория, изучить его и выполнить продвинутую часть задания.
Вы можете интерпретировать текстовое описание проекта по-своему. Работа над дипломом - это в первую очередь творческий процесс. Главное - отсутствие плагиата (не сдавать работы других студентов).

Исходные данные для проекта
Общее описание сервиса
Спецификация (API) - 1 шт.
Файлы yaml для импорта товаров - 1 шт.
Базовый пример API Сервиса для магазина
Этапы разработки
Разработку backend рекомендуется разделить на следующие этапы.

Базовая часть:

Создание и настройка проекта.
Проработка моделей данных.
Реализация импорта товаров.
Реализация API views.
Полностью готовый backend.
Продвинутая часть (выполняется по желанию, если базовая часть полностью готова):

Реализация forms и views админки склада.
Вынос медленных методов в задачи Celery.
Создание docker-compose файла для приложения.
Разработку следует вести с использованием git (github/gitlab/bitbucket) с регулярными коммитами в репозиторий, доступный вашему дипломному руководителю. Старайтесь делать коммиты как можно чаще.

Этап 1. Создание и настройка проекта
Критерии достижения

Вы имеете актуальный код данного репозитория на рабочем компьютере.
У вас создан Django-проект, и он запускается без ошибок.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 2. Проработка моделей данных
Критерии достижения

Созданы модели и их дополнительные методы.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 3. Реализация импорта товаров
Критерии достижения

Созданы функции загрузки товаров из приложенных файлов в модели Django.
Загружены товары из всех файлов для импорта.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 4. Реализация APIViews
Критерии достижения

Реализованы API Views для основных страниц сервиса (без админки):
Авторизация
Регистрация
Получение списка товаров
Получение спецификации по отдельному товару в базе данных
Работа с корзиной (добавление, удаление товаров)
Добавление/удаление адреса доставки
Подтверждение заказа
Отправка email c подтверждением
Получение списка заказов
Получение деталей заказа
Редактирование статуса заказа
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 5. Полностью готовый backend
Критерии достижения

Полностью работающие API Endpoint'ы
Корректно отрабатывает следующий сценарий:
пользователь может авторизироваться,
есть возможность отправки данных для регистрации и получения email с подтверждением регистрации,
пользователь может добавлять в корзину товары от разных магазинов,
пользователь может подтверждать заказ с вводом адреса доставки,
пользователь получает email с подтверждением после ввода адреса доставки,
пользователь может переходить на страницу «‎Заказы» и открывать созданный заказ.
Для получения подробностей по данному этапу перейдите по ссылке.

Полезные материалы
Информация о сервисе
Спецификация API
Описание страниц сервиса
Продвинутая часть (выполняется по желанию, не влияет на получение зачёта)
Обязательное условие: базовая часть проекта полностью готова.

Этап 6. Реализация API views админки склада
Критерии достижения

Реализованы API views для страниц админки сервиса.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 7. Вынос медленных методов в задачи Celery
Критерии достижения

Создано Celery-приложение c методами:
send_email,
do_import.
Создан view для запуска Celery-задачи do_import из админки.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 8. Создание docker-compose файла для приложения
Создать docker-compose файл для сборки приложения.
Предоставить инструкцию для сборки docker-образа.
Важно: не нарушайте дедлайн сдачи, возникающие вопросы задавайте в чате с дипломным руководителем.

Правила приёма дипломной работы
Проект разместить в GitHub. Ссылка на дипломную работу должна оставаться неизменной, чтобы дипломный руководитель мог видеть ваш прогресс.
Сдавать финальный вариант дипломной работы в личном кабинете Нетологии.
Критерии оценки
Зачёт по дипломной работе можно получить, если работа соответствует критериям:

работоспособный проект в репозитории с документацией по запуску,
выполненная базовая часть проекта,
наличие собственных комментариев к коду,
использование сторонних библиотек и фреймворков.