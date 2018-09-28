# MOREARDUINOCODE
//MIKE LOOK ARDUINO CODE for potentiometer

/*
Potentiometer and switching LEDs

programming 
 

 Source: http://www.arduino.cc/en/Tutorial/AnalogInput
*/

int sensorPin = A0;    // select the input pin for the potentiometer
int ledPin = 13;
int ledPin2 = 12;
int ledPin3 = 11;
int ledPin4 = 10;      // select the pin for the LED
int sensorValue = 0;  // variable to store the value coming from the sensor

void setup() {
  // declare the ledPin as an OUTPUT:
   pinMode(ledPin, OUTPUT);
  pinMode(ledPin2, OUTPUT);
  pinMode(ledPin3, OUTPUT);
  pinMode(ledPin4, OUTPUT);
}

void loop() {
 // 
 int val = analogRead(sensorPin);
  val = map(val, 0, 1023, 10, 13);    //if potentiometer is at a certain level between 0 and 1023, the repsective ledPin will turn on and the others will turn off
    
   if (val == 10){
    digitalWrite(ledPin, HIGH);
    digitalWrite(ledPin2, LOW);
    digitalWrite(ledPin3, LOW);
    digitalWrite(ledPin4, LOW);
   }

    if (val == 11){
    digitalWrite(ledPin, LOW);
    digitalWrite(ledPin2, HIGH);
    digitalWrite(ledPin3, LOW);
    digitalWrite(ledPin4, LOW);
   }
    if (val == 12){
    digitalWrite(ledPin, LOW);
    digitalWrite(ledPin2, LOW);
    digitalWrite(ledPin3, HIGH);
    digitalWrite(ledPin4, LOW);
   }
    if (val == 13){
    digitalWrite(ledPin, LOW);         
    digitalWrite(ledPin2, LOW);  
    digitalWrite(ledPin3, LOW);
    digitalWrite(ledPin4, HIGH);
    }
}
