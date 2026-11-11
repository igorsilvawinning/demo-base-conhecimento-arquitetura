---
title: Microsoft Cloud Adoption Framework
kind: referencia
order: 14
summary: Ordem para uma organização adotar cloud — estratégia, plano, prontidão, adoção, governação e gestão. Complementa o Well-Architected, não o repete.
uses: []
sources:
  - label: Cloud Adoption Framework
    href: https://learn.microsoft.com/azure/cloud-adoption-framework/
---

O Cloud Adoption Framework descreve como uma organização se prepara e governa a adoção de cloud. Nasceu para a Azure. A parte de estratégia, prontidão e governação lê-se mesmo quando há mais do que um fornecedor. A parte de landing zone e controlos técnicos, essa, é específica da Azure e não se finge o contrário.

## Metodologias

- **Estratégia.** Motivos, resultados de negócio, alinhamento. Sem isto a migração é um projeto de infraestrutura.
- **Plano.** Inventário, racionalização (manter, rehost, refactor, rebuild, replace), backlog.
- **Prontidão.** Landing zone, identidade, rede, subscrições, capacidades da equipa.
- **Adoção.** Migrar e inovar, por ondas, com dono de cada carga.
- **Governação.** Política, custo, segurança, consistência, com exceção tratada como exceção.
- **Gestão.** Operação, monitorização, backup, o dia dois.

Há orientações adicionais, entre elas segurança, que se cruzam com estas seis. Não substituem a ordem.

## O que aproveitamos

A distinção entre «a carga está bem desenhada?» (Well-Architected) e «a organização consegue operá-la?» (CAF). Não se migra uma carteira de aplicações para cima de uma subscrição sem dono, sem regra de custo e sem identidade pensada.

## O que não fazemos

Não usamos o CAF como checklist de pilares de uma única API. Não o impomos como padrão de landing zone AWS.
