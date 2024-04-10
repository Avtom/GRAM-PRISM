# GRAM PRI$M ARCADE VERSION

## Table of Content
- [Introduction](#Introduction)
- [How to build the exact same model](#How-to-build-the-exact-same-model)
- [How to modify it and make it even better](#How-to-modify-it-and-make-it-even-better)
- [Dev log](#Dev-log)

## Introduction

![Arcade](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/arcade-1.jpg "Arcade")

This is an experimental version of the [PRI$M](https://github.com/GrammyMoney/GRAM-PRISM) that fit 24mm and 30mm, relatively low profile, arcade buttons instead of Kaith Choc mini switches.
The goal is to have very fast buttons (short activation point and short bottom out) while keeping your wrist in a comfortable and straight position.
The controller is powered by [RP2040 Advanced Breakout Board](https://github.com/OpenStickCommunity/Hardware/tree/main/RP2040%20Advanced%20Breakout%20Board) running the [GP2040-CE firmware](https://github.com/OpenStickCommunity/GP2040-CE).



## How to build the exact same model

### Bill of materials
- 1 x GRAM PRI$M Frame
    - [stl  here](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/stl/gram%20prism%20v1%20frame.stl)
    - [instructions here](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1?tab=readme-ov-file#the-frame)
- 1 x set of Arcade PRI$M Aluminum Panels
    - [look for the .zip files in the exported for JLBPCB folders](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/kicad)
    - [instructions here](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1?tab=readme-ov-file#the-panels)
        - Please note that the minimum quantity that you can order is 5 for each panel. Maybe try to find other interested person on discord?
        - Please note that black panels cost significantly more than white one (in case you don’t care about the color)
- 5 x 30mm buttons and 14 x 24mm low profile arcade buttons.
    - The challenge is to find buttons that are not too deep because of the limited space inside the Prism, especially on the side.
        - Punk workshops one are OK, Quanba Gravity KS most likely OK.
	- Sanwa snap-ins and Crowns 202/204 are NOGO.
    - Max diameter of the rim is 29mm for the 24mm buttons and 34mm for the 30mm buttons
- (if you go with snap-in buttons) 1 set of 22-24mm rubber o-rings (likely 2mm thick) and 1 set of 28mm one. 
    - To compensate for the 1.6mm thickness of the panels which is significantly thinner than normal arcade stick enclosure.
- ON/OFF button of 21mm of diameter ([I used this one](https://focusattack.com/mini-round-2-pin-spdt-on-off-rocker-switch-black/))
- Some padding for the bottom panel (foam or rubber). [I went with rubber ones to add more weight to the controller](https://www.amazon.ca/dp/B09KC846TX)
- Wires (typical harness for leverless works well. Depending of the board you will use, you might need extra wires to jst-2pin to connect the ON/OFF and one of the Aux front button. )
- Advanced break board (I used a 5.2 one from [TheTrain](https://github.com/TheTrainGoes)).
- (optional) Adhesive PCB feets to keep the board on the inside of the resin panel. [Example](https://focusattack.com/3mm-hole-low-profile-adhesive-pcb-feet-set-of-4/)
- 8 x low profile M5x0.8 8mm screws.([the ones I used](https://makerparts.ca/products/low-profile-screws-m5?variant=16606601284))
- Usb-c male (90 angle) to female cable (20cm). [Went with a flat ribbon one](https://www.amazon.ca/Degree-Angled-Ribbon-Standard-Charging/dp/B07C4RD344).
- (optional) Mx tilters if you want to adjust the angle of some of the fingers. [I used that](https://3dkeycap.com/products/mx-tilters-adapters-10-pack)     

### Tools
- Solder iron (if you can’t find wires with some connectors on it)
- Super glue or 3M tape for the panels without screws
- Some electrical tape to hold the usb-c femal in place. (not super clean, there is way of doing better than that)

### Assembly
1. Connect the usb-c cable and harness to the board.
2. Stick the board inside of the frame on the back panel (the only one that is part of the frame) to avoid having the board touching the metal panels (for static eletricity)
    - ![assembly 1](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly1.jpg "Assembly 1")
3. Get the back panel ready:
    1. Install/solder the cables on the button
    2. Put the button in place
	- ![assembly 2](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly2.jpg "Assembly 2")
    3. Connect the cable to the board
4. Get the usb female in place
    - ![assembly 3](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly3.jpg "Assembly 3")
5. Get the front pannel ready:
    1. Put the button in place and glue the board
       - ![assembly 4](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly4.jpg "Assembly 4")
6. Get the bottom pannel ready:
    1. Cut a rectangle in the foam/rubber if you want the GP2040-CE logo visible
    2. Stick the pad on the bottom panel and cut what remains on the sides after
    3. Glue the panel to the frame.
        - ![assembly 5](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly5.jpg "Assembly 5")
        - ![assembly 6](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly6.jpg "Assembly 6")
        - with the glue in ![assembly 7](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly7.jpg "Assembly 7")
7. Get the 2 top pannel ready:
    1. Get the bottons in. Don’t forget the o-rings if you are using snaps-in.
        - ![assembly 8](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly8.jpg "Assembly 8")
    2. Do the wiring
        - ![assembly 9](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/Assembly9.jpg "Assembly 9")


## How to modify it and make it even better

- If you want to iterate on the layout of the buttons, you can use the .ai files.
   - Make sure the buttons are not too close from each others
   - Keep using mm as a unit everywhere
   - Use the helpers to see where the inner layer of the frame stops
   - When done, export to dxf (in illustrator you need to select the shapes who want, then export, then there is a checkbox for exporting only the selected ones)
   - Need dxf can be imported in kicad (as graphics) if you want metal panels, but I recommand 3D printing them first to validate the layout is playable (I used Autodesk fusion to extrude the shape. 2mm thick is ok)

- if you want to change the art, the .psd files is available. But basically you just need to export 5 png (one for each panel) that you will be able to import in Kicad (the art to bitmap convertor).
   - For metal panels, only black and white art works.
   - In photoshop you can make a selection, rotate it, and then copy the content of the selection, that you can open a new file and copy it inside then export.
   - All the masks and the layout overlay are just helpers, you don’t want to export with them on. (in Photoshop: shift-click to activate or desactivate a mask. Alt + drag and drop to duplicate a mask on a different layer)

## What should be improved first?

- The usb-c passthrough situation is the first thing that needs to be dealt with.
   - Dirty solution is to move the usb-c somewhere else and instal a typical passthrough that you can find in most arcade shops
   - The better solution is to take the usb-c breakout pcb from the original [PRI$M](https://github.com/GrammyMoney/GRAM-PRISM) and modify it to be a passthrough instead of one that end with a JST connector.

## Dev log

Here is the different steps taken to create this version of the **PRI$M**:
- Print the stl frame (through JLBPCB)
- Use cardboard to prototype the layout of the different panels
    - Using a circular cutter made that process way easier
    - It was a good opportunity to check that there is enough room under the panels for all the buttons to fit
        - ![cardboard test 1](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/cardboard-check-room1.jpg "Card board test 1")
        - ![cardboard test 2](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/cardboard-check-room2.jpg "Card board test 2")
    - Different version of the layout have been born out of this experiment, with different placement and size of the Aux buttons (start, select, etc) and with and without a focus mode button
    - Tip: the correct way of holding the Prism is with the top middle edge perpandicular to you. Meaning the controller will be tilted with your right hand closer to you than your left hand.
    - ![cardboard layout 1](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/cardboard-layout1.jpg "Card layout test 1")
    - ![cardboard layout 2](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/cardboard-layout2.jpg "Card layout test 2")
    - ![cardboard layout 3](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/cardboard-layout3.jpg "Card layout test 3")
    - ![cardboard layout 4](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/cardboard-layout4.jpg "Card layout test 4")
    - ![cardboard front layout](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/cardboard-front-layout1.jpg "Card front layout")
- Import the dxf of the GRAM PRI$M V1 in illustrator and replicate the layout prototyped with the cardboard
    - [Ai files](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/illustrator)
- Generate a new dxf out of the illustrator files.
    - [Dxf files](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/dxf)
- Import the dxf in Autodesk Fusion and extrude the surface to create an stl file.
    - stl files are not mandatory, but it was used to 3D print the panels in order to find out possible mistake made in the creation process so far (and one issue was found with the wrong unit being used). 
        - [Stl files](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/stl/stl%202mm%20thick)
- Checking the layout with a cardboard has it’s limits. It was nice to figure out if how buttons fits in the frame and how to place them under fingers but the lack of rigidity prevented in game testing while playing at full speed. This is where the 3D prints became handy and revealed flaws of the early cardboards layouts (things getting tiring after 30 min of playing tense matches, etc)
    - Lots of iterations were printed to until a good, playable, layout was found.
      - ![3D print layout 1](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/3D-print-1.jpg "3D print layout 1")
      - ![3D print layout 2](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/3D-print-2.jpg "3D print layout 2")
      - ![3D print layout 3](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/3D-print-3.jpg "3D print layout 3")
      - ![3D print layout 4](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/3D-print-4.jpg "3D print layout 4")
      - ![3D print layout 5](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/3D-print-5.jpg "3D print layout 5")
- The art for panels has been designed in Photoshop and the exported in png
    - [Photoshop files](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/art)
- Once the layout were locked, then the last step was designing the panels in KiCad (as we are basically manufacturing aluminium pcb to make metal panels).
    - Import the dxfs as graphics for the edge.cuts layer
    - Import the art in the bitmap tool of Kicad and then copy/paste it as a silkscreen layer.
    - Plot everything to export the gerber files
- Ran into problem with the hand screws I had that happened to be be to tall and in the way when holding the controller.
    - ![Smaller Screws 1](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/smaller-screws-1.jpg "Smaller screws 1")
    - ![Smaller Screws 2](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/smaller-screws-2.jpg "Smaller screws 2")
- Order the pcbs (through JLBPCB again)
   - ![Metals panels](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/explosed.jpg "Metal Panels")
- Assemble the beast.
    - With some improvisation on the usb-c passthrough part… initial plan didn’t worked out so some spare plastic part have been glued and the cable tapped to stay in place
    - Outside of the top panels that are screwed, all the others are glued with some super glue.
    - First steps of the assembly:
        - ![Without Buttons 1](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/without-button-1.jpg "without button 1")
	- ![Whitout Buttons 2](https://github.com/Avtom/GRAM-PRISM/blob/arcade-V1/Arcade%20%20v1/documentation/without-button-1.jpg "without button 2")
