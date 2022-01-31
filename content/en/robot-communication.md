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

Useful Links:

- [rwaldron github](https://github.com/rwaldron/johnny-five/wiki/Getting-Started-with-Johnny-Five-and-HC-05-Bluetooth-Serial-Port-Module)
- [pofay.github.io]([https://pofay.github.io/2018/11/08/setup-wireless-tethering-for-johnny-five-in-arduino-using-hc05-BT.html](https://pofay.github.io/2018/11/08/setup-wireless-tethering-for-johnny-five-in-arduino-using-hc05-BT.html))

Steps:

- First setup the HC-05 Wiring (see rwaldron link above) for the INITIAL configuration (NOTE this means the HC-05 RX goes to Pin 11, TX to Pin 10 - using voltage divider).
- Next download the sample code (rwaldron)
- Change the robotname in the code. Leave the baud rate as 38400
- Connect the enable (EN) pin on the HC-05 to the 3.3 V on the Arduino.
- Power up. Upload the sample code and run. You should get the correct output (see rwaldron).
- ISSUES:
    - I ended up hooking up Pin 9 to EN.
    - Disable VCC
    - Upload Sketch (above) and then press button AND power VCC
- Power Down. Remove the enable pin and re-wire the TX and RX pins as required.
- Now upload the StandardFirmataPlus example (You may need to power off HC-05 to do this)
- NOW boot up robot by plugging into power (battery).
- Go to Bluetooth Devices to pair robot with laptop (using Windows 10)
- Pin for HC-05 by default is 0000 (used in pairing)
    - I used the password 1234 for pairing with newer HC-05 modules.
- Now check the Arduino IDE ports and you should see the actual port number to use with Johnny-Five (eg. COM10).
    - Windows 10 - Needed to go to Bluetooth & Ohter Devices, then More Bluetooth Options, then COM Ports tab to see the port!

<hr/>

- Using the Aliexpress Purchased HC-05
    
    [Example HC-05](https://www.aliexpress.com/item/32786773297.html?spm=a2g0o.9042311.0.0.1cd34c4dm6O6L3](https://www.aliexpress.com/item/32786773297.html?spm=a2g0o.9042311.0.0.1cd34c4dm6O6L3))
    
- Wire up to Command Mode (Setting Board Parameters)
    
    ![commandmode.png](/images/commandmode.png)
    
- Upload the following Sketch:
    
    [Sketch](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/284b9be2-25db-4a01-8d0d-5c17d7585967/SETUPHC05.ino)
    
    - Get Above Sketch in Arduino IDE
    - Change the value for ROBOT_NAME
    - Plugin Board with USB
    - Disconnect 5V to HC-05
    - Open Serial Monitor in Arduino IDE
    - Upload the Sketch
    - WHEN you see “Starting config” in monitor, Connect 5V to HC-05 WHILE pressing the button on the HC-05 Module.
    - Check you see the following:
        
        ![goodres.png](/images/goodres.png)
        
        **NOTE: You must see the OK results as above. If they are missing, it did not work! ALSO, note that the above has ERROR for “PSWD”. IF this is an error, it means the bluetooth password (used below) will be the default (typically 1234). IF there was NO error, then the bluetooth password will be now 0000
        
- Disconnect the USB Connection to the Arduino.
    - Disconnect the HC-05 Module
    - Upload the StandardFirmataPlus Sketch to Arduino now (using USB and Arduino IDE)
    - Once complete, disconnect the Arduino USB again.
- Reconnect the HC-05 as per below:
    
    ![HC05connection.png](/images/HC05connection.png)
    
    **NOTE that in the above diagram, the BLUE wire will connect to RX (Pin 0) on Arduino. The GREEN wire will connect to TX (Pin 1) on Arduino.**
    
- Power up (this time with battery connections).
    - Go to bluetooth settings and Add new Bluetooth Device
    - Pair the new device (should appear with ROBOT_NAME set as above).
    - Now go to “More Bluetooth Options”, COM Ports Tab and check what COM port the device is listed under. THIS will be the port used in the Robot Settings for the controller.