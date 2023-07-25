# servo-motor-arduino
![Screenshot 2023-07-25 191632](https://github.com/M7moodalhayes/-servo-motor-arduino/assets/79692306/ff0f397e-6e1e-4c07-aca8-623d4c8b8641)
int output;
int pin = 6;

void setup()
{
  Serial.begin(9600);
}

void loop()
{
  output = map(analogRead(A0), 0, 1023, 0, 255);
  Serial.println(output);
  analogWrite(pin, output);
  delay(100);
}
![Screenshot 2023-07-25 192210](https://github.com/M7moodalhayes/-servo-motor-arduino/assets/79692306/a7c428ad-23d8-4639-9996-d2b00989012b)
// Incluimos la librería para Servo
#include <Servo.h>

Servo servoBase;//Asigno un nombre específico

void setup() {
   servoBase.attach(A1);//Pin a utilizar para servo
   servoBase.write(0);  //asigno 0 al servo motor
}

void loop() {

  for(int i=0; i<=180; i=i+10)
  {
   servoBase.write(i);
   delay(2000);
  }
 }
 
