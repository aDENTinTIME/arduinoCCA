##### arduinoCCA


## May 25, 2017
I was trying to get two LEDs to blink at the same time, but wanted to minimize the code necessary, I tried a couple things I figured wouldn't work, just to see how it would act.

**First:**
```
int led = 3;
int led = 7;

void loop() {
  analogWrite(led, brightness);
}
```
>This gave me an error becuase I was trying to "redefine" the integer.

**Second:**
```
int led = 3;
int led2 = 7;

void loop() {
  analogWrite(led + led2, brightness);
}
```
>This compiled and uploaded fine, but didn't blink EITHER LED, after looking at it written out I realized what the program was doing, (obviously) it was sending a signal to PIN 10 as it added the two integers together. This however gave me an idea.

**Third:**
```
int led = 1;
int led2 = 2;

void loop() {
  analogWrite(led + led2, brightness);
}
```
>YAY... I got the first LED blinking (again.) This wasn't really a huge revelation but it's interesting nonetheless to me.

**Conclusion:**
```
1+2=3
```



## May 24, 2017
```
// Two_Blinks

void setup() {
  // initialize digital pins 11 & 12 as outputs.
  pinMode(11, OUTPUT);
  pinMode(12, OUTPUT);
}

void loop() {
  digitalWrite(11, HIGH);  //11 ON
  delay(500);
  digitalWrite(11, LOW);  //11 OFF

  digitalWrite(12, HIGH);  //12 ON
  delay(250);
  digitalWrite(12, LOW);  //12 OFF
}
```
