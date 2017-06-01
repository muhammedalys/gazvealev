int led1 = 7;
int led2 =6;
void setup() {
  Serial.begin(9600);
  pinMode(led1,OUTPUT);
    pinMode(led2,OUTPUT);
}
void loop() {
  int sensorDegeri = analogRead(A0); /* Arduinonun A0 ayagindaki gerilim olculuyor */
   int sensorDegeri2 = analogRead(A1);
     Serial.println("Gaz Sensoru");
  Serial.println(sensorDegeri); /* olculen deger seri haberlesme ile yollaniyor */
    Serial.println("Alev Sensoru");
  Serial.println(sensorDegeri2);
  delay(1000); /* daha dogru bir olcum icin biraz bekleme kullanilmalidir */
if (sensorDegeri >300)
{
digitalWrite(led1, HIGH);
}
 else {
 digitalWrite(led1, LOW);
 }
 if (sensorDegeri2 >100)
{
digitalWrite(led2, HIGH);
}
 else {
 digitalWrite(led2, LOW);
 }
}
