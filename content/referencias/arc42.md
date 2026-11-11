---
title: Arc42
kind: referencia
order: 1
summary: Template aberto de documentação de arquitetura em doze secções. Esqueleto, não um método de desenho.
uses: []
sources:
  - label: arc42.org
    href: https://arc42.org
  - label: Documentação do template
    href: https://docs.arc42.org
---

O arc42 organiza a descrição de um sistema de software para alguém que não esteve na sala. Não escolhe a arquitetura. Dá sítios estáveis às respostas.

## As doze secções

1. Introdução e objetivos, incluindo requisitos de qualidade e stakeholders.
2. Restrições que a equipa não pode remover.
3. Contexto e âmbito, o sistema como caixa negra.
4. Estratégia de solução, as decisões que condicionam o resto.
5. Vista de blocos, a decomposição estática.
6. Vista de runtime, os cenários que importam.
7. Vista de deployment.
8. Conceitos transversais, o que se repetiria em cada bloco.
9. Decisões de arquitetura.
10. Requisitos de qualidade em cenário, não em adjetivo.
11. Riscos e dívida técnica.
12. Glossário.

## O que aproveitamos

Um documento por sistema. Prioridade às secções 1, 3, 4, 10 e 11. Diagramas no modelo C4 onde a secção pede uma vista. A secção 9 reduzida a um índice de ADRs. Glossário alinhado com a linguagem do domínio.

## O que não fazemos

Não tratamos as doze secções como formulário de compliance. Não duplicamos o template por microserviço. Não deixamos o documento numa ferramenta que o código não encontra.
