# Additional Documentation for Dire Wolf Software TNC #


Most of the Dire Wolf documentation is part of the source code repository [https://github.com/wb2osz/direwolf/tree/master/doc](https://github.com/wb2osz/direwolf/tree/master/doc) 

The large number of documentation files and revisions are making the source code repository very large which means long download times.  The more general purpose documentation will be migrated here to slow down the source code repository growth.


## Application Notes ##

These dive into more detail for specialized topics or typical usage scenarios.


- [**Lora APRS - VHF APRS Bridge**](APRS-LoRa-VHF-APRS-Bridge.pdf)  [ [*download*](../../../direwolf-doc/raw/main/doc/APRS-LoRa-VHF-APRS-Bridge.pdf) ]

    LoRa is a radio technology that combines low rate data and long range with low power by using spread spectrum.  It is often used for Internet of Things and Meshtastic.    Devices are very inexpensive.  A typical board combines a LoRa radio, WiFi, Bluetooth, GPS receiver, USB port, battery charger, and OLED display.

    Recently there have been many new LoRa APRS projects gaining great popularity in Europe.  They include trackers, digipeaters, and IGates.   

    There is a large chasm between these new projects and the existing VHF APRS network. Here is a simple and very flexible approach to provide bridging between LoRa APRS and traditional APRS.   


- [**APRS Digipeaters**](APRS-Digipeaters.pdf)  [ [*download*](../../../direwolf-doc/raw/master/doc/APRS-Digipeaters.pdf) ]

    AX.25 digital repeaters (digipeaters) use a “store and forward” approach.  A packet is received, examined, then possibly modified and retransmitted.   Usually it is retransmitted on the same radio channel but it is also possible for a multi-port digipeater to link multiple radio channels.  Packets received on one channel can be retransmitted on different channels.   

    The APRS Protocol Reference 1.01 doesn’t describe how a digipeater should work.  As a result, we find many implementations that don’t behave exactly the same.   Newer implementations have found different ways to overcome weaknesses in the traditional TNCs.


- [**Successful APRS IGate Operation**](Successful-APRS-IGate-Operation.pdf)  [ [*download*](../../../direwolf-doc/raw/master/doc/Successful-APRS-IGate-Operation.pdf) ]


	Dire Wolf can serve as a gateway between the APRS radio network and APRS-IS servers on the Internet.

    This explains how it all works, proper configuration, and troubleshooting.

- [**Internal Packet Routing**](Internal-Packet-Routing.pdf)  [ [*download*](../../../direwolf-doc/raw/master/doc/Internal-Packet-Routing.pdf) ]

    Dire Wolf can support multiple audio channels which correspond to a physical audio interface, a virtual audio pipe, stdin (receive only), or a UDP port (receive only).  Each of these channels is configured to have its own modem (AFSK, GMSK, PSK) and framing type (AX.25, FX.25, IL2P, AIS, EAS SAME).

    Dire Wolf can support many concurrent client applications using serial KISS, KISS over TCP, and AGW network protocol over TCP.   The serial port connection can also be used for Bluetooth.

    Dire Wolf started out very simple, but over time, many new options were added for creative use cases.  All of the different options, are in various places in the User Guide, and can be confusing.   This is an attempt to reduce the confusion.




- [**Dire Wolf Radio Interface Guide**](Radio-Interface-Guide.pdf)  [ [*download*](../../../direwolf-doc/raw/master/doc/Radio-Interface-Guide.pdf) ]

    There is a surprising amount of confusion about interfacing Dire Wolf with radios.  Perhaps it is because the documentation is scattered in different places.  Here, I have attempted to gather it all together in one place, hopefully in an easy to use format.

    Please share what you have discovered so others can benefit from your experience.  The best way would be to open an issue in the “direwolf-doc” project (not the normal “direwolf” project) so nothing slips through the cracks.

    I’m especially interested in what you found when using soundcards and USB PTT control built into some modern rigs.




- [**SHARI and Dire Wolf**](SHARI-and-Dire-Wolf.pdf)  [ [*download*](../../../direwolf-doc/raw/master/doc/SHARI-and-Dire-Wolf.pdf) ]

    SHARI is a compact low power VHF or UHF transceiver packaged with a soundcard.  It was originally intended for an Allstar Node but can be used with many other applications.

    It has an antenna connector and two USB connectors, spaced so they can plug into a Raspberry Pi:

    *	CM119A USB audio adapter equivalent of the DINAH interface with provides transceiver audio and PTT control.

    *	USB to serial converter to configure the SA818 transceiver.


- [**APRS Weather Station with Dire Wolf**](Weather-Station.pdf)  [ [*download*](../../../direwolf-doc/raw/master/doc/Weather-Station.pdf) ]

    Many hams have home weather stations and would like to transmit weather data over APRS.

    This explains how to use Dire Wolf to transmit data from a home weather station.



## Miscellaneous ##


- [**Dire Wolf Developer Notes**](Dire-Wolf-Developer-Notes.pdf)  [ [*download*](../../../direwolf-doc/raw/master/doc/Dire-Wolf-Developer-Notes.pdf) ]

    Some might wish to add their own enhancements.  Others might want to adapt the code to run in some other environment, or just might be curious about how it works.

    This is a collection of notes intended for anyone that wants to understand how the Dire Wolf application fits together, the rationale for a few decisions, and things to look out for.   



- [**One Bad Apple Don't Spoil the Whole Bunch**](One-Bad-Apple-Dont-Spoil-the-Whole-Bunch.pdf)  [ [*download*](../../../direwolf-doc/raw/master/doc/One-Bad-Apple-Dont-Spoil-the-Whole-Bunch.pdf) ]

    Even a single bit error causes an AX.25 frame to be discarded.

    This describes an experiment which attempted to repair a small number of bit errors in a normal AX.25 frame.   


