---
title: "MTTR — Mean Time to Recovery"
description: "Tempo médio que um sistema leva para se recuperar de uma falha."
tags: [observabilidade, sre, confiabilidade]
layout: post
---

## Definição

**MTTR** (_Mean Time to Recovery_ / _Mean Time to Repair_) é a média de tempo que um serviço leva para se **recuperar de uma falha**, desde o momento em que ela ocorre até o retorno ao funcionamento normal.

---

## Como é calculado

```
MTTR = Tempo total de recuperação / Número de incidentes
```

**Exemplo:** Se você teve 3 incidentes no mês com tempos de recuperação de 30min, 20min e 10min:

```
MTTR = (30 + 20 + 10) / 3 = 20 minutos
```

---

## Por que reduzir o MTTR?

Um MTTR baixo indica que o time consegue **detectar, diagnosticar e corrigir** falhas rapidamente. Para isso, você precisa de:

- **Observabilidade** — logs, métricas e traces bem estruturados
- **Alertas acionáveis** — que indicam o problema, não só o sintoma
- **Runbooks** claros para os incidentes mais comuns
- **On-call bem definido** com responsabilidades claras

---

## MTTR vs MTTD vs MTTF

| Sigla    | Significado                                         |
| -------- | --------------------------------------------------- |
| **MTTD** | _Mean Time to Detect_ — tempo para detectar a falha |
| **MTTR** | _Mean Time to Recovery_ — tempo para recuperar      |
| **MTTF** | _Mean Time to Failure_ — tempo médio entre falhas   |

MTTR = MTTD + tempo de diagnóstico + tempo de correção.

---

## Recursos

- [Google SRE Book — Incident Response](https://sre.google/sre-book/incident-management/)
