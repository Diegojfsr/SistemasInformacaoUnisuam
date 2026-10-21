## Apresentação

O processo é a abstração usada pelos sistemas operacionais para representar cada uma das tarefas, sendo executadas em um dado instante. Cada programa executado em um sistema operacional terá suas informações mantidas através de processos que são gerenciados pelo sistema.

Um processo é composto por informações sobre valores dos registradores durante a sua execução; posições de memória relativas ao código; pilha de execução e dados do programa; seu relacionamento com outros processos; e o seu estado, que define se um processo está sendo executado, está disponível para ser executado ou se há algo que bloqueie a sua execução no momento. Uma das tarefas mais básicas de um sistema operacional é garantir que cada processo seja executado sem que haja interferência de outros. Em computadores modernos, com múltiplas CPUs e execução realmente paralela, o gerenciamento de processos é essencial para o correto funcionamento do sistema.

Nesta Unidade de Aprendizagem, você aprenderá como um sistema operacional utiliza o conceito de processo para permitir a execução de múltiplos programas em um computador, desde a criação, o gerenciamento (passando pela máquina de estados de execução), até o término dos processos.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Explicar o modelo de um processo.
- Reconhecer eventos de criação e de término de processos em um sistema operacional.
- Apontar as mudanças de estado de um processo.


## Desafio

Gerenciadores de tarefa são aplicações que permitem que os usuários de um sistema operacional visualizem o andamento dos processos em execução. Sistemas operacionais com foco em usuários comuns, como Windows e Ubuntu Linux, possuem gerenciadores de tarefa gráficos, com interfaces de uso simples e com destaque para as principais informações necessárias para o entendimento do funcionamento do sistema, como uso de CPU, Memória, Disco e Rede de cada processo. A análise destes valores é importante para profissionais de TI ao realizar análises de performance de sistemas, redes ou aplicações. Também são disponibilizadas ferramentas de linha de comando com o mesmo objetivo, como o tasklist (Windows) e o top (Linux e outras variações de Unix), que geralmente são preferidas por profissionais mais experientes. Muitos problemas podem ser indicados pelo adequado acompanhamento dos valores disponíveis nestas aplicações.

Considere a situação a seguir:

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/5ee81869-2e11-4122-a19c-8fbfb402acd4/fb641956-2ffc-4839-9a0f-5fb382d61418.png)

​​​​​​​

Para compreender o que está acontecendo em ambos os computadores e identificar o problema que está ocorrendo na aplicação, responda as questões a seguir:

a) Com base nas observações do gerenciador de tarefas e nos conhecimentos adquiridos sobre processos e seus estados, este problema pode ser causado por um excesso de chamadas de E/S realizadas pela aplicação? Justifique sua resposta.  
  
b) Por que em um dos computadores o consumo de CPU chega a 100% e inviabiliza o uso da interface gráfica do sistema operacional, e no outro computador a mesma aplicação aparenta usar menos processamento e o sistema continua usável, ainda que a aplicação em si esteja quase travada?  
  
c) Qual tipo de erro, a nível de código, pode estar causando este problema? Justifique sua resposta.

#### Padrão de resposta esperado

a) Já que o gerenciador de tarefas está mostrando que o processo está sendo executado, seu estado não está sendo bloqueado. Isso indica que a aplicação está realizando muitos processamentos, mas não há muita espera por resposta de dispositivos de Entrada e Saída. Com base nessas observações, é possível afirmar que o excesso de chamadas de E/S não é responsável pelo problema da aplicação.

b) O computador que chega a 100% de uso da CPU só tem um núcleo. Como apenas um processo por núcleo pode ser executado de cada vez, e o processo da aplicação está consumindo muitos ciclos de processamento, não está deixando tempo livre para que outros processos que precisam rodar no sistema operacional, inclusive os que gerenciam a própria interface gráfica do sistema operacional, tenham sua vez. O outro computador tem quatro núcleos, então o processo da aplicação está consumindo quase 100% de um único núcleo, mas ainda há três que podem executar outros processos, logo, do total de ciclos disponíveis na máquina, o processo da aplicação está consumindo no máximo 25%.

c) Como o processo executa sem parar, chegando a travar um computador com um único núcleo, e mesmo no outro ele não termina e a possibilidade de ser um problema de E/S foi excluída, os desenvolvedores devem suspeitar de problemas em laços que por algum motivo não estejam sendo terminados, entrando numa situação de loop infinito.  
Se a aplicação está sendo desenvolvida em uma linguagem cujo compilador efetue otimização de chamada de cauda, o problema também pode ser em uma recursão efetuada no fim do próprio método, já que este tipo de otimização removeria a possibilidade de ocorrer um erro de estouro de pilha e permitiria que a aplicação, ao executar, tivesse o comportamento observado.

####  ✅ Resposta ao desafio:

Com base na situação apresentada e nos conceitos de sistemas operacionais, aqui estão as respostas detalhadas para cada uma das questões:

a) O problema pode ser causado por um excesso de chamadas de E/S?
Não. Como o gerenciador de tarefas indica que o processo está em execução contínua consumindo alta capacidade de processamento, o seu estado não é o de bloqueado por espera de E/S. Isso demonstra que a aplicação está realizando um processamento computacional massivo ou travado, e não há uma espera excessiva por respostas de dispositivos de Entrada e Saída.   

b) Por que em um computador o consumo chega a 100% (travando o SO) e no outro fica em cerca de 25% (mantendo o SO usável)?Computador de um único núcleo: Como o processador possui apenas um núcleo e a aplicação consome vorazmente os ciclos de CPU, nenhum tempo livre ou processamento adicional sobra para os demais processos do sistema operacional — incluindo os responsáveis por renderizar a interface gráfica —, causando o travamento geral.   Computador de quatro núcleos: A aplicação consome 100% da capacidade de um único núcleo (o que equivale a 25% do total de processamento da máquina de quatro núcleos). Como sobram os outros três núcleos livres, o sistema operacional consegue alocar recursos para rodar outras tarefas e manter a interface gráfica usável, embora a aplicação específica continue travada.   

c) Qual tipo de erro, a nível de código, pode estar causando este problema?
O problema é caracterizado por um processo que executa ininterruptamente sem nunca terminar. Os desenvolvedores devem suspeitar de um loop infinito (laços de repetição cuja condição de parada nunca é atingida) ou de um problema de recursão infinita (uma função que chama a si mesma sem um caso base adequado para encerrar a chamada). 


## Infográfico

A máquina de estados de um processo define, a partir do estado atual do processo, quais mudanças de estado são possíveis. Sistemas operacionais como Windows e Linux usam máquinas mais complexas, mas de forma geral é possível resumir o número de estados em que um processo pode estar, que são três: 1. Em execução; 2. Pronto; e 3. Bloqueado (também chamado de Espera). Ao entrar em um destes estados, o processo só poderá ser alterado para outro respeitando o fluxo definido na máquina de estados.

No Infográfico a seguir, você vai ver a máquina de estados de um processo, compreender o que está acontecendo com ele em cada um dos possíveis estados e entender que eventos podem disparar uma mudança de estado.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/563c4961-1978-4fa2-b36c-b0647f5502d8/aa850bd7-5f84-4253-8333-9b39010af2c5.png)

​​​​​​​​​​​​​
## Conteúdo do Livro

Em sistemas operacionais, quando se inicia um programa, automaticamente ele é atribuido a um processo. Os processos são gerenciados pelo sistema, de maneira que, durante toda a sua execução, são coletas informações importantes, como, por exemplo, os dados do programa que iniciou sua execução.

Considerando os computadores modernos e sua evolução, temos a falsa sensação de que inúmeros processos são executados ao mesmo tempo. No entanto, as coisas não ocorrem bem dessa forma.

No capítulo Conceituação e gerenciamento de processos, base teórica desta Unidade de Aprendizagem, você poderá compreender como de fato os processos se comportam, identificando que cada processo executado tem seu tempo de criação e finalização, bem como diferentes fases de execução.

Boa leitura.

## Dica do Professor

Processos precisam ser constantemente criados e terminados pelo Sistema Operacional, que acontecem em determinados eventos. Desenvolvedores e administradores de sistemas que precisam interagir com processos criam aplicações e garantem o bom funcionamento de computadores, aplicando os conhecimentos destes eventos em suas atividades do dia a dia.

Nesta Dica do Professor, você vai estudar sobre a criação e o término de processos. Também verá que eventos podem causar o início de um processo e também o que leva um processo a ser encerrado.​​​​​​​​​​​​​​


## Exercícios

#### Questão 1
Programas com interface de linha de comando (command line interface - CLI), apesar de não intuitivos para usuários normais de computadores, são populares entre programadores devido à sua praticidade e agilidade quando o utilizador conhece seus comandos e atalhos. Estes programas são muito dependentes de entrada do usuário, podendo solicitar que seu utilizador digite comandos para poder efetuar seu trabalho.
Assinale a alternativa correta sobre o estado no qual o processo de um programa CLI se encontra enquanto aguarda que seu utilizador digite um comando:
Selecione a resposta:
A.Executando.
B.Pronto.
C.Bloqueado ou Espera.
D.Terminado.
E.Em transição.

✅ A alternativa correta é: C

#### Questão 2
A diferença entre programa e processo é essencial para compreender como um sistema operacional executa suas atividades. Enquanto um programa é a implementação de um algoritmo para completar uma tarefa, um processo é a representação da execução deste algoritmo por um computador. Sabendo disso, assinale a alternativa que contém apenas elementos da tabela de processo:​​​​​​​
Selecione a resposta:
A.Contador de programa; ponteiros para base e topo da pilha; valores dos registradores; e estado do processo.
B.Atributos de instância; métodos estáticos e de classe; constantes; e máquina de estados do processo.
C.Linhas de código; arquivo-objeto; compilador; e ambiente de execução.
D.Chamadas de sistema; escalonadores; memória; e modelo de processos.
E.Hierarquia de processos; estados de processos; código fonte; e gerenciamento de memória.

✅ A alternativa correta é: A


#### Questão 3
O modelo de processo é uma característica bastante importante para sistemas operacionais modernos. A partir deste modelo, é definido como um sistema específico irá executar os programas que seus usuários desejarem. O modelo de processos de um computador multiprogramado permite que vários programas estejam em execução em um determinado momento, passando para o usuário a impressão de que o computador está fazendo todas as atividades simultaneamente. Considerando um computador com apenas um núcleo de processamento e três programas sendo executados, cada um com seu processo sendo gerenciado pelo sistema operacional, assinale a alternativa correta.​​​​
Selecione a resposta:
A.Os três processos estão sendo executados pelo processador ao mesmo tempo, não havendo necessidade de manutenção de tabela de processos.
B.Um dos processos está sendo executado e os outros dois estão prontos ou bloqueados. Apenas os processos bloqueados têm registros na tabela de processos.
C.Os três processos estão sendo executados pelo processador ao mesmo tempo. Todos os três processos têm registros na tabela de processos
D.Um dos processos está sendo executado e os outros dois estão prontos ou bloqueados. Todos os três processos têm registros na tabela de processos.
E.Um dos processos está sendo executado e os outros dois estão prontos ou bloqueados. Apenas o processo em execução tem registro na tabela de processos.

✅ A alternativa correta é: D

#### Questão 4
Frequentemente, programadores têm a necessidade de iniciar novos programas a partir do software que estão criando. Isto pode servir para facilitar o desenvolvimento de uma determinada funcionalidade, efetuar ajustes de configuração ou aproveitar um software já existente que não fornece APIs para acesso às suas funcionalidades na linguagem usada pelo programador.
Assinale a alternativa correta em relação a como um programador usando Java, C# ou Python deve efetuar a criação de um novo processo em um programa que será executado em um sistema operacional moderno.​​​​​​​
Selecione a resposta:
A.Solicitar que o usuário inicie manualmente o outro programa e bloqueie o processo, devendo ele informar que o programa foi terminado para desbloquear e continuar a execução.
B.Incluir trechos de código assembly para mudar o contexto do processador para Kernel Mode e posteriormente solicitar a troca de contexto para um novo processo.
C.Efetuar chamadas de sistema explícitas utilizando código nas linguagens citadas na questão, para que o sistema operacional viabilize a criação dos novos processos.
D.Iniciar uma nova tarefa em lote e despachá-la para o sistema operacional para que o sistema possa executá-la quando houverem recursos computacionais livres.
E.Utilizar métodos, funções ou classes de bibliotecas que abstraem as chamadas de sistema e efetuam a criação do processo de acordo com o sistema operacional em execução.

✅ A alternativa correta é: E


#### Questão 5
Aplicações desenvolvidas para uso em servidores Web devem ser projetadas tendo em mente que em vários momentos este servidor receberá um grande número de requisições paralelas. Software de servidores Web, como o Apache, possuem configurações para que cada nova requisição recebida dispare a criação de um novo processo independente para tratá-la. Um Administrador de Sistemas está analisando um problema em que um servidor Web com baixo uso de processador e bastante memória disponível não está sendo capaz de atender todas as requisições. Ao listar os processos que estão sendo executados, há centenas de processos do servidor Web, mas nenhum usando recursos da CPU. Assinale uma alternativa que contém uma explicação possível para o problema em questão.​​​​​
Selecione a resposta:
A.Os processos do servidor Web estão todos bloqueados, devido à escassez de banda de E/S com o disco rígido do servidor.
B.A tabela de processos do sistema operacional está cheia, não permitindo a criação de novos processos.
C.O modelo de processo do sistema operacional utilizado no servidor é inadequado para a execução de um servidor Web.
D.Há um erro na aplicação que está causando um término por saída involuntária dos processos.
E.O código da aplicação contém um erro em um dos laços (for ou while), causando um loop infinito.

✅ A alternativa correta é: A


## Na prática

Ferramentas de Gerenciamento de Tarefas gráficas são bastante úteis, tanto para usuários comuns quanto para Desenvolvedores e Administradores de Sistemas. Sistemas como o Microsoft Windows e o Ubuntu Linux dedicam esforços contínuos para melhorar a visualização das informações de processos sendo executados, aumentando a quantidade de dados disponíveis para que o usuário entenda como está a saúde do sistema. Um bom profissional conhece as funcionalidades deste tipo de ferramenta e é capaz de interpretar as informações disponíveis.

Neste Na Prática, confira algumas ações que podem ser tomadas a partir do Gerenciador de Tarefas do Windows 10 e do Monitor do Sistema do Ubuntu Linux 18.04LTS.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/e98b513c-0ac5-430b-b811-540e8013e274/1db1006a-c96f-4448-adc1-3e606411a494.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Gerenciamento de Processos no Linux
Neste conteúdo, você irá entender melhor como o kernel do Linux realiza internamente o gerenciamento e o escalonamento de processos, e como o administrador pode interferir nessa dinâmica através dos comandos “nice” e “renice”.
[Mais](https://linuxsemfronteiras.com.br/gerenciamento-de-processos-no-linux/)

Como usar o Gerenciador de Tarefas no Windows 10
Tem dúvidas sobre como usar o Gerenciador de Tarefas do Windows 10? Acesse este site e confira algumas dicas.
[Mais](https://www.techtudo.com.br/noticias/2017/02/como-usar-o-gerenciador-de-tarefas-no-windows-10.ghtml)

Utilizando o Process Explorer
O Process Explorer é um utilitário de gerenciamento de tarefas mais completo que o Gerenciador de Tarefas do Windows. Este link explica como instalar e usar a ferramenta. Clique para saber mais.
[Mais](https://learn.microsoft.com/pt-br/archive/technet-wiki/2541.utilizando-o-process-explorer)

RedHat Linux - Ferramentas de Monitoramento de Linha de Comando Embutida
Neste site, você verá uma sugestão de ferramentas para gerenciamento de sistemas e consequentemente dos seus processos no RedHat Linux. Clique para conhecer.
[Mais](https://docs.redhat.com/pt-br/documentation/red_hat_enterprise_linux/6/html/performance_tuning_guide/s-analyzeperf-cli-tools)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

DEITEL, Harvey; DEITEL, Paul; CHOFFNES, David. Sistemas operacionais. 3. ed. São Paulo:
Prentice Hall do Brasil, 2005.

HOFFMAN, Chris. Windows Task Manager: The Complete Guide. How-To Geek, 28 mar. 2019.Disponível em: https://www.howtogeek.com/405806/windows-task-manager-the-complete-guide/.Acesso em: 16 dez. 2019.

TANENBAUM, Andrew. Sistemas operacionais modernos. São Paulo: Pearson Brasil, 2003.

TANENBAUM, Andrew; WOODHULL, Albert. Sistemas operacionais: projeto e implementação.Porto Alegre: Bookman, 2008.

Banco de imagens Shutterstock.
SAGAH, 2020.


