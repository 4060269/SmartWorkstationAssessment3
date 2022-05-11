First Button Behaviour: The third button will act as an on and off switch for the Servo Motor. One push will turn it off and pushing it again will turn it back on. 

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setbuttonValue(int buttonthirdState = 0)
activateButton0(if buttonthirdState == 1)
activateButton1(deactivateServo = 1)
activateButton2(buttonthirdState == 0)
activateButton3(deactivateServo = 0)
   
terminalStart --> setbuttonValue
setbuttonValue --> activateButton0
activateButton0 --> |True| activateButton1
activateButton0 --> |Else If| activateButton2
activateButton1 --> terminalEnd
activateButton2 --> activateButton3
activateButton3 --> terminalEnd
