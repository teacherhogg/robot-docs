---
title: Robot API
description: 
position: 43
category: Robot Control Apps
badge: Robot Control Apps
multiselectOptions:
    - VuePress
    - Gridsome
    - Nuxt
---

<alert type="info">
API is a programming term that means 'Application Programming Interface'. It is the details of what commands to call (in this case) to drive the robot.
</alert>

<h2 class="bg-orange-700 text-white rounded p-4">Robot API</h2>

The Robot API allows **Robot Controller Apps** to be run from ANY coding environment that supports a third-party web call (http). Programming an App using Java, Javascript, Python, C++, and more are all possible. However, the simplest way to get started is to use [Code.org](/code-org) to develop your Robot Controller App using the [Code.org App Lab](https://code.org/educate/applab) *(Which uses Javascript and also offers a block programming environment.)*

A [Sample App](/robot-controller-sample-app) can be imported into a free Code.org account to quickly get started.

<h2 class="bg-orange-700 text-white rounded p-4">Code.org and the Sample App</h2>

If you are using the [Code.org and the Sample App](/robot-controller-sample-app), then a **Robot Command** (described below) means calling the built-in function defined in the App as **runRobotCommand** which will send the **Robot Instructions** defined in the variable **robotCommand** to the Robots.

For example, the following line in the Code.org Sample App will cause the robot to move forward full speed for 3 seconds:

```
robotCommand = "FWD-255-3000"
runRobotCommand()
```

<h2 class="bg-orange-700 text-white rounded p-4">Robot Instructions</h2>

The following table outlines the available **Robot Instructions** to be used to control the robot's motion.

<p class="italics">Note that XXX below refers to SPEED and must be between 0 (stopped) and 255 (full speed). YYY is the time for the motor to be on (in milliseconds, so 1000 is 1 seconds)</p>

<table><tbody>
    <tr><th>Motor Command</th><th>Description</th></tr>
    <tr><td>FWD-XXX-YYY</td><td>Go Foward</td></tr>
    <tr><td>BACK-XXX-YYY</td><td>Go Back</td></tr>
    <tr><td>TURNL-XXX-YYY</td><td>Turn Left</td></tr>
    <tr><td>TURNR-XXX-YYY</td><td>Turn Right</td></tr>
    <tr><td>TURNFWDL-XXX-YYY</td><td>Turn Left (While Moving Forward)</td></tr>
    <tr><td>TURNFWDR-XXX-YYY</td><td>Turn Right (While Moving Forward)</td></tr>
</tbody></table>

<h2 class="bg-orange-700 text-white rounded p-4">Robot Commands</h2>

Participants are able to send one or more **Robot Instructions** with each **Robot Command**.

Depending on the [Challenge Mode](/challenge-modes) and **Win Condition** for a given challenge, it can be very advantageous to send multiple instructions in one command. For example, some challenges may be run where the winning team is the team that completes the challenge in the least number of commands (as opposed to the first who completes the challenge).

To send multiple **Robot Instructions** in one **Robot Command**, separate each instruction with a comma.

For example, the following **Robot Command** tells the Robot to perform a 'U-turn' by sending multiple instructions (5 in this case).

```
FWD-255-1000,TURNR-150-4000,FWD-255-1000,TURNR-150-4000,FWD-255-1000
```

<h2 class="bg-orange-700 text-white rounded p-4">Robot Instruction Calibration</h2>

<alert type="warning">
These values are only examples and depend on the Robot Hardware and may need to be reviewed to determine appropriate values for the robots being used.
</alert>

<table><tbody>
    <tr><th>Example</th><th>How far robot moves</th></tr>
    <tr><td>FWD-255-1000</td><td>17 cm forward</td></tr>
    <tr><td>BACK-255-1000</td><td>17 cm backward</td></tr>
    <tr><td>TURNL-150-4000</td><td>Turns in place about 90 degrees</td></tr>
    <tr><td>TURNR-150-4000</td><td>Turns in place about 90 degrees</td></tr>
    <tr><td>TURNFWDL-200-500</td><td></td></tr>
    <tr><td>TURNFWDR-200-500</td><td></td></tr>
</tbody></table>