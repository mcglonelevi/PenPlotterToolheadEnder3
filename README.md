
# Pen Plotter for Ender 3 / Ender 3 V2
## Introduction
I had an old Ender 3 V2 that was sitting around collecting dust.  I thought it would be fun to make a pen plotter attachment for the Ender 3 V2.  In case others were interested in making it, I am making this open-source under the MIT license.

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

## Recommended Print Settings
There are two parts to print in this build - the pen carriage and the base plate that attaches to the printer.  I printed both parts with 4 walls and 40% infill.  No support should be necessary, but there are a few overhangs.  The size of the overhangs are very small though.

## Quick Assembly Instructions
1. Print out the carriage and base plate.
2. In the carriage, press 2 brass inserts into the front 2 screw holes.  Use a soldering iron to melt the plastic and press them into place.  For PLA, I would recommend a soldering temp ~525F or 200C
3. Check the fit of the 3mm steel rods in the pen carriage.  The pen carriage should slide but not move.  Depending on the tolerances of your printer, you may need to use a 1/8in drill bit to expand the holes.  Also, some PTFE lube may also help things slide a little easier.
4. Insert the steel rods into the baseplate but do not push them all the way down.
5. Slide the springs over the steel rods.
6. Compress the spring and move one side of the pen carriage into place and push the steel rod all the way down.  If the rod will not press all the way into the bottom, I would recommend a clamp or a vice and gently hammer the rod into place.  It should be flush or close to flush with the top of the base plate.
7. Compress the other spring and insert the other rod through the other hole in the pen carriage.
8. Remove the toolhead and hot end from your Ender 3.  The instructions for this vary by model, but should involve unscrewing a screw in the back of the toolhead and then 2 screws for the hotend.
9. Using 2 M3 screws, attach the base plate to your printer.
10.Using 2 more M3 screws, thread them into the brass inserts on the front of the pen carriage. 

## Calibration
Here are my recommended calibration steps.
1. Using the prepare menu, home all the axes on your printer.  At the end of calibration, it's pretty likely that your Z height will not be ~13mm.
2. Using the controls on the printer, set the Z axis to 0.1mm.
3. Take a thick piece of paper like card stock or a playing card and insert it under the pen carriage so that it is just slightly elevated off of the base plate.
4. Insert a pen and let it touch the build plate.  Turn both screws in the pen carriage to secure the pen in place.
5. Remove the card stock from under the pen carriage.
6. Lift up on the pen slightly and put a piece of paper in place.  I secure the paper to the build plate with binder clips.
7. Using the controls on the printer, you can manually move the head around for a quick test.  Another option is to disable the stepper motors and move the gantry and bed by hand.  Assuming the lines look nice and solid, your printer is calibrated.

## Generating G-Code
I followed the instructions from Andrew Sink for the PLTR V2 here:
[https://github.com/AndrewSink/pltr_toolhead](https://github.com/AndrewSink/pltr_toolhead)

Page 18-29 of the user guide shows how to configure Inkscape.

## Debugging GCode
For some reason, my Ender 3 started skipping instructions from the GCode generated from the Inkscape Extension.  It could be that my printer is old and half-dead, so I ended up using [Pronterface](https://www.pronterface.com/) to run the GCode by hooking up my Ender 3 to my laptop via the USB port.  [NC Viewer](https://ncviewer.com/) is also a great tool for verifying the generated GCode.

## Other Recommended Builds / Reads
My design for this was inspired by AndrewSink's PLTR V2 toolhead.  I really recommend looking at the PLTR V2 repo as well.
[PLTR V2](https://github.com/AndrewSink/pltr_toolhead)
