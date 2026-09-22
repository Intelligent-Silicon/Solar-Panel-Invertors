# Power Event Detail


### 15th May 2026 13:52:47

Inverter logs an over voltage in the solar panels (DC side) at the corrected 13:52:47.

https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/data/AllEvents_CoPilotCorrectedDateHoursMinsSecsSortOrder.csv

```
                                                                             |-- Corrected --|
Type               Event                           Group   Date     HH MM SS Date     HH MM SS
[Incoming warning] Overvoltage input A (SW) (3401) DC Side 25/03/15  0 44 12 15/05/26 13 52 47
```


### 15th May 2026 14:58

Text message received at 14:58 

![Power Alert 1](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/PowerAlertTxtMsgSmall.jpg)


### 15th May 2026 

Power Generation appears to stop sometime from lunchtime, early afternoon onwards to today.

![Inverter Meter Reading](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/InverterData.jpg)


### 15th July 2026 20:33:11

Inverter failure from 15th July 2026 onwards.

```
                                                                                                               |-- Corrected --|
Warning                            Type                    Event                    Group   Date     HH MM SS  Date     HH MM SS
                                   [Outgoing information ] Interference device (64) Device  25/05/15  7 24 36  15/07/26 20 33 11
                                   [Incoming warning]      Self-diagnosis (64)      Device  25/05/15 16 39 45  16/07/26  5 48 20
[Fault! Please contact installer.] [Incoming error]        Interference device (64) Device  25/05/15 16 46 42  16/07/26  5 55 17
                                   [Outgoing information ] Interference device (64) Device  26/05/15  7 10  4  16/07/26 20 18 39
                                   [Incoming warning]      Self-diagnosis (64)      Device  26/05/15 16 47 52  17/07/26  5 56 27
[Fault! Please contact installer.] [Incoming error]        Interference device (64) Device  26/05/15 16 54 50  17/07/26  6  3 25
                                   [Outgoing information ] Interference device (64) Device  27/05/15  7 28 28  17/07/26 20 37  3

```



### Inverter Log Corrected Date Time

The Inverter logs an event based on local time ([see link](https://www.sma-sunny.com/en/service-tip-1-setting-the-system-time/)) not UTC. 

The Inverter log time was set to British Summer Time, +1hr ahead from UTC time, because this was the time when the inverter was logged into using the SunnyBoy software on 16th Sept 2026.

The date & time for the logged events before the events generated when the SunnyBoy software logs in to the Inverter for the first time, is corrected backwards.

### Overvoltage Events

The solar panel ```Overvoltage event id 3401``` are unusual, but appear to always occur during the day, suggesting the solar panels are generating too much electricity, but unusually is the first entry at 9am on a Feb of all days!!! 

The sun can not be bright enough in the UK to generate an over voltage event at 9am on a Feb Morning.  So something else must be generating these events...

```
10th Feb  2020 09:06:17
11th July 2022 13:59:13
13th July 2022 14:39:07
15th July 2026 13:52:47
```

### What can cause a solar panel to generate too much power? 

What are the exact parameters for the SMA Inverter to register this event, ie is there a sustained period of time at a higher voltage that needs to occur to register the event, or simply a momentary increase in voltage for a split second?

We know that the most brilliant of sunny days on the most cloudless of days or pollution free of days on the planet, should NOT generate an over voltage event with the solar panels. Solar Panels are built to handle the best sunny conditions plus a small tolerance. 

So something else must be causing these overvoltage events. 

Why does this knowledge below presented on Youtube (click the link) spring to mind???

[![Trolling](https://img.youtube.com/vi/7pSqk-XV2QM/0.jpg)](https://youtu.be/7pSqk-XV2QM)


### Interference Device

The Inverter than registers the first of many ```interference device (64)``` entries in the log from 15th July 2026 at 20:33:11 onwards. 

A self diagnosis starts around 05:48:20 on the 16th July 2026 and one occurs everyday at sunrise there after. This self diagnosis event occurs 30-60mins after sunrise.

| Location | Time |
| Felixstowe | 04:55am |
| Southampton | 05:03am |
| Devonport | 05:24am |



