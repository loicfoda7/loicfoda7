// Lauflicht mit Taster
int taster=7;
int tasterstatus=0;
void setup() {
  // put your setup code here, to run once:
  for (int i=3; i<7;i++){
    pinMode(i, OUTPUT); // Pin 7 ist ein Ausgang.
  }
}

void loop() {
  // put your main code here, to run repeatedly:
  tasterstatus=digitalRead(taster);
  if (tasterstatus==HIGH){
for(int i=3; i<7;i++){
digitalWrite(i, HIGH); // Schalte die LED an Pin7 an.

delay(1000); // Warte 1000 Millisekunden.
}
for(int i=6; i>2; i--){
  delay(1000);
  digitalWrite(i, LOW); // Schalte die LED an Pin7 aus.
}
  }


}

