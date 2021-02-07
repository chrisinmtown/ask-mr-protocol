# ASK MR. PROTOCOL (#8a): Mr Protocol Answers His Mail

## November 1, 1984

From: Ms Charlotte Mooers

When Mike O’Brien announced that he intended to leave the CSNET CIC at the end of a one-year tour of duty, and return to California, we all wept — yet the first question on everyone’s lips was “But what happens to Mr. Protocol?”

Never fear! Mike may have left to pursue other professional interests at the Rand Corp. (and fled the wintry gales of Massachusetts), but Mr. Protocol’s benign and genteel savoir-faire remains to shed its beneficence over the turbulent hubbub of network message traffic.

To prove it, we have a communication from Mr. Protocol in this issue of CSNET-FORUM, and we plan to have many more to come. Mr. P writes privately that he is somewhat disturbed because he has not received many communications on his chosen subject recently. Show him that you care! Send messages to obrien@csnet-sh.arpa, or to his new alias, mr-protocol@csnet-sh.arpa.

Subject Addressing Potpourri

From: Mr Perry A. Caro

Dear Mr. Protocol,

A friend of mine is trying to figure out how to send mail to the University of Chicago from Xerox (and once he gets there, vice versa). He attempted to determine the address in the canonical way: that is, he called up a friend and asked her to send something to “Miller.pasa@Xerox.ARPA.”

Here is what he got back:
```
Return-Path: <@MIT-MULTICS.ARPA,@UChicago.MailnetX9.XES@UChicago>
Received: from MIT-MULTICS.ARPA by Xerox.ARPA ; 03 AUG 85 10:47:59 PDT Received: from UChicago.Mailnet by MIT-MULTICS.ARPA with Mailnet id <2669391549609110@MIT-MULTICS.ARPA>; 03 Aug 1985 13:39:09 edt Date: Sat, 3 Aug 85 08:49:54 CDT From: Ellen Seebacher <x9.xes@UChicago.ARPA>
To: Miller.pasa
```

Referring to the “Return-Path” I must confess that I have never seen anything quite so bizarre in the 7 years of my ARPA community membership (and I’ve received quite a few DECNET to ARPA to UUCP messages, believe you me!)

Could you explain this nonsense? Needless to say, when my friend tries to reply to that message, his mail reading program barfs on the return path as if it were so much bicarbonate of soda. I am curious as to the etymology of that return-path, and I’m sure that my friend will be grateful if you could give him some idea as to how he can get mail to UChicago.

Thanks in advance.

Perry A. Caro

PS: Love your column in the CSNET-Digest! Keep up the good work.

Subject: Re: Addressing Potpourri

From: Mr Chris Miller

I don’t know if it will be any help to the general disection here, but the only address that I have been able to use successfully in getting a message from here in Pasadena to (here in Chicago is:

    ihnp4! gargoyle! sphinx! see 1 @ topaz.arpa

Furthermore, the net gurus here (such as they are.) assure me that this is a UUCP address.

So, does anybody have any idea how I can go about sending a message to X.pasa@ Xerox. ARP A once I get to Chicago, or should I just go there and try?
—Chris

Subject* Re: Addressing Potpourri

From: Mr. Protocol

<Ahem> Mr. Protocol apologizes for not having answered your query earlier, but he has been busy driving across the country for the entire month of August, to his new job here at the Rand Corporation. Although he is no longer associated with the CSNET CIC, he will continue to write his column for the Forum, so long as the thoughtful souls at the CIC continue to send him his regular diet of fine wine, brie, and chocolate chip cookies.

In answer to your question, that return-path is complex but pseudo-legal, and your mailer ought to be able to handle it However, it is, by the strict letter of the law, not your mailer’s fault if it can’L Here is the “Return-Path” line again, for reference:

    Return-Path: <@MIT-MULTICS.ARPA,@UChicago.MailnetX9.XES@UChicago>

This is a “source-routed” address, which means that it’s really supposed to go to “X9.XES@UChicago”, but is supposed to go through, first “MIT-MULTICS.ARPA” and then “UChicago.Mailnet” to get there. The fly in the ointment is that according to the strict principles of RFC 822 addressing, all hosts named in source-routed addresses are supposed to be Internet addresses. Well, UChicago isn’t It’s on Mailnet (another government-supported network brought to you by your friendly local federal government). All Internet mail to Mailnet goes through MIT-MULTICS.ARPA. That’s the mailnet gateway. Your host is supposed to open a connection to MIT - MUL TICS .ARPA and send that magic cookie of an address to the SMTP server there. It can unwind it and send the message on its way through Mailnet

What good, you may ask, is source-routed addressing if RFC 822 says that only Internet hosts are supposed to be listed? To which Mr. Protocol responds: What good, indeed? Not much. That’s why RFC 822 is roundly violated in this respect It’s the only reasonable way to do business. Mr. Protocol turns a blind eye to such violations, and asks if there are any more cookies left.
