Line Sensor Behaviour: When the line sensor detects someone on the seat, it will trigger the events that authenticate that it is the correct user is on the seat, like a bluetooth connection, otherwise all of the sensors besides the sonar will stay deactivated.


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setLinePin(int linePin = 5)
currentValue(digitalRead = lineValue)
activateLine0(if lineValue == 1)
activateLine1(write HIGH to bluetoothState)
activateLine2(write LOW to bluetoothState && deactivatemostCircuit)

terminalStart --> setLinePin
setLinePin --> currentValue
currentValue --> activateLine0
activateLine0 --> |True| activateLine1
activateLine0 --> |Else| activateLine2
activateLine1 --> terminalEnd
activateLine2 --> terminalEnd
```
