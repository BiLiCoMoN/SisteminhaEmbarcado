# Sisteminha Embarcado
---------------------------------------
O circuito escolhido é baseado na atuação de um LDR no controle de luminosidade de um led, por meio de um arduino e linguagem de programação.
Situação que pode se aplicar, por exemplo, ao controle de luminosidade de um jardim
## Segue a lista de componentes utilizados:
-Placa Arduino (como Arduino Uno)
-Sensor de Luz (LDR - Light Dependent Resistor)
-Resistor (10kΩ)
-LED
-Resistor para o LED (220Ω)
-Fios de conexão
-Protoboard (opcional, mas recomendado para facilitar as conexões)
---------------------------------------
## Segue o código utilizado:

int sensorPin = A0; // Pino do sensor
int ledPin = 9;     // Pino do LED

void setup() {
    pinMode(ledPin, OUTPUT);
}

void loop() {
    int sensorValue = analogRead(sensorPin); // Leitura do sensor
    if (sensorValue < 500) { // Se a luz estiver baixa
        digitalWrite(ledPin, HIGH); // Liga o LED
    } else {
        digitalWrite(ledPin, LOW); // Desliga o LED
    }
    delay(100); // Espera um pouco antes da próxima leitura
}

![image](https://github.com/user-attachments/assets/1300f69d-2d2e-4fa1-a6f7-792ba14418ae)
