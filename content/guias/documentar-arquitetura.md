---
title: Documentar a arquitetura
kind: guia
order: 1
summary: Um sistema, um arc42. Diagramas C4 nos níveis certos. Cada decisão que custa reverter fica num ADR no formato de Nygard.
uses:
  - arc42
  - c4
  - adr
sources: []
---

A documentação de arquitetura responde a três perguntas. O que é o sistema e com quem fala. Como está partido e onde corre. Porque é que está assim e não de outra maneira. Três artefactos chegam. Mais do que isso, sem dono, apodrece.

## O que se escreve

Um **arc42** por sistema, no repositório, em Markdown. Não um arc42 por serviço. Um serviço só ganha documento próprio quando a fronteira, os dados ou o ciclo de vida são diferentes do resto.

Dentro desse documento:

- As secções 1, 3, 4, 8, 10 e 11 são obrigatórias assim que o sistema tem utilizadores. Objetivos de qualidade, contexto, estratégia, conceitos transversais, cenários de qualidade e riscos.
- As secções 5, 6 e 7 (blocos, runtime, deployment) existem para as partes que já têm forma. Uma secção vazia fica vazia, com uma frase a dizer porquê.
- A secção 9 não repete o texto das decisões. É o índice dos ADRs.
- A secção 12, o glossário, usa os mesmos termos do domínio. Se o guia de fronteiras ainda não fixou a linguagem, não se inventa um segundo vocabulário aqui.

**Diagramas C4**, não «um diagrama de arquitetura».

- Um C1 (contexto) por produto. Pessoas, o sistema, vizinhos. Sem tecnologia.
- Um C2 (contentores) por sistema, atualizado no mesmo pull request que muda a topologia. Cada caixa tem uma responsabilidade. Cada seta diz o que passa e com que protocolo.
- Um C3 (componentes) só do contentor que está a ser discutido.
- Código fica no código. Um diagrama de classes mantido à mão mente em semanas.

**Um ADR por decisão** que leve mais de um dia a reverter, no formato de Michael Nygard: título, estado, contexto, decisão, consequências. Numeração monótona em `docs/adr`. Estado `proposto` enquanto se discute, `aceite` quando o pull request entra, `substituído` quando outra decisão o ultrapassa. O antigo não se apaga. Aponta para o novo.

## O que conta como feito

Um colega que não participou na discussão consegue, em menos de uma hora, dizer qual é o âmbito, quais são os dois objetivos de qualidade que ganham numa troca, e qual foi a última decisão estrutural. Se precisa de uma reunião para isso, o documento não existe. Existe um ficheiro.

## O que não se faz

Não se preenche o arc42 no fim, para uma gate. Nessa altura o contexto já foi reescrito para justificar o que ficou feito.

Não se desenha o C2 com classes dentro das caixas, nem o C1 com nomes de produtos cloud. Cada nível tem uma audiência. O diretor de produto lê o C1. Quem vai operar lê o C2.

Não se abre um ADR para o nome de uma pasta, nem se esconde uma mudança de base de dados numa frase do README.
