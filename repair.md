# To Repair or Not Repair

The Inverter in question is a SMA Sunny Boy SB 2500HF-30. Installed from 8th Feb 2012, switched on 17th Feb 2012, (yes, they took that long to fit everything!) so 14+ years old and its generated 38MWh of electricity, about £15K at the 43p KWh 2010 Feed-In Tariff Rate (a Govt Hook-Price to ensnare early adopters), but that 38MWh is only a mere £1100 at 2018-onward 3p KWh rates!!!

So is home solar electrical generation even worth it today? Or has the British Govt tricked people into fitting eye sores on their roof because these are not Tesla Solar Roof panels...


### Quotes 

Quotes from installers to replace the inverter can be expensive, prices can range between £3000 to £4000 (Sept 2026) to replace the inverter. Getting the model numbers in quotes can be difficult, making it harder to see whether value for money is being offered or not.

Trade prices for a single phase (domestic household electricity) (<= 3KW) Inverter will be in the range of £200-£400 + VAT (20% - [its still 20%, I remember when it was a single digit!](https://en.wikipedia.org/wiki/Value-added_tax_in_the_United_Kingdom#Historical_rates) )

It will take half a day (<= 4hrs) for 1 person to swap out an old Inverter and replace with a new inverter. I'm being generous with a 4hr time frame for unknowns, but an experienced person could swap a non-identical inverter out in 1-1.5hr, van-job-van.

Disposal of the old inverter will cost from £50 - £200 (+VAT).

| Quote | Quote Ex. Vat | Inverter Trade Price Ex. VAT | Old Disposal Inverter Ex. VAT | Consumables (Cabling, Connectors, etc) Ex. VAT | 4hrs Labour per hour Ex. VAT | 1hr Labour per hour Ex. VAT |
| -- | -- | -- | -- | -- | -- | -- |
| £3000 | £2500 | £400 | £200 | £200 | £425 | £1700 |
| £4000 | £3333 | £400 | £200 | £200 | £633 | £2533 |

Thats a lot of money, and initial outlay for electrician tools can be put at £1000+VAT, so I guess there's a fair few Porsche 911 GT3 RS's parked on driveways in some places....



### Spare Parts

The [Installation Manual of the Inverter SB 2500HF-30](https://www.inbalance-energy.co.uk/datasheets_downloads/SunnyBoy/sb2000-3000hf_installation_manual.pdf) also lists "Accessories" Page 93 which are also known as "Wearable" parts, to avoid people getting the mistaken belief this is a low risk job that involves consumables like replacing the inkjet or laser toner in a printer.

The manual also provides guidance on how to test the SMA inverter (Failure Search). Any competent person is capable of doing this if they can read and write, because the manual tells you how to safely shutdown the inverter, break it apart and start it back up so there is no guess work. You just need the right tools because nobody wants this to happen....

[![Banana in the Eye](https://img.youtube.com/vi/NaEfU47QY_k/0.jpg)](https://www.youtube.com/watch?v=NaEfU47QY_k)


Page 93 lists as the very first option the Varistors. ```MSWR-TV-7  Replacement Varistors Set of thermally monitored varistors (2pc)```. 

There will be two of these because these are cheaper equivalent of the IGBT ( Insulated-gate bipolar transistor ) which are the sacrifical lamb in PCB design, to protect the main board. 

There's two power sources, one from the solar and one from the mains. These are attack vectors to use a hacking term, so they need to ensure the power coming into be "processed" doesnt get out of hand. They are like nightclub bouncers, if the electricity coming in doesnt look good, its not coming into the party on the main board!

Now its worth mentioning that party on the main board. Electricity primarily comes into two forms, DC (Direct Current) and AC (Alternating Current). DC travels in one direction, where as AC is always shuffling backwards and forwards, making the other electrons around it shuffle backwards and forwards. Anyone who has ever consumed gram amounts of the fat soluble Zinc Acetate DiHydrate to permanently disable common cold (SARS aka Covid) viruses will be able to feel the electrical fields that leak out of unshielded cables which we witness as electrical interference. If you havent done this, but have put a 9v battery on your tongue and experienced a painful sensation will have experienced the mild directional current of DC voltage. Those who have tripped the RCD fusebox, holding onto 240V mains electrical cables (definitely not advised) to see how long the RCD main fuse box takes to trip, will know what AC feels like travelling through the body in its painful backwards and forwards wave-like motion as it heads to planet earth...



