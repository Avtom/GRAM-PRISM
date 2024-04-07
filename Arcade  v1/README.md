# GRAM PRI$M ARCADE VERSION

## Table of Content
- [Introduction](#Introduction)
- [How to build the exact same model](#How-to-build-the-exact-same-model)
- [How to modify it and make it even better](#How-to-modify-it-and-make-it-even-better)
- [Dev log](#Dev-log)

## Introduction

This is an experimental version of the [PRI$M](https://github.com/GrammyMoney/GRAM-PRISM) that fit 24mm and 30mm, relatively low profile, arcade buttons instead of Kaith Choc mini switches.
The goal is to have very fast buttons (short activation point and short bottom out) while keeping your wrist in a comfortable and straight position.
The controller is powered by [RP2040 Advanced Breakout Board](https://github.com/OpenStickCommunity/Hardware/tree/main/RP2040%20Advanced%20Breakout%20Board) running the [GP2040-CE firmware](https://github.com/OpenStickCommunity/GP2040-CE).

## How to build the exact same model

## How to modify it and make it even better


## Dev log

Here is the different steps taken to create this version of the **PRI$M**:
- Print the stl frame (through JLBPCB)
- Use cardboard to prototype the layout of the different panels
    - Using a circular cutter made that process way easier
    - It was a good opportunity to check that there is enough room under the panels for all the buttons to fit
    - Different version of the layout have been born out of this experiment, with different placement and size of the Aux buttons (start, select, etc) and with and without a focus mode button
    - Tip: the correct way of holding the Prism is with the top middle edge perpandicular to you. Meaning the controller will be tilted with your right hand closer to you than your left hand.


- Import the dxf of the GRAM PRI$M V1 in illustrator and replicate the layout prototyped with the cardboard
    - [Ai files](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/illustrator)
- Generate a new dxf out of the illustrator files.
    - [Dxf files](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/dxf)
- Import the dxf in Autodesk Fusion and extrude the surface to create an stl file.
    - stl files are not mandatory, but it was used to 3D print the panels in order to find out possible mistake made in the creation process so far (and one issue was found with the wrong unit being used). 
        - [Stl files](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/stl/stl%202mm%20thick)
- Checking the layout with a cardboard has it’s limits. It was nice to figure out if how buttons fits in the frame and how to place them under fingers but the lack of rigidity prevented in game testing while playing at full speed. This is where the 3D prints became handy and revealed flaws of the early cardboards layouts (things getting tiring after 30 min of playing tense matches, etc)
    - Lots of iterations were printed to until a good, playable, layout was found.
- The art for panels has been designed in Photoshop and the exported in png
    - [Photoshop files](https://github.com/Avtom/GRAM-PRISM/tree/arcade-V1/Arcade%20%20v1/art)
- Once the layout were locked, then the last step was designing the panels in KiCad (as we are basically manufacturing aluminium pcb to make metal panels).
    - Import the dxfs as graphics for the edge.cuts layer
    - Import the art in the bitmap tool of Kicad and then copy/paste it as a silkscreen layer.
    - Plot everything to export the gerber files
- Order the pcbs (through JLBPCB again)
- Assemble the beast.
    - With some improvisation on the usb-c passthrough part… initial plan didn’t worked out so some spare plastic part have been glued and the cable tapped to stay in place
    - Outside of the top panels that are screwed, all the others are glued with some super glue.
