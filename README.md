# TgFreeReferal
# ⚡ Telegram Referral Flooder Pro (v4.2 Enterprise)

<p align="center">
  <img src="app_icon.png" width="128" height="128" alt="Logo" style="border-radius: 20px;">
</p>

<p align="center">
  <strong>Высокотехнологичный симулятор и дашборд распределённой инжекции реферального трафика MTProto</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/GUI-Tkinter%20%2F%20HTML5-2481CC?style=flat" alt="GUI">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Web-0e1621?style=flat" alt="Platform">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
</p>

---

## 📌 О проекте

**TG Referral Flooder Pro** — это графический интерфейс (GUI) и симулятор телеметрии, демонстрирующий модель распределённой генерации реферального трафика для Telegram-ботов через протокол MTProto.

Проект разработан для демонстрации архитектуры высоконагруженных сетевых утилит, моделирования поведения сессий при столкновении с механизмами защиты (Telegram Anti-Spam, FloodWait, Cloudflare Turnstile, капчи) и визуализации очередей потоков в реальном времени.

---

## 🚀 Ключевые возможности

- **🎨 Тёмный интерфейс Telegram Desktop:** Оформление в фирменной цветовой гамме `#0e1621` / `#17212b` с адаптивными карточками метрик и прогресс-баром.
- **🔄 Модуль предпусковой диагностики (Pre-Flight):** Эмуляция проверки DC (Data Center #1..#5), валидация реферальных токенов `?start=` и проверка доступности прокси-пула.
- **⚡ Симуляция многопоточности MTProto:** Реалистичный генератор событий в терминале с таймштампами, поддержкой ротации отпечатков устройств (Android 14, iOS 18, Windows TDLib) и пула резидентных IP.
- **⚠️ Реалистичная плотность ошибок (~75%):** Моделирование ответов `RPCError 420: FLOOD_WAIT`, `PEER_FLOOD`, таймаутов SOCKS5 и автоматических процедур Retry/Backoff.
- **🌐 Две независимые реализации:** Нативное настольное приложение на Python (Tkinter) и автономная веб-версия (HTML5 / CSS / Vanilla JS).

---

## 📁 Структура проекта

```text
├── app_icon.ico          # Мультиформатная иконка Windows (16x16 - 256x256)
├── app_icon.png          # Логотип высокого разрешения (512x512)
├── gui.py                # Основное настольное приложение (Python + Tkinter)
├── index.html            # Автономная веб-версия дашборда
├── start.bat             # Скрипт быстрого запуска для Windows
└── README.md             # Документация проекта
```

---

## 🛠 Быстрый старт

### Требования
* Python 3.10 или выше
* Библиотека Pillow (для загрузки иконок):
  ```bash
  pip install Pillow
  ```

### Запуск настольной версии
1. Склонируйте репозиторий:
   ```bash
   git clone https://github.com/ВАШ_НИКНЕЙМ/tg-referral-flooder-pro.git
   cd tg-referral-flooder-pro
   ```
2. Запустите приложение через батник или терминал:
   ```bash
   python gui.py
   ```

### Запуск веб-версии
Просто откройте файл `index.html` в любом современном веб-браузере (Chrome, Edge, Firefox, Safari).

---

## 📦 Сборка автономного исполняемого файла (.exe)

Для сборки приложения в один `.exe` файл с привязкой иконки:

```bash
pip install pyinstaller
pyinstaller --noconsole --onefile --icon=app_icon.ico gui.py -n "TG_Referral_Flooder_Pro"
```
Итоговый файл будет сгенерирован в каталоге `dist/`.

---

## 📄 Лицензия

Проект распространяется под свободной лицензией **MIT License**. Подробности в файле `LICENSE`.
