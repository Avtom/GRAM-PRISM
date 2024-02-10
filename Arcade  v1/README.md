# GRAM PRI$M ARCADE VERSION

## Introduction

This is an experimental version of the [PRI$M](https://github.com/GrammyMoney/GRAM-PRISM) that fit 24mm and 30mm, relatively low profile, arcade buttons instead of Kaith Choc mini switches.
The goal is to have very fast buttons (short activation point and short bottom out) while keeping your wrist is a comfortable and effective position.
The controller is powered by [RP2040 Advanced Breakout Board](https://github.com/OpenStickCommunity/Hardware/tree/main/RP2040%20Advanced%20Breakout%20Board) running a [GP2040-CE firmware](https://github.com/OpenStickCommunity/GP2040-CE).

## Dev log

Here is the different steps taken to create this version of the **PRI$M** so far:
- Print the stl frame (through JLBPCB)
- Use cardboard to prototype the layout of the different panels
    - Using a circular cutter make that process way easier
    - It was good opportunity to check that there is enough room under the panels for all the buttons to fit
    - Different version of the layout have been born out of this experiment, with different placement and size of the Aux buttons (start, select, etc) and with and without a focus mode button
- Import the dxf of the GRAM PRI$M V1 in illustrator and replicate the layout prototyped before
- Generate a new dxf out of the illustrator files.
- Import the dxf in Autodesk Fusion and extrude the surface to create an stl file.
    - stl files are not mandatory, but it was use to 3D print the panels in order to find out possible mistake made in the creation process so far (and one issue was found with the wrong unit being used)