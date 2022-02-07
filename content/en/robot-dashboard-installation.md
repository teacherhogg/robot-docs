---
title: Installation
description:
position: 11
category: Robot Dashboard
badge: Robot Dashboard
---

The Robot Dashboard is open-source and can be found on [Github](https://github.com/teacherhogg/robot-controller).

Pre-built binaries are also available for easy install on Windows (tested on Windows 10) on the [releases page](https://github.com/teacherhogg/robot-controller/releases).

<alert type="warning">
The Robot Dashboard's project name is "robot-controller".
</alert>

[Robot Dashboard for Windows]()

Download the application ([See releases page on github](https://github.com/teacherhogg/robot-controller/releases)) and run the installer. Once installed, the Robot Dashboard will automatically run (actually, this will happen more than once during install where the Dashboard will appear and then disappear until eventually staying up.).

<alert type="info">
<p>On Windows 10, the default location for the application to be installed is at something like:</p>

<p>C:\Users\EXAMPLE\AppData\local\robot_dashboard\robot-controller.exe</p>

<p>(Where EXAMPLE is your Windows username.)</p>
</alert>

<alert type="warning">
On Windows 10, watch for (may be hidden by the dashboard itself) a "Windows Security Alert" asking for access through the Windows Defender Firewall. Select "Allow Access" as the dashboard does need to communicate to the Robot Server (as well as the locally installed Robots).
</alert>

You will then need to configure the application's **Setting Folder** location and setup two required configuration files (see [Robot Dashboard Setup](/robot-dashboard-setup)).
