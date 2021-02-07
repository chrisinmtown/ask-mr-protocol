# ASK MR. PROTOCOL (#3a)

## December 17 and 18, 1984

Q: (From Mr. Henry F. Turner)

Mr. Protocol points out with some disgust...

Indeed, Indeed. But exactly who left the detail work undone and is
there an available fix for it now? Someone out in netville is running
around with a “shar” program that prepends \”s to each line in the
archived file(s). Thus “blank” lines turn into message terminator
lines and pmdf-del chokes! Everytime message transfer is completed
with csnet-relay, pmdf-del is invoked to pass these messages to
sendmail. When these terminator lines are sent to sendmail, it
delivers the incomplete message and pmdf-del dies with a broken pipe
leaving other messages undelivered in the queue. If one of these
messages comes in on Friday night, by Monday morning there will have
been lots of duplicate incomplete messages sent to sendmail and lots
of undelivered messages stuck in the queue behind this
one. Suggestions?

I did put the ^U in our login script and it seems to have helped
some. Still, line quality leaves something to be desired and the
protocol does occasionally breakdown (timeout). When this happens,
pmdf-del is not invoked to deliver any successfully received mail and
it sits in the queue. When I notice this, I often run pmdf-del to get
it on to its destination. I have been noticing a lot of duplicate
messages lately though and I wonder if, when the connection breaks
down, does the software on your end know that some (and which)
messages WERE successfully delivered, or does it assume that
everything was lost and start the whole batch over again at the next
successful connection? I know that some message duplication is due to
problems unrelated to csnet but I did get 3 duplicate messages from
Charlotte last week. Ideas on this?

A: Mr. Protocol, being the compulsive twit that he is, invariably
sleeps with a copy of the 4.2BSD manual set next to his bed (which is
where he should be, at this hour). He is therefore in a wonderful
position to point out that in Appendix B of the “Sendmail Installation
and Operation Guide”, it mentions the little-known option “i”, to
“ignore dots in incoming messages.” Few people realize that this is
not in the standard configuration file, because “sendmail” is used as
an SMTP server at those places with Ethernet and/or Internet
connections, “pmdf-del” ought to call “sendmail” with a “-oi” flag. In
the next release, Mr. Protocol hastens to assure you, it will do
so. Meanwhile, you should make this change yourself. If you have no
TCP-based local nets, just put “Oi” somewhere in your “sendmail.cf'
file; that will take care of the matter with no necessity for code
changes. If on the other hand you do run “sendmail” as an SMTP server,
then you’ll have to change the PMDF interface to “sendmail” to put in
a “-oi” flag.

As for your other problem, our MMDF system dequeues messages one at a
time, as your site indicates that it has- received the message. So,
broken phone calls will not cause repeat messages. If you’ve been
getting repeats Of messages from Charlotte, we’d love to know why. And
yes, if the call terminates prematurely, you’ll have to take other
actions to ensure that the mail gets posted. Running “pmdf-del” from
“/etc/crontab” some hours after you call us to pick up any queued mail
is probably not such a bad idea.
