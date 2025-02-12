const int motorPin1 = 9; 
const int motorPin2 = 10; 
const int buttonPin = 2;  

void setup() {
  pinMode(LED_BUILTIN, OUTPUT); 
  pinMode(motorPin1, OUTPUT);
  pinMode(motorPin2, OUTPUT);
  pinMode(buttonPin, INPUT_PULLUP); 
  Serial.begin(9600); 
}

void loop() {
  
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000);
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000);

  
  int buttonState = digitalRead(buttonPin);

  
  Serial.print("Button State: ");
  Serial.println(buttonState);

   
  if (buttonState == LOW) { 
    digitalWrite(motorPin1, HIGH);
    digitalWrite(motorPin2, LOW);
  } else {
    digitalWrite(motorPin1, LOW);
    digitalWrite(motorPin2, HIGH);
  }
}
# motor
