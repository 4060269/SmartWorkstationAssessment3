Piezo Behaviour: The buzzer will output a tone when the circuit is successfully turned on, if not successful an alternate tone will play. It will check the integrated LED on the Arduino UNO to determine if the ‘boot’ is successful.

bootSuccess is a global boolean variable that stores whether the 'boot' process of the Ardiuno UNO has been completed.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setValue0(bool localbootSuccess = bootSuccess)
activate0(if localbootSuccess == TRUE)
activate1(use tone function)
activate2(use a different tone function)

terminalStart --> setValue0
setValue0 --> activate0
activate0 --> |True| activate1
activate0 --> |Else| activate2
activate1 --> terminalEnd
activate2 --> terminalEnd
```
