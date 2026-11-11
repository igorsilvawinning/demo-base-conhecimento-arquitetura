---
title: Software Architecture — The Hard Parts
kind: referencia
order: 9
summary: Trade-offs de sistemas distribuídos — granularidade, dados, contratos, consistência — decididos com consequência escrita, não com estilo preferido.
uses: []
sources:
  - label: O'Reilly, ficha do livro
    href: https://www.oreilly.com/library/view/software-architecture-the/9781492086888/
---

Neal Ford, Mark Richards, Pramod Sadalage e Zhamak Dehghani tratam as decisões que continuam difíceis depois de escolhida a tecnologia. O livro é um conjunto de trade-offs com um domínio exemplo. Não se reproduz aqui. Usamos as perguntas.

## Perguntas que ficam

- Esta parte muda sozinha, tem dados próprios e uma equipa que a percebe? Se não, a granularidade está fina demais.
- Quem é a fonte de verdade deste facto, e quem guarda cópia?
- A chamada síncrona torna o vizinho parte da nossa disponibilidade? Se sim, esse acoplamento foi aceite em voz alta?
- A consistência pode ser diferida? Durante quanto tempo, e o que vê o utilizador?
- O contrato entre os dois lados sobrevive a uma mudança só de um deles?
- Partir isto em transações distribuídas cria um monólito distribuído com passos extra?

## O que aproveitamos

Nenhuma destas perguntas se responde com «microserviços» ou «monólito» como identidade. Responde-se com um ADR que diga a alternativa rejeitada e o custo que ficou. Voltar a juntar dois serviços é um desenho válido quando a mudança continua a atravessá-los juntos.

## O que não fazemos

Não citamos o livro como autoridade para uma granularidade fixa. O ponto do livro é que o trade-off depende do contexto, que tem de estar escrito.
