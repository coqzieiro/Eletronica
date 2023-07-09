# SSC0180-Eletrônica
## Projeto: Dado Eletrônico
O projeto foi desenvolvido com o objetivo de construir um dado eletrônico que sorteia números aleatórios num intervalo de 1 à 6. Foi utilizado a IDE do Arduino UNO para desenvolver o código e a plataforma do Tinkercad para idealizar o projeto na prática.

Software:
```cpp
int pinLeds1 = 10;
int pinLeds2 = 9;
int pinLeds3 = 7;
int pinLed4 = 8;
int buttonPin = 6;
int buttonState;
long ran;
int time = 2000;

void setup ()
{
  pinMode (pinLeds1, OUTPUT);
  pinMode (pinLeds2, OUTPUT);
  pinMode (pinLeds3, OUTPUT);
  pinMode (pinLed4, OUTPUT);
  pinMode (buttonPin, INPUT);
  randomSeed(analogRead(0));
}

void loop()
{
  buttonState = digitalRead(buttonPin);
  if (buttonState == HIGH){
    ran = random(1, 7);
    if (ran == 1){
      digitalWrite (pinLed4, HIGH);
      delay (time);
    }
    if (ran == 2){
      digitalWrite (pinLeds1, HIGH);
      delay (time);
    }
    if (ran == 3){
      digitalWrite (pinLeds3, HIGH);
      digitalWrite (pinLed4, HIGH);
      delay (time);
    }
    if (ran == 4){
      digitalWrite (pinLeds1, HIGH);
      digitalWrite (pinLeds3, HIGH);
      delay (time);
    }
    if (ran == 5){
      digitalWrite (pinLeds1, HIGH);
      digitalWrite (pinLeds3, HIGH);
      digitalWrite (pinLed4, HIGH);
      delay (time);
   }
   if (ran == 6){
      digitalWrite (pinLeds1, HIGH);
      digitalWrite (pinLeds2, HIGH);
      digitalWrite (pinLeds3, HIGH);
      delay (time);
   }
  }
  digitalWrite (pinLeds1, LOW);
  digitalWrite (pinLeds2, LOW);
  digitalWrite (pinLeds3, LOW);
  digitalWrite (pinLed4, LOW);
}

```
Peças necessárias:
Arduino
7 LEDs de qualquer tipo
1 resistor de 10k 
7 resistores de 220 
Um pequeno botão de pressão
Placa de prototipagem (breadboard)
Alguns fios para a placa de prototipagem (breadboard)

Circuito com TODAS as conexoes com o Arduino/ESP32:

![image](https://github.com/coqzieiro/SSC0180-Eletronica/assets/129008295/def71c95-d318-4088-9e58-1edb742e9f23)
![image](https://github.com/coqzieiro/SSC0180-Eletronica/assets/129008295/93d661a2-f6e3-49b7-a4a9-2945497139c6)


Imagens do Projeto:

Incluir um VIDEO mostrando o Projeto funcionando e/ou simulando, e explicando como calculou os valores dos componentes periféricos (Upa o vídeo no Youtube ou google drive e poe um link no Readme do teu Github/gitlab).
