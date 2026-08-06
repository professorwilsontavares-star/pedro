# Estudos do Pedro — site

Material escolar do Pedro (14 anos, Ensino Fundamental Anos Finais / 9º ano), publicado como um site simples via **GitHub Pages**.

- **Link (mandar pro Pedro):** https://professorwilsontavares-star.github.io/pedro/
- **Repositório:** `professorwilsontavares-star/pedro` (público — exigência do GitHub Pages no plano gratuito)
- **Branch publicada:** `master` (raiz `/`)

## Como publicar / atualizar
1. Edite os `.html` nesta pasta.
2. `git add -A && git commit -m "..." && git push`
3. Em ~1-2 min o GitHub Pages republica no link acima.

## Conteúdo atual

**No ar hoje (só Biologia):**

| Arquivo | O que é |
|---|---|
| `index.html` | **Hub** — página inicial que lista as atividades |
| `bio-mod07-revisao.html` | Revisão em cartões (47 cartões) |
| `bio-mod07-quiz.html` | Quiz interativo (65 questões, embaralha sozinho) |
| `bio-mod07-resumo.html` | Resumo + figuras SVG + **respostas de todos os exercícios** do módulo |
| `port-estrangeirismos-trabalho.html` | **Trabalho de Português** sobre estrangeirismos (entrega 20/08). Não é material de estudo: é o texto redigido para o Pedro copiar à mão, com capa, 10 tópicos com 5 exemplos cada e conclusão. Tem CSS de impressão. |

**Ocultos no hub** (ficam dentro do comentário `OCULTO_ARQUIVO` no `index.html`; para reexibir, apague a linha do marcador de abertura e a `FIM_OCULTO_ARQUIVO`):
`geo-mod04-*`, `geo-mod05-*` (Europa: economia e setor primário), `quim-distribuicao-*` e `quim-vanadio-instagram` (Química), `port-felicidade-clandestina-*` e `port-argumentacao-*` (Português), `hist-mod06-*` e `hist-mod07-*` (História).

> Fonte do módulo de Biologia: **Caderno 4 de Ciências** (Marmo, Velloso e Usberco), Setor A, Módulo 7, páginas 364 a 381. Prints em `C:\Projetos\Pedro\fontes\Biologia\`.
>
> Prefixos por matéria: `bio-` (Biologia), `fis-` (Física), `quim-` (Química), `hist-` (História), `geo-` (Geografia), `port-` (Português). Para obras literárias, o nome do arquivo usa o título da obra em vez de `modNN`.

## PADRÕES obrigatórios de toda página nova
(seguir SEMPRE — foi assim que o Wilsi pediu)

1. **Botão "← Voltar" (voltar ao HUB):** TODA página tem um botão fixo no **topo, centralizado**, que volta pro `index.html` (coral, texto "← Voltar"). Colocar logo depois de `<body>`. Snippet:
   ```html
   <a href="index.html" class="btn-voltar-hub" style="position:fixed;top:12px;left:50%;transform:translateX(-50%);z-index:9999;display:inline-flex;align-items:center;gap:7px;background:#E25E42;color:#fff;text-decoration:none;font-weight:800;font-size:1rem;padding:11px 18px;border-radius:30px;box-shadow:0 4px 14px rgba(0,0,0,.3);font-family:'Segoe UI',system-ui,Arial,sans-serif;">← Voltar</a>
   ```
2. **Nome do arquivo:** `<materia>-mod<NN>-<tipo>.html` — ex.: `hist-mod08-quiz.html`, `geo-mod01-revisao.html`. Prefixo = matéria REAL (história = `hist`, geografia = `geo`).
3. **Registrar no hub:** todo material novo entra como um card no `index.html`, com a **contagem certa** (ex.: "48 perguntas", não deixar número velho). O **nome da disciplina** (a `.tag`, ex.: "PORTUGUÊS · ...") fica sempre em **destaque grande** no topo de cada bloco.
4. **Autocontido:** CSS e JS inline no próprio `.html` (funciona offline).
5. **Estilo:** simples, linguagem de adolescente, interativo. NÃO é apostila de concurso — foco em lembrar os pontos principais.

### Padrões por tipo de página
- **Quiz:** 3 alternativas; **embaralhar automaticamente** a ordem das perguntas E das alternativas a cada rodada (Fisher-Yates); resposta de cada questão **reforça o conceito** (ex.: "O ataque à base americana de Pearl Harbor…"); incluir **pares de questões parecidas** (mesmo conceito perguntado de 2-3 jeitos) para massificar; botão final "🔀 Embaralhar e refazer".
- **Resumo:** linguagem BEM simples, **tópicos** (listas) no lugar de textão, e **figuras** feitas em SVG na própria página (bandeiras, linha do tempo, ícones) — nada de imagem externa. Evitar símbolos impróprios (ex.: nada de suástica; usar bandeira atual do país).
- **Revisão:** cartões curtos (pergunta → clicar → resposta curta), só os pontos principais.
