# Objective

Understand the basic mechanics of ethernet, IP, TCP, UDP, ICMP, and ARP

## Instructor Notes

## Required Resources

## I Do

Before computers, important information was transmitted in all sorts of ways: word of mouth, song, dance, cave drawings, railroads, postmen on horses, even carrier pigeons. Each of these prior methods of data transmission required some element of human interaction - a postman needed to sort letters by zip code, an orator needed to use the correct inflection and tone, a pigeon handler needed to tie the note to the bird's leg, you get the idea. The invention of computers and the internet meant that tons of data could be quickly transported, without the need for human intervention! This was huge! But it meant that very specific rules needed to be developed. We call these rules 'protocols' and they dictate exactly how your computer connects to google.com, how it sends an email to your boss, and how humans were able to finally step back from the business of information transmission.

This objective deals with 6 important protocols involved in data transmission. Here, we'll draw a distinction between protocol by grouping the ones globally involved in packet transmission and those involved on the local level.  Though they can be grouped for learning, each protocol is connected to another, and all work together to get data from point A to point B.

### Global Transmission Protocol

|Acronym| Meaning | Definition  |
|--|--|--|
|IP|Internet Protocol| Basis for communication between devices.  |
|TCP|Transmission Control Protocol |Ensures accurate communication between devices.  |
|UDP|User Datagram Protocol|Ensures accurate communication between devices when TCP cannot be used. |

You've heard of IP, and at the very least know that every device in the world has a unique IP address. In a broader context, IP is a set of rules that govern and standardize how packets move from one router to another. IP is great, but IP isn't perfect, and sometimes, packets can get lost. This is where TCP comes in.

TCP works with IP to ensure that 1) no packets get lost or duplicated, 2) packets are assembled correctly, and 3) delays aren't significant. In cases where delays are significant, a less sophisticated protocol called UDP can be used to ensure similar packet delivery promises are kept. Sometimes, UDP is intentionally used instead of TCP where massive amounts of data need to be sent and reliability isn't as important.

### Local Network Protocol

|Acronym| Meaning |Definition  |
|--|--|--|
|ICMP|Internet Control Message Protocol | Blocks inaccurate communication between devices when TCP and UDP fail. |
|ARP|Address Resolution Protocol| Makes sure communication goes to the correct device on a network.|
|Ethernet|Ethernet| Connects all the devices on a network (computers and routers). |

ICMP is triggered when UDP or TCP fails and offers suggestions (never seen by the user) to fix the issues, often when ICMP is triggered, the user doesn't know, and TCP/UDP finds another way to get the packets to their destination.

Finally, we need to consider ARP and ethernet. Both are working on the physical, network layer level. That means in your home, at the coffee shop, wherever connectivity exists. When data gets to its final network, it needs the ARP to find the specific device (computer, phone, tablet) that it should arrive at. It moves through the ethernet (more commonly, wifi*) until the message is finally received.

*Ethernet and wifi are _not_ the same thing, but they accomplish the same goal in the communication process. Namely, communicating between all devices on the same network.

### Technical Definitions

Slightly more technical definitions might be easier to digest with that background:

|Acronym| Meaning | Definition  |
|--|--|--|
|IP|Internet Protocol|Host or network interface identification and location addressing. |
|TCP|Transmission Control Protocol |Breaks down data into packets and manages delivery from one system to another |
|UDP|User Datagram Protocol|Alternate to TCP, used for establishing low-latency and loss-tolerating connections |
|ICMP|Internet Control Message Protocol |Error Reporting activated when there is an issue with TCP/IP|
|ARP|Address Resolution Protocol|Links MAC addresses and IP addresses to ensure each computer has unique network identification|
|Ethernet|Ethernet|A system for connecting several computer systems to form a local area network, with protocols to control the passing of information and to avoid simultaneous transmission by two or more systems.  |

## We Do

Let's expand on our OSI model whiteboarding activity by placing each protocol into an OSI layer.

Recall that our OSI model contains 7 layers, and looks like this:
![source: [https://www.webopedia.com/quick_ref/OSI_Layers.asp](https://www.webopedia.com/quick_ref/OSI_Layers.asp)](https://lh3.googleusercontent.com/iMnsbSRP1rAS3MgO3u_A2BhOBz1OXgPNzhkd-Xi6awQnsktyU0Iulyark66HuXaHVOfWuSAj2G0) *need to make a lambda-approved graphic*

In the first objective, we talked about OSI on a conceptual level, without knowledge of protocols. Now, we can start to add on to that understanding, by placing protocols into specific layers.

*Whiteboarding should include this information!
Ethernet isn't included in this diagram but belongs on the Data Link layer
Note that all of the protocols we're worried about are in the 'moving data around' layers*
![enter image description here](https://lh3.googleusercontent.com/VlhP4wEeA5VqVRrgEqmUoECuTq28G9UFdMcRQZuTwu0GJSJqaNHFYhWLR1-xOeIY9nxg5LAs63Y)![Screen Shot 2019-10-18 at 4.05.48 PM](https://i.imgur.com/JsKfszH.png)

## You Do

Summarize your current understanding of what happens when you type google.com into your internet browser in paragraph format or long-form bulleted list. Be prepared to share in breakout rooms.

Your summary must include all of the following terms:

- User
- Client
- Application
- Server
- Presentation
- Session
- Transport
- Network
- Data Link
- Physical
- TCP
- HTTP
- IP
- Ethernet
- ARP
- UDP
- ICMP

## Additional Resources

- Tech Dictionary: [Techterms.com]((https://techterms.com/))
- Animated Video: [The Internet: Packets, Routing, and Reliability]([https://www.youtube.com/watch?v=AYdF7b3nMto](https://www.youtube.com/watch?v=AYdF7b3nMto)) *the whole series on Internet is likely helpful*
- Reading (IP/TCP): [What IP means and How It Works](https://www.lifewire.com/internet-protocol-explained-3426713)
- Reading (UDP vs TCP): [User Diagram Protocol](https://www.lifewire.com/user-datagram-protocol-817976)
