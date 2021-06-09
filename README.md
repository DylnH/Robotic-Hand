# Robotic-Arm

### Overview

- This projects goal was to make a Robotic arm. The fun part was that there weren't any real specifications, so anything could happen. What we decided was to make a flex sensor controlled arm, that would mimic the fingers of an individual. In Theory, this arm could be used as a multi-purposed arm. It could pick up certain toxic objects that may be considered dangerous for humans to touch or come in contact with, being attached to a rover, used to test chemical reactions from a distance, additional virtual assistants, or even petting porcupines. The user could wear a glove with the flex sencors attached, and the hand does exactally what the controller does. It's a fairly Simple idea, but carrying it out is a whole other story.

_________________________________________________________________________________________________________________________________________________________________________

### Tools

 [- Arduino (Code)](https://www.arduino.cc/en/software)
 
 [- Onshape (CAD)](https://www.onshape.com/en/)
 
 [ - Tinkercad (Wiring Diagram)](https://www.tinkercad.com/)
 
 [ - Github (Documentation)](https://github.com/)
 
 ________________________________________________________________________________________________________________________________________________________________________
 
 #### Wiring Diagram and Commented Code

<img src="Screenshot%20(3).png?raw=true" width="400">

[Code (there are only two because 3 out of 5 are broken. however the code still works with five)](https://drive.google.com/file/d/16vUKTdU-LGm613mKrdmvg-yJmQ_zKxg0/view?usp=sharing)

<details><summary>Code</summary>
 
``` arduino
#include <Servo.h>

Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;

int flex1 = A0;
int flex2 = A1;
int flex3 = A2;
int flex4 = A3;
int flex5 = A4;

void setup()
{
  Serial.begin(9600);
  
  servo1.attach(8);
  servo2.attach(9);
  servo3.attach(10);
  servo4.attach(11);
  servo5.attach(12);
}

void loop()
{
  int flexValue1;
  int flexValue2;
  int flexValue3;
  int flexValue4;
  int flexValue5;
  int servoPosition1;
  int servoPosition2;
  int servoPosition3;
  int servoPosition4;
  int servoPosition5;

  flexValue1 = analogRead(flex1);
  flexValue2 = analogRead(flex2);
  flexValue3 = analogRead(flex3);
  flexValue4 = analogRead(flex4);
  flexValue5 = analogRead(flex5);

  servoPosition1 = map(flexValue1, 600, 800, 0, 180);
  servoPosition1 = constrain(servoPosition1, 0, 180);
  servoPosition2 = map(flexValue2, 600, 800, 0, 180);
  servoPosition2 = constrain(servoPosition2, 0, 180);
  servoPosition3 = map(flexValue3, 600, 800, 0, 180);
  servoPosition3 = constrain(servoPosition3, 0, 180);
  servoPosition4 = map(flexValue4, 600, 800, 0, 180);
  servoPosition4 = constrain(servoPosition4, 0, 180);
  servoPosition5 = map(flexValue5, 600, 800, 0, 180);
  servoPosition5 = constrain(servoPosition5, 0, 180);

  servo1.write(servoPosition1);
  servo2.write(servoPosition2);
  servo3.write(servoPosition3);
  servo4.write(servoPosition4);
  servo5.write(servoPosition5);

  delay(100);
  }
```

</details>
 
_________________________________________________________________________________________________________________________________________________________________________

### Plans and designs

#### [- Planning Document and Pseudocode](https://docs.google.com/document/d/1A5yr3gwvPFNczzGg2IPSaRJFIutgpFQ-Hbp36jQhLAk/edit?usp=sharing)

- We had many iterations of what the project could look like, however, in the end, you can see that the designs we came up with ended up looking nothing like the end result. At First, we thought it would be good to attach the arm to some sort of stand or wall. However, we soon realized that this would take extra time away from the actual design, so we stayed away from it. We even had a prototype design for these specifications, and it would’ve moved along the wall like [Mark Rober’s moving dart board,](https://www.youtube.com/watch?v=MHTizZ_XcUM) but we scratch that idea as well. This design could be done in the future, but we decided to keep it simple. Our final design uses a premade hand, controlled by servos pulling on each finger, with elastic pulling back to keep its shape.

#### Stand and Wall designs
<img src="Idea%231's.jpg?raw=true" width="200"><img src="Idea%232's.jpg?raw=true" width="200"><img src="Idea%233's.jpg?raw=true" width="200">

#### [- CAD Prototype Specified for wall ](https://cvilleschools.onshape.com/documents/bb650a5758ea41f57e61b52f/w/1ee44fa1089f16d3b393ba3a/e/24473f01d90508c6ebd4ea05)

<img src="Screenshot%202021-06-09%202.15.11%20PM.png?raw=true" width="400"> [(Wall design moving)](https://drive.google.com/file/d/1KeHIvSfq9kleZb0yazV1TSGmkmo0Zmrf/view?usp=sharing)

#### [- Final Design](https://cvilleschools.onshape.com/documents/e2edc0296736b251a4e3fe74/w/817a81a4a4728dc8bb2cad43/e/76581a513e1b4ba1cefbcda2)

<img src="Screenshot%202021-05-03%2011.10.20%20AM.png?raw=true" width="400"> [hand working](https://drive.google.com/file/d/125KFlFFFpU-OIzBG-1Z3dFMdSSbtWHqi/view?usp=sharing)


### Collaborators

- [Henry C.](https://github.com/hcoyle91)
- [Dylan H.](https://github.com/OstrichIsYum)

________________________________________________________________________________________________________________________________________________________________________

## Project Update #1

1. What major obstacle is keeping you from making better progress on your project?

### Issues related to Code

- The one major issue that is giving me problems with making good progress on our project is the continous issues I keep having with the USB cable. Its such a small issue, yet if I leave this problem unresolved, I will not be able to code. I don't know what causes this to happen, but the only solution that has worked in the past was to replacing the cable entirely. But since this problem has happened before and the USB cables cost money, going through multiple of them at a time is not ideal. 

- Due to the previous problem, I am not able to submit any of the code I have so far, but I will do so when the problem is fixed. Despite this, Note that I was makeing good progess with using flex sensors to rotate servo.

### Issues related to CAD
- [Servo wrist extension](https://cvilleschools.onshape.com/documents/e2edc0296736b251a4e3fe74/w/817a81a4a4728dc8bb2cad43/e/ad8df5c5b138ea41852755f6)


## Project Update #2

1. Code as of right now, is complete. However, It might have to be changed to meet the needs of the CAD half of the project.
2. CAD as of right now, is complete*. However, It might have to be changed to meet the needs of the Code half of the project.(dylan's notes. I acutally don't know if cad is complete. It looks like it is based on what I've seen on Onshape).


## Project Update #3

1. We are officially almost done with the robotic arm... fabrication is complete, coding is complete, however we only need two more flex sensors and the project will be complete.

