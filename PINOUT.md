# ピン配置（基板上面から見た番号）

| JH1 | 信号 | JH2 | 信号 |
|---:|---|---:|---|
| 1 | GND | 1 | GND |
| 2 | 3V3 | 2 | 未接続 |
| 3 | GPIO0 | 3 | 未接続 |
| 4 | GPIO1 | 4 | 未接続 |
| 5 | GPIO2 | 5 | 未接続 |
| 6 | GPIO3 | 6 | GPIO19 / USB D+相当 |
| 7 | GPIO4 / PWM | 7 | GPIO18 / USB D-相当 |
| 8 | GPIO5 | 8 | GPIO21 / UART TX |
| 9 | GPIO6 | 9 | GPIO20 / UART RX |
| 10 | GPIO7 | 10 | 3V3 |
| 11 | GPIO8 | 11 | GPIO10 |
| 12 | GND | 12 | GND |

## A105ヘッダ J4

| ピン | 信号 |
|---:|---|
| 1 | GND |
| 2 | BOOT（ESP32-C3 GPIO9） |
| 3 | EN / RESET |
| 4 | A105 TXD → ESP32 GPIO20/RX |
| 5 | A105 RXD ← ESP32 GPIO21/TX |
| 6 | A105 3.3 V |

BOOT/RESETボタンは省略しました。A105がGPIO9とENを制御するため、通常は自動書き込みできます。復旧時は必要に応じてJ4のBOOTをGNDへ落としてENをリセットします。

## LED出力 J3

- 1: LED+（DCジャックの入力電圧がそのまま出ます）
- 2: LED-（MOSFETでGND側をPWMスイッチ）

USB-C選択時はLED+へUSB 5 Vを送る構成ではありません。LED負荷はDCジャックを使ってください。
