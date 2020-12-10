# Not-So-Basic-Arduino
Arduino work folder


## LED Blink

### Description
I made and LED blink

### Code
void setup() {
    pinMode(11, OUTPUT);
}
void loop() {
    analogWrite(11,255);   
   
    delay(100);
   
    analogWrite(11,200);
    
    delay(100);
    
    analogWrite(11,150);
    
    delay(100);
    
    analogWrite(11,100);
    
    delay(100);
    
    analogWrite(11,50);
    
    delay(100);
    
    analogWrite(11,0);
    
    delay(500);
    
}

### Reflection
I learned how to make and LED blink using analogWrite 

---
## Hello Functions

### Description
Using an ultrasonic senser I moved a servor motor.

### Code
/*
   HC-SR04 example sketch
  getDist function based from this,
   https://create.arduino.cc/projecthub/Isaac100/getting-started-with-the-hc-sr04-ultrasonic-sensor-036380

   by Isaac100
*/
#include <Servo.h>
const int trigPin = 9;
const int echoPin = 10;
Servo motor;

void setup() {
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  motor.attach(11);
  Serial.begin(9600);
}

void loop() {

  Serial.print("Distance: ");
  Serial.println(getDist());
  delay(100);
  if (getDist() > 20) {
    motorRight();
  }
  else {
    motorLeft();
  }
}

int getDist() {
  long duration;
  int distance;
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  duration = pulseIn(echoPin, HIGH);
  distance = (duration * .0343) / 2;
  return distance;

}

void motorRight() {
  motor.write(60);
}

void motorLeft() {
  motor.write(150);
}
### Reflection
I had a really hard time on this but I eventually got it with lots of help. I did learn how to use a servo motor and a ultrasonic senser.
