int count=0;
int pir1=5;
int pir2=6;
void setup()
{
  pinMode(pir1,INPUT);
  pinMode(pir2,INPUT);
  Serial.begin(9600);
  
}

void loop()
{
  if (digitalRead(pir1)==1)
  {
    delay(1000);
    if(digitalRead(pir2)==1){count++;Serial.println(count);}
    
  }
  else if (digitalRead(pir2)==1)
  {
    delay(1000);
    if(digitalRead(pir1)==1){count--;Serial.println(count);}
    
  }
  else{Serial.println(count);}
       delay(2000);
}
