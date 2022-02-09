---
title: Challenge Modes
description:
position: 28
category: Robot Dashboard
badge: Robot Dashboard
---

Robot Dashboard allows for a variety of ways to challenge participants.

Three **Challenge Modes** are available:

- `sync`
- `team`
- `reject`

## **sync** Mode

In this mission condition, every command received (which generally means every command sent - unless your network is down!), the command will be put into a command queue.

Commands run synchronously which means a second command will run once the FIRST command is completed. For example, if you send a command to move forward for 2 seconds, a second command received while the robot is moving forward will be put in the queue and THEN run once the first command is complete.

Be careful, as ANY command sent my any team member WILL eventually get run! Make sure to coordinate with your team members before sending more commands!

This is a great simulation of what it might be like to drive a rover on Mars, since it is dangerous for all participants to simply send commands without seeing how the robot is responding. If team aggressively and non-cooperatively try to drive the robot, they most likely will see there robot get hopelessly stuck as the queue of commands continues to be executed.

## **team** Mode

In this mission condition, there IS also a command queue. HOWEVER, if you send a command (or command string), then any subsequent commands from YOU will be rejected until someone ELSE on your team sends a command.

It is important to coordinate the sending of robot commands so you don't end up having your commands rejected!

## **reject** Mode

In this mission condition, any command received WHILE a current command is being run will be rejected and discarded! Only when NO commands are currently running will a new command be able to run.

The number of rejected commands is recorded, so it is possible to penalize a team based on how many rejected commands were received (indicating how well the team coordinated).

<alert type="info">
    TBD WIN CONDITIONS!!!
</alert>
