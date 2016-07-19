# Overview

The [Ognite Flameless Digital Candle](http://ognite.com/) is an original project by Josh Levin. It displays a realistic flame animation on its LED matrix and is also an exercise in minimalism: The only components are an AVR microcontroller, 40 LEDs, and a rather ingenious laser-cut cardboard construction that not only acts as the box that the components come in but also holds the assembled circuit and batteries in place.

Unfortunately, the project seems to be dead and I do not have access to a laser cutter either so I decided to make a PCB. And since I was breaking with the minimalism theme anyway I also added an on/off switch.

The `.sch` and `.brd` files are in [EAGLE 7](http://www.cadsoftusa.com/download-eagle/eagle-freeware/) format and compatible with the freeware version.

# Bill of materials

| Qty | Component | Notes | Farnell item# |
| --- | --- | --- | --- |
| 1 | Ognite Clone PCB | Can be ordered at [Dirty PCBs](http://dirtypcbs.com/view.php?share=20653&accesskey=263dad38d5838c2409e7b28eb41107fe) |
| 40 | 3mm Amber LED | A lot of brightness is lost due to the matrix switching so go with some super bright ones! | 1581166 |
| 1 | ATtiny4313-PU | With [Ognite firmware](https://github.com/cyraxx/ognite-firmware/) | 1841620 |
| 1 | DIP-20 socket | Technically optional if you are very certain that you will never have to re-flash the chip... | 1103848 |
| 1 | 3x AAA battery box | | 1650688 |
| 1 | SPDT slide switch | Pretty much any model with ~4.6-4.8 mm pin distance should fit | 807527 |

# Assembly notes

The flat side of the LED outline on the silkscreen denotes the cathode, i.e. the shorter lead.

The switch is meant to be mounted on the back of the PCB but since it's symmetrical it can also go on the front.

The assembled PCB can be mounted on top of the battery box with some hot glue like so:

![Assmbled Ognite PCB and battery box](assembled.jpg?raw=true)

# Gerber files

Gerber files created to [Dirty PCBs](http://dirtypcbs.com/) specifications are included in the `gerbers` directory. If you create your own Gerber or other export from EAGLE it is recommended that you include the `tDocu` layer in the silkscreen as it contains the LED orientation.
