# Kerala IOT Challenge

> Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program “Kerala IoT Challenge 2021”, with a vision to mould 100 IoT experts in Kerala, hosting on the µLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.
# About Me
> Hi everyone! I'm Ajayraj K.K.I'm currently pursuing BTech in Electronics and Communication Engineering from Eranad Knowledge City Technical Campus, Manjeri.
My major area of interests are IOT,Android App Development,Cyber Security and Programming.
## Experiment 1 : Hello World LED Blinking

> A basic program similar to printing "*Hello World*" in any programming language. The aim is to blink an LED using **Arduino Uno Board**.

>**Arduino Uno** is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

## Components Required  
* Arduino Uno Board 
* USB Cable 
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard 
* Jumper Wires (Male to Male ) X 2 Nos

## Circuit Diagram
![WhatsApp Image 2021-11-28 at 1 57 36 AM](https://user-images.githubusercontent.com/61041490/143734907-3348e28f-129c-42c6-8160-a50b93e9ca5f.jpeg)

![5h7X9_3102_1627394356](https://user-images.githubusercontent.com/91405741/137279765-8a82a34f-1dc0-4afc-9bd3-a31d7f62c428.png)

## Code

```

int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}

```

## Output

> The LED is blinked with a time interval of 1 second

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/61041490/142443959-d03a662d-dbff-44fa-8832-08e881966352.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 2 : Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.

## Components Required 

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3

## Circuit Diagram

![WhatsApp Image 2021-11-28 at 1 54 04 AM](https://user-images.githubusercontent.com/61041490/143734941-34a9e59b-96c9-4dc3-b7a3-ca1d67a2b1a4.jpeg)


![yiU1x_3102_1627566759](https://user-images.githubusercontent.com/91405741/137288387-e85f8db9-ae97-49d0-888d-a2fc15e4c496.png)

## Code

```

int redled =10; // initialize digital pin 10.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds
digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}

```

## Output

> In Traffic light the green LED blink about 5 second, then it is turnoff. Then the yellow LED blinks 3 times with a time interval of 0.5 second.Then the red LED blink about 5 seconds. This process continues.

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/61041490/142653873-cdd259a9-29e5-4908-9d50-0ab50528a62c.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 3 : LED Chasing Effect

> We often see billboards composed of colorful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate LED chasing effect. The long lead of LED is the positive side; short lead is negative.

## Components Required

* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

## Circuit Diagram
![WhatsApp Image 2021-11-28 at 2 15 13 AM](https://user-images.githubusercontent.com/61041490/143734882-4bebc7b8-e2e3-482f-9e36-ac30f8db5fa2.jpeg)


![s5yR0_3102_1627567167](https://user-images.githubusercontent.com/91405741/137292096-feb60c91-1a9a-474b-a596-300285f7b011.png)

## Code

```

int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(400);        // delay
   }  
}

```

## Output

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/61041490/142654980-b1a8c6e6-f196-4149-acf2-a5ddceae817f.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 4 : Button Controlled LED

> An experiment to light an LED using a Push Button.

## Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

## Circuit Diagrams


![WhatsApp Image 2021-11-27 at 8 05 22 AM](https://user-images.githubusercontent.com/61041490/143665616-c32bc20a-a3e2-4fa4-95cf-8804403acac8.jpeg)

![push2](https://user-images.githubusercontent.com/56971600/138454527-5b05c4fd-0954-41e8-af5a-490ca53a783c.jpg)

![wQGca_3102_1628160139](https://user-images.githubusercontent.com/91405741/137344321-3e662dee-cb00-421d-a34d-848c2ffd1a6f.png)

## Code

```

int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}

```
## Output

> When the push button is pressed the LED is turned on otherwise it is off.

<iframe width="560" height="315"
src=


https://user-images.githubusercontent.com/61041490/143664845-33cd31b9-5ee6-4264-8ba7-32a3ccbbd58d.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 5 : Buzzer

> An experiment to understand the working of a buzzer.

## Components Required

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

## Circuit Diagrams
![WhatsApp Image 2021-11-27 at 7 51 10 AM](https://user-images.githubusercontent.com/61041490/143665286-4acec9c1-c304-4eb3-9e7a-2d3b3e3a32fe.jpeg)


![BBr05_3102_1628160460](https://user-images.githubusercontent.com/91405741/137346830-1fa2408c-2a1d-4fdf-a049-5736aeb803ec.png)

![e9Pdc_3102_1628160446](https://user-images.githubusercontent.com/91405741/137346912-0f871dbf-8e86-4734-a337-fceeff454e33.png)

## Code

```

int buzzer=8;// initialize digital IO pin that controls the buzzer
void setup() 
{ 
  pinMode(buzzer,OUTPUT);// set pin mode as “output”
} 
void loop() 
{
digitalWrite(buzzer, HIGH); // produce sound
}

```

## Output

> The Buzzer makes beep sound.

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/61041490/142656619-e64fdbfc-da22-4fda-9734-449af80785b4.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

# Experiment 6 : RGB LED

> An experiment to understand the working of a RGB LED.

## Components Required

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

## Circuit Diagrams

![WhatsApp Image 2021-11-28 at 2 19 45 AM](https://user-images.githubusercontent.com/61041490/143734847-367d2ee0-bad9-42b5-8c29-403e316c3449.jpeg)

![xX9cw_3102_1628160649](https://user-images.githubusercontent.com/91405741/137347719-6966c0b1-021d-471c-b0a7-48d0441752d0.png)

![A8a40_3102_1628160631](https://user-images.githubusercontent.com/91405741/137347782-e0a8a008-8706-4b7c-ba31-38ef0ab6ca72.png)

![TefdI_3102_1628167200](https://user-images.githubusercontent.com/91405741/137347822-228ccf9c-3a89-45ba-bb24-c3b0ee587818.png)

## Code

```

int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}

```

## Output

> The RGB LED blinks.

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/61041490/142665247-9e94f44c-6f0d-449f-b075-b8ad1309f177.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 7 : LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.

### LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

## Circuit Diagrams

![WhatsApp Image 2021-11-28 at 1 59 30 PM](https://user-images.githubusercontent.com/61041490/143735314-eee735f3-2660-47ca-911f-c459e0131d2f.jpeg)

![L5Iw9_3102_1628755894](https://user-images.githubusercontent.com/91405741/138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5.png)

## Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

## Circuit Diagrams


![WhatsApp Image 2021-11-27 at 8 14 06 AM](https://user-images.githubusercontent.com/61041490/143735034-0547c2f9-a62c-45ac-b4a1-15c36bb9195a.jpeg)
![schema_Myt5vqqplZ](https://user-images.githubusercontent.com/91405741/138436635-60cb2ec4-091d-4f24-bf96-b0289e06fa00.png)

## Procedure

* Connect the 3.3v output of the Arduino to the positive rail of the breadboard
* Connect the ground to the negative rail of the breadboard
* Place the LDR on the breadboard
* Attach the 10K resistor to one of the legs of the LDR
* Connect the A0 pin of the Arduino to the same column where the LDR and resistor is connected (Since the LDR gives out an analog voltage, it is connected to the analog input pin on the Arduino. The Arduino, with its built-in ADC (Analog to Digital Converter), then converts the analog voltage from 0-5V into a digital value in the range of 0-1023). - Now connect the other end of the 10K resistor to the negative rail
* And the the second (free) leg of the LDR to the positive rail
Pretty much this is what we need for the light sensing. Basic circuits like this can be done without an Arduino aswell. However, if you want to log the values and use it to create charts, run other logics etc. I will recomend an Arduino or ESP8266 or may be a ESP32 for this.
Now, as we want our circuit to do something in the real world other than just displaying the values on the computer screen we will be attaching a LED to the circuit. The LED will turn on when its dark and will go off when its bright. To achieve this we will:
* Place the LED on the breadboard
* Connect the 220ohm resistor to the long leg (+ve) of the LED
* Then we will connect the other leg of the resistor to pin number 13 (digital pin) of the Arduino
* and the shorter leg of the LED to the negative rail of the breadboard

## Code

```

const int ledPin = 13;
const int ldrPin = A0;
void setup() {
Serial.begin(9600);
pinMode(ledPin, OUTPUT);
pinMode(ldrPin, INPUT);
}
void loop() {
int ldrStatus = analogRead(ldrPin);
if (ldrStatus <= 200) {
digitalWrite(ledPin, HIGH);
Serial.print("Its DARK, Turn on the LED : ");
Serial.println(ldrStatus);
} else {
digitalWrite(ledPin, LOW);
Serial.print("Its BRIGHT, Turn off the LED : ");
Serial.println(ldrStatus);
}
}

```

## Output

<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/61041490/142664590-a0ead512-3d24-4162-858b-0cc8d1fc7f99.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 8 : Flame Sensor

> We are using Infrared Receiver (IR)for detecting Flame 

## Components Required
* Arduino Uno Board*1
* Flame Sensor *1
* Buzzer *1
* LED *2
* Breadboard 
* Jumper Wire*6
* USB cable*1

## Circuit Diagram

![image](https://user-images.githubusercontent.com/56971600/141062255-a1d478aa-1392-4f93-9b1c-d18d5540345c.png)


## Code

```

const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;
int redled = 5;
int greenled = 6;
void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(redled, OUTPUT);
  pinMode(greenled, OUTPUT);

  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    digitalWrite(buzzerPin, HIGH);
    digitalWrite(redled, HIGH);
    digitalWrite(greenled, LOW);
  }
  else
  {
    digitalWrite(buzzerPin, LOW);
    digitalWrite(greenled, HIGH);
    digitalWrite(redled, LOW);
  }
}



```

## Output

> The buzzer produces a beep noise along with red LED lighting up when the IR Reciever is exposed to flames.

![WhatsApp Image 2021-11-28 at 2 06 14 PM](https://user-images.githubusercontent.com/61041490/143735487-86326210-e0ca-42cb-8e9e-04971595ec9a.jpeg)


<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/61041490/143664977-d099f71c-1a2f-4e0e-a9b6-5f4cbe99bcd6.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>

## Experiment 9 : LM35 Temperature Sensor

> LM35 is a common and easy-to-use temperature sensor.

![image](https://user-images.githubusercontent.com/56971600/138459624-95113dfa-f21f-4677-9c1f-c337a03476af.png)

![image](https://user-images.githubusercontent.com/56971600/138459742-1db27599-5b4e-4bcd-ae48-f809a8371ceb.png)

## Components Required 

> LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing.

> LM35 temperature sensor can produce different voltage by different temperature
When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.
The output temperature is 0℃～100℃, the conversion formula is as follows:

![image](https://user-images.githubusercontent.com/56971600/138460051-cbde66eb-988b-4f15-b350-fb4c29fafa99.png)

## Components Required

* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

## Circuit Diagram 

![image](https://user-images.githubusercontent.com/56971600/138460381-ef0df7aa-f13c-45d8-9131-4b1141053052.png)

![image](https://user-images.githubusercontent.com/56971600/138460454-2eda2604-3b8f-4522-bf98-01e5c31314df.png)

## Code

```

int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}

```

## Output

> Temperature values read by LM35 sensor can be seen in the Serial Moniter.

![image](https://user-images.githubusercontent.com/56971600/138462544-6cf66ae7-ee0f-46c5-9623-ee42a00e7b58.png)


<iframe width="560" height="315"
src=

https://user-images.githubusercontent.com/61041490/142663423-d815b3fc-62a9-4a30-b47b-cb95b3758568.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe>
# Experiment 10:IR Remote Control Using TSOP

> An experiment to understand the working of IR Remote Control using TSOP.

## Components Required

* Arduino Uno Board*1
* Infrared Remote Controller(You can use TV Remote or any other remote) *1
* Infrared Receiver *1
* LED *6
* 220ΩResistor *6
* Breadboard Wire 
* USB cable*1

## Circuit Diagrams

![WhatsApp Image 2021-11-28 at 2 09 46 PM](https://user-images.githubusercontent.com/61041490/143735576-0c520267-8ff9-4340-8b7f-feb5871c5675.jpeg)

## Code

```

#include <IRremote.h> 
int RECV_PIN = 3;              
int c=0;                      
IRrecv irrecv(RECV_PIN);
decode_results results;
void setup()
{
   pinMode(8, OUTPUT);
   pinMode(9, OUTPUT);
   pinMode(10, OUTPUT);
   pinMode(11, OUTPUT);
   pinMode(12, OUTPUT);

   Serial.begin(9600);
  irrecv.enableIRIn();                     
}
void loop() {
  if (irrecv.decode(&results)) {
    Serial.println(results.value);
    irrecv.resume();                        
  if(results.value==16773645)      //Up                            
  {
             digitalWrite(8,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(8,LOW);
  }
   if(results.value==16763445)  //Down                                     
  {
             digitalWrite(9,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(9,LOW);
  }
    if(results.value==16769565) //left                                       
  {
             digitalWrite(10,HIGH);
  }
  else if(results.value==4294967295) 
  {
             digitalWrite(10,LOW);
  }
    if(results.value==16771605) //right                                       
  {
             digitalWrite(11,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(11,LOW);
  }
    if(results.value==16714485) //ok                                       
  {
             digitalWrite(12,HIGH);
  }
  else if(results.value==4294967295)
  {
             digitalWrite(12,LOW);
  }
  }
}

```

## Output

<iframe width="560" height="315"
src=
     

https://user-images.githubusercontent.com/61041490/143720953-bf0870a9-a25b-41cb-b4eb-c71412fce093.mp4

   
frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 


# Experiment 11 :Potentiometer analog Value Reading

> An experiment to understand the working of Potentiometer.

## Components Required

* Arduino Uno Board*1
* 10K Potentiometer *1
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1

## Circuit Diagrams
![WhatsApp Image 2021-11-28 at 2 31 04 PM](https://user-images.githubusercontent.com/61041490/143743472-89d58988-2269-4eea-9e5b-a816a3a7331b.jpeg)


## Code

```

int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}

```

## Output

<iframe width="560" height="315"
src=
        
https://user-images.githubusercontent.com/61041490/143720528-3febf955-4266-4794-bd24-f44fe0650e5e.mp4

frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 


# Experiment 12 : 7 Segment Display
        
> An experiment to understand the working of 7 Segment Display.

## Components Required

* Arduino Uno Board*1
* digit LED Segment Display*1
* 220Ω Resistor*8
* Breadboard*1
* Breadboard Jumper Wires *several
* USB cable*1

## Circuit Diagrams


![WhatsApp Image 2021-11-28 at 2 14 37 PM](https://user-images.githubusercontent.com/61041490/143735853-87849c88-3c77-4bd0-96e0-6fb5be9e4471.jpeg)

```

int a=7;// set digital pin 7 for segment a
int b=6;// set digital pin 6 for segment b
int c=5;// set digital pin 5 for segment c
int d=10;// set digital pin 10 for segment d
int e=11;// set digital pin 11 for segment e
int f=8;// set digital pin 8 for segment f
int g=9;// set digital pin 9 for segment g
int dp=4;// set digital pin 4 for segment dp
void digital_0(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,LOW);
digitalWrite(dp,LOW);
}
void digital_1(void) // display number 1
{
unsigned char j;
digitalWrite(c,HIGH);// set level as “high” for pin 5, turn on segment c
digitalWrite(b,HIGH);// turn on segment b
for(j=7;j<=11;j++)// turn off other segments
digitalWrite(j,LOW);
digitalWrite(dp,LOW);// turn off segment dp
}
void digital_2(void) // display number 2
{
unsigned char j;
digitalWrite(b,HIGH);
digitalWrite(a,HIGH);
for(j=9;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
digitalWrite(c,LOW);
digitalWrite(f,LOW);
}
void digital_3(void) // display number 3
{digitalWrite(g,HIGH);
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(dp,LOW);
digitalWrite(f,LOW);
digitalWrite(e,LOW);
}
void digital_4(void) // display number 4
{digitalWrite(c,HIGH);
digitalWrite(b,HIGH);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
digitalWrite(a,LOW);
digitalWrite(e,LOW);
digitalWrite(d,LOW);
}
void digital_5(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b, LOW);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void digital_6(void) // display number 6
{
unsigned char j;
for(j=7;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(c,HIGH);
digitalWrite(dp,LOW);
digitalWrite(b,LOW);
}
void digital_7(void) // display number 7
{
unsigned char j;
for(j=5;j<=7;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
for(j=8;j<=11;j++)
digitalWrite(j,LOW);
}
void digital_8(void) // display number 8
{
unsigned char j;
for(j=5;j<=11;j++)
digitalWrite(j,HIGH);
digitalWrite(dp,LOW);
}
void digital_9(void) // display number 5
{
unsigned char j;
digitalWrite(a,HIGH);
digitalWrite(b,HIGH);
digitalWrite(c,HIGH);
digitalWrite(d,HIGH);
digitalWrite(e, LOW);
digitalWrite(f,HIGH);
digitalWrite(g,HIGH);
digitalWrite(dp,LOW);
}
void setup()
{
int i;// set variable
for(i=4;i<=11;i++)
pinMode(i,OUTPUT);// set pin 4-11as “output”
}
void loop()
{
while(1)
{
digital_0();// display number 0
delay(1000);// wait for 1s
digital_1();// display number 1
delay(1000);// wait for 1s
digital_2();// display number 2
delay(1000); // wait for 1s
digital_3();// display number 3
delay(1000); // wait for 1s
digital_4();// display number 4
delay(1000); // wait for 1s
digital_5();// display number 5
delay(1000); // wait for 1s
digital_6();// display number 6
delay(1000); // wait for 1s
digital_7();// display number 7
delay(1000); // wait for 1s
digital_8();// display number 8
delay(1000); // wait for 1s
digital_9();// display number 9
delay(1000); // wait for 1s
}
}

```

## Output

<iframe width="560" height="315"
src=
        

https://user-images.githubusercontent.com/61041490/143720581-61cc7aa6-836f-45cf-b7bb-2b0ff0e21908.mp4


frameborder="0" 
allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
allowfullscreen></iframe> 


