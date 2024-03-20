# Line-Follower-Bot

Group members: Abhirup Choudhary, Akshaya Jha, Arush Srivastava, Tanya Yadav, Anirban Chatterjee, Palak Kumari, Muskan Jain
Project alloted on 4th March,2024
Submission deadline: 20th March,2024

Materials and devices used: Arduino, 2 motors, 1 castor wheel, male to male wires, male to female wires, wooden, drilling machine, soldering machine, hot glue gun, double sided tape; 5 IR sensors, breadboard, battery, pair of wheels, 

Week 1: 
Cutting of wood for chassis and gathering other components done by Arush, Abhirup and Anirban
Basic code for sensors and motors written by Tanya and Akshaya
Assembly of components like castor wheel, motors, and wheels on the chassis done by Abhirup, Arush, Anirban, Tanya, Akshaya

Week 2: 
Code according to the bot written by Abhirup for ir and motors separately.
Basic code for sensor esp 32

#define SENSOR_PIN_1
#define SENSOR_PIN_2

#define MOTOR_PIN_RIGHT_1
#define MOTOR_PIN_lEFT_1
#define MOTOR_PIN_RIGHT_2
#define MOTOR_PIN_LEFT_2

void setup(){
  pinMode(SENSOR_PIN_1,INPUT)
  pinMode(SENSOR_PIN_2,INPUT)

  pinMode(MOTOR_PIN_RIGHT_1,OUTPUT)
  pinMode(MOTOR_PIN_LEFT_1,OUTPUT)

void loop(){
  int sensor1=digitalRead(SENSOR_PIN_1)
  int sensor2=digitalRead(SENSOR_PIN_2)

  if(sensor1==HIGH && sensor2==LOW){
    moveRightwards();
  }
  else if (sensor2==HIGH && sensor1==LOW){
    moveLeftwards(); 
  }
  else if (sensor1==HIGH && sensor2==HIGH}{
    moveForward();
  }
  else if (sensor1==LOW && sensor2==LOW){
    stopMoving();
  }
}

void moveForward(){
  digitalWrite(MOTOR_LEFT_PIN_1, HIGH);
  digitalWrite(MOTOR_RIGHT_PIN_1, HIGH);
}

void moveLeftwards(){
  digitalWrite(MOTOR_LEFT_PIN_1, HIGH);
  digitalWrite(MOTOR_RIGHT_PIN_1, LOW);
}

void moverRightwards(){
  digitalWrite(MOTOR_LEFT_PIN_1, LOW);
  digitalWrite(MOTOR_RIGHT_PIN_1, HIGH);
}

void ()stopMoving{
  digitalWrite(MOTOR_LEFT_PIN_1, LOW);
  digitalWrite(MOTOR_RIGHT_PIN_1, LOW);
}
