---
title: Clean Architecture
kind: referencia
order: 11
summary: A regra de dependências. O domínio não conhece o framework, a base de dados nem o transporte. Os detalhes é que apontam para dentro.
uses: []
sources:
  - label: InformIT, ficha do livro
    href: https://www.informit.com/store/clean-architecture-a-craftsmans-guide-to-software-9780134494166
---

Robert C. Martin formula uma regra que já aparecia em outras variantes (hexagonal, onion): as dependências de código apontam para a política de negócio, nunca o contrário. O livro acrescenta princípios de componentes e de fronteiras. Esta ficha fica na regra que verificamos na revisão.

## A regra

Uma regra de negócio é expressável e testável sem subir um servidor, sem a base de dados concreta e sem o framework web. Os adaptadores — HTTP, fila, SQL, interface — traduzem entre o exterior e essa regra. Quando o adaptador muda, a regra não muda.

Isto aplica-se dentro de um contexto delimitado. Não desenha a fronteira entre contextos. Essa decisão é de domínio e de trade-off, não de pastas.

## O que aproveitamos

Na revisão de código de um contexto com lógica própria: o domínio não importa o framework. Um teste da invariante não precisa de infraestrutura. A estrutura de pastas pode variar. A direção das dependências, não.

## O que não fazemos

Não impomos quatro projetos, nem os nomes UseCase, Interactor e Gateway, a serviços sem lógica. Não confundimos esta regra com a decisão de extrair um serviço.
