# Hybrid IIDX-SDVX Controller (DIY)
 
Last update: January 22nd 2017
I'll update in february-march when the rest of the stuff arrives.
 
<div style='float: center'>
  <img style='width: 200px' src='http://iidxsdvx.pancakeapps.com/pics/pic001.png'></img>
</div>

<hr>

Check http://iidxsdvx.pancakeapps.com for full instructions.

CODE INSTRUCTIONS:

Folder iidxsdvx/IIDX 9+1e+9leds/Arduino Leonardo/ contains 2 folders.


  * leovx: for low quality encoders (24ppr)
  
  * leovxhq: for high quality encoders (600ppr)

<hr>

# Variations

The code and CAD files included will let you make a DJDAO-size controller with interchangeable button plates, using an Arduino Leonardo to wire everything up.

Included in this tutorial you can choose from 2 variations:
 
- Beatmania IIDX Controller (9 buttons + Turntable + 9 LEDs)

- Beatmania IIDX+SDVX Controller (9 buttons + Turntable + 2 Knobs + 5 LEDs) 

You can either build just one of them or build both.
But you'd have to change the code everytime you change the button keypad layout.

Due to the number of pins it's imposible to have 3 encoders, 9 buttons and also have 9 LED's, so you either use me code (with only 5 LED's) or modify it to remove 1 encoder for 2 more LED's.

## Part List / Hardware

Most of these links are from chinese webpages that give world-wide free shipping (if you can wait 2 months). Buying locally is also a good option.

* Arduino Leonardo
* 1 High quality encoder (600ppr)
* 2 Rotary encoders (24ppr)
* 2 25x22 aluminum knobs
* 9 50x33 beatmania buttons
* 2 33x33 square buttons
* 9 Omron D2MV-01-1C3 (50gr.) microswitch
* Jumper wires
* Crimp connectors
* 400pin breadboard

## Part List / Building Materials

Most of these parts should be CNC cut or laser cut (which expensive). You can also use a cardboard box or wood MDF planks.
I used clear acrylic because it's cheaper, also using only one thickness will make it even less expensive.
**Main mounting plate**
* 3 or 5mm Black/Clear Acrylic with holes for button pad and disc encoder, also screw holes. I used 5mm clear acrylic, but I found out it's better to use 3mm black acrylic fr the DJDAO FPS look.

**Button pads**
* 5mm Clear acrylic with holes for buttons and encoders. Black looks way better, I used clear.
  
**Turntable mounting plate**
* 5mm Clear acrylic with holes for encoder and screws.
  
**Turntable base**
* 2x5mm round discs with holes for encoder and mounting screws. Use this base to bring your turntable to your desirable height.
  
**Turntable disc**
* 5mm round disc with hole to fit the encoder. You can also cover this with a rubber skin for maximum gripness. The acrylic itself is really slippery.

**Mounting Box**
* I used 9-12mm MDF for the box walls, 5,5mm MDF for the base and 3mm MDF for the back door. Every cut and hole was made by me with a saw and some sandpaper. Using an electric saw and a sandpaper machine is a lot easier.

I used what was available on the store, but on a next revision I'd go for 9mm walls, 3mm base and 3mm door, posibly made of acrylic.

<hr>

**PIN DIAGRAM**

The pins are assigned to every button and encoder. You'll see that the PCB has many pins from A0 to A5, and from 0 to 13, so you'll have 19 pins in total. Remember that buttons use one pin, but encoders will use 2 pins for the cheap ones and 3 pins for the high quality (Pending revision). The PCB also has 3 grounds (GND) to choose from.

This table shows configuration for both keypad layouts.

**Hybrid IIDX-SDVX Layout**

(revision pending)

<table><thead>
<tr>
<th>Button</th>
<th style="text-align: center">Pin #</th>
<th style="text-align: center">Button #</th>
</tr>
</thead><tbody>
<tr>
<td>FxR</td>
<td style="text-align: center">11</td>
<td style="text-align: center">Button 8</td>
</tr>
<tr>
<td>FxL</td>
<td style="text-align: center">12</td>
<td style="text-align: center">Button 9</td>
</tr>
<tr>
<td>BT-A</td>
<td style="text-align: center">13</td>
<td style="text-align: center">Button 7</td>
</tr>
<tr>
<td>BT-B</td>
<td style="text-align: center">A0</td>
<td style="text-align: center">Button 5</td>
</tr>
<tr>
<td>BT-C</td>
<td style="text-align: center">A1</td>
<td style="text-align: center">Button 3</td>
</tr>
<tr>
<td>BT-D</td>
<td style="text-align: center">A2</td>
<td style="text-align: center">Button 1</td>
</tr>
<tr>
<td>Start</td>
<td style="text-align: center">A3</td>
<td style="text-align: center">Button 4</td>
</tr>
<tr>
<td>Button 6</td>
<td style="text-align: center">A4</td>
<td style="text-align: center">Button 6</td>
</tr>
<tr>
<td>Button 2</td>
<td style="text-align: center">A5</td>
<td style="text-align: center">Button 2</td>
</tr>
</tbody></table>

BUtton 2 and 6 are not used in SoundVoltex unless you want to use them as the Service button and Test button (which I don't recommend)

<table><thead>
<tr>
<th>ENCODERS</th>
<th style="text-align: center">DATA 1</th>
<th style="text-align: center">DATA 2</th>
</tr>
</thead><tbody>
<tr>
<td>Encoder Right</td>
<td style="text-align: center">0</td>
<td style="text-align: center">1</td>
</tr>
<tr>
<td>Encoder Left</td>
<td style="text-align: center">2</td>
<td style="text-align: center">3</td>
</tr>
<tr>
<td>Encoder Turntable
<td style="text-align: center">4</td>
<td style="text-align: center">5</td>
</tr>
</tbody></table>

That leaves pin 6 to 10 for LEDS (5 buttons)

**Beatmania IIDX only Layout**


<table><thead>
<tr>
<th>Button</th>
<th style="text-align: center">Pin #</th>
<th style="text-align: center">Button #</th>
</tr>
</thead><tbody>
<tr>
<td>Start</td>
<td style="text-align: center">11</td>
<td style="text-align: center">Button 8</td>
</tr>
<tr>
<td>VFX</td>
<td style="text-align: center">12</td>
<td style="text-align: center">Button 9</td>
</tr>
<tr>
<td>Button 1</td>
<td style="text-align: center">13</td>
<td style="text-align: center">Button 1</td>
</tr>
<tr>
<td>Button 2</td>
<td style="text-align: center">A0</td>
<td style="text-align: center">Button 2</td>
</tr>
<tr>
<td>Button 3</td>
<td style="text-align: center">A1</td>
<td style="text-align: center">Button 3</td>
</tr>
<tr>
<td>Button 4</td>
<td style="text-align: center">A2</td>
<td style="text-align: center">Button 4</td>
</tr>
<tr>
<td>Button 5</td>
<td style="text-align: center">A3</td>
<td style="text-align: center">Button 5</td>
</tr>
<tr>
<td>Button 6</td>
<td style="text-align: center">A4</td>
<td style="text-align: center">Button 6</td>
</tr>
<tr>
<td>Button 7</td>
<td style="text-align: center">A5</td>
<td style="text-align: center">Button 7</td>
</tr>
</tbody></table>

<table><thead>
<tr>
<th>ENCODERS</th>
<th style="text-align: center">DATA 1</th>
<th style="text-align: center">DATA 2</th>
</tr>
</thead><tbody>
<tr>
<td>Encoder Tuntable
<td style="text-align: center">0</td>
<td style="text-align: center">1</td>
</tr>
</tbody></table>

That leaves pins 2 to 10 for LEDS (9 LEDS, enough for each button)

## Assembly / Building the controller

1. Take the keypad of your choose. In this case I'll be using the IIDX&SDVX hybrid keypad
2. Prepare buttons with the ammount of pressure you like (button + spring + led + microswitch)
3. Insert every button where it belongs and screw the plastic nut from bellow
4. Insert both cheap encoders and screw the nut from above.
5. Mount the disc mounting plate on the Main mounting plate with the screws.
6. Mount the disc base on top of the Disc mounting plate with screws.
7. Mount th ehigh quality encoder in it's place with 3 screws.
8. Turn around the main mounting plate and mount the Leonardo and Protoboard/Breadboard
9. Wire every pin on the Leonardo PCB with a pin on the Breadboard using jumper wires.
10. Also wire one Ground to the PCB.
11. Mount the keypad plate on the Main plate with screws.
12. Wire every button and LED with the breadboard using jumper wires.
13. Connect the PCB to the computer using a USB cable, and using Arduino IDE load the code into the Arduino Leonardo.
14. Finally mount the plate onto the mounting box and mount the disc on the high quality encoder.

If everything went right there should be a new Arduino controller on your pc.
Buttons 1 to 9 are the main buttons, and X and Y axis are both encoders.

<hr>

## Gallery

[Check out these awesome pictures!](http://imgur.com/a/Vh7uL)
