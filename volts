#include <Wire.h>

#include <LiquidCrystal.h>

LiquidCrystal lcd(13, 12, 11, 10, 9, 8);

int analogPin1 = A0;
int analogPin2 = A1;
int val1 = 0;
int val2 = 0;
int val = 0;
int lastVal = -1;

void setup() {
  // put your setup code here, to run once:
  pinMode(4, OUTPUT);
  lcd.begin(16, 2);
  lcd.setCursor(0, 0);
  // lcd.print("Hello World");
}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite(4, HIGH);
  val1 = analogRead(analogPin1);
  val2 = analogRead(analogPin2);
  val = val1 - val2;
  if (val != lastVal) {
    lastVal = val;
    lcd.setCursor(0, 0);
    lcd.print((val * (5.0 / 1023.0)));
    lcd.print("    ");
  }
}
