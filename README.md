# TopSlotBatterySaver

A minimal Top Slot battery failure memory saver for PSION Organiser II (all family) devices. The design reduces risk of internal devce memory loss due to Lithium 9 Volt surrogate battery discharge characteristics (limited if any warning). By providing sufficent standby power for longer term internal memory retention and specifially not operation. Permitting hours / days for recharge of main power battery or months of power down. The design fits a classic PSION Organiser II Top Slot Case (See all notes).
<BR>
<div align="center">
  <div style="display: flex; align-items: flex-start;">
  <img src="https://github.com/nofitnessforpurpose/TopSlotBatterySaver/blob/main/photos/BATSVE-03.png?raw=true" width="400px" alt="PSION Organiser II Top Slot Battery Saver. Image copyright (c) 14 December 2024 nofitnessforpurpose All Rights Reserved">
  </div>
</div>
<BR>

[![Organiser](https://img.shields.io/badge/gadget-Organiser_II-blueviolet.svg?%3D&style=flat-square)](https://en.wikipedia.org/wiki/Psion_Organiser)
[![GitHub License](https://img.shields.io/github/license/nofitnessforpurpose/TopSlotRetroIOBasic?style=flat-square)](https://github.com/nofitnessforpurpose/TopSlotCase/blob/main/LICENSE)
[![Maintenance](https://img.shields.io/badge/maintained%3F-yes-green.svg?style=flat-square)](https://github.com/nofitnessforpurpose/TopSlotCase/graphs/commit-activity)
![GitHub repo size](https://img.shields.io/github/repo-size/nofitnessforpurpose/TopSlotRetroIOBasic?style=flat-square)
[![Static Badge](https://img.shields.io/badge/format-GERBER-blue?style=flat-square)](https://en.wikipedia.org/wiki/Gerber)

<br>  
All the files are required for a complete assembly.  
<BR>
 - The default code format is <a target="_blank" rel="noopener noreferrer" href="https://en.wikipedia.org/wiki/Open_Programming_Language">OPL</a> or 6303 Assembler as flat text files.
<BR>
 - The default repository format is STEP (<a target="_blank" rel="noopener noreferrer" href="https://en.wikipedia.org/wiki/ISO_10303"> ISO 10303</a> ) due to its high fidelity.  
<BR>
 &nbsp;&nbsp;&nbsp;&nbsp;{ STL files are surface geometry as opposed to solid model representations, often containing export processing artifacts }. <br>  
 - The default repository format for PCB files is <a targer="_blank" rel="noopener noreferrer" href="https://en.wikipedia.org/wiki/Gerber_format">GERBER</a> .
<BR>

<BR>
<a target="_blank" rel="noopener noreferrer" href="https://www.freecad.org/" > FreeCAD </a> may prove suitable for viewing, handling and, if desired modifying STEP files.
<BR>
<a target="_blank" rel="noopener noreferrer" href="https://www.kicad.org/" >KiCad </a> may prove suitable for viewing GERBER files.
<BR>
<BR>

## Implementation
The design presents a battery backup system interface to the Top Slot hardware of a PSION Organiser II family of devices. The 4 layer PCB dimensions (38.0 x 43.6 mm) are ideally suited to low cost manufacture. The 4 layer PCB design provides improved EMC performance over two layer implementations. Whilst the PCB space claim is intented to be suitable for a classic <a target="_blank" rel="noopener noreferrer" href="https://github.com/nofitnessforpurpose/TopSlotCase">Top Slot Case </a> and construction is through hole PCB based for ease of assembly.
<BR>
### Device Power Source  
A classic Barrel Jack (5.5 mm outer, 2.0 mm pin) connector for the ~10.4 Volt 175 milli Amp center positive pin power supply is located to be compatible with the classic Top Slot Case. The Barrel Jack connections are brought to 2 header pins on the left of the PCB to permit alternate power sources to be readily accomodated. 
<BR>
### Power Backup
A low voltage 'secondary' power source is held on the PCB to allow for longer term retention when the main power supply or internal battery become depleted. Switching is automatic and the purposefully lower secondary battery level restricts usage to notification and memory backup only,
<BR>
### Retention period
This will be determined when battery size selection has been finalised, months are envisaged for stand by operation only. This will be shortened by power on sequences which are considerably higher power drain events.
<BR>

### Connections  
Internally a 0.1" header is avilable to accomodate alternate 9 volt power systems (possibly <a target="_blank" rel="noopener noreferrer" href="https://www.adafruit.com/product/5644">this</a> and a USB lead).  

The unit uses the Vbb and 0 Volt connection of the Top Slot, no other connections are used.
<BR>
<BR>

## Use Case  
<div align="center">
  <div style="display: flex; align-items: flex-start;">
  <img src="https://github.com/nofitnessforpurpose/TopSlotRetroIOBasic/blob/main/images/TSRIOB-09.png?raw=true" width="300px" alt="PSION Organiser II Top Slot Basic I/O Interface. Image copyright (c) 08 December 2024 nofitnessforpurpose All Rights Reserved">
  </div>
</div>
<BR>

<BR>
<BR>
Testing indicates good compatability, no software is required.

A minimal configuration requires:  
- 4 layer PCB
- 1N4148 Diode
- 1N5817 Diode
- 2 Coin cells (TBC size)
- 2 x 8 way Right angle header (~8 mm engagement length)

An advantage of using the approach is the use of a classic power supply case with no modification (removal of screws necessitated for secondary battery change is considered a safety feature (reducing potential risk to young children).  

## Considerations
Models or files makes no accomodation for manufacturing tolerances, process or material - see Notes below.  

The original male 8 way 2 row top slot header style connector (marked MXS 70224) may have included a custom pin support moulding. Data from a parts list kindly indicated in this <a href="https://www.organiser2.com"> hardware forum</a> seemed to confirm this theory. Readily avialable 8 way 2 row header connectors tend to have smaller pin support mouldings. The effect of using pin headers with smaller moulding is to permit the PCB to displace vertically in the slot guide channel, resulting in poor alignment with the mating female connector and potential insertion difficulty. There are a number of mitigations, such as changing the height of the male header connector in the PCB and adding material to support the top of a smaller male header pin support moulding. The precise accomodation will depend on your selected pin header moulding.  

Connecting any device which has not undergone thorough testing, will lead to irreversible degredation!  


## Questions / Discussion
See <a target="_blank" rel="noopener noreferrer" href="https://www.organiser2.com/"> Organiser 2 Hardware </a> forum, though see note below first.


## Please note:  
All information is For Indication only.
No association, affiliation, recommendation, suitability, fitness for purpose should be assumed or is implied.
Registered trademarks are owned by their respective registrants.