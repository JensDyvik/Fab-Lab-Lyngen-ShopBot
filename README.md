# Fab-Lab-Lyngen-ShopBot
*Documentation of the ShopBot GRBL conversion at Fab Lab Lyngen*

The ShopBot at FabLab Lygen runs GRBL on an Arduino Uno. You can use any kind of CAM software that can make normal G-Code to make jobs for the machine. A quick guide is avaiable [here](https://docs.openbuilds.com/doku.php?id=docs:software:overview).

**Free CAM software you can use:**

 - OpenBuildsCAM *(Easy to begin with)*
 - FreeCAD *(Advanced*)
 - BarkBeetle *(requieres a Rhino License)*
 - Fusion360 *(restricted functionality in free version)*

**Paid CAM software**

- VCarve Pro Makerspace edition

### Running a job

We use OpenBuilds Control to send jobs / G-Codes to the machine. Documentation of of how to use this control software [here](https://docs.openbuilds.com/doku.php?id=docs:software:openbuilds-control).

- Place material on the machine bed
- Insert milling bit in the spindle *(lefty loosey, righty tigthey)*
- Jog the machine to where you want X and Y zero to be and Zzro X and Y *(the buttons to left of the coordinates)*
- Set the Z Zero height 
- Start the spindle by pressing the physical RUN button on the VFD *(the VFD is mounted on the wall)*
- Adjust spindle speed with up and down buttons *(multiply with 60, 300 = 18000 RPM and 150 = 9000 RPM)*

### Differences between ShopBot3 and the GRBL control

- X axis is along the gantry and Y axis is away from you (swapped)
- You can now override feedrate in realtime
- You can now intantly see a preview of your job/path before you start it
- The X Y and homing switches are not wired *(pending)*


### To do

 - Fix electronics for 24V induction homing switches
 - Adjust lower v-wheel postions on X axis *(along gantry axis)*
 - Clean v-wheels on X and Y axis
 - Add new brushes to dust skirt
