# Networking

. In simple terms computer networks are a group of devices connected together allowing them to share information and resources.

. They are important in modern infrastructure as its the foundation that  enables communication between devices, facilitates sharing of files, printers and more and most importantly their the backbone of app connectivity and data transfer. 



## Networking in DevOps

- Networking plays a critical role in DevOps, one of the main things they do is interact between different servers, then comes deployment where it allows you to manage deployments for your applications effectively. The next thing they do is help you manage your infrastructure, networking enables monitoring and managing devices and applications effectively that can help engineers like myself to spot issues quickly.


  <img width="463" height="248" alt="image" src="https://github.com/user-attachments/assets/ec17ede8-b138-42fa-9ed7-5f3103bb4166" />

## LAN & WAN 

- LAN stands for local area network, think of it like your homes wifi network, it connects devices within a small area like your home or office allowing them to share resources.
- WAN is known as a wide area network , it covers a larger geographical area then a LAN. The best example of a WAN is the Internet which connects devices across the globe. WAN's are used to connect multiple LAN's enabling communication and data transfer over long distances.

## Key Networking Components

- Switches: Think of it like a manager for your local area network, it connects mutliple devices within the same network. The switch ensures data flows smoothly between these devices preventing any congestion and ensuring efficient communication.
- Routers: The main purpose of a router is to direct traffic between different networks ensuring data gets in to the right place whether your browsing a wesbite or streaming a movie.
- Firewall: Acts like a security guard for your network monitoring incoming and outgoing traffic based on pre-defined security rules. Its main purpose is to protect your network from unauthorised access.


## IP Addressing 

- Its a unique identifier assigned to each device on a network, it allows devices to locate and communicate with each other.
- There is two types of IP addresses, IPV4 and IPV6.
- IPV4 addresses are 32 bit numbers written in a decimal format, they are seperated by four groups of numbers, with each group ranging between 0-255 providing 4.3 million unique IP addresses.
- IPV6 addresses are 128 bit numbers, they provide a vastly large pool of unqiue addresses, they are written in hexadecimal format and they are seperated by colons.
- Without IP addresses, devices wouldnt know where to send or recieve data.

  <img width="502" height="240" alt="image" src="https://github.com/user-attachments/assets/9d35904c-eb4b-4b2d-b966-213e12b2d117" />

## MAC Addresses 

- Its a unique identifier assigned to network interfaces, its a 48 bit address displayed in a hexadecimal format
- MAC addresses operate at the data link layer of the OSI model, they help to facilitate device identification within a local network.
- They play a critical role in ensuring data packets get sent to the right place.

  <img width="434" height="220" alt="image" src="https://github.com/user-attachments/assets/9f826b4f-a1d6-4122-be76-77eef2cb5dbe" />

## Ports & Protocols

- Ports can be described as logical doors on your device, each door is numbered and each number is used for a specific type of network communication.
- When your computer wants to send data, it uses ports to ensure data gets sent to the right place.
- Protocols are a set of rules that  define how data is formatted and transmitted across a network.
- Without Ports and Protocols network communicaton would be a mess, ports ensure data gets sent to the right application on your device while Protocols ensure data is understandable  and formatted for smooth communication.

## TCP & UDP

- TCP is like the postman of the internet, it ensures data sent from one device reaches the other device accurately and in the correct order.
- Characteristics of TCP :
  1. Connection-orientated - This means before any data is sent, a connection is established between two devices
  2. 3 Way Handshake - It ensures that both devices are ready to send and recieve data
  3. Reliable data transfer - It ensures that all data sent is recieved correctly on the other end, meaning if any data is lost or corrupted, TCP will resend it hence making it reliable.

- TCP is used when two devices need to exchange data  back and forth, a common example could be web browsing, file transfer and emails.
- To sum up its essential for any application where reliable delivery of data is crucial.

- UDP is a simple protocol used for sending and recieving data.
- Unlike TCP no prior communication is needed when sending out data
- Its conncetionless, data can be sent without establishing a connection, however the downside is there is no guarantee that data will reach its destination.
- It is much faster then TCP since there is no connection needed to setup however its unreliable due to the fact being there is no guarantee that data will get delivered to its intended destination.
- UDP is suitable for real-time applications, for example (video gaming, online streaming) where speed is more important then reliability.
- Some VPN's use UDP because its faster and more suitable for real-time applications

<img width="487" height="244" alt="image" src="https://github.com/user-attachments/assets/0969cb92-af8c-4ba9-be09-1b117b6c0dbb" />


