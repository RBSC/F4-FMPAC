F4/FMPAC Combo Board version 1.4
Copyright (c) 2016-2019 RBSC
Portions (c) Kamil Karimov


Connection to the mainboard
---------------------------

The board requires a few wires to be connected to the MSX mainboard. The +12v and -12v are required for the FM chip and the
amplifier and must be connected to the JP1 connector. Also the GND (ground) must be connected to JP1, especially if the SJ3
solder jumper stays open. Those voltages and ground can be taken from the side slot of Yamaha MSX2 computers (YIS503, CX5M2
or CX7). On other computers those voltages could be taken from one of the slots or from the power supply's connection to the
mainboard.

The CE pin of the JP2 connector must be connected to the available STLSEL signal. On Yamaha MSX2 computers this could be taken
from the front slot (3.1). On other computers any unused slot signal could be used. The OE pin must be connected to CS1 signal
of the selected slot. However, in case of 27C512 EPROM installation, this pin must be connected to RD signal.


Audio connections
-----------------

The board has 2 different mono audio outputs marked as AMP and SLT. The AMP pin of JP3 must be only connected to the mixer point
of the internal amplifier, where all other SNDIN pins of cartridge slots are connected to. The AMP circuit already contains the
necessary resistor and capacitor and can be directly connected to the amplifier's input. To avoid interference from the other
components it's recommended to use the shielded wire. The shield should be connected to the GND pin of JP3.

The SLT pin of JP3 must be only connected to pin 49 (SNDIN) of any cartridge slot. On Yamaha MSX2 YIS503 and similar computers
the best place to connect the SLT pin is pin 59 on the side slot. Please be careful when connecting the wires - if not sure -
measure the voltages before connecting the wires. In correct connection could result in a damage for the board!


BIOS versions
-------------

The EPROM of the board contains 2 different FMPAC BIOSes. One is for external FMPAC (cartridge), the other is for internal FMPAC
(built-in into MSX2+). The BIOS is selected by JP4 jumper. It is recommended to use the internal FMPAC BIOS with the board. For
this option the jumper should not be installed.

Please pay special attention on the configuration notes on the board for solder jumpers SJ1 and SJ2! Those jumpers must be
configured correctly depending on the used EPROM chip. Otherwise FMPAC's BIOS will not work and there will be no FM music and
sounds in Basic as well as in certain games that detect the BIOS.


Notes
-----

The solderable jumper SJ3 is used to separate digital and analogue grounds. The board works fine without this jumper as long as
you connect the GND wire to JP1. The SJ3 should be only soldered if you don't connect GND to the board. But if you hear any
digital interference in the audio channel after you bridged the SJ3 jumper, please remove the bridge and connect GND wire to JP1.

The F4 Register part of the board is optional. It is only needed when the board is being installed into a computer that is converted
to MSX2+. Normal MSX1 or MSX2 computers don't need F4 port.

This FMPAC board does not support writing anything to SRAM (there's no SRAM on board). Also this device only provides mono sounds
and music. Stereo is not available.

Please note that the provided FMPAC BIOS image doesn't contain the UI (user interface). The full version of the FMPAC BIOS is
available in the RBSC's Carnivore2 cartridge. The BIOS is even translated into English.


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided information,
software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small amount of bare boards for
personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the copyright!


Contact information
-------------------

The members of RBSC group Ptero, Wierzbowsky, Tnt23, Pencioner and DJS3000 can be contacted via the MSX.ORG or ZX-PK.RU forums. Just
send a personal message and state your business.

The RBSC repository can be found here:

https://github.com/rbsc


-= ! MSX FOREVER ! =-
