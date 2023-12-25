# Arduino-Servo-Control-with-Potentiometer
Control a servo motor using a potentiometer with Arduino.
#define SERVO_PIN 9
#define POTENTIOMETER_PIN A0

void setup() {
    pinMode(SERVO_PIN, OUTPUT);
    pinMode(POTENTIOMETER_PIN, INPUT);
}

void loop() {
    int potValue = analogRead(POTENTIOMETER_PIN);
    int servoAngle = map(potValue, 0, 1023, 0, 180);
    digitalWrite(SERVO_PIN, servoAngle);

    // Servo control logic here
}
