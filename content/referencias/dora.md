---
title: Métricas DORA
kind: referencia
order: 7
summary: Frequência de deploy, lead time, taxa de falha das alterações e tempo de restauro. Sinal de capacidade de um serviço, não ranking de pessoas.
uses: []
sources:
  - label: DORA
    href: https://dora.dev
---

O programa DORA, ligado ao trabalho publicado em *Accelerate*, isolou quatro métricas que se movem juntas nas organizações com boa capacidade de entrega de software. Os relatórios anuais atualizam faixas e contexto. A definição estável é a que importa.

## As quatro

- **Frequência de deploy** em produção, por aplicação.
- **Lead time** do commit até produção. Não inclui o tempo em que a ideia esperou por aprovação, que se mede à parte se doer.
- **Taxa de alterações com falha.** Percentagem de deploys que exigem hotfix, rollback ou correção. A definição de falha fixa-se antes do gráfico.
- **Tempo de restauro** do serviço, do ponto de vista de quem o usa. Não é o tempo até ao post-mortem.

A DORA também trata confiabilidade como resultado visível para o utilizador. Não substitui as quatro. Senta-se ao lado.

## O que aproveitamos

Medição por serviço, a partir do sistema de versões e do de incidentes. As quatro leem-se juntas. As faixas publicadas em dora.dev são linguagem comum, não uma meta copiada de um relatório velho.

## O que não fazemos

Não comparamos pessoas. Não otimizamos uma métrica isolada. Não exigimos a faixa mais alta a um produto que, por decisão de negócio, muda pouco.
