# Instant Value 20260923 11:00

Instant Values 23rd Sept 2026 from 11:00am - 11:30am

To get the min, max, (sum), (average) & number of devices data, click on the SunnyBoy Inverter node in the far left panel in the SunnyBoy Explorer software. 

This will then give you the view of the "Fleet" data, fleet being multiple device's. 

To get the data for an individual device, highlight the device in the far left panel and you will get the data for the device, minus the subnode showing min, max, (sum), (average), number of devices data.



```
Status (Solar Inverters) ! The addition of "(Solar Inverters)" indicates the "Fleet" view. The absence of "(Solar Inverters)" means an individual device has been selected or the SunnyBoy node selected.
	Operation
		Reason for derating: not active
		Grid relay status: Open
		Condition: Fault
		Waiting time until feed-in  ! Seems to cycle every 10mins
			Minimum: 7.23min 
			Maximum: 7.23min
			Average: 7.23min
			Number of Devices: 1
		
	Current Event
		Fault correction measure: ---
		Event number manufacturer
			Minimum: 6,408 ! UCE (U/CE (Collector-Emitter Voltage)) monitoring error, which relates to an internal hardware or power transistor (IGBT) fault rather than a simple external grid issue.
			Maximum: 6,408
			Number of devices: 1
			
		Current event number
			Minimum: 64
			Maximum: 64
			Number of devices: 1
			Message: Interference device
			Recommended action: Contact manufacturer
		
	Device status
		Fault
			Sum: 2,500W
			Number of Devices: 1
		OK
			Sum: 0W
			Number of devices: 0
		Warning
			Sum: 0W
			Number of devices: 0
			
		Device control
			Status: Off
			
		PV system control
			Status: Off
			
		Status (Communication products)
		Operation
			Condition: Ok
	
Device
	There is no data currently available. ! Same for Fleet view or device selected view.
	
DC Side (Solar Inverters) ! The addition of "(Solar Inverters)" indicates the "Fleet" view. The absence of "(Solar Inverters)" means an individual device has been selected.
	DC measurements ! These figures appear to be fluctuate every second when a device is selected, and polled every few minutes, possibly every 5 mins, in fleet view, so could be considered realtime. This will be more noticeable on a patchy cloudy day.
		Current [A]: 
			Minimum: 0.000A
			Maximum: 0.000A
			Sum: 0.000A
			Average: 0.000A
			Number of Devices: 1
		Voltage [A]: 
			Minimum: 405.35V 
			Maximum: 405.35V
			Average: 405.35V
			Number of Devices: 1
		Power [A]:
			Minimum: 0W
			Maximum: 0W
			Sum: 0W
			Average: 0W
			Number of Devices: 1
	Insulation monitoring
		Insulation resistance: 
			Minimum: 3,000.00kOhm
			Maximum: 3,000.00kOhm
			Average: 3,000.00kOhm
			Number of Devices: 1
		
AC Side (Solar Inverters) ! The addition of "(Solar Inverters)" indicates the "Fleet" view. The absence of "(Solar Inverters)" means an individual device has been selected.
	Grid measurements ! These figures appear to be fluctuate every second when a device is selected, and polled every few minutes, possibly every 5 mins, in fleet view, so could be considered realtime. This will be more noticeable on a patchy cloudy and/or windy day.
		Grid frequency: 49.90Hz
			Minimum: 49.90Hz
			Maximum: 49.90Hz
			Average: 49.90Hz
			Number of Devices: 1
		Reactive power: 0 var  ! Appears when an individual device is selected.
		Power: 
			Minimum: 0W
			Maximum: 0W
			Sum: 0W
			Average: 0W
			Number of Devices: 1
		Phase currents
			Phase L1: 0.000A
				Minimum: 0.000A
				Maximum: 0.000A
				Sum: 0.000A
				Average: 0.000A
				Number of Devices: 1
			Phase L2: --- ! Appears when an individual device is selected
			Phase L3: --- ! Appears when an individual device is selected
		Phase voltage
			Phase L1: 240.15V
				Minimum: 240.15V
				Maximum: 240.15V
				Average: 240.15V
				Number of Devices: 1
			Phase L2: --- ! Appears when an individual device is selected
			Phase L3: --- ! Appears when an individual device is selected
		Active Power
			Phase L1: 0W
				Minimum: 0W
				Maximum: 0W
				Sum: 0W
				Average: 0W
				Number of Devices: 1
			Phase L2: --- ! Appears when an individual device is selected
			Phase L3: --- ! Appears when an individual device is selected
		Measured values	
			Day yield: 0Wh
			Feed-in time: 56,056.05h
			Operating time: 59,466.65h
			Total yield: 38.230MWh
		
System communication (Communication products) !Only appears when using "Fleet" view or Sunny Explorer node. The absence of this section means an individual device has been selected.
	Bluetooth
		Downlink
			Connection quality: 100%
				Minimum: 100%
				Maximum: 100%
				Average: 100%
				Number of devices: 1
			NetID: FF
			Status: Connected
```			

	

	