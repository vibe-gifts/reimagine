# reimagine

**Português** · [English](README.en.md) · [Español](README.es.md)

**Uma skill que faz a IA redesenhar o processo a partir do objetivo, em vez de remendar os passos.**

Remendar passos rende 10%. Reimaginar rende 10 vezes mais, porque muda a estrutura que obriga aqueles passos a existir.

Você diz o resultado que quer, de preferência um objetivo absurdo ("quero esse vídeo pronto em 5 minutos, não em 2 horas"). A IA lê os seus arquivos e o histórico, acha de onde vem o vai e volta e devolve um sistema novo. Ela não muda nada antes do seu OK.

## Por que um objetivo absurdo funciona

"20 minutos" convida a IA a ajustar o que já existe. "5 minutos" a obriga a apagar, juntar e reordenar. A meta absurda é uma ferramenta: ela proíbe o remendo. Se a meta for impossível de verdade, a skill diz isso com honestidade e mostra quanto dá para chegar, e por qual caminho.

Peça o **resultado**, não as etapas. Quem descreve etapas descreve o sistema que já tem, e a IA só vai rearrumar esse sistema.

## O que ela faz

1. **Fixa o objetivo e a meta** numa linha. Se você não der meta, ela cria uma e avisa: tempo dividido por 10, uma rodada de correção, no máximo 2 paradas suas.
2. **Mede a realidade antes de opinar.** Lê os arquivos, o histórico do Git, as conversas antigas e as versões velhas, e conta: quantas rodadas, quanto foi refeito, onde está o tempo. O achado mais comum é "está escrito, mas nada confere".
3. **Acha as causas de estrutura.** Regra que nasce só na revisão, fontes que se contradizem, o caro antes do barato, uma peça fazendo 4 trabalhos, trava em cima de trava, a mesma coisa feita duas vezes, tudo feito do zero a cada vez.
4. **Corta na ordem certa.** Questiona cada exigência (e descobre por que ela existe antes de cortar), apaga, simplifica, põe o barato antes do caro e só então automatiza.
5. **Desenha o sistema novo:** uma frase-tese, uma fonte única de verdade, uma tarefa por peça, peças aprovadas no lugar de trabalho novo, cada reprovação virando uma conferência automática, a lista do que sai e uma meta medível.
6. **Faz um pré-mortem:** as 3 formas mais prováveis de o desenho novo falhar.
7. **Entrega e espera:** a estrutura em tabela, árvore ou esboço, o que não foi verificado e uma única decisão para você.

Serve para processo e esteira de produção, tela e painel, bot ou agente de IA, e estrutura de pastas. Não serve para consertar um defeito conhecido nem para ajuste pequeno de texto.

## Instalação

**Claude Code:** na caixa de mensagem, digite:

```
/plugin marketplace add vibe-gifts/reimagine
/plugin install reimagine@reimagine
```

No app do Claude (aba Code), clique no **+** ao lado da caixa de mensagem, depois em **Plugins** e **Adicionar marketplace**. Digite `vibe-gifts/reimagine` e clique em **Adicionar plugin**.

**Codex ou outro agente:** baixe este repositório (botão **Code** → **Download ZIP**), descompacte e aponte o agente para a pasta `skills/reimagine`.

Depois, é só pedir:

> reimagine como a gente publica os posts do blog. Hoje leva 3 dias e vai e volta demais. Objetivo: post no ar em 1 hora, aprovado de primeira.

## Bom saber

- **As instruções estão em inglês**, mas ela responde na sua língua.
- **Ela só propõe.** Nada no seu projeto muda antes do seu OK.
- A pasta `skills/reimagine/evals` tem 3 casos de teste no formato do `claude plugin eval`.

## Licença

MIT
