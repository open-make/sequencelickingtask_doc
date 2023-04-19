[M4x10 screws]:Parts.yaml#M4x10PanSteel
[No. 2 Phillips screwdriver]:Parts.yaml#Screwdriver_Philips_No2
# Satellites system

Though you should feel free to use any system such as BPOD or what else to implement your task, we have our custom solution using the Satellites system I developed.

{{BOM}}

## Videos

 A comprehensive tutorial series on the Satellites system is in this YouTube playlist: https://www.youtube.com/playlist?list=PLPB2m00RRCw33eNtJLqkyPb1VPAy_Gf38
 
## Microcontroller and firmware

We use two Teensy boards, one for behavioral control using the program from https://github.com/oconnorlab/Xu_et_al_2021/tree/main/Arduino%20code/SeqlickSatellite, and one for audio using the program from https://github.com/oconnorlab/Xu_et_al_2021/tree/main/Arduino%20code/SeqlickSound. Both programs require the Satellites library among a few others (https://github.com/oconnorlab/satellites/tree/master/Arduino%20libraries). 

Note that some of these dependencies may contain machine-specific configurations, e.g. https://github.com/oconnorlab/satellites/blob/master/Arduino%20libraries/ManyRig/ManyRig.cpp. This is how we separate configuration from computation. You may need to change them to fit your configurations.


## Microcontroller interface board
A custom-designed PCB that helps the Teensy board to interface with various periphery such as the lick port controller, valves, etc.
https://github.com/oconnorlab/satellites/tree/master/Satellites%20Shield/SatellitesPCB_v2_0

The electronic parts can be found in the [added spreadsheet](extras/ordering-list-electronics.csv) for now.

## SatellitesViewer

This is the Matlab app that communicates with the firmware and controls the hardware.
https://github.com/oconnorlab/satellites/tree/master/SatellitesViewer
 