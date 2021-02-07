# ASK MR. PROTOCOL (#4a)

## February 12, 1985

Q: (From Mr Peter Vanderbilt). Please comment on the use of route
addresses as defined in RFC 822. Why did you not advocate them in your
article? For example,

    princeton! honey! down%purdue@csnet-relay.ARPA

could be phrased as

    <@csnet-relay.arpa, @purdue.csnet, @princeton.uucp: down@ honey. uucp>

if I understand 822 correctly. It may not be a great work of art but
at least it’s unambiguous.

Is the problem that many hosts cannot handle source routes? In this
case, can purdue.csnet invoke the uucp mailer with the appropriate
address (princeton!honey!down)? If so, please send me a copy of their
sendmaiLcf, especially if they could generate a working return address
(from honey .uucp)...

A: ... The answer to your ... question, as you have guessed, is that
there are many hosts which do not understand source-routed 822
addresses. In fact, in the UUCP world, there are many hosts which do
not understand any sort of RFC 822 message at all. Sending a message
to UUCP-land means assuming that one or more links along the way will
not understand any metacharacters other than ’!’.

As for the problem of constructing correct return addresses, this is a
non-trivial problem, mostly solved on an ad hoc basis. I don’t know
what Purdue uses in their ”sendmail.cf” file, and picked that
particular example from Peter Honeyman’s paper (since he was kind
enough to use an address that we had generated). In future I plan to
construct a library of “correct” sendmail.cf files for distribution as
samples to the membership; I’ll try to include one from Purdue at that
time. In the meantime, I suggest you contact “postmaster@purdue.arpa”
yourself if you are really eager for a sample of their file.

Comment: (From Mr Charles Hedrick). The reason why no one uses

    @a,@b:c@d

is that it doesn’t accomplish anything. Host names a, b, and d must
all be valid Internet host names. Thus this form cannot be used to
express routes involving UUCP hosts. Since all Internet hosts can talk
to each other directly anyway, this means that the syntax is of
dubious usefulness. Most sites will optimize routes by delivering
directly to the final destination. (That is, they don’t implement
source routing.)

There was considerable discussion within the Internet community when
this ruling was first made. Many of us felt that it was helpful to
have a syntax to express routes to non-Intemet sites, and advocated
that any syntactically valid host name should be allowed. I am not
clear why the restriction was imposed.
