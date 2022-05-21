The program's layout: There will be two main loops that the program will loop through, the first loop, void loop(), will hold all of the functions that need to constantly be checked like the sonar function; it will mostly hold all of the input functions. After that is the void main() loop, which will mainly store the output functions as the data required for these functions are created in the input functions. 


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setValue(int lineValue = digitalRead from line sensor)
activateLine0(if lineValue == 1)
activateLine1(write 1 to bluetoothState)
activateLine2(write 0 to bluetoothState)

terminalStart --> setValue
setValue --> activateLine0
activateLine0 --> |True| activateLine1
activateLine0 --> |Else| activateLine2
activateLine1 --> terminalEnd
activateLine2 --> terminalEnd
```
