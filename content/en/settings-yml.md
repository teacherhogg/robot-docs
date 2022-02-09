---
title: settings.yml (Settings File)
description: ""
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
testmode: true
multiteams: false
robot-server-url: https://hoggrobotchallenge.herokuapp.com
```

### group property

The last used group in a Robot Challenge.

### groups property

Available list of groups for Robot Challenges. These are added through the Robot Dashboard. You may want to have a different group for each class or club you are running.

### challengeModes property

The challengeModes is the possible list of modes available in the Dashboard. **Leave as is unless you want to restrict the possible choices.**

These modes are explained under [Challenge Modes](/challenge-modes).

### challengeName property

This is the default (or last used) challenge name.

### skipchallengename property

**Leave as is. This in an advanced feature.**

### challengeNames property

The challengeNames is the possible list of challenge names available in the Dashboard. **Leave as is. This in an advanced feature.**

### challengeMode property

This is the default (or last used) challenge mode.

### testmode property

<alert type="danger">
NOTE that by default, testmode is set to true. This is convenient for quickly getting started, but NOT GOOD in general as you will have students attempt to hijack the driving of robots when others are competing! 
</alert>

### multiteams property

**Leave as is. This in an advanced feature.**

### robot-server-url property

You can initially use the default value. However, you will need to change this if you setup your own version of the [Robot Server](/robot-server).
