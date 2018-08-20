# Power Surge
### Related service provider: MegaBus  
## Background:
Back in 2015, I was returning to Atlanta after visiting my family near Washington D.C.  
I did not want to drive almost 10 hours one way, so I left my car in Atlanta and was riding a bus for the round trip.  

MegaBus was one of a few options I had at the time.  
I could not really schedule ahead of the trip to book a flight,  
and other buses simply made trip longer by requiring a transfer or were red eye trips in inconvenient departure time.  

However, that trip ended up to be a nightmare.  
All I do when I ride for such long hours is either sleeping or use smartphone/tablet to kill time.  
Thus, an extra method to charge devices was important to me.  
Many bus services including MegaBus offer power outlets like this in many seats.  
  <img src="http://perceptivetravel.com/blog/wp-content/Megabus-seat-plug-640x358.jpg" alt="alt text" width="320" height="240">  
image source : http://perceptivetravel.com/blog/wp-content/Megabus-seat-plug-640x358.jpg

I was plugging this usb wall adapter to charge my devices.
https://www.amazon.com/gp/product/B00NA9JQLM

When the bus was probably about three or four hours left to Atlanta,  
I noticed there was a small spark has flashed around my cell phone connector, shutting the cell off.  
I was astonished, quickly detached the connector from my devices.  
Fortunately, the phone was still alive, worked fine after a boot up, but the adapter no longer worked  
and the metal pin portion of the connector cable was burnt like this.  
  <img src="https://o2uk.i.lithium.com/t5/image/serverpage/image-id/12218i17CA8A3321E8589E/image-size/original?v=mpbl-1&px=-1" alt="alt text" width="320" height="240">  
image source : https://o2uk.i.lithium.com/t5/image/serverpage/image-id/12218i17CA8A3321E8589E/image-size/original?v=mpbl-1&px=-1

Worse part was, the bus has been malfunctioning since after;  
speed of the bus was slow down to about 20 mph and A/C began not working.  
The bus driver tried another 2~30 minutes before declaring unable to drive.  
Eventually, the bus was side stopped at the highway for over two hours until MegaBus dispatched another bus.  

  <img src="https://github.com/na6an/GlitchReport/blob/master/img/mbus-advisory.PNG" alt="alt text" width="600" height="200">   
  <img src="https://github.com/na6an/GlitchReport/blob/master/img/mbus-ticket.PNG" alt="alt text" width="520" height="140">   

The original arrival time was 9:40 PM according to this receipt, but it was almost 3 AM when we arrived.  
A few days later, MegaBus has issued a full refund for the trip.

## Typical Vehicle Electrical System:
Now, I cannot go into too much detail because I’m just an automotive engineer interested in electronic devices,  
not really an electrical expert with EE degree or with technician certificate.  
The following diagram is just a rough schematic diagram to explain how electrical system in a vehicle is wired.   
This is not a formal circuit diagram and rather to describe simply what kind of components are wired together.  

Battery is always the starting place in a vehicle. (Indigo Blue)  
When the vehicle is turned off, it slowly discharges like every other battery does.  
That’s why you have to jump start the battery when a vehicle was parked for weeks and runs out of juice.  
When a vehicle is on, engine recharges the battery with its generator.  

As you can see, many different electrical subsystems are wired to the battery either in series or parallel.   
Of course, specific circuit design varies by vehicle models.  

One common thing about vehicle electrical system is the fuse box. (Green)  
Fuse box is simple where the fuses of a vehicle are located.  
A fuse is basically a shield that mitigates the electrical damage by shutting the electrical flow off.  
It helps repair by breaking itself and allowing fuse replacement as an easy repair.  
Without a fuse, a serious teardown is required to identify a source of damage.  

Obviously, not every car has a power outlet. (Orange)  
(Many cars provide electricity through a cigar lighter though)  
In this case, however, there is not just one but many outlets in the bus.


## Root Cause:
It is pretty clear power surge from shorted circuit was the likely cause of the bus breakdown.  
The surge probably fried up fuse or spark plug of the bus. Exact source of the surge, however, isn’t really clear.  

Perhaps, my adapter was responsible for the breakdown.  
In fact, there are some Amazon reviews say the adapter broke devices connected to it.  
Or maybe it was simply the bus failure - spark could be just a symptom.  
Or maybe someone else’s device could be the cause.  

Whatever the reason was, it’s likely the electrical system of the bus was not design protected against surge.  
More specifically, it probably failed balancing the power load.  
We simply don’t know how much power would be drawn by passengers or if any of devices has short.  
See following experiment for what happens if power load is imbalanced.  

[![IMAGE](http://img.youtube.com/vi/HsSlQnGCvdg/0.jpg)](https://youtu.be/HsSlQnGCvdg?t=1m)
