#  Django-проект Kittygram: управление котиками.

![]https://github.com/VladSmyslov/kittygram_final/actions/workflows/main.yml/badge.svg

##  Описание проекта

Kittygram — социальная сеть для обмена фотографиями любимых питомцев. Это полностью рабочий проект, который состоит из бэкенд-приложения на Django и фронтенд-приложения на React.

##  Как работать с репозиторием финального задания


### Как запустить проект:

Установить Docker

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/yandex-praktikum/kittygram_backend.git
```

Запустить проект:

```
docker compose up
```
Выполнить миграции:

```
docker compose exec backend python manage.py migrate
```

### Как заполнить .env:

Установите модуль python-dotenv с помощью pip.

Создайте файл .env со следующими переменными:
```
POSTGRES_USER - имя пользователя БД.
```
```
POSTGRES_PASSWORD - пароль пользователя БД.
```
```
POSTGRES_DB - название базы данных.
```
```
DB_HOST - адрес, по которому Django будет соединяться с базой данных.
```
```
DB_PORT - порт, по которому Django будет обращаться к базе данных. 5432 — это порт по умолчанию для PostgreSQL.
```
```
SECRET_KEY - секретный ключ
```
```
DEBUG - режим отладки
```
```
ALLOWED_HOSTS - список имен хостов / доменов, на которых может обслуживаться ваш веб-сервер.
```

Добавьте его в файл .gitignore, чтобы git не закоммитил его.

Загрузите конфигурацию в файлы Python с помощью модуля Python-dotenv.

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.

## Стек используемых технологий

- Django.
- Django REST Framework.
- PostgreSQL.
- Docker и Docker-compose.
- Git.
- GitHub Actions.
- Flake8.

## Автор

Vladislav Smyslov
