If you run Containers on Docker and you need them to have static IPs one way (there are maybe others) is to put them on a MACVLAN.

The fix to where I got stuck (and you might be too!):

-> Set up the MACVLAN. Note: the IP range doesn't need to be within the DHCP of the router. 

**The Vital Second Step!**

You need to create a **second network**. I can't pretend to understand why but .. you need to do this.

- Add network
- It's a macvlan again
-
But this time the 'Creation' button isn't grayed out!

![[system/images/image.png]]

The first macvlan goes as the network in config:
![[system/images/image-1.png]]

Finally turn on enable manual container attachment also:

![[system/images/image-2.png]]

Create this network.

And THIS network is the one you add the containers to!