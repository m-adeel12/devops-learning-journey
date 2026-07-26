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

## OSI Model:
- OSI model stands for Open Systems Interconnection model, it's a standard framework that simplifies how devices and applications communicate over a network.
- It consists of 7 Layers, starting from the bottom
  1. Physical Layer- It transmits raw bits of stream over the physical medium. Physical medium can be copper, fibre, cables or even switches
  2. Data link layer- This layer is reponsible for node to node data transfer, think of it like a traffic cop that ensures data packets are sent and are recieved correctly between different network nodes. At layer 1 data was unorganised, however this layer puts your data packets into frames where its actually organised. Frames are like envelopes that carry data and ensures it gets to the right place. Some of the components that do the job here are MAC address, switches and bridges.
  3. Network layer- This layer determines how data is sent to the recipient, on top of that it manages packet forwarding including routing through different routers. It decides the best path for data to travel across different networks, ensuring it gets to the right place. Some of the components that work in this layer are IP addresses and routers. Data in this layer are organised into packets,  packets are like little parcels that carries data from one device to another, this is where IP addressing comes in, it handles where packets go to, and routers are the components that allows them to do this job by directing data packets across the best paths across the networks.
  4. Transport layer- This layer is responsible for providing reliable data transfer services across to the upper layers, think of it like a delivery service that ensures your data parcels arrive safely and in the correct sequence. Now some of the protocols that allows it to do this job are TCP and UDP
  5. Session Layer- This layer is responsible for three things, establishing, managing and terminating sessions. Establising a session means getting a session started, for example logging in to a website and maintaning a session means keeping the session alive. Some of the example components are management protocols like RPC, NetBIOS and more.
  6. Presentation Layer- This layer is sometimes known as a syntax layer as it ensures data being sent is in a useable or readable format. This layer can handle encryption ensuring data security as well as data formatting
  7. Application Layer- This layer provides network services directly to applications. It handles things like web browsing, file transfers and emails, some of the example protocols are HTTP used for accessing websites.FTP used for transferring files.
 
## TCP/IP Model

- This model consists of 4 layers:
  1. Application Layer
  2. Transport Layer
  3. Internet Layer
  4. Network Access Layer
 
    <img width="435" height="248" alt="image" src="https://github.com/user-attachments/assets/fcc65bea-d8d7-4870-a56b-d12d7fc62ba3" />
 
## Domain Name System (DNS)
- In simple terms DNS allows us humans to keep track of websites and hosts by name instead of an IP address, think of it like a contact for the internet, if you dont know someones name you can easily search it up rather then having to memorise their number, same conecpt applies to DNS, it simplifies navigation on the Internet and is essential for accessing wesbites and services.

## DNS Components 

- Name servers are crucial for DNS functionality, they load DNS settings and configurations, and also respond to your queries from clients or other servers about domain names.
- There are two types
  1. Authoritative servers - These servers hold the actual DNS records
  2. Recursive servers - These servers do not hold the final answer. Instead they query the other name servers on behalf of the client to find the correct DNS record.

- Zone files are stored inside your name servers, and they contain information about the domain. They help name servers answer queries about how to get to the domain if the name server doesnt know the answer directly.
- Zone files organise your DNS information in a readable and managed way, making it easier to handle DNS records. 
     
- Zone files are comprised of multiple resource records. Each record contains specific information about hosts, name servers and various other resources.
- Some components of the resource record are record names, TTL, Class, Type, Data


  <img width="449" height="169" alt="image" src="https://github.com/user-attachments/assets/89ee2d84-925e-40cc-95ac-4dc6fca47025" />

## DNS Records 

. A - Maps a domain name to an IPv4 address
. AAAA - Maps a domain name to an IPv6 address 
. CNAME - Alias of one name to another, allows you to match multiple domain names to the same IP address, example www.google.com > google.com
. MX - Specifies the mail server responsible for recieving email for the domain
. TXT - Allows domain administrators to insert any text into DNS. Commonly used for verification purposes and to hold SPF(Sender Policy Framework) data
