int i=0;
int randnumber=0;
void setup() {
  // put your setup code here, to run once:
  pinMode(1,OUTPUT);
  pinMode(2,OUTPUT);
  pinMode(3,OUTPUT);
  pinMode(4,OUTPUT);
  pinMode(5,OUTPUT);
  pinMode(6,OUTPUT);
  pinMode(8,INPUT);  
}

void loop() {
  int pressed=digitalRead(8);
  randnumber=random(1,7);

  if(pressed==HIGH){
    for(i=1;i<7;i++){
      digitalWrite(i,LOW);
    }
    delay(50);
    for(i=1;i<7;i++){
      if (i!=1){
        digitalWrite(i-1, LOW);
      }
      digitalWrite(i, HIGH);
      delay(100);
    }
    for(i=6;i>=1;i--){
      if(i!=6){
        digitalWrite(i+1, LOW);
      }
      digitalWrite(i, HIGH);
      delay(100);
    }
    if(randnumber==1){
      digitalWrite(1,HIGH);
      }
    if(randnumber==2){
      digitalWrite(1,HIGH);
      digitalWrite(2,HIGH);
      }
    if(randnumber==3){
      digitalWrite(1,HIGH);
      digitalWrite(2,HIGH);
      digitalWrite(3,HIGH);
      }
    if(randnumber==4){
      digitalWrite(1,HIGH);
      digitalWrite(2,HIGH);
      digitalWrite(3,HIGH);
      digitalWrite(4,HIGH);
      }
    if(randnumber==5){
      digitalWrite(1,HIGH);
      digitalWrite(2,HIGH);
      digitalWrite(3,HIGH);
      digitalWrite(4,HIGH);
      digitalWrite(5,HIGH);
      }
    if(randnumber==6){
      digitalWrite(1,HIGH);
      digitalWrite(2,HIGH);
      digitalWrite(3,HIGH);
      digitalWrite(4,HIGH);
      digitalWrite(5,HIGH);
      digitalWrite(6,HIGH);
      }
  }
}
