# meian-dissector
Shenzhen Meian Technology / Focus safety alarm systems protocol dissector for Wireshark

Shenzhen Meian Technology products are widely known and marketed low cost safety alarm systems. 
Sold all around the world with custom OEM brand names and logos (the generic one is Focus, 
anyway I prefer to avoid other brand named cause I don't want to get in trouble with vendors). 

These alarm systems are hybrid wired/wireless (FSK 433/868MHz) systems with GSM/GPRS and TCP/IP.

There are iOS and Android clients, but firmware, protocols and apps are closed source. There are no API/webservice available 
to arm/disam, configure the alarm system and to interact with home automation.

With a bit reverse engineering and using a demo installation I wrote a python client for Meian proprietary TCP protocol.
I had nothing to do with Meian, simply I wish/need some bindings for home automation so I wrote it. 

This is the [Wireshark](https://www.wireshark.org/) dissector I used to analyze the protocol and write the client [meian-client](https://github.com/wildstray/meian-client/)

To use the dissector, get [meian.lua](https://raw.githubusercontent.com/wildstray/meian-dissector/master/meian.lua) and put it in ~/.wireshark/plugins for GNU/Linux, Mac OSX and *nix systems or
in %APPDATA%\Wireshark\plugins for M$ Windows systems.
