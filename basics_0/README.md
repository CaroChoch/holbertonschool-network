# Networking basics #0  

## Task 0 : OSI model  

OSI (Open Systems Interconnection) is an abstract model to describe layered communication and computer network design. The idea is to segregate the different parts of what make communication possible.

It is organized from the lowest level to the highest level:

The lowest level: layer 1 which is for transmission on physical layers with electrical impulse, light or radio signal
The highest level: layer 7 which is for application specific communication like SNMP for emails, HTTP for your web browser, etc
Keep in mind that the OSI model is a concept, it’s not even tangible. The OSI model doesn’t perform any functions in the networking process. It is a conceptual framework so we can better understand complex interactions that are happening. Most of the functionality in the OSI model exists in all communications systems.

In this project we will mainly focus on:

The Transport layer and especially TCP/UDP
On the Network layer with IP and ICMP
The image bellow describes more concretely how you can relate to every level.

### Question 0: 

What is the OSI model?

1- Set of specifications that network hardware manufacturers must respect  
2- The OSI model is a conceptual model that characterizes the communication functions of a telecommunication system without regard to their underlying internal structure and technology  
3- The OSI model is a model that characterizes the communication functions of a telecommunication system with a strong regard for their underlying internal structure and technology  

--> The correct answer is : 2- The OSI model is a conceptual model that characterizes the communication functions of a telecommunication system without regard to their underlying internal structure and technology.  

### Question 1: 

How is the OSI model organized?

1- Alphabetically  
2- From the lowest to the highest level  
3- Randomly  

--> The correct answer is : 2- From the lowest to the highest level.  

## Task 1. Types of network

LAN connect local devices together, WAN connects LANs together, and WANs are operating over the Internet.  

### Question 0:

What type of network a computer in local is connected to?  

1- Internet  
2- WAN  
3- LAN  

--> The correct answer is : 3- LAN (Local Area Network).  
A LAN is a network that covers a relatively small geographical area, such as a home, office, or building. It allows devices within that area to communicate with each other and share resources like files, printers, and internet access.  


### Question 1: 

What type of network could connect an office in one building to another office in a building a few streets away?  

1- Internet  
2- WAN  
3- LAN  

--> The correct answer is : 2- WAN (Wide Area Network).  
A WAN is a network that spans a larger geographical area, such as multiple buildings, cities, or even countries. It enables the interconnection of LANs over long distances, providing connectivity between geographically dispersed locations. The internet is often used as a means to establish a WAN connection between remote offices, utilizing various networking technologies such as leased lines, MPLS (Multiprotocol Label Switching), VPN (Virtual Private Network), or other wide area networking solutions.  

### Question 2: 

What network do you use when you browse www.google.com from your smartphone (not connected to the Wifi)?  

1- Internet  
2- WAN  
3- LAN  

--> The correct answer is : 1- Internet  
The Internet is a global network of networks that allows devices from different locations to communicate and access online resources. Mobile devices, such as smartphones, connect to the Internet using cellular data networks provided by mobile service providers. This enables users to access websites, services, and applications from anywhere with cellular coverage.  

## Task 2 : MAC and IP address  

### Question 0:  

What is a MAC address?  

1- The name of a network interface  
2- The unique identifier of a network interface  
3- A network interface  

--> The correct answer is : 2- The unique identifier of a network interface.  
A MAC address (Media Access Control address) is a unique identifier assigned to a network interface, such as a network card or a wireless adapter, by the manufacturer. It is a hardware address that is permanently assigned to the device during its production.

The MAC address is a 48-bit (or 6-byte) address and is typically represented in a hexadecimal format, with groups of two digits separated by colons or hyphens. It serves as a unique identifier for the network interface at the data link layer of the OSI model.

Each network interface, whether it's an Ethernet card, Wi-Fi adapter, or other networking device, has a distinct MAC address. This address is used to identify the device on the local network, allowing data to be sent and received by the correct device. MAC addresses play a crucial role in Ethernet and Wi-Fi communications, where they are used for addressing and routing data packets within a local network.  

### Questtion 1:

What is an IP address?  

1- Is to devices connected to a network what postal address is to houses  
2- The unique identifier of a network interface  
3- Is a number that network devices use to connect to networks  

--> The correction answer is : 1- Is to devices connected to a network what postal address is to houses.  
An IP address (Internet Protocol address) is a numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. It serves as a unique identifier for a device or a network interface within a network.

An IP address is similar to a postal address for houses in the sense that it enables devices connected to a network to be located and communicated with. It allows devices to send and receive data across networks and enables network communication by providing a standardized addressing scheme.

IP addresses are typically represented as a series of numbers separated by periods. There are two main types of IP addresses: IPv4 (Internet Protocol version 4) and IPv6 (Internet Protocol version 6). IPv4 addresses are composed of four sets of numbers, while IPv6 addresses are longer and consist of eight sets of hexadecimal digits.

Devices use IP addresses to connect to networks, communicate with other devices, and access resources on the Internet. The IP address is essential for routing data packets to the correct destination within a network or across the internet.  

## Task 3. UDP and TCP  

### Question 0:  

Which statement is correct for the TCP box:  
1- It is a protocol that is transferring data in a slow way but surely  
2- It is a protocol that is transferring data in a fast way and might loss data along in the process  

--> The correct answer is : 1- It is a protocol that is transferring data in a slow way but surely.
TCP is a reliable transport protocol that guarantees the delivery of data packets in a reliable and orderly manner. It ensures that data is transferred accurately and without loss or corruption. TCP achieves reliability through mechanisms such as acknowledgment, retransmission of lost packets, and flow control.

While TCP provides reliability, it may introduce some additional overhead and latency compared to other protocols. However, its primary focus is on the secure and accurate delivery of data rather than speed.  

### Question 1 :  

Which statement is correct for the UDP box:  
1- It is a protocol that is transferring data in a slow way but surely  
2- It is a protocol that is transferring data in a fast way and might loss data along in the process  

--> The correct answer is : 2- It is a protocol that is transferring data in a fast way and might loss data along in the process.  
UDP is a connectionless transport protocol that offers a faster and more lightweight method of transmitting data compared to TCP. It provides a best-effort delivery mechanism, meaning that it does not guarantee the reliable delivery of packets. UDP does not have built-in mechanisms for acknowledgment, retransmission, or flow control like TCP.

While UDP is faster due to its reduced overhead, it does not prioritize reliability. In certain scenarios where speed is crucial, such as real-time streaming, video conferencing, or online gaming, UDP is preferred. However, this speed advantage comes at the cost of potentially losing packets during transmission, as UDP does not have mechanisms to ensure reliable delivery.  

### Question 3: 

Which statement is correct for the TCP worker:  
1- Have you received boxes x, y, z?  
2- May I increase the rate at which I am sending you boxes?  

--> The correct answer is : 1- Have you received boxes x, y, z?  
TCP employs acknowledgment mechanisms, where the sender expects acknowledgments from the receiver for the successful delivery of packets. This allows the sender to ensure that all sent packets have been received by the recipient. In this context, the statement is asking for confirmation of packet receipt.

The statement "May I increase the rate at which I am sending you boxes?" does not align with the characteristics of TCP. TCP utilizes flow control mechanisms to regulate the rate of data transmission based on the receiver's ability to handle and process the incoming data. The sender adjusts the transmission rate dynamically based on the acknowledgments and feedback received from the receiver. Therefore, the sender would not directly ask for permission to increase the sending rate, but rather it would be controlled automatically by the TCP protocol based on the network conditions and congestion control algorithms.  










