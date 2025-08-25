# Кейс №3 - Hot-Warm архитектура

- [Кейс №3 - Hot-Warm архитектура](#кейс-3---hot-warm-архитектура)
  - [Цель](#цель)
  - [Стэк](#стэк)
  - [Чекпоинты](#чекпоинты)
  - [Результат](#результат)
  - [Контакты](#контакты)

## Цель

Для экономии места и ресурсов при хранении логов, необходимо переносить старые логи на виртуальные машины с менее мощным железом.

## Стэк

![Opensearch](https://img.shields.io/badge/opensearch_2.15-005EB8.svg?style=for-the-badge&logo=OpenSearch&logoColor=white)

## Чекпоинты

1. Развернуть [кластер](https://docs.opensearch.org/latest/tuning-your-cluster/#advanced-step-7-set-up-a-hot-warm-architecture) из 3 нод со следующими настройками:
   *  1 master-нода
   * 2 data-ноды c атрибутом температуры (hot,warm)
2. Создать [шаблон](https://docs.opensearch.org/latest/im-plugin/index-templates/) для индекса со следующими настройками:
   * 
   * Новые шарды создаются на ноде с атрибутом hot

## Результат

...

## Контакты

Нужна помощь? Пиши в [наш Telegram чат](https://t.me/+nSELCyIX8ltlNjU6) 🫶
