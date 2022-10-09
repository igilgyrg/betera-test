# Betera APOD service

Cервис юного астролога. Сервис выполняет функции:

1) Получает картинку дня [APOD](https://api.nasa.gov/). При отсутствии есть возможность сохранить в AWS S3 bucket;
2) Реализованы API: метод получения всех записей альбома и записи за выбранный день;
3) Реализован функционал JWT авторизации.
4) Сервис собиратся в docker-образ;

**Технологии**: postgreSQL, docker, docker-compose, makefile, aws s3, echo

**Примечания:**

- Для конфигурирования проекта используются переменные ENV;
- Сервис создает таблицу юзеров в базу данных. Фотограции хранятся в S3 бакете;

## How to use it

### Running

Чтобы запустить сервис локально, используйте команду

    make run-local
    
    Test user
        FIRST NAME: Igor
        LAST NAME: Pomazkov
        EMAIL: ig.pomazkov@gmail.com
        PASSWPRD: cherry

Чтобы собрать сервис в докер образ и запустить одновременно используйте команду

```bash
make build-local
```