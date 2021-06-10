# Convex Touch surface project

This is a complete guide to implement touch on a convex shape. The guide utilises unity as a car simulation to try navigation of a vehicle using touch on a convex shape and regular joystick (xbox One Controller using bluetooth) for research purposes. 

### Hardware requirements

- Microchip AVR128DA48 Curiosity Nano Evaluation Kit (https://www.microchip.com/Developmenttools/ProductDetails/DM164151)
- QT8 Xplained Pro Extention Kit (https://www.microchip.com/developmenttools/ProductDetails/AC164161)
- Curiosity Nano Touch Adapter (https://www.microchip.com/developmenttools/ProductDetails/AC80T88A)
- Xbox One Controller (https://www.xbox.com/da-dk/accessories/controllers/xbox-wireless-controller#white)

### Required requipment and materials
- Dual extrude 3D printer (Ultimaker S5 in our case)
- Conductive filament (Proto pasta, but other conductive filaments works as well)
- PLA plastic
- Conductive paint (https://www.bareconductive.com/blogs/blog/what-is-electric-paint-the-composition-and-application-of-conductive-paints)

### Required software (free)
- Microchip Studio (https://www.microchip.com/en-us/development-tools-tools-and-software/microchip-studio-for-avr-and-sam-devices)
- Unity (https://unity3d.com/get-unity/download)
- Microsoft Visual Studio (https://visualstudio.microsoft.com/vs/)

### Provided code in this project
- Microchip Studio project for retriving touch input from the AVR128DA48 (can be found here: https://drive.google.com/drive/folders/1C58eHFaWfg5DDBVdRvJmySgB696HPGgb?usp=sharing)
- Complete unity project to run simulation including scrip to retrieve touch input from the touch surface (can be found here: https://drive.google.com/drive/folders/1WipsEkQ0Yfhp3_48dP_lTpbd8AY_Ymgy?usp=sharing)

### 3D models for printing
- Convex shape in a SolidWorks Assembly

## Credits and thanks to
- Vehicle Phycis Pro (https://vehiclephysics.com/)

## Get started

1. Download Microchip Studio and Connect AVR128DA48 using a data USB-A to USB-Micro-b
2. Once conneted, build the provided Microchip Studio project onto the AVR128DA48
3. (Debugging) - Using PuTTY or Digi XCTU, open a serial console using our COM port (COM3 in our case), baudrate=38400, data bits=8, Parity=None, Stop Bits=1 and Flow Control = None and confirm the setup coordinates
4. The unity project has 4 scenes, which can be found in Assets/Vehicle Phycis Pro/Scenes. A scene test, Scene 1, Scene 2 and Scene 4.
5. Make sure when you load each scene, that you have chosen your desired input controller, either joystick or touch input. Navigate in the Hierarchy in the left and choose "VPP Sport Coupe" and select "COM". You should now see two scripts, enable the one you want to use and try it out.
6. The default COM port is COM3, edit to fit your specific COM port in SerialComm script (can be found in PuTTY or Digi XCTU)
7. Note that if you want to use joystick, simple connect the Xbox controller using bluetooth in Windows. When you have a connection, unity will write in the button that it is connected and ready to use. Just make sure to select it as described in step 5
8. Print the provided 3d model that supports touch on a convex shape.
9. Using conductive paint, which acts as glue, place it on the 3d printet model and place on the QT8 Xplained Pro touch surface. Make sure to fit it precicely and with enough conductive paint to insure a good connection
10. Ready to use both convex shape and joystick in the car simulation 
11. When the joystick or touch surface is used, unity automatically creates a txt file with the coordinates and timestamp. This can be used for tracking the driving route



