[![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/Anubis-EFL/Shaviry/blob/main/README.md)
# Shaviry

 Amiga Video to VGA adapter and Monitor Switcher with RGB amplifier all in one 

****Warning: This is not a scandoubler, your monitor must sync at 15Khz.****

About the name: Shaviry is our 15 year old beloved lovebird, I decided to give it her name as a tribute and find an (somewhat forced) acronym.
There is two options:

  1) ****SH****arp ****A****miga ****V****ideo ****I****nput switche****R**** s****Y****stem.
  2) ****SH****ort for ****A****miga ****V****ideo ****I****nput switche****R**** s****Y****stem.

I've made the tests with an AGA machine on a DELL SE2722HX with THS7374 and THS7376 RGB amplifiers.

With THS7374 the bars are slightly visible but the image is blurred, I think it is due the 9,5Mhz bandwidth of the filter.

With THS7376 the image is sharp and the bars a nearly invisible, I still notice them if I actively look for them. In normal use (games, demos...) most of the time I don't even notice them.


They can't bee seen in a photo of the screen (or almost), so I don't know if it's just me. Therefore, until I can do more tests, I would stick with the second option.

Anyway, here goes the typical photo. With THS7376 and active filter.

![Image Alt text](/imagenes/Amiga_boot_con_Shaviry.jpg "Boot Screen")

The adapter has jumpers to configure its operation in two ways:

1) As only VGA adapter in case you do not have a graphics card or pistorm (with HDMI to VGA adapter)
2) As an automatic input switch controlled by a 5v signal.


This signal can be sent by switchcontrol through the CIA or the parallel port. In the case of pistorm you can replace switchcontrol with the P96 driver option.

If you don't want to use those options you can always activate the switching by inserting a 5v signal controlling it with a switch, arduino or whatever you want.

The switching 5v signal is isolated with an optocoupler to avoid bad things.

There is also a solderable jumper where you can choose to turn on or off the filter, you must choose one option or the other, it should not be left floating. With the THS7376 it is best to leave it active.

The switching in a CRT monitor is instantaneous, although in an LCD it takes a little longer.

****Part list:****
 | Part | Value | Size | Qty|
 | --- | --- | --- | --- |
 | R1, R2, R3, R4, R5, R6 | 75r | 0603 | 6 |
 | R7 | 1k | 0603 | 1 |
 | R8 | 10k | 0603 | 1 |
 | C1 | 10nf | 0603 | 1 |
 | C2, C3, C4 | 100nf | 0603 | 3 |
 | FB1, FB2, FB3, FB4, FB5 | Ferrite bead | 0603 | 5 |
 | U1 | 74HCT14 | SO-14 | 1 |
 | U2 | SGM4717 | MSOP-10 | 1 |
 | U3 | THS7373/THS7374/THS7376 | TSSOP-14 | 1 |
 | U4 | SGM330A | SSOP-16 | 1 |
 | U5 | PC817/EL817 | DIP-4 SMD | 1 |
 | J1 | DB23 Female | For cable | 1 |
 | J2, J3 | DB15HD Female | For PCB 3,08mm | 2 |
 | J4 | 3x2 pin strip | 2,54mm | 1 |
 | Others | Jumpers | | 2 |
 
First of all, I would like to point out that I am simply an electronics hobbyist and this is my first project in KiCad, so there may be things done better.

My thanks to Alberto Benitez (Lince/EA4GGE) for his advice, without which I'd probably still be scratching my head about how to route the pcb.

## Revisions:

Revisions are named REV followed by the date in dd/mm/yyyy format


  ****REV19122023****

Initial revision. (Published on 31/12/2023)

 ****REV02012024****

Changed the amplifier inputs and outputs to make it fully compatible with the THS7373, 7HS7374 and THS7376.

 ****REV21012024****

Only a track rerouted. There is no change in functionality.

 ****REV23012024****

Removed all unconnected ground islands.


## Some images.

Shaviry with Shaviry
![Image Alt text](/imagenes/Shaviry_adapter_1.jpg "Shaviry with Shaviry")
Shaviry telling Shaviry who's boss.
![Image Alt text](/imagenes/Shaviry_adapter_2.jpg "Shaviry arguing with Shaviry")
Algunas Vistas:
![Image Alt text](/imagenes/Shaviry_adapter_3.jpg "Vista 1")
![Image Alt text](/imagenes/Shaviry_adapter_4.jpg "Vista 2")
![Image Alt text](/imagenes/Shaviry_adapter_5.jpg "Vista 3")
![Image Alt text](/imagenes/Shaviry_adapter_6.jpg "Vista 4")
![Image Alt text](/imagenes/Shaviry_adapter_7.jpg "Vista 5")

Next to the Commodore adapter. Yes, it is very dirty, but he has been plugged into my Amiga 4000 for more than 25 years and I haven't even noticed it.
![Image Alt text](/imagenes/Shaviry_adapter_8.jpg "Next to the Commodore adapter")

## Videos

On a LCD monitor (DELL SE2722HX)

https://github.com/Anubis-EFL/Shaviry/assets/154557850/1416b5dd-fce8-4823-900b-c1d1edef9626

On a CRT monitor (Microvitec 1438) the RTG is displaced because the hdmi mode of the pistorm32 is not fully adjusted.

https://github.com/Anubis-EFL/Shaviry/assets/154557850/919e8689-20b6-4c1b-af77-966b4a6acc1a

