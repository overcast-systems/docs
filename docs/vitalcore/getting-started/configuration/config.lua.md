---
sidebar_position: 1

title: config.lua
description: Main config file
---

This is the main configuration file of this script. In here are the most important options you need to adjust the script to your likings. We will go through each option one by one

## Config.DevMode

This is mainly used if you are actively working with the integrated API reference and need information of the script.


**Normal script operation** 
```lua
Config.DevMode = false
```
**Using Developer Mode**
```lua
Config.DevMode = true
```
<span style={{color: 'red'}}> NOTE: </span>This also unlocks custom commands, make sure to set this to ```false``` during active operation.


---
## Config.BloodAmount

This option specifies how much blood the player has on default in *ml* (milliliters)

**Recommended Values**
```
4500 - 5500
```
Values above ```5500``` or below ```4500``` would be unrealistic so we recommend to set it to a value between those above. Default value is ```5000```

### Config.BloodLevelThreshold
The following options specify different blood levels at which specific actions will take place. <br />
There are some important aspects to keep in mind. Take a look at this table:

| Config Option | Optional | Can be 0 |
|---|---|---|
| ```Config.BloodLevelThreshold_1``` | No | No |
| ```Config.BloodLevelThreshold_2``` | No | No |
| ```Config.BloodLevelThreshold_Critical``` | No | Yes |
<br />

**Config.BloodLevelThreshold_1**

This threshold defines the blood level at which the player will start to get into a state of hypovolemia: <br />
The player lost so much blood that the heart has to work at a higher rate to keep the blood flowing through the body. This also increases blood pressure and other vital signs. Read more about it **[here](/docs/vitalcore/how-it-works/)**.
```lua
Config.BloodLevelThreshold_1 = 4000
```
You can set this value to anything you like but it has to be higher than ```Config.BloodLevelThreshold_2```

<br />

**Config.BloodLevelThreshold_2**

This threshold defines the blood level at which the player will start to get into a state of bradycardia: <br />
The body of the player will start to slowly shut down. Heart rate and blood pressure go down and immediate medical attention is required. Read more about it **[here](/docs/vitalcore/how-it-works/)**.
```lua
Config.BloodLevelThreshold_2 = 2000
```

You can set this value to anything you like but it has to be higher than ```Config.BloodLevelThreshold_Critical``` and lower than ```Config.BloodLevelThreshold_1```

<br />

**Config.BloodLevelThreshold_3**

This threshold defines the blood level at which the player will start to get into a very critical state close to dying. Heart rate will be close to 0 with technically zero blood pressure. At this point the player can be considered as dying or dead. Read more about it **[here](/docs/vitalcore/how-it-works/)**.
```lua
Config.BloodLevelThreshold_2 = 500
```

You can set this value to anything you like but it has to be lower than ```Config.BloodLevelThreshold_2```

##