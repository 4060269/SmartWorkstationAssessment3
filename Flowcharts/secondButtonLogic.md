Second Button Behaviour: The second button will act as an on and off switch for the DC Motor; one push will turn it off, once it is pushed again it will reactivate the DC Motor.


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setbuttonPin(int buttonPin = 3)
setbuttonValue(int buttonValue = 0)
activateButton0(if buttonValue == 1)
activateButton1(digitalWrite 1 to deactivateDC)
activateButton2(digitalwrite 0 to deactivateDC)
   
terminalStart --> setbuttonPin
setbuttonPin --> setbuttonValue
setbuttonValue --> activateButton0
activateButton0 --> |True| activateButton1
activateButton0 --> |Else| activateButton2
activateButton1 --> terminalEnd
activateButton2 --> terminalEnd
```

