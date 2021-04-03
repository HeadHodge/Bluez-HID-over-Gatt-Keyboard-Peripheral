## _Bluez-HID-over-GATT-Keyboard-Emulator-Example_

A working example of a BLE Keyboard Peripheral (Server) ran on my Raspberry PI4-b with Buster Raspbian-Lite for all to use. My desire is to hopefully save at least one other person the literal weeks I've spent trying to get this working for my little home automation project.

Verified working connected to my Blade Android, Windows 10 laptop, and Amazon FireTV stick devices

#### _TIPS_

#### Tip #1:
Ensure you use Bluez Version 5.56 or better. This example uses Bluez features that were only experimental in prior versions.

#### Tip #2:
The PI4 ships with a dual bluetooth chip. You must ensure you pair devices in BLE mode. To help, change this option in the /etc/bluetooth/main.conf file:

```python
#Restricts all controllers to the specified transport. Default value
#is "dual", i.e. both BR/EDR and LE enabled (when supported by the HW).
#Possible values: "dual", "bredr", "le"
#ControllerMode = dual
#ControllerMode = bredr
ControllerMode = le
```

#### Tip #3:
Once you have this example running, use the Bluetoothctl command to make sure your bluetooth controller's 'power' option is on and that the 'advertise' option is on. This will advertise your bluetooth controller to other bluetooth client devices in order to discover and pair with your server.
