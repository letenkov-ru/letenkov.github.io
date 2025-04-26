# Letenkov.ru

Дизайн сайта построен на [Hugo](https://gohugo.io) и теме [Hextra](https://github.com/letenkov-ru/hextra).

## Быстрый старт

Установите необходимые зависимости:

```shell
brew install hugo golang
```

Запустите сервер для локальной разработки:

```shell
hugo server --buildDrafts --source ./
```

## Локальная разработка

Для разработки и тестирования сайта используйте следующие команды:

```shell
# Запустить сервер Hugo с автоматической перезагрузкой
hugo server --disableFastRender --buildDrafts --source ./

# Сгенерировать статический сайт
hugo --source ./

# Обновление модулей для локального тестирования
hugo mod clean --all
hugo mod get -u ./...
hugo mod tidy --source ./

# Обновить основную ветку темы Hextra (только для локального тестирования)
hugo mod get -u github.com/letenkov-ru/hextra@main
```

## Управление зависимостями

Проект использует [Renovate](https://github.com/renovatebot/renovate) для автоматического обновления зависимостей, включая модули Hugo и тему Hextra.  
Renovate создаёт pull request'ы при выходе новых версий.

В большинстве случаев команды обновления модулей нужны только для локальной разработки, так как в основной ветке обновления происходят через Renovate.

Чтобы посмотреть текущую конфигурацию модулей, используйте:

```shell
hugo mod graph
```

Больше информации о работе с модулями Hugo можно найти в [официальной документации](https://gohugo.io/hugo-modules/).
