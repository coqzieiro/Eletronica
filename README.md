# SSC0180-Eletrônica
## Projeto: Dado Eletrônico
O projeto foi desenvolvido com o objetivo de construir um dado eletrônico que sorteia números aleatórios num intervalo de 1 à 6.

#### Teoria



### Software: IDE Arduino

Código do projeto: 
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

### Componentes Eletrônicos
| Quantidade     | Componentes | Especificações | Valor |
| ---      | ---       | ---      | ---     |
| 7 | [LED](https://produto.mercadolivre.com.br/MLB-2601528464-transformador-trafo-1212v-500ma-bivolt-_JM)  | 2V/20mA     |  R$ 0,27   |
| 1 |[Resistor 10kΩ](https://www.baudaeletronica.com.br/produto/resistor-10k-5-18w.html)| 10000Ω 1/8W | R$ 0,06 |
| 7     | [Resistor 220 Ω](https://loja.fabricadebolso.com.br/10-x-resistor-220-ohms-14-w-eletronica-resistencia-220r)        | 220Ω 1/4W     | R$ 0,15  |
| 1     | [Botão de Pressão](https://www.baudaeletronica.com.br/produto/chave-tactil-6x6x5mm-4-terminais.html)        | 6x6x5mm 4 Terminais  | R$ 0,25    |
    
Valor Total: R$ 3, 25


### Imagens

Segue abaixo, as imagens que representam o funcionamento do dado eletrônico com todas as conexões:

- Circuito completo (TinkerCAD): 
O projeto esquemático no TinkerCAD nos permitiu modelar o funcionamento do Dado Eletrônico e prever possíveis erros durante a montagem.

[Link Circuito](https://www.tinkercad.com/things/570NiqwNX0R-brave-allis-sango/editel?tenant=circuits)
  
[Projeto .BDR](https://drive.google.com/drive/folders/1SZlMijGtk7tgy2nftMfKCPZPz4bhTYNO?usp=sharing)

![image](https://github.com/coqzieiro/SSC0180-Eletronica/assets/129008295/b2378904-44b4-4cdc-ac6d-9afe407cfc59)

- Circuito na protoboard:
Montou-se o circuito na protoboard usando o modelo do TinkerCAD e verificando se os valores de tensão e corrente estavam compatíveis com a teoria.

![WhatsApp Image 2023-07-09 at 12 51 49 (2)](https://github.com/coqzieiro/SSC0180-Eletronica/assets/129008295/22842ad0-7525-43b6-b4e9-3cfb37687a07)

- Placa de Arduino UNO:
A placa de arduino foi usada como meio para controlar o funcionamento da tensão e da corrente que passam pelos resistores e LEDS.

![WhatsApp Image 2023-07-09 at 12 51 49 (1)](https://github.com/coqzieiro/SSC0180-Eletronica/assets/129008295/4c2fadf5-6738-4cde-9b9b-1570ab5276e6)

#### Vídeo Funcionando

Segue abaixo o vídeo do projeto em funcionamento. Perceba que a cada vez que o botão é pressionado os LEDS acendem de maneira diferente.

https://github.com/coqzieiro/SSC0180-Eletronica/assets/129008295/c80bf15b-5357-403e-a236-c5eecd4eabc7

### Resposáveis
- Felipe da Costa Coqueiro
- Fernando Alee Suaiden
- Guilherme Torquato
- Adhemar Molon Neto
