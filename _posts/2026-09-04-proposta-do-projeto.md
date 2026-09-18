---
layout: post
title: "Proposta do Projeto GASr: Guardião Automatizado Sobre Rodas"
date: 2026-09-04
---

# Projeto GASr — Guardião Automatizado Sobre Rodas

---

## 1. Descrição e Escopo do Projeto

Vazamentos de gases tóxicos e riscos de incêndio em ambientes fabris representam ameaças sérias à segurança dos trabalhadores. O **GASr** é uma plataforma robótica móvel autônoma do tipo seguidor de linha projetada para monitorar essas variáveis em tempo real.

O robô circulará por rotas industriais pré-determinadas realizando a medição contínua de temperatura, umidade, pressão e gases tóxicos, enviando as informações de forma remota para uma central de controle.

---

## 2. Arquitetura de Hardware

O sistema será dividido modularmente em dois nós de processamento com microcontroladores ESP32:

* **Carrinho (ESP Escravo):** Responsável pela locomoção, seguimento de linha e identificação do setor na pista.
* **Sensoriamento (ESP Mestre):** Responsável pela aquisição dos dados do sensor BME280 (temperatura, umidade e pressão) e do sensor MQ-135 (detecção de gases), além da transmissão sem fio.
* **Interface do Usuário:** Dashboard/aplicativo para monitoramento contínuo e acionamento do comando de parada remota.

---

## 3. Arquitetura de Software e FreeRTOS

Para garantir respostas rápidas no controle dos motores sem interrupções provocadas por leituras de sensores ou comunicação Wi-Fi, o software utilizará o sistema operacional de tempo real **FreeRTOS** distribuído nos dois núcleos (*cores*) do ESP32:

* **Core 1:** Tarefas de alta prioridade de controle de linha e motores.
* **Core 0:** Tarefas de comunicação, telemetria e envio de dados para a interface.

---

## Próximos Passos

Nas próximas postagens, compartilharemos:
1. Montagem do kit de chassi 2WD e testes iniciais de movimentação.
2. Calibração dos sensores infravermelhos de linha.
3. Integração e testes do sistema operacional FreeRTOS.
