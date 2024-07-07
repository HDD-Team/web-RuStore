# Проект чата

Этот проект представляет собой QnA бота RuStore (система по технической документации), написанный на Vue.js. Чат позволяет задавать вопросы по технической документации RuStore.
## Установка

Чтобы установить и запустить проект, вам понадобится Node.js и npm. Выполните следующие команды:

1. Скачайте проект

2. Установите taiwindcss по документации:
```
https://tailwindcss.com/docs/guides/vite#vue
```
3. Запустите проект:
```
npm run dev
```
4. Запустите сервер FastAPI:
```
https://github.com/HDD-Team/back-RuStore
```

## Использование

После запуска приложения вы увидите интерфейс чата. В верхней части экрана расположена панель для выбора версии и логотип Rustore. Чтобы выбрать версию, нажмите на кнопку "Выберите версию" и выберите нужную версию из выпадающего меню.

В центральной части экрана расположен блок сообщений. Этот блок содержит все сообщения, которые были отправлены в чат. Сообщения отображаются в виде текстовых блоков с аватарами пользователей.

В нижней части экрана расположено поле ввода для отправки сообщений и две кнопки: для отправки сообщения и для очистки истории чата. Чтобы отправить сообщение, введите текст в поле ввода и нажмите кнопку "Отправить" или нажмите Enter.

## Структура проекта

Проект состоит из следующих папок и файлов:

* `public` - содержит статические файлы, такие как индексный файл HTML и фавикон.
* `src` - содержит исходные файлы приложения.
	+ `assets` - содержит статические ресурсы, такие как изображения и шрифты.
	+ `components` - содержит компоненты Vue.js.
	+ `App.vue` - основной компонент приложения.
	+ `main.js` - точка входа приложения.
* `.gitignore` - файл для игнорирования файлов и папок при коммите в Git.
* `babel.config.js` - файл конфигурации Babel.
* `package.json` - файл конфигурации проекта, содержит информацию о зависимостях и скриптах.
* `README.md` - этот файл.

## Демонстация

[DEMO](https://disk.yandex.ru/d/CHGsrcLrrUEKrA)

## Автор

[HDD](https://hdd-team.github.io/HDD-TEAM/)

---

Этот README-файл содержит основную информацию о проекте чата, включая инструкции по установке и использованию, структуру проекта и автора. Вы можете использовать этот файл в качестве шаблона для создания своего README-файла для проекта на GitHub.
