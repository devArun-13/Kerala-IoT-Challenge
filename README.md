# Kerala-IoT-Challenge
> [**Foxlab Makerspace**](https://www.facebook.com/foxlabmakerspace/) in association with [**GTech - Group of Technology Companies**](https://atfg.gtechindia.org/) in Kerala is launching our prestigious program **“Kerala IoT Challenge 2022”**, hosting on the µLearn platform. **Kerala IoT Challenge** is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

> This page is maintained so as to keep the track of my experiments at different levels of the **Kerala IoT Challenge**.

# About Me
Hi,everyone I am Arun Mathew ,Currently pursuing B-tech from RIT Kotayam,My field of intrests are
* Robotics
* 3D printing
* Automation
* Mechanical design

# Experiment-1 HELLO WORLD LED BLINKING
Iintoduction to Arduino IDE and Its programming is intended here

## Components Required
* Arduino Uno R3 *1
* Bread Board *1
* Jumper Wires(Male to male ) *2
* LED *1
* 220 Ohm resistor *1
* Usb A to B cable *1
 
## Circuit Diagram
 ![](https://user-images.githubusercontent.com/95708160/147387609-b5e0f3f3-b38d-4238-9df4-a200e6406678.jpeg)
 
##  Code
 ```
 
 int ledPin=5;  //defining ledpin as pin 5
void setup() {
   pinMode(5,OUTPUT); //define pin5 as output type: 
}

void loop() {
  digitalWrite(ledPin,HIGH);//setting pin to on position
  delay(1000); //delay of 1 second
  digitalWrite(ledPin,LOW);//set led to off position
  delay(1000); //wait for a second
  
  

}
 ```
## Output
The LED blinks with a delay of one second 
## Output Giff
 ![](https://user-images.githubusercontent.com/95708160/147388479-4a22307c-f547-4966-bcf2-cfc4f9be810f.gif)
 
 
 
# Experiment-2 Traffic Light

## Components Required

* Arduino board *1
* USB type A to B cable *1
* Red Led*1
* Yellow  LED*1
* Green LED*1
* 220ohm resistor *3
* Breadboard*1
* Breadboard jumper wires* several

## Circuit Diagram
![](https://user-images.githubusercontent.com/95708160/147388021-c1dcd075-6980-4278-acdc-6e65f96adda9.jpeg)

## Code

```
int Green=5;//defining ledpin as pin 5
int Yellow=8;//defining ledpin as pin 8
int Red=6;//defining ledpin as pin 6
void setup() {
   pinMode(5,OUTPUT); //define pin5 as output type: 
   pinMode(8,OUTPUT); //define pin8 as output type:
   pinMode(6,OUTPUT); //define pin6 as output type:
}

void loop() 
{
  digitalWrite(Green,HIGH);//setting Green to On position
  delay(5000); //delay of 5 second
  digitalWrite(Green,LOW);//set led to off position
  delay(1000); //wait for a second
  for(int i=1;i<=3;i++)
     {
      digitalWrite(Yellow,HIGH);//setting Yellow to On position
      delay(500); //delay of 0.5 second
      digitalWrite(Yellow,LOW);//set led to off position
      delay(500); //wait for 0.5 second
     }    // Blinks Yellow 3 times
      digitalWrite(Red,HIGH);//setting RED to On position
      delay(500); //delay of 5 second
      digitalWrite(Red,LOW);//set led to off position
      delay(500); //wait for 0.5 second
     
}
```
## Output
The green Led lights for five seconds followed by yellow LED blinking three times with a delay of 0.5seconds followed by the red LED ON for 5 seconds 
## Output video
![](https://user-images.githubusercontent.com/95708160/147835010-9d50fff5-8f44-44a2-96e3-e504d8294237.gif)
## Observed Limitation  
When all the six Leds turn on at a time the brightness of LEDs reduce owing to the higher power demand than the output.


# Experiment-3 LED Chasing Effect
 In this experiment, we compile a program to simulate LED chasing effect.
 
## Components Required
* Arduino Uno *1nos
* Bread Board *1nos
* Usb Type A to Type B *1nos
* Jumper Cable *13nos
* Led *6nos
* 220ohm resistor*6nos

## Circuit Diagram

![](https://user-images.githubusercontent.com/95708160/147388050-c91db1bd-febc-4b23-bbd1-5cbe55789a78.jpeg)

## Code
```
int BASE = 2;  // the I/O pin for the first LED
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
     digitalWrite(i, LOW);    //  turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // turning on LED s one by one
     delay(200);        // delay
   }  
}
```
##  OUTPUT

The Leds will all lights up with a delay of 0.2 seconds and then turns of one by one with a delay of 0.2 second
## Output video

 ![](https://user-images.githubusercontent.com/95708160/147388536-50e1d46d-23a3-4101-9b8d-a555aab5759c.gif)
 
 
#  Experiment 4 BUTTON CONTROLLED LED
 
Taking feedback from a button to control any output pin,also to study setting of pins as input.
 
##  Components Required 
 * Arduino Uno*1
 * Usbtype A to type B cable*1
 * Button switch*1
 * Red M5 LED*1
 * 220ΩResistor*1
 * 10KΩ Resistor*1
 * Breadboard*1
 * Breadboard Jumper Wire*6
 
##  Circuit Diagram
 
![](https://user-images.githubusercontent.com/95708160/147835043-41ab71e6-49de-4430-9aa3-c20a88e0f40e.jpeg)
 
##  Code
 ```
 int ledpin=11;
int button=7;
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as output type
pinMode(button,INPUT);// set button as input pin
}
void loop()
{
val=digitalRead(button);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
  {
  digitalWrite(ledpin,LOW);
  }
else
  { 
  digitalWrite(ledpin,HIGH);}
  }
  ```
##  OUTPUT 
  
The led blinks as the button is pressed.
## output vedio
![](https://user-images.githubusercontent.com/95708160/147835211-cbac1881-55e0-43f8-83cb-5df7f88f2ae7.gif)
  
# EXPERIMENT 5 Buzzer
 
## AIM
 
 To control a buzzer and manipulate delay to make tunes
 
## COMPONENTS REQUIRED
 
 * Arduino Uno
 * Buzzer*1
 * Breadboard*1
 * Breadboard Jumper Wire*2
 * USB type A to type b*1
  
## CIRCUIT DIAGRAM
 
![](https://user-images.githubusercontent.com/95708160/147835057-cecfa081-db21-4fb0-a296-7445a9cc94f5.jpeg)
 
## CODE
 ```
int buzzer=8;
void setup() 
{ 
  pinMode(buzzer,OUTPUT);
} 
void loop() 
{
digitalWrite(buzzer, HIGH);// produce tune
delay(100);
digitalWrite(buzzer, LOW);
delay(100);

}
```

## OUTPUT

The buzzer buzzes with a delay of 100ms
## OUTPUT VEDIO
![](https://user-images.githubusercontent.com/95708160/147835183-a98a47b6-c13e-42b0-b464-de36c3074a94.gif)

# EXPERIMENT 6 RGB LED

## AIM

To control the RGB LED to give diffrent pattern output

## Note

An RGB LED bulb uses three diodes in Red, Green and Blue. These are mixed in different intensities to produce a variety of different colours. The process is based on additive color mixing, the same technique which is used in TV sets, computer monitors and flat screens.

analogWrite() takes two or three arguments:
pin: the number of the pin whose value you wish to set
value: the duty cycle: between 0 (always off) and 255 (always on). Since 0.6.0: between 0 and 255 (default 8-bit resolution) or 2^(analogWriteResolution(pin)) - 1 in general.
frequency: the PWM frequency (optional). If not specified, the default is 500 Hz.


## Components required
* Arduino Uno *1
* USB Cable type A to type B * 1
* RGB LED * 1
* Resistor 220ohm *1
* jumper wire*5
## Code
```
int redpin = 11; // red LED
int bluepin =10; //  blue LED
int greenpin =9;//  green LED
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
## Circuit Diagram
![](https://user-images.githubusercontent.com/95708160/147835078-a7bffb41-32f2-4910-8369-1106b5a2ac6b.jpeg)

## OUTPUT
The  RGB LED glows with aspecific pattern and brightness level
## OUTPUT VIDEO
![](https://user-images.githubusercontent.com/95708160/147835168-fe700260-dfc5-407d-a829-485e1f8a3c28.gif)

# EXPERIMENT 7-LDR Light Sensor

## LDR sensor
LDR ( light dependent resistor ) also called photoresistors are responsive to light. Photoresistors are used to indicate the intensity or the presence or the absence of light. When there is darkness the resistance of photoresistor increases and when there is sufficient light it dramatically decreases.
## COMPONENTS REQUIRED
 * Arduino Uno 
 * Photo Resistor
 * Red M5 LED*
 * 10KΩ Resistor
 * 220Ω Resistor
 * Breadboard
 * Breadboard Jumper Wire
 * USB cable
## CIRCUIT DIAGRAM
![](https://user-images.githubusercontent.com/95708160/151667212-71587939-2c72-4206-8c25-1c2cc3934596.jpeg)
## CODE
```
int in=0;
int ledpin=11; 
int val=0;
void setup()
{
pinMode(ledpin,OUTPUT);
Serial.begin(9600);
}
void loop()
{
val=analogRead(in);
Serial.println(val);
analogWrite(ledpin,val/4);
delay(10);
}
```
## NOTE
 * Ldr resistance will decrease as the incident light increases
 * The analogread() varies from 0 to 1023 
 * analogWrite() varies from 0 to 255 (1/4 th)
## OUTPUT
When the light falling on the Ldr the analog value is read and is fed to the led as duty cycle of range 255.and the Led attains brightness at the same rate the light in the room decreases.
## OUTPUT VIDEO
![](https://user-images.githubusercontent.com/95708160/151668761-be8c85e8-96e1-44e5-9d22-ca6f18b436b7.gif)

# EXP-8 Flame Sensor

## WORKING
When fire burns it emits a small amount of Infra-red light, this light will be received by the Photodiode (IR receiver) on the sensor module. Then we use an Op-Amp to check for a change in voltage across the IR Receiver, so that if a fire is detected the output pin (DO) will give 0V(LOW), and if the is no fire the output pin will be 5V(HIGH).
## COMPONENTS REQUIRED
  * Arduino Uno (any Arduino board can be used)
  * Flame sensor module
  * LED
  * Buzzer
  * Resistor
  * Jumper wires
    
## CODE
```
int buzzer = 13;
int LED = 12;
int flame_sensor = 4;
int flame_detected;

void setup()
{
  Serial.begin(9600);
  pinMode(buzzer, OUTPUT);
  pinMode(LED, OUTPUT);
  pinMode(flame_sensor, INPUT);
}

void loop()
{
  flame_detected = digitalRead(flame_sensor);
  if (flame_detected == 0)
  {
    Serial.println("Flame detected! take action immediately.");
    digitalWrite(buzzer, HIGH);
    digitalWrite(LED, HIGH);
    delay(200);
    digitalWrite(LED, LOW);
    delay(200);
  }
  else
  {
    Serial.println("No flame detected");
    digitalWrite(buzzer, LOW);
    digitalWrite(LED, LOW);
  }
  delay(1000);
}

```

## CIRCUIT DIAGRAM
![](https://user-images.githubusercontent.com/95708160/151667195-fdea2c1f-6b61-494c-b028-da896b285607.jpeg)

## PRECAUTION
* While using IR flame sensor module always keep in mind that logic'1' is for no flame and logic'0' is for flame detected 
  
## OUTPUT VIDEO
![](https://user-images.githubusercontent.com/95708160/151666688-86e20433-37cd-4385-8a9e-94dc86b59f8d.gif)

## OUTPUT
The flame sensor detects the presence of fire or flame based on the Infrared (IR) wavelength emitted by the flame and triggers the alarm in case of fire deteced

# EXP-9  LM35 Temperature Sensor

## LM35 SENSOR
LM35 is an analog, linear temperature sensor whose output voltage varies linearly with change in temperature.It can measure temperature from-55 degree celsius to +150 degree celsius. The voltage output of the LM35 increases 10mV per degree Celsius rise in temperature. LM35 can be operated from a 5V supply.
## COMPONENTS REQUIRED
 * Arduino Uno 
 * LM35
 * Breadboard
 * Breadboard Jumper Wire
 * USB cable
## CIRCUIT DIAGRAM
![](https://user-images.githubusercontent.com/95708160/151667222-15649f1e-0864-4191-a1de-3364b758b92c.jpeg)
## CODE

```
int potPin = 0; 
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);
dat=(125*val)>>8;
Serial.print("Temp");
Serial.print(dat);
Serial.println("C");
delay(500);
}

```
## NOTE
 LM35 is an analog temperature sensor. This means the output of LM35 is an analog signal. Microcontrollers dont accept analog signals as their input directly. We need to convert this analog output signal to digital before we can feed it to a microcontroller’s input. For this purpose, we can use an ADC( Analog to Digital Converter).Arduino uno has an in built 10 bit ADC (6 channel). We can make use of this in built ADC of arduino to convert the analog output of LM35 to digital output.
 
## OUTPUT
The temperature is displayed on serial monitor

# EXP-10 IR Remote Control Using TSOP

## IR 
The signal from the infrared remote controller is a series of binary pulse code. To avoid the other infrared signal interference during the wireless transmission, the signal is pre-modulated at a specific carrier frequency and then send out by an infrared emission diode. The infrared receiving device needs to filter out other waves and receive signals at that specific frequency and to modulate it back to binary pulse code, known as demodulation.

## WORKING
IR remote controls, as the name would imply, make use of pulses of infrared light to send signals to a receiving device such as a television or sound system. Each button on the remote control sends out a unique pattern of pulses which are decoded by the receiver so that the appropriate action 

## COMPONENTS REQUIRED
* Arduino Uno Board
* Infrared Remote Controller
* Infrared Receiver 
* LED
* 220ΩResistor
* Breadboard Wire
* USB cable
## CIRCUIT DIAGRAM
[Magnificent Elzing](https://user-images.githubusercontent.com/66871603/167665286-83c352a4-be3d-4e7a-8c45-72ddde70f21b.png)

## CODE

```
#define IR_PIN A0 //ir recieve connect
#include<IRremote.h>
unsigned long receveData[]={0x80BF49B6,0x80BFC936,0x80BF33CC,0x80BF718E,0x80BFF10E,0x80BF13EC};
bool statusData[]{0,0,0,0,0,0};
int led[]={7,6,5,4,3,2};
IRrecv irrecv(IR_PIN);
decode_results  result;
void setup(){ 
  Serial.begin(9600);
  irrecv.enableIRIn();
  for(int i=0;i<6;i++)
    pinMode(led[i],OUTPUT);
} 
void loop(){
  if(irrecv.decode(&result)){
    Serial.println(result.value,HEX);
    for(int i=0;i<6;i++){
      if(result.value==receveData[i]){
        statusData[i]=!statusData[i];
        digitalWrite(led[i],statusData[i]);
      }
    }
    irrecv.resume();
  }
}

```
## OUTPUT
The leds are toggled as the two buttons(power and 1)of the IR remote is pressed 
## OUTPUT VIDEO
[ezgif-3-29cd788d62](https://user-images.githubusercontent.com/66871603/167666228-e2c4ad6b-7d14-4ff8-a981-35371ab55ef2.gif)


# EXP-11 POTENTIOMETER ANALOG VALUE READING

## Potentiometer working principle 
the potentiometer will act as a variable resistor. When you turn the knob, the resistor will increase or decrease, which will also increase or decrease the voltage on the analog pin to which the potentiometer is connected.Arduino Uno has a max voltage of 5V. The voltage on pin A0 will vary from 0V to 5V when you turn the knob.
## Components required 
* Arduino Uno 

*10K Potentiometer

*Breadboard

*Breadboard Jumper Wire

*USB cable
## Circuit diagram
![Frantic Tumelo-Blad](https://user-images.githubusercontent.com/66871603/167667574-97dd7974-77c5-4bb7-8f36-60cedbeac6b6.png)

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


## OUTPUT
![](https://user-images.githubusercontent.com/95708160/151671652-3e4f1ee0-4aa3-4108-a8bf-9b4cd1ebf58c.png)
## OUTPUT VEDIO
![](https://user-images.githubusercontent.com/95708160/151666711-63f6a052-013c-4257-be37-12efb034a8bd.gif)

# EXP-12 7 SEGMENT DISPLAY

There are two types of seven-segment displays: common anode and common cathode. The Internal structure of each of these types is nearly the identical. However, the polarity of the LEDs and common terminal are different. In most standard cathode seven-segment displays (the one we used in the experiments), all seven LEDs, in addition to a dot LED, have the cathodes connected to pins 8 and pin 3. To use this display, we must connect GROUND to pin 3 and pin 8, then connect +5V to the other pins and make each of the individual segments light up
## Components required
* Arduino Uno Board
* 1-digit LED Segment Display
* 220Ω Resistor
* Breadboard
* Breadboard Jumper Wires
* USB cable
## Working
![](https://user-images.githubusercontent.com/95708160/151671959-ccb0767f-dd9d-40ab-b24f-9c0df678d45c.gif)
## Circuit diagram
![](https://user-images.githubusercontent.com/95708160/151667411-61ffe689-8c8e-456f-ad90-0bf2f3145e9c.jpeg)

## Code

```

 int a=7;
int b=6;
int c=5
int d=10;
int e=11;
int f=8;
int g=9;
int dp=4
void digital_0(void) 
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
digitalWrite(c,HIGH);
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
digital_0();
delay(1000);
digital_1();
delay(1000);
digital_2();
delay(1000); 
digital_3();
delay(1000);
digital_4();
delay(1000); 
digital_5();
delay(1000); 
digital_6();
delay(1000); 
digital_7();
delay(1000); 
digital_8();
delay(1000); 
digital_9()
delay(500); 
}}

```
## OUTPUT
![](https://user-images.githubusercontent.com/95708160/152190589-b23a24fe-9a7a-4275-ac79-c2042036624a.png)

# ASSIGNMENT 1-Night lamp with LDR and LED

## Working
when the lights fade out the LED should automatically fix the light 

## COMPONENTS REQUIRED
 * Arduino Uno 
 * Photo Resistor
 * Red M5 LED*
 * 10KΩ Resistor
 * 220Ω Resistor
 * Breadboard
 * Breadboard Jumper Wire
 * USB cable
 
## CIRCUIT DIAGRAM
![Mighty Hango-Allis](https://user-images.githubusercontent.com/66871603/167676471-9cbd239a-7f71-4657-b715-5e6e4a4f35e2.png)

## CODE
```
int potpin=0;
int ledpin=7; 
int val=0;
void setup()
{
pinMode(ledpin,OUTPUT);
Serial.begin(9600);
}
void loop()
{
val=analogRead(potpin);
Serial.println(val);
analogWrite(ledpin,val/4);
delay(10);
}

```
## OUTPUT
![WhatsApp Video 2022-05-10 at 9 43 30 PM](https://user-images.githubusercontent.com/66871603/167675239-82a289f9-630e-4123-b9a7-250117a2a817.gif)


# ASSIGNMENT 2-Digital dice using button and 6 LEDs

## Components Required
* Arduino Uno
* 6-LEDs
* push button Switch
* 10K Ohm Resistor
* Connecting Wires
* 6-220K Ohm Resistor

## Connection Setup
![167541050-f24bd9c8-1846-4977-a5c4-3ef96f427490](https://user-images.githubusercontent.com/66871603/167677686-177f51c2-693f-4cfe-b39c-e453dc978f1a.jpg)

 
## Code
```
int led1 = 12;
int led2 = 11;
int led3 = 10;
int led4 = 9;
int led5 = 8;
int led6 = 7;
int button = 6;
int randNum = 0;
void setup() {
  // put your setup code here, to run once:
  randomSeed(analogRead(0));

  pinMode(button,INPUT);

  pinMode(led1,OUTPUT);
  pinMode(led2,OUTPUT);
  pinMode(led3,OUTPUT);
  pinMode(led4,OUTPUT);
  pinMode(led5,OUTPUT);
  pinMode(led6,OUTPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
  if(digitalRead(button)==HIGH)
  {
    randNum = random(7,13);
    digitalWrite(randNum,HIGH);
    delay(2000);
    digitalWrite(randNum,LOW);
  }
}
```
## Output Gif
![ezgif-3-ae74864a10](https://user-images.githubusercontent.com/66871603/167683194-11fb73d4-b408-4f21-8758-5cc0388be1b3.gif)

