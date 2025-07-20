# LED-AND-BUTTON-
## 🔴🟢 Button-Controlled LED System – Arduino Uno


This is a simple Arduino Uno project created using Tinkercad Circuits. The system features 3 push buttons and 3 LEDs connected to an Arduino Uno. Each button controls a corresponding LED—press a button, and the assigned LED lights up.


#### 🔧 What It Does:
Press Button 1 → LED 1 (Red) lights up

Press Button 2 → LED 2 (Yellow) lights up

Press Button 3 → LED 3 (Green) lights up

Releasing the button turns off the LED (momentary behavior)


### 🧰 Components Used:
Arduino Uno

Breadboard

3x Push Buttons

3x LEDs (Red, Yellow, Green)

3x 220Ω Resistors (LED current limiting)

Jumper wires

Optional: External Pull-down Resistors (not used here, using internal pull-ups)


### 💡 Circuit Design Highlights
Internal pull-up resistors are enabled in code to simplify wiring.

Buttons are connected between the digital input pins and GND.

LEDs are connected to digital output pins with current-limiting resistors.
