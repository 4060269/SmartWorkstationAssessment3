The program's layout: There will be two main loops that the program will loop through, the first loop, void loop(), will hold all of the functions that need to constantly be checked like the sonar function; it will mostly hold all of the input functions. After that is the void main() loop, which will mainly store the output functions as the data required for these functions are created in the input functions. 


```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
activate0(Global variables. setting pins, general initialization)
activate1(void setup)
activate2(this will house all of the code that is needed to run once)
activate3(void loop)
activate4(this will run all of the functions in the order shown below, to make them run repeatedly)
activate5(void Sonar)
activate6(void Line sensor)
activate7(void Buttons)
activate8(void Potentiometer)
activate9(void buttons)
activate10(void Light module)
activate11(void Piezo)
activate12(void DC motor)
activate13(void Servo motor)
activate14(void SD card)
activate15(Extra code that will go after all functions, e.g SD card log event)


terminalStart --> activate0
activate0 --> activate1
activate1 --> activate2
activate2 --> activate3
activate3 --> activate4
activate4 --> activate5
activate5 --> activate6
activate6 --> activate7
activate7 --> activate8
activate8 --> activate9
activate9 --> activate10
activate10 --> activate11
activate11 --> activate12
activate12 --> activate13
activate13 --> activate14
activate14 --> activate15
activate15 --> terminalEnd
```
