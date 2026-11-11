---
title: OWASP Top 10
kind: referencia
order: 13
summary: As dez categorias de risco aplicacional da edição 2025. Mapa de atenção, não lista de verificação.
uses: []
sources:
  - label: OWASP Top 10
    href: https://owasp.org/projects/top-ten
  - label: Edição 2025
    href: https://owasp.org/Top10/2025/
---

O Top 10 ordena categorias de risco com base em dados de testes e numa consulta à comunidade. Muda de edição. A edição corrente, e a desta base, é a **2025**. A de 2021 continua útil para ler histórico. Não se usa como lista de trabalho.

## 2025

1. **Controlo de acesso partido.** Continua em primeiro. SSRF passou para dentro desta categoria.
2. **Má configuração de segurança.** Subiu. Mais comportamento da aplicação vive em configuração.
3. **Falhas na cadeia de fornecimento de software.** Alarga o antigo «componentes vulneráveis e desatualizados» a dependências, builds e distribuição. Poucos achados nos dados, impacto alto, e a comunidade pô-la no topo das preocupações.
4. **Falhas criptográficas.**
5. **Injeção.** Inclui desde XSS até injeção de SQL. Frequência e impacto não se distribuem por igual lá dentro.
6. **Desenho inseguro.** Falha de desenho, anterior ao bug de implementação.
7. **Falhas de autenticação.** O nome perdeu «identificação» face a 2021. O foco são os CWEs de autenticação.
8. **Falhas de integridade de software ou de dados.** Confiança em código, artefactos ou dados sem verificar a fronteira. É mais local do que a categoria da cadeia de fornecimento.
9. **Falhas de registo e de alerta.** Sem rasto útil, o incidente descobre-se tarde.
10. **Mau tratamento de condições excecionais.** Categoria nova. Falhar de forma insegura, estados a meio, erros que abrem um caminho.

## O que aproveitamos

Na conversa de arquitetura: acesso, configuração, cadeia de fornecimento, desenho e registo têm de ter resposta concreta. O critério verificável é o ASVS, não esta lista.

## O que não fazemos

Não colamos os dez títulos num slide e chamamos ao resultado um modelo de ameaças. Não ignoramos a edição nova só porque a de 2021 já estava na apresentação antiga.
