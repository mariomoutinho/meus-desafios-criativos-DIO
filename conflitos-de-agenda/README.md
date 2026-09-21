# Conflitos de agenda: exercício de requisitos com IA

Uma agenda pode conter compromissos válidos individualmente e ainda assim ser impossível de cumprir. Este experimento verifica pares de intervalos e informa conflitos, sem alterar a agenda nem enviar mensagens.

## Regra escolhida

- Cada compromisso tem `id`, `titulo`, `inicio` e `fim` com horário e fuso explícitos.
- O início precisa ser anterior ao fim. Identificadores devem ser únicos.
- Dois compromissos entram em conflito se os intervalos se sobrepõem. Um termina exatamente quando o outro começa: sem conflito.
- Se qualquer compromisso estiver inválido, o lote é recusado; não há recomendação parcial.
- Saídas: `CONFLITOS`, `AGENDA_LIVRE`, `SEM_DADOS`, `ENTRADA_INVALIDA`.

## Usar

1. No n8n, importe [`workflow.json`](workflow.json) como arquivo.
2. Abra **Dados de exemplo** e substitua o objeto de demonstração pelos seus dados, mantendo a estrutura de [`exemplo.json`](exemplo.json).
3. Clique em **Executar workflow**. O resultado aparece em **Analisar dados**. A execução é somente manual.

Os dados são fictícios. O fluxo utiliza somente Manual Trigger e Code, sem credenciais ou integrações. A lógica foi verificada localmente pelo script `verificar.js` na raiz destes desafios; a importação e execução em uma instância n8n ainda precisam de confirmação.

## Pergunta que orientou o experimento

Quando duas atividades se encostam no horário, há conflito? Decidi que não: somente a sobreposição real gera aviso. Essa escolha muda o resultado mais do que a aparência do workflow.
