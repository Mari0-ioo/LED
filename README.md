# LED
// the setup routine runs once when you press reset:
int led =2;

int brightness = 255;

int fadeamout = 5;

void setup() {


  // initialize serial communication at 9600 bits per second:
  
  Serial.begin(9600);
  
  pinMode(led, OUTPUT);
  
}


// the loop routine runs over and over again forever:

void loop() {

  // read the input on analog pin 0:
  
  int knobValue = analogRead(A0);
  
   // print out the value you read:
   
  Serial.println(knobValue);
  

 if(knobValue >= 400)
 
 {
  digitalWrite(led, HIGH);
  
 }

 else {
  digitalWrite(led, LOW);
  
 }
 
}
