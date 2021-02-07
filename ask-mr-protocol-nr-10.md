# ASK MR. PROTOCOL (#10): Mr Protocol Performs An Operation

## December 29, 1987

> New brain! — M. Python

> No room! No room! — M. Hatter

> Network administrators are either very thin or very fat, depending on how they deal with stress.
— T. Hardgrave

> This time for sure! — B. Moose


Mr. Protocol recently had occasion to assist at a brain transplant operation. A core gateway was being given new smarts in order to alleviate a severe case of brain strain. Why, you may ask, was the gateway under strain? What, in fact, is a core gateway? Mr. Protocol, as usual, is glad you asked.

As CSNET sites begin to move towards full Internet connectivity, even over dialup phone lines, they are joining a community which has grown many times larger than originally anticipated. Fifteen or twenty years ago (Mr. Protocol is sure you will excuse him for a moment while he listens to his joints creak), when the original Arpanet was being put together, the designers of the original NCP protocol scratched their heads over the exact format of the fields in the packets. “How large should we make the host field?” they asked. “Large enough,” they replied. “WELL!!?!?” they asked once more. “...,” they replied. Finally they decided they should make it so large that the number of hosts would never possibly exceed the size of the host number field, even if the network grew to a gigantic size.

They made it large enough for 255 hosts.

Hindsight being a wonderful thing, when the NCP protocol was replaced with the current IP protocol, they made the host field (actually the host-cum-netwoik field) large enough for “billyuns and billyuns” of hosts.

It still isn’t large enough, many people think.

It is obvious that the net has grown rather large.

What is interesting to note is HOW it has grown. Rather than placing more and more hosts directly onto the Arpanet/Milnet/etc. long-haul networks, almost all institutions have connected many processors together into a high-speed local-area network, and connected only one of these locally networked machines to the “rest of the world” via a long-haul net In the case of CSNET this operation may be repeated: local hosts are connected to the PhoneNet or X25Net machine, which is connected (along with the rest of the PhoneNet/X25Net machines) to the Csnet-Relay machine, which is connected to the Internet

Usually what this means is that most of the hosts are able to communicate at very high speed with their “gateway” machines, which in turn are able to communicate at only moderate data rates via the long-haul networks, which are slower due to the cost of long-distance data transmission. Mr. Protocol feels it should be obvious that this is exactly backwards from the ideal state of affairs. The long-haul nets SHOULD be much faster than the local-area nets, to avoid having high-speed traffic back up at the gateways. Mr. Protocol also realizes it will be a cold day in a warm place before this Platonic ideal is attained.

The result is just what one would expect: extremely congested long-haul networks and extremely busy gateways. However, this state of affairs has been analyzed in excruciating detail • in theory • for many years. Unfortunately bringing the theory to bear on the real world has not
proved trivial. Some real performance improvements in severely congested nets have been realized using fixes which Mr. Van Jacobson of Lawrence Berkeley Laboratory has evolved based on network congestion theory. These fixes permit the best use possible to be made of congested networks. though they consist of only about five extra lines and two lines moved in a typical Berkeley UNIX kernel. Unfortunately, as Mr. Protocol has proved time and again, messing with this code is extremely risky business. It is very easy to create a kernel which will happily babble nonsense at frequent intervals, to the great distress of network neighbors. Two sample exchanges demonstrate this point.

BEFORE “IMPROVEMENT” TO HOST1:

**Host1:** “Here’s a packet!”

**Host2:** “Thanks, Jack. But you should be sending this stuff via gateway foobar.fooble.arpa” (Actually the gateway would say that; We’re illustrating a point)

**Host1:**	(via new gateway) “OK! ”

**Host2:**	(etc.)

AFTER “IMPROVEMENT”	TO HOST1:

**Host1:**	(Hic!) ’’Here’s a packet!”

**Host2:**	“Thanks, Jack. But you should be sendingg this stuff via gateway foobar.fooble.arpa”

**Host1:**	(still via old gateway) (Hic!) “She’s right, mate! Here’s another packet!”	

**Host2:**	“Thanks, Jack. But you should be sending this stuff via gateway foobar.fooble.arpu (Hosts can be dull conversationalists.)

**Host1:**	(still via old gateway) (Hic!) “She’s right, mate! Here’s another packet! And while we’re on it, mate, did you know the world is a cube?”

**Host2:**	“Thanks, Jack. But you should be sending this stuff via gateway foobar.fooble.axpa. And that’s very interesting!” (Then valiantly rational to the last). “But that would be mean we should be falling toward the center of the cube face.”

**Host1:**	(still via old gateway) (Hie!) “Right you are mate! Are ya read to roll?

**Host2:**	“Thanks, Jack. But you should be sending this stuff via gateway foobar.
fooble.arpa. And yes, I am!”

**Host1:**	(\*\*ZIP\*\* !!!CRASH!!!)

**Host2:**	(\*\*ZIP\*\* !!!CRASH!!!)

In the face of this, Mr. Protocol has been totally impressed by Mr. Jacobson, and raises his glass high in the direction of LBL-on-the-Hill.

Hence Mr. Protocol’s assistance at a brain transplant operation. The various long-haul nets are glued together by means of a set of special gateway machines, called “core gateways.” These arcane beasts are understood by only a few people. Mr. Protocol is pleased to announce that he is not one of them. Protocols are bad enough, he feels, without also entering into matters which would have gotten one burned in Salem a mere few hundred years ago. Suffice it to say that much of the congestion in the long-haul nets is due to the fact that many of these gateway machines are not particularly speedy. A program is currently underway to improve gateway performance by swapping in faster processors, as well as more memory to hold bigger tables. These locally cached tables are referred to with discouraging frequency by hosts around the net, and to the extent that they can be made as large as possible, long-haul network traffic will be reduced.

All the brains in the world, however, will not replace a good pair of legs. There are plans in the offing to increase the speed of the long-haul networks, which speed has not changed in all the years since the Arpanet’s first few hosts were linked.

Of course in those days, said hosts were not fast enough to keep up with the neb As Mr. Protocol hammers away on his workstation, which is about five times faster than the time-sharing machine he first saw hooked to the Arpanet, he ruefully notes that Times Have Changed.
