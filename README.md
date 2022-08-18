# API для сервиса YAMDB
## 
**YAMDB**  собирает отзывы пользователей на произведения в категориях «Книги», «Фильмы», «Музыка».
Проект представляет собой web-приложение и базу данных, поднятых в двух docker-контейнерах.

При разработке приложения использованы фреймфорки ```django и django-rest-framework```. В качестве базы выступает ```postgresql```
Запуск проекта осуществляется средствами ```docker```

## Установка

#### 1. Установка docker и docker-compose

Если у вас уже установлены docker и docker-compose, этот шаг можно пропустить, иначе можно воспользоваться официальной [инструкцией](https://docs.docker.com/engine/install/).

#### 2. Запуск контейнера
```bash
docker-compose up
```
### 3. Выключение контейнера
```bash
docker-compose down
```


## Использование
#### Создание суперпользователя Django
```bash
docker-compose run web python manage.py createsuperuser
```

#### Пример инициализации стартовых данных:
```bash
docker-compose run web python manage.py loaddata fixtures.json
```


#### Работа с api
Документация ко всем ручкам описана в redoc

## Основные использованные технологии
* python
* [django](https://www.djangoproject.com/)
* [drf](https://www.django-rest-framework.org/)
* [posgresql](https://www.postgresql.org/)
* [docker](https://www.docker.com/)