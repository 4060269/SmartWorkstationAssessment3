Bluetooth Behaviour: This acts as authentication to automate the login process when the Bluetooth module detects the user's phone, tablet, laptop or even smartwatch within a certain threshold, it will automatically unlock the user's computer, otherwise, it will stay locked.

blueconState is a boolean global variable that stores the bluetooth module's connection state; whether it is paired with a device or not.

```mermaid
flowchart TD
terminalStart([Start])
terminalEnd([End])
setValue(bool blueValue = digitalRead from bluetooth state pin)
activateBluetooth0(if blueValue == 1)
activateBluetooth1(write true to blueconState)
activateBluetooth2(write false to blueconState)

terminalStart --> setValue
setValue --> activateBluetooth0 
activateBluetooth0 --> |True| activateBluetooth1
activateBluetooth0 --> |Else| activateBluetooth2
activateBluetooth1 --> terminalEnd
activateBluetooth2 --> terminalEnd
```
