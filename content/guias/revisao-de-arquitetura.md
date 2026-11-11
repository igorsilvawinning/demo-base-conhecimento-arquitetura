---
title: Revisão de arquitetura
kind: guia
order: 6
summary: A lista que um revisor percorre antes de aceitar uma mudança estrutural. Cada pergunta aponta ao guia onde a regra está explicada.
uses:
  - arc42
  - c4
  - adr
  - ddd
  - hard-parts
  - azure-waf
  - aws-waf
  - asvs
  - owasp-top10
  - dora
sources: []
---

Uma revisão de arquitetura olha para uma mudança que custa reverter: sistema novo, fronteira nova, novo armazenamento, nova integração, nova exposição à internet, mudança de fornecedor cloud. Não se convoca para uma feature dentro de um contexto já decidido.

O revisor pede evidência, não uma apresentação. O que não está no repositório não foi decidido. Foi dito numa reunião.

## Âmbito e qualidade

- Há um objetivo de negócio numa frase e dois a cinco objetivos de qualidade ordenados, com cenário (estímulo, ambiente, resposta, medida). Guia: documentar.
- O que está fora do âmbito está escrito. Inclui o que este sistema recusa fazer.

## Forma

- Existe um C1 atualizado se a mudança mexe em pessoas ou em sistemas vizinhos.
- Existe um C2 que mostra onde a mudança corre e com que protocolo fala.
- As decisões difíceis têm ADR em estado `proposto` ou `aceite`, com consequências negativas escritas. Uma lista só de benefícios reprova a revisão.

## Domínio e acoplamento

- Os termos novos estão no glossário, com um significado.
- Está nomeada a fonte de verdade de cada facto que a mudança escreve.
- Se nasce um serviço, ele tem dados ou uma invariante própria. Se não tem, a proposta explica porque é que um módulo não chega.
- A consistência entre contextos está dita: o que pode esperar, durante quanto tempo, e o que vê o utilizador enquanto espera.

## Cloud e operação

- A revisão Well-Architected usa o quadro do fornecedor onde a carga corre, e deixa riscos na secção 11 do arc42.
- Há dono do serviço em produção, objetivo de fiabilidade com número, e um restauro compatível com esse número.
- O caminho de deploy é o caminho pavimentado. Se a mudança precisa de uma exceção permanente, a exceção é a decisão, e leva ADR.
- Dá para ver, ou há um plano datado para ver, frequência de deploy, lead time, falhas de alteração e tempo de restauro deste serviço.

## Segurança

- O nível ASVS alvo está declarado e é coerente com o dano se a aplicação falhar.
- Controlo de acesso, configuração, cadeia de fornecimento, desenho e registo foram respondidos em concreto. «Vamos seguir o OWASP» não é resposta.
- Segredos, dados sensíveis e o que fica em logs estão identificados.

## Resultado da revisão

A revisão acaba com um de três estados, escrito no pull request: aceite, aceite com riscos assumidos (cada risco tem dono e data), ou recusada até as perguntas em aberto terem evidência. Não acaba com «ficou alinhado».
