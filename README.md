# Web3 Multisender
Distribute ether or tokens to multiple addresses.

## Установка и использование
1. Скачиваем и устанавливаем [Python 3.10.8](https://www.python.org/downloads/release/python-3108/).
	- Ставим галочку напротив "Add python.exe to PATH".
2. Запускаем `install.bat`: этот файл установит отсутствующие библиотеки в виртуальное окружение. Установка может занять несколько минут.
3. Задаем настройки скрипта.
4. Запускаем `start.bat`: этот файл запустит скрипт.

## Настройка
Настройки скрипта находятся по пути `./settings/settings.toml`:

```toml
# Отправлять токен (true) или монету сети (false)?
token_sending = true
# Адрес контракта токена:
# (Если token_sending = true)
token_contract_address = "0x0000000000000000000000000000000000000000"
# Количество токенов:
amount = 0.001
```

Адреса, на которые будут рассылаться токены, записываются в `./settings/public_keys.txt`.

Приватный ключ кошелька, с которого будут рассылаться токены, задается в переменных окружения или в `./settings/.env`:

```dotenv
PRIVATE_KEY=your_private_key
```