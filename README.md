# TG-exchange

Telegram-бот для конвертации валют с использованием реальных курсов. Проект демонстрирует навыки работы с API, обработку исключений и создание телеграм-ботов.

---

## 🚀 Особенности
- Конвертация через API Cryptocompare
- Кастомизированные исключения с понятными сообщениями
- Валидация ввода: отрицательные значения, некорректные валюты
- Модульная архитектура (конфиг, логика, ядро)

## 🔧 Технологии
- Python 3.8+
- `python-telegram-bot` для взаимодействия с API Telegram
- `requests` для HTTP-запросов

---

💬 Примеры Использования
Copy
/start -> "Введите: <валюта1> <валюта2> <количество>"
/values -> Список доступных валют
USD EUR 100 -> "Цена 100 USD в EUR: 93.5"
🧩 Структура Кода
python
Copy
# Обработчик конвертации
def get_price(message):
    try:
        quote, base, amount = message.text.split()
        result = Converter.get_price(quote, base, amount)
        bot.send_message(message.chat.id, f"Результат: {result}")
    except APIException as e:
        bot.reply_to(message, f"Ошибка: {e}")
        
📌 Для Работодателей
Чистая модульная архитектура

Документированный код

Готовность к масштабированию (добавление новых API/валют)
