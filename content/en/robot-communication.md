---
title: Robot Communication
description:
position: 55
category: Robots
badge: Robots
---

<alert type="info">
    Ideally you will have wireless communication between your robots and the <a href="/robot-dashboard">Robot Dashboard computer</a>. There are many options to accomplish this, but this page describes how to setup communication using an <span class="font-bold">HC-05 Bluetooth Module</span>. An even simpler option is simply using a USB cable.
</alert>

**NOTES for setting up HC-05 Bluetooth Module:**

## Useful Links:

- [rwaldron github](https://github.com/rwaldron/johnny-five/wiki/Getting-Started-with-Johnny-Five-and-HC-05-Bluetooth-Serial-Port-Module)
- [pofay.github.io](https://pofay.github.io/2018/11/08/setup-wireless-tethering-for-johnny-five-in-arduino-using-hc05-BT.html)
- [Example Aliexpress Purchased HC-05](https://www.aliexpress.com/item/32786773297.html?spm=a2g0o.9042311.0.0.)

## Steps

### Setup the HC-05 Wiring for Command Mode.

- Example to wire up to Command Mode (Setting Board Parameters)
  ![commandmode.png](/images/commandmode.png)

### Use Sample Sketch to configure HC-05

- Next download the sample code (from rwaldron link above). [Link to Sketch here](/robotics/SETUPHC05.ino)
- Now Upload the Sketch to your board using the Arduino IDE:
  - Open Above Sketch in Arduino IDE
  - Change the value for ROBOT_NAME (first line of Sketch)
  - Leave the baud rate as 38400
  - Connect the enable (EN) pin on the HC-05 to Pin 9 on the Arduino.
  - Plugin Board with USB
  - Disconnect 5V to HC-05
  - Open Serial Monitor in Arduino IDE (Menu item 'Tools/Serial Monitor')
  - Upload the Sketch
  - WHEN you see “Starting config” in monitor, Connect 5V to HC-05.
  - Check you see the following:
    ![goodres.png](/images/goodres.png)
    \*\*NOTE: You must see the **OK** as shown in the results as above. If they are missing, it did not work! ALSO, note that the above has ERROR for “PSWD”. IF this is an error, it means the bluetooth password (used below) will be the default (typically 1234). IF there was NO error, then the bluetooth password will be now 0000
  - If you did not get the **OK** as shown, try again. I find this step can be a bit finicky and can take a few tries. Another option is try pressing the button on the HC-05 module in the config step.

## Re-wire the HC-05 for Operation

- Power Down. Remove the enable pin and re-wire the TX and RX pins as required (using voltage divider if instructions suggest it).
- Make sure to disconnect EN to Pin 9 (if used above).
- Now upload the StandardFirmataPlus example (You may need to power off HC-05 to do this).
- To upload the StandardFirmataPlus example, in the Arduino IDE go to 'File/Examples/Firmata/StandardFirmataPlus'
- Power down and reconnect the power pin to the HC-05.
- Reconnect the HC-05 as per below:
  ![HC05connection.png](/images/HC05connection.png)
  **NOTE that in the above diagram, the BLUE wire will connect to RX (Pin 0) on Arduino. The GREEN wire will connect to TX (Pin 1) on Arduino.**

## Pair Robot with Robot Dashboard Computer

- Power up (this time with battery connections).
  - Go to bluetooth settings and Add new Bluetooth Device
  - Pair the new device (should appear with ROBOT_NAME set as above).
  - Now go to “More Bluetooth Options”, COM Ports Tab and check what COM port the device is listed under. THIS will be the port used in the Robot Settings for the controller.
- Pin for HC-05 by default is 0000 (used in pairing)
  - Another password to try if 0000 doesn't work is 1234.
- Now check the Arduino IDE ports and you should see the actual port number to use with Johnny-Five (eg. COM10).
  - Windows 10 - Needed to go to Bluetooth & Ohter Devices, then More Bluetooth Options, then COM Ports tab to see the port!
