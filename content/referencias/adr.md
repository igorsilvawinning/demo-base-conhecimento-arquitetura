---
title: ADR de Michael Nygard
kind: referencia
order: 3
summary: Um ficheiro curto por decisão de arquitetura, com contexto, decisão e consequências. O registo fica; a decisão pode ser substituída.
uses: []
sources:
  - label: Documenting Architecture Decisions (2011)
    href: https://www.cognitect.com/blog/2011/11/15/documenting-architecture-decisions
---

Em 2011 Michael Nygard descreveu um formato de uma página para decisões que condicionam o sistema. O valor está em o «porquê» sobreviver à saída das pessoas, não no cerimonial.

## Estrutura

- **Título** numerado, no presente, como se a decisão já valesse.
- **Estado:** proposto, aceite, substituído ou descontinuado. O substituído aponta para o sucessor e conserva-se.
- **Contexto:** factos e forças, antes de defender uma opção.
- **Decisão:** uma escolha, na voz ativa.
- **Consequências:** o que fica mais fácil, o que fica mais difícil, o que passa a ser verdade. Inclui operação.

Uma lista curta de alternativas rejeitadas não faz parte do texto original. Usamo-la quando a mesma discussão tende a voltar.

## O que aproveitamos

ADRs no repositório, em `docs/adr`, revistos como código, escritos antes de a decisão estar espalhada por vários serviços. Merece ADR o que leva mais de um dia a reverter: dados, fronteira, integração, identidade, consistência, «não vamos extrair isto».

## O que não fazemos

Não reescrevemos o contexto depois para ficar mais elegante. Não abrimos ADR para estilo de código. Não aceitamos uma decisão cujas consequências são todas positivas. Isso não foi uma decisão.
