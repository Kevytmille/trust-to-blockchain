# X)

I watched the IEC62443-4-2-wtf? Operational Technology Device Security by Lauri Paatero : https://www.youtube.com/watch?v=0XZkEJLzCuc
I am in the industrial sector, so i kinda had a feeling of what he will talk about
The industrial devices are widely un-secure, there has previously NOT been a unified security standard as the devices are typically not connected to the internet or they do not rely on outside connections to functions. 
Things like elevators, cranes, mining equipment etc.
However nowaday everything is connected and they pose a security risk if a possibility of outside tampering would be possible. 

## The different security levels are listed as:

  SL1 - Unintentional or accidental misuse  
  
  SL2 - Simple means with few resources, general skillss and low motivation  
  
  SL3 - Sophisticated means with moderate resources, IACS-Specific knowledge and moderate motivation  
  
  SL4 - Sophisticated means with extensive resources, IACS-specific knowledge and high motivation  


## There is also the problem of network zones, the different layers Lauri goes through are:

  Control (Analog proprietary)
  
  Field network (Fieldbus)
  
  Plant network
  
  IT-Network

  Now the control and field networks are highly insecure, as they are not designed with any protocals aking to TLS in mind. They are simple lines that moves the commands given to the machine. The plant network 
  is the isolated internal network within the industrial plant which might have some sort of security attached to it, and finally the IT-network which is a typical TCP/IP network with TLS and other securitys in place.
  If you are able to bypass the IT-network and the devices are connected you are able to access nearly everything. You might also be able to bypass the IT-network and attack the plant network directly for a much easier task
, however this might need some physical location access to be able to hack properly.

Lauri finished the report with a happy message that the industrial sector is catching up security wise, but culture is slow to change at it will take a long time before we can say that everything is truely "safe".

