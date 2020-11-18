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
