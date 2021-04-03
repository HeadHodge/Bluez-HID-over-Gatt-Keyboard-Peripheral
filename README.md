# Bluez-HID-over-GATT-Keyboard-Emulator-Example

A working example of a BLE Keyboard Peripheral (Server) ran on my Raspberry PI4-b with Buster Raspbian-Lite for all to use. My desire is to hopefully save at least one other person the literal weeks I've spent trying to get this working for my little home automation project.

Verified working connected to my Blade Android, Windows 10 laptop, and Amazon FireTV stick devices

NOTE: Ensure you use Bluez Version 5.56 or better. This example uses Bluez features that were only experimental in prior versions.

TIPS:

Tip #1:
  The PI4 ships with a dual bluetooth chip. You must ensure you pair devices in BLE mode. To help, change this option   in the /etc/bluetooth/main.conf file:

`#Restricts all controllers to the specified transport. Default value
#is "dual", i.e. both BR/EDR and LE enabled (when supported by the HW).

#Possible values: "dual", "bredr", "le"`

`#ControllerMode = dual`
#ControllerMode = bredr
ControllerMode = le

