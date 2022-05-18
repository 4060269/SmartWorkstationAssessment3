Sonar Behaviour: The sonar will detect a human coming close to the computer, if there is a person within a certain threshold of the sonar range, it will start the boot-up process of the computer, otherwise, the process ends.

gpotValue is a global variable that holds the potientiometres value it is currently set; see in the potientiometre flowchart.

powcomputState is another global variable that is a boolean and it stands for power computer state; this would be used for turning the computer.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setsonarValue(int sonarValue = digitalRead from sonar pin)
setsonarThreshold(int threshold = gpotValue)
activateSonar0(if the sonarValue is < or = to the threshold)
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
