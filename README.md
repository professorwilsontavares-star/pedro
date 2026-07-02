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
| `hist-mod07-revisao.html` | Revisão em cartões (pontos principais) |
| `hist-mod07-quiz.html` | Quiz interativo (48 questões, embaralha sozinho) |
| `hist-mod07-resumo.html` | Resumo da matéria (linguagem simples + figuras) + gabarito |
| `port-felicidade-clandestina-revisao.html` | Revisão em cartões do conto |
| `port-felicidade-clandestina-quiz.html` | Quiz interativo (20 questões, embaralha) |
| `port-felicidade-clandestina-resumo.html` | Resumo do conto (enredo, personagens, temas) + figuras |

> História Módulo 7 = 2ª Guerra Mundial. Português = conto "Felicidade Clandestina" (Clarice Lispector). Geografia fica para o futuro (prefixo `geo-`). Para obras literárias, o nome do arquivo usa o título da obra em vez de `modNN`.

## PADRÕES obrigatórios de toda página nova
(seguir SEMPRE — foi assim que o Wilsi pediu)

1. **Botão "← Voltar" (voltar ao HUB):** TODA página tem um botão fixo no **topo, centralizado**, que volta pro `index.html` (coral, texto "← Voltar"). Colocar logo depois de `<body>`. Snippet:
   ```html
   <a href="index.html" class="btn-voltar-hub" style="position:fixed;top:12px;left:50%;transform:translateX(-50%);z-index:9999;display:inline-flex;align-items:center;gap:7px;background:#E25E42;color:#fff;text-decoration:none;font-weight:800;font-size:1rem;padding:11px 18px;border-radius:30px;box-shadow:0 4px 14px rgba(0,0,0,.3);font-family:'Segoe UI',system-ui,Arial,sans-serif;">← Voltar</a>
   ```
2. **Nome do arquivo:** `<materia>-mod<NN>-<tipo>.html` — ex.: `hist-mod08-quiz.html`, `geo-mod01-revisao.html`. Prefixo = matéria REAL (história = `hist`, geografia = `geo`).
3. **Registrar no hub:** todo material novo entra como um card no `index.html`, com a **contagem certa** (ex.: "48 perguntas", não deixar número velho).
4. **Autocontido:** CSS e JS inline no próprio `.html` (funciona offline).
5. **Estilo:** simples, linguagem de adolescente, interativo. NÃO é apostila de concurso — foco em lembrar os pontos principais.

### Padrões por tipo de página
- **Quiz:** 3 alternativas; **embaralhar automaticamente** a ordem das perguntas E das alternativas a cada rodada (Fisher-Yates); resposta de cada questão **reforça o conceito** (ex.: "O ataque à base americana de Pearl Harbor…"); incluir **pares de questões parecidas** (mesmo conceito perguntado de 2-3 jeitos) para massificar; botão final "🔀 Embaralhar e refazer".
- **Resumo:** linguagem BEM simples, **tópicos** (listas) no lugar de textão, e **figuras** feitas em SVG na própria página (bandeiras, linha do tempo, ícones) — nada de imagem externa. Evitar símbolos impróprios (ex.: nada de suástica; usar bandeira atual do país).
- **Revisão:** cartões curtos (pergunta → clicar → resposta curta), só os pontos principais.
