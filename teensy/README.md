### Teensy Testing Code ###

#### Validating Motors ####
This Arduino code allows you to validate two motors at a time to ensure wiring and motor direction is correct. It only tests the motors turning, no encoder checks.

`//Motor 1 IN Pins
int motor1pin1 = 0;
int motor1pin2 = 23;

//Motor 2 IN Pins
int motor2pin1 = 2;
int motor2pin2 = 3;

//Motor 1 PWM Pin
int motor1PWM = 22;
//Motor 2 PWN Pin
int motor2PWM = 4;

void setup() {
  // put your setup code here, to run once:
  Serial.begin(115200);
  while(!Serial) {}
  pinMode(motor1pin1, OUTPUT);
  pinMode(motor1pin2, OUTPUT);
  pinMode(motor2pin1, OUTPUT);
  pinMode(motor2pin2, OUTPUT);

  pinMode(motor1PWM, OUTPUT); 
  pinMode(motor2PWM, OUTPUT);
  Serial.print("Setup complete");
  Serial.print("\n");
}

void loop() {
  // put your main code here, to run repeatedly:   
  Serial.print("Top of loop");
  Serial.print("\n");
  //Controlling speed (0 = off and 255 = max speed):
  analogWrite(motor1PWM, 200); //ENA pin
  analogWrite(motor2PWM, 200); //ENB pin

  //Controlling spin direction of motors:
  digitalWrite(motor1pin1, HIGH);
  digitalWrite(motor1pin2, LOW);

  digitalWrite(motor2pin1, HIGH);
  digitalWrite(motor2pin2, LOW);
  delay(1000);

  digitalWrite(motor1pin1, LOW);
  digitalWrite(motor1pin2, HIGH);

  digitalWrite(motor2pin1, LOW);
  digitalWrite(motor2pin2, HIGH);
  delay(1000);
  Serial.print("Bottom of loop");
  Serial.print("\n");
}`

#### Validating IMU ####
- On the Arduino IDE menu select Tools->Manage Libraries....
- Search for the MPU9250 and install `Bolder Flight Systems MPU9250`
- Under examples look for the folder and select Basic_I2C.  This should validate your MPU is connected properly to the Teensy board.

#### Encoder Calculations ####
- I rotated the front and rear left wheels 360 degrees, 3 times each and then took the average for the encoder count.  Here is the data:

  - [INFO] [1455208918.384447]: Encoder FrontLeft  : 3996
  - [INFO] [1617307219.144740]: Encoder FrontLeft  : 2662
  - Result 1: 1334
  - [INFO] [1617307542.280087]: Encoder FrontLeft  : 1364
  - Result 2: 1298
  - [INFO] [1617307655.408345]: Encoder RearLeft   : 51
  - Result 3: 1313
  - [INFO] [1455208918.393122]: Encoder RearLeft   : 4011
  - [INFO] [1617307219.155708]: Encoder RearLeft   : 2691
  - Result 4: 1320
  - [INFO] [1617307542.290093]: Encoder RearLeft   : 1386
  - Result 5: 1305
  - [INFO] [1617307655.408345]: Encoder RearLeft   : 51
  - Result 6: 1335
  - Average:1317.5 or 1318
