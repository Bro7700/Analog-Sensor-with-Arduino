# Analog-Sensor-with-Arduino
Task 6







## Introduction








## Technologies


1- Arduino IDE 1.8.19 [To Download](https://www.arduino.cc/en/software)



2- AUTODESK TINKERCAD [To Download](https://www.tinkercad.com/)






## Components required



1. Arduino UNO
2. Temperature
3. jumper wirs





## Connections


connecting Temperature to Pin A0  and connecting GNR  and 5V in Arduino









## Block diagram & simulation


for watching simulation [OPEN](https://www.tinkercad.com/things/0eRq1obqDea-bodacious-crift-albar/editel?tenant=circuits)

![Bodacious Crift-Albar](https://user-images.githubusercontent.com/109243989/182015816-39feef29-438f-4fcb-96f1-5e7f084be29a.png)



#### The Code




int sensorPin = 0;

 
void setup()

{

  Serial.begin(9600);
  
}
 
void loop()

{
 
 int reading = analogRead(sensorPin);
 
 // measure the 5v with a meter for an accurate value
 
 //In particular if your Arduino is USB powered
 
 float voltage = reading * 4.68;
 
 voltage /= 1024.0;
 
 // now print out the temperature
 
 float temperatureC = (voltage - 0.5) * 100;
 
 Serial.print(temperatureC);
 
 Serial.println(" degrees C");
 
 delay(1000);
 
}


