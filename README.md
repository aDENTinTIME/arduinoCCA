##### arduinoCCA

## HW May 24, 2017
void setup() {
  // initialize digital pins 11 & 12 as outputs.
  pinMode(11, OUTPUT);
  pinMode(12, OUTPUT);
}

void loop() {
  digitalWrite(11, HIGH);  //11 ON
  delay(500);
  digitalWrite(11, LOW);  //11 OFF
  delay(200);

  digitalWrite(12, HIGH);  //12 ON
  delay(250);
  digitalWrite(12, LOW);  //12 OFF
  delay(50);
}
