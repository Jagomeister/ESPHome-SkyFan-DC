# ESPHome-SkyFan-DC

Reworked yaml config file to control TYUA based SkyFan DC fans.


## Supported modules

Written to support ESP8266
Example: Wemos D1 Mini

PINOUT:
|  PIN   |     FUNCTION    |
| ------ | ----------------|
| GPIO1  | UART TX         |
| GPIO3  | UART RX         |
| GPIO2  | LED             |
| A0     | NTC Thermister  |
| GPIO14 | Thermister VCC  |
| GPIO4  | TMP117 SDA      |
| GPIO5  | TMP117 SCL      |


### Fan

- Sky fan is a 5 speed fan via the remote with a 6th speed selectable via ECO mode.
- There are 2 included pakages. One acts as a 5 speed fan with mode selection (same as remote), other acts as a 6 speed fan mapping ECO in and still providing mode selection.


5 Speed (skyfan_fan5.yaml)

| Fan Speed | Skyfan DC |
| --------- | ----------|
| 0         | OFF       |
| 1         | Speed 1   |
| 2         | Speed 2   |
| 3         | Speed 3   |
| 4         | Speed 4   |
| 5         | Speed 5   |


6 Speed (skyfan_fan6.yaml)

| Fan Speed | Skyfan DC |
| --------- | ----------|
| 0         | OFF       |
| 1         | Speed 1   |
| 2         | ECO       |
| 3         | Speed 2   |
| 4         | Speed 3   |
| 5         | Speed 4   |
| 6         | Speed 5   |

### Modes

ECO, SLEEP and NORMAL

### LED

Provides basic feedback by flashing when the modules changes a datapoint. 