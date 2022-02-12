---
title: Typical Robot Challenge
description:
position: 44
category: Robot Control Apps
badge: Robot Control Apps
---

<h4 class="bg-orange-700 text-white rounded p-4">Typical Challenge Sequence</h4>

<ol>
    <li>Challenge name is given and you will need to set this in your app.</li>
    <li>ONCE Challenge is open for registration, you will need to register as a user (calls the function registerRobotUser).</li>
    <li>Challenge registration will be closed. You can not do anything.</li>
    <li>Challenge will be set to run. You can NOW send commands (call runRobotCommand after setting the variable robotCommand). Remember that one command can include multiple instructions.</li>
    <li>Depending on the challenge, you may have limits on number of simultaneous commands, length of allowed run time, etc.</li>
    <li>You and your team (if applicable) will then need to drive your robot to victory!</li>
</ol>

<h4 class="bg-orange-700 text-white rounded p-4">Robot Problems</h4>

<p>
    To be succesful at a mission, you want to move your robot as quickly as possible. However, more commands more quickly means you are 'driving blind' and may end up causing your robot to get stuck or fall off a 'cliff'. To make things worse, you may find your robot a bit unreliable. A given command may not result in the robot moving exactly the same each time. This problem is called <span class="italic">repeatability and reliability</span>. 
</p>

<p>
    The following table summarizes some of the reasons why your robot may not respond as expected. Can you think of more? Can you think of ways of changing how you control your robot so it completes a mission efficiently, but not fail due to these issues?
</p>

<table class="border-collapse w-3/4">
    <thead>
        <tr>
            <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border border-gray-300 hidden lg:table-cell">Problem</th>
            <th class="p-3 font-bold uppercase bg-gray-200 text-gray-600 border border-gray-300 hidden lg:table-cell">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr class="bg-white lg:hover:bg-gray-100 flex lg:table-row flex-row lg:flex-row flex-wrap lg:flex-no-wrap mb-10 lg:mb-0">
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 text-xs font-bold uppercase">Problem</span>
                Uneven surface
            </td>
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 text-xs font-bold uppercase">Description</span>
                The uneven surface may cause a given command to not behave completely as expected. This is particularly a problem with the sharp turn commands (TURNL, TURNR) as they are more sensitive to the amount of friction on the rover wheels.
            </td>
        </tr>
        <tr class="bg-white lg:hover:bg-gray-100 flex lg:table-row flex-row lg:flex-row flex-wrap lg:flex-no-wrap mb-10 lg:mb-0">
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 mb-4 text-xs font-bold uppercase">Problem</span>
                Robot Hardware
            </td>
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 mb-4 text-xs font-bold uppercase">Description</span>
                Your job on these missions is to develop software (app) and use that software to control your robot. Of course, a robot includes BOTH hardware and software. If you are driving the robot from home, you have no way to fix hardware issues or even the design of the robot and you must rely on the engineers whose job was robot design (or in this case - on Mr. Hogg). Note that this is exactly what happens for space missions where often an error in design or manufacturing must be cleverly handled (not fixed) through software 
            </td>
        </tr>        
        <tr class="bg-white lg:hover:bg-gray-100 flex lg:table-row flex-row lg:flex-row flex-wrap lg:flex-no-wrap mb-10 lg:mb-0">
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 mb-4 text-xs font-bold uppercase">Problem</span>
                Network Issues
            </td>
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 mb-4 text-xs font-bold uppercase">Description</span>
                Just like NASA Engineers driving real robots on Mars, you may encounter issues with network connectivity. You are ACTUALLY driving robots over the internet, so its possible a command may get lost or your network may go down. Note that while this is possible - it is definitely NOT the most likely reason for issues. Network issues happen, but generally networks are fairly reliable. Note that the various networks used to control your robot include your own internet (if working from home), the code.org servers, the robot controller server, the school network, and then bluetooth connections to the individual robots. Lots of tech means lots of ways for problems to show up!
            </td>
        </tr>
    </tbody>
</table>
