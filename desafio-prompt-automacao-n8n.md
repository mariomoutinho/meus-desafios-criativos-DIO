# Desafio Criativo DIO — Automação com n8n para Lembretes e Acompanhamento de Pacientes

## 📌 Contexto

Este projeto foi desenvolvido como parte de um desafio criativo da DIO, com foco na construção de um prompt completo para orientar a criação de uma automação no n8n.

A proposta é apoiar diferentes profissionais da saúde e terapeutas no envio de lembretes de consultas e no acompanhamento pós-atendimento dos pacientes.

## 🎯 Objetivo da automação

Criar uma automação no n8n capaz de:

- identificar consultas agendadas;
- enviar lembretes aos pacientes no dia anterior;
- enviar um novo lembrete próximo ao horário da consulta;
- verificar se o atendimento foi realizado;
- iniciar um fluxo de acompanhamento pós-sessão;
- lembrar o terapeuta de entrar em contato com o paciente;
- registrar confirmações, cancelamentos, reagendamentos e acompanhamentos.

## 👥 Público

A solução foi pensada para diferentes profissionais da saúde e terapeutas, como:

- fisioterapeutas;
- psicólogos;
- acupunturistas;
- psiquiatras;
- terapeutas integrativos;
- outros profissionais que realizem atendimentos periódicos.

## 🛠️ Ferramentas envolvidas

- n8n;
- Google Calendar ou outro sistema de agenda;
- Google Sheets, Airtable ou banco de dados;
- WhatsApp Business API, e-mail ou SMS;
- Telegram, WhatsApp ou e-mail para notificações aos profissionais;
- Webhooks;
- APIs externas.

## 🔄 Fluxo desejado

1. Consultar periodicamente a agenda dos terapeutas.
2. Identificar consultas agendadas para o dia seguinte.
3. Enviar automaticamente ao paciente uma mensagem com data e horário da consulta.
4. Permitir confirmação, cancelamento ou solicitação de reagendamento.
5. Enviar um segundo lembrete próximo ao horário do atendimento.
6. Verificar posteriormente se a consulta foi realizada.
7. Caso tenha sido realizada, iniciar o fluxo de acompanhamento pós-sessão.
8. Aguardar o período configurado para o profissional ou tipo de atendimento.
9. Notificar o terapeuta para que entre em contato com o paciente e verifique como ele está após a sessão.
10. Registrar se o acompanhamento foi realizado.
11. Manter histórico dos lembretes, confirmações, cancelamentos, reagendamentos, erros e acompanhamentos.
12. Permitir novos lembretes de acompanhamento longitudinal, quando necessário.

## ⚠️ Regras importantes

- Somente pacientes com consultas ativas devem receber mensagens.
- Consultas canceladas ou reagendadas não devem continuar no fluxo original.
- O workflow deve evitar mensagens duplicadas.
- Os horários e a antecedência dos lembretes devem ser configuráveis.
- O intervalo para acompanhamento pós-sessão deve variar conforme o terapeuta e o tipo de atendimento.
- A mesma automação deve atender diferentes profissionais por meio de configurações individuais.
- O sistema deve registrar o status das mensagens quando o canal utilizado disponibilizar essas informações.
- Cancelamentos e solicitações de reagendamento devem gerar notificação ao profissional.
- Mensagens automáticas não devem expor diagnósticos, medicamentos ou outros dados sensíveis desnecessários.
- O tratamento dos dados deve considerar privacidade, consentimento, segurança e os requisitos aplicáveis da LGPD.
- Respostas que indiquem urgência, agravamento ou intercorrência clínica devem ser encaminhadas para avaliação humana.
- A automação deve apoiar, e não substituir, o julgamento clínico ou terapêutico.
- O sistema deve possuir tratamento de erros para falhas de API, números inválidos, ausência de dados obrigatórios e indisponibilidade de serviços.

---

# 🤖 Prompt Final

```text
Atue como um especialista em n8n, automação de processos e integração de APIs.

Crie uma automação no n8n para gerenciamento de lembretes de consultas e acompanhamento pós-atendimento de pacientes de diferentes profissionais da saúde e terapeutas.

Público:
Fisioterapeutas, psicólogos, acupunturistas, psiquiatras, terapeutas integrativos e outros profissionais que realizam atendimentos periódicos e precisam manter comunicação e acompanhamento com seus pacientes.

Objetivo:
Automatizar o envio de lembretes de consultas aos pacientes e organizar o acompanhamento pós-sessão, reduzindo esquecimentos e faltas, melhorando a comunicação entre terapeuta e paciente e facilitando o acompanhamento longitudinal.

Ferramentas envolvidas:
- n8n para criação e gerenciamento dos workflows;
- Google Calendar ou outro sistema de agenda para consultar consultas agendadas;
- Google Sheets, Airtable ou banco de dados para armazenar dados operacionais dos agendamentos;
- WhatsApp Business API, e-mail ou SMS para envio de mensagens aos pacientes;
- WhatsApp, Telegram, e-mail ou outro canal interno para notificações aos terapeutas;
- Webhooks e APIs para comunicação entre os diferentes sistemas.

Fluxo:
1. Consultar periodicamente a agenda dos terapeutas.
2. Identificar consultas agendadas para o dia seguinte.
3. Enviar automaticamente ao paciente uma mensagem lembrando a data e o horário da consulta.
4. Permitir que o paciente confirme o atendimento ou informe necessidade de cancelamento ou reagendamento.
5. Próximo ao horário da consulta, enviar um segundo lembrete ao paciente.
6. Verificar posteriormente se o atendimento foi realizado.
7. Caso a consulta tenha sido realizada, iniciar o fluxo de acompanhamento pós-sessão.
8. Aguardar o período configurado para aquele profissional ou tipo de atendimento.
9. Enviar uma notificação ao terapeuta lembrando-o de entrar em contato com o paciente para saber como ele está após a sessão.
10. Permitir o registro de que o acompanhamento foi realizado.
11. Registrar no sistema os lembretes enviados, confirmações, cancelamentos, reagendamentos, erros e acompanhamentos realizados.
12. Caso necessário, permitir novos lembretes de acompanhamento longitudinal.

Regras:
- Somente pacientes com consultas ativas devem receber mensagens.
- Consultas canceladas ou reagendadas não devem continuar no fluxo de lembretes original.
- O workflow deve evitar mensagens duplicadas para a mesma consulta.
- O horário e a antecedência dos lembretes devem ser configuráveis.
- O tempo para o acompanhamento pós-sessão deve ser configurável de acordo com o terapeuta e o tipo de atendimento.
- Diferentes profissionais devem poder utilizar a mesma automação com configurações individuais.
- Registrar o status de cada mensagem, como enviada, entregue, respondida ou com erro, quando essas informações estiverem disponíveis.
- Caso o paciente solicite cancelamento ou reagendamento, o profissional responsável deve ser notificado.
- As mensagens automáticas não devem expor diagnóstico, medicamentos, condição clínica ou outros dados sensíveis desnecessários.
- O tratamento dos dados deve considerar privacidade, consentimento, segurança e os requisitos aplicáveis da LGPD.
- Utilizar somente os dados necessários para executar os lembretes e acompanhamentos.
- Respostas que indiquem situação de urgência, agravamento importante ou intercorrência clínica devem ser encaminhadas para avaliação humana.
- A automação deve funcionar como suporte ao acompanhamento profissional e não substituir decisões clínicas ou terapêuticas.
- O sistema deve possuir tratamento de erros para situações como falha na API, número inválido, indisponibilidade do serviço ou ausência de informações obrigatórias.

Explique detalhadamente quais nós do n8n devem ser utilizados em cada etapa do workflow.

Para cada nó, informe:
- nome do nó;
- função dentro da automação;
- principais configurações;
- dados recebidos;
- dados enviados para o próximo nó.

Apresente também a lógica das conexões entre os nós.

Utilize, quando apropriado, nós como:
- Schedule Trigger;
- Google Calendar;
- Google Sheets;
- HTTP Request;
- Webhook;
- IF;
- Switch;
- Wait;
- Set ou Edit Fields;
- Code;
- Merge;
- Data Store;
- Error Trigger.

Organize o workflow de forma modular, evitando criar fluxos completamente diferentes para cada profissão.

Sempre que possível, utilize campos configuráveis como:
- ID do terapeuta;
- nome do terapeuta;
- nome do paciente;
- telefone ou contato;
- data da consulta;
- horário da consulta;
- status da consulta;
- tipo de atendimento;
- antecedência do primeiro lembrete;
- antecedência do segundo lembrete;
- tempo até o acompanhamento pós-sessão;
- status do lembrete;
- status do acompanhamento.

Ao final, apresente a estrutura do workflow em ordem, no formato:

Nó 1 → Nó 2 → Nó 3 → Nó 4...

Depois, explique um exemplo completo do fluxo de uma consulta, desde o agendamento até o acompanhamento pós-sessão.

Priorize uma solução simples o suficiente para ser implementada por alguém que está aprendendo n8n, mas estruturada de forma que possa evoluir posteriormente para um sistema utilizado por vários terapeutas.
```

## 📚 Aprendizados

Este desafio permitiu praticar:

- estruturação de prompts;
- definição de objetivos e regras de negócio;
- automação de processos;
- organização de workflows no n8n;
- integração de APIs;
- tratamento de exceções;
- privacidade e proteção de dados;
- pensamento modular para soluções que possam evoluir futuramente.

## 🚀 Possíveis evoluções

Como próximos passos, a proposta pode evoluir para:

- implementação real do workflow no n8n;
- integração com Google Calendar;
- integração com WhatsApp Business;
- painel de acompanhamento de consultas;
- confirmação automática de atendimentos;
- acompanhamento longitudinal configurável;
- suporte a múltiplos terapeutas e clínicas.
