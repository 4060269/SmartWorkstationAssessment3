Line Sensor Behaviour: To further automate the boot-up and login process for the end-user; if the line sensor detects someone on the seat, it will send a message to activate the Bluetooth module and set it to sniff mode; Otherwise the sensor will do nothing.


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setlineValue(int lineValue = digitalRead from line sensor)
activateLine0(if lineValue == 1)
activateLine1(write 1 to bluetoothState)
activateLine2(write 0 to bluetoothState)

terminalStart --> setlineValue
setlineValue --> activateLine0
activateLine0 --> |True| activateLine1
activateLine0 --> |Else| activateLine2
activateLine1 --> terminalEnd
activateLine2 --> terminalEnd
```
