#define led 6
#define red 4
char code;

void setup() {
  Serial.begin(9600);
  pinMode(led,OUTPUT);
  pinMode(red,OUTPUT);


}

void loop() {
  if(Serial.available())
  {
    code=Serial.read();

  }
  if(code=='1')
  {
    digitalWrite(led,HIGH);
    digitalWrite(red,LOW);
  }
  else if (code=='0')
  {
    digitalWrite(led,LOW);
    digitalWrite(red,HIGH);
  }
}
