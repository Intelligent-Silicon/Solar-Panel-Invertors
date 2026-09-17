# The Burden of Proof

As with anything that will go to court, the burden of proof is on the person making the claim. 

Sometimes the action or event is not always what it seems, and no one should ever under estimate entities better resourced than yourself. Even during peacetime, the military will always be developing new methods to destabilise entities. 

### Things to check.

### Routers

Most households will have a Router of sorts to connect to the internet, not all but most. These routers will have a system log, that captures events with a date and time stamp. This information can be exported or printed off to a report or PDF.

### Online email 

Checking the send box of online email is worth checking, you might even find out that an email has been sent around the time of the power event.

### Online Forums

If the users posts to any online forums, and its possible they may have posted at the time of the power event, these are worth checking.

### Social Media

If the users posts to any online forums, its worth checking those and trying to get to the data.


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

MS Windows is still the most popular operating system for computer's, so looking through the Event logs built into windows, can also show if anything occurred around the date.

On Windows 11, this can be done using two methods.

Press ```Windows Key``` and ```R``` at the same time to display the Run command window, and type in ```eventvwr.msc``` before clicking the OK button.

You will see a screen similar to this. You will need to expand the nodes on the left, scroll to the bottom of the middle pane, to see if the log goes back far enough and then review any information shown around the time. Some logs are set to not go above a certain size, and when the size limit is reached, will start removing old records to free up space for new records.

![Event Viewer](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/EventVwr.jpg)


Here we can see a gap between 14:40:49 and 17:33:00 indicating a possible power event, if a battery backup was not connected to a desktop.
![Event Viewer2](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/EventVwr2.jpg)

Here we can see an Event Log entry suggesting the device is starting up. Session 0 in Windows is a dedicated, isolated system session that hosts background services and critical operating system processes rather than interactive user applications.
The numerous entries all within a few seconds and minutes are typically seen when a device starts up or shuts down.
![Event Viewer3](https://github.com/Intelligent-Silicon/Solar-Panel-Invertors/blob/main/pics/EventVwr3.jpg)

It should be noted that its NOT possible to delete individual entries from a Windows log file. Deletion of records is an all or nothing approach. Microsoft designed the Windows Event Log architecture to be immutable to prevent malicious actors and tampering from covering up system changes or forensic footprints.

The information contained in the Event Log contradicts the information sent in the two text messages, about the time of the power event and the time when it came back on! 

Obviously a desktop not sat behind a Surge protector, will almost have certainly packed up considering the power surge took out the IGBT in a solar power invertor. It should be noted that an IGBT is a component which is considered a sacrificial lamb. Likewise most surge protectors built into multi-socket extension leads will not have any means to log a power event like a power surge, and will only show up a power cut in any devices which can log meta data like a computer.

Here in the UK, this also wont be considered a criminal offence, and when has the British Police ever investigated a power surge at least of an electrical kind!?! Obtusity and opaqueness is a special quality within the British State when it suits but the NHS can be so quick to label someone delusion to shutdown any conversation! And I'm always reminded that accidents happen!

Another way to collect information is to use the ```Microsoft-Windows-DeviceManagement-Enterprise-Diagnostics-Provider```. It tracks enrollment, recording when a PC joins or fails to join corporate management systems like Microsoft Intune or Microsoft Entra ID. More information can be found here: https://learn.microsoft.com/en-us/windows/client-management/mdm-collect-logs This facility allows the remote collection of activity from a PC thats located in remote locations like people working from home. 


### Software using Win32 Device Power API

You may have software installed that uses the Device Power API's (https://learn.microsoft.com/en-us/windows/win32/power/using-the-device-power-api). These API's can detect such things as the type of computer being used, ie desktop or laptop, whether the laptop lid is open or closed, whether the device has gone into a low power mode, hibernate, the new hybrid power mode, if the device is running on mains or battery with the battery percentage remaining, and if the screen saver is on or off, or display is switched on or off.

### Onus

Collecting the data from all possible sources will help show there was a problem with the power whilst also showing the device may or may not have been at fault. Obviously not all device's will collect data, but increasingly more and more are.






 