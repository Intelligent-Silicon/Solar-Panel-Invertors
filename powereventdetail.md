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

### 23rd Sept 2026 11:00

Instantaneous values collected 23d Sept 2026 from 11:00am

https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/InstantValues_20260923_1100.md

```
Current Event
		Fault correction measure: ---
		Event number manufacturer
			Minimum: 6,408 ! UCE (U/CE (Collector-Emitter Voltage)) monitoring error, which relates to an internal hardware or power transistor (IGBT) fault rather than a simple external grid issue.
			Maximum: 6,408
			Number of devices: 1
```

Insulated-gate bipolar transistors aka IGBT could have failed and not the Varistors, making this a more expensive repair, and introduces the question is it safer to get a new inverter, with another warranty? These IGBT's are located on the rearside of the invertor main board as seen in the youtube video below cued up at 3:41. Due to the small monetary amounts recovered from the Feed-In Tarrif, it may not make financial sense to get a new inverter, which leaves scrap on the roof and in the loft which will need disposal at some point. This is where the Govt has solar panel users over a barrel because this will affect the resale value of their properties.

[![Errorcode 6408](https://img.youtube.com/vi/tYEVBwqifZY/0.jpg)](https://youtu.be/tYEVBwqifZY?t=221)



### Inverter Log Corrected Date Time

The Inverter logs an event based on local time ([see link](https://www.sma-sunny.com/en/service-tip-1-setting-the-system-time/)) not UTC. 

The Inverter log time was set to British Summer Time, +1hr ahead of UTC time, because this was the time when the inverter was logged into using the SunnyBoy software on 16th Sept 2026.

The date & time for the logged events before the events generated when the SunnyBoy software logs in to the Inverter for the first time, is corrected backwards.

### Overvoltage Events

The solar panel ```Overvoltage event id 3401``` are unusual, but appear to always occur during the day, suggesting the solar panels are generating too much electricity, but unusually is the first entry at 9am on a Feb of all days!!! 

The sun can not be bright enough in the UK to generate an over voltage event at 9am on a Feb Morning.  So something else must be generating these events...

```
10th Feb  2020 09:06:17  7°C
11th July 2022 13:59:13 23°C
13th July 2022 14:39:07 24°C
15th July 2026 13:52:47 23°C
```

### Interference Device

The Inverter than registers the first of many ```interference device (64)``` entries in the log from 15th July 2026 at 20:33:11 onwards. 

A ```Self Diagnosis (64)``` event ID starts around 05:48:20 on the 16th July 2026 and one occurs everyday at sunrise + (30-60mins) there after. This will be variable depending on cloud cover and strength of the sun during different times of the year. 


| Sunrise | 16th July 2026 |
| -- | -- |
| Location | Time |
| Felixstowe | 04:55am |
| Southampton | 05:03am |
| Devonport | 05:24am |
| Self Diagnosis (64)  | 05:48am | 


### What can cause a solar panel to generate too much power? 

What are the exact parameters for the SMA Inverter to register this event, ie is there a sustained period of time at a higher voltage that needs to occur to register the event, or simply a momentary increase in voltage for a split second?

We know that the most brilliant of sunny days on the most cloudless of days or pollution free of days on the planet, should NOT generate an over voltage event with the solar panels. Solar Panels are built to handle the best sunny conditions plus a small tolerance. 

So something else must be causing these overvoltage events. 

Why does this knowledge below presented on Youtube (click the link) spring to mind???

[![Trolling](https://img.youtube.com/vi/7pSqk-XV2QM/0.jpg)](https://youtu.be/7pSqk-XV2QM)


So the general opinion of a DC Overvoltage event is the solar panels generate more DC power than the inverter can handle. Thats fine, except it shouldnt happen at 9am on a Feb morning, maybe around lunchtime on a bright sunny day at the height of summer, but not Feb coming out of winter. 

Could it also be caused by a lightening strike? Perhaps, but there werent any thunderstorms at 9am on Feb 10 2020, or on any of the other days around the time the overvoltage events were generated. 

Are there too many solar panels for the inverter to handle? No.

Can natural phenomena cause overvoltage?

In some situations. Solar Panels are engineered to perform at optimum at 25°C. For ever 1°C they get hotter, they generate about 0.5% less voltage, and for every 1°C colder than 25°C, they generate more voltage in sunshine. 

A more detailed example is explained [here](https://www.uksn.org.uk/post/how-to-protect-your-solar-power-station-from-overvoltage-in-cold-weather)

But the voltage changes are not much, perhaps a change of 10volts.

So are there any other things that could cause a solar panel to generate more power to trigger an overvoltage event?

Yes.

Fighter aircraft are strictly prohibited from using live or weaponised missile targeting systems to target civilian properties in the UK. 

Under the UK Civil Aviation Authority (CAA) regulations, the Law of Armed Conflict (LOAC), and strict Royal Air Force (RAF) peacetime operational rules, civilian structures cannot be actively targeted or used for weapons-live training.

Unfortunately not all the links on this webpage below, go anywhere, pages are missing. 
https://www.caa.co.uk/commercial-industry/airspace/event-and-obstacle-notification/airspace-restrictions/

Missing https://www.caa.co.uk/cap2038a00

There is also a specific post on Stack Exchange.
https://aviation.stackexchange.com/questions/101213/do-the-military-really-use-ga-planes-as-target-practice

```the military sometimes use GA as target practice (obviously they're not actually doing any 'firing').```

```As for the US, they do practice intercepts on GA planes and they aren't supposed to. A F-16 was involved in a hull-loss crash due to perceived loss of control during a low-speed interception, and the mishap investigation report states:```

GA = General Aviation.

Now with the new F-35's, the [EOTS](https://www.lockheedmartin.com/en-us/products/f-35-lightning-ii-eots.html) system has an infrared laser targetting system. 

https://deagel.com/Components/EOTS/a001541

```
The EOTS comprises a third generation FLIR (Forward-Looking InfraRed), a laser, and a CCD-TV (charge-coupled device) camera providing target detection and identification at greatly increased standoff ranges, high resolution imagery, automatic tracking, infrared search and track IRST, laser designation, laser rangefinder, and laser spot tracking. The EOTS F-35 sub-system functionality could be expanded in the future.
```
The Deagle website runs ASP.NET core. 

Infrared can also cause solar panels to generate more voltage. 

Solar Panels are designed to generate electricity from the Infrared band, through the visible light band on into the UV light band. Obviously UV will generate more electricity, than visible light or Infrared because its a higher energy wavelength.  

The specs of the EOTS system are hard to come by, but would it be possible for an military targetting system to cause an overvoltage event?

Whilst I would like to say FlightRadar24 could be useful, the USAF dont always use their transponders to signal their aircraft position, or only one aircraft in a group sortie may have it switched on to hide their numbers. You've all probably seen TopGun...

Could InfraRed from a weather satellite have enough power despite being in Low Earth Orbit (LEO) to trigger an over voltage event? Latest gen weather satellites, shine a laser down towards earth to measure things in the atmosphere at different depths. 

What about solar flares, or solar reflections from satellite solar panels reflecting the sun down onto solar panels on buildings?


I think the first course of action is to get the Varistors checked out, to find out if they are still functional, but also to find out if both have failed, or if one has failed, which side? Solar panel side or Mains side?











