# [Introductory Networking](https://tryhackme.com/room/introtonetworking)

### Room created by  [MuirlandOracle](https://tryhackme.com/p/MuirlandOracle)


## Task 2 - The OSI Model: An Overview

>Q: - "Which layer would choose to send data over TCP or UDP?"

A: - **Transport Layer(#4)** is used, it chooses which protocol to use TCP or UDP and both have their advantages.

>Q: - "Which layer checks received packets to make sure that they haven't been corrupted?"

A: -  **Data Link Layer(#2)** is used , outside of adding the MAC, it also checks if the data has been corrupted.(Communication Theory or Coding Theory, can teach you how such data is fixed if corrupted)

>Q: - "In which layer would data be formatted in preparation for transmission?"

A: - **Data Link Layer(#2)** is used, it adds the physical MAC and then sends it across the network.

>Q: - "Which layer transmits and receives data?"

A: - **Physical Layer(#1)** is used, its the raw hardware in the computer, the impulses that it receives are what is being transfered.

>Q: - "In which layer would data be formatted in preparation for transmission?"

A: - **Data Link Layer(#2)** is used, it adds the physical MAC and then sends it across the network.

>Q: - "Which layer encrypts, compresses, or otherwise transforms the initial data to give it a standardised format?"

A: - **Presentation Layer(#6)** is used, the information it receives is in a format that an application can read, but since eventually this will reach the hardware and other layers, it has to be standadised.

>Q: - "Which layer tracks communications between the host and receiving computers?"

A: - **Session Layer(#5)** is used, it  tries to establish a sucessfull session between computers and responds if successfull or not.

>Q: - "Which layer accepts communication requests from applications?"

A: - **Application Layer(#7)** is used, it essentially just works in the application and works the needed options before it passes to the Presentation Layer(#6).

>Q: - "Which layer handles logical addressing?"

A: - **Network Layer (3)** is used, this layer works to adress the destination, based on IP which is the logical adressing part.

>Q: - "When sending data over TCP, what would you call the "bite-sized" pieces of data?"

A: - For TCP we call the "bite-sized" pieces of data **"segments"** , in UDP they are called "datagrams"

>Q: - "Which layer would the FTP protocol communicate with?"

A: - Since FTP is built on the client-server model it runs networking options for the Application, therefore it communicates on the **Application Layer(#7)**.

>Q: - "Which transport layer protocol would be best suited to transmit a live video?"

A: - When it concers live video, we need fast transfered data , therefore we will use **UDP** to throw fast data to the targeted computer.

## Task 3 - Encapsulation

>Q: - "How would you refer to data at layer 2 of the encapsulation process (with the OSI model)?"

A: - Layer 2 of the encapsulation is the Data Link layer(#2), therefore the data is refered as **"Frames"**

>Q: - "How would you refer to data at layer 4 of the encapsulation process (with the OSI model), if the UDP protocol has been selected?"

A: - At layer 4 which is the Transportation Layer(#4), the UDP "bite-sized" data that is encapsulated would be called **"datagrams"**

>Q: - "What process would a computer perform on a received message?"

A: - The reverse process of encapsulation which is **"de-encapsulation"**

>Q: - "Which is the only layer of the OSI model to add a trailer during encapsulation?"

A: - **The Data Link layer(#2)** adds a trailer at the end which verifies if the data has been corrupted on transmission.

>Q: - "Does encapsulation provide an extra layer of security (Aye/Nay)?"

A: - Aye!

## Task 4 - The TCP/IP Model

>Q: - "Which model was introduced first, OSI or TCP/IP?"

A: - **TCP/IP** was firstly introduced, after OSI was also introduced, it only is left as a starting learning point since its a bit more robust.

>Q: - "Which layer of the TCP/IP model covers the functionality of the Transport layer of the OSI model"

A: - Just like in the OSI model in the TCP/IP Model the **Transport layer** covers that.

>Q: - "Which layer of the TCP/IP model covers the functionality of the Session layer of the OSI model"

A: - In the TCP/IP model the **Application** covers the functionality of the Session Layer(OSI Model).

>Q: - "The Network Interface layer of the TCP/IP model covers the functionality of two layers in the OSI model. These layers are Data Link, and?.. "

A: - The Network Interface layer of TCP/IP covers the duo of the Data Link and the **Physical Layer** inside the OSI model.

>Q: - "Which layer of the TCP/IP model handles the functionality of the OSI network layer?"

A: - In the TCP/IP model we call it **Internet**

>Q: - "What kind of protocol is TCP?"

A: - TCP is a **connection-based** protocol.

>Q: - "What is SYN short for?"

A: - Synchronise.

>Q: - "What is the second step of the three way handshake?"

A: - SYN/ACK (which refers to Synchronise/acknowledgement)

>Q: - "What is the short name for the "Acknowledgement" segment in the three-way handshake?"

A: - ACK

## Task 5 - Wireshark

>Q: - "What is the protocol specified in the section of the request that's linked to the Application layer of the OSI and TCP/IP Models?"

A: - Domain Name System

>Q: - "Which layer of the OSI model does the section that shows the IP address "172.16.16.77" link to (Name of the layer)?"

A: - **Network Layer** covers the IP adresses in the OSI Model.

>Q: - "In the section of the request that links to the Transport layer of the OSI and TCP/IP models, which protocol is specified?"

A: - User Datagram Protocol.

>Q: - "Over what medium has this request been made (linked to the Data Link layer of the OSI model)?"

A: - As we see in the requests its stayed **Ethernet II** for the Data Link layer.

>Q: - "Which layer of the OSI model does the section that shows the number of bytes transferred (81) link to?"

A: - The transfering is done by the **Physical layer** therefore that is the part that shows the transffered number.

>Q: - "Can you figure out what kind of address is shown in the layer linked to the Data Link layer of the OSI model?"

A: - In this case it shows the [**MAC**](https://en.wikipedia.org/wiki/MAC_address) address.

## Task 6 - Ping

>Q: - "What command would you use to ping the bbc.co.uk website?"

A: - In this case we use the standard **ping** command **ping bbc.co.uk**

>Q: - "Ping muirlandoracle.co.uk ; What is the IPv4 address?"

A: - When we use the **ping muirlandoracle.co.uk** command we receive the following information 

`PING muirlandoracle.co.uk (217.160.0.152) 56(84) bytes of data.`

From this we can see that the IPv4 adress is **217.160.0.152**

>Q: - "What switch lets you change the interval of sent ping requests?"

A: - As per the **man pages** we learn the following **-i**

`-i interval ; Wait interval seconds between sending each packet. `

>Q: - "What switch would allow you to restrict requests to IPv4?"

A: - We use **-4** to restrict to IPv4, as stated in **man pages**

>Q: - "What switch would give you a more verbose output?"

A: - We use **-v** to specify a more verbose output as written in **man pages**

` Verbose output. Do not suppress DUP replies when pinging multicast address.`

## Task 7 - Traceroute

>Q: - "Use traceroute on tryhackme.com ; Can you see the path your request has taken?" 

A: - Just test the command **traceroute tryhackme.com** and study what you get as a result!

>Q: - "What switch would you use to specify an interface when using Traceroute?"

A: - Using **man traceroute** we learn that the **-i** switch, lets use specify and interface

`Specifies the interface  through  which  traceroute  should send packets`

>Q: - "What switch would you use if you wanted to use TCP SYN requests when tracing the route?"

A: - Using **man traceroute** we learn that the **-t** switch, lets use use TCP SYN requests.

>Q: - "Which layer of the TCP/IP model will traceroute run on by default (Windows)?"

A: - Since the traceroute sends requests and receive the path they take and the IP adresses we can surmise it is based around the
**Internet** layer, which is the Network layer in the OSI Model.

## Task 8 - WHOIS

>Q: - "Perform a whois search on facebook.com"

A: - Simply run a **whois facebook.com** and study the information received!

>Q: - "What is the registrant postal code for facebook.com?"

A: - After studying the whois of facebook.com we can determine the postal code is **94025**

`Tech Postal Code: 94025`

>Q: - "When was the facebook.com domain first registered?"

A: - Again after studying the whois , we learn the date it **29/03/1997**

`Creation Date: 1997-03-29T05:00:00Z`

>Q: - "Perform a whois search on microsoft.com"

A: - We just perform a **whois microsoft.com** and study the given information again!

>Q: - "Which city is the registrant based in?"

A: - After we study the infromation we determine that **Redmond** is the registrant city.

`Registrant City: Redmond`

>Q: - "What is the name of the golf course that is near the registrant address for microsoft.com?"

A: - After a google map search at the adress of the registrant, [**Bellevue Golf Course**](https://www.google.com/maps/place/Bellevue+Golf+Course/@47.6622501,-122.1454504,15.44z/data=!4m13!1m7!3m6!1s0x54900d4b4d6a7d5d:0xb20ed2fa66d35bf3!2z0KDQtdC00LzRitC90LQsINCS0LDRiNC40L3Qs9GC0L7QvSA5ODA1Miwg0KHRitC10LTQuNC90LXQvdC4INGJ0LDRgtC4!3b1!8m2!3d47.6701193!4d-122.1182369!3m4!1s0x54906d441ff622d3:0x674fb4f6e6569f39!8m2!3d47.6557658!4d-122.1518621) can be seen next to the adress.

>Q: - "What is the registered Tech Email for microsoft.com?"

A: - The registered tech mail is **msnhst@microsoft.com**

`Tech Email: msnhst@microsoft.com`

## Task 9 - Dig

>Q: - "What is DNS short for?"

A: -  A DNS is **Domain Name System**

>Q: - "What is the first type of DNS server your computer would query when you search for a domain?"

A: - After checking the local cache it would check the  **Recursive** DNS server

>Q: - "What type of DNS server contains records specific to domain extensions (i.e. .com, .co.uk*, etc)*? Use the long version of the name."

A: - **Top-Level Domain** deals with the domain extension.

>Q: - "Where is the very first place your computer would look to find the IP address of a domain?"

A: - The **local cache** is where it first checks.

>Q: - "Google runs two public DNS servers. One of them can be queried with the IP 8.8.8.8, what is the IP address of the other one?"

A: - A brief google search tell us that **8.8.4.4** is the second public DNS that needs to be queried. [Link](https://developers.google.com/speed/public-dns)

>Q: - "If a DNS query has a TTL of 24 hours, what number would the dig query show?"

A: - **86400** *(1 h = 3600seconds - > 24h x 3600 = 84 600)*