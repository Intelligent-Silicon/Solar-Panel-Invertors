# War Driving

[Wardriving](https://en.wikipedia.org/wiki/Wardriving) is the practice of searching for wireless networks, usually from a moving vehicle, using a laptop or smartphone. Software for wardriving is freely available on the internet.

Warbiking, warcycling, warwalking and similar use the same approach but with other modes of transportation.

The term comes from this iconic 1983 Sci-Fi Thriller called WarGames.

[![War Games](https://img.youtube.com/vi/KXzNo0vR_dU/0.jpg)](https://www.youtube.com/watch?v=KXzNo0vR_dU)

With this in mind, and with today's Artificial Intelligence, it doesnt take much for an experienced programmer to build a phone app, thats capable of detecting the Solar Panel Inverter's bluetooth signal and have it automatically log in to extract data and/or upload malicious firmware.

Do you want this to happen to your Solar Panel installation?

So for most people they will have solar panels and inverters that are commonly available through distributors in your country.

Here in the UK one of the easiest place's to see whats available would be to check out your local Electrical Supply company.

Such examples include:
[CEF](https://www.cef.co.uk/catalogue/categories/renewables/solar/inverters)
[Solar Trade](https://www.solartradesales.co.uk/solar-pv-inverters)
[Segen](https://www.segen.co.uk/products/inverters/)
[midSummer Energy](https://midsummerwholesale.co.uk/promotions)
[Triple Solar](https://www.triplesolar.co.uk/collections/inverters)
[Alternergy](https://www.alternergy.co.uk/shop/category/solar-inverters-14)
[Rexel](https://www.rexel.co.uk/uki/root-category/Solar-PV/Inverters/c/RXPV_3)


Looking at the manuals for Growatt, Fox & SunSynk, they generally all appear to use have USB interface on the Inverter for a USB dongle with different communication technology, namely 2.4Ghz & 5Ghz Wifi, 4G mobile phone data, RF dongle and Ethernet connections, to communicate on.

The Wifi & 4G dongles eventually connect to a cloud server, and the data from the inverter can be extracted using a Smart Phone App, that also needs to connect to a cloud server, owned by the Inverter manufacturer.

The QR code on the dongle contains the Dongle's Serial number and a check code which is required to pair the dongle to the smart phone app. 

On the whole this is reasonably secure from attacker's outside of the property, whist also providing the manufacturer data to remotely monitor the performance of their own devices. This can be useful for a whole host of reasons, like monitoring the performance of different manufacturing processes, to getting a realtime idea of the cloud cover in the country its installed in, or how dusty and smokey the location is, which can also affect solar generation performance as explained here...

[![1 Year with Tesla Solar Roof](https://img.youtube.com/vi/DG8ImNJHeKI/0.jpg)](https://www.youtube.com/watch?v=DG8ImNJHeKI)

I should also mention Tesla Solar have announced they will be shortly withdrawing from the market place, so a Tesla Solar Roof is no longer a consumer option. Shame, they look so much nicer in olde world Europe and the UK, and yet strangely the planning dept's of council's, dont seem to care too much about giant slabs of solar panels being in keeping with their surroundings.... Awkward Hypocrits when thinking of the other hurdles builder's have to jump through with planning depts! Hoever it would be remiss of me to not point out, this the UK Govt's way of creating jobs for those that dont want to spend too much time thinking. Thats why there are no building regs for driveways and patios, life cant be made too complicated with too much paperwork, otherwise nothing would ever get done!


The inverters do appear to use the same ```admin``` and ```12345678``` to connect to the USB wifi dongle, which could present problems if the Solar Panel installer hasnt configured and setup the dongle with the app at the time of installation, but it does require scanning the QR code on the dongle which contains the Serial Number and Check Code, that is then used to pair with the Smart Phone App.

The risk here is, the USB dongle could become unusable, forcing the property owner to purchase another USB dongle which will set you back upwards of £10+ plus time, something very few of us have.

A couple of blog posts [here](https://www.whizzy.org/2026-06-14-growatt-shinewifi-x-esphome-modbus-bridge/) and [here](https://medium.com/@rorygallagher2010/flashing-a-growatt-shinewifi-x-replacing-cloud-firmware-with-esphome-for-local-solar-monitoring-99cacaa910f0) show the USB Dongle uses an ESP8266 wifi chip and is a dumb bridge using MODBUS. MODBUS is a communication standard typically found in Industrial Automation, and is an open request-response communication protocol created in 1979 by Modicon (now [Schneider Electric](https://www.se.com) probably more famous for the [APC Battery Backups](https://www.se.com/uk/en/product-range/61883-apc-backups/) for computers and servers) to connect industrial electronic devices. Managed today by the [Modbus Organization](https://www.modbus.org/), it lets control systems talk to sensors, meters, and actuators.

Flashing the USB WiFi dongle firmware using the ESP8266EX must always be done in person for the very first time and only then you can subsequently update the dongles firmware Over The Air (OTA), if configured to do so. 

This presents a security risk, because if some hacker somewhere in the world subsequently discovers some bugs which can be leveraged, which is often the case if we are being honest, the USB dongle cant be updated remotely unless it was already  configured in the factory to allow OTA updates. So either your solar panel installer needs to come out and update the firmware (who is picking up that cost ___IF___ it gets done), or OTA updates were configured in the factory, which then potentially creates a different attack vector, lets hope the wifi comms is at least encrypted so [Wireshark](https://www.wireshark.org/) cant sniff.

A full breakdown of Growatt Inverter codes can be found here https://github.com/pvprodk/GrowattESPHome and may also be similar if not identical to those found in Fox or SunSynk. The clue is the Printed Circuit Board (PCB) design's, where these companies dongles may simply be the same PCB's under the covers, because there's only so many ways to design a circuit board and there's only so many electrical components available en-mass globally, something we see with car brand's sharing the parts bin but adding a brand tax to the part cost.

The Growatt MODBUS tools can be found here. https://github.com/8none1/growatt_modbus

### TLDR

The Wifi might be a risk because it can spread over a distance, so you need to live on a farm to keep prying neighbours at bay!


### Older inverters

Well the [SMA Sunny Boy inverter](https://www.sma.de/en/products/hybrid-inverters) I've been given access to is some 13 years old. 

Same thing again, go through the manuals that the defaults for the monitoring software are ```user``` & ```0000``` and ```installer``` and ```1111```. 

These typically use Bluetooth, which in this situation is generally better suited because of its limited range, if you live in a terrace or semi detached, you really only have your immediate neighbours, the postie, courier or some random walking onto your property to suspect. Its not hard to keep a mobile phone in the pocket, to make things look even less suspicious. Have you had some local church member's visiting recently? Were they church member's or just someone who popped into a nearby church, nicked some leaflets and then bowled up to your front door pretending?

I think you can see how easy it is to impersonate someone, and even if they did show you a printed plastic id card on some branded lanyard, with a vaguely similar looking headshot thats worn out, would you even know if its genuine? You know the types, you see them every lunch time, walking up and down the highstreet of your local town or city, ignoring your existence as they push their way through, thrusting their chest forward because it contains a branded lanyard and worn out ID card. You know who you are! You can probably be found virtue signalling on [LinkedIn](https://www.linkedin.com/) after it got all bot-ridden and spammy, and walk the corridors of your employer because its not exactly taxing...

Anyway, Wireshark is also capable of sniffing the bluetooth out of the air using the [NordicSemi nRF52840](https://www.nordicsemi.com/Products/Development-hardware/nRF52840-Dongle) for a mere [£8](https://uk.farnell.com/nordic-semiconductor/nrf52840-dongle/bluetooth-module-v5-2mbps-1-7/dp/2902521?CMP=grhb-synd-frn-oems-buynow-invf), making it possible to listening on bluetooth communication for "debugging" purposes. Or you can simply run Wireshark on a bluetooth capable laptop and use the laptop's bluetooth to talk directly to the inverter.

Fortunately SMA make life really easy to get access, with their earlier inverter's broadcasting over bluetooth what device and serial number it was, like so ```SMA002d SN: 1234567890 SN1234567890``` so anyone in range could detect this, made obvious by the solar cells being visible on the roof, or by using Google Maps Satellite view. Do you need access to trade databases? No, just change use the [historical imagery that Google Maps provides](https://developers.google.com/maps/documentation/earth/historical-imagery), to see how far back the solar panels were installed, and you'll have a good idea of how old the invertor is and depending on area, what make and model it could even be!

With that information, you can then cold call the door step and use bluetooth to confirm your suspicions before reminding the home owner of the need to replace their out of warranty equipment for something more recent!























