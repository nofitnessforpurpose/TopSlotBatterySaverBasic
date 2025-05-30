# Top Slot Battery Saver Basic - Protect Basic

A minimal Top Slot, battery failure memory saver for PSION Organiser II (all family) devices. The design reduces risk of internal device memory loss especially due to Lithium 9 Volt surrogate battery discharge characteristics (limited if any warning). By providing sufficient standby power for longer term internal memory retention and specifically not operation. Permitting hours / days for recharge of main power battery or months of power down whilst preserving the internal RAM contents. The design fits a classic PSION Organiser II Top Slot Case (See all notes).
<BR>
<div align="center">
  <div style="display: flex; align-items: flex-start;">
  <img src="https://github.com/nofitnessforpurpose/TopSlotBatterySaverBasic/blob/main/photos/BATSVE-11.jpg?raw=true" width="400px" alt="PSION Organiser II Top Slot Battery Saver. Image copyright (c) 14 December 2024 nofitnessforpurpose All Rights Reserved">
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

### On-Line Preview   
Models might be viewed on line using the following links. Noting display of any mesh lines is a feature of the renderer and are not contained in the source STEP model. It is strongly recommended to use the source STEP file where ever possible, as any export process will introduce artifacts.  
 - PCB - <a target="_blank" href="https://3dviewer.net/#model=https://github.com/nofitnessforpurpose/TopSlotBatterySaverBasic/blob/main/CAD/Asspcb.stp">here</a>  
 - Assembly - <a target="_blank" href="https://3dviewer.net/#model=https://github.com/nofitnessforpurpose/TopSlotBatterySaverBasic/blob/main/CAD/Assbsb.stp">here</a>  
<BR>
<BR>

## Implementation  
The design presents a battery backup system interface to the <a href="https://www.jaapsch.net/psion/manxp.htm#c1">Top Slot</a> hardware of a PSION Organiser II family of devices. The PCB dimensions (38.0 x 43.6 mm) are ideally suited to low cost manufacture. The 2 layer PCB design provides low cost of implementation. Whilst the PCB space claim is intended to be suitable for a classic <a target="_blank" rel="noopener noreferrer" href="https://github.com/nofitnessforpurpose/TopSlotCase">Top Slot Case </a> (See Considerations) and construction is through hole PCB based for ease of assembly.  
<BR>
A minimum configuration comprises:  
- a 2 layer PCB  
- 1N4148 diode
- 2 battery clips
- 2 x 8 way Right angle header (~8 mm engagement length, gold plated)
- 2 off CR2032 batteries or similar
<BR>

### Device Power Source  
A classic Barrel Jack (5.5 mm outer, 2.0 mm pin) connector for the ~10.4 Volt 175 milli Amp centre positive pin power supply is located to be compatible with the classic Top Slot Case. The Barrel Jack (This is the same connector used on the classic Arduino Uno and Mega boards),  connections are brought to 2 header pins on the left of the PCB to permit alternate power sources to be readily accommodated.   

### Power Backup
A low voltage 'secondary' power source is held on the PCB to allow for longer term retention when the main power supply or internal PP3 battery become depleted. Switching is automatic via diodes and the purposefully lower secondary battery level restricts usage to notification and memory backup only.  

Details on testing and backup battery performance are located in the <a target="_blank" rel="noopener noreferrer" href="https://github.com/nofitnessforpurpose/TopSlotBatterySaverBasic#testing">Top Slot Battery Saver Basic - Testing</a>.

### Software
The device is transparent to the Organiser's Operating system and requires no software to operate.  

<BR>

## USE
It is preferable to avoid conneting the unit with no power source avilable e.g. absence of 9 Volt internal battery or power sourced via the units power connections i.e. 10.4 Volt Barrel Jack connection. So as to avoid unecessarily discharging the backup batteries. By providing a main power source prior to connection of the unit. The internal capacitors of the Orgnaiser are 'pre-charged' from the main power source rather than the backup battery system, thus ensuring maximum life and protection.

<BR>


## Operation  
The principle of the approach is embodied in the classic 10.4 Volt, and potentially other, PSION Organiser power supplies. The classic 10.4 Volt power supply includes a resistor and Zener Diode arrangement which will present a 6.4 Volt regulated voltage to the device for a short period in the event no internal <a target="_blank" rel="noopener noreferrer" href="https://en.wikipedia.org/wiki/Nine-volt_battery">9 Volt PP3 battery</a> and loss of mains power. With the arrangement the internal memory contents would be retained for a limited period (longer than the ~30 seconds provided by the internal capacitor - <a href="https://www.jaapsch.net/psion/manxp.htm#c2">CM/XP Manual Section 2</a>) e.g. during PP3 battery change.  
<BR>
Operation of the Low Battery Voltage mode is described in section <a target="_blank" rel="noopener noreferrer" href="https://www.jaapsch.net/psion/tech07.htm#p7.4.3">7.4.3  LOW BATTERY TEST</a>. Typically when a machine is powered on, either by pressing the ON/CLEAR button or via activation of the Top Slot AC line, the keyboard buffer will be empty and the Low Battery state evaluated by testing the state of D0 on PORT 5 of the Hitachi 6303 micro processor.  
<BR>
In the case of low or no main system voltage (e.g. 9 Volt battery), the Battery Saver voltage will (with new batteries) present ~6.3 volts on the Top Slot main power line VB (SVB). Via a diode, thus causing the system to retain internal RAM contents. In the event the system is activated e.g. via the ON/CLEAR button, there is typically sufficient power for the device to momentarily activate and the BATTERY TOO LOW message is displayed on the Organiser's screen (See section 10 of the <a target="_blank" rel="noopener noreferrer" href="https://www.jaapsch.net/psion/manxp2.htm#p10-1">CM/XP Manual</a>).  

<BR>

## Retention period
In standby mode, the device typically consumes 30 uA as described in section <a target="_blank" rel="noopener noreferrer" href="https://www.jaapsch.net/psion/tech03.htm#p3.4">3.4  STANDBY REGULATOR</a>. An XP device was measured at 19 uA continous current draw from backup cells, not including clock maintenance. Assuming high performance Lithium / Manganese Dioxide (Li/MnO2) CR2032's and the device power not activated by pressing ON/CLEAR, the device at room temperature. Memory protection of ~1 year is anticipated, following loss of the 9 Volt main battery power.  

<BR>

## Testing
Test conditions:  
MODEL XP ROM 3.6, 1 x 32k ROM (COMMS), 1 x 32K RAMPAK, Battery Saver Rev 0.1, Panasonic CR2025's  
Commence and complete fitting of PP3 battery or mains sourced power, followed by insertion of Battery Saver into Top Slot. No Power refers to removal of main power (PP3 or other).  
a) 2 cycles - No Power Source - Off 1 Minute - ON/CLEAR - Low Battery Warning sequences - No issues  
b) 2 cycles - No Power Source - Off 5 minutes - Battery fitted - No issues  
c) 2 cycles - No Power Source - Off 9 hours - Battery fitted - No issues  

Test a) is believed to be the most demanding current draw and simulates the most likely scenario for regular use.  
Test c) is believe to be the most realistic scenario for regular use.  
All the above tests performed on the same battery set.  
<BR>

## Assembly testing
PCB is tested for trace continuity and trace short circuits.  
 - PCB visual inspection including screen printing, traces, coatings, via quality and dimensional verification
 - PCB Electrical verifications for trace continuity and short circuits
   
Assembled PCB is tested for:
 - Visual inspection for connector alignment, solder balls or whiskers
 - Electrical tests on connector for short circuits
 - 0 Volt connection continuity
 - Diode(s) polarity test
 - Diode type and location verification
 - Barrel Jack connector polarity verification
 - Battery spring retention check
 - Standby battery power provision

Post Assembly tests:
 - Insertion into Organiser Model CM
 - Test a) and b) included in 1 hour use in Top Slot  

Note: tests are performed using the <a target="_blank" rel="noopener noreferrer" href="https://github.com/nofitnessforpurpose/TopSlotSpy">Top Slot Spy</a> and using a MODEL CM device.  

<BR>

## Internal Connections  
Internally a 0.1" header is available to accommodate alternate 9 volt power systems (possibly <a target="_blank" rel="noopener noreferrer" href="https://www.adafruit.com/product/5644">this</a> and a USB lead).  

The unit uses the Vbb and 0 Volt connection of the Top Slot, no other connections are used.  

<BR>

## Use Case  
The envisaged use case is in place of the classic power supply adaptor. However, the adaptor may remains in place to protect the internal memory of the unit.

<div align="center">
  <div style="display: flex; align-items: flex-start;">
  <img src="https://github.com/nofitnessforpurpose/TopSlotRetroIOBasic/blob/main/images/TSRIOB-09.png?raw=true" width="300px" alt="PSION Organiser II Top Slot Basic I/O Interface. Image copyright (c) 08 December 2024 nofitnessforpurpose All Rights Reserved">
  </div>
</div>
<BR>

Note it is recommended to:  
 - Not to have the unit powered when inserting or removing devices  
 - Connect a PP3 (ANSI:1604A IEC:6LR61) battery to the target unit, followed by inserting the Battery Saver   
   or
 - Power from via the external power sourced via the Battery Saver unit
 - Use only the original adaptor, or power supply having the same supply voltage
 - Following 'Low Battery Notification', replace the main power source promptly  
 - Replace the Battery Saver internal standby batteries following any extended period of main power loss
 - Ensure regular backups are maintained
 - Always use a case requiring a tool to obtain access to batteries i.e. screw fixing
 

Where a Battery Saver unit is inserted into a discharged device without 'internal power', such as a PP3 battery, the units internal capacitors will draw relatively high current from the standby batteries. This will relatively rapidly discharge the standby batteries, reducing the battery capacity available to act for long term storage protection. The design is intended not to provide sufficient voltage to allow operation. Pressing the ON/CLEAR button will result in the unit notifying Low Battery status and powering down.

When the main power source is in a good state, no power is drawn from the Battery Saver standby batteries.
<BR>
<BR>
Testing indicates good compatibility, no software is required.

An advantage of using the approach is the use of a classic power supply case with no modification (See note on original connector). Removal of case screw necessitated for secondary battery change, is considered a safety feature (reducing potential risk to young children accessing coin cells).

The device supports extended use from alternate external power sources i.e. without main battery, as when external source removed the Coin cells automatically switch in to retain internal memory. This reduces reliance on 9 volt battery use and would provide up to 12 months memory retention, provided the ON/CLEAR not utilised whith no main power source connected (see Testing).

<BR>

## Stored Energy Use  
Precautions when using any stored energy device must be employed, with particular focus in this instance on batteries.

Where Coin Cells are used the following guidance may be of assistance:  
<BR>
Guidance:  
 - Keep batteries away from children  
 - Always install the batteries correctly as per instructions
 - Remove batteries and store carefully when device not in use  
 - Remove discharged batteries from device promptly  
 - Ensure that the contact points are clean and conductive  
 - Do not mix different types of battery  
 - Do not heat batteries  
 - Do not attempt to recharge batteries not specifically designed for recharging  
 - Do not dispose of in a fire  
 - Do not allow batteries to form a 'Short Circuit' connection  
 - Dispose in accordance with local regulations, use Re-cycling facilities    
 - If chemical exposure occurs, seek immediate medical attention  
 - If a battery is swallowed, seek immediate medical attention  
 - Always follow battery manufacturer guidance to prevent thermal events  

<BR>

## Considerations
Models or files makes no accommodation for manufacturing tolerances, process or material - see Notes below.  

The original male 8 way 2 row top slot header style connector (marked MXS 70224) may have included a custom pin support moulding. Data from a parts list kindly indicated in this <a href="https://www.organiser2.com"> hardware forum</a> seemed to confirm this theory. Readily available 8 way 2 row header connectors tend to have smaller pin support mouldings. The effect of using pin headers with smaller moulding is to permit the PCB to displace vertically in the slot guide channel, resulting in poor alignment with the mating female connector and potential insertion difficulty. There are a number of mitigations, such as changing the height of the male header connector in the PCB and adding material to support the top of a smaller male header pin support moulding. The precise accommodation will depend on your selected pin header moulding.  

Connecting any device which has not undergone thorough testing, will lead to irreversible degradation!  

<BR>

## Questions / Discussion
See <a target="_blank" rel="noopener noreferrer" href="https://www.organiser2.com/"> Organiser 2 Hardware </a> forum, though see note below first.

<BR>

## Please note:  
Such a system does not obviate the need for standard good practice backup procedures.  
Assessment for any fitness for purpose is entirely the users responsibility. Use is entirely at the users own risk. Any degradation to hardware, data loss or corruption is the responsibility of the user.

All information is For Indication only.
No association, affiliation, recommendation, suitability, fitness for purpose should be assumed or is implied.
Registered trademarks are owned by their respective registrants.
