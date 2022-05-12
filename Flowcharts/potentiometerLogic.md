Potentiometer Behaviour: The purpose of this is to be able to quickly and granularly change the distance in which the sonar sensor triggers, if the potienmetres value is set to 1024, it will set the trigger distance to 1024 in cm.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setVariable(int potValue = analogRead)
activatePotentiometer0(if potValue => 0)
activatePotentiometer1(write potValue to potsonarDistance)

terminalStart --> setvariable
setVariable --> activatePotentiometer0
activatePotentiometer0 --> activatePotentiometer1
activatePotentiometer1 --> terminalEnd
```
