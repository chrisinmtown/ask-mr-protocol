# ASK MR. PROTOCOL (#4): Music To My Eyes

## January 31, 1984

Q: You nice folks at the CIC have given us some “simple, easy
guidelines” on the proper format of mail addresses. How do you explain
those monsters we keep seeing in real mail?

A: Mr. Protocol is glad you asked. He has been watching the address
wars for some time now and has been amazed at the creativity shown,
not only by users, but by programs. He feels that the neglected area
of address composition is one of the most fertile artistic arenas in
the latter half of the Twentieth entury. While artists are still
stupefied by the invention of photography, and attempt to create works
which either look like giant soup cans, or like nothing at all, and
while musicians attempt to destroy their instruments without losing
rhythm, network users are composing entire symphonies where a simple
address would do.

These compositions have a structure familiar to students of
music. They begin with the introduction of a theme, generally
involving various mixtures of host names and exclamation points. From
there they move to the development, involving more host names, percent
signs, and perhaps the introduction of an actual user name. There
follows a climax, involving one, two, and possibly even three signs,
from which develops a coda of one or two final host names, plus a
domain or three, generally pulled from the mists of artistic
creativity rather than any real specification. These marvelous
creations are then subjected to the tender mercies of various
automatic mail routing systems, which will often, in an attempt to be
helpful, introduce further complexities. Often the final product, so
far from being legal, cannot be understood by any known entity, human
or mechanical. (Mr. Procotol regards much electronic music in the same
light, but then he IS a fuddy old so-and-so, isn’t he?)

Mr. Protocol is particularly enamored of the solution proposed by
Peter Honeyman, who, given a message which has already traversed a
path, is able to construct the best possible return path using a
priori knowledge and a healthy dose of graph theory. (See “A Parser
for Electronic Mail Addresses”, by Peter Honeyman and Pat
E. Parseghian, PROCEEDINGS, USENIX Association Winter Conference,
Dallas 1985, pp 184-190.)

This theory, of course, only works on healthy addresses, complex as
they may be. It would take an expert system (or an expert postmaster)
to determine what, if anything, can be done with some of the wonders
spewed forth by the Internet soup.

Let us examine one of these compositions, and see if we can make some
sense of it:

    princeton! down! honey %purdue@ csne t-relay .ARPA

This pleasant little melody is actually relatively healthy. While
there is no single Official Specification which describes how to parse
it, there are a number of ad hoc rules which may be applied. The real
problem represented here is that this address includes pieces of three
networks: UUCP, CSNET, and Internet.

“princeton!down!honey” is in the key of UUCP, “honey” is evidently the
user. However, we do not know offhand if “honey” is at host “down”,
which we are supposed to get to from “princeton” via
“purdue@csnet-relay.ARPA”, or if the user is really “honey@purdue”,
and host “down” is supposed to talk to host “purdue.”

Mr. Protocol’s long-standing migraine is caused by the fact that there
is no obvious answer to this question. In fact, he is often to be
found hunched over a glass of milk at his kitchen table at 3 A.M.,
mourning the fact that fundamental independence of network addressing
schemes means fundamental ambiguity in network address parsing.

In fact, as Mr. Honeyman has pointed out, only a priori knowledge can
tell us how to parse this example. We must know either that
“princeton” talks to “purdue” and that “down” does not, or we must
know that “honey” is at “down” and not at “purdue.” (Pop Quiz: Is
“purdue” in the key of UUCP, the key of CSNET, or B-flat Minor?)

All of this assumes that the sign has the loosest binding, and that
the address is to be “cracked” there first. In cases with multiple “@”
signs, all bets may be off:

    honey@princeton!down%purdue@csnet-relay

This thundering piece of network nonsense is typical of the sort of
address which goes nowhere fast (Mr. Protocol is reminded of the works
of Mahler, but is much too polite to suggest such a thing.) This
cripple is destined for the bit basement at some host and which host
that will be cannot easily be predicted. In fact, a human who had seen
correctly formatted addresses would probably be able to recast this,
but such work is chancy, and generally beyond the capabilities of
automatic programs. Of course, there is always the chance that the
mail systems along the way will all happen to do the right thing, in
which case the user who originated this address will continue to use
it quite happily, until someone along the way changes their software
and the address breaks forever.

A few simple rules:

1)	BE LAZY. Try to use domain routing where possible. If your destination address lies in UUCP-land, try to get someone else to figure out how to do the work. The Relay will forward mail sent to “user@host.UUCP” to a host which can generally figure out a path.
2)	STAY ON KEY. Try to gather together all information having to do with a single network. That is, keep all “!’”s together, all “%’”s together, and please, for the sake of Mr. Protocol’s digestion, and that of all mailers along the way, try to use only ONE “@” sign.
3)	BE CURIOUS. When in doubt, ask the CIC. The wizards here have been constructing address symphonies for some time, and have some ideas as to what works and what doesn’t

When domain routing becomes real, all of this external ugliness will
disappear, and be replaced by internal ugliness, hidden from the
user. While this notion often does not work terribly well in society
at large, it is a genuine relief in mail systems. Of course, this
means the Death of an Art Form, but it was a pretty noisy art form, at
that.
