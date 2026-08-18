##  Requisitos Funcionais (RF)

Descrevem as ações, recursos e comportamentos que o sistema deve executar diretamente para atender às necessidades dos usuários:

### 1. Autenticação e Perfil de Usuário
* **RF01 - Gestão de Acessos:** O sistema deve permitir o login diferenciado para cada perfil de usuário (Professores, Coordenadores, Equipe de Suporte/TI e Manutenção).
* **RF02 - Perfil do Colaborador:** O sistema deve armazenar a grade de horários, disciplinas lecionadas, carga horária semanal e banco de horas de cada professor.

### 2. Gestão e Substituição de Aulas
* **RF03 - Solicitação de Ausência:** O professor deve conseguir cadastrar uma ausência (com opção de anexo de atestado) diretamente pelo aplicativo.
* **RF04 - Algoritmo de Recomendação de Substitutos:** O sistema deve analisar a disponibilidade, horário e disciplina para sugerir automaticamente uma lista de professores aptos para cobrir a aula vaga.
* **RF05 - Notificação de Convite:** O sistema deve enviar notificações em tempo real para o professor selecionado confirmar ou recusar a substituição.

### 3. Reserva de Recursos e Espaços
* **RF06 - Agendamento via QR Code / NFC:** O sistema deve permitir que os funcionários reservem e façam *check-in* de equipamentos e salas apontando a câmera do celular para o QR Code do item.
* **RF07 - Controle de Inventário:** O sistema deve registrar quem retirou determinado recurso, o horário de devolução previsto e o status do equipamento (em uso, disponível, em manutenção).

### 4. Assistente de Planos de Aula (IA)
* **RF08 - Gerador de Estrutura de Aula:** O sistema deve permitir a criação de planos de aula integrados às diretrizes da BNCC, com sugestões automáticas de dinâmicas via IA.
* **RF09 - Biblioteca de Atividades:** O sistema deve manter um repositório interno para que professores da mesma disciplina compartilhem e reutilizem planos de aula anteriores.

### 5. Central de Chamados e Manutenção
* **RF10 - Abertura de Chamados com Imagem:** O sistema deve permitir o registro de chamados de manutenção e TI anexando fotos e localização do problema dentro da escola.
* **RF11 - Acompanhamento de Status:** O sistema deve atualizar em tempo real o andamento do chamado (*Pendente*, *Em Atendimento*, *Concluído*).

### 6. Diagnóstico de Carga de Trabalho
* **RF12 - Painel Preditivo de Sobrecarga:** O sistema deve exibir para a gestão pedagógica alertas visuais indicando acúmulo excessivo de substituições, chamados pendentes ou horas extras por colaborador.

---

##  Requisitos Não Funcionais (RNF)

Descrevem os critérios de qualidade, desempenho, segurança e usabilidade que sustentam o funcionamento do sistema:

### 1. Usabilidade e Acessibilidade
* **RNF01 - Design Responsivo:** A interface web e móvel deve adaptar-se perfeitamente a smartphones, tablets e computadores de mesa.
* **RNF02 - Facilidade de Uso:** O fluxo de agendamento ou abertura de chamados deve ser concluído em no máximo 3 toques/cliques na tela.

### 2. Desempenho e Escalabilidade
* **RNF03 - Tempo de Resposta:** As requisições comuns (login, consultas de horários e reservas) devem responder em menos de 2 segundos.
* **RNF04 - Notificações Instantâneas:** O envio de alertas sobre substituições de aula deve ocorrer em até 5 segundos após a solicitação.

### 3. Segurança e Privacidade
* **RNF05 - Proteção de Dados:** O sistema deve estar em conformidade com a LGPD (Lei Geral de Proteção de Dados), criptografando senhas e dados sensíveis dos funcionários.
* **RNF06 - Autenticação Segura:** As sessões de usuário devem utilizar tokens JWT com tempo de expiração definido e renovação segura.

### 4. Disponibilidade e Manutenibilidade
* **RNF07 - Disponibilidade:** O sistema deve manter uma taxa de disponibilidade de no mínimo 99,5% durante os horários de funcionamento escolar.
* **RNF08 - Arquitetura Modular:** O backend deve ser desenvolvido de forma modular (ex: NestJS com microsserviços/módulos bem definidos) para facilitar futuras expansões e manutenções.
