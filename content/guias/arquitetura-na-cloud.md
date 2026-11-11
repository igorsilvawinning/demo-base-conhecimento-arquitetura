---
title: Arquitetura na cloud
kind: guia
order: 4
summary: Uma revisão Well-Architected por carga, com os pilares do fornecedor onde o sistema corre. A adoção segue o CAF. A maturidade cloud native é um chão, não uma pontuação.
uses:
  - azure-waf
  - aws-waf
  - caf
  - cncf
sources: []
---

Há dois fornecedores no vocabulário desta base e um modelo de maturidade que não pertence a nenhum deles. Não se mantêm dois manuais paralelos a repetir «segurança» e «custo». Mantém-se um ritual de revisão e uma regra para escolher a lista de perguntas.

## Que lista usar

O sistema corre sobretudo na Azure: a revisão usa os cinco pilares do Azure Well-Architected Framework. Corre sobretudo na AWS: usa os seis da AWS, incluindo sustentabilidade. Corre nos dois: cada carga é revista com o quadro do sítio onde corre. Um quadro caseiro que mistura os dois perde as perguntas específicas de serviço e fica impossível de manter.

Os nomes parecem-se. As diferenças que importam na revisão:

- A AWS trata sustentabilidade como pilar próprio. Na Azure entra como preocupação dentro dos outros pilares e nas cargas de trabalho, não como sexto pilar com o mesmo peso.
- Excelência operacional, segurança, fiabilidade, eficiência de desempenho e otimização de custo existem nos dois. As perguntas concretas — serviços, limites, identidade, rede — não se copiam de um lado para o outro.

A revisão produz uma lista curta de riscos no arc42 (secção 11) e, quando muda uma escolha estrutural, um ADR. Não produz um certificado.

## Adoção, não só desenho

Para uma organização que ainda está a mover trabalho para a cloud, o Microsoft Cloud Adoption Framework dá a ordem: estratégia, plano, prontidão, adoção, governação, gestão. Well-Architected responde «esta carga está sã?». O CAF responde «a organização está em condições de a operar?». Saltar para a migração de aplicações sem dono, sem landing zone e sem regra de custo é o falhanço típico. O CAF é útil mesmo quando o destino não é só Azure. A parte de prontidão e governação não depende do logótipo.

## Maturidade cloud native

O modelo da CNCF lê-se por produto, em cinco níveis — construir, operar, escalar, melhorar, adaptar — e em cinco dimensões: resultados de negócio, pessoas, política, processo e tecnologia. O nível é um chão. Faltar uma condição do nível 3 mantém o produto no nível anterior, mesmo que o resto pareça avançado. Nível 5 não é obrigatório. Para muitos produtos, operar com controlo chega.

Usa-se este modelo para perceber se a plataforma e as equipas aguentam o que a arquitetura pede (self-service, supply chain, política como código). Não se usa para avaliar pessoas.

## Evidência mínima numa revisão

Identidade e rede desenhadas, não herdadas de uma subscrição antiga. Objetivo de fiabilidade com número. Orçamento ou unidade de custo que alguém olha. Dono operacional. Caminho de restauro ensaiado ao nível que o objetivo de fiabilidade exige. Sem estes cinco, os pilares são uma apresentação.
