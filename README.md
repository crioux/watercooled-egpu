
# Watercooled eGPU for Thunderbolt 3 / OSX
---------------------------------------------------

![EGPU](https://github.com/crioux/watercooled-egpu/blob/master/pics/egpu1.jpg)


### Prices listed below are from February 23rd, 2019.


## 3D Printed Parts:

You will need to print:
 * 3x frontleg.stl
 * 1x front.stl
 * 1x Middle.stl
 * 1x BackClip.stl
 * 1x LockNut.stl
			
**Hardware:**
 * 8x 6-32x3/8" screws to mount the radiator
 * 2x M4x16 hex head bolts + 2x M4 hex nuts to mount the front legs
 * 1x M4x20 hex head bolt + 1x M4 hex nut to mount the back leg
 * 4x M4x8 hex head bolt to mount the pump/reservoir to the back clip
 * 2x M4x14 hex head bolt + 2x M4 hex nuts to affix the back clip to the middle section

Parts List
----------

**Razer Core X eGPU Case:**  
https://www.razer.com/gaming-laptops/razer-core-x  
https://www.amazon.com/Razer-Core-Thunderbolt-External-Enclosure/dp/B07CQG2K5K  
$299.99  


**MSI RX Vega 64 AIR Boost 8G OC:**  
https://www.amazon.com/MSI-RX-64-AIR-8G/dp/B07DH7S1X1  
$679.99  

**Watercooling Equipment:**  
https://www.ekwb.com  		

| Item                                    | QTY | Price   | Total   |
| --------------------------------------- | --- | ------- | ------- |
| EK-FC Radeon Vega RGB - Nickel          |	1	  | $154.99 | $154.99 |
| EK-KIT L240 (R2.0)                      |	1	  | $279.99 | $279.99 |
| EK-AF Angled 2×45° G1/4 Black           | 4   | $9.99   | $39.96  |
| EK-AF Pass-Through G1/4 - Black         | 2   | $7.99   | $15.98  |
| EK-AF Angled 90° G1/4 Nickel            | 2   | $8.99   | $17.98  |
| EK-ACF Fitting 10/16mm - Nickel         | 4	  | $6.99   | $27.96  |
| EK-AF Extender Rotary M-F G1/4 - Nickel	| 2		|	$5.99		| $11.98  |
| Total                                   |     |         |	$548.84 |
														
**5x 4 Pin Fan Extension Cables:**  
https://smile.amazon.com/gp/product/B01FFFHDKO  
$5.31  

**Lamptron PCI Bracket 4-Way High Power Fan Controller, Black:**  
https://smile.amazon.com/gp/product/B073C5CHXX  
$39.99  

**PCI Express Power Splitter Cable 8-pin to 2x 6+2-pin (6-pin/8-pin) 18 AWG:**  
https://www.amazon.com/JacobsParts-Express-Power-Splitter-Cable/dp/B07611QXG4  
$3.95  

### Grand Total: $1528.82

---------------------

## DISCLAIMER - DISCLAIMER - DISCLAIMER - DISCLAIMER - DISCLAIMER

This is $1528.82 of *BUILD AT YOUR OWN RISK* hacking.  

Read all instructions before attempting. I am not responsible if you screw everything up.  
Even if you read these instructions, they might be wrong. Use your good judgement.  
If something is wrong in the instructions here, feel free to file a bug report and i'll fix them if I get around to it.  
To that end, make sure you check the repo for bug reports first as well, since I might not have fixed something that someone else did.  

**Never do any of this assembly or with the power cable plugged in.**
-----------------------------------------------------------------

## Instructions

## Water Block

Follow the instructions on the EK-FC Radeon Vega water block, and make sure you swap out the back slot panel with their substitute 1-slot-wide panel that comes with the waterblock.
You'll want the extra room for the fan controller card.

![Slot Panel](https://github.com/crioux/watercooled-egpu/blob/master/pics/slotpanel.jpg)

# Case Prep
Before doing anything, first remove the stock fan from the Core X case, you won't be needing it.
Note that the fan connector (3 pin) can not be used to power the pump and fans because it won't source enough current. You'll need to tap the PCIE 12V to get that. More on that later.

You probably want to lay a towel over the electronics to catch wayward particles before attempting any drilling.
You'll want to make sure you take good care not to get a bunch of tiny metal particles into the circuitry or power supply. Your level of caution here is your business.

Then, drill the two holes in the back for the Pass-Through G1/4 connectors. See the pictures to see where I did it.
Then, drill or dremel a notch in the same back panel in the top-middle area where the fan cables can sneak through. You may want to avoid notching through to the edge
of the back panel, because doing so will make the case harder to close as the fit is reasonably tight.

Insert the GPU card and before hooking it all up, note that there is no proper hole for the 1-slot-wide EK-FC panel to screw into the case, as this case expects only a dual-slot wide panel.
Now would be a good time to mark where the hole should go, remove the card, and drill it to fit a thumbscrew (not provided, find one someplace).

# 3D Printing

3D print and assemble the mounting system. Captive hex nuts are used to mount many of the screws, fit them in gently. 
I printed everything with black PETG. You might want to use more than 20% infill, as I managed to snap one of the back legs when assembling the unit. Ensure you slice with supports. Screw everything together for the mount.

![Mount Assembly](https://github.com/crioux/watercooled-egpu/blob/master/pics/mount-assembly.png)

Attach the fans to the radiator, such that the cables exit the fan closest to the back of the unit. Attach the radiator and pump/reservoir to the mount. Adjust the lock nut so the mount fits tightly onto the top of the outer shell and the legs grip the edge in their notch. The EKWB hose they provide is very stiff and will likely want to apply pressure and push the mount off the top of the case unless you clip it well.

![EGPU](https://github.com/crioux/watercooled-egpu/blob/master/pics/egpu4.jpg)

Before you assemble the watercooling loop, make sure you leak-test all the angled/swivel/rotary adapters. They are notorious for leaking after you've already assembled the whole thing and filling it.

You can test them by plugging one end with a finger, filling it with water, and then applying pressure to the other end with another finger. Squeeze tightly, and if you see any water beading out of the swivel joint, throw the thing away or ask for a refund, because the o-ring is probably torn on the inside.

Insert the GPU card and assemble the loop. Do not fill anything with coolant until it's completely put together and tightened. How you route your hoses and the length of the hoses is up to you and your style. Error a little bit on the 'longer' side, though, since shorter hoses will be less flexible. This thing already looks like a monster, so don't skimp on the hoses.

Insert one of the PCIE power splitters between the Core X power supply and the graphics card, so you can power the fan controller and LED driver box.

You will need to build one cable as a 12V power tap:  
 * One end is IDE POWER MOLEX 4 PIN FEMALE 
   (you can chop one of these: https://www.amazon.com/Aiyide-Computer-Molex-Supply-Extension/dp/B07DMTT8G5) 
 * One end is PCIE 8 PIN FEMALE  
   (you bought two of these, chop one of them: https://www.amazon.com/JacobsParts-Express-Power-Splitter-Cable/dp/B07611QXG4)  

You only need to connect the 12V pin on the 4 pin connector and its adjacent ground to one 12V+GND pair on the PCEI cable.  

![Power Split](https://github.com/crioux/watercooled-egpu/blob/master/pics/powersplit.jpg)

Insert the fan controller card and secure it with a thumbscrew. Power the fan controller and LED driver box. Plug the cable for the waterblock's RGB lighting into the LED driver box.

![Fan Cabling](https://github.com/crioux/watercooled-egpu/blob/master/pics/fancabling.jpg)

Now, fill the loop from the reservior, using the liter bottle filled with water and the coolant concentrate that came with the kit. You will want to use the pump testing power cable adapter that came with the kit rather than trying to power on the whole unit to power the pump. 

First off you don't want to have insufficient water in the loop or you might harm your GPU. Also, you will have turn on and off the power multiple times while filling the reservior, because it will pump into the unit, and then be empty, and you will then need to add more fluid. You might want to replace the cap each time on the top of the reservior before turning the pump back on to minimize splashing.

Once it's totally full, you can seal it all back up and rotate things around a bit to get the air bubbles to travel out of the water block and back up to the reservoir.
	
Adjust fans to desired speed, ensuring they are sufficiently powered to cool your typical GPU load.

**Ensure the power to the pump is at 100%. The pump does not like being underpowered.**

Some cable ties and mesh wire sleeves help with aesthetics.

Also, do not freak out if you turn the power on on the case and nothing happens. The USB-C Thunderbolt 3 cable must be attached to your powered-on computer before the onboard circuitry will bother turning on the card and the pump power.

![EGPU](https://github.com/crioux/watercooled-egpu/blob/master/pics/egpu3.jpg) ![EGPU](https://github.com/crioux/watercooled-egpu/blob/master/pics/egpu2.jpg)



	

