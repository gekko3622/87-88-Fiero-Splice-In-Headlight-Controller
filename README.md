# 1987-1988 Pontiac Fiero Headlight Motor Controller
**PCB Designed by Ryan Blanchard 4.2024**\
**Based On An Project by WalkerTexan** (See credits section for details and link)\
**FOR NON-COMMERCIAL USE ONLY.**

![image0](https://github.com/gekko3622/87-88-Fiero-Headlight-Controller/assets/166318874/afa2760a-d98e-4d06-80ae-5b2233025cc9)\
**Note:** This is my personal PCB, based on version 2.0. The files contained in this project are version 2.1.\
V2.1 is electrically identical. The only changes made were to reposition and enlarge some of the silkscreen label text for legibility.

## Intro
This project is a PCB implementation of WalkerTexan's "Fiero Headlight Controller".\
I started this 	project after getting frustrated with the cost and questionable reliability of used modules.\
While there are also new production versions of the original module available now, I found the cost to be way too high.

## Purpose and Origin
I started this project to replace the second failed module in my 87 Pontiac Fiero.\
It started as a basic DIY project and grew into a proper PCB design after my prototype proved to be reliable.

Pictured here is my original DIY prototype. The PCB version is night-and-day BEAUTIFUL compared to this thing.
![IMG_0994](https://github.com/gekko3622/87-88-Fiero-Headlight-Controller/assets/166318874/832f47c2-72c2-4619-88f2-a183105d53cd)
![image0(1)](https://github.com/gekko3622/87-88-Fiero-Headlight-Controller/assets/166318874/9cde2d03-9614-4fc4-8acb-887a5dca8696)


## Repository Contents
**1. Arduino Nano Program**
- WalkerTexan's code for the Arduino Nano.\
This MUST be programmed onto the Arduino for the module to function.

**2. Gerber Files (For Production)**
- These are the files that must be provided to a fabricator to produce a PCB.\
  **VERY IMPORTANT:** This PCB MUST be produced with 2 Oz copper weight in order to meet power handling requirements.\
  The provided gerber files will produce an electrically identical copy of the PCB installed in my own car.

  The provided Zip file can be directly submitted to a fabricator and contains all of the other individual files in this folder.
  

**3. KiCad Project Files**
- These are my original KiCad 8.0 project files.\
  You will need these if you intend to make any alterations to the PCB's design.

## Installation Location
This module is designed to be installed under the hood, in the area around the brake master cylinder.\
This allows for easier access and makes it possible to install without damaging the original connectors.\
NOTE: Installing this module will require you to cut and slice a new connector onto the original front wiring harness.

## Wiring Guide
You will need to provide two sets of waterproof automotive connectos for this project.\
For the sake of this writeup, I'll assume you have 5-pin and 4-pin connector sets.\
Connector/pin numbers are based on the labels printed on my version of the PCB (See image below).\
Wire colors give are for the wires contained in the factory wiring harness, which runs inside the frunk, driver side.\
If you make changes, you will need to determine your own wiring scheme.


![Screenshot 2024-04-11 233351](https://github.com/gekko3622/87-88-Fiero-Headlight-Controller/assets/166318874/fcdd3d95-4449-4d28-abfd-25a15d8cbd68)



**SAFETY WARNING: Please splice into the wiring harness after any fusible links. They are there for a reason.**

### To Wiring Harness
	
C1-1  -  Connect to red wire on harness. (there are two, both will be used)\
C1-2  -  Connect to ground. I recommend running a new ground wire. The harness contains MANY black ground wires.\
C1-3  -  Connect to white wire on harness.\
C1-4  -  Connect to other red wire on harness.\
C1-5  -  Connect to yellow wire on wiring harness.

### To Headlight Motors
		
C2-1  -  Light Green/Black\
C2-2  -  Gray/Black\
C2-3  -  Dark Green\
C2-4  -  Gray

**You may want to run new wires and connectors to the headlight motors to preserve original wiring.**

I used a generic equivalent of AC Delco PT724.\
The connector has notches cut into the plastic pin barrels. These do not match the notches on the headlight motor connector.\
I solved this problem by heating a knife with a lighter and cutting my own matching notches into the new connectors.

If you go this route, cut the new notches as indicated in red on this image:\
![IMG_0999](https://github.com/gekko3622/87-88-Fiero-Headlight-Controller/assets/166318874/2b60277c-8df9-4c41-be6a-6ab5698545a2)

## Component List
See BOM.xlsx for a full list of required components.

## Enclosure
The PCB is intended to be installed within a water-resistant project box.\
The specific box I used is this: https://www.amazon.com/dp/B075WZFWFV?th=1  
Any enclosure with space for a 170mm x 110mm PCB could be used, though mounting hole pattern should be considered.\
Keep in mind there needs to be some space for the wiring too.

![image1](https://github.com/gekko3622/87-88-Fiero-Headlight-Controller/assets/166318874/7103cce1-4432-4cc2-b39d-5212d92ebda4)

**PCB Mounting Holes (center to center):** 160 mm x 90 mm

## Modifications to Original Source
1. Recreated the schematic diagram in KiCad.
2. Designed a PCB based on the schematic.
3. Substituted the 5V relays for an alternate part with higher current rating.
4. Added detachable headers and connectors for connecting to the car's wiring.

## Credits
The electrical schematic and Arduino code this project is based on were created by WalkerTexan.\
See his original project here: https://www.hackster.io/walkertexan/fiero-headlight-controller-8eaa4c

KiCad Schematic and PCB Layout/Design by Ryan Blanchard.

## License
This project is published under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International license.\
Use of this project for commercial purposes is prohibited.

For full details, see the license file.
