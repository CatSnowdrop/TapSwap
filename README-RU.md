# TapSwap

[![Static Badge](https://img.shields.io/badge/Telegram-BOT-Link?style=for-the-badge&logo=Telegram&logoColor=white&logoSize=auto&color=blue)](https://t.me/tapswap_mirror_1_bot?start=r_352437152)

[![Static Badge](https://img.shields.io/badge/My_Telegram_Сhannel-@CryptoCats__tg-Link?style=for-the-badge&logo=Telegram&logoColor=white&logoSize=auto&color=blue)](https://t.me/CryptoCats_tg)

![img1](.github/images/demo.png)

[![Static Badge](https://img.shields.io/badge/README_in_Ukrainian_available-README_%D0%A3%D0%BA%D1%80%D0%B0%D1%97%D0%BD%D1%81%D1%8C%D0%BA%D0%BE%D1%8E_%D0%BC%D0%BE%D0%B2%D0%BE%D1%8E-blue.svg?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAwIiBoZWlnaHQ9IjgwMCI+DQo8cmVjdCB3aWR0aD0iMTIwMCIgaGVpZ2h0PSI4MDAiIGZpbGw9IiMwMDU3QjciLz4NCjxyZWN0IHdpZHRoPSIxMjAwIiBoZWlnaHQ9IjQwMCIgeT0iNDAwIiBmaWxsPSIjRkZENzAwIi8+DQo8L3N2Zz4=)](README-UA.md)
[![Static Badge](https://img.shields.io/badge/README_in_russian_available-README_%D0%BD%D0%B0_%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%BE%D0%BC_%D1%8F%D0%B7%D1%8B%D0%BA%D0%B5-blue?style=for-the-badge)](README-RU.md)


## Функционал
| Функционал																| Поддерживается |
|---------------------------------------------------------------------------|:---------:|
| Многопоточность															|     ✅     |
| Привязка прокси к сессии													|     ✅     |
| Авто-выполнение заданий🔥													|     ✅     |
| Авто-покупка предметов при наличии монет (tap, energy, charge)			|     ✅     |
| Рандомное время сна между кликами											|     ✅     |
| Рандомное количество кликов за запрос										|     ✅     |
| Поддержка tdata / pyrogram .session / telethon .session					|     ✅     |


## [Настройки](https://github.com/CatSnowdrop/TapSwap/blob/main/.env-example)
| Настройка                | Описание                                                                                      |
|--------------------------|-----------------------------------------------------------------------------------------------|
| **API_ID / API_HASH**    | Данные платформы, с которой запускать сессию Telegram _(сток - Android)_                      |
| **MIN_AVAILABLE_ENERGY** | Минимальное количество доступной энергии, при достижении которой будет задержка _(напр. 100)_ |
| **SLEEP_BY_MIN_ENERGY**  | Задержка при достижении минимальной энергии в секундах _(напр. [1800,2400])_                  |
| **ADD_TAPS_ON_TURBO**    | Сколько тапов будет добавлено при активации турбо _(напр. 2500)_                              |
| **AUTO_TASK**			   | Автовыполнение заданий _(True / False)_                            						   |
| **MAX_TASK_ITERATIONS**  | Количество заданий за 1 цикл _(напр. 4)_           						                   |
| **AUTO_UPGRADE_TAP**     | Улучшать ли тап _(True / False)_                                                              |
| **MAX_TAP_LEVEL**        | Максимальный уровень прокачки тапа _(до 20)_                                                  |
| **AUTO_UPGRADE_ENERGY**  | Улучшать ли энергию _(True / False)_                                                          |
| **MAX_ENERGY_LEVEL**     | Максимальный уровень прокачки энергии _(до 20)_                                               |
| **AUTO_UPGRADE_CHARGE**  | Улучшать ли заряд энергии _(True / False)_                                                    |
| **MAX_CHARGE_LEVEL**     | Максимальный уровень прокачки заряда энергии _(до 5)_                                         |
| **APPLY_DAILY_ENERGY**   | Использовать ли ежедневный бесплатный буст энергии _(True / False)_                           |
| **APPLY_DAILY_TURBO**    | Использовать ли ежедневный бесплатный буст турбо _(True / False)_                             |
| **RANDOM_CLICKS_COUNT**  | Рандомное количество тапов _(напр. [50,200])_                                                 |
| **SLEEP_BETWEEN_TAP**    | Рандомная задержка между тапами в секундах _(напр. [10,25])_                                  |
| **USE_PROXY_FROM_FILE**  | Использовать-ли прокси из файла `bot/config/proxies.txt` _(True / False)_                     |

## Быстрый старт 📚
1. Чтобы установить библиотеки в Windows, запустите INSTALL.bat.
2. Для запуска бота используйте `START.bat` (или в консоли: `python main.py`).

## Предварительные условия
Прежде чем начать, убедитесь, что у вас установлено следующее:
- [Python](https://www.python.org/downloads/) версии 3.10 или 3.11.

## Получение API ключей
1. Перейдите на сайт [my.telegram.org](https://my.telegram.org) и войдите в систему, используя свой номер телефона.
2. Выберите **"API development tools"** и заполните форму для регистрации нового приложения.
3. Запишите `API_ID` и `API_HASH` в файле `.env`, предоставленные после регистрации вашего приложения.

## Установка
Вы можете скачать [**Репозиторий**](https://github.com/CatSnowdrop/TapSwap) клонированием на вашу систему и установкой необходимых зависимостей:
```shell
~ >>> git clone https://github.com/CatSnowdrop/TapSwap.git 
~ >>> cd TapSwap

# Linux
~/TapSwap >>> python3 -m venv venv
~/TapSwap >>> source venv/bin/activate
~/TapSwap >>> pip3 install -r requirements.txt
~/TapSwap >>> cp .env-example .env
~/TapSwap >>> nano .env  # Здесь вы обязательно должны указать ваши API_ID и API_HASH , остальное берется по умолчанию
~/TapSwap >>> sh install.sh
~/TapSwap >>> python3 main.py

# Windows
~/TapSwap >>> python -m venv venv
~/TapSwap >>> venv\Scripts\activate
~/TapSwap >>> pip install -r requirements.txt
~/TapSwap >>> copy .env-example .env
~/TapSwap >>> # Указываете ваши API_ID и API_HASH, остальное берется по умолчанию
~/TapSwap >>> python main.py
```

Также для быстрого запуска вы можете использовать аргументы, например:
```shell
~/TapSwap >>> python3 main.py --action (1/2/3)
# Или
~/TapSwap >>> python3 main.py -a (1/2/3)

# 1 - Создает сессию
# 2 - Запускает кликер
# 3 - Запуск через Telegram
```