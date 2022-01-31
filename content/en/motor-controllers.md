---
title: Motor Controllers
description: 
position: 53
category: Robots
badge: Robots
---

<alert type="info">
    Note that almost ANY motor controller can be used. The Robot Dashboard uses the open-source library <a href="http://johnny-five.io/">Johnny-Five Robotics Platform</a> and any boards compatible with it can be used with Robot Coders. However, only 2 easily obtained motor controllers are discussed here.
</alert>

Two Motor Controllers described here are:

**L298N** and the **TB612FNG**.

**L298N Motor Controller**

- Wiring setup of Arduino Uno and L298N and motors.
    
    ![](/images/power_3_ZxyMAfYTPQ.png)
    
    **NOTE that the jumpers on the L298N (all 3) are installed (they come this way by default).**
    
- Arduino Ide basic TEST code (C).
    
    [Test Code](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/15e52832-b0f0-4b46-8419-ee35f5dc2437/code_without_speed_control.ino)
    
- Steps for getting working from Robot Dashboard
    Install the firmware on the Arduino (Note - this can be done on any computer). Using Arduino IDE:
            
    **Firmware**
    
    The StandardFirmataPlus firmware is the one that is used for Johnny-Five to communicate with the board. That means you have to install it first, then you can execute the nodejs programs. **Arduino IDE**
    
    - Open [Arduino IDE](http://arduino.cc/en/main/software)
    - Verify correct port and board
    - Navigate to File > Examples > Firmata > StandardFirmataPlus
    - Load sketch onto board.

**TB612FNG Motor Controller**

*In Arduino IDE, you an go Sketch → Include Library → add .ZIP Library*

[ZIP Library](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bb3bd3c9-100d-4b6f-b89e-4618e44e2483/SparkFun_TB6612FNG_Arduino_Library-master.zip)

**Sample Code**

[Sample Code](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b7a99c77-64fa-47ad-8a2c-1da1c3ff713f/MotorTestRun.ino)