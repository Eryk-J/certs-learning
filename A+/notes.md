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

A Router is a device that forwards traffic between different IP subnets, the router uses the IP Address that's within the packet to determine what the next hop might be.
Since this happens on Layer 3 these devices are called Layer 3 devices.
If you have a router that can be configured inside of a switch those are referred to as layer 3 switches.

Most routers can connect different types of networks together like LAN, WAN, copper, and fiber connections all into one device.

If you are using a copper wire/connection you are likely connecting to a Switch.

A router commonly routes traffic based on the destination IP Address that's in a packet. 
A switch determines where traffic is to be forwarded based on the destination MAC Address inside of that frame.

The switch can also traffic data at a very fast speed because a lot of the forwarding decisions are based in the hardware itself. ASIC, which allows for very fast through put.

At the core of an enterprise network there may be a switch with tens or even hundreds of interfaces.
Many of these switches add additional power to the switch using PoE (Power over Ethernet) Ethernet copper cabling.

Switches that do both MAC routing and IP routing are called layer 3 or multi layer switches.

Unmanaged switches give very few configuration options.
This would include no options for VLAN all devices connected would all essentially be on **ONE** VLAN.

SNMP is typically used to query devices on the network for performance or error checking, however, unmanaged switches don't have SNMP capabilities and therefore are could not be polled or queried for these checks.

Managed switches allows you to configure different interfaces to be on completely different IP subnets or what is called VLAN's.


These switches also typically allow you to set priority to different types of traffic.
Many of these networks in an enterprise setting will have many switches and one way to prevent loops between all of those switches is to use the [[STP]].
Port mirroring is something that is also typically available in a managed switch, this allows you to set all traffic on a specific port to another port on a switch so that you can plug in a protocol analyzer to view all of those packets traversing on a specific port.

An Access point provides wireless connectivety for a LAN.
Typically all these WAPs do is provide a connection to the wired network via a wireless network.
These are bridges because its bridging or extending the wired connection into a wireless one.
It makes forwarding decisions based on MAC address (layer2)

In an office building you typically have something like a wiring closet where all desks will have a wire coming into it.
This will typically all go into a patch panel (permanent run) and a 110 block from there there will be rj45 connectors which then can all be individually plugged into a switch.
This makes sure that if any change is required all you have to do is move the cables on the front of the patch panel (rj45) which limits the ***SCOPE*** of any problems that may occur.

Firewalls disallow traffic based on IP addresses and port numbers which means its a Layer 4 device (Transportation). Some newer firewalls are able to filter based on application layer traffic which would make them Layer 7 devices. Some firewalls allow for traffic to be encrypted between two sites by creating an encrypted tunnel. Some can also act as a proxy so if someone is browsing a website on the internet the firewall will stop that communication it will preform the browsing, it will receive the response from that device and then check it for anything malicious and then forward the results of that query to the user. And most firewalls can also act as layer 3 routers.

Power over Ethernet that comes from the switch are called Endspans, if you need something in between the switch and a device you would use an In-line power injector and these are called Midspans.

Hubs are bad. Sometimes called "multi-port repeater" Repeater because any traffic on one port is repeated to all other ports on the hub. These devices are also all "Half-duplex" think a walkie talkie that can't receive data while its being transmitted on. Maximum of 10/100 megabit speed.

Cable modems use Broadband meaning they transmit over a variety of frequencies and different traffic types.
These modems are [[DOCSIS]], can have a speed of 1GB/s or more and offer multiple services - Data, voice, video (TV).


[[(A)DSL]] uses telephone lines instead of cable television lines. Asymmetrical because typically download speed are much better than upload speeds. maximum distance limit of ~10000 feet from provider.

Fiber networks use [[ONTs]] these boxes convert the ISPs fiber network into copperwire Ethernet that can be used in the home. These ONT is usually outsides which delineates the ISPs Network from your Network. This is called the Demarcation point or the demarc.
THE DEMARC IS IMPORTANT so that you know where the responsibilities are split on one side is the ISP and the other is your network.

[[NICs]] are what you plug a copper ethernet cable into, computers, servers, printers, routers, switches, phones, tablets, cameras will all have a Network interface card.


In the cloud SDN's take switches, routers, firewalls and change them into software. for example you take every little piece that makes up a switch and create software versions that are used in the cloud.

there are typically three layers in [[SDN]]s, Layer 1 is called the Infrastructure layer/data plane. Things in this layer include, processing the network frames and packets, forwarding, trunking, encrypting, [[NAT]] or anything happening at the PACKET level.

When our routers and switches need to forward traffic in the data plane they need some reference to know where the traffic will be going. Most of these references will be located in the Control Layer/Plane of that device.

NAT tables in a router, a forwarding table, session table basically any routing information it will be in the Control Layer

The Application layer of a networking device is the Management plane. It is where I or some process actually manages/interfaces with the device. Need to actually login or access the device, either via [[API]], SSH or some other GUI you are managing that device from the Application Layer/Management Plane.

802.11a operates at 5ghz and at 54megabits per second.
5ghz signals travel much less distance than 2.4 gigahertz signals due to the absorption vs bouncing
802.11b operates at 2.4ghz and a max speed of 11 megabits per second.

in 2003 .11b got its first upgrade to 802.11g which also operates at 2.4ghz and 54 megabits per second.


Wireless networks are the not the only networks that use 2.4 and 5ghz frequencies, baby monitors, wireless phones, microwave ovens, Bluetooth all can use 2.4ghz so in areas with these you could see interference/conflict.

Instead of memorizing letters we now use numbers to differentiate between Wi-Fi standards.

Wi-Fi 4 (802.11n) is a straight upgrade of 11a, 11b & 11g offering both 5ghz and 2.4ghz with 40Mhz channel widths a maximum throughput of 600 Megabits per second (Mbit/s) with 4 antennas, 150 each.
Wifi-4 uses [[MIMO]] which allows transmit of information simultaneously between the end station and the access point. released in october 2009. 

Wi-Fi 5 (802.11ac) an upgrade of Wi-Fi 4 it only operates at 5ghz range. Up to 160 Mhz channel [[bandwidth]] and increased channel bonding ([[Multiplexing (mux)]]). Denser signaling modulation so faster data transfer. WiFi 5 introduces MU-[[MIMO]] (multi-user). WiFi 5 can get nearly 7gbp/s. 
 released in january 2014

WiFi 6 (802.11ax) this operates at both 2.4 and 5ghz and 20, 40, 80, and 160 megahertz and some access points allow simultaneous connection on both frequencies. 
All in all with Wi-Fi 6 you can get 1.2 gigabits per second per channel and 9.6 total. Wi-Fi 6 solves many of the issues we see at scale/with large numbers of people.
Wi-Fi 6 does this by using [[OFDMA]].

Standard access points will have ~40-50m range. To send signals between neighboring building for example you would use antennas pointed from one building at another set of antennas on the other building.

There are some rules and laws that you have to follow when working with wireless connections where, when and how much/strong it can be. You'll need outdoor antenna aswell if you are connecting two buildings. which comes with its own laws and regulations also need to keep an eye out for lightning strikes and other environmental hazards.

[[RFID]] is used in access badges, it will also be used for chipping your dog. They can be very small, as small as a grain of rice. Most RFID tags don't have batteries instead they "listen" for radio signals being emitted and then harness that power and send a signal back.
Others do have batteries or are self powering these are called Powered RFID.

[[NFC]] builds on RFID it is used when paying with your phone, tapping with a credit card, bluetooth pairing.

A [[DNS]] (Domain Name System) is a Distributed naming system meaning there may be many different DNS servers in an environment and outside the network there might be many other DNS server conversions as well.

A File server is a centralized storage of documents, spreadsheets, videos, pictures, and any other files. Since these files are stored on the network you can log in from anywhere on the network and access these files. These servers use the [[SMB]] protocol on Windows and [[AFP]] on MacOS.

Print Servers provide printing services for all network devices. Technically this "print server" could be a software that is running on a computer that is connected to a printer, everyone would send their print jobs to this computer so that it could handle it all. Some printers come with a hardware card that have a ethernet interface to be able connect directly to the network via cable. These print servers would typically use SMB on windows or [[IPP]], or [[LPD]].

Mail server is for sending and receiving mail. This is one of the most mission critical servers since its used by everyone and even a slight downtime can cause massive failures. For that reason it is typical to use a cloud service that is 24/7 with 24/7 support.


Web servers use http/https protocols and are built with HTML/HTML5. Web pages are stored on the server and are then downloaded to the browser. This can be static pages or dynamically built (in real time).

Load balancers are used to balance the load to multiple servers to make sure that not single server is overwhelmed and shutsdown/crashes that way you prioritize overall uptime. It uses Fault tolerance so that if one server becomes unresponsive it can balance the load to other servers on the network so there is no downtime.
These Load balancers sit between the internet and all of your servers so it can manage many things. For example, TCP offloading so that a constant connection can be maintained between the load balancer and the servers whilst still using that protocol. SSL offloading as well so that the balancer handles the encryption/decryption instead of the server. (you can imagine an ASIC for encrypt/decrypt.)
They can also act as Caching devices in order to respond to requests without having to contact the servers.
It can use QoS aswell as content switching capabilities for sending certain traffic to specific servers to maximize performance.

Proxy servers sit in the middle of a conversation. Users make a request to a proxy server and then the proxy will communicate with a 3rd party service and get the required information. It will then scan the information and if its OK'd it will then send that information to the User. In so doing proxies can have many great security features like, Access Control, caching, URL filtering, content scanning, and many other security features.
