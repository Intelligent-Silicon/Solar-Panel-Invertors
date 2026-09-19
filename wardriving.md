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

I should also mention Tesla Solar have announced they will be shortly withdrawing from the market place, so a Tesla Solar Roof is no longer a consumer option. Shame, they look so much nicer in olde world Europe and the UK, and yet strangely the planning dept's of council's, dont seem to care too much about giant slabs of solar panels being in keeping with their surroundings.... Awkward Hypocrits when thinking of the other hurdles builder's have to jump through with planning depts!


The inverters do appear to use the same ```admin``` and ```12345678``` to connect to the USB wifi dongle, which could present problems if the Solar Panel installer hasnt configured and setup the dongle with the app at the time of installation, but it does require scanning the QR code on the dongle which contains the Serial Number and Check Code, that is then used to pair with the Smart Phone App.

The risk here is, the USB dongle could become unusable, forcing the property owner to purchase another USB dongle which will set you back upwards of £10+ plus time, very few of us have.

A couple of blog posts [here](https://www.whizzy.org/2026-06-14-growatt-shinewifi-x-esphome-modbus-bridge/) and [here](https://medium.com/@rorygallagher2010/flashing-a-growatt-shinewifi-x-replacing-cloud-firmware-with-esphome-for-local-solar-monitoring-99cacaa910f0) show the USB Dongle uses an ESP8266 wifi chip and is a dumb bridge using MODBUS. MODBUS is a communication standard typically found in Industrial Automation, and is an open request-response communication protocol created in 1979 by Modicon (now [Schneider Electric](https://www.se.com) probably more famous for the [APC Battery Backups](https://www.se.com/uk/en/product-range/61883-apc-backups/) for computers and servers) to connect industrial electronic devices. Managed today by the [Modbus Organization](https://www.modbus.org/), it lets control systems talk to sensors, meters, and actuators.

Flashing the USB WiFi dongle firmware using the ESP8266EX must always be done in person for the very first time and only then you can subsequently update the dongles firmware Over The Air (OTA). 

This presents a security risk, because if some hacker somewhere in the world subsequently discovers some bugs which can be leveraged, which is often the case if we are being honest, the USB dongle cant be updated remotely unless it was already  configured in the factory to allow OTA updates. So either your solar panel installer needs to come out and update the firmware (who is picking up that cost if it gets done), or OTA updates we configured in the factory.

A full breakdown of Growatt Inverter codes can be found here https://github.com/pvprodk/GrowattESPHome and may also be similar if not identical to those found in Fox or SunSynk. The clue is the Printed Circuit Board (PCB) design's, where these companies may simply be the same under the covers, because there's only so many ways to design a circuit board and there's only so many electrical components available en-mass globally. 











