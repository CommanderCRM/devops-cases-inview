# Кейс №2 - Очистка образов 🧹

- [Кейс №2 - Очистка образов 🧹](#кейс-2---очистка-образов-)
  - [Цель](#цель)
  - [Стэк](#стэк)
  - [Чекпоинты](#чекпоинты)
  - [Результат](#результат)
  - [Контакты](#контакты)

## Цель

Артефакты, собранные при разработке, должны удаляться после того они перестают использоваться, во избежании быстрого переполнения хранилища артефактов

## Стэк

![Gitlab](https://img.shields.io/badge/Gitlab-FC6D26.svg?style=for-the-badge&logo=gitlab&logoColor=white)
![SonatypeNexus](https://img.shields.io/badge/Nexus-0FAF6C?style=for-the-badge&logo=sonatype&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

## Чекпоинты

1. Создать три виртуальные машины с ОС Ubuntu: *gitlab*, *build*, *nexus*;
2. [Установить GitLab](https://about.gitlab.com/install/) на виртуальную машину *gitlab*;
3. [Установить gitlab-runner](https://docs.gitlab.com/runner/) на виртуальную машину *build* и зарегистрировать в Gitlab;
4. Создать проект на Gitlab и написать Dockerfile и [пайплайн для сборки](https://docs.gitlab.com/ee/ci/) Docker-контейнера. Можно использовать [этот репозиторий](https://github.com/docker/docker-gs-ping.git) для работы;
5. [Установить Nexus](https://help.sonatype.com/en/installation-methods.html) на виртуальную машину *nexus*;
6. Создать Docker Hosted репозиторий в Nexus для хранения Docker-образов;
7. Добавить в пайплайн новую джобу для загрузки собранных образов на Nexus;
8. Добавить в пайплайн джобу для удаления ранее загруженного Docker-образа с Nexus, которая должна запускаться [по расписанию](https://docs.gitlab.com/ee/ci/pipelines/schedules.html) или при остановке Gitlab Environment;
9. Настроить в Nexus [задачи](https://help.sonatype.com/en/tasks.html) по расписанию для удаления неиспользуемых слоев и блобов. 

## Результат

По расписанию или при остановке Gitlab Environment должна происходить очистка образа в Nexus. Размер репозитория должен уменьшаться после удаления из него образов.

## Контакты

Нужна помощь? Пиши в [наш Telegram чат](https://t.me/+nSELCyIX8ltlNjU6) 🫶
