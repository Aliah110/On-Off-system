# Push-Button-and-LED-control-with-the-Arduino

The Design in tinkercad Open the link : 
https://www.tinkercad.com/things/2siMxeUBJhd

## Hardware Required 
- Arduino Uno 
- Relay DPDT
- LED 
- Button 
- Resistor 
- Wires 
- Breadboard
- Light bulb
- 9V Battery


## Steps :
- LED attach to board .
- Resistor connect to LED's long leg ( + ).
- The wire connect to resistor's other leg .
- Wire connect to digital pin 2 from resistor.
- Wire connect to LED's short leg , after that wire connect to ground from LED.
- The button attach to board .
- Resistor connect to button leg .
- wire connect to resistor leg , after that wire connect ground from resistor .
- wire connect to button's other leg , after that connect to 5V from button .
- Wire connect to button's top leg , after that connect to digital pin4 from button .

## Circuit design :
![Tremendous Wolt-Blad (3)](https://user-images.githubusercontent.com/108204114/182014336-b12c453f-5b4e-48fe-8c7f-c9cae1a4a8df.png)

## The Code :
```
#define LED_PIN 2
#define BUTTON_PIN 4
#define Relay_PIN 7


byte lastButtonState = LOW;
byte ledState = LOW;



void setup() {
  pinMode(LED_PIN, OUTPUT);
  pinMode(BUTTON_PIN, INPUT);
  pinMode(Relay_PIN, OUTPUT);
}
void loop() {
  byte buttonState = digitalRead(BUTTON_PIN);
  if (buttonState != lastButtonState) {
    lastButtonState = buttonState;
    if (buttonState == LOW) {
      ledState = (ledState == HIGH) ? LOW: HIGH;
      digitalWrite(LED_PIN, ledState);
      digitalWrite(Relay_PIN, ledState);
    }
  }
}
```
## The simulation 
<img width="538" alt="image" src="https://user-images.githubusercontent.com/108204114/182014585-dc5239e9-da8c-47c1-ade6-ba4e56f0f2f9.png">

Reference : <br>
- https://youtu.be/58Ynhqmvzoc
- https://roboticsbackend.com/arduino-turn-led-on-and-off-with-button/

