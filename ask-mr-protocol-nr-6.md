# ASK MR. PROTOCOL (#6): It’s All Done With Mirrors

## April 2, 1985

Q: What IS the “Internet?” Why is it called that?

Sincerely,
Eager to Understand

A: This opportunity for an historical excursis, my dear Eager, endears you forever to Mr. Protocol’s heart

In the dim and distant mists of time, when the first organisms began to populate the Pre-Cambrian Network Sea, a far-sighted collection of researchers began the design of a computer network. This project would demonstrate the practicality of connecting computers in a high-speed, long- distance network. Any computer in the network could communicate with any other in such a way that it would appear that the two computers were directly connected; intervening machines and transport mechanisms would be invisible.

The project was also designed to demonstrate that machines of any type could communicate. This had a profound effect not only upon the protocol which was designed but on the implementation of the network in hardware. Rather than implementing the low-level routines in each system they wished to connect to the net, the researchers decided that the real network would consist of identical machines, while the actual research machines would speak a higher-level protocol to the network engines. These network engines were to be called IMPs, or Interface Message Processors, since they stood as an interface between the so-called “host” computers and the network.

A number of very intelligent design decisions were made. First, the host- to-IMP and IMP-to-host protocols were designed to be independent of the word length of the host machine. Second, the IMPs woe made as small and cheap as practical, and able to interface to several hosts at once. Finally, each host was assigned an identifying number. The field in the network protocol which held this host ID was made far larger than necessary to accommodate the number of hosts which would ever connect to this demonstration research network, which was called the Arpanet.

As usual, the benefits of success became the headaches of too much success in a startlingly short period of time. Within a few years, sites had large numbers of machines, many of which were cheaper than the IMP’S used to connect them. Local-area networks became widely available, but the network protocol used on the Arpanet (Network Control Protocol, or NCP) couldn’t understand the notion of several hosts connected on a local net and communicating with the Arpanet through a common connection. Finally, the extremely large host ID field, which allowed all of 256 hosts, was too small by many orders of magnitude.

Imagine, if you will, a motor caravan. This caravan has been traveling for some years across foreign lands, when it is discovered that a) the roads are getting too narrow, and b) all the engines have to be replaced because now there’s no gasoline available, only diesel fuel. There is, of course, only one possible logical decision. Replace all the engines and rebuild all the vehicle bodies without stopping.

The carnage which followed was amazing, not so much for the people who were run off the road, or run over, but for the fact that it worked so smoothly. The introduction of the Internet Protocol (IP) allowed hosts on local networks to communicate with other hosts on different networks through machines called “gateways.” In the space of less than a year, the number of hosts at least potentially reachable over the “Internet” (which, my dear Eager, is defined as the collection of networks using IP which are connected via gateways...did you think I’d never answer your question?) increased enormously from the 150 or so hosts which made up the old Arpanet

Next time, my dear Eager, if you’re still listening, we'll discuss the current state of the Internet. If it started Pre-Cambrian times, we must be at least in the Jurassic by now (see all the lovely dinosaurs still hanging about?).
