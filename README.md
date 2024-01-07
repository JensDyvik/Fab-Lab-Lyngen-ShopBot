# Fab-Lab-Lyngen-ShopBot
*Documentation of the ShopBot GRBL conversion at Fab Lab Lyngen*

The ShopBot at FabLab Lygen runs GRBL on an Arduino Uno. You can use any kind of CAM software that can make normal G-Code to make jobs for the machine. A quick guide is avaiable [here](https://docs.openbuilds.com/doku.php?id=docs:software:overview).

**Sugggested Free CAM software:**

 - [OpenBuildsCAM](https://cam.openbuilds.com/) *(easy to begin with)*
 - [FreeCAD](https://www.freecadweb.org/) *(advanced*)
 - [BarkBeetle](https://github.com/fellesverkstedet/Bark-beetle-parametric-toolpaths) *(requieres a Rhino License)*
 - [Fusion360](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwi71tWk-suDAxXpAhAIHec7BYoQFnoECBQQAQ&url=https%3A%2F%2Fwww.autodesk.com%2Fproducts%2Ffusion-360%2Fpersonal&usg=AOvVaw2Qpz756Hs5P4X8QVNBXLeT&opi=89978449) *(restricted functionality in free version)*

**Suggested Paid CAM software**

- [VCarve Pro Makerspace edition](https://www.vectric.com/products/makerspace)

### Running a job

We use OpenBuilds Control to send jobs / G-Codes to the machine. Documentation of of how to use this control software [here](https://docs.openbuilds.com/doku.php?id=docs:software:openbuilds-control).

- Place material on the machine bed
- Insert a milling bit in the spindle *(lefty loosey, righty tigthey)*
- Jog the machine to where you want X and Y zero to be and zero X and Y *(the buttons to left of the X and Y coordinates)*
- Set the Z Zero height with the probe plate *(ctr+p to start the macro)*
- Start the spindle by pressing the physical **RUN** button on the VFD *(the VFD is mounted on the wall)*
- Adjust spindle speed with up and down buttons *(multiply with 60: 300 = 18000 RPM and 150 = 9000 RPM)*
- Start the dust extraction
- Open your job / G-Code
- Start the job by pressing the play button
- When the job is done stop the spindle by pressing the **OFF** button and stop the dust extraction

### Differences between ShopBot3 and the GRBL control

- X axis is along the gantry and Y axis is away from you (swapped)
- You can now override feedrate in realtime
- You can now intantly see a preview of your job/path before you start it
- The X and Y homing switches are not wired *(pending)*


### To do

 - Fix electronics for 24V induction homing switches
 - Adjust lower v-wheel postions on X axis *(along gantry axis)*
 - Clean v-wheels on X and Y axis
 - Add new brushes to dust skirt
 - Surface the bed
