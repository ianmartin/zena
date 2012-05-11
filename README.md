ZENA packet capture
===================

Captures packets from a ZENA 2.4GHz 802.15.4 / ZigBee network analyser
from Microchip Technologies. Can create raw hex dump of the output or
a pcap file suitable for use with Wireshark.

Entirely based on http://code.google.com/p/microchip-zena/

Requirements
------------

Needs libusb 1.0.  On Ubuntu / Debian:

    apt-get install libusb-1.0-0-dev

Installation
------------

    ./configure
    make
    make install

To build from the git repository you will need autotools. First run:

    autoreconf -fvi

Then follow the usual configure + make steps.

Usage
-----
The ZigBee channel to sniff on must always be specified. The default is behaviour is to output in pcap format to stdout.

To log to a file:

    zena -c [channel] > log.pcap

See the [original blog post][blog] for some more (slightly out of date) details.

The major change since version 0.4.3 is the output of the TI CC24XX
FCS instead in the pcap format. This allows Wireshark to read the RSSI
and LQI indicators. This setting must be enabled in Wireshark via
Edit->Preferences->Protocol->IEEE 802.15.4, then make sure "TI CC24XX
FCS format" is checked.

[blog]: http://jdesbonnet.blogspot.co.uk/2011/02/using-microchip-zena-zigbee802154.html