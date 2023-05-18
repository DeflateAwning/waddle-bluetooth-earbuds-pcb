# waddle-bluetooth-earbuds-pcb
A PCB to drive KZ-ATE or similar earbuds wirelessly, because all other cheap wireless earbuds suck.

After trying a variety of wireless earbuds (which go directly in your ear), I set out to combine the high quality of the wired KZ-ATE family of earbuds with the convenience of wireless earbuds (especially while wearing winter clothing).

## Core Components BOM
After creating the Requirements (below), the following rough BOM was picked out:

1. Bluetooth Module: [DFR0781 BT401 V3 module](https://www.dfrobot.com/product-2177.html), [Datasheet](https://wiki.dfrobot.com/Audio_BLE_SPP_Pass_Through_Module_Bluetooth_5.0_SKU_DFR0781)
2. Microcontroller: TBD
3. PCB: custom, designed in this repo with KiCAD
4. Battery: 3.7V nominal lipo battery, used in RC helicopters and similar. Uses a 2.54mm header pin as the connector.
5. Battery charge circuit: TBD
6. Earbuds: KZ-ATE (TBC), with wires cut


## Requirements
Prior to designing anything, laying out the requirements and a rough proposed solution is important.

### The Obvious
1. Be battery powered.
2. Optimize for low cost, small size, and good battery life.
3. Be wireless over bluetooth.
4. Sound good. No static.
5. Must have play/pause buttons, which are easily controllable. 

### Core Requirements
1. The PCB will contain a microcontroller, bluetooth module
2. The Bluetooth module must be configurable. It must support play/pause, name changes, and audio beep configuration.
3. The PCB must drive two separate earbuds (left and right).
4. The PCB must have a battery and charging circuit.
5. USB-C only.
6. LED indicator(s) for currently playing, powered on, state-of-charge.
7. Good volume control, with a range of options over the spectrum.
8. Under CAD$80 unit cost.
9. Easy-to-control gestures via capacitive touch or tactile buttons.
10. 5h battery life.
11. Easy integration with a 3D printed case by smart layout and/or mounting holes.

### Ideal Requirements
The following features will be considered, and will be integrated if possible:

1. Control by capacitive touch.
2. Have two separate identical PCBs, one for each ear. More than likely though, there will only be a single PCB, which sits behind the user's neck or dangles in front.
3. Serial debugging if you plug it into a cell phone.
4. Equilizer of some sort.
5. >10h battery life, and/or changable batteries.
6. Include a microphone, and/or make the mic possible to disable.
7. Potentially integrate a microSD card right on the board, if beneficial.
