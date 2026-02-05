# Público-alvo — Reino OIDC

Este documento define o **público-alvo** do Reino OIDC e serve como diretriz para o planejamento e a entrega de **novas features** no repositório público [reino-oidc-releases](https://github.com/chmulato/reino-oidc-releases).

---

## Quem é o público-alvo?

### Primário

- **Jovens altruistas que almejam ser Desenvolvedoras de Software (feminino)** — Pessoas em formação (ensino médio, técnico, graduação) com vontade de impactar positivamente e construir carreira em desenvolvimento e **segurança da informação**, **identidade** e **autenticação**.
- **Jovens programadoras** — Mulheres em início de carreira ou em formação que queiram atuar em Security, OIDC e OAuth.
- **Estudantes de Security e desenvolvimento** — Quem precisa entender OAuth 2.1 e OpenID Connect (OIDC) de forma acessível e memorável.
- **Educadoras** — Professoras e instrutoras em busca de material didático criativo sobre logins federados (Google, Microsoft, Big Tech).

### Secundário

- **Qualquer pessoa** curiosa sobre como funcionam os logins "Entrar com Google" e "Entrar com Microsoft".
- **Profissionais de TI** em transição para OAuth 2.1/OIDC ou que queiram revisar conceitos com uma abordagem lúdica.

---

## Foco temático

- **Segurança de autenticação** — OIDC e OAuth como base dos logins modernos.
- **Big Tech e identidade** — Google, Microsoft e outros provedores de identidade.
- **Linguagem dual** — Explicações para **leigos** e para **técnicos** no mesmo material.
- **Gamificação e narrativa** — Personagens (Lady OAuth, Lord OIDC, Devia, etc.), histórias em três partes e Academia com flashcards.

Todas as **novas features** devem reforçar esse foco e servir a esse público.

---

## Diretrizes para novas features

Ao propor ou implementar novas funcionalidades no portal público (reino-oidc-releases), priorize:

1. **Acessibilidade** — Conteúdo e interface utilizáveis por pessoas com diferentes necessidades (leitura, navegação, contraste).
2. **Linguagem inclusiva** — Uso de "você", "desenvolvedoras", "estudantes" e evitação de jargão sem explicação quando o texto for para leigos.
3. **Conteúdo dual** — Sempre que possível, oferecer versão "para leigos" e "para técnicas" (como no glossário e na Academia).
4. **Segurança em primeiro lugar** — Exemplos e boas práticas alinhados a OAuth 2.1 e OIDC (PKCE, HTTPS, validação de tokens).
5. **Conexão com o mundo real** — Referências a Google, Microsoft, login único e cenários do dia a dia.
6. **Progressão clara** — Níveis bem definidos (Iniciante → Aventureiro → Mestre) e próximos passos sugeridos.

---

## Sugestões de features futuras

Ideias alinhadas ao público-alvo e ao foco em Security/OIDC:

- **Novos níveis ou categorias na Academia** — Ex.: JWT, SAML, gestão de sessão.
- **Tradução** — Versão em inglês (ou outros idiomas) para ampliar o alcance.
- **Melhorias de acessibilidade** — WCAG, leitores de tela, contraste e navegação por teclado.
- **Relatórios de progresso** — Resumo do que a pessoa já estudou e certificações.
- **Simulador de fluxos** — Visualização interativa do Authorization Code Flow (e variantes).
- **Vídeos ou animações** — Pequenos vídeos dos personagens explicando conceitos.
- **Modo escuro** — Tema dark para estudo noturno.
- **Exportação de certificados** — PDF ou badge ao completar níveis na Academia.

Ao implementar, documente no **CHANGELOG.md** e atualize o **VERSION** conforme o impacto da mudança.

---

## Onde este documento é usado

- **Repositório público:** [chmulato/reino-oidc-releases](https://github.com/chmulato/reino-oidc-releases) — gestão de releases e conteúdo para o público.
- **Workspace de desenvolvimento:** Repositório privado do Reino OIDC — desenvolvimento de conteúdo e features antes de sincronizar para o repo público e para o delivery Cara Core.

Feito com 💜 para jovens altruistas que almejam ser desenvolvedoras e para o mundo da Security.
