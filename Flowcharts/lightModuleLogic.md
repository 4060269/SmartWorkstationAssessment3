Light Module Behaviour: This light module consists of three LEDs, one being red, orange and green. When an input has been triggered, the green light will turn on, otherwise, the light will be off. The orange light will turn on when an event has been triggered previously and no other event is currently happening, a standby LED. Finally, the red light will trigger when the circuit has been turned on and there have not been any events triggered. 

eventValue is a global boolean variable that stores if an event is running or not

orangeeventValue is another global boolean variable that stores if an event has been run in the last five seconds.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setValue0(bool localeventValue = eventValue)
setValue1(bool localorangeValue = orangeeventValue)
activate0(if localeventValue == TRUE)
activate1(write HIGH = green LED)
activate2(localorangeValue == TRUE)
activate3(write HIGH = orange LED)
activate4(localeventValue == FALSE)
activate5(write HIGH = red LED)
   
terminalStart --> setValue0
setValue0 --> setValue1
setValue1 --> activate0
activate0 --> |True| activate1
activate0 --> |Else If| activate2
activate2 --> |True| activate3
activate2 --> |Else If| activate4
activate4 --> |True| activate5
activate1 --> terminalEnd
activate3 --> terminalEnd
activate5 --> terminalEnd 
```
