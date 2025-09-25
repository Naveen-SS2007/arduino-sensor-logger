# arduino-sensor-logger
LED blinking using Arduino board and Arduino IDE


// Pin assignments
const int ledPin = 13;      // Built-in LED on most Arduino boards
const int buttonPin = 2;    // Digital pin where the pushbutton is connected

void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT_PULLUP); // use internal pull-up resistor
}

void loop() {
  // Read button (LOW when pressed because of INPUT_PULLUP)
  int buttonState = digitalRead(buttonPin);

  if (buttonState == LOW) {
    digitalWrite(ledPin, HIGH); // LED on while button pressed
  } else {
    digitalWrite(ledPin, LOW);  // LED off when button released
  }
}