# Exercitando requisitos com IA: uma agenda cheia pode esconder conflitos

Desta vez, propus uma situação comum: duas atividades parecem caber na agenda, mas acontecem ao mesmo tempo. Como uma automação poderia avisar isso sem criar alarmes desnecessários?

Antes de construir o fluxo, precisei decidir algo simples e importante: se uma reunião termina exatamente quando outra começa, isso é um conflito? Neste experimento, considerei que não. Também defini que uma data incoerente deve interromper a análise, porque um aviso baseado numa agenda incompleta pode enganar.

Usei a IA para transformar essas escolhas em um workflow no n8n e verificar exemplos diferentes. Com três compromissos fictícios, ele encontrou uma sobreposição de 30 minutos. O mais interessante foi perceber que a utilidade do resultado depende das perguntas feitas antes de criar os nodes.

O projeto e o JSON para importar estão aqui:
https://github.com/mariomoutinho/meus-desafios-criativos-DIO/tree/main/conflitos-de-agenda

Para vocês, compromissos que apenas se encostam no horário deveriam gerar aviso?
