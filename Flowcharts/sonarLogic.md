Sonar Behaviour: When the sonar sensor detects a human coming close to the computer, it will start the boot up process, otherwise it will keep the computer i its current state.


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
settrigPin(trigPin = pin4)
setechoPin(echoPin = pin5)
setdistanceValue(int distance = 0)
setdurationValue(long duration = 0)
setthresholdValue(int threshold = 50)
sonarloop1(digitalWrite - trigPin = LOW)
sonarloop2(digitalWrite - trigPin = HiGH)
sonarloop3(duration = pulseIn - echoPin = HIGH)
sonarloop4(distance = duration * 0.034 / 2)
sonarloop5(Serial.print - distance)
sonarloop6(if distance <= threshold)
sonarloop7(
sonarloop8()

terminalStart --> setsonarPins
setsonarPins --> setsonarThreshold
setsonarThreshold --> setsonarValue
setsonarValue --> setsonarRead
setsonarRead --> activateSonar0
activateSonar0 --> |True| activateSonar1
activateSonar0 --> |False| activateSonar2
activateSonar1 --> terminalEnd
activateSonar2 --> terminalEnd
```
