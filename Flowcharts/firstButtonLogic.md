First Button Behaviour: When the user is away or does not want the circuit to function, when the button is pressed, it will deactivate all of the whole circuit, if it is pressed again, the circuit will re-activate the circuit and let it function as normal.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setbuttonPin(int buttonPin = 3)
setbuttonValue(int buttonValue = 0)
activateButton0(if buttonValue == 1)
activateButton1(digitalWrite 1 to deactivateCircuit)
activateButton2(digitalwrite 0 to deactivateCircuit)
   
terminalStart --> setbuttonPin
setbuttonPin --> setbuttonValue
setbuttonValue --> activateButton0
activateButton0 --> |True| activateButton1
activateButton0 --> |Else| activateButton2
activateButton1 --> terminalEnd
activateButton2 --> terminalEnd
```
