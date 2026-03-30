🍅 Técnica Pomodoro — Timer Online
📌 Sobre o Projeto

Este projeto consiste em um timer online baseado na Técnica Pomodoro, com funcionalidades de gerenciamento de tarefas e foco produtivo.

A aplicação permite que o usuário:

Execute ciclos de foco (Pomodoro)
Gerencie tarefas
Acompanhe tempo produtivo
Siga o método clássico de produtividade

A técnica Pomodoro divide o trabalho em ciclos de 25 minutos de foco + 5 minutos de pausa, com pausas maiores após múltiplos ciclos .

🧠 Conceito do Produto

O sistema foi desenvolvido com base na Técnica Pomodoro, criada por Francesco Cirillo, que visa melhorar a produtividade por meio de ciclos de concentração e descanso .

Fluxo do método:
Escolher tarefa
Trabalhar por 25 minutos
Fazer pausa curta (5 min)
A cada 4 ciclos → pausa longa (15–30 min)
🏗️ Processo de Desenvolvimento
1. 📋 Levantamento de Requisitos

Funcionalidades definidas:

Timer Pomodoro (start, pause, reset)
Alternância automática entre:
Foco
Pausa curta
Pausa longa
Contador de ciclos
Lista de tarefas
Interface simples e responsiva
Feedback visual do tempo
2. 🎨 Design e UX

Objetivo:

Interface minimalista
Zero distrações
Foco total no timer

Decisões de UI:

Timer central destacado
Botões grandes e claros
Cores suaves para foco
Seção de tarefas abaixo
3. ⚙️ Arquitetura do Sistema

Estrutura típica de front-end:

/project
 ├── index.html
 ├── css/
 │    └── style.css
 ├── js/
 │    └── script.js
 └── assets/

Separação de responsabilidades:

HTML → estrutura
CSS → layout e responsividade
JavaScript → lógica do timer e estado
4. ⏱️ Implementação do Timer

Principais regras implementadas:

25 minutos (foco)
5 minutos (pausa curta)
15–30 minutos (pausa longa)
Contador de ciclos
Lógica base:
let time = 25 * 60;
let isRunning = false;

function startTimer() {
  if (!isRunning) {
    isRunning = true;
    interval = setInterval(() => {
      time--;
      updateDisplay();
      
      if (time === 0) {
        switchMode();
      }
    }, 1000);
  }
}
5. 🔄 Controle de Estados

Estados do sistema:

FOCUS
SHORT_BREAK
LONG_BREAK

Transições:

FOCUS → SHORT_BREAK → FOCUS → ...
A cada 4 ciclos → LONG_BREAK
6. 📝 Sistema de Tarefas

Funcionalidades:

Adicionar tarefa
Listar tarefas
Marcar como concluída
Limpar tarefas concluídas

Exemplo:

function addTask(task) {
  tasks.push({
    title: task,
    done: false
  });
}
7. 📊 Feedback de Produtividade

O sistema exibe:

Número de pomodoros concluídos
Tempo total focado
Progresso do usuário
8. 🎵 Recursos Extras
Música para foco (opcional)
Interface motivacional
Dicas de produtividade
9. 📱 Responsividade
Mobile-first
Layout adaptável
Botões acessíveis em telas pequenas
10. 🚀 Deploy

Possíveis opções utilizadas:

Vercel 
Hospedagem tradicional
Domínio próprio

Etapas:

Build do projeto
Upload dos arquivos
Configuração do domínio
HTTPS ativo


🧪 Testes

Testes realizados:
Timer regressivo correto
Troca de estados automática
Persistência de tarefas (se aplicável)
Responsividade

📈 Melhorias Futuras
🔔 Notificações sonoras
📊 Dashboard de produtividade
☁️ Sincronização em nuvem
📅 Histórico de uso


🛠️ Tecnologias Utilizadas
HTML5
CSS3
JavaScript 
React
Nest.js


🎯 Objetivo do Projeto

Ajudar usuários a:

Melhorar foco
Reduzir procrastinação
Organizar tarefas
Aumentar produtividade
📄 Licença

Este projeto é de uso livre para fins educacionais e pessoais.

👨‍💻 Autor

Desenvolvido por Guilherme Mestre
