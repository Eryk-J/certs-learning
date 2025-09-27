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

[[SCADA]] / [[ICS]] are used to manage and control industrial machines. SCADA allows you to see real time information of these devices and control them across the network. They are very secure and typically are segmented off to prevent outside tampering/outages.

Legacy systems are often very hard to remove. They are typically really old but run extremely critical services.
Embedded systems are purpose built devices that do not have a direct access to the operating system like, an Alarm system, door security, or a time card system. You rely on the manufacturers to provide support/maintenance.

IoT devices are becoming more and more popular. Appliances, smart devices, air control, smart doorbells, thermostats, speakers, are all connecting to a network and due to the security risk that these devices bring you'll typically want to segment the network to limit any possible security issues these devices may bring.

[[IPv4]] is the main protocol for everything we do, there is also IPv6.

[[IPv4]] it consists of 4 sets of 1 byte numbers or octets (8 bits).

[[IPv6]] is larger and should last forever as it is a 128-bit address. This means that it consists of 8 sections 2 octets or 16 bits long each. 
You'll typically see your [[IPv6]] address displayed with the first 64 bits as the subnet (network address) and the last 64 bits as the host address. there are 340 undecillion possible ipv6 addresses.

An IP Subnet is the combination of an IP address and a Subnet mask.
In order for a device to communicate OUTSIDE of its local subnet it will need to know the default gateways IP address.

Subnet masks are used by the **local device** to determine what subnet it's on.
SUBNET MASKS ARE REQUIRED FOR IP ASSIGNMENT!
The default gateway is used to communicate outside of the local network.
These 3 things are the bare minimum configs for a local device.
IP address, Subnet mask, and default gateway.

DNS servers are required for name to IP translations (google.com to 142.251.211.238) these are critical so you'll typically have two different DNS servers or more incase of one being unresponsive

The original/predecessor [[DHCP]] (automatic IP address assignment daemon/protocol) was called BOOTP or the bootstrap protocol. It had some shortcomings though, it couldn't know if a device left the network and there were still some manual configs you had to do.

Thats when we invented [[DHCP]] in 1997. There are 4 steps that DHCP goes through to get you connected to the network, they are named D-O-R-A or Dora. 
D - Discover, where devices try and find a DHCP Server on the network.
O - Offer, where the DHCP server offers an IP address to the device.
R - Request, where the device chooses one of the options given and requests the IP address.
A - Acknowledge, where the DHCP server acknowledges the request and provides the device with all the IP config settings required.

DHCP IP Reservation is handled by the DHCP Server as opposed to manually setting an IP address which is done via individual devices.

[[APIPA]] is used by a device connected to a network which is having trouble communicating or receiving an IP from a DHCP server on a LAN. This Automatic Private IP Addressing or IPv4 link-local address will be able to communicate with devices on the local subnet to allow you to troubleshoot why you cant communicate with the DHCP server.

The APIPA standard uses reserved IP Addresses from 169.254.1.0 - 169.254.254.254.255. When a devices attempts to assign itself one of these IP addresses it sends an ARP broadcast over the network

Syslog protocol is a standard for consolidating system logs to a single place/location.
Usually used to put logs on the central server [[SIEM]] 

[[AAA]] is a centralized server to add security to a network. It is used to Authenticate users using login and passwords think of it as a login server.

Database servers use Data table storage. Much like a large spreadsheet it saves information in columns and rows which allows for relational database structures by linking tables together these tables are flexible and fast. This data is accessed by [[SQL]].

Mail Services typically have a  Spam Mail Server that is given spam emails based on rules from the firewall these are called "Spam Gateways."

Next-generation firewall, [[UTM]] device, or Web security gateway are all names for the same thing, an All-in-one security appliance.
This UTM can have URL filtering capabilities, Content inspection, Malware inspection, Spam filter, [[CSU.DSU|CSU/DSU]], Router/Switch interfaces, Firewall functionality, [[IDS.IPS|IDS/IPS]], [[Bandwidth shaping]], and even a [[VPN]] endpoint. (THINK PFSENSE.)

Load Balancers are devices that balance and share the load of a network. This is done to maintain the uptime of services on their network. If for example you had 8 Web Servers you wouldn't want 3 of those servers doing all of the work while 5 do none. Instead you connect all of these servers to a Load Balancer so that each of the 8 Servers service an equal amount of tasks. If one of these Servers failed the load balancer would distribute the load equally to the remaining 7 servers.

[[Proxy]] Servers receives requests from a client then the the proxy server makes a request to a service on behalf of that client, receives the response from the service and after analysis of that response sends it to the client. It is a proxy, in-between, an intermediary. 

[[DNS]] lookup commands like nslookup on windows and dig on linux/MACOS allow you to query them and give you information on data stored in dns servers. The information given can be query time, DNS server queried, IP addresses of domain entered. This information is stored in the RR (Resource Records)

###### "A" or AAAA records
in a DNS database DEFINE the IP address for a particular hostname.
A record is for [[IPv4]] addresses and AAAA records are for [[IPv6]] addresses.
	Example A record: 
	[www.jensenserver.com](notreal.com).  IN A  162.149.134.126       ;   Jensen Server
	Exmaple AAAA record:
	www.jensenserver.com IN AAAA 2001:10AC:4942:FE01:: ; Jensen Server

###### CNAME records 
or Canonical records are the aliases of one physical server hosting multiple services.
	`; Alias names ==(Canonical)==     EXAMPLES
	`==chat==    IN CNAME   mail.google.com.
	`==ftp==      IN CNAME   mail.google.com.
	`==www==  IN CNAME   mail.google.com.

###### MX records 
or Mail Exchanger records make sure you can send and receive email messages from your domain.
	`; This is the Mail-Exchanger. You can list more than one in the integer field which indicates ;priority(lower being higher priority)
	`IN MX mail.google.com
	`; This provides optional info on the machine type and OS of the server
	`IN HINFO LINUX
	
	; A list of machine names and addresses
	jack.google.com.     IN A           ; windows 10
	mail.google.com.      IN A           ; LINUX
	sam.google.com.       IN A          ; Windows 11

###### Text Records 
or TXT Records are used to store useful public information. From verification purposes to spam minimization.

`"dig google.com. txt" or "nslookup -type=txt google.com"`

are used to view text records of a given domain, in this case, google.com


[[DKIM]] Records hold the public key to mail servers which are used to verify authenticity of signed emails from those servers.

[[SPF]] protocol is a text record and is used to authorize servers to send emails on a domain. It consists of and @ (all) host name and the outgoing email server name.

[[DMARC]]. If for instance an email is received and does not have an associated SPF record and its not digitally signed with a DKIM Record then the DMARC is used to decide what to do with that email. It can be dropped if something comes from my domain and does not have an SPF and or DKIM sign or it can sent through into the SPAM of the user so that they can decide what to do with it. As well as setting up a email compliance report for all data on emails sent. (to see how many were identified as spam.)








###### Internet Connection Types

Satellite networking is high cost relative to normal/terrestrial networking.
100 Mbit/s down, 5 Mbit/s up are common
Good for remote locations with no option for normal internet connectivity connection types.
Some systems have 250 ms up, 250ms down
Starlink can get as low as 25 ms though it typically will be 25-60ms on average.
Rain fade is an issue when there is a storm or heavy rain.

Fiber Optics is one of the fastest and most efficient ways to communicate.
Compared to copper its more expensive to install and repair. Though it allows for much faster and longer travel compared to copper. Because it can transmit larger data much faster it is typically used in Large network systems where LOTS of data needs to be transmitted quickly like in the WAN core with a SONET ring or Large businesses. Nowadays Fiber is more common at homes where a fiber line is converted to a copper one outside the home.

Broadband is transmission across multiple frequencies and so you can get all different traffic types over the same wire.
This is called [[DOCSIS]], you can get Data, voice, and video all from that one wire.

[[(A)DSL]] uses telephone lines instead of cable television lines. Asymmetrical because typically download speed are much better than upload speeds. maximum distance limit of ~10000 feet from provider.

Mobile Internet Networks for transmitting data use the same towers as regular mobile networking used for voice.
Tethering is a method of unicasting to provide internet to a device using your mobile device over the cellular network.
Mobile hotspot is a method of multicasting to provide internet to multiple devices in the same way.

[[WISP]] is used if copper cabling/satellite is not available. WISP just uses an antenna to connect to to the network and that's it. WISP could use meshed 802.11 or 5g home internet or some other propriety network.
Speeds vary widely from 10 to 1000 Mbit/s.

###### Network Types
[[LAN]]s usually are local and typically communicate over ethernet or wireless connection.

[[WAN]] these networks are large and are what connect LANs over a large distance. There are many WAN technologies from Point-to-point serial, [[MPLS]] (Multiprotocol Label Switching), etc.
[[WAN]]s can be terrestrial or otherwise.

[[PAN]]s like bluetooth, IR, NFC, Car connection to phone, watch workout telemetry are all typically forms of Personal Area Networks.

[[MAN]]s are more uncommon and sit in-between LAN and WAN these are not really a thing idk

[[SAN]]s differ from NASs because they act and feel like local storage devices, they offer Block-level access and are very effecient read and write speeds. NASs on the other hand are just for file-access and sharing on a [[LAN]]. 

[[WLAN]] - Based on 802.11 links two or more devices wirelessly to created a local area network
