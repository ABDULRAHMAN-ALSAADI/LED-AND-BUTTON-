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


### 🧠 Code (Arduino)

int LEDR = 2;
int LEDY = 7;
int LEDG = 8;

int Butt0 = 4;
int Butt1 = 12;
int Butt2 = 13;
int BS0 = 0;
int BS1 = 0;
int BS2 = 0;

void setup() {
  pinMode(LEDR, OUTPUT);
  pinMode(LEDY, OUTPUT);
  pinMode(LEDG, OUTPUT);
  pinMode(Butt0, INPUT_PULLUP); // Use internal pull-up resistor
  pinMode(Butt1, INPUT_PULLUP);
  pinMode(Butt2, INPUT_PULLUP);
  
}

void loop() {
  BS0 = digitalRead(Butt0);
  if (BS0 == LOW){  
    digitalWrite(LEDR, HIGH);
}else
    digitalWrite(LEDR, LOW);
  
   BS1 = digitalRead(Butt1);
  if (BS1 == LOW){  
    digitalWrite(LEDY, HIGH);
}else
    digitalWrite(LEDY, LOW);
  
   BS2 = digitalRead(Butt2);
  if (BS2 == LOW){  
    digitalWrite(LEDG, HIGH);
}else
    digitalWrite(LEDG, LOW);
  

}

