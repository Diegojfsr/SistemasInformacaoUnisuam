## Apresentação

Um computador executa diversas atividades simultaneamente,  
​​​​​​​processos oriundos das mais diversas funcionalidades que essa máquina tão surpreendente é capaz de desempenhar. O sistema operacional tem a função de realizar a comunicação entre o hardware e as ações que o usuário pode vir a executar em um computador.

Nesta Unidade de Aprendizagem, você vai aprender sobre a sincronização de processos, ou seja, aplicações concorrentes. Uma vez que o computador executa diversos processos ao mesmo tempo, é importante saber como ele consegue administrar essas atividades. Você vai estudar também sobre possíveis problemas acerca do compartilhamento de recursos.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir aplicações concorrentes.
- Discutir a comunicação entre aplicações concorrentes.
- Identificar os problemas de compartilhamento de recursos.

## Desafio

Ao acessar páginas Web, você já notou que, ao longo dos anos, elas passaram a trazer muitos contextos diferentes? Antes viam-se apenas textos; hoje, além dos textos, veem-se também diversas imagens, vídeos, gifs, dentre outros elementos.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/55877bec-b484-4eeb-8185-bd7c73e60ecf/61d11749-9ab8-4a3d-bd3f-ba730ebefbe7.jpg)

​​​​​​​Para solucionar o impasse, você percebe que deve haver a implementação de uma thread para que o desempenho da aplicação atenda às demandas do cliente.

Descreva como as várias solicitações da aplicação do cliente serão atendidas pelo seu site.

#### Padrão de resposta esperado
A solução mais adequada é a utilização de um ambiente multithread, onde cada processo pode responder a várias solicitações concorrentemente, ou mesmo simultaneamente caso haja mais de um processador.

A grande vantagem do uso de threads é a possibilidade de minimizar a alocação de recursos do sistema, além de diminuir o overhead na criação, troca e eliminação de processos.

####  ✅ Resposta ao desafio:

Para atender às várias solicitações da aplicação do cliente de forma eficiente e otimizar o desempenho, a solução mais adequada é a utilização de um ambiente multithread, onde cada processo pode responder a várias solicitações concorrentemente, ou mesmo simultaneamente caso haja mais de um processador.

Funcionamento da Solução
Concorrência e Paralelismo: Em vez de realizar requisições de forma puramente sequencial o que causaria um gargalo significativo devido ao tempo necessário para o navegador estabelecer conexões separadas para cada imagem, vídeo ou elemento gráfico , o servidor ou a aplicação utiliza múltiplas threads para processar diversos pedidos em paralelo.

Minimização de Recursos: A grande vantagem do uso de threads é a possibilidade de minimizar a alocação de recursos do sistema. Como as threads compartilham o mesmo espaço de memória do processo principal, o custo de gerenciamento é drasticamente reduzido.

Redução de Overhead: O uso de threads diminui o overhead (sobrecarga computacional) associado à criação, troca de contexto (context switching) e eliminação de processos completos, garantindo uma resposta muito mais ágil e fluida para os usuários que acessam a página web.


## Infográfico

Conforme Silberschatz (2015), um thread é uma unidade básica de utilização da CPU. É composto por um ID de thread, um contador de programa, um conjunto de registradores e uma pilha. Um thread compartilha com outros threads pertencentes ao mesmo processo sua seção de código, a seção de dados e outros recursos do sistema operacional, como arquivos abertos e sinais.

Os threads estão presentes em diversos níveis dentro de um processo. Dessa forma, é importante conhecer alguns conceitos de threads de modo usuário, modo kernele modo híbrido.

Confira no Infográfico a seguir.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/fa2286cd-6e01-4008-996a-80e44c446a8f/5f76f14c-691b-485a-b10d-1b9f54fb0266.png)

​​​​​​​​​​​​​​


## Conteúdo do Livro

Descobrir como um computador opera todas nossas ações diante de suas funcionalidades é genial. É impossível sequer imaginar a quantidade de componentes que fazem parte dessa ferramenta, todos funcionando de maneira simultânea. Na obra Sistemas operacionais, leia o capítulo Concorrência e sincronização de processos, no qual são abordados conceitos acerca dos processos, ou seja, o que compõe um processo. Você vai ver como o computador executa diversas atividades quase que simultaneamente e como se torna capaz de solucionar nossas necessidades diárias.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/49b649e0-e515-473c-a72c-362b22d138b1/535c4a1e-cd36-4a47-b7b8-af3b65a52a96.jpg)

​​​​​​​

## Dica do Professor

A gerência de processos é uma atividade muito importante para o funcionamento computacional. Assim, os sinais são utilizados para notificar processos oriundos do próprio sistema operacional.

Confira na Dica do Professor alguns conceitos acerca do tema.


## Exercícios

#### Questão 1
Ao serem salvos, todos os dados de controle do processador, registradores e outras informações do primeiro são substituídas por informações de processo do segundo. Esses conceitos são referentes a qual tipo de ação?​​​​​​​
Selecione a resposta:
A.Troca de processos.
B.Criação de threads.
C.Threads.
D.Troca de registradores.
E.Troca de programas.

✅ A alternativa correta é: A

#### Questão 2
Um processo é formado por três partes fundamentais, as quais são capazes de, juntas, manter as informações necessárias para a execução de um programa. Assinale a alternativa que apresenta essas três partes.​​​​​​​
Selecione a resposta:
A.Contexto de hardware, tempo de processador e espaço de endereçamento.
B.Espaço de endereçamento, contexto de hardware e contexto de software.
C.Registrador de PC, registrador de status e tempo de processador.
D.Quotas, privilégios e tempo de processador.
E.Registradores, contexto de software e registrador de status.

✅ A alternativa correta é: B


#### Questão 3
Quando um processo tem apenas um programa em seu espaço de endereçamento, estamos nos referindo a qual tipo de ambiente de atuação de uma thread?​​​​​​​
Selecione a resposta:
A.Multithread.
B.Troca de processos.
C.Monothread.
D.Troca de contexto.
E.Troca de registradores.

✅ A alternativa correta é: C

#### Questão 4
Em um processo, podemos localizar diversas informações. Um processo é composto por código, dados e arquivos e, em determinadas situações, haverá momentos em que teremos diversos registradores e pilhas agindo no mesmo processo. Assinale a seguir a alternativa que apresenta o conceito referente a esse contexto.​​​​​​​
Selecione a resposta:
A.Registrador de PC.
B.Tempo de processador.
C.Contexto de software.
D.Monothread.
E.Multithread.

✅ A alternativa correta é: E

#### Questão 5
Assinale a alternativa que apresenta o conceito implantado com o objetivo de reduzir o uso de recursos do sistema e o tempo gasto em criação de contexto de processos nas aplicações.
Selecione a resposta:
A.Thread.
B.Contexto de hardware.
C.Contexto de software.
D.Espaço de endereçamento.
E.Registrador de status.

✅ A alternativa correta é: A


## Na prática

Mal sabemos que, ao utilizarmos o computador, estamos quase que simultaneamente criando diversas threads e, assim, executando diversos processos. Pois bem, cada atividade desempenhada em um computador requer o processamento de diversas informações e, consequentemente, a organização completa do modo como tudo isso deve acontecer. Confira na prática como threads podem ser criadas por meio da programação dos computadores com a linguagem Java.  

  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/9d408302-b356-44a1-a7f5-d20d72aff078/23dae5f1-49ce-42df-995c-bcd672e43feb.jpg)

​​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Sincronização e comunicação entre processos
Assista ao vídeo para conhecer um pouco sobre a sincronização e a comunicação entre processos. A possibilidade de execução simultânea de mais de um processo faz com que o computador disponibilize diversos comportamentos possíveis diante desse contexto.
[Mais](https://www.youtube.com/embed/bRAEToyq3mg)

Sincronização de processos
Assista ao vídeo para conferir na prática como pode ser programada a sincronização, que corresponde à possibilidade de um processo ser executado quase que simultaneamente a outro, caso em que o computador deve aplicar métodos para permitir e organizar a execução dos processos.
[Mais](https://www.youtube.com/embed/txK7TN7d9kI)

Threads e sincronização e comunicação entre processos
Assista ao vídeo para compreender mais sobre a thread, que pode ser considerada um programa que permite a divisão de um processo em diversos outros subprocessos, além de permitir aplicações concorrentes e compartilhamento de recursos pelo mesmo processo.
[Mais](https://www.youtube.com/embed/NucqOdjrprg)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

DELGADO, J.; RIBEIRO, C. Arquitetura de computadores. 5. ed. atual. Rio de Janeiro: LTC, 2017.

MACHADO, F.B.; MAIA, L.P. Arquitetura de sistemas operacionais. 5. ed. Rio de Janeiro: LTC, 2017.

MACHADO, F.B.; MAIA, L.P. Fundamentos de sistemas operacionais. Rio de Janeiro: LTC, 2011.

PAIXÃO, R.R. Arquitetura de computadores. 1. ed. Sã o Paulo: É rica, 2014.

SILBERSCHATZ, A.; GALVIN, P.B.; GAGNE,G. Fundamentos de sistemas operacionais. 9. ed. Rio deJaneiro: LTC, 2015.

STALLINGS, W. Arquitetura e organização de computadores. 8.ed. São Paulo: Prentice Hall, 2010.

TANENBAUM, A. Organização estruturada de computadores. São Paulo: Pearson Prentice Hall,2013.

TANENBAUM, A.S.; ALBERT, W.S. Sistemas operacionais: projeto e implementaçã o. 3. ed. PortoAlegre: Bookman, 2008.

Banco de imagens Shutterstock.
SAGAH, 2018.

