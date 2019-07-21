# Создание подключения к Metrica Logs API

{% note important %}

Перед созданием подключения к Metrica Logs API, вам необходимо создать кластер ClickHouse в Яндекс.Облаке. DataLens сохранит данные Metrica Logs API в датасет в созданный кластер.

{% endnote %}

Чтобы создать подключение к Metrica Logs API:
1. Перейдите на [страницу подключений](https://datalens.yandex.ru/connections).
1. Нажмите кнопку **Создать подключение**.
1. Выберите коннектор **Metrica**.
1. Укажите параметры подключения:
    - **Имя подключения**. Задайте имя подключения. Имя может быть произвольным.
    - **OAuth-токен**. Укажите OAuth-токен для получения доступа к данным Яндекс.Метрики.
    Если у вас уже есть счетчик, нажмите кнопку **Получить токен**.
    - **Счетчик**. Укажите счетчик для подключения.
    - **Подключение**. Выберите **Через Logs API** в качестве типа подключения.
1. Укажите параметры выгрузки данных:
    - **Источник счетчика**. Укажите таблицу c данными, которая будет выгружена из Metrica Logs API.
    - **Загружать с**. Укажите дату, начиная с которой будут выгружены данные.
    - **Регулярность**. Укажите режим обновления данных в подключении.
1. Укажите информацию о целевой базе данных:
    - **Имя хоста**. Укажите путь до хоста кластера ClickHouse в Яндекс.Облаке.
    - **Порт**. Укажите порт подключения к БД.
    - **Имя базы данных**. Укажите имя БД для подключения.
    - **Кластер**. Укажите кластер БД.
    - **Имя пользователя**. Укажите имя пользователя для подключения к БД.
    - **Пароль**. Укажите пароль для указанного пользователя.
1. Нажмите **Подключить**. Подключение появится в списке.

Примечания:
- Загрузка данных в подключение может занять от нескольких минут до нескольких часов в зависимости от объема данных в счетчике и указанной начальной даты загрузки.
- Изменение параметра **Загружать с** влечет за собой полную перезагрузку данных подключения.
- Изменение параметра **Регулярность** с `Единовременной` на `Регулярную` загрузку влечет полную перезагрузку данных подключения.