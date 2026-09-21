# Prazos e prioridades: exercício de requisitos com IA

Uma lista de tarefas pode deixar tudo com aparência de urgência. Este experimento separa tarefas abertas atrasadas, próximas e futuras, além das concluídas, sem enviar cobranças ou tomar decisões por ninguém.

## Regra escolhida

- A entrada contém `dataReferencia` em `YYYY-MM-DD` e uma lista de tarefas com `id`, `titulo`, `vencimento` e `concluida` booleano.
- O cálculo usa dias de calendário, inclusive o dia da referência, sem depender do relógio ou do fuso da instância.
- Tarefas abertas vencidas ficam em `atrasadas`; as com vencimento hoje ou em até três dias ficam em `proximas`; depois disso, `futuras`.
- Tarefas concluídas ficam em `concluidas`, mesmo com data passada.
- Se qualquer tarefa ou data for inválida, o lote inteiro é recusado. Identificadores repetidos também invalidam a entrada.
- Saídas: `RESUMO_OK`, `SEM_DADOS`, `ENTRADA_INVALIDA`.

## Usar

1. No n8n, importe [`workflow.json`](workflow.json) como arquivo.
2. Em **Dados de exemplo**, ajuste a data de referência e as tarefas seguindo [`exemplo.json`](exemplo.json).
3. Clique em **Executar workflow** e consulte **Analisar dados**. A execução é somente manual.

Os dados são fictícios. O fluxo usa Manual Trigger e Code, sem credenciais ou integrações. A lógica foi verificada localmente pelo script `verificar.js` na raiz destes desafios; a importação e execução em uma instância n8n ainda precisam de confirmação.

## Pergunta que orientou o experimento

Uma tarefa concluída e vencida deve aparecer como atraso? Decidi que não, porque o objetivo é ajudar a olhar para o que ainda exige ação. A decisão fica explícita para poder ser revista em outros contextos.
