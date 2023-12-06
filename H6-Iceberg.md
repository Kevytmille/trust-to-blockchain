## X) Basic Information:
•	Tor is a modified web browser for anonymous use that hides your IP address.
# History and Intended Use:
•	Created by the US government in 2002, Tor enables private online communication.
•	Used for both legal and illegal activities.
•	Ongoing development to keep it up to date and secure.
# How It Works:
•	Tor directs internet traffic through random relays, encrypting data for anonymity. The route changes every 10 minutes, making tracking Tor traffic very difficult. An analogy is mailing a letter through different people, each unwrapping only the outermost layer (probably where they got the idea for the onion logo) of encryption.
# Exit Node Reality:
•	Illustrates a case where someone running a Tor exit node was mistakenly raided for child pornography distribution. This highlights how innocent individuals operating exit nodes can be wrongly implicated due to Tor's anonymity due to people not understanding how Tor works.

# Tracking Criminals Using Tor:
•	Governments worldwide are working on deanonymizing Tor to find criminals or restrict citizens' internet access. Successes often result from exploiting suspects' errors rather than breaking Tor itself. 
Breaking Tor Possibility:
•	The FBI successfully took down a child pornography hosting service by exploiting a Firefox bug in Tor browsers. Tor's biggest weakness is the user; customization can leak information. 
For example, allowing location sharing or certain plugins can compromise anonymity. Various research methods aim to deanonymize Tor, such as attacking the network or controlling entry and exit nodes.
Identifying Tor Users:
•	Investigating Tor users requires significant resources that are outside the scope of Tor.
•	Methods rely on suspects' mistakes, such as customizing Tor settings or using additional non-Tor browsers. Victim-initiated strategies, like seeding e-mails with tracking codes, can reveal the true IP address of a Tor user.
Open-Source Investigation:
•	Identifying Tor users outside the network may be possible by using open-source and online investigative methods. Even minimal information about a suspect, like a username, can lead to more insights in the Dark Web.
Case Examples:
•	The Silk Road case shows how a suspect's mistake, using a personal email and real name, facilitated identification and a life sentence.
•	Internal corporate networks have an advantage in identifying Tor users, as network administrators can detect Tor usage.
Additional Examples:
•	A Harvard student using Tor for email bomb threats was caught when IT logs revealed his Tor access during the threat period.
•	Cases are often solved through suspects' mistakes, like inadvertently using a non-Tor browser, revealing their true IP address to victims.

## A)	TOR browser installation:

I tried following the guide listed here:
https://community.torproject.org/relay/setup/bridge/debian-ubuntu/ 
But I ran into several errors and had to resort to simply installing it on my windows device.
https://github.com/Kevytmille/trust-to-blockchain/blob/main/Tor1-error.PNG

So I downloaded the installer from: https://www.torproject.org/download/ and installed it with default settings. It works!


## B)	Browsing with Tor:
https://github.com/Kevytmille/trust-to-blockchain/blob/main/Tor-Browsing-1.PNG
Not sure what exaclty to try to find a bit overwhelmed here, but a quick search and we got drugs!
https://github.com/Kevytmille/trust-to-blockchain/blob/main/Tor-Browsing-2.PNG

I did not think of a forum I would like to visit on the darknet, and I was unable to find darknet site of a well-known company. DuckDuckGo gives me only “regular” pages when I tried a few companies I could think of.

# C)	Anonymity

Tor anonymity seems to work by obfuscating the start and end point of your connection. You are vulnerable to governmental reach of ISP and access point logs. But you are completely incognito in the actual browsing. 
If what you do on the internet does not have a real-world effect, it is most likely impossible to properly de-anonymize you. The encryption seems to be a some sort of signed hash encryption that is utilized in multiple layers when you go through all the nodes.

# D)	Threat models

I think tor is a bit “overblown” for normal internet use but as a privacy advocate myself, it seems like a necessary evil if at this point, even normal stuff now requires a true level of anonymity to escape advertisers. 
I would think the most beneficial point of Tor is for journalists and researchers who need to make some statement public without the fear of being tracked and killed for their opinion (in this case, they would still probably know who leaked the info maybe…?). 
