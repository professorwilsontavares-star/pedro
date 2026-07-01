# Estudos do Pedro — site

Material escolar do Pedro (13 anos, Ensino Fundamental Anos Finais / 9º ano), publicado como um site simples via **GitHub Pages**.

- **Link (mandar pro Pedro):** https://professorwilsontavares-star.github.io/pedro/
- **Repositório:** `professorwilsontavares-star/pedro` (público — exigência do GitHub Pages no plano gratuito)
- **Branch publicada:** `master` (raiz `/`)

## Como publicar / atualizar
1. Edite os `.html` nesta pasta.
2. `git add -A && git commit -m "..." && git push`
3. Em ~1-2 min o GitHub Pages republica no link acima.

## Conteúdo atual
| Arquivo | O que é |
|---|---|
| `index.html` | **Hub** — página inicial que lista todas as atividades |
| `geo-mod07-revisao.html` | Revisão em cartões (pontos principais) |
| `geo-mod07-quiz.html` | Quiz interativo (20 questões) |
| `geo-mod07-resumo.html` | Resumo da matéria + gabarito comentado |

> ⚠ **PENDENTE (ajustar depois):** a matéria é **HISTÓRIA**, não Geografia (o Wilsi tinha falado errado). Renomear os arquivos `geo-mod07-*` → `hist-mod07-*`, atualizar os links no `index.html` e a pasta `fontes/Geografia` → `fontes/Historia`. Os títulos DENTRO das páginas já dizem "História". Não renomear antes de combinar, pra não quebrar o link já compartilhado.

## PADRÕES obrigatórios de toda página nova

1. **Botão "🏠 Início" (voltar ao HUB):** TODA página de atividade tem que ter um botão fixo no canto superior esquerdo que leva de volta ao `index.html`. É o padrão do projeto. Snippet:
   ```html
   <a href="index.html" class="btn-voltar-hub" style="position:fixed;top:14px;left:14px;z-index:9999;display:inline-flex;align-items:center;gap:6px;background:#1E2B38;color:#fff;text-decoration:none;font-weight:700;font-size:.88rem;padding:9px 15px;border-radius:30px;box-shadow:0 3px 12px rgba(0,0,0,.22);font-family:'Segoe UI',system-ui,Arial,sans-serif;">🏠 Início</a>
   ```
   (Colocar logo depois de `<body>`.)
2. **Nome do arquivo:** `<materia>-mod<NN>-<tipo>.html` — ex.: `geo-mod08-quiz.html`, `hist-mod01-revisao.html`.
3. **Registrar no hub:** todo material novo entra como um card no `index.html`.
4. **Autocontido:** CSS e JS inline no próprio `.html` (funciona offline, sem depender de internet ou de outros arquivos).
5. **Estilo:** simples, linguagem de adolescente, interativo. NÃO é apostila de concurso — foco em lembrar os pontos principais.
