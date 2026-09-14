# Laboratório de Reações

Jogo web para aprender **reações orgânicas** — adição, eliminação, substituição e oxirredução — no nível de uma prova difícil de 3º ano do ensino médio.

Tudo cabe em um único arquivo (`index.html`). Não tem servidor, não tem instalação, não tem conta: basta abrir. Depois de carregado uma vez, funciona **offline**, no computador e no celular.

## Como usar em sala

Abra o link, ou baixe o `index.html` e mande para os alunos — o arquivo funciona sozinho, inclusive sem internet. O progresso de cada aluno fica salvo no navegador dele e pode ser exportado em JSON pelo ícone de engrenagem.

## Os seis modos

| Modo | O que o aluno faz |
|---|---|
| **Trilha** | Seis níveis, do básico à integração. Cada um tem teoria, tutorial guiado, prática e um desafio que libera o próximo. |
| **Construtor** | Monta qualquer molécula tocando na tela e vê na hora o nome IUPAC, as fórmulas, a classificação de cada carbono, o Nox, os carbonos quirais e a lista de reações que aquela estrutura pode sofrer. |
| **Molécula aleatória** | O jogo sorteia uma estrutura do nível escolhido e pergunta nome, função, classificação, Nox, testes e isômeros. |
| **Laboratório** | Escolhe reagente e condição e prevê o produto principal — escolhendo entre quatro alternativas ou **desenhando o produto** no construtor. Ao errar, vê a regra que faltou, o mecanismo e o produto se formando passo a passo. |
| **Reação inversa** | Recebe os produtos e descobre o composto de partida — o raciocínio que a prova cobra na ozonólise e na oxidação enérgica. |
| **Identificação** | Recebe um frasco desconhecido e escolhe testes de bancada (água de bromo, Baeyer, Tollens, Fehling, dicromato, sódio, NaOH, bicarbonato, chama) para descobrir o que é com o menor número de testes. |
| **Simulado** | De 10 a 15 questões misturadas, com cronômetro e sem dicas, seguidas de correção comentada e diagnóstico dos pontos fracos. |

Há ainda um **livro de regras** pesquisável com todo o conteúdo, disponível a qualquer momento.

## Conteúdo coberto

**Nomenclatura** — cadeia principal, numeração pelos menores localizadores, prioridade de funções, prefixos em ordem alfabética. Aceita o formato atual (`but-2-eno`) e o antigo (`2-buteno`), além dos nomes comuns.

**Adição** — Markovnikov, anti-Markovnikov (peróxido, só com HBr), hidrogenação, halogenação, hidratação, alcinos consumindo 2 mols, enol e tautomeria, dienos conjugados 1,2 e 1,4, abertura de ciclos tensionados, polimerização.

**Eliminação** — Saytzeff, desidratação a 140 °C e a 170 °C, KOH aquoso contra KOH alcoólico, desalogenação, desidrogenação.

**Substituição** — reatividade 3° > 2° > 1°, contagem de isômeros de monossubstituição, as quatro reações do benzeno e as duas exceções, dirigência orto-para e meta, haletos com nucleófilos, esterificação (com a pegadinha do oxigênio-18), hidrólise e saponificação.

**Oxirredução** — Nox carbono a carbono, combustão balanceada, Baeyer, oxidação enérgica, ozonólise, oxidação de álcoois, bafômetro, Tollens e Fehling, reduções e as reações de dupla classificação.

## Sob o capô

Não usa nenhuma biblioteca. O motor químico é próprio: as moléculas são grafos de átomos com hidrogênios implícitos, desenhados em SVG; o nomeador IUPAC tem rotas separadas para cadeia aberta, ciclo e aromático; as reações são regras declarativas que transformam o grafo; e uma canonicalização por refinamento de cores é o que permite contar isômeros por hidrogênios equivalentes e conferir a molécula que o aluno desenhou.

**Ctrl+Shift+T** abre um painel de autoteste com 76 verificações químicas — útil para conferir que nada quebrou depois de mexer no código.
