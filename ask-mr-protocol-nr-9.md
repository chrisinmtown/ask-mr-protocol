# ASK MR. PROTOCOL (#9): Why It All Looks Ugly Sometimes

## December 6,1985

> Sometimes you win, and sometimes you lose, and sometimes you get rained out, but win, lose, or draw, it always pays to suit up.

> L. B.

> It’s alive! It’s alive!

> V. von F.

Sometimes people ask Mr. Protocol: *‘The CIC seems like such a bright bunch...why is there still evil in the world?”

Others load the MMDF tape and. after picking themselves up off the floor, say, “(*@#&$(*&@#$!!! FOO! That sucker’s BIG!”

Still others ask, “Where’s the restroom?” [“Around the comer.” Well, SOME questions are easy to answer!]

The question most of these are groping towards is, Mr. Protocol feels, best summed up as: “Why are mail systems so big, so ugly, so difficult to maintain, and so unreliable? Strange as UNIX is, these have to be the most frightening things in it!” Nothing can really excel without help from others: there are several contributing factors to the general ugliness of mail systems. Surprisingly, few or none of the current examples of mail systems started out badly. Let us take a few examples (we will combine mail transport and user interface programs here):

**MMDF:** “Hello there. I am made up of pieces. See this PhoneNet protocol here? Think of it as a mitochondrion: it came from somewhere else and used to have a life of its own. It has been grafted in and made to exist as part of me. Meanwhile, the rest of me is very well ordered and structured, at the expense of execution speed. Assignment of responsibility for a message within me is exact, and all of my channels are part of me. But do not ever, ever expect to get your machine back anytime soon after I start running, for I am huge and powerful, and I feed on cycles for breakfast!”

**MH:** “Remember the old days? Remember that message system called MS? It was huge. It was ugly. It was a first attempt. It did everything. It was HERMES for a PDP-11. It blew up regularly. I came along in a single weekend. I was small. I was fast I was a mammal among dinosaurs. See me now? I am a Megatherium. I became more and more huge and powerful, and I have outstripped the ability of processors to run me rapidly. But I can do anything! And I come in lots and lots of little pieces...imagine what I would be like if I were a single, huge system!”

**HERMES:** “I am a single, huge system. I am well-designed and I can REALLY do anything! Hark! What is that? Why, it is a lone, unguarded DECsystem-20. I am always hungry. I will eat this machine now. It will never be seen or heard from again.”

**MSG:** “I am the ghost of Christmas Past. I started out in Illinois in 1973. I have been at Rand, UCLA, UDel, BRL, and almost everywhere else you care to name. I am not all that large, but my code looks like nothing on Earth. I am three feet tall and green, and I have an indeterminate number of limbs.”

\*urf\* \*ugh\* \*\*SLAM!!\*\* There. Mr. Protocol has gotten rid of all the others. He thinks you’ve probably heard enough by now.

Why this state of affairs? Certainly one factor is the simple history of software evolution. Any sizable system that has been through as many hands as these have will have architectural flaws. But there is more at work. These systems have been chasing an evolving standard. Yes, the paper on which RFC 733 and RFC 822 were written doesn’t change, but the de facto standards must include those from outside “RFC-land.” These "foreign” standards cannot blend well, and a large part of the ugliness comes from being forced to make them live together.

In addition, mail systems are the peculiar point where human aesthetics most directly come in contact with a network. Other network services, such as TELNET and File Transfer Protocol, are really more or less invisible to the user. Mail messages, however, with their headers and all, generally are seen and processed by humans. Few mail user interfaces do more with these header elements than rearrange them, or delete the most arcane and useless. The result is that people want all sorts of services from their mail reader that they would never think of demanding from TELNET. (Not entirely true: see SUPDUP. But it never caught on.)

Finally, mail systems of necessity must implement their own store-and-forward queueing system. This makes no sense at all for TELNET, and File Transfer Protocol has no history: it either works or it dot n’t, but requests are not queued. Any queueing system is prone to breakage, and mail systems - written to be as paranoid as possible in an effort to prevent this. Automated paranoia makes for big programs.

Mr. Protocol once took a course in wild animal training. He learned how to saddle an elephant, and how to take a tiger for a walk. He never dreamed that what he learned there would be so directly applicable to his later work.