---
layout: post
title: "Entregável de Mecânica: Montagem do Chassi 2WD e Estrutura do GASr"
date: 2026-10-23
---

# Entregável de Mecânica — Montagem e Estrutura Física

**Disciplina:** Oficina de Integração — Engenharia Eletrônica (UTFPR - Curitiba)  
**Equipe:** Adrian Valt Hohmann, Fabio Manoel, Luiz Henrique de Souza Correia e Rafael JS  
**Data do Entregável:** 23/10/2026  

---

## 1. Visão Geral da Montagem Mecânica

Dando continuidade ao desenvolvimento do **GASr (Guardião Automatizado Sobre Rodas)**, concluímos a etapa referente à montagem e estruturação mecânica da plataforma robótica móvel.

A estrutura foi baseada no kit de chassi acrílico 2WD, projetada para garantir estabilidade no percurso e suporte adequado para a eletrônica embarcada:

* **Chassi Base:** Montagem da estrutura acrílica principal e fixação dos suportes mecânicos.
* **Sistema de Tração:** Acoplamento dos dois motores DC com caixa de redução e rodas de borracha principais.
---

## 2. Elementos de Segurança e Alimentação

Em conformidade com os requisitos de hardware e segurança definidos na proposta do projeto:

* **Botão Físico de Parada:** Instalação do interruptor mecânico diretamente interligado à linha principal de alimentação, garantindo o corte físico imediato de energia em situações de emergência.
* **Sistema de Baterias:** Fixação do suporte para baterias 18650 recarregáveis com chave ON/OFF integrada, posicionadas estrategicamente para equilibrar o centro de gravidade do robô.
* **Organização Espacial:** Disposição dos níveis para fixação futura dos drivers de motor (Ponte H TB6612FNG), dos dois microcontroladores ESP32 (Mestre e Escravo) e das placas de prototipagem.

---

## 3. Status das Atividades do Cronograma

Com base no planejamento da equipe para o entregável de 23/10, o progresso das tarefas mecânicas encontra-se detalhado a seguir:

| Atividade / Entregável | Responsável | Status |
| :--- | :--- | :--- |
| Comprar chassi, motores e itens mecânicos | Rafael / Luiz | **Concluído no prazo** |
| Montar base/chassi do carrinho | Fabio / Rafael | **Concluído no prazo** |
| Montar motores, rodas e suportes | Fabio / Adrian | **Concluído no prazo** |
| Instalar botão físico de parada | Rafael / Luiz | **Concluído no prazo** |
| Verificar material da pista de testes | Rafael / Fabio | **Em andamento** |

---

## Próximos Passos

Com a estrutura mecânica montada e validada, as próximas etapas focarão na eletrônica de acionamento e sensoriamento:

1. Fixação do conjunto de sensores infravermelhos (QRE1113/TCRT5000) na parte inferior do chassi para o segue-linha.
2. Montagem e teste de acionamento dos motores via PWM com o driver Ponte H.
3. Fixação do suporte mecânico para os sensores ambientais (BME280 e MQ-135) no nó Mestre.


<p align="center">
  <img src="/BlogGASr/assets/images/diagrama_mecanico.svg" alt="Diagrama Mecânico e Elétrico" width="100%">
</p>


<p align="center">
  <img src="/BlogGASr/assets/images/DiagramaCarrinho.jfif" alt="Diagrama de montagem" width="100%">
</p>


<p align="center">
  <img src="/BlogGASr/assets/images/Foto_carrinho.jpeg" alt="Foto do estado atual do projeto" width="100%">
</p>
