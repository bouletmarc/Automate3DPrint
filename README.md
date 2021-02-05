# Automate3DPrint

Automate your 3D Printer with this GCODE Mod

# How it's work

You can modify the GCODE of your printer to print several parts while freeing up the space used by the last printing session before starting the new one.

# How to do it

There are two ways to do this, either by manually modifying your gcode using a text editor or by using the supplied software 'Automate3DPrint.exe'.

-Method #1 (Modifying your own GCODE)

To modify your GCODE so that your printer prints several parts and have the bed cleaned up between every parts, you will have to remove the end of printing code in the GCODE, then add the automation code shared here on github (AutomateCode.txt), add again the printing code of the part that you want (without having the end printing code!) and repeat the process for the desired number of repetitions, then after it's done, add the end of printing code back again. 

-Method #2 (Using Automate3DPrint.exe)

To use the Automate3DPrint.exe, load your desired GCODE that your want to repeat the printing and put the repetition amount that you desire then save again your gcode. (Use the 'Save As' button if you want to save a new file and not overwrite the file that you previously loaded!)

# Suggestions

I suggest that you DO NOT USE Any Build Plate Adhesion or atleast not the Skirt type. The Skirt will have issue getting removed from the bed which get lead to printing failure toward the nexts prints.

# Codes Informations

- MOVE OUT THE WAY

This is almost the Ending Code of a print. It will move up and away the Hotend a bit and also retract a bit.

- MOVE CENTER

Move the Hotend to the center coordination and down (X110 Y110 = the center of the Ender3 V2 Build plate)

- COOLDOWN

Stop Fan, Stop Bed Heating, Stop Hotend Heating, then wait til the Bed cooldown to the desired Temperature (Default: 35 Celsius)

- MOVE PARTS

Move the Hotend so that it push the last printed part
