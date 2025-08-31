
# Pen Plotter for Ender 3 / Ender 3 V2
## Introduction
I had an old Ender 3 V2 that was sitting around collecting dust.  I thought it would be fun to make a pen plotter attachment for the Ender 3 V2.  In case others were interested in making it, I am making this open-source under the MIT license.

![Hardware](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/demo.jpg)

## Demo
I made a YouTube video showcasing the toolhead in action: https://www.youtube.com/watch?v=6iu8gkPlm34

## Design Constraints
I looked at other pen plotting attachments for the ender 3 V2.  I wanted the following features in my build:
1. I wanted the pen to have some pressure via springs to account for an unlevel bed.
2. I am running [Jyers Marlin firmware](https://github.com/Jyers/Marlin) on my Ender 3 V2 with a BL Touch.  I didn't want to install the old endstops, so I made my solution compatible with models of the Ender 3 with a BL touch.

## Bill of Materials
1. About 25 grams of PLA or equivalent of your preferred filament.
2. 3mm * 40mm steel rods (2).  I bought [these](https://www.amazon.com/Lyrlidr-Stainless-Industry-Working-Hobbies/dp/B0DCBCRB1C) on Amazon and cut them down to size.
3. 2 M3 brass inserts - I used [these](amazon.com/dp/B0CDH36ZMX?ref=ppx_yo2ov_dt_b_fed_asin_title)
4. 4 M3 screws.  I think M3x20mm should work for most cases.
5. 1 M3 nut.
6. 2 springs.  I used 0.3mm x 4mm x 15mm - Something [like these](https://www.amazon.com/PATIKIL-Compression-Stainless-Mechanical-Assortment/dp/B0DKCRH26S/ref=sr_1_1?crid=2YPIPNPZV0TVB&dib=eyJ2IjoiMSJ9.zrTW4QX48CQNP_jUS1kaHjvaTrfqq_Rypn8CPh1w9G1KUKY_KzR_puDsWAFM71_RbcTMmy4xnSn8xV6Hsi3eUQIqBf8G60oqLXZ83t9nsKQYQa_6lak7JeHlSxfA5gmG2156aAYdmnGm5eSWGwkzsPX6I1oCKU_UT50pMy8KtdEqpQef6gqdCewJkrbELp7Iiv-KmxqAM2nPNDv7bhIDMMky6WlEhJwCP7vpiXC6wpG748u3Fadvy2PhzL-lcV4B_do8RrsJvg6vSuLuFziHHOrV2Nf_mpZ2qKUNqYRxOGE.Y5VAdmfX7MKsC9qINN9PoeogPl6I3XBzB-H9gtceSwY&dib_tag=se&keywords=0.3mm%2bx%2b4mm%2bx%2b15mm%2bspring&qid=1756666907&s=industrial&sprefix=0.3mm%2bx%2b4mm%2bx%2b15mm%2bspring,industrial,87&sr=1-1&th=1) should work.

![Hardware](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/bom/hardware.jpg)
![Printed Parts](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/bom/printed_parts.jpg)

## Recommended Print Settings
There are two parts to print in this build - the pen carriage and the base plate that attaches to the printer.  I printed both parts with 4 walls and 40% infill.  No support should be necessary, but there are a few overhangs.  The size of the overhangs are very small though.

## Quick Assembly Instructions
These instructions assume the toolhead and hotend have been removed from your Ender 3.  The instructions for this vary by model, but should involve unscrewing a screw in the back of the toolhead and then 2 screws for the hotend.

### Instructions
1. In the carriage, press 2 brass inserts into the front 2 screw holes.  Use a soldering iron to melt the plastic and press them into place.  For PLA, I would recommend a soldering temp ~525F or 200C [image](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/assembly/step_1.jpg)
2. Check the fit of the 3mm steel rods in the pen carriage.  The pen carriage should slide but not move.  Depending on the tolerances of your printer, you may need to use a 1/8in drill bit to expand the holes.  Also, some PTFE lube may also help things slide a little easier.
3. Insert the steel rods into the baseplate but do not push them all the way down. [image](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/assembly/step_3.jpg)
4. Slide the springs over the steel rods. [image](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/assembly/step_4a.jpg)
5. Compress the spring and move one side of the pen carriage into place and push the steel rod as far in as you can. [image](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/assembly/step_5a.jpg)  Compress the other spring and insert the other rod through the other hole in the pen carriage. [image](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/assembly/step_5b.jpg)
6: If the rods are not flush with the top, I would recommend a clamp or a vice or gently hammering the rod into place until its flush with the top.  It should be flush or close to flush with the top of the base plate if the length is close to 40mm. [image](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/assembly/step_6.jpg)
7. Using 2 M3 x 8MM screws, thread them into the brass inserts on the front of the pen carriage. [image](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/assembly/step_7.jpg)
8. The base plate has 2 holes for attaching the plate to the printer.  For the right hole, use an M3x8mm screw.  For the right hole, stick a M3x12mm screw through it and the screw should poke through the back of the plate.  Secure it with a nut. [image](https://github.com/mcglonelevi/PenPlotterToolheadEnder3/blob/main/img/assembly/step_8.jpg)

## Calibration
Here are my recommended calibration steps.
1. Using the prepare menu, home all the axes on your printer.  At the end of calibration, it's pretty likely that your Z height will be ~13mm.
2. Using the Move controls on the printer, set the Z axis to ~0.5mm.
3. Insert a pen and let it touch the build plate.  Turn both screws in the pen carriage to secure the pen in place.
4. Lift up on the pen slightly and put a piece of paper in place.  I secure the paper to the build plate with binder clips.
5. Using the controls on the printer, you can manually move the head around for a quick test.  Another option is to disable the stepper motors and move the gantry and bed by hand.  Assuming the lines look nice and solid, your printer is calibrated.

If your pen doesn't make contact with the paper, rerun the calibration steps above but use a slightly higher number on the Z in step 2 (0.7mm or 0.9mm may work better depending on pen and paper thickness).

## Generating G-Code
I followed the instructions from Andrew Sink for the PLTR V2 here:
[https://github.com/AndrewSink/pltr_toolhead](https://github.com/AndrewSink/pltr_toolhead)

Page 18-29 of the user guide shows how to configure Inkscape.

## Debugging GCode
For some reason, my Ender 3 started skipping instructions from the GCode generated from the Inkscape Extension.  It could be that my printer is old and half-dead, so I ended up using [Pronterface](https://www.pronterface.com/) to run the GCode by hooking up my Ender 3 to my laptop via the USB port.  [NC Viewer](https://ncviewer.com/) is also a great tool for verifying the generated GCode.

## Other Recommended Builds / Reads
My design for this was inspired by AndrewSink's PLTR V2 toolhead.  I really recommend looking at the PLTR V2 repo as well.
[PLTR V2](https://github.com/AndrewSink/pltr_toolhead)
