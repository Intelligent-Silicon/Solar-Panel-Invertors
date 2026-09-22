# Inverter Events

The Inverter of the SMA Sunnyboy is accessible using Bluetooth. Other modules exist, making it possible to plug in an ethernet cable to monitor the device and extract the data.

There is Bluetooth installed on most laptops, making it possible to use the software supplied by SMA to download the data. There are also a number of sources online, which provide code/scripts to extract this data, automatically on a scheduled basis. 

Bluetooth on most laptops is not that powerful, if you have difficulty reaching the inverter despite being able to detect it, it could be worth investing in a £10-£20 USB bluetooth adapter that have antenna's fitted. These bluetooth adapters will transmit a signal in the 5dB range, where as nano usb bluetooth adapters will be transmitting bluetooth in the 2.5dB power range or less. Its highly likely, your laptop bluetooth will also be transmitting in this 2.5dB or less power range.

Having established a good connection to the inverter, download the information. 

Raw fixed width logs can be found in the https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/tree/main/data folder.

All Data files will be in Comma Separated Values (CSV) or fixed width format, both with CSV file extension.

### AllEvents

These 3 files are as follows

| Filename | Description |
|-- | -- |
| AllEvents_RetrievalOrder.csv | Original order showing in the SunnyBoy software |
| AllEvents_DateHoursMinsSecsSortOrder.csv | Order sorted into Date, HH, MM, SS |
| AllEvents_CoPilotCorrectedDateHoursMinsSecsSortOrder.csv | Date & Time Corrected by MS CoPilot |

The All Events were scraped from the SunnyBoy Explorer Windows Program. It became apparent, that the original installers had not set the date and time, and this was only corrected when the owner logged in for the very first time. This data time correction occurred on 16th Sept 26 at 19:56:28. So 4 new columns were added to show the corrected date and time in the CoPilotCorrected file. Its interesting to note, this correction is automatically applied by the SMA Sunnyboy software when looking at the graph showing the date 15th May 2026 in the ReadMe.md (front page) [here](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/InverterData.jpg). Obviously SMA are aware of the problems they face with some installers, and in this owner's case, the original installers went bust and disappeared, perhaps once realising a bit of work needs to be done, or it just was not as profitable as first thought. When dealing with businesses in any sector, this is sadly an all too frequent problem, so you get what you pay for, but the flip side is, consumer's dont want to pay for quality unless they can show it off to massage their ego's, hence the existence of Rolls Royce and bling in general!