# Workspace local — Reino OIDC (releases)

Este documento descreve o **workspace local** do repositório público do Reino OIDC e o fluxo de **delivery de novas features** para o público-alvo.

---

## Repositório público no GitHub

- **URL:** https://github.com/chmulato/reino-oidc-releases  
- **Clone (HTTPS):** `https://github.com/chmulato/reino-oidc-releases.git`  
- **Nome do repositório:** `reino-oidc-releases` (com hífens)

O workspace local pode estar em qualquer pasta (ex.: `D:\dev\reino_oidc_releases`). O que importa é o **remote** apontar para o repo acima.

### Configurar o remote (primeira vez)

Se você clonou ou criou a pasta localmente e ainda não vinculou ao GitHub:

```bash
git remote add origin https://github.com/chmulato/reino-oidc-releases.git
git branch -M main
git push -u origin main
```

Se o remote já existir com outro nome ou URL, ajuste:

```bash
git remote set-url origin https://github.com/chmulato/reino-oidc-releases.git
```

---

## Estrutura do workspace

| Pasta/arquivo | Uso |
|---------------|-----|
| **docs/** | Conteúdo do site estático (HTML, assets, md). Publicado via GitHub Pages (Source: branch `main`, folder `/docs`). |
| **README.md** | Apresentação do projeto, público-alvo e links. |
| **CHANGELOG.md** | Histórico de versões e novas features. |
| **VERSION** | Número da versão atual (ex.: 1.0.0). |
| **LICENSE** | MIT. |
| **WORKSPACE.md** | Este arquivo — workspace local e fluxo de delivery. |
| **PUBLICO_ALVO.md** | Definição do público-alvo e diretrizes para novas features. |

---

## Fluxo de delivery de novas features

1. **Desenvolvimento** — As novas funcionalidades e o conteúdo são criados no repositório **privado** (Reino OIDC / workspace de desenvolvimento, ex.: `reino_oidc`).

2. **Sincronização para este repo** — Quando uma feature está pronta para o público:
   - No workspace de desenvolvimento, rode:  
     `python scripts/sync_to_delivery_oidc.py --releases`  
   - Isso atualiza a pasta `docs/` **deste** workspace local (`reino_oidc_releases`) com os HTML, assets e md mais recentes.
   - Ou copie manualmente o conteúdo de `reino_oidc` para `reino_oidc_releases/docs/`.

3. **Commit e push** — Neste workspace:
   ```bash
   git add docs/ VERSION CHANGELOG.md
   git commit -m "feat: descrição da nova feature"
   git push origin main
   ```
   Atualize **VERSION** e **CHANGELOG.md** conforme o [Semantic Versioning](https://semver.org/) e as boas práticas do projeto.

4. **Delivery Cara Core** — Para atualizar também o site no portfólio da Cara Core:
   - No workspace **reino_oidc**, rode:  
     `python scripts/sync_to_delivery_oidc.py`  
   - Isso atualiza `D:\dev\site\cara-core\delivery\oidc\`. O deploy do site Cara Core é feito pelo fluxo próprio do repositório do site.

5. **GitHub Pages** — Com Pages ativado (Settings → Pages → Source: branch `main`, folder `/docs`), o conteúdo de `docs/` fica em:  
   **https://chmulato.github.io/reino-oidc-releases/**

---

## Público-alvo e novas features

Todas as novas features devem ser pensadas para o **público-alvo** do Reino OIDC. Consulte **PUBLICO_ALVO.md** para:

- Quem é o público (jovens programadoras, foco em Security, OIDC/Google/Microsoft).
- Diretrizes para conteúdo (linguagem dual, acessibilidade, inclusão).
- Sugestões de tipos de features (novos níveis na Academia, acessibilidade, tradução, etc.).

---

## Resumo

| Ação | Onde |
|------|------|
| Desenvolver conteúdo/features | Repositório privado (reino_oidc). |
| Atualizar portal público | Este workspace → push para `reino-oidc-releases`. |
| Atualizar delivery Cara Core | Script `sync_to_delivery_oidc.py` no reino_oidc (sem `--releases` ou com). |
| Publicar no GitHub | Push para `origin main` em **reino-oidc-releases**. |
| Ver o site público | https://chmulato.github.io/reino-oidc-releases/ (após configurar Pages). |
