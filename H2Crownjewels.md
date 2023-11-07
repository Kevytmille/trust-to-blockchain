
## X)

The current world has evolved beyond the simple intrusion detection of a firewall and anti-virus. The modern attacks are sophisticated and social engineered attacks that conventional “yes/no” roadblocks are not able to stop in time.
The kill chain is divided into seven categories:

•	Reconnaissance

•	Weaponization

•	Delivery

•	Exploitation

•	Installation

•	Command and Control (C2)

•	Actions on Objectives

The idea of the kill chain is that before the attacker would be able to actually achieve its mission (or objectives) it would need to go through steps 1-6 first. Thus if you are able to stop the attack at any point before, you can successfully stop the attack before it happens. (https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)

I see this as perfectly clear way of thinking about it, if it’s a day0 vulnerability there is no single system that can stop the attack before it happens. However if you can increase the security profile of the entire company, the chance that the attack will get all the way to step 7 is lowered by a huge margin. This is simple training for user like “don’t open PDFs you are not expecting”, not having the users as admins on their own machines, maybe even have a deep discussion on what information is truly necessary to be public in the marketing materials. All these combined will hinder (or at least slow down) and attack before it can get to actually infect and control a computer in the internal network. 

## A)

The company is Kim’s Oy and it does high-quality socks that are so in-style right now that all the high profile people want to use them and so most of the worlds high profile people are found in the company CRM systems.

The Socks™ are honestly of poor quality and outsourced to a third-party supplier, plus they are a physical, but they are not important. What I mean is that they are not a digital asset that can be accessed remotely or hacked. However, the company’s main objective is to keep up the appearance of being the best and to keep the marketing boom(scam) running as long as possible.

Hence, the most important part of the company is its appearance to the public and the customers. The most obvious risk is therefore the loss of customer data, or that information of a possible data leak is made public.

The following risk-assessment is done in an internal meeting:
 Riskassesement.png

The risk-assessment reveals that even if it is very unlikely that all systems are down at the same time (Risk1, R1) it is a possible scenario with extremely severe consequences that needs to be taken seriously and a plan needs to be formulated immediately, one possible scenario is to separate all systems, either to different suppliers or otherwise block from a centralized access to stop any lateral movement between attackers.

The risks marked in yellow are of concern and needs to be have a proper reason for why they are allowed to exists and what is done the make sure they do not come to pass. They are also marked to be reviewed individually to make sure that the risk-assessment is identified correctly.

The risk marked with green (risk5, R5) is an acceptable risk that is notified it exists but at this point does not need a contingency plan. It will be up in the next general risk-assessment meeting next year but will be forgotten for the mean time.

The risk-assessment meetings should take place annually at least once, and the severe risks have their own individual task-force that will allocate resources to assess and work on mitigating the risk of happening.

## B)

I chose Intrusion attempt 3 from the Hutchins et al 2011 paper found here: https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf

Following the kill chain diagram, the intrusion had already gone through phases, Reconnaissance and Weaponization and the kill-chain was stopped at Delivery. The target they attempted to exploit was know and had been sent a personal E-mail to from within the company. The method of starting the intrusion was a 0day exploit found in PowerPoint. However, the evil people made a mistake and used the same downstream IP-address to connect to the internal webmail service the e-mail containing the PowerPoint was sent from. This allowed the intrusion detection team to intercept and stop the malicious PowerPoint file from ever doing any harm. On the even worse side for the people with malicious intent, the PowerPoint was now being analyzed and they were able to discover the 0day exploit within it without it ever got a chance of being used against them.

