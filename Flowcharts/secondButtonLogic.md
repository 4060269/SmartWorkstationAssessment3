Second Button Behaviour: The second button will act as an on and off switch for the DC Motor; one push will turn it off, once it is pushed again it will reactivate the DC Motor.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setbuttonValue(int buttonsecondState = digitalRead from the second button)
activateButton0(if buttonsecondState == 1)
activateButton1(deactivateCircuit = 1)
activateButton2(deactivateCircuit = 0)
   
terminalStart --> setbuttonValue
setbuttonValue --> activateButton0
activateButton0 --> |True| activateButton1
activateButton0 --> |Else| activateButton2
activateButton1 --> terminalEnd
activateButton2 --> terminalEnd
```
