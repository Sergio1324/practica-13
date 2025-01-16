# practica-13

// C++ code
//

#define L_VERDE 13
#define L_ROJO 12
#define RELE 11
#define PULS 10
bool pulsador = 0;
void setup(){
  pinMode (13, OUTPUT);
  pinMode (12, OUTPUT);
  pinMode (11, OUTPUT);
  pinMode (10, INPUT);
}

void loop() {
  pulsador = digitalRead(PULS);
  if (pulsador == 0) {
    digitalWrite (13, HIGH); //encende pin 13
    delay(4000); //wait for 4000 millisecond(s)
    digitalWrite (12, LOW); //encende pin 12
    delay(2000); //wait for 2000 millisecond(s)
    digitalWrite (11, LOW); //encende pin 11
    delay(2000); //wait for 2000 millisecond(s)
    digitalWrite (13, LOW); //apaga pin 13
    delay(2000); //wait for 2000 millisecond(s)
    digitalWrite (12, HIGH); //apaga pin 12
    delay(4000); //wait for 4000 millisecond(s)
    digitalWrite (11, HIGH); //apaga pin 11
    delay(4000); //wait for 4000 millisecond(s)
  }
}
