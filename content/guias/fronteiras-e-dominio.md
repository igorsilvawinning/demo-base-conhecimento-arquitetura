---
title: Fronteiras e domínio
kind: guia
order: 2
summary: Primeiro o contexto delimitado e o dono do dado. Depois a regra de dependências dentro do contexto. A equipa segue a fronteira quando ela já é estável.
uses:
  - ddd
  - clean-architecture
  - hard-parts
  - team-topologies
sources: []
---

Partir um sistema é uma decisão sobre mudança, consistência e carga cognitiva. Não é uma decisão sobre tecnologia. Este guia fixa a ordem em que essas perguntas se respondem.

## Ordem das decisões

1. **Linguagem e contexto.** Há um glossário com um significado por termo. Os termos que mudam juntos, e que uma mesma pessoa de negócio reconhece, formam um contexto delimitado. Dois significados para a mesma palavra — «cliente» na angariação e «cliente» na cobrança — são dois contextos, mesmo que hoje vivam no mesmo processo.
2. **Dono do dado.** Cada facto tem uma fonte de verdade. Os outros contextos guardam uma cópia, uma referência ou perguntam. Não há duas escritas do mesmo facto. Esta é a decisão que [The Hard Parts](../referencias/hard-parts.md) trata como trade-off, e que aqui fica registada num ADR.
3. **Como os contextos colaboram.** Chamada síncrona quando a resposta é necessária para continuar e a indisponibilidade do vizinho é aceitável como indisponibilidade nossa. Evento quando o trabalho pode seguir e a consistência pode ser diferida. As duas opções escrevem-se com a consequência, não com a preferência da equipa.
4. **Dentro do contexto, a regra de dependências.** O domínio não importa frameworks, clientes HTTP nem o schema da base de dados. Os adaptadores é que dependem do domínio. É o que se pede emprestado à Clean Architecture. Não se exige a mesma árvore de pastas em todos os serviços. Exige-se que uma regra de negócio seja testável sem subir a infraestrutura.
5. **Equipa.** Uma equipa de fluxo fica dona de um ou mais contextos que consegue perceber por inteiro. Enquanto a fronteira ainda se descobre, duas equipas colaboram com prazo para acabar. Quando a fronteira estabiliza, a interação passa a contrato. Uma plataforma interna, se existir, oferece um caminho self-service. Não executa o deploy dos outros por ticket.

## Sinais para não extrair

- O «serviço» não tem dados próprios. Só encadeia chamadas. Isso é um distribuído à procura de um módulo.
- Toda a alteração de negócio toca nos dois lados ao mesmo tempo. A fronteira está no sítio errado. Voltar a juntar é uma decisão válida e também leva ADR.
- A equipa não consegue explicar o contexto sem ler o código do vizinho. Falta linguagem, não falta Kubernetes.

## O que fica escrito

Por cada contexto: o nome, os termos que lhe pertencem, os factos de que é fonte de verdade, e as integrações com o modo (síncrono ou evento) e a consistência aceite. Isto cabe na secção 3 e na secção 4 do arc42, mais os ADRs das escolhas que doeram.

Um agregado, no sentido do DDD, define-se quando há uma invariante que tem de ser verdade no fim de cada transação. Não se cria um agregado por tabela.
