# Introductory Networking


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

Q: - "How would you refer to data at layer 2 of the encapsulation process (with the OSI model)?"
A: - Layer 2 of the encapsulation is the Data Link layer(#2), therefore the data is refered as **"Frames"**

Q: - "How would you refer to data at layer 4 of the encapsulation process (with the OSI model), if the UDP protocol has been selected?"
A: - At layer 4 which is the Transportation Layer(#4), the UDP "bite-sized" data that is encapsulated would be called **"datagrams"**

Q: - "What process would a computer perform on a received message?"
A: - The reverse process of encapsulation which is **"de-encapsulation"**

Q: - "Which is the only layer of the OSI model to add a trailer during encapsulation?"
A: - **The Data Link layer(#2)** adds a trailer at the end which verifies if the data has been corrupted on transmission.

Q: - "Does encapsulation provide an extra layer of security (Aye/Nay)?"
A: - Aye!

## Task 4 - The TCP/IP Model

Q: - "Which model was introduced first, OSI or TCP/IP?"
A: - **TCP/IP** was firstly introduced, after OSI was also introduced, it only is left as a starting learning point since its a bit more robust.

Q: - "Which layer of the TCP/IP model covers the functionality of the Transport layer of the OSI model"
A: - Just like in the OSI model in the TCP/IP Model the **Transport layer** covers that.

Q: - "Which layer of the TCP/IP model covers the functionality of the Session layer of the OSI model"
A: - In the TCP/IP model the **Application** covers the functionality of the Session Layer(OSI Model).

Q: - "The Network Interface layer of the TCP/IP model covers the functionality of two layers in the OSI model. These layers are Data Link, and?.. "
A: - The Network Interface layer of TCP/IP covers the duo of the Data Link and the **Physical Layer** inside the OSI model.

Q: - "Which layer of the TCP/IP model handles the functionality of the OSI network layer?"
A: - In the TCP/IP model we call it **Internet**

Q: - "What kind of protocol is TCP?"
A: - TCP is a **connection-based** protocol.

Q: - "What is SYN short for?"
A: - Synchronise.

Q: - "What is the second step of the three way handshake?"
A: - SYN/ACK (which refers to Synchronise/acknowledgement)

Q: - "What is the short name for the "Acknowledgement" segment in the three-way handshake?"
A: - ACK