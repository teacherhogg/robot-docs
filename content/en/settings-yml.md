---
title: settings.yml (Settings File)
description: ''
position: 13
category: Robot Dashboard
badge: Robot Dashboard
---

<alert type="info">
The settings.yml file needs to be in the Robot Dashboard settings folder (see <a href="/robot-dashboard-setup">Robot Dashboard Setup</a>).
</alert>

<alert type="success">
Generally, you can leave the settings.yml file with the default values. The only property that may need to be modified is the <span class="bold">robot-server-url</span> if you have setup your own <a href="/robot-server">Robot Server</a>.
</alert>

## Example settings.yml file

```yaml
---
  group: testgroup
  groups:
    - testgroup
  challengeName: testchallenge
  challengeNames:
    - testchallenge
  challengeMode: sync
  challengeModes:
    - sync
    - team
    - reject
  skipchallengename: true
  testmode: false
  multiteams: false
  robot-server-url: https://hoggrobotchallenge.herokuapp.com
```


### group property

The last used group in a Robot Challenge.

### groups property

Available list of groups for Robot Challenges. These are added through the Robot Dashboard. 

### challengeModes property

The challengeModes is the possible list of modes available in the Dashboard. **Leave as is unless you want to restrict the possible choices.**

These modes are explained under [Challenge Modes](/challenge-modes).

### challengeName property

This is the default (or last used) challenge name.

### challengeNames property

The challengeNames is the possible list of challenge names available in the Dashboard. **Leave as is. This in an advanced feature.**

### challengeMode property

This is the default (or last used) challenge mode.

### testmode property

TBD

### multiteams property

TBD