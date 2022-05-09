First Button Behaviour: When the user is away or does not want the circuit to function, when the button is pressed, it will deactivate all of the whole circuit, if it is pressed again, the circuit will re-activate the circuit and let it function as normal.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setbuttonPin(ButtonPin = 6)
currentValue(fbRead = buttonPin)
activateButton0(if fbRead == 1)
activateButton1(write 1 to ButtonPin)
activateButton2(write 0 to ButtonPin)

terminalStart --> setButtonPin
setButtonPin --> currentValue
currentValue --> activateButton0
activateButton0 --> |True| activateButton1
activateButton0 --> |Else| activateButton2
activateButton1 --> terminalEnd
activateButton2 --> terminalEnd
```
