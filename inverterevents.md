# Inverter Events

The Inverter of the SMA Sunnyboy is accessible using Bluetooth. Other modules exist, making it possible to plug in an ethernet cable to monitor the device and extract the data.

There is Bluetooth installed on most laptops, making it possible to use the software supplied by SMA to download the data. There are also a number of sources online, which provide code/scripts to extract this data, automatically on a scheduled basis. 

Bluetooth on most laptops is not that powerful, if you have difficulty reaching the inverter despite being able to detect it, it could be worth investing in a £10-£20 USB bluetooth adapter that have antenna's fitted. These bluetooth adapters will transmit a signal in the 5dB range, where as nano usb bluetooth adapters will be transmitting bluetooth in the 2.5dB power range or less. Its highly likely, your laptop bluetooth will also be transmitting in this 2.5dB or less power range.

Having established a good connection to the inverter, download the information. 

Raw fixed width logs can be found in the https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/tree/main/data folder.

All Data files will be in Comma Separated Values (CSV) or fixed width format, both with CSV file extension.

### AllEvents Files

These 3 files are as follows

| Filename | Description |
|-- | -- |
| AllEvents_RetrievalOrder.csv | Original order showing in the SunnyBoy software |
| AllEvents_DateHoursMinsSecsSortOrder.csv | Order sorted into Date, HH, MM, SS |
| AllEvents_CoPilotCorrectedDateHoursMinsSecsSortOrder.csv | Date & Time Corrected by MS CoPilot |

The All Events were scraped from the SunnyBoy Explorer Windows Program. It became apparent, that the original installers had not set the date and time, and this was only corrected when the owner logged in for the very first time. This data time correction occurred on 16th Sept 26 at 19:56:28. So 4 new columns were added to show the corrected date and time in the CoPilotCorrected file. Its interesting to note, this correction is automatically applied by the SMA Sunnyboy software when looking at the graph showing the date 15th May 2026 in the ReadMe.md (front page) [here](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/InverterData.jpg). Obviously SMA are aware of the problems they face with some installers, and in this owner's case, the original installers went bust and disappeared, perhaps once realising a bit of work needs to be done, or it just was not as profitable as first thought. When dealing with businesses in any sector, this is sadly an all too frequent problem, so you get what you pay for, but the flip side is, consumer's dont want to pay for quality unless they can show it off to massage their ego's, hence the existence of Rolls Royce and bling in general!

These files show all the major events that the inverter has encountered. Problems with the solar panels, and the mains National Grid, and there's alot of problems with the National Grid over the 14+ years this installation has been live.


### Group Summary

The Group column will show either Grid Monitoring, Device (ie Inverter) or DC Side ie the solar panels. 

Then there will be a series of events with an ID code, think of them as a warning or error code.


| Group             | Event Count |
| ----------------- | ----------: |
| Device            |         248 |
| Grid Monitoring   |         247 |
| DC Side           |          11 |
| User Rights       |           2 |
| Device Components |           2 |


### National Grid Events

These are all the National Grid events encountered by the Solar Panel Inverter over the last 14 years.

| Event ID | Event Description | Problem | SMA Link |
| -- | -- | -- | -- | 
| 101 | Grid undervoltage (spot value) | The grid voltage or grid impedance at the connection point of the inverter is too high. The inverter has disconnected from the utility grid. | https://manuals.sma.de/SBxx-1AV-41/en-US/11010502283.html |
| 203 | Grid Undervoltage slow | The utility grid has been disconnected, the AC cable is damaged or the grid voltage at the connection point of the inverter is too low. The inverter has disconnected from the utility grid. | https://manuals.sma.de/SBxx-1AV-41/en-US/11010931083.html |
| 205 | PLL outside lmits | The utility grid has been disconnected, the AC cable is damaged or the grid voltage at the connection point of the inverter is too low. The inverter has disconnected from the utility grid. | https://manuals.sma.de/SBxx-1AV-41/en-US/11011030027.html |
| 401 | Island grid | The inverter has disconnected from the utility grid. A stand-alone grid or a very large change in the grid frequency was detected. | https://manuals.sma.de/SBxx-1AV-41/en-US/10970702091.html |
| 501 | Grid frequency disturbance | The grid frequency is not within the permissible range. The inverter has disconnected from the utility grid. | https://manuals.sma.de/SBxx-1AV-41/en-US/10970714251.html |
| 801 | Grid Failure | The inverter disconnects from the utility grid for safety reasons. As soon as the measured grid voltage is in the permissible range again, the inverter automatically switches itself on again after the grid monitoring time specified in the country standard. | https://my.sma-service.com/s/article/Event-8-or-801?language=en_US |
 

All Event ID's except 801 can be found here https://manuals.sma.de/SBxx-1AV-41/en-US/12481461387.html.


| Event                               | Count |
| ----------------------------------- | ----: |
| Grid failure (801)                  |    96 |
| PLL outside limits (205)            |    74 |
| Grid undervoltage slow (203)        |    61 |
| Grid overvoltage (spot value) (101) |    11 |
| Grid overvoltage slow (103)         |     3 |
| Grid frequency disturbance (501)    |     1 |
| Island grid (401)                   |     1 |



### DC side

These are all the events encountered from the Solar Panel side of the inverter.

| Event ID | Event Description | Problem | SMA Link |
| -- | -- | -- | -- |
| 39 | Waiting for DC start conditions | This condition typically appears at dawn and dusk when the inverter’s on-board electrical system has already been supplied with sufficient power but the PV array’s input power and voltage is not yet sufficient for feed-in into the grid. In order to commence feed-in operation, the inverter needs a minimum DC starting power and a device-specific minimum DC voltage as a critical voltage. The exact critical voltage to start the feed-in has been saved as a parameter in the inverter. As a rule of thumb, the minimum open-circuit voltage is approx. 20% above the minimum MPP voltage (see type plate). | https://my.sma-service.com/s/article/Event-39-3901-3902-or-3903?language=en_US | 
| 3401 | Overvoltage input A (SW) | Overvoltage at the DC input. This can destroy the inverter. | https://manuals.sma.de/SBSExx-50/en-US/13656924939.html |
| 3501 | Insulation Failure | The inverter has detected a ground fault in the PV module. | https://manuals.sma.de/SBxx-1AV-41/en-US/10970856075.html |


When looking at Event 39, it doesnt occur too often, only 4 times, so thats 4 days in 14 years where the conditions were not quite right. 

So what could have caused these?

| Event 39 Date Time |
| -- | 
| 21/07/26 06:26:50 |
| 21/07/26 06:26:54 |
| 20/08/26 20:02:34 |
| 20/08/26 20:02:37 |

It doesnt look like solar full or partial is affecting them...

| Solar Eclipses |
| -- | 
| 20 March 2015 |
| 10 June 2021 |
| 25 October 2022 | 
| 29 March 2025 |
| 12 August 2026 |

Is this what wild fire's can do?

https://en.wikipedia.org/wiki/2026_United_Kingdom_wildfires#England_2

Sadly because the 60day buffer that logs the granular generation data was and is not operational since the varistors have blown, and they werent logged automatically before hand, its hard to say for sure. It would have been nice to even see if solar eclipses affected the solar generation in any noticeable way, but the vast majority of owners are simply not interested in these sort of things. This makes life harder getting to the bottom of problems.


### Device

These are all the events reported by the Inverter. The vast majority are the Event ID 64, which is understandable, and also gives an idea of how often the system polls itself.


| Event ID | Event Description | Problem | SMA Link |
| -- | -- | -- | -- |
| 64 | Interference Device (64) | Event is displayed regularly or permanently: Please contact your installer for further investigation and refer to this article. Event is displayed once or only rarely and the inverter then reconnects to the grid within a few minutes: No further action required.  | https://my.sma-service.com/s/article/Inverter-Displays-Event-6401?language=en_US |
| 64 | Self Diagnosis (64) | As above | As Above |
| 10104 | Parameter "Set user password" set successfully (10104) | Parameter "…" set successfully | https://files.sma.de/downloads/NG_PAR-TB-en-22.pdf |
| 10104 | Parameter "Set installer password" set successfully (10104) | Parameter "…" set successfully | https://files.sma.de/downloads/NG_PAR-TB-en-22.pdf |
| 10108 | Time adjusted / old time (10108) | Time adjusted / old time | https://manuals.sma.de/STPxx3SE40/en-US/12173208203.html |
| 10109 | Time adjusted / new time (10109) | Time adjusted / new time | https://manuals.sma.de/STPxx3SE40/en-US/12173276171.html |
| 10010 | Restart diagnosis system (10010) | No time information could be called up from the set NTP server. | https://manuals.sma.de/STPxx3SE40/en-US/10972117643.html |
 
When shutting down these inverters, there's a couple things to test. The first is a quick shutdown, so isolate the solar panels, switching the solar panel isolator switch to 0 which represents Off, and then do the same for the property mains side.

These isolaters on both sides of the electricity input (solar and mains) will kill the power to the invertor. 

Wait 15mins for all the residual power in the inverter to dissipate. Technically it should be between 5-10mins, but 15mins is safest.
Switch it back on, Mains isolater switch first, then Solar isolator, and see if the Event ID 64 goes away. 

If it doesnt, you can try switching it off over night. Its unlikely this will resolve the matter, but it gives components time to lose all their heat, so any component failure caused by operating temperatures will show up here as metals contract when cold and expand when hot.
 
This last bit was more relevant with electronics from the 90's to the 00's when manufacturers started experimenting with the removal of lead from solder before the EU deadline on 1st July 2006. 
Lead in electronic's solder added weight to the solder joint so less had to be used. The removal of lead forced manufacturers to experiment with using different types of solder and different amounts, to ensure a good connection. Sometimes not enough of the lead-free solder was used on a joint, and when the components, boards and case got up to operating temperatures, tiny breaks occurred affecting the circuit. Today its largely not an issue.

