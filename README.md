# AI Trading Assistant — GitHub Pages

Репозиторий для публикации frontend через GitHub Pages.

## Что важно

GitHub Pages запускает только статический frontend. Он **не запускает** Python/FastAPI backend, постоянный Telegram polling bot, worker или базу данных. После публикации frontend будет работать в явно обозначенном demo-режиме. Для реальных запросов к API нужен отдельно размещённый HTTPS backend.

## Как опубликовать

1. Загрузите содержимое папки проекта из [готового архива](https://github.com/setmyww/ai-trading-assistant) в корень этого репозитория. Должна появиться папка `frontend/` с файлами `package.json`, `vite.config.ts`, `index.html` и `src/`. Также сохраните папку `.github/workflows/`.
2. Откройте **Settings → Pages** и в поле **Build and deployment → Source** выберите **GitHub Actions**.
3. Откройте **Actions**. Workflow **Deploy frontend to GitHub Pages** должен запуститься после добавления frontend в ветку `main`.
4. Когда workflow завершится успешно, адрес сайта будет показан в **Settings → Pages**. Для репозитория это обычно `https://setmyww.github.io/ai-trading-assistant/`.

## Безопасность

Не публикуйте `.env`, Telegram bot token, приватные API-ключи, локальные базы данных или пользовательские данные. Переменные `VITE_*` встраиваются в публичные файлы браузера, поэтому в них нельзя хранить секреты.

Технические сигналы являются информационными и не гарантируют результат. Приложение не исполняет сделки.
