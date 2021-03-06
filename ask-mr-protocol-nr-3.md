# ASK MR. PROTOCOL (#3)

## December 7, 1984

Q: I tried to send my binary program to my friend and it never got
there. Instead I got a strong message from the CIC telling me not to
do that any more. What happened?

A: Mr. Protocol confidently looks forward to the day when one can put
absolutely anything this side of legality into a mail message with
complete confidence that it will arrive intact at the
destination. Unfortunately, 8-bit binary code in CSNET mail messages
enjoys the same popularity as rainbow trout in the Postal Service: it
packages well, but it gives the mail system fits along the way, and
arrives in less than prime condition, when it arrives at all.

The problem is (of course) one of protocol. The PhoneNet and SMTP
protocols specify that all characters in the message be from the
128-character ASCII set. Since they are sent in 8-bit bytes, there is
one bit left over. This bit must be zero and is not transmitted
intact. The protocols also specify that the length of a line is
limited. Currently, this limit is 510 characters for PhoneNet and 256
characters for SMTP on the Internet (Mr. Protocol realizes that the
SMTP specification calls for 1000-character lines. He is still waiting
for the More Perfect World to which he continually refers.) This means
that binary files, which have newline characters sprinkled at random,
are liable to cause gastric distress in MMDF due to long lines, as
well as having all the high-order bits turned off.

Protocols, of course, are designed to help, never to harm.
Consequently, people have designed ways to transmit real 8-bit
programs over 7-bit networks. This is done by encoding the binary data
using one of several schemes. The resulting messages consist entirely
of ASCII text with reasonable line lengths, but are encoded versions
of the real binary data being transmitted. On some UNIX systems,
“uuencode” and “uudecode” can be used; these programs were written at
Berkeley to facilitate just this sort of operation over UUCP mail,
which has the same sort of problem. There is another program, called
“binhex”, which seems to have found favor among those who are addicted
to the exchange of Macintosh software.

Mr. Protocol points out with some disgust that there is another
intrusion of protocol which can cause damage to perfectly legal mail
messages. The SMTP specification uses a line consisting of a single
period to terminate transmission of the text of a message. Any lines
in the message which already consist of a single '.' are to be changed
to and fixed at the far end. However, some network implementors prefer
to boldly paint the network canvas in sweeping strokes, and leave the
detail work to others. The result is that many mail systems will do
unfortunate things to lines consisting of a single period Such lines
will either have the period doubled, or will break the mail system, or
will cause the message to be truncated at that point. In general they
behave like rainbow trout. Consequently, though it is perfectly correct
to send a mail message with lines consisting solely of '.', Mr. Protocol
sadly admits that this is Tempting Fate, and is to be Avoided.
