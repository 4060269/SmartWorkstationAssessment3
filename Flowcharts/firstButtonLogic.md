First Button Behaviour: When the user is away or does not want the circuit to function, when the button is pressed, it will deactivate all of the whole circuit, if it is pressed again, the circuit will re-activate the circuit and let it function as normal.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setbuttonValue(int buttonfirstState = 0)
activateButton0(if buttonfirstState == 1)
activateButton1(deactivateDC = 1)
activateButton2(buttonfirstState == 0)
activateButton3(deactivateDC = 0)
   
terminalStart --> setbuttonValue
setbuttonValue --> activateButton0
activateButton0 --> |True| activateButton1
activateButton0 --> |Else If| activateButton2
activateButton1 --> terminalEnd
activateButton2 --> activateButton3
activateButton3 --> terminalEnd
```
