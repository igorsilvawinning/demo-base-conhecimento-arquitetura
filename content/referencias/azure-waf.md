---
title: Azure Well-Architected Framework
kind: referencia
order: 5
summary: Cinco pilares para rever uma carga na Azure. Instrumento de revisão, não um carimbo.
uses: []
sources:
  - label: Azure Well-Architected
    href: https://learn.microsoft.com/azure/well-architected/
---

O Well-Architected da Microsoft é um conjunto de princípios, listas de verificação e trade-offs para cargas que correm na Azure. A unidade de revisão é a carga, não a empresa.

## Pilares

- **Fiabilidade.** O serviço cumpre o compromisso apesar de falhas. Objetivo numérico, degradação definida, restauro ensaiado.
- **Segurança.** Identidade, rede, dados, aplicações. Defesa em profundidade com dono.
- **Otimização de custo.** Alguém vê a unidade de custo e consegue ligá-la a uma decisão de desenho.
- **Excelência operacional.** Deploy, observabilidade, resposta a incidentes, como prática da equipa que muda o sistema.
- **Eficiência de desempenho.** Capacidade para a procura real, com medida, não com o tamanho máximo imaginado.

Sustentabilidade aparece nas orientações da Microsoft como preocupação transversal e em cargas específicas. Não é um sexto pilar com o mesmo estatuto que na AWS. Por isso as duas revisões não se copiam uma da outra.

## O que aproveitamos

Uma passagem por estes pilares quando a carga corre na Azure. Os riscos entram na secção 11 do arc42. Uma escolha que mude o desenho entra num ADR.

## O que não fazemos

Não usamos este quadro para rever uma carga que corre na AWS. Não tratamos a revisão como certificação.
