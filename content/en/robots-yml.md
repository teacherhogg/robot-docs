---
title: robots.yml (Settings File)
description: ""
position: 14
category: Robot Dashboard
badge: Robot Dashboard
---

<alert type="info">
The robots.yml file needs to be in the Robot Dashboard settings folder (see <a href="/robot-dashboard-setup">Robot Dashboard Setup</a>).
</alert>

## Example robots.yml file

The following robots.yml file is an example defining two robots using a <a href="/motor-controllers">TB6612FNG motor controller</a> and using <a href="/robot-communication">Bluetooth</a> to communicate from the Robot Dashboard to the Robot itself.

```yaml
---
Alpha:
  # Using the TB6612FNG controller
  # NOTE that the mappings are:
  #   cdir for AIN2 or BIN2
  #   dir for AIN1 or BIN1
  metadata:
    name: Alpha Board
    color: red-700
    colortext: white
  port: COM13
  motors:
    left:
      pins:
        pwm: 5
        dir: 4
        cdir: 2
    right:
      pins:
        pwm: 6
        dir: 7
        cdir: 8
  active: true
Beta:
  # Using the TB6612FNG controller
  # NOTE that the mappings are:
  #   cdir for AIN2 or BIN2
  #   dir for AIN1 or BIN1
  metadata:
    name: Beta Board
    color: purple-700
    colortext: white
  port: COM15
  motors:
    left:
      pins:
        pwm: 5
        dir: 4
        cdir: 2
    right:
      pins:
        pwm: 6
        dir: 7
        cdir: 8
  active: true
```

## Robot IDs

A top-level property needs to be defined for every Robot you are using. In this sample, there are two such properties for the Alpha and Beta robots (can be any name with NO spaces).

### metadata properties

The metadata properties include a robot name (any name and spaces allowed) as well as defining the background color (color) and text color (colortext). The acceptable color values for these properties are the colors allowed using [Tailwind CSS](https://tailwindcss.com/docs/customizing-colors#default-color-palette).

### port property

The port is the communication port used to communicate with the robot on the computer running the [Robot Dashboard](/robot-dashboard).

See [Robot Communication](/robot-communication) for more information.

### motors properties

The motors defines the pin connections to control the left and right motors on the robot. The pins used will depend on the type of [Motor Controller](/motor-controllers) used.

## Johnny-Five Robotics & IoT Platform

Note that the Robot Dashboard uses the [Johnny-Five Robotics Platform](http://johnny-five.io/) to control the robots. This means the motor commands being used reflect the setup parameters defined for Johnny Five, and that any motor controllers and microcontrollers that Johnny-Five supports are also supported by Robot Coders.
