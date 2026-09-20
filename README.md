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

**No ar hoje (Regência de Português e Biologia, Módulos 7, 9 e 10):**

| Arquivo | O que é |
|---|---|
| `index.html` | **Hub** — página inicial que lista as atividades |
| `bio-mod07-revisao.html` | Revisão em cartões (47 cartões) |
| `bio-mod07-quiz.html` | Quiz interativo (65 questões, embaralha sozinho) |
| `bio-mod07-resumo.html` | Resumo + figuras SVG + **respostas de todos os exercícios** do módulo |
| `bio-mod09-resumo.html` | Resumo de **Doenças genéticas** (Módulo 9) com figuras SVG e **respostas de todos os exercícios** |
| `bio-mod09-revisao.html` | Revisão em cartões (56 cartões) |
| `bio-mod09-quiz.html` | Quiz interativo (63 questões, embaralha sozinho) |
| `bio-mod10-resumo.html` | Resumo de **Evolução é transformação** (Módulo 10) com figuras SVG e **respostas de todos os exercícios** |
| `bio-mod10-revisao.html` | Revisão em cartões (46 cartões) |
| `bio-mod10-quiz.html` | Quiz interativo (47 questões, embaralha sozinho) |
| `port-regencia-resumo.html` | Resumo de **Regência verbal e nominal** com esquemas em SVG, tópicos, treino rápido e a **lista do caderno** (os 23 nomes que o professor passou, um a um, com dois exemplos cada) |
| `port-regencia-revisao.html` | Revisão em cartões (50 cartões: a matéria e os 23 nomes da lista do caderno) |
| `port-regencia-quiz.html` | Quiz interativo (68 questões, embaralha sozinho) |

**Ocultos no hub** (ficam dentro do comentário `OCULTO_ARQUIVO` no `index.html`; para reexibir, apague a linha do marcador de abertura e a `FIM_OCULTO_ARQUIVO`):
`port-estrangeirismos-trabalho` (trabalho de 20/08, já entregue: saiu do hub em 20/09, o arquivo continua aqui), `geo-mod04-*`, `geo-mod05-*` (Europa: economia e setor primário), `quim-distribuicao-*` e `quim-vanadio-instagram` (Química), `port-felicidade-clandestina-*` e `port-argumentacao-*` (Português), `hist-mod06-*` e `hist-mod07-*` (História).

> Fonte do módulo de Biologia: **Caderno 4 de Ciências** (Marmo, Velloso e Usberco), Setor A, Módulo 7, páginas 364 a 381. Prints em `C:\Projetos\Pedro\fontes\Biologia\`.
>
> Prefixos por matéria: `bio-` (Biologia), `fis-` (Física), `quim-` (Química), `hist-` (História), `geo-` (Geografia), `port-` (Português). Para obras literárias, o nome do arquivo usa o título da obra em vez de `modNN`.

> **Revisão em cartões:** desde 20/09/2026 a resposta aparece **junto com a pergunta**, sem clicar. O botão "Ver resposta" fica oculto e a regra `.resposta.mostrar` não tem animação (animação em aba de fundo deixava a resposta invisível). Vale para as páginas novas também.

## PADRÕES obrigatórios de toda página nova
(seguir SEMPRE — foi assim que a coordenação pediu)

1. **Botão "← Voltar" (voltar ao HUB):** TODA página tem um botão fixo no **topo, centralizado**, que volta pro `index.html` (coral, texto "← Voltar"). Colocar logo depois de `<body>`. Snippet:
   ```html
   <a href="index.html" class="btn-voltar-hub" style="position:fixed;top:12px;left:50%;transform:translateX(-50%);z-index:9999;display:inline-flex;align-items:center;gap:7px;background:#E25E42;color:#fff;text-decoration:none;font-weight:800;font-size:1rem;padding:11px 18px;border-radius:30px;box-shadow:0 4px 14px rgba(0,0,0,.3);font-family:'Segoe UI',system-ui,Arial,sans-serif;">← Voltar</a>
   ```
2. **Nome do arquivo:** `<materia>-mod<NN>-<tipo>.html` — ex.: `hist-mod08-quiz.html`, `geo-mod01-revisao.html`. Prefixo = matéria REAL (história = `hist`, geografia = `geo`).
3. **Registrar no hub:** todo material novo entra como um card no `index.html`, com a **contagem certa** (ex.: "48 perguntas", não deixar número velho). O **nome da disciplina** (a `.tag`, ex.: "PORTUGUÊS · ...") fica sempre em **destaque grande** no topo de cada bloco.
4. **Autocontido:** CSS e JS inline no próprio `.html` (funciona offline).
5. **Estilo:** simples, linguagem de adolescente, interativo. NÃO é apostila de concurso — foco em lembrar os pontos principais.

6. **Cor da matéria:** cada disciplina tem a sua, usada no header, nos títulos de seção e nos botões.

| Matéria | Cor | Claro |
|---|---|---|
| Biologia | `#0f766e` (teal) | `#d5f2ee` |
| Geografia | `#4d7c0f` (verde-oliva) | `#eef6e6` |
| Português | `#6c3fa3` (roxo) | `#f0e9f8` |

### Padrões por tipo de página
- **Quiz:** 3 alternativas; **embaralhar automaticamente** a ordem das perguntas E das alternativas a cada rodada (Fisher-Yates); resposta de cada questão **reforça o conceito** (ex.: "O ataque à base americana de Pearl Harbor…"); incluir **pares de questões parecidas** (mesmo conceito perguntado de 2-3 jeitos) para massificar; botão final "🔀 Embaralhar e refazer".
- **Resumo:** linguagem BEM simples, **tópicos** (listas) no lugar de textão, e **figuras** feitas em SVG na própria página (bandeiras, linha do tempo, ícones) — nada de imagem externa. Evitar símbolos impróprios (ex.: nada de suástica; usar bandeira atual do país).
- **Revisão:** cartões curtos (pergunta → clicar → resposta curta), só os pontos principais.
- **Trabalho a entregar:** ⚠ **não é material de estudo.** É o **texto redigido**, na ordem em que vai ser copiado à mão, com capa, desenvolvimento e conclusão. Sem quiz, sem cartões, sem caixas de curiosidade, sem seção "como montar". Levar CSS de impressão (`@media print`) e botão Imprimir, porque o aluno copia com a folha do lado.

## Como TESTAR antes de publicar
⚠ Abrir por `file://` no preview **não funciona**: vira snapshot estático e o JavaScript não roda, então quiz e cartões não podem ser testados.

Use a entrada **`pedro-site`** do `C:\Projetos\github\.claude\launch.json`, que sobe um `python -m http.server` na porta **8795** servindo esta pasta. Depois do push, o Pages leva **1 a 2 minutos** para propagar: confirme com cache-buster antes de dizer que está no ar.

## Como OCULTAR uma matéria do hub
As matérias que não devem aparecer ficam dentro de **um único comentário HTML** no `index.html`, entre os marcadores `OCULTO_ARQUIVO` e `FIM_OCULTO_ARQUIVO`. Para reexibir tudo, apague essas duas linhas.

⚠ Não pode existir `-->` dentro desse bloco, senão o comentário fecha antes da hora e metade do conteúdo escondido reaparece.
