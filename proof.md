# The Burden of Proof

As with anything that will go to court, the burden of proof is on the person making the claim. 

Sometimes the action or event is not always what it seems (herding behaviour), and no one should ever under-estimate entities better resourced than yourself. Even during peacetime, the military will always be developing new methods to destabilise entities and learn from. At Government, National Broadcaster & Press level's, most have little to no control or protection over this mass manipulation of the population. See Electrical prices by Country for one example.

### Things to check.

### Routers

Most households will have a Router of sorts to connect to the internet, not all but most. These routers will have a system log, that captures events with a date and time stamp. This information can be exported or printed off to a report or PDF.
The level of detail contained in this router logs will vary, pretty much the same events will occur, like a wifi device connecting or disconnecting to the wifi, but the capture and logging of the event will vary between routers. Obviously this can be used to show a device was in a location or not, even if it doesnt have a password to connect to the wifi. MAC ID blocking is one example, if a wifi device tried to connect to a wifi source but didnt have the password. This is where you need to be careful of the software you download.

### Online email 

Checking the send box of online email is worth checking, you might even find out that an email has been sent around the time of the power event.

### Online Forums

If the user(s) posts to any online forums, and its possible they may have posted at the time of the power event, these are worth checking.

### Social Media

If the users post to any social media accounts, even one's not public, its worth checking those and trying to get to the data. Unfortunately at the time of writing, some social media accounts have become inaccessible, making it impossible to tell if a device was online. 


### Text Messages

Its worth checking text messages to see if there has been any mention of a power cut sent by people in the property around the time of the power event.

![Power Alert 1](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/PowerAlertTxtMsgSmall.jpg)

![Power Alert 2](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/PowerAlertTxtMsg2Small.jpg)

![Power Alert 2](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/PowerAlertTxtMsg3Small.jpg)


### Battery Backups

Whilst laptops are very common and convenient, desktops computers are still popular and many will come with a battery backup that logs information. This will also show pertinent information which could be useful.

![Battery 1](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/Battery1.jpg)

![Battery 2](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/Battery2.jpg)


### Windows Event Logs

MS Windows is still the most popular operating system for computer's, so looking through the Event logs built into Windows, can also show if anything occurred around the date and time of the power outage.

On Windows 11, this can be done using two methods.

Press ```Windows Key``` and ```R``` at the same time to display the Run command window, and type in ```eventvwr.msc``` before clicking the OK button.

You will see a screen similar to this. You will need to expand the nodes on the left, scroll to the bottom of the middle pane, to see if the log goes back far enough and then review any information shown around the power event time. Some logs are set to not go above a certain size, and when the size limit is reached, will start removing old records to free up space for new records, creating what is mainly called a circular log.

![Event Viewer](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/EventVwr.jpg)


Here we can see a gap between 14:40:49 and 17:33:00 indicating a possible power event, if a battery backup was not connected to a desktop.
![Event Viewer2](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/EventVwr2.jpg)

Here we can see an Event Log entry suggesting the device is starting up. Session 0 in Windows is a dedicated, isolated system session that hosts background services and critical operating system processes rather than interactive user applications. From a hacking perspective, a background service is ideal because it can gain the highest level of security well above user accounts using Administrator level of security, and it gains Persistence, by virtue of being a background service, out of sight out of mind.

The numerous entries all within a few seconds and minutes are typically seen when a device starts up or shuts down.
![Event Viewer3](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/EventVwr3.jpg)

It should be noted that its NOT possible to delete individual entries from a Windows log file. Deletion of records is an all or nothing approach. Microsoft designed the Windows Event Log architecture to be immutable to prevent malicious actors from tampering with to cover up system changes or forensic footprints.

The information contained in the Event Log contradicts the information sent in the two text messages, about the time of the power event and the time when it came back on! This will be seen when the Bios is set to restart the computer when power becomes available after a power outage. This Bios setting might not always be active, but when it is, you can see when the power comes back on because the event log will show entries seen during the boot process.

Likewise most surge protectors built into multi-socket extension leads will not have any means to log a power event like a power surge. 

Obviously a desktop computer not sat behind a Surge protector, will almost have certainly packed up considering the power surge took out the IGBT in a solar power inverter. It should be noted that an IGBT is a component which is considered a sacrificial lamb in Printed Circuit Board (PCB) design. This is also seen by the fact the part is not soldered into place, so it can be easily removed from the circuit board, and there are two on the PCB, one connecting to the Solar panel's to protect against lightening strikes and one that feeds electricity into the mains, to protect against power surges coming from the property or grid. An IGBT (Insulated Gate Bipolar Transistor) is a three-terminal power semiconductor device that acts as an electronic switch, combining the easy voltage-controlled input of a MOSFET with the high current and low saturation voltage capability of a bipolar junction transistor (BJT).

Here in the UK, this also wont be considered a criminal offence, and when has the British Police ever investigated a power surge at least of an electrical kind!?! Obtusity and opaqueness is a special quality within the British State when it suits but the NHS can be so quick to label someone delusional to shutdown any conversation! And I'm always reminded that accidents happen for the greater good.

Another way to collect information is to use the ```Microsoft-Windows-DeviceManagement-Enterprise-Diagnostics-Provider```. It tracks enrolment, recording when a PC joins or fails to join corporate management systems like Microsoft Intune or Microsoft Entra ID. More information can be found here: https://learn.microsoft.com/en-us/windows/client-management/mdm-collect-logs This facility allows the remote collection of activity from a PC thats located in remote locations like people working from home. 


### Software using Win32 Device Power API

You may have software installed that uses the Device Power API's (https://learn.microsoft.com/en-us/windows/win32/power/using-the-device-power-api). These API's can detect such things as the type of computer being used, ie desktop or laptop, whether the laptop lid is open or closed, whether the device has gone into a low power mode, hibernate, the new hybrid power mode, if the device is running on mains or battery with the battery percentage remaining, and if the screen saver is on or off, or display is switched on or off. Quite a lot of information can be garnered about the device by simply using this information, and when combined with [WiFi API's](https://learn.microsoft.com/en-us/windows/win32/NativeWiFi/portal) typically found on a laptop, you can start to work out the geolocation of the device, without even having to use any GPS, and in some cases have the device automatically phone home, placing it at a geolocation, despite being surrounded by password protected wifi systems, but thats beyond the remit of this repo.

### Bios Logs

Most modern computers will have a BIOS (Basic Input Output System) firmware, although now a days this is often called a UEFI bios. This BIOS may also be capable of capturing power events, but it may not be accurate because the firmware and/or hardware is simply not working properly, or a sensor is faulty.


### Alarm Systems

Some alarm systems will log power events. Since the 90's here in the UK, some alarm systems namely [BT RedCare](https://en.wikipedia.org/wiki/Redcare) have used the telephone network to send signals back to a control centre and they work in much the same way as ADSL internet connections. This signal was an ideal way to test and monitor the UK's telephone network for realtime problems, like a telephone cable coming down in the wind because of a falling tree branch, vehicles crashing into the telegraph pole, or builders breaking cables, but it also provided the means to monitor the signal quality before ADSL was rolled out years later. And if you ever had the misfortune of being targeted by BT when your ADSL connection played up and they made you swap ADSL filter's and other time-wasting actions like resetting your router or interruptions to business which is an abuse of power the British Police, Press and muppet politicians including Prime Ministers simply have no idea of at best and complicit in the coverup if they do. It makes a mockery of countless FTSE 100 companies that may be genuine companies and not simply a tool of the British Military in plausibly deniable ways.

If you think of a cable connection, like a network cable or telephone line or mains electrical cable, its capable of transmitting signals down the wire. These signals are generally contained within the cable, but the concept of multiple radio signals down a wire are just like the different Radio Frequencies (Radio Stations) we can pick up with a radio, if you think of the air as one giant all encompassing cable. When you look at the different frequencies the ADSL router can pickup, its like a radio that can pick up and process multiple radio stations all at the same time! Which makes the router CPU's kind of interesting when looked at as a [Software Defined Radio. ](https://en.wikipedia.org/wiki/Software-defined_radio)


### Onus

Collecting the data from all possible sources will help show there was a problem with the power whilst also showing the device may or may not have been at fault. Obviously not all device's will collect data, but increasingly more and more are.

You have to admit, these digital devices are an excellent way of keeping people contained for the best part of their lives, inactive which contributes to poor health, believing whatever the device says. Little Britain - Computer says no, was so prescient! Who needs a prison when you have a digital device which controls your income and ability to live as you desire...

So bearing in mind the ease at which digital information can be changed, and the difficulty in remotely removing or altering hard copies (paper print outs) of data, even though its considered environmentally damaging to use lots of paper, those pieces of paper can be ever so helpful in some situations. Its probably why many Govt entities still use pen and paper. Do they know something we dont?






 