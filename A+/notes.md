# CompTIA 220-1201 A+
### Mobile Devices
Most batteries are either lithium ion, nickel-cadmium, nickel-metal hydride, or lithium-ion polymer. ; [[Laptop Hardware - 220-1101 CompTIA A+ - 1.1#^e54143|ref]]

The keyboard is the most-used component of a laptop and is typically a single ribbon connector. ; [[Laptop Hardware - 220-1101 CompTIA A+ - 1.1#^89de2f|ref]]

[[NFC]] builds on RFID it is used when paying with your phone, tapping with a credit card, bluetooth pairing.


*The CompTIA A+ specifically lists five steps for Bluetooth connection. The first step is to enable Bluetooth, followed by enable pairing, locate the pairing device, enter the PIN, and check the connection.*
###### Definitions
1. [[SO-DIMM]] - RAM for Laptops
2. [[NFC]] - Contactless data transfer method, Often used for authentication or payment (think tap to pay on phone.)

### Networking
The Ethernet Frame is part of the Data-Link Layer (Layer 2). It consists of the Ethernet header and trailer as well as the Ethernet Payload.

Inside of the Ethernet Payload is the IP header which consists of the source and destination IPs as well as the TTL, Designation of Protocol (UDP/TCP/ICMP), Type of Service (TOS) / DSCP (QoS Flags). And the IP Payload (Layer 3, Network Layer)

Inside of the IP Payload is the Protocol Header (TCP/UDP/ICMP). In the case of TCP this consists of the Source and Destination port, the Sequence Number (Where the data starts in the stream), Acknowledgement number, and checksum for error detection, and FLOW CONTROL all to give us a reliable protocol.
In the case of UDP has the header is the source/destination ports and length of header & data thats it.

The usage of Ports in Layer 4 is what allows [[Multiplexing (mux)|Multiplexing]] and Demultiplexing.

A Switch is a "single use device"
SOHO routers are both switches, routers and WAPs all in one.
