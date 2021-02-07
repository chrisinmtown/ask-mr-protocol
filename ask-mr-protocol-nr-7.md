# ASK MR. PROTOCOL (#7): Who That Say Who That?

## June 12, 1985

> No sound was heard of clashing wars;

> Peace brooded o’er the hushed domain...

> —	Alfred Domett

> Don't look back — someone might be gainin' on you.

> —	Satchel Paige

Q: What’s in a name?

A: More than we wanted. In halcyon days of yore, when everybody knew everybody (or, at least, everybody worth mentioning), figuring out what hosts were where on the network was as simple as looking at a table associating host names with host addresses.

These clean and simple days were, of course, doomed by progress. Mr. Protocol is not complaining; far from it! More complications mean more protocols, which mean more grist for the mill. If everything was easy, Mr. Protocol would have to go back to something simple, like taking tigers for their afternoon strolls.

The particular complication which caused this particular bit of nuisance was the development of IP, the Internet Protocol. Using this protocol, entire networks may be connected through transparent gateways, allowing any host on any network to communicate with any other host without knowing or caring which network the foreign host is on. The problem comes in finding out that address in the first place.

The early Arpanet was a fairly patriarchal place, hackers notwithstanding. Clearly the Network Information Center was on top of the situation and was always informed whenever a new host came onto the net When more than one network put in an appearance, more than one center with authority to name hosts was thereby created. Coordination with the NIC worked for some years, but lately, it would seem, the blueness of the network blood is becoming somewhat diluted. It is now impossible even to name all the networks, let alone all the hosts, which can now communicate via what used to be the Arpanet This new Internet needs a new scheme for associating host names with host addresses.

The problem being that if more than one organization (many, in fact) can name hosts, then more than one organization should provide the needed information to the network at large. This is done by separating the Internet into zones of naming authority, called domains. Each organization with the authority to name hosts runs a special network server, called a domain server, which understands a network-wide language used for exchanging queries and answers concerning host names, addresses, and services. Starting from a “root” domain, subauthority is granted to progressively more localized domains, until a domain is reached which actually contains the host machine in question.

For example, the host “UCLA-LOCUS” is now “LOCUS.UCLA.EDU”, meaning that from the (unnamed) root domain, go to domain EDU, then domain UCLA, and that contains the host LOCUS. There may be a host named LOCUS in one or several other domains; that is the whole point of specifying domains completely. The fully qualified (i.e. complete) domain name distinguishes this LOCUS from any other elsewhere.

The “tree-walking” is not necessary to reach the host If the Internet address is known it may be used directly. If the address is not known, then a tree of domain servers is used. First one would ask the root server (whose Internet address is presumed known) for the address. It would respond with a pointer to the domain server for EDU; the EDU server, when similarly interrogated, would respond with a pointer to the UCLA server, which in turn would finally be able to respond with the address of the host in question.

The software to do all the poking is called a “resolver." It lives on the local host and presumably remembers the answers to all of these questions for some time, so that in future it can provide the various addresses instantaneously.

Some might think that this means that the friendly and intimate days when everyone knew everyone else are gone forever. Mr. Protocol prefers to think of it as a return to the (yet more bygone) days of directory assistance. Think of it: the phone book is no more, and now you can ask the operator for the number every time!
