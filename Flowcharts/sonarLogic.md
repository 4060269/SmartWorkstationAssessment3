Sonar Behaviour: When the sonar sensor detects a human coming close to the computer, it will start the boot up process, otherwise it will keep the computer i its current state.


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setsonarValue(int sonarValue = digitalRead from the sonar)
setsonarThreshold(int threshold = 50cm)
activateSonar0(if the sonarValue is <= the threshold)
activateSonar1(digitalWrite 1 to powercomputerState)
activateSonar2(do nothing)

terminalStart --> setsonarValue
setsonarValue --> setsonarThreshold
setsonarThreshold --> activateSonar0
activateSonar0 --> |True| activateSonar1
activateSonar0 --> |False| activateSonar2
activateSonar1 --> terminalEnd
activateSonar2 --> terminalEnd
```
