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

These files show all the major events that the inverter has encountered. Problems with the solar panels, and the mains National Grid, and there's alot of problems with the National Grid!

The Group column will show either Grid Monitoring, Device (ie Inverter) or DC Side ie the solar panels. 

Then there will be a series of events with an ID code, think of them as a warning or error code.

### National Grid Events

| Event ID | Event Description | Problem | SMA Link |
| -- | -- | -- | -- | 
| 101 | Grid undervoltage (spot value) | The grid voltage or grid impedance at the connection point of the inverter is too high. The inverter has disconnected from the utility grid. | https://manuals.sma.de/SBxx-1AV-41/en-US/11010502283.html |
| 203 | Grid Undervoltage slow | The utility grid has been disconnected, the AC cable is damaged or the grid voltage at the connection point of the inverter is too low. The inverter has disconnected from the utility grid. | https://manuals.sma.de/SBxx-1AV-41/en-US/11010931083.html |
| 205 | PLL outside lmits | The utility grid has been disconnected, the AC cable is damaged or the grid voltage at the connection point of the inverter is too low. The inverter has disconnected from the utility grid. | https://manuals.sma.de/SBxx-1AV-41/en-US/11011030027.html |
| 401 | Island grid | The inverter has disconnected from the utility grid. A stand-alone grid or a very large change in the grid frequency was detected. | https://manuals.sma.de/SBxx-1AV-41/en-US/10970702091.html |
| 501 | Grid frequency disturbance | The grid frequency is not within the permissible range. The inverter has disconnected from the utility grid. | https://manuals.sma.de/SBxx-1AV-41/en-US/10970714251.html |
| 801 | Grid Failure | The inverter disconnects from the utility grid for safety reasons. As soon as the measured grid voltage is in the permissible range again, the inverter automatically switches itself on again after the grid monitoring time specified in the country standard. | https://my.sma-service.com/s/article/Event-8-or-801?language=en_US |
 

All Event ID's except 801 can be found here https://manuals.sma.de/SBxx-1AV-41/en-US/12481461387.html.



