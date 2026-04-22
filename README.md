# bridge-led-lighting-22-april-2026
 task to lighting three led with push button
 2.tools used >Arduino IDE
 >push button
 >led
>resister
>jumper wires
>code generation
int buttonPin = 2;

int led1 = 8;
void setup() {
int led2 = 9;
int led3 = 10;

bool ledState = false;    
int lastButtonState = HIGH; 

  pinMode(buttonPin, INPUT_PULLUP);

  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
}

void loop() {
  int currentButtonState = digitalRead(buttonPin);

  // Detect button press (HIGH → LOW)
  if (lastButtonState == HIGH && currentButtonState == LOW) {
    ledState = !ledState;   
    delay(50);              
  }

  lastButtonState = currentButtonState;

 
  if (ledState) {
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
  } else {
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
  }
}
