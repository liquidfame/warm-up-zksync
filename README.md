# warm-up-zksync
Скрипт свапает ETH => coin в одной из четырех сетей : zksync / arbitrum / optimism / arbitrum nova.

Настройка :

В config.py меняем значения переменных :

CHAIN = сеть с которой работаем ( ZKSYNC | NOVA | ARBITRUM | OPTIMISM )

FROM_AMOUNT = от какого кол-ва eth свапать

TO_AMOUNT = до какого кол-ва eth свапать

RM_AMOUNT = кол-во цифр после точки

SLEEP_FROM = sleep от (в секундах) между swap и следующим кошельком

SLEEP_TO = sleep до (в секундах) между swap и следующим кошельком

FROM_COIN = от какого кол-ва монет покупать (дефолт 1)

TO_COIN = до какого кол-ва покупапать (>= 1)

RM_WALLETS = True если нужно рандомизировать кошельки, False если не нужно

COINS = сюда можно добавить монеты, нужно указать address и symbol монеты, я уже добавил несколько, для обычного прогрева хватит

В файл private_keys.txt добавляем приватники от кошельков. Пустых строк быть не должно.
Запускаем файл run.py
____________________
Ошибка 'Account' object has no attribute 'privateKeyToAccount'

Решение:
1)  откатываем на старую версию библиотеку web3
pip install web3==5.31.1

