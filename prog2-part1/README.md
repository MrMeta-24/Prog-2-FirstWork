# prog2-att

To install dependencies:

```bash
bun install
```

To run:

```bash
bun run index.ts
```

This project was created using `bun init` in bun v1.3.11. [Bun](https://bun.com) is a fast all-in-one JavaScript runtime.

SISTEMA DE LISTA DE TAREFAS (TODO CLI)

Este sistema permite gerenciar tarefas via terminal utilizando comandos simples.
As tarefas possuem texto, prioridade e data opcional.

COMANDOS DISPONÍVEIS

1. Adicionar tarefa

Formato:
bun cli.ts add "texto" prioridade data

Exemplos:
bun cli.ts add "Estudar JavaScript" high 2026-04-10
bun cli.ts add "Comprar pão" low
bun cli.ts add "Treinar"

Observações:
- O texto é obrigatório
- A prioridade é opcional (padrão: low)
- A data é opcional

----------------------------------------

2. Listar tarefas

Formato:
bun cli.ts list

Descrição:
Exibe todas as tarefas com:
- índice
- status (concluído ou não)
- prioridade
- informação de data (se existir)

----------------------------------------

3. Atualizar tarefa

Formato:
bun cli.ts update indice "novo texto"

Exemplo:
bun cli.ts update 0 "Estudar TypeScript"

----------------------------------------

4. Remover tarefa

Formato:
bun cli.ts remove indice

Exemplo:
bun cli.ts remove 0

----------------------------------------
REGRAS IMPORTANTES
----------------------------------------

1. Texto com espaços deve estar entre aspas

Correto:
bun cli.ts add "Estudar JS"

Incorreto:
bun cli.ts add Estudar JS

----------------------------------------

2. Ordem obrigatória dos parâmetros no comando add

texto -> prioridade -> data

----------------------------------------

3. Prioridades válidas

Baixa
Medio
FAZ LOGO SEU PUTO

obs exatamente como ta escrito até com as letras maiuscolas

----------------------------------------

4. Formato da data

YYYY-MM-DD

Exemplo:
2026-04-10

----------------------------------------

OBSERVAÇÕES TÉCNICAS

- As tarefas são armazenadas em arquivo JSON
- A lista é carregada em memória e salva após modificações
- A data é opcional e representa a data limite da tarefa
- A prioridade possui valor padrão "low" quando não informada

