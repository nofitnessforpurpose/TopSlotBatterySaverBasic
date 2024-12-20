# TopSlotBatterySaver

A minimal Top Slot, battery failure memory saver for PSION Organiser II (all family) devices. The design reduces risk of internal devce memory loss especially due to Lithium 9 Volt surrogate battery discharge characteristics (limited if any warning). By providing sufficent standby power for longer term internal memory retention and specifially not operation. Permitting hours / days for recharge of main power battery or months of power down. The design fits a classic PSION Organiser II Top Slot Case (See all notes).
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
The design presents a battery backup system interface to the Top Slot hardware of a PSION Organiser II family of devices. The PCB dimensions (38.0 x 43.6 mm) are ideally suited to low cost manufacture. The 2 layer PCB design provides low cost of implementation. Whilst the PCB space claim is intented to be suitable for a classic <a target="_blank" rel="noopener noreferrer" href="https://github.com/nofitnessforpurpose/TopSlotCase">Top Slot Case </a> (See Considerations) and construction is through hole PCB based for ease of assembly.
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
The envisaged use case is in place of the classic power supply adaptor. However, the adaptor may remains in place to protect the internal memory of the unit.

<div align="center">
  <div style="display: flex; align-items: flex-start;">
  <img src="https://github.com/nofitnessforpurpose/TopSlotRetroIOBasic/blob/main/images/TSRIOB-09.png?raw=true" width="300px" alt="PSION Organiser II Top Slot Basic I/O Interface. Image copyright (c) 08 December 2024 nofitnessforpurpose All Rights Reserved">
  </div>
</div>
<BR>

Note it is recomended to:  
 - Not to have the unit powered when inserting or removing devices  
 - Connect a PP3 (ANSI:1604A IEC:6LR61) battery to the target unit, followed by the Battery Saver  
 - Following 'Low Battery Notification', replace the main power source promptly  
 - Replace the internal standby batteries following  
 - Ensure regular backups are maintained  

Where a Battery Saver unit is connected to a device without 'internal power', such as a PP3 battery, the units internal capacitors will draw considerable current from the standby batteries. This will relatively rapidly discharge them and reduce the available capcity available to act for long term storage protection. The design is intended not to provide sufficient voltage to allow operation. Pressing the ON / CLEAR button will result in the unit notifying Low Battery status and powering down.

When the main power source is in a good state, no power is drawn from the Battery Saver standby batteries.
<BR>
<BR>
Testing indicates good compatability, no software is required.

A minimal configuration requires:  
 - 4 layer PCB  
 - 1N5187 Diode  
 - 2 Coin cells ( CR2032 )  
 - 2 x 8 way Right angle header (~8 mm engagement length)  

An advantage of using the approach is the use of a classic power supply case with no modification (See note on original connector). Removal of case screw necessitated for secondary battery change, is considered a safety feature (reducing potential risk to young children accessing coin cells).

The device would support extended use from alternate external power sources i.e. without main battery, as when external source removed the Coin cells automatically switch in to retain internal memeory.

## Stored Energy Use  
Precautions when using any stored energy device must be employed, with particular focus in this instance on batteries.

Where Coin Cells are used the following guidance may be of assistance:  
<BR>
Guidance:  
 - Keep batteries away from children  
 - Always install the batteries correctly as per instructions  
 - Ensure that the contact points are clean and conductive  
 - Do not mix different types of battery  
 - Do not heat batteries  
 - Do not attempt to recharge batteries not specifically designed for recharging  
 - Do not dispose of in a fire  
 - Do not allow batteries to form a 'Short Circuit' connection  
 - Dispose in accordance with local regulations, use Re-cylcing facilties  
 - If chemical exposure occurs, seek immediate medical attention  
 - If a battery is swallowed, seek immediate medical attention  
 - Always follow battery manufacturer guidance to prevent thermal events  

<BR>

## Considerations
Models or files makes no accomodation for manufacturing tolerances, process or material - see Notes below.  

The original male 8 way 2 row top slot header style connector (marked MXS 70224) may have included a custom pin support moulding. Data from a parts list kindly indicated in this <a href="https://www.organiser2.com"> hardware forum</a> seemed to confirm this theory. Readily avialable 8 way 2 row header connectors tend to have smaller pin support mouldings. The effect of using pin headers with smaller moulding is to permit the PCB to displace vertically in the slot guide channel, resulting in poor alignment with the mating female connector and potential insertion difficulty. There are a number of mitigations, such as changing the height of the male header connector in the PCB and adding material to support the top of a smaller male header pin support moulding. The precise accomodation will depend on your selected pin header moulding.  

Connecting any device which has not undergone thorough testing, will lead to irreversible degredation!  


## Questions / Discussion
See <a target="_blank" rel="noopener noreferrer" href="https://www.organiser2.com/"> Organiser 2 Hardware </a> forum, though see note below first.


## Please note:  
Such a system does not obviate the need for standard good practice backup proceedures.  
Assessment for any fitness for purpose is entirely the users responsiblity. Use is entirely at the users own risk. Any degredation to hardware, data loss or corruption is the responsibility of the user.

All information is For Indication only.
No association, affiliation, recommendation, suitability, fitness for purpose should be assumed or is implied.
Registered trademarks are owned by their respective registrants.
