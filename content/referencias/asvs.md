---
title: OWASP ASVS
kind: referencia
order: 12
summary: Standard de verificação de segurança aplicacional. A edição de trabalho é a 5.0.0, com três níveis e dezassete capítulos.
uses: []
sources:
  - label: asvs.owasp.org
    href: https://asvs.owasp.org/
  - label: Edição 5.0.0
    href: https://github.com/OWASP/ASVS/tree/v5.0.0
---

O Application Security Verification Standard lista requisitos testáveis para aplicações e serviços web. Não é uma lista de vulnerabilidades célebres. É uma barra que se pode verificar.

A edição de trabalho desta base é a **5.0.0** (maio de 2025). Tem cerca de 350 requisitos em 17 capítulos. Há mapa de ida e volta com a 4.0.3 para quem ainda tem avaliação antiga.

## Níveis

Os níveis são cumulativos na intenção, com requisitos que mudam de exigência à medida que se sobe.

- **L1.** Mínimo e ponto de entrada. Primeira linha contra ataques comuns. Poucos requisitos, de propósito. Não assumir que um teste externo sem código chega para os fechar todos.
- **L2.** Prática normal. Alvo da maior parte das aplicações de negócio.
- **L3.** Alta garantia, onde o dano justifica o custo de verificação.

Uma organização pode puxar um requisito de nível alto para a frente se o risco local o pedir. Isso documenta-se. Não se sobe o nível inteiro por reflexo.

## Capítulos da 5.0

Codificação e sanitização. Validação e lógica de negócio. Frontend web. API e web services. Ficheiros. Autenticação. Sessão. Autorização. Tokens autocontidos. OAuth e OIDC. Criptografia. Comunicação segura. Configuração. Proteção de dados. Código e arquitetura seguros. Registo e erros. WebRTC.

## O que aproveitamos

Um nível alvo por aplicação, declarado por escrito. L1 como condição de produção. L2 como padrão. O Top 10 fica para a conversa de risco. O ASVS fica para o critério de «feito».

## O que não fazemos

Não misturamos requisitos da 4.0.3 com os da 5.0 na mesma avaliação. Não tratamos o standard como pen test.
