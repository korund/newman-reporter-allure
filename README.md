This is a fork of https://github.com/dvargas46/newman-reporter-allure

## Особенности


Реализована поддержка Allure TestOps:
- Добавлены следующие Labels: testClass, testMethod, epic, owner, layer.
- Изменена логика формирования story и suite.

Отсуттвуют проблемы с формированием русскоязычных имён тестов.

Добавлена обработка test-scripts errors.

## Установка

```bash
$ npm install -g https://github.com/cmttwd/newman-reporter-allure.git
```

## Запуск

```bash
$ newman run <Collection> -e <Environment> -r allure
$ newman run <Collection> -e <Environment> -r allure --reporter-allure-export <allure-results-out-dir>
$ newman run <Collection> -e <Environment> -r allure --reporter-allure-export <allure-results-out-dir> --reporter-allure-epic <Epic name> --reporter-allure-owner <Owner name> --reporter-allure-layer <Layer>
```

```bash
--reporter-allure-export <allure-results-out-dir> - путь результов отчета
--reporter-allure-epic <Epic name> - установка параметра Epic для всех тестов запуска
--reporter-allure-owner <Owner name> - установка Владельца/Ответсвенного для всех тестов запуска
--reporter-allure-layer <Layer> - доп параметр
```

## Генерация отчета

```bash
$ allure generate --clean
$ allure generate --clean <allure-results-out-dir>
```

## Открытие сгенерированного отчета
```bash
$ allure open
$ allure open <allure-report-dir>
```