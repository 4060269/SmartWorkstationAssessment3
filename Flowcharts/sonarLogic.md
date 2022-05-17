Sonar Behaviour: The sonar will detect a human coming close to the computer, if there is a person within a certain threshold of the sonar range, it will start the boot-up process of the computer, otherwise, the process ends.


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setsonarValue(int sonarValue = digitalRead from the sonar)
setsonarThreshold(int threshold = 50cm)
activateSonar0(if the sonarValue is < or = to the threshold)
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
