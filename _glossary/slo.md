---
title: "SLO — Service Level Objective"
description: "Meta mensurável de confiabilidade que um serviço deve atingir dentro de um período."
tags: [observabilidade, sre, confiabilidade]
layout: post
---

## Definição

Um **SLO** (_Service Level Objective_) é uma meta de confiabilidade definida internamente para um serviço. Ele expressa **o quão disponível ou performático** um serviço precisa ser dentro de um período de tempo.

---

## Exemplo prático

> "99,9% das requisições ao serviço de login devem ter latência inferior a 500ms, medido mensalmente."

Isso significa que o serviço pode falhar essa métrica em apenas **0,1% do tempo** — o chamado **error budget** (orçamento de erro).

---

## SLO vs SLA vs SLI

| Termo   | O que é                                                                              |
| ------- | ------------------------------------------------------------------------------------ |
| **SLI** | _Service Level Indicator_ — a métrica real sendo medida (ex: latência p99)           |
| **SLO** | _Objective_ — a meta que você quer atingir (ex: latência < 500ms em 99,9% dos casos) |
| **SLA** | _Agreement_ — o contrato com o cliente, com penalidades se não for atingido          |

O SLO é o mais importante para o time de engenharia: ele guia decisões de priorização e alertas.

---

## Por que SLOs importam?

- Evitam o ciclo vicioso de "precisamos de 100% de uptime"
- Criam um **error budget** explícito que permite inovar com segurança
- Alinham engenharia e produto em torno de metas reais de confiabilidade
- São a base para alertas **acionáveis** (ao invés de alertas que ninguém age)

---

## Recursos

- [Google SRE Book — SLOs](https://sre.google/sre-book/service-level-objectives/)
- [SLO Adoption Guide — Datadog](https://www.datadoghq.com/knowledge-center/service-level-objectives/)
