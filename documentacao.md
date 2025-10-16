<p align="center">
  <img src="assets/Arduino_Logo.svg" width="200">
</p>

# Projeto Piscar LED com Arduino

Este projeto demonstra como controlar um LED (Light Emitting Diode) usando a placa de desenvolvimento **Arduino Uno**, um dos exercícios mais fundamentais e importantes para quem está começando com eletrônica e programação embarcada.

## 1. Componentes Necessários

Para replicar este projeto, você precisará dos seguintes componentes:

*   1 x Placa **Arduino Uno** (ou compatível)
*   1 x **Protoboard** (Placa de Ensaio)
*   1 x **LED** (de qualquer cor)
*   1 x **Resistor** de 220 Ohms (para proteger o LED)
*   2 x **Fios Jumper** (ou mais, dependendo da conexão)
*   1 x **Cabo USB** para conectar o Arduino ao computador

## 2. Montagem do Circuito

O circuito é simples e segue o princípio básico de ligar um LED com um resistor limitador de corrente.

### 2.1. Diagrama de Fiação (Tinkercad)

O diagrama a seguir, gerado no **Tinkercad Circuits**, ilustra a conexão correta dos componentes:

<p align="center">
  <img src="assets/tinkercad.png" width="600">
</p>

**Detalhes da Conexão:**

1.  Conecte o **ânodo** (perna mais longa) do LED a uma trilha da protoboard.
2.  Conecte um terminal do **resistor** de 220 Ohms à mesma trilha do ânodo do LED.
3.  Conecte o outro terminal do resistor ao **pino digital 13** do Arduino Uno (usando um fio jumper, geralmente vermelho para sinal).
4.  Conecte o **cátodo** (perna mais curta) do LED a outra trilha da protoboard.
5.  Conecte o cátodo do LED ao pino **GND** (Terra) do Arduino Uno (usando um fio jumper, geralmente preto).

### 2.2. Montagem Física (Protoboard)

A imagem abaixo mostra a montagem física do circuito na protoboard, conectada ao Arduino Uno:

<p align="center">
  <img src="assets/foto_protoboard.jpeg" width="500">
</p>

## 3. O Código

O programa é responsável por controlar o LED, fazendo-o piscar em intervalos regulares. O código foi extraído da imagem fornecida:

<p align="center">
  <img src="assets/print_codigo.jpeg" width="600">
</p>

```arduino
void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH); // acende o LED
  delay(1000);            // espera 1 segundo
  digitalWrite(13, LOW);  // apaga o LED
  delay(1000);            // espera 1 segundo
}
```

### 3.1. Explicação do Código

| Função | Descrição |
| :--- | :--- |
| `void setup()` | Executada uma única vez quando o Arduino é ligado ou reiniciado. |
| `pinMode(13, OUTPUT);` | Configura o pino digital 13 como **saída** (`OUTPUT`), permitindo que o Arduino envie energia para o LED. |
| `void loop()` | Executada repetidamente (em loop) enquanto o Arduino estiver ligado. |
| `digitalWrite(13, HIGH);` | Define o estado do pino 13 como **ALTO** (`HIGH`), fornecendo 5V e acendendo o LED. |
| `delay(1000);` | Pausa a execução do programa por **1000 milissegundos** (1 segundo). |
| `digitalWrite(13, LOW);` | Define o estado do pino 13 como **BAIXO** (`LOW`), fornecendo 0V e apagando o LED. |

## 4. Demonstração do Funcionamento

O vídeo a seguir demonstra o LED piscando após o código ser carregado na placa Arduino:

<p align="center">
  <video src="assets/video_funcionamento.mp4" width="500" controls>
  </video>
</p>
