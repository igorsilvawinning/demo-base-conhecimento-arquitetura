---
title: Domain-Driven Design Distilled
kind: referencia
order: 10
summary: Linguagem ubíqua, subdomínios e contextos delimitados. O destilado de Vaughn Vernon, usado como disciplina de fronteira e não como catálogo de padrões.
uses: []
sources:
  - label: InformIT, ficha do livro
    href: https://www.informit.com/store/domain-driven-design-distilled-9780134434421
---

*Domain-Driven Design Distilled* é a versão curta, feita pelo Vaughn Vernon, das ideias de Eric Evans. Serve para alinhar negócio e software na fronteira do domínio. Não é um manual de implementação de todos os padrões táticos.

## Ideias que usamos

- **Linguagem ubíqua.** Um termo, um significado, usado no código, no glossário e na conversa com o negócio. Dois significados obrigam a dois contextos.
- **Subdomínio.** Uma zona do problema. Pode ser núcleo (a razão pela qual o produto existe), de suporte ou genérico. O esforço de modelação concentra-se no núcleo.
- **Contexto delimitado.** A fronteira dentro da qual o modelo e a linguagem são consistentes. É a unidade que se integra com outras, não a classe.
- **Mapa de contextos.** A relação entre contextos: quem publica, quem consome, quem está a jusante e sofre a linguagem do outro.
- **Agregado.** O conjunto de objetos que muda numa transação para manter uma invariante. Não é sinónimo de tabela nem de serviço.

Padrões táticos — entidades, value objects, repositórios, eventos de domínio — usam-se dentro do contexto quando simplificam o modelo. Não são uma arquitetura de pastas obrigatória.

## O que aproveitamos

Contextos descobertos pela linguagem e pela mudança, antes de haver repositórios git separados. Glossário no arc42. Dono do facto por contexto. Integração descrita no mapa, com o modo de consistência no ADR.

## O que não fazemos

Não criamos um microserviço por agregado, nem um agregado por tabela. Não exigimos o livro tático completo a uma aplicação CRUD sem invariantes.
