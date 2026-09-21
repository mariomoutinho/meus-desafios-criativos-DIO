# Exercitando requisitos com IA: o que realmente está atrasado?

Neste exercício, parti de uma lista de tarefas com prazos diferentes. A ideia era destacar o que pede atenção agora, mas logo apareceu uma dúvida: uma tarefa já concluída, mesmo com a data no passado, deve contar como atraso?

Decidi separar as tarefas concluídas das pendentes. Também defini o que significa “próximo”: vence hoje ou nos três dias seguintes. Com essas escolhas, orientei a IA a montar um workflow no n8n que organiza a lista sem fingir que toda tarefa é igualmente urgente.

No exemplo fictício, o resultado mostra uma tarefa atrasada, uma próxima do prazo, uma futura e uma concluída. Se os dados estiverem incoerentes, o fluxo sinaliza o problema em vez de produzir uma lista parcial.

Para mim, o aprendizado está em formular os critérios antes de pedir à IA que construa a automação. O workflow e o JSON estão aqui:
https://github.com/mariomoutinho/meus-desafios-criativos-DIO/tree/main/prazos-e-prioridades

Como vocês definiriam o que merece atenção primeiro?
