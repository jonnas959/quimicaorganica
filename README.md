# Laboratório de Reações

Jogo web para aprender **reações orgânicas** — adição, eliminação, substituição e oxirredução — no nível de uma prova difícil de 3º ano do ensino médio.

Tudo cabe em um único arquivo (`index.html`). Não tem servidor, não tem instalação, não tem conta: basta abrir. Depois de carregado uma vez, funciona **offline**, no computador e no celular.

O conteúdo segue os **capítulos 19 a 23** do material de aula.

## Como usar em sala

Abra o link, ou baixe o `index.html` e mande para os alunos — o arquivo funciona sozinho, inclusive sem internet. O progresso de cada aluno fica salvo no navegador dele e pode ser exportado em JSON pelo ícone de engrenagem.

## A trilha

| Nível | Conteúdo |
|---|---|
| **Fundamentos** | Reconhecer funções, classificar álcool/haleto/amina em 1°, 2° e 3°, carbonos α e β, nomenclatura IUPAC, Nox, carbono quiral |
| **Cap. 19 — Adição** | Markovnikov, efeito Kharasch (peróxido), Sabatier-Senderens, adição cis, ordens de reatividade, alcinos, enol e tautomeria, dienos 1,2 e 1,4, HCN, polimerização |
| **Cap. 20 — Substituição em alcanos** | Mecanismo radicalar, reatividade 3° > 2° > 1°, contagem de isômeros, nitração, sulfonação, haletos e nucleófilos, teoria das tensões de Baeyer |
| **Cap. 21 — Aromáticos** | Halogenação, nitração, sulfonação, Friedel-Crafts, dirigência orto-para e meta, ativantes e desativantes, exceções do benzeno, tolueno no anel ou na cadeia lateral |
| **Cap. 22 — Oxirredução** | Ozonólise, oxidação branda (Baeyer), oxidação enérgica, ciclanos e aromáticos, oxidação de álcoois, bafômetro, Tollens e Fehling, combustão, reduções |
| **Cap. 23 — Eliminação e ésteres** | Regra de Zaitsev, carbonos α e β, 140 °C e 170 °C, desidro-halogenação, esterificação e a pegadinha do O-18, hidrólise |
| **Sabões e integração** | Saponificação, sabão duro e mole, tensoativos, micelas, água dura, detergentes, biodiesel por transesterificação, sequências de reações |

Cada nível tem teoria, tutorial guiado passo a passo, prática com dicas e um desafio que libera o próximo.

## Os modos

**Treinar** reúne os treinos livres:

- **Funções** — reconhecer a função, classificar em 1°/2°/3°, achar o grupo tocando na estrutura, os pares que mais se confundem (aldeído com cetona, ácido com éster, álcool com éter, amina com amida), a associação grupo ↔ função e uma tabela com as 17 funções desenhadas
- **Nomenclatura e leitura** — molécula sorteada, com perguntas de nome IUPAC, função, classificação, Nox, testes e isômeros
- **Laboratório de reações** — escolher reagente e condição e prever o produto principal, marcando a alternativa ou **desenhando o produto** no construtor
- **Reação inversa** — dos produtos de volta ao reagente
- **Identificação de frasco** — nove testes de bancada para descobrir um líquido desconhecido

**Construtor** monta qualquer molécula por toque e devolve, em tempo real, nome IUPAC, fórmulas, classificação de cada carbono, Nox, carbonos quirais e a lista de reações que aquela estrutura pode sofrer.

**Simulado** aplica de 10 a 15 questões misturadas, com cronômetro e sem dicas, seguidas de correção comentada e diagnóstico dos pontos fracos.

**Livro de regras** é a referência pesquisável, disponível a qualquer momento.

## Sob o capô

Não usa nenhuma biblioteca. O motor químico é próprio: as moléculas são grafos de átomos com hidrogênios implícitos, desenhados em SVG; o nomeador IUPAC tem rotas separadas para cadeia aberta, ciclo e aromático; as 44 reações são regras declarativas que transformam o grafo; e uma canonicalização por refinamento de cores é o que permite contar isômeros por hidrogênios equivalentes e conferir a molécula que o aluno desenhou.

**Ctrl+Shift+T** abre um painel de autoteste com 95 verificações químicas — útil para conferir que nada quebrou depois de mexer no código.
