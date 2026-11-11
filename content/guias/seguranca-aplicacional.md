---
title: Segurança aplicacional
kind: guia
order: 5
summary: O OWASP Top 10 diz onde o risco se concentra. O ASVS 5.0 diz o que se consegue verificar. O nível declara-se por aplicação, começando no L1.
uses:
  - owasp-top10
  - asvs
  - adr
sources: []
---

Consciencialização e verificação não são o mesmo documento. O Top 10 serve para falar de risco com quem não vai ler trezentos requisitos. O ASVS serve para dizer, num pull request, se o controlo existe.

## O que se declara

Cada aplicação com utilizadores ou com dados que não são públicos tem um nível ASVS alvo, escrito no arc42 ou num ADR:

- **L1** é o mínimo para entrar em produção. Cerca de um quinto dos requisitos do ASVS 5.0. Primeira linha de defesa contra ataques comuns. Não assumas que um teste de intrusão externo, sem código nem documentação, cobre o nível inteiro.
- **L2** é o alvo das aplicações de negócio normais. A maior parte dos requisitos vive aqui.
- **L3** reserva-se a sistemas em que a falha tem consequência grave e o custo de verificação se aceita. Não é o default para «ficar bem visto».

O nível sobe por risco, não por entusiasmo. Um requisito de nível superior pode ser puxado para a frente se o risco concreto o justificar. Isso também fica escrito.

## Como o Top 10 entra na revisão

A edição de trabalho é a **OWASP Top 10:2025**. Serve para perguntar «onde é que isto nos tem corrido mal?», não para substituir o ASVS.

1. Controlo de acesso partido, ainda em primeiro, e com SSRF incluído nesta categoria.
2. Má configuração de segurança.
3. Falhas na cadeia de fornecimento de software, mais larga do que «dependência antiga».
4. Falhas criptográficas.
5. Injeção.
6. Desenho inseguro.
7. Falhas de autenticação.
8. Falhas de integridade de software ou de dados, num nível mais baixo do que a cadeia de fornecimento.
9. Falhas de registo e de alerta.
10. Mau tratamento de condições excecionais. Categoria nova face a 2021.

Na revisão de uma arquitetura nova, os pontos 1, 3, 6 e 9 são os que o diagrama e os ADRs já deviam conseguir responder. Os outros confirmam-se no ASVS e nos testes.

## Regras de prática

- Autorização no serviço que detém o dado, em cada operação, não só no ecrã.
- Segredos fora do repositório e fora da imagem. Rotação com dono.
- Dependências com origem definida, build reproduzível o suficiente para saber o que corre em produção, e um prazo para vulnerabilidades exploráveis. É o ponto 3 do Top 10 a tornar-se operacional. O detalhe de pipeline está no guia de entrega.
- Erros que o cliente vê não devolvem stack, SQL nem identificadores internos. O caso excepcional tem comportamento definido: falha fechado quando a dúvida é de autorização ou de integridade.
- Registo de segurança é consultável por quem responde ao incidente, sem ser o único sítio onde vive o dado sensível.

## O que não se faz

Não se cola o Top 10 num slide e se chama ao resultado «modelo de ameaças». Um modelo de ameaças nomeia ativos, atores e abusos daquele sistema.

Não se exige L3 a uma aplicação interna sem dados sensíveis para cumprir uma gate uniforme. O esforço deixa de estar onde o risco está.
