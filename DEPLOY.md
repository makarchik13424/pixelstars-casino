# Pixelstars Casino - Деплой

Этот проект готов для развертывания на https://pixelstars1.onrender.com

## Настройка Render.com

### 1. Настройка переменных окружения в Render
В панели Render добавьте следующие переменные:
```
BOT_TOKEN=ваш_токен_бота_от_BotFather
WEBHOOK_URL=https://pixelstars1.onrender.com/webhook
WEBAPP_URL=https://pixelstars1.onrender.com
NODE_ENV=production
PORT=10000
WEBHOOK_SECRET=любая_случайная_строка_для_безопасности
```

### 2. Настройка бота в @BotFather
1. Откройте @BotFather в Telegram
2. Отправьте команду `/setmenubutton`
3. Выберите вашего бота
4. Добавьте кнопку меню:
   - Текст: "🎮 Играть"
   - URL: `https://pixelstars1.onrender.com`

### 3. Автодеплой
- Render автоматически пересобирает проект при каждом пуше в main ветку
- Команда запуска: `npm start` (уже настроена в package.json)
- Порт: 10000 (стандарт для Render)

## После деплоя

1. Откройте вашего бота в Telegram
2. Нажмите /start или кнопку "🎮 Играть"
3. Проверьте работу кейсов
4. Протестируйте систему пополнения через @puwmvshop_bot

## Мониторинг

- Логи доступны в панели Render
- Webhook автоматически настроится при первом запуске
- База данных SQLite создается автоматически

## Обновления

Для обновления просто делайте:
```bash
git add .
git commit -m "Update description"
git push origin main
```

Render автоматически пересоберет и задеплоит!