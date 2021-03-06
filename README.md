# Arduino circuit to control 5servo motors
* **Design an Arduino circuit to control 5 servo motors .**<br>
 * **Program the servo motors at 90 deg .** <br>
 * **Control the motors by using potentiometer.** <br>

## ❶ The design
 

 <div> The circuit was designed using <a href=https://www.tinkercad.com/dashboard>Tinkercad website. </a> &nbsp; <img width="100" src="https://user-images.githubusercontent.com/52053143/127372588-fb30e614-62b4-4f9a-bda3-eaf2061234e0.png"> </div> <br> 
 
**The Steps:**
 
  1. Research and selection of tools required for the work of the circuit.
 <div> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img width="150"  alt="2" src="https://user-images.githubusercontent.com/52053143/127376455-828c7581-9515-4936-8cb5-2cb90df3aab2.png"> <img width="150" alt="4" src="https://user-images.githubusercontent.com/52053143/127376471-b2a52950-3f6f-4a7d-ac1c-1581f9f0f402.png"> <img width="100" alt="3" src="https://user-images.githubusercontent.com/52053143/127376479-fa99dd17-fca5-4764-ab6f-847b3c5382f5.png">
 </div>
  <br>
   2. Connect the contents of the circuit to each other
   


![Mighty Blorr-Allis](https://user-images.githubusercontent.com/52053143/127379225-e7b40c0e-a877-47f6-bc79-72eaedc11fe9.png)
<br><br>
***
## ❷ Program the servo motors at 90 degree

Programming the circuit in C++ so that all motors are at (90) degrees.
```
// C++ code
#include <Servo.h>

Servo servo1; 
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;

void setup() {
  servo1.attach(3);
  servo2.attach(5); 
  servo3.attach(6); 
  servo4.attach(9);
   servo5.attach(10); 
}

void loop() {
 
    servo1.write(90);              
    servo2.write(90);     
    servo3.write(90);
    servo4.write(90);
    servo5.write(90); 
    delay(10);                      

}

```
 Simulation end result 
![Mighty Blorr-Allis (1)](https://user-images.githubusercontent.com/52053143/127381496-aed49684-ccc2-4d17-a841-b0cecba172b1.png)

<br>

***

## ❸ Control the motors by using potentiomete
&nbsp; &nbsp;&nbsp; Add &nbsp; <img width="92" alt="p" src="https://user-images.githubusercontent.com/52053143/127400425-418bcf01-1aa8-4513-862e-fd54669e8b8b.png"> &nbsp; to the previous circuit

Programming the circuit in C++
```
// C++ code
#include <Servo.h>

Servo servo1; 
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;

int value; // variable to read the value from the analog pin
int angle; //variable to store the mapped angle

void setup()
{
   servo1.attach(3);
  servo2.attach(5); 
  servo3.attach(6); 
  servo4.attach(9);
   servo5.attach(10);
}
void loop()
{
  value = analogRead(A0);
   angle = map(value, 0, 1023, 0, 90); // scale it to use it with the servo
     servo1.write(angle); 
  
  value = analogRead(A1);
   angle = map(value, 0, 1023, 0, 90); // scale it to use it with the servo
     servo2.write(angle); 
  
  value = analogRead(A2);
   angle = map(value, 0, 1023, 0, 90); // scale it to use it with the servo
     servo3.write(angle); 
  
  value = analogRead(A3);
  angle = map(value, 0, 1023, 0,90); // scale it to use it with the servo
  servo4.write(angle); 
  
  value = analogRead(A4);
  angle = map(value, 0, 1023, 0, 1023); // scale it to use it with the servo
  servo5.write(angle);
   
  delay(15); // waits for the servo to get there
}
```

<br>







https://user-images.githubusercontent.com/52053143/127402536-a4b88671-5678-44c1-b3a2-143ab2891c29.mp4








 

