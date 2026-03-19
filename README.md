# hello-world
Practing GitHub flow

// the setup function runs once when you press reset or power the board
void setup() {
  //making pin 8 output pin
  pinMode(8, OUTPUT);
  //adding button to circuit, reading from pin 2
  //pullup mode because we are reading the pin as an active low, so when pressed light blinks
  pinMode(2, INPUT_PULLUP);
}
void loop (){
  //making button a variable to read when doing comparison in loop
  int button = digitalRead(2);

// the loop function runs over and over again foreve
  if (button == LOW){
      digitalWrite(8, HIGH);  // turn the LED on (HIGH is the voltage level)
      delay(500);                      // wait for a second
      digitalWrite(8, LOW);   // turn the LED off by making the voltage LOW
      delay(500);     
      digitalWrite(8, HIGH); 
      delay(500);                      
      digitalWrite(8, LOW);   
      delay(500);                  
  }
  //if high, not pressed, keep the light off
  else{
    digitalWrite(8, LOW);
  }
}
