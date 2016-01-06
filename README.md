# nanoWii
-----
This is a Circuit Board redesign for a NTSC C/RVL-CPU-40 Nintendo Wii Console with the intention of minimizing the size for a portable. The board design is done in the open source software Kicad.

A big thanks needs to be given to Dyxlesci of Modretro for his extensive research of different Wii revisions and bourd sourcing.

##Why?

Glad you asked! A portable video game console is just what it sounds like. It's taking an in home video game system and stripping it down to the bare minimum, wiring it to a screen, controller, and batteries, and building it into a custom case. It's a niche hobby with very popular and impressive outcomes if done correctly.

One of the more popular options for a portable is the Nintendo Gamecube. This is due to its small board size, low power consumption, and plethora of homebrew applications. 

This project takes the design one step further. The Nintendo Wii is nothing but a super Gamecube. The hardware and software architecture is extremely similar and allows Gamecube games to be played as well as Wii games. The main advantage is that with custom power regulation the Wii draws almost half the power as the Gamecube, while improving processing speed and increasing your game library.

The main disadvantage of the Wii is the board layout. While it can be trimmed, the board is still large and cumbersom due to the layout. And after only a small amount of trimming the components require major relocation and rewiring, which is not good in a portable environment and is prone to breaking. 

This project hopes to remedy that issue by creating a smaller Wii board with custom breakout pads for power, battery charging, and video output.
---
##Requirements

1. NTSC C/RVL-CPU-40 Nintendo Wii
2. DC/DC converter that can output 1.2v 4A and 3.3v 1.5A totalling just under 10 Watts
3. Reballing equipment for CPU/GPU/RAM
4. Soldering skills for all other components

This design requires an NTSC C/RVL-CPU-40 and the nanoWii PCB that can be fabricated using the provided files. Revision 40 of the Wii is preferred as it has the lowest power consumption while retaining gamecube support. Revision 60 is the same as the only change was DC/DC components and those will not be included on this board. Later revisions that did not include gamecube ports can be used but any gamecube connectors must be added, this includes the RVK-CPU-01 and RVK-CPU-02. The Wii Mini cannot and should not be used as most of the featues have been locked out. A custom regulator will need to be used such as the TI DC/DC standalone modules like the PTR08100w.

To ensure that you get an RVL-CPU-40 or RVL-CPU-60 Wii you can purchase a black a NTSC Wii with gamecube support. This appears to be exlusively Rev 40 and 60.
---
##FAQ

#####How much will this cost?
The actual hard ware requirements are relatively inexpensive thanks to how common a Wii is. A Black Wii with gamecube support can be purchased for $10-$30 depending on how frugal you are. The pcb is 4 layers and can be source from websites like PCBWAY.com for about $50 for 10 boards. Other options such as different solder masks and gold immersion will increase the price to nearly $100 for 10 boards. These options will most likely be desired due to the complex soldering. The rest of the cost will depend on your DC/DC conversion choice and what kind of reballing equipment you have access to or need to purchase.

#####What about the controller/wiimote requirement?
Thanks to auto booting to the homebrew channel and gamecube controllers a Wiimote is not required for most functionality. Other options such as data management and wi-fi setup may require a wiimote, but can be accessed through various homebrew.

#####Aren't the components difficult to solder?
Yes that is correct. Moving the Processor, GPU, and RAM is not for the faint of heart, as these components are ball grid array components and will most likely require a reballing station to resolder. Reballing kits are also available for the Wii that are relatively inexpensive. With the right heatgun you may be able to do this by hand. Other components such as the TSSOP NAND or MX chip can be easily transferred with little soldering background experience.

#####Doesn't that make this project impossible?
Nope! The biggest challenges of this project will be the board redesign, which I will be publishing for free. And once you get over the reballing transfer, which is pretty easy once you figure out the right temperature and timings, the board is done and ready to boot!
---
##Legality

This circuit board design is completely legal, in no way, shape, or form is any firmware or security features of the wii tampered with on this circuit board design. An original Wii is still required to obtain the main components for this circuit board, your rights to modify the hardware of that system comes with the ownership.
---
##License

######Copyright (c) 2016 bentomo

######All rights reserved.

######Redistribution and use in source and binary forms, with or without
######modification, are permitted provided that the following conditions are met:

######1. Redistributions of source code must retain the above copyright notice,
######   this list of conditions and the following disclaimer.
######2. Redistributions in binary form must reproduce the above copyright notice,
######   this list of conditions and the following disclaimer in the documentation
######   and/or other materials provided with the distribution.

######THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
######AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
######IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
######ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE
######LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
######CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
######SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
######INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
######CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
######ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF
######THE POSSIBILITY OF SUCH DAMAGE.
