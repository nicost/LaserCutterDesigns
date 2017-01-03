#Box with 3 BNC inputs and 1 output, logical OR.

##Purpose
Microscope equipment can be synchronized using TTL signals.  These are 3.3 or 5.0 V signals that most often travel through BNC cables.  We often use the camera as the "master", with the camera TTL signaling that the camera is exposing.  Modern microscope systems often contain more than one camera, and we need to combine the TTL signal from those multiple cameras.  If you connect the BNC cables coming from multiple cameras, then the "high" from one camera is pulled down by the other camera(s), so that no signal ever reaches the peripheral equipment.  To get around that, you need a small circuit that performs a logical "OR".

##Implementation
This design is inspired by [Kurt Thorn's blog post](http://nic.ucsf.edu/blog/2016/03/triggering-a-device-from-multiple-cameras/#more-1668) using the 74HCY4075 triple 3-input OR gate.  It puts this chip in a box, powered by a micro-USB cable, and has LEDs that signal power, as well as input and output signals.

##Parts List
- 3.0 mm thick acrylic (for instance: [McMaster-Carr](https://www.mcmaster.com/#standard-plastic-sheets/=15ljyhm))
- 1 Adafruit Perma-Proto board (the design works with either the [1/2 size](http://www.digikey.com/products/en?mpart=571&v=1528) or [1/4 size boards](http://www.digikey.com/products/en?mpart=589&v=1528)) 
- 1 [74HC4075 in a DIP packaging](http://www.digikey.com/products/en?keywords=1026-M74HC4075B1R)
- 1 [14 position DIP socket](http://www.digikey.com/product-detail/en/assmann-wsw-components/A-14-LC-TT/AE9989-ND/821743)
- 2 [hex standoffs, 3/16'' x 1/2''](https://www.mcmaster.com/#92319A873), or [cheaper but thicker](http://www.digikey.com/product-detail/en/keystone-electronics/1902C/36-1902C-ND/61868)
- 4 [Push-In Bumpers 1/4''](https://www.mcmaster.com/#catalog/122/3844/=15lk4kl)
- 4 ~ 5k resistors
- 1 [Micro-USB connector on a PCB board](https://www.sparkfun.com/products/12035) 
- 4 [BNC connectors](http://www.digikey.com/products/en?keywords=5-1634523-1) 
- 4 [Red LEDs in square package, WP934CB/ID](http://www.digikey.com/product-detail/en/kingbright/WP934CB-ID/754-1298-ND/1747697)
- 1 [5mm round Green LED](https://www.sparkfun.com/products/9881)
- Various wires

##Assembly
See accompanying Photo.  Note that the LEDs are all optional (if you do not want to use them, you can delete the wholes in the design).  However, if you omit the LEDs at the input side, then ground the pull-down resistors at the input.


Nico Stuurman, Dec. 2016