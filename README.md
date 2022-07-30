# Push-Button-and-LED-control-with-the-Arduino

The Design in tinkercad Open the link : 
https://www.tinkercad.com/things/2siMxeUBJhd 

## Hardware Required 
- Arduino Uno 
- LED 
- Button 
- Resistor 
- Wires 
- Breadboard

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
![Tremendous Wolt-Blad](https://user-images.githubusercontent.com/108204114/181375273-fde23609-cf11-4910-a68e-3c4dabc81fa1.png)

## The Code :
```
//set pin numbers
const int ledPin = 2;         //const won't change
const int buttonPin = 4;

//variables will change
int buttonState = 0;          //variables for reading the pushbutton status

void setup() {

  Serial.begin(9600);
  pinMode(ledPin, OUTPUT);    //initialize the LED pin as an output
  pinMode(buttonPin, INPUT);  //initialize the pushbutton pin as an output
}

void loop() {

  buttonState = digitalRead(buttonPin); //read the state of the pushbutton value

  if (buttonState == HIGH) {            //check if the pushbutton is pressed
    //if it is, the buttonState is HIGH
    digitalWrite(ledPin, HIGH);         //turn LED on    
    Serial.println("LED ON +++++++"); 
  }
  else {

    digitalWrite(ledPin, LOW);          // turn LED off
    Serial.println("LED OFF -------");
  }

}
```
## The simulation 
<img width="959" alt="image" src="https://user-images.githubusercontent.com/108204114/181376950-1fa2e826-7688-40d1-b6a7-49867899a1e3.png">

Reference : <br>
https://youtu.be/58Ynhqmvzoc

