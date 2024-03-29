# Fab-Lab-Lyngen-ShopBot

The ShopBot at FabLab Lyngen is a [CNC router](https://en.wikipedia.org/wiki/CNC_router) controlled by [GRBL](https://github.com/gnea/grbl/wiki) on an Arduino Uno. You can use any kind of CAM software that makes normal G-Code to make jobs for the machine. A quick guide is available [here](https://docs.openbuilds.com/doku.php?id=docs:software:overview).

**Suggested Free CAM software:**

 - [OpenBuildsCAM](https://cam.openbuilds.com/) *(easy to begin with)*
 - [FreeCAD](https://www.freecadweb.org/) *(advanced*)
 - [BarkBeetle](https://github.com/fellesverkstedet/Bark-beetle-parametric-toolpaths) *(requires a Rhino License)*
 - [Fusion360](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwi71tWk-suDAxXpAhAIHec7BYoQFnoECBQQAQ&url=https%3A%2F%2Fwww.autodesk.com%2Fproducts%2Ffusion-360%2Fpersonal&usg=AOvVaw2Qpz756Hs5P4X8QVNBXLeT&opi=89978449) *(restricted functionality in free version)*

**Suggested Paid CAM software**

- [VCarve Pro Makerspace edition](https://www.vectric.com/products/makerspace)

![](/img/lyngen-shopbot.jpg)

### Running a job

We use OpenBuilds Control to send jobs / G-Codes to the machine. Documentation of how to use this control software [here](https://docs.openbuilds.com/doku.php?id=docs:software:openbuilds-control).

1. Place/fixture your material on the machine bed
2. Insert a milling bit in the spindle *(lefty loosey, righty tigtehy)*
3. Jog the machine to where you want X and Y zero to be and zero X and Y *(the buttons to left of the X and Y coordinates)*
4. Set the Z Zero height with the probe plate *(ctr+p to start the macro)*
5. Start the spindle by pressing the physical **RUN** button on the VFD *(the VFD is mounted on the wall)*
6. Adjust spindle speed with up and down buttons *(multiply with 60: 300 = 18000 RPM and 150 = 9000 RPM)*
7. Start the dust extraction
8. Open your job / G-Code
9. Start the job by pressing the play button
10. When the job is done stop the spindle by pressing the **OFF** button and stop the dust extraction

![](/img/instruction-graphics.png)

### Setting up

- Plug the three-phase power cable and single-phase extension cord into the outlets by the entrance to the barn. *(the thee phase spindle cable shares a socket with the hay separator machine and the single phase extension cord for the dust extraction shares a socket with electric fence for the horses)*.
- Turn on the ShopBot control cabinet with the switch mounted on the wall in between the VFD and the electrical enclosure.
- Warm up the spindle by running it in the air for 5 minutes. *(Start the spindle by pressing the physical **RUN** button on the VFD, stop the spindle with the red the **OFF** button)*

### Differences between ShopBot3 and the GRBL control

- The X axis is along the gantry and the Y axis is away from you (swapped)
- You can now override the feedrate in real-time
- You can now instantly see a preview of your job/path before you start it
- The X and Y homing switches are not wired *(pending)*


### To do

 - Fix electronics for 24V induction homing switches
 - Adjust lower v-wheel positions on X axis *(along gantry axis)*
 - Clean v-wheels on X and Y axis
 - Add new brushes to the dust skirt
 - Surface the bed
