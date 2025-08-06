# Кейс №1 - изоляция сборки

- [Кейс №1 - изоляция сборки](#кейс-1---изоляция-сборки)
  - [Цель](#цель)
  - [Стэк](#стэк)
  - [Чекпоинты](#чекпоинты)
  - [Результат](#результат)
  - [Контакты](#контакты)

## Цель

Процесс сборки кода должен происходить автоматически, в том числе когда нет доступа в Интернет и внешние зависимости недоступны.

## Стэк

![Gitlab](https://img.shields.io/badge/Gitlab-FC6D26.svg?style=for-the-badge&logo=gitlab&logoColor=white)
![SonatypeNexus](https://img.shields.io/badge/Nexus-0FAF6C?style=for-the-badge&logo=sonatype&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

## Чекпоинты

1. Создать три виртуальные машины с ОС Ubuntu: *gitlab*, *build*, *nexus*;
2. [Установить gitlab](https://about.gitlab.com/install/) на виртуальную машину *gitlab*;
3. Установить [gitlab-runner](https://docs.gitlab.com/runner/) на виртуальную машину *build* и зарегистрировать в Gitlab;
4. Создать проект на Gitlab и написать Dockerfile и [пайплайн для сборки](https://docs.gitlab.com/ee/ci/) Docker-контейнера. Можно использовать [этот репозиторий](https://github.com/docker/docker-gs-ping.git) для работы;
5. [Установить Nexus](https://help.sonatype.com/en/installation-methods.html) на виртуальную машину *nexus*;
6. Создать Docker Hosted репозиторий в Nexus для хранения Docker-образов;
7. Добавить в пайплайн новую джобу для загрузки собранных образов на Nexus;
8. Создать [Docker Proxy репозиторий](https://help.sonatype.com/en/proxy-repository-for-docker.html) в Nexus для кэширования Docker-образов из других источников;
9. Добавить в джобу сборки использование Docker-proxy ([зеркалирование](https://docs.docker.com/docker-hub/mirror/)) с Nexus;
10. Создать [Golang Proxy репозиторий](https://help.sonatype.com/en/go-repositories.html) в Nexus для кэширования зависимостей Golang;
11. Добавить в Dockerfile использование прокси для сборки Golang проекта.

## Результат

При пуше новых изменений в репозиторий должна автоматически запускаться сборка образа через Gitlab CI/CD. Сборка должна успешно завершаться даже при отсутствии доступа в интернет. После сборки образ должен автоматически сохраняться в Nexus. Используя UI Nexus, можно увидеть загруженный образ.

## Контакты

Не стесняйтесь задавать вопросы в [нашем Telegram чате](https://t.me/+nSELCyIX8ltlNjU6)! Мы будем рады помочь🥰
