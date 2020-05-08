# SihanXia__CCA_Mechatronics_2020
# Week 1-2
Linkage:
The first one failed because the pulley would get stuck with too much friction during rotation
![week1](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Pulley/IMG_3060.JPG)
![week1](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Pulley/IMG_3061.JPG)
![week1](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Pulley/IMG_3060.JPG)
![week1](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Pulley/IMG_3063.JPG)
![week1](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Pulley/IMG_3064.gif)
And then I did the second one, and I fixed the shaft of the pulley in the middle, and I increased the friction of the rope, and I made it work.
![week1](/Pulley/IMG_0660.JPG)
![week1](Pulley/IMG_0661.JPG)
![week1](Pulley/IMG_0674.JPG)
![week1](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Pulley/IMG_0676%20%5B640i%5D.gif)
![week1](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Pulley/IMG_0677%20%5B640i%5D.gif)
# Week 3-4

Class exercise:

![week3-4](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/LED/IMG_0865%20%5B640i%5D.gif)
![week3-4](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/LED/IMG_0866%20%5B640i%5D.gif)
![week3-4](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/LED/IMG_0867%20%5B640i%5D.gif)
![week3-4](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/LED/IMG_1207(1).gif)
![week3-4](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/LED/IMG_1215(1).gif)
![week3-4](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/LED/sd1582254138_2%20%5B640i%5D.gif)

Homework:

![week3-4](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/LED/20200506210718_HD~1.gif)

Code:
//initializing a variable for digital pin 2 to 10
int led1 = 2;
int led2 = 3;
int led3 = 4;
int led4 = 5;
int led5 = 6;
int led6 = 7;
int led7 = 8;
int led8 = 9;
int led9 = 10;
int led10 = 11;

void setup() {
  // put your setup code here, to run once:
 //initialize digital pin as output
 pinMode(led1, OUTPUT);
 pinMode(led2, OUTPUT);
 pinMode(led3, OUTPUT);
 pinMode(led4, OUTPUT);
 pinMode(led5, OUTPUT);
 pinMode(led6, OUTPUT);
 pinMode(led7, OUTPUT);
 pinMode(led8, OUTPUT);
 pinMode(led9, OUTPUT);
 pinMode(led10, OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
 digitalWrite(led1, HIGH);//it mean to give 5v(high) to pins.here ,the led will be on.
 delay(1000);//1000 = 1 second
 digitalWrite(led2, HIGH);
 delay(1000);
 digitalWrite(led3, HIGH);
 delay(1000);
  digitalWrite(led4, HIGH);
 delay(1000);
  digitalWrite(led5, HIGH);
 delay(1000);
  digitalWrite(led6, HIGH);
 delay(1000);
  digitalWrite(led7, HIGH);
 delay(1000);
  digitalWrite(led8, HIGH);
 delay(1000);
  digitalWrite(led9, HIGH);
 delay(1000);
  digitalWrite(led10, HIGH);
 delay(1000);

 digitalWrite(led1, LOW);//it mean to give 0v(low) to pin.here, led will be off
 delay(1000);
 digitalWrite(led2, LOW);
 delay(1000);
 digitalWrite(led3, LOW);
 delay(1000);
 digitalWrite(led4, LOW);
 delay(1000);
 digitalWrite(led5, LOW);
 delay(1000);
 digitalWrite(led6, LOW);
 delay(1000);
 digitalWrite(led7, LOW);
 delay(1000);
 digitalWrite(led8, LOW);
 delay(1000);
 digitalWrite(led9, LOW);
 delay(1000);
 digitalWrite(led10, LOW);
 delay(1000);
}


![week3-4](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/LED/20200507223322_HD.gif)

Code:

const int trig = 12;
const int echo = 13;

const int LED1 = 8;
const int LED2 = 7;
const int LED3 = 6;
const int LED4 = 5;
const int LED5 = 4;
const int LED6 = 3;
const int LED7 = 2;

int duration = 0;
int distance = 0;

void setup() 
{
  pinMode(trig , OUTPUT);
  pinMode(echo , INPUT);
  
  pinMode(LED1 , OUTPUT);
  pinMode(LED2 , OUTPUT);
  pinMode(LED3 , OUTPUT);
  pinMode(LED4 , OUTPUT);
  pinMode(LED5 , OUTPUT);
  pinMode(LED6 , OUTPUT);
  pinMode(LED7 , OUTPUT);
  
  Serial.begin(9600);

}

void loop()
{
  digitalWrite(trig , HIGH);
  delayMicroseconds(1000);
  digitalWrite(trig , LOW);


  duration = pulseIn(echo , HIGH);
  distance = (duration/2) / 28.5 ;
  Serial.println(distance);
  

  if ( distance <= 7 )
  {
    digitalWrite(LED1, HIGH);
  }
  else
  {
    digitalWrite(LED1, LOW);
  }
  if ( distance <= 14 )
  {
    digitalWrite(LED2, HIGH);
  }
  else
  {
    digitalWrite(LED2, LOW);
  }
  if ( distance <= 21 )
  {
    digitalWrite(LED3, HIGH);
  }
  else
  {
    digitalWrite(LED3, LOW);
  }
  if ( distance <= 28 )
  {
    digitalWrite(LED4, HIGH);
  }
  else
  {
    digitalWrite(LED4, LOW);
  }
  if ( distance <= 35 )
  {
    digitalWrite(LED5, HIGH);
  }
  else
  {
    digitalWrite(LED5, LOW);
  }
  if ( distance <= 42 )
  {
    digitalWrite(LED6, HIGH);
  }
  else
  {
    digitalWrite(LED6, LOW);
  }
  if ( distance <= 49 )
  {
    digitalWrite(LED7, HIGH);
  }
  else
  {
    digitalWrite(LED7, LOW);
  }
}
# Week 5-6
![week5-6](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Motor/IMG_1227.gif)
![week5-6](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Motor/IMG_1228.gif)

# Mid-term
The proposal: Use a DC motor to control a linkage.

The linkage:Made by wood;Cardboard and foam.

![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/IMG_3056.JPG)
![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/IMG_3057.JPG)
![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/IMG_3058.JPG)
![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/IMG_3059.JPG)
Arduino control dc motor:

![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/IMG_2412(1).JPG)
![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/IMG_2414.JPG)
Code:
![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/IMG_2407(20200430-210539).JPG)
![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/IMG_2408(20200430-210537).JPG)
![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/Midterm%20project.gif)
![Mid-term](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Midterm/Mid-term%202.gif)

Mid-term video: https://youtu.be/ZndI5C-QjuU

# Final
Click to see the final proposal:
![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final1/final%20project%20proposal.doc)
The first thing I plan to do is use; The capacitive sensor controls the servo motor, but it failed because I didn't have enough resistance (10M); I'm trying to control it with a resistance of 1M; However, due to the insufficient resistance, the motor was not successfully controlled, and only the LED was successfully controlled. (the failed test can be seen in the video in my folder "final 2" :20200430214550_HD.MP4,20200430211350_HD.MP4.  

Then I dicided to do "Tone" first I made a capacitivesensor piano. (Use the coductive paint showed in my final proposal); And I also did a simple melody controled by button.

The conductive paint piano.(The first one for testing. The second one is the final one)

![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final1/IMG_2905.JPG)
![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final1/IMG_3036.JPG)
![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final1/IMG_3035.JPG)
![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final2/20200430213849_HD.gif)
![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final2/IMG_3026.gif)
![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final2/20200430214202_HD.gif)

Final video1(CapacitiveSensor piano):https://youtu.be/Lfuaku4985Y
Final video1 code:
![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final1/Final%20code.txt)

Final video2(Melody):https://youtu.be/XTN3QwFY7os
Final video2 code:
![Final](https://github.com/sihanxia/SihanXia__CCA_Mechatronics_2020/blob/master/Final1/%E6%96%87%E6%9C%AC(2020-05-01%20135809).txt)
