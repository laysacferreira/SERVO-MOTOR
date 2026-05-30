# 🤖 Projeto: Sistema de Controle com OLED, Servo e LEDs (MicroPython)

## 🧠 Sobre o Projeto

Este projeto foi desenvolvido em MicroPython com o objetivo de criar um sistema interativo utilizando botões, LEDs, display OLED e um servo motor. Ele simula um controle de estado (ligado/desligado) com feedback visual e físico.

## 📄 Descrição

O sistema utiliza os seguintes componentes:

* 🔴 LED vermelho (pino 25)
* 🟢 LED verde (pino 26)
* 🔘 Botão azul (pino 12)
* 🔘 Botão verde (pino 14)
* 📟 Display OLED (I2C)
* ⚙️ Servo motor (pino 18)

### 🔵 Botão Azul – Luz Acesa

Ao pressionar:

* O display mostra **"Luz acesa"**
* O LED verde pisca
* O servo motor se move para a posição 0°

### 🟢 Botão Verde – Luz Apagada

Ao pressionar:

* O display mostra **"Luz apagada"**
* O LED vermelho pisca
* O servo motor retorna para 90°

O sistema roda continuamente, verificando o estado dos botões e executando as ações correspondentes.

## ⚙️ Funcionamento Técnico

O projeto utiliza:

* Comunicação I2C para o display OLED (`ssd1306`)
* Controle de servo com PWM (`machine.PWM`)
* Leitura de botões com `PULL_UP`
* Controle de LEDs com saídas digitais
* Loop infinito (`while True`) para monitoramento contínuo

A função `mover_servo(angulo)` converte o ângulo desejado em sinal PWM, permitindo o posicionamento do servo.

## ▶️ Execução
![imagemservo](https://github.com/laysacferreira/SERVO-MOTOR/blob/main/servo.png)

## 🎯 Conclusão

Este projeto é ideal para quem deseja avançar em programação embarcada, integrando múltiplos componentes em um único sistema.

Ele demonstra, na prática, como combinar entrada (botões), saída visual (OLED e LEDs) e ação mecânica (servo), criando uma aplicação interativa completa.


