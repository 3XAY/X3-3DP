Made by: @3XAY <br>
Repository link: https://github.com/3XAY/X3-3DP/ <br>
Total hours so far: 3.5


* [X] I have a 3D printer or will be getting one before March 21st


## Goal:
- Build volume must be at LEAST 200x200x200mm, ideally close to 250, but is optional depending on budget
- Must be CoreXY
- All parts should be printable in a build volume of 180x180x180mm (Bambu Lab A1 Mini)
- Should be simple to build
- Should be simple to maintain
- Be able to print PETG
- Use common parts
- Quality and/or speed should be similar to Bambu Lab A1 Mini
- Direct drive extruder
- Auto bed leveling
- Klipper support
- Screen is optional (planning on using web GUI)
- Built=in belt tensioner (like Sovol SV07)
- Video monitoring (optional)
- Use a custom PCB (that can include the LEDs + accelerometer and would be super close to the nozzle)

***
### Day 1 (2/6/25):
**Goal for the day:** Preliminary research, figure out the basics of how a printer is made + what parts I would need to add in my BOM. <br>
**Why is this goal useful:** It allows me to better understand each part + helps me start planning the parts list, which affects the cost (duh) <br>
**Time spent:** 1.5hrs

#### Useful links:
- https://www.youtube.com/watch?v=yuAN5AzEWCg
- https://youtu.be/4VSu_gG-nlk?si=x5pDPoq5jk2_qxVh
- https://all3dp.com/2/direct-vs-bowden-extruder-technology-shootout/
- https://www.matterhackers.com/articles/anatomy-of-a-3d-printer?srsltid=AfmBOopqtgdCkqYFV2tYERDfQR2jrDC7kC8GteZoND3dc5894tnvVWVd
- https://www.thingiverse.com/thing:1752766

#### Info collected:
- ~~Steel chassis could be good~~ Too expensive in America, I should probably stick to aluminum channel
- Motion system: Z-axis would use a lead screw + 1 motor and move the bed up and down, more research is required for XY axes
- Motors: NEMA 17 motors appear to be the standard, LDO motors seems to be a good brand
- Belt: Apparently, the GT2 Timing belt is standard
- Controller board: BigTreeTech SKR Mini E3 is a really common controller board that isn't used much for CoreXY builds but is pretty good for a budget build
- Wiring: About as easy as making a PC, so not too bad
- Nozzle: Maybe use Bambu A1 nozzles? (This way I can use them for both printers)
- Overall parts: Motors for motion system + extruder, heatbed, frame, power supply, controller, hotend, bed leveling sensor, accelerometer (input shaping), limit switches, raspberry pi (for Klipper), cooling fans, something to hold the z-axis (probably lead screw), something to hold the xy axes (linear rods/rails)
- Filament for printer: PETG is good enough for everything, use PLA if you want for accent pieces + parts that aren't going to be under high stress (mechanical and/or temperature), Nylon CAN be printed on A1 mini if heat is REALLY a concern, but is much more expensive, and PETG will be fine for the toolhead
- Total parts list (need to research in greater detail):
  * Frame
    - Leadscrew/Threaded rods (for the Z-Axis)
    - Belts (for the XY axes)
    - Aluminum extrusion (normally T-slot or V-slot)
    - Smooth rods (for XY axes)
  * Toolhead
    - Hotend (Bambu hotends are ~$12 and have the heatsink + nozzle)
    - Heater cartridge (This actually heats up the filament)
    - Thermistor/Thermocouple/RTD (Lets you know what the temp of the hotend is)
    - Nozzle (Part of the Bambu hotend)
    - Part cooling fan (cools down the layer that was just printed)
    - Hotend cooling fan (cools the heatsink itself down, ensures that the plastic doesn't melt early, allowing for greater control)
  * Electronics
    - Heatbed
    - Controller (Actually controls the motors, heaters, etc. BigTreeTech SKR Mini E3 is a start for researching)
    - Computer (To run Klipper on, allows for faster processing, will likely be a Raspberry Pi)
    - Cooling fans
    - Limit switches
    - Bed leveling sensors
    - Accelerometer (For input shaping)
    - Motors (Normally NEMA 17 stepper motors that tend to have 200ppr)
    - LEDs (To allow you to see the part + for recording)
    - Camera (For print monitoring + videos + timelapses)
  * Other
    - Build plate
    - PTFE tube
    - Silicone sock (Bambu lab)
    - Nozzle cleaning (Like the Bambu Lab A1 Mini, completely optional, would be nice to have as a pre-print macro in Klipper)
   
    ***
### Day 2 (2/16/25):
**Goal for the day:** Make the BOM <br>
**Why is this goal useful:** Helps me finalize the cost of everything + lets me know what parts I'm using so I can start the CAD <br>
**Time spent:** 2hrs

#### Useful links:
- [Frames](https://youtu.be/E5FqrycYL40?si=j6Fz1LKAvbOmlVJB)
- [3D printed frames](https://youtu.be/5remLFeUT-k?si=JSoOi04MDNEIEDqR) (Not happening)
- [Motor controller, M8P](https://youtu.be/wPqDxiU8-5A?si=cE4t9tCw5YM5Fe2U)
- [Motor controller, E3EZ](https://youtu.be/B2tAd0lNgnc?si=KCBrcj5Dog0s6xvy)
- [Choosing the motors](https://youtu.be/RleJKkO6E64?si=XVJ-940wYRUIblx8)

#### Info collected:
[BOM Spreadsheet](https://docs.google.com/spreadsheets/d/12bk38MyKBaCSnbDqkn_daGvMrIUmXt25-RTHfP_S9RE/edit?usp=sharing)
