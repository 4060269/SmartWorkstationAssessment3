DC Motor Behaviour: This motor will attach to the back of any monitor or computer case and will hold a bottle on top of it, once the user presses the button, the DC motor will bring the bottle forward and when the user presses the button again, it will put the DC motor back to its original position.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setsonarValue(int sonarValue = digitalRead from sonar pin)
setsonarThreshold(int threshold = gpotValue)
activateSonar0(if dcState is < or = to the threshold)
activateSonar1(digitalWrite true to powcomputState)
activateSonar2(do nothing)

terminalStart --> setsonarValue
setsonarValue --> setsonarThreshold
setsonarThreshold --> activateSonar0
activateSonar0 --> |True| activateSonar1
activateSonar0 --> |False| activateSonar2
activateSonar1 --> terminalEnd
activateSonar2 --> terminalEnd
```
