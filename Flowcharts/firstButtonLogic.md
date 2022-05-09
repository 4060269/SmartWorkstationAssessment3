First Button Behaviour: When the user is away or does not want the circuit to function, when the button is pressed, it will deactivate all of the whole circuit, if it is pressed again, the circuit will re-activate the circuit and let it function as normal.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setButtonPin(ButtonPin = 6)
currentValue(distanceRead = ButtonPin)
activateButton0(if distanceRead == 1)
activateButton1(write HIGH to ButtonPin)
activateButton2(write LOW to ButtonPin)

terminalStart --> setButtonPin
setButtonPin --> currentValue
currentValue --> activateButton0
activateButton0 --> |True| activateButton1
activateButton0 --> |Else| activateButton2
activateButton1 --> terminalEnd
activateButton2 --> terminalEnd
```
