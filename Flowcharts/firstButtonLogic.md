First Button Behaviour: When the user is away or does not want the circuit to function, when the button is pressed, it will deactivate all of the whole circuit, if it is pressed again, the circuit will re-activate the circuit and let it function as normal.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setbuttonValue(int buttonfirstState = digitalRead from the first button)
activateButton0(if buttonfirstState == 1)
activateButton1(deactivateCircuit = 1)
activateButton2(deactivateCircuit = 0)
   
terminalStart --> setbuttonValue
setbuttonValue --> activateButton0
activateButton0 --> |True| activateButton1
activateButton0 --> |Else| activateButton2
activateButton1 --> terminalEnd
activateButton2 --> terminalEnd
```
