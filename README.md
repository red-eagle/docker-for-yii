docker-compose для yii-advanced.

Папку нужно поместить в корень проекта и выполнить docker-сompose up
Будет создан образ docker на базе php56-apache. В качестве БД используется mariadb последней версии.
frontend/web будет доступен по адресу localhost:8002
Данные для доступа к БД записываются в переменные окружения WEB_DB_HOST, WEB_DB_PORT, WEB_DB_PASSWORD.
Виртуальные хосты прописаны для фронт и бэкенда: yii.local и admin.yii.local соответственно.

TODO: в xdebug брать IP для удаленной отладки из системы.