# SSC0180-Eletrônica
## Projeto: Dado Eletrônico
O projeto foi desenvolvido com o objetivo de construir um dado eletrônico que sorteia números aleatórios num intervalo de 1 à 6. Foi utilizado a IDE do Arduino UNO para desenvolver o código e a plataforma do Tinkercad para idealizar o projeto na prática.

  Software:
// C++ code
//
int N_C3_BAmero = 0;

int numero = 0;

void setup()
{
  pinMode(9, INPUT);
  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(8, OUTPUT);
  pinMode(7, OUTPUT);
  pinMode(6, OUTPUT);
}

void loop()
{
  // Quando aperta o botão, Leds ligam alternadamente
  while (digitalRead(9) == HIGH) {
    // Cada LED liga e desliga o anterior.
    digitalWrite(2, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(3, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(2, LOW);
    digitalWrite(5, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(3, LOW);
    digitalWrite(4, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(5, LOW);
    digitalWrite(8, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(4, LOW);
    digitalWrite(7, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(8, LOW);
    digitalWrite(6, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(7, LOW);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(6, LOW);
    delay(100); // Wait for 100 millisecond(s)
    // Quando chega no último, todos começam a ligar.
    digitalWrite(6, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(7, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(8, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(4, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(5, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(3, HIGH);
    delay(100); // Wait for 100 millisecond(s)
    digitalWrite(2, HIGH);
    delay(300); // Wait for 300 millisecond(s)
    // Todos desligam.
    digitalWrite(2, LOW);
    digitalWrite(3, LOW);
    digitalWrite(4, LOW);
    digitalWrite(5, LOW);
    digitalWrite(6, LOW);
    digitalWrite(7, LOW);
    digitalWrite(8, LOW);
    delay(500); // Wait for 500 millisecond(s)
    // Sorteia o número
    numero = random(1, 6 + 1);
  }
  // Dependendo do número sorteado, liga os LEDs
  // correspondentes.
  if (numero == 1) {
    digitalWrite(2, LOW);
    digitalWrite(3, LOW);
    digitalWrite(4, HIGH);
    digitalWrite(5, LOW);
    digitalWrite(6, LOW);
    digitalWrite(7, LOW);
    digitalWrite(8, LOW);
  }
  if (numero == 2) {
    digitalWrite(2, HIGH);
    digitalWrite(3, LOW);
    digitalWrite(4, LOW);
    digitalWrite(5, LOW);
    digitalWrite(6, HIGH);
    digitalWrite(7, LOW);
    digitalWrite(8, LOW);
  }
  if (numero == 3) {
    digitalWrite(2, HIGH);
    digitalWrite(3, LOW);
    digitalWrite(4, HIGH);
    digitalWrite(5, LOW);
    digitalWrite(6, HIGH);
    digitalWrite(7, LOW);
    digitalWrite(8, LOW);
  }
  if (numero == 4) {
    digitalWrite(2, HIGH);
    digitalWrite(3, LOW);
    digitalWrite(4, LOW);
    digitalWrite(5, HIGH);
    digitalWrite(6, HIGH);
    digitalWrite(7, LOW);
    digitalWrite(8, HIGH);
  }
  if (numero == 5) {
    digitalWrite(2, HIGH);
    digitalWrite(3, LOW);
    digitalWrite(4, HIGH);
    digitalWrite(5, HIGH);
    digitalWrite(6, HIGH);
    digitalWrite(7, LOW);
    digitalWrite(8, HIGH);
  }
  if (numero == 6) {
    digitalWrite(2, HIGH);
    digitalWrite(3, HIGH);
    digitalWrite(4, LOW);
    digitalWrite(5, HIGH);
    digitalWrite(6, HIGH);
    digitalWrite(7, HIGH);
    digitalWrite(8, HIGH);
  }
}
Circuito com TODAS as conexoes com o Arduino/ESP32:

Imagens do Projeto:

Incluir um VIDEO mostrando o Projeto funcionando e/ou simulando, e explicando como calculou os valores dos componentes periféricos (Upa o vídeo no Youtube ou google drive e poe um link no Readme do teu Github/gitlab).
