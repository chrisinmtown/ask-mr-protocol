# ASK MR. PROTOCOL (#2)

## November 21, 1984

Q: What was that awful problem with the WISCVM gateway talking to the CSNET Relay?

A: Mr. Protocol is genuinely fond of this question. It is a sterling
illustration of the necessity of adhering to protocol in all things.

In the SMTP mail exchange protocol (which was shamelessly based on the
old NCP FTP protocol), there is a provision to allow the reply codes
(which are rarely seen by the user) to extend over several lines. For
a single-line reply, the format is: “three-digit number, followed by a
space, followed by text of reply”, (for example, “504 text of
reply”). For a multi-line reply, the single space is replaced by a
hyphen on all lines but the last one. Mr. Protocol calls particular
attention to the fact that the format of a continuation reply line is:
“three-digit number, hyphen, text of reply”, (for example, “504-text
of reply”) and NOT “three-digit number, space, hyphen, text of reply”,
(for example, “504 -text of reply”).

Mr. Protocol has a long memory (a necessity in his calling) and
remembers that in the days of “iron men and wooden wires”, there were
at least one, and possibly several, important sites which believed
that either form of continuation was acceptable, no matter what the
protocol said. Mr. Protocol was horrified but there was little he
could do. Consequently, he allowed a mailer (it was an FTP mailer in
those days) to be installed which would accept either form. This was
perfectly correct: Mr. Protocol’s genteel watchword is: “Accept
anything from anyone, but send only what is correct”

[N.B.: Mr. Protocol is aware of the pragmatic attitude evinced by the
phrase “important site.” If one receives many messages which break
one’s mail service, one is more likely to fix one’s server than if
such messages are rarely received. Consequently “important site” is
often defined to mean “A site which it behooves us to talk to
correctly, lest our mail service break.” Mr. Protocol believes, of
course, that one should speak correctly to everyone, but he also
believes that a sense of priorities is not out of place.]

Many years later, the WISCVM gateway was created, with a whole new set
of software. And, strictly according to protocol, they sent out a
reply line (in the event of mail failure) which was of the form:
three-digit number, space, hyphen, text of reply. This was NOT a
continuation line and was perfectly legal. The SMTP mailer on CSNET
-RELAY, however, was still being overly forgiving and believed that it
WAS a continuation line, and sat around idly waiting for the rest of
the reply. Situation: deadlock. Mr. Protocol cried into his tea and
caused the mailer to be fixed. It is now less forgiving, but also
adheres strictly to protocol. Mr. Protocol feels sad but virtuous, and
the mail flows once more.
