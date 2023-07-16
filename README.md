### Чтобы проверить что при `pull request` проходят все проверки

Возникнут трудности, пишите: https://t.me/rruslan_10

Версия node.js: v16.13.0

- Форкните проект
- Создайте ветку от `main`
- Внесите изменения(изменения можете сделать в файле test.txt в корне проекта), сделайте коммит и запуште
- Затем сделайте `pull request` из этой вашей ветки в `main`
- Во вкладке 'Pull requests' можете видеть как проходят проверки

### Чтобы проверить что при появлении релизного тэга создается Issue

- Находясь в `main` внесите изменения и сделайте коммит
- Затем добавьте тэг к этом коммиту командой `git tag <имя_тэга> <хэш_коммита>`
- Выполните команду `git push --tags`
- Во вкладке 'Actions' можете видеть как выполняются проверки
- После того как проверки пройдут появится релизная ветка с новым тэгом, а во вкладке 'Issues' в закрытых issue появится запись с этим тэгом
- Приложение выкладывается на gh-pages [https://rruslan10.github.io/shri-infrastructure-hw](https://rruslan10.github.io/shri-infrastructure-hw)

В этом репозитории находится пример приложения с тестами:

- [e2e тесты](e2e/example.spec.ts)
- [unit тесты](src/example.test.tsx)

Для запуска примеров необходимо установить [NodeJS](https://nodejs.org/en/download/) 16 или выше.

Как запустить:

```sh
# установить зависимости
npm ci

# запустить приложение
npm start
```

Как запустить e2e тесты:

```sh
# скачать браузеры
npx playwright install

# запустить тесты
npm run e2e
```

Как запустить модульные тесты:

```sh
npm test
```
