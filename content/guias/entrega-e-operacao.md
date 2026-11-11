---
title: Entrega e operação
kind: guia
order: 3
summary: Lotes pequenos, feedback que volta a quem pode agir, e quatro métricas DORA lidas em conjunto. A plataforma é um produto interno, não uma fila.
uses:
  - devops-handbook
  - dora
  - team-topologies
  - cncf
sources: []
---

Entrega e operação medem-se pela capacidade de mudar produção com controlo, e de saber que o utilizador ainda está a ser servido. O vocabulário vem das três vias do *DevOps Handbook* e das métricas DORA. Os limiares numéricos mudam de relatório para relatório. Vão-se buscar a [dora.dev](https://dora.dev). Não se gravam no objetivo anual.

## As três vias, em regras

**Fluxo.** O caminho do commit à produção é o mesmo para toda a gente daquele serviço. O lote cabe numa revisão. Há testes automáticos nesse caminho. Sair do caminho é que é excecional, não usá-lo.

**Feedback.** Um teste que falha, falha no commit de quem o provocou. Produção tem telemetria que a equipa dona do serviço olha sem abrir um ticket a outra equipa. Alerta sem dono não conta como feedback.

**Aprendizagem.** Um incidente produz uma alteração no sistema — teste, limite, alerta, runbook — na semana seguinte, ou uma decisão explícita de não a fazer. A conversa procura a condição que tornou o erro fácil, não a pessoa que estava de turno.

## Como se lê a DORA

Por serviço, não por pessoa e não pela média da empresa.

- Frequência de deploy e lead time do commit até produção dizem a velocidade do caminho.
- Taxa de alterações com falha e tempo de restauro dizem o controlo. «Falha» define-se antes do gráfico existir: hotfix, rollback ou correção atribuída àquele deploy.
- As quatro leem-se juntas. Frequência alta com taxa de falha a subir não é melhoria. Taxa de falha baixa com lead time de um mês também não.

Confiabilidade vista pelo utilizador fica ao lado, não no lugar destas quatro. Um serviço pode fazer deploy todos os dias e estar inutilizável.

## Plataforma

Se várias equipas precisam do mesmo caminho — cluster, pipeline, observabilidade, identidade — isso é um produto interno, com utilizadores, documentação e contrato. O modo de trabalho, quando o caminho está maduro, é self-service. Uma equipa central que executa os deploys dos outros recria a fila que estas métricas vão mostrar no lead time.

O nível de maturidade cloud native diz o que falta para esse self-service ser real. Não é uma nota da organização. Um produto pode estar a operar e outro ainda a construir. O guia de cloud trata essa leitura.

## O que não se faz

Não há meta individual de número de deploys. Não há ranking de equipas com domínios diferentes. Não se chama DevOps a uma ferramenta instalada em cima de um lote trimestral.
