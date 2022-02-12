---
title: App Studio (Code.org)
description:
position: 43
category: Robot Control Apps
badge: Robot Control Apps
---

As mentioned in the [Robot API](/robot-api) section, the [Sample Robot Controller App](/robot-controller-sample-app) includes pre-built functions that simply sending Robot Commands to the robot.

<h4 class="bg-orange-700 text-white rounded p-4">Building (Modifying) your Robot Controller App</h4>

<p>Once a participant has completed the steps describing the [Sample Robot App](/robot-controller-sample-app), the controller app can then be modified for greater control during the challenges. For example, depending on the Challenge Mode, it may be useful to have the ability to drive the robot in a more autonomous mode.</p>

<p>Note that the <span class="font-bold">runRobotCommand</span> runs the instruction(s) you set in the variable <span class="font-bold">robotCommand</span>. The next section below describes all the possible instructions. Note that you can provide multiple instructions at once by separating the instructions with commas.</p>

<p>Example</p>

<table><tbody>
    <tr>
        <td>
            <code>
                robotCommand = "FWD-255-1000,TURNR-150-2000";
                runRobotCommand();    
            </code>
        </td>
        <td>
            <p>This example is calling the runRobotCommand with two instructions. The first instruction FWD-255-1000 says to go forward at full speed (255) for 1 seconds (1000 ms).</p>
            <p>The second instruction (separated by comma) TURNR-150-2000 says to turn right at medium speed (150) for 2 seconds (2000 ms).</p>
        </td>
    </tr>
</tbody></table>
