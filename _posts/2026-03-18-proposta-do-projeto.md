---
layout: post
title: "Proposta do Projeto GASr: Guardião Automatizado Sobre Rodas"
date: 2026-03-18
---

# Projeto GASr — Guardião Automatizado Sobre Rodas[cite: 1]

**Disciplina:** Oficina de Integração — Engenharia Eletrônica (UTFPR - Curitiba)[cite: 1]  
**Orientador:** Prof. César M. Vargas Benítez[cite: 1]  
**Equipe:** Adrian Valt Hohmann, Fabio Manoel, Luiz Henrique de Souza Correia e Rafael JS[cite: 1]  

---

## 1. Descrição e Escopo do Projeto[cite: 1]

Vazamentos de gases tóxicos e riscos de incêndio em ambientes fabris representam ameaças sérias à segurança dos trabalhadores[cite: 1]. O **GASr** é uma plataforma robótica móvel autônoma do tipo seguidor de linha projetada para monitorar essas variáveis em tempo real[cite: 1].

O robô circulará por rotas industriais pré-determinadas realizando a medição contínua de temperatura, umidade, pressão e gases tóxicos, enviando as informações de forma remota para uma central de controle[cite: 1].

---

## 2. Arquitetura de Hardware[cite: 1]

O sistema será dividido modularmente em dois nós de processamento com microcontroladores ESP32[cite: 1]:

* **Carrinho (ESP Escravo):** Responsável pela locomoção, seguimento de linha e identificação do setor na pista[cite: 1].
* **Sensoriamento (ESP Mestre):** Responsável pela aquisição dos dados do sensor BME280 (temperatura, umidade e pressão) e do sensor MQ-135 (detecção de gases), além da transmissão sem fio[cite: 1].
* **Interface do Usuário:** Dashboard/aplicativo para monitoramento contínuo e acionamento do comando de parada remota[cite: 1].

---

## 3. Arquitetura de Software e FreeRTOS[cite: 1]

Para garantir respostas rápidas no controle dos motores sem interrupções provocadas por leituras de sensores ou comunicação Wi-Fi, o software utilizará o sistema operacional de tempo real **FreeRTOS** distribuído nos dois núcleos (*cores*) do ESP32[cite: 1]:

* **Core 1:** Tarefas de alta prioridade de controle de linha e motores[cite: 1].
* **Core 0:** Tarefas de comunicação, telemetria e envio de dados para a interface[cite: 1].

---

## Próximos Passos[cite: 1]

Nas próximas postagens, compartilharemos:
1. Montagem do kit de chassi 2WD e testes iniciais de movimentação[cite: 1].
2. Calibração dos sensores infravermelhos de linha[cite: 1].
3. Integração e testes do sistema operacional FreeRTOS[cite: 1].
