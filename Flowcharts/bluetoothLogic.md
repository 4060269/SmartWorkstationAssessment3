Bluetooth Behaviour: This acts as authentication to automate the login process, when the bluetooth module detects the users phone, tablet, laptop or even smart watch within a certain threshold, it will automatically unlock the users computer, otherwise it will stay locked.


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setSonarPins(sonarPins = 3, 4)
setThreshold(threshold = 50cm)
createSonarValue(sonarValue = 0)
currentValue(distanceRead = pin 3, 4)
activateSonar0(if distanceRead <= 50)
activateSonar1(write HIGH to sonarPins)
activateSonar2(write LOW to sonarPins)

terminalStart --> setSonarPins
setSonarPins --> setThreshold
setThreshold --> createSonarValue
createSonarValue --> currentValue
currentValue --> activateSonar0
activateSonar0 --> |True| activateSonar1
activateSonar0 --> |False| activateSonar2
activateSonar1 --> terminalEnd
activateSonar2 --> terminalEnd
```
