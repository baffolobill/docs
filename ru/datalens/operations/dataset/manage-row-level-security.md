# Управление доступом к строкам данных датасета

Чтобы настроить права доступа к строке данных:
1. Откройте датасет.
1. В правой части строки нажмите значок ![image](../../../_assets/datalens/horizontal-ellipsis.svg) и выберите **Права доступа**.
1. Введите значение поля и пользователей в указанном формате и нажмите **Сохранить**.

   ```yaml
   '[значение 1]': [пользователь 1], [пользователь 2]
   '[значение 2]': [пользователь 3]
   ```
   
   Например,
   
   ```yaml
   '2017-01-01': login-to-access-your-row-data@yandex.ru
   ```
   
1.  Сохраните датасет.

{% include [rls-note](../../../_includes/datalens/datalens-rls-note.md) %}