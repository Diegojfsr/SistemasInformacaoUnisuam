## Apresentação

O estudo sobre sistemas distribuídos busca entender todas as características e todos os detalhes envolvidos acerca desse tema. Para isso, é necessário que você aprenda suas complexidades e todo o mecanismo central de comunicação entre processos que existem. É importante examinar cuidadosamente quais as formas como os processos, em máquinas diferentes, trocam de informações.

A diferença de comunicação entre um sistema distribuído para um sistema não distribuído está na forma mais difícil de como a comunicação é estabelecida. Em sistemas distribuídos, a comunicação ocorre por troca de mensagens; já nos sistemas não distribuídos a comunicação ocorre de maneira mais fácil, por meio de memória compartilhada.

Nesta Unidade de Aprendizagem, você irá aprender como ocorre, de fato, a comunicação em um sistema distribuído e qual sua importância, analisando os processos com suas trocas de mensagens, em máquinas diferentes, bem como conhecer a estrutura dessa comunicação.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Descrever os conceitos de escalonamento de processos e de sincronização de processos.
- Analisar a troca de mensagens entre processos em diferentes computadores.
- Caracterizar a arquitetura de comunicação.



## Desafio

Um sistema distribuído reúne vários computadores independentes, fazendo com que eles pareçam um sistema único. Esse sistema faz com que todos os componentes de hardware e software, localizados nos computadores interligados por uma rede, realizem a comunicação e coordenem suas ações somente por meio de troca de mensagens.

Em um contexto geral, podemos citar diversos exemplos de sistemas distribuídos, entre eles a Internet e a Intranet. Esses sistemas distribuídos realizam suas comunicações, mantendo um padrão de interligação e comunicação. A diferença entre eles é que a Internet é pública, aberta para que todos possam acessar, já a Intranet, apesar de utilizar a Internet, não é pública, mas sim utilizada por um grupo específico de pessoas. Ou seja, a Intranet não possui acesso aberto para qualquer pessoa.

Assim, considere a seguinte situação.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/5175ece4-432c-48e9-83d7-5000e7792f23/95f40724-f933-46fb-a5e6-3ba0de864df1.png)

  
Mostre alguns pontos importantes, como os pedidos a seguir.  

a) Desenhe o esboço do sistema distribuído de uma rede com acesso aberto para todos, uma rede de Internet.
b) No esboço do sistema distribuído de Internet, é necessário demonstrar qual é a importância dos protocolos.
c) No esboço do sistema distribuído de Internet, é necessário demonstrar quais serviços são utilizados nesse sistema.
d) Desenhe o esboço do sistema distribuído de rede fechada para um grupo específico de um usuário, uma rede de Intranet.
e) No esboço do sistema distribuído de Intranet, é necessário demonstrar quem faz o filtro da entrada e da saída de informações.
f) No esboço do sistema distribuído de Intranet, é necessário demonstrar se é possível a comunicação de mais de uma rede local.


#### Padrão de resposta esperado
Confira as respostas a seguir.
a) Esboço de um sistema distribuído de Internet:
(Ilustração que mostra um esquema de rede conectando a Internet a um Roteador 1, um Switch, computadores e dispositivos conectados por cabos e Wi-Fi (identificados pelas letras A, B, C, D e E), além de setas indicando navegação em rede local e impressão em rede local).
b) Protocolos intermedeiam a comunicação entre processos. Sendo assim, qualquer aplicação consegue se comunicar com outra aplicação, em plataformas diferentes.
c) Os serviços utilizados nesse sistema distribuído são: WWW, FTP e e-mail.
d) Esboço de um sistema distribuído de Intranet:
(Ilustração que mostra um esquema de Intranet com a Internet conectada a um Servidor de Firewall, dividindo o fluxo de dados para a Rede 1 (com um Servidor de Intranet e computadores) e a Rede 2).
e) No sistema distribuído de Intranet, o firewall é responsável pelo filtro de entrada e de saída de informações.
f) No sistema distribuído de Intranet, é possível que duas ou mais redes locais diferentes se comuniquem entre si, por meio de um servidor.


####  ✅ Resposta ao desafio:

Com base na proposta do projeto sobre sistemas distribuídos (Internet vs. Intranet), elaborei o esboço estruturado e detalhado conforme os pontos solicitados:

1.Sistema Distribuído de Internet (Rede de Acesso Aberto)
a) Esboço do sistema distribuído de Internet

``` bash
[ Dispositivos Finais: PCs, Smartphones, Servidores ] 
                        │
                  ( Wi-Fi / Cabo )
                        │
                        ▼
               [ Roteador / Switch ]
                        │
                        ▼
             [ Nuvem da Internet ] ── (Acesso Público e Aberto)
```

Descrição: O sistema consiste em múltiplos computadores, dispositivos móveis e servidores independentes interligados globalmente por meio de redes públicas, permitindo que qualquer usuário acesse os recursos livremente.

b) A importância dos protocolos
Papel fundamental: Os protocolos atuam como regras padronizadas que intermedeiam a comunicação entre processos. Graças a eles, aplicações executadas em plataformas, sistemas operacionais e hardwares totalmente diferentes conseguem se comunicar e trocar mensagens de forma compreensível (como o conjunto TCP/IP).

c) Serviços utilizados nesse sistema
Os principais serviços que operam sobre essa infraestrutura distribuída são:
WWW (World Wide Web): Acesso a páginas e aplicações web.
FTP (File Transfer Protocol): Transferência de arquivos.
E-mail: Envio e recebimento de mensagens eletrônicas.


2.Sistema Distribuído de Intranet (Rede Privada/Fechada)
d) Esboço do sistema distribuído de Intranet

``` Bash
[ Internet (Pública) ]
         │
         ▼
  [ Firewall / Roteador ] ── (Filtro de Segurança)
         │
         ├──► [ Rede Local 1 (LAN 1) ] ── (Servidor de Intranet + Computadores)
         │
         └──► [ Rede Local 2 (LAN 2) ] ── (Outros Computadores / Setores)
```

Descrição: A Intranet é uma rede privada que utiliza os mesmos padrões tecnológicos da Internet, mas restrita a um grupo específico de usuários (como os colaboradores de uma empresa).

e) O filtro de entrada e saída de informações
O elemento responsável por fazer o filtro de segurança na entrada e na saída de informações é o Firewall. Ele protege os dados internos da organização, bloqueando acessos não autorizados vindos da Internet pública e controlando o tráfego que sai da rede fechada.

f) Comunicação de mais de uma rede local
Sim, é totalmente possível. É viável interligar duas ou mais redes locais (LANs) diferentes dentro de uma mesma Intranet. Essa comunicação entre subredes ou redes locais distintas é realizada de forma centralizada ou roteada por meio de servidores e dispositivos de rede internos (como roteadores e switches), mantendo a integração e a troca de mensagens de forma segura.


## Infográfico

Em um sistema distribuído, quem define quais processos podem ser realizados em uma comunicação é a atividade de escalonamento. Sendo assim, um escalonamento realiza a distribuição dos processos que estão em processamento, auxiliando na comunicação entre processos em um dado sistema distribuído. A comunicação entre componentes em um sistema distribuído ocorre basicamente por troca de mensagens. Existem alguns métodos para que a comunicação ocorra e os processos troquem mensagens, como a comunicação síncrona (bloqueante) ou assíncrona (não bloqueante), comunicação por canais, por socketes, por portas e por protocolos, além da comunicação pelo modelo cliente-servidor e pelo modelo em grupo multicast.

Neste Infográfico, acompanhe o funcionamento do método por protocolo de comunicação entre processos em um sistema distribuído.​​​​​​​

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/6e110b8d-a572-414e-9259-f9dfa9a03e9f/7835ee92-ef80-497f-950d-54e104c9cb7a.jpg)

​​​​​​​
## Conteúdo do Livro

A comunicação entre sistema distribuídos envolve muitos fatores e elementos. Graças à evolução dos estudos relacionados à rede de computadores e do desenvolvimento dos micropocessadores, os sistemas distribuídos surgiram para melhorar o desempenho de aplicações compartilhadas e a comunicação dos agentes envolvidos em um sistema distribuído, seja software ou hardware.

No capítulo Comunicação entre processos, da obra Sistemas distribuídos, base teórica desta Unidade de Aprendizagem, aprenda a comunicação entre processos em um sistema distribuído e quais são as formas de comunicação (como um sistema distribuído se comunica). Saiba também a importância de escalonamento e de sincronização de processos, e o que, de fato, essas duas operações contribuem para um sistema distribuído. Por último, estude sobre a arquitetura de um sistema distribuído.

Boa leitura.


![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/a83b3a47-a643-4ac2-a41a-200654be4771/c498094e-a3ac-4f6a-b02a-bd6dc2ae1958.jpg)



## Dica do Professor

Em um sistema distribuído, é muito presente a utilização de sincronização de processos. Essa sincronização se define como uma ordenação de processos, não permitindo acessos excessivos ou desorganizados na comunicação em um sistema distribuído. Existem alguns algoritmos de sincronização de processos, como o Algoritmo de Lamport. Leslie Lamport é um cientista da computação norte-americano e fez grandes contribuições para a evolução dos estudos sobre sistemas distribuídos.

Nesta Dica do Professor, entenda melhor quais métodos um sistema distribuído utiliza para realizar a sincronização de processo e aprenda como a sincronização de processo ocorre, segundo o Algoritmo de Lamport.


## Exercícios

#### Questão 1
Graças ao desenvolvimento dos microprocessadores e da evolução do sistema computacional, em que os usuários passaram a usar computadores em rede, nasceram os sistemas distribuídos. Nesses sistemas, é necessário desenvolver técnicas eficientes para a distribuição de todos os processos que envolvem os elementos de processamento.
​​​​​​​Qual o nome da atividade que define quais processos poderão ser processados em um sistema distribuído?
Selecione a resposta:
A.Semáforo.
B.Escalonamento.
C.Síncrona.
D.Sockete.
E.Cliente-servidor.

✅ A alternativa correta é: B

#### Questão 2
Em um sistema distribuído, é necessário desenvolver técnicas eficientes para a distribuição de todos os processos que envolvem os elementos de processamento. Entende-se por distribuição a atividade de escalonamento de processos. A figura a seguir demonstra um método de algoritmo de escalanamento conhecido como prioridade:

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/7c0eace9-744d-4396-b90b-52c9ea72d16b/c411d0f0-3104-4498-a373-4c70b283ff7c.png)

​​​​​​​Além do método por prioridade, no algoritmo de escalonamento de sistemas em lote há quais exemplos?
Selecione a resposta:
A.Chaveamento circular (round-robin), prioridade e múltiplas filas.
B.Shortest process next, garantido e lottery.
C.Interativo, tempo real e garantido.
D.Chaveamento circular (round-robin), prioridade e garantido.
E.First-come First-served, Shortest job first e Shortest remaining time next.

✅ A alternativa correta é: E


#### Questão 3
A arquitetura de um comunicação envolve muitos processos e elementos importantes. É necessário entendê-la porque ela é a estrutura, a base que os processos utilizam dentro um sistema distribuído para realizar uma comunicação. Em uma arquitetura de comunicação, existem particularidades e mecanismos que auxiliam nesse processo. Sobre as particularidades e os elementos que a envolvem, analise as assertivas a seguir.
I. Um elemento que serve de mediador da comunicação ou da cooperação entre componentes, realizando as chamadas de procedimentos (remotos), passagem de mensagem ou fluxo de dados é conhecido como componente.
II. Síncrona, conhecida como conector, é uma operação que atua como não bloqueante no envio de mensagens.
III. O conector media a comunicação entre componentes, realiza chamadas remotas e passagem de mensagem entre processos.
IV. Componente faz parte de uma arquitetura de comunicação, atuando com conectores.
Quais estão corretas?
Selecione a resposta:
A.Apenas I e IV.
B.Apenas II e III.
C.Apenas III e IV.
D.Apenas I e III.
E.Apenas II.

✅ A alternativa correta é: C


#### Questão 4
A comunicação em sistemas distribuídos ocorre por troca de mensagens, em que há alguns mecanismos para que essas mensagens possam ser trocadas. Existem alguns métodos de comunicação entre processos que realizam a troca de mensagens. Sobre esses métodos, marque V para verdadeiro e F para falso.
( ) Na comunicação síncrona bloqueante, o seu destino (send) aguarda até que a mensagem chegue ao seu receptor, e a origem (receive) aguarda até que a mensagem fique disponível.
( ) Na comunicação assíncrona não bloqueante, as mensagens podem ser enviadas uma após a outra.
( ) A comunicação por portas não ocorre por meio de regras padronizadas do modelo OSI e não utiliza protocolos.
( ) A comunicação por grupo multicast é um paradigma de comunicação indireta. Todos os processos pertencentes a um determinado grupo recebem mensagens, mas não reconhecem a identidade do destinatário.
Feito isso, assinale a alternativa que apresenta a sequência correta.
Selecione a resposta:
A.F, F, V, V.
B.F, V, F, V.
C.V, V, F, V.
D.V, F, V, F.
E.F, F, F, V.

✅ A alternativa correta é: C


#### Questão 5
A comunicação entre processos pode ser realizada por meio de alguns métodos. Um deles é mecanismo de serviço de transporte utilizado para a comunicação entre processos em um sistema distribuído, sendo gerenciados pela camada de protocolos de transporte, e utilizam as funcionalidades de comunicação TCP/IP.
Essa comunicação é a:
Selecione a resposta:
A.cliente-servidor.
B.por sockete.
C.por memória compartilhada.
D.por middleware.
E.por sincronização.

✅ A alternativa correta é: B


## Na prática

Os sistemas distribuídos têm diversas aplicações, desde as mais simples, realizando operações essenciais, até as mais complexas, em que temos exemplos de sistemas computacionais em rede se comunicando, trocando informações e interações entre processos.

Neste Na Prática, conheça um estudo de caso com base no esboço de projeto que João, funcionário de uma empresa de TI, organizou. Aprenda como funciona o processo de comunicação que ocorre com uma simples aplicação facilmente encontrada em computadores: a calculadora. Observe como o projeto montado por João mostrou a comunicação de sistemas distribuídos.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/a6c5e763-75cc-422e-adfc-69ee7e336eef/d611c505-1ff3-4dd7-8a7b-2a2d274c2c7f.png)

​​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja as sugestões do professor:

Sistemas distribuídos
Leia mais sobre definições e conceitos de sistemas distribuídos do ponto de vista do professor Dr. Francisco Isidro Massetto, da Universidade Federal do ABC. Após a leitura, você compreenderá sobre as características de comunicação e de sincronização entre processos.
[Mais](http://professor.ufabc.edu.br/~francisco.massetto/sd/01-Aula1-Intro.pdf)

Sistemas distribuídos
Leia mais sobre definições e conceitos de sistemas distribuídos do ponto de vista do professor Dr. Francisco Isidro Massetto, da Universidade Federal do ABC. Após a leitura, você compreenderá sobre as características de comunicação e de sincronização entre processos.
[Mais](http://professor.ufabc.edu.br/~francisco.massetto/sd/01-Aula1-Intro.pdf)

Modelo OSI e TCP/IP: como funciona o processo de comunicação em redes | Redes Brasil
Assista ao vídeo da empresa Redes Brasil, que trata sobre o modelo OSI e TCP/IP, e veja como funciona o processo de comunicação em redes entre dois hosts.
[Mais](https://www.youtube.com/embed/oz8gvGIUKFw)

Escalonamento de processos não preemptivos: um modelo de simulação
Faça o download da pesquisa que tem a finalidade de construir um modelo de simulação que demonstra o comportamento do escalonador First-in First-out em cenários com um, dois e três processadores, com processos de duração aleatória.
[Mais](https://atenaeditora.com.br/post-artigo/8714)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

COULOURIS, G.; DOLLIMORE, J.; KINDBERG, T. Distributed systems: concepts and design. 4.
ed. Boston: Addison-Wesley, 2005.

COULOURIS, G.; DOLLIMORE, J.; KINDBERG, T. Sistemas distribuídos: conceitos e projetos.
5.ed. Porto Alegre: Bookman, 2013.

JORGE10INFRC. Modelo OSI, modelo TCP/IP. [S. l.], 2020. Disponível em:
https://sites.google.com/site/jorge10infrc/sistema-osi-1. Acesso em: 16 jul. 2020.

MACHADO, F. B.; MAIA, L. Arquitetura de sistemas operacionais: incluindo exercícios com o
simulador Sosim e questões do Enade. 5. ed. São Paulo: LTC, 2013a.

MACHADO, F. B.; MAIA, L. P. Fundamentos de sistemas operacionais. São Paulo: LTC,
2013b.

TANENBAUM, A. S. Sistemas operacionais: projeto e implementação. 3. ed. Porto Alegre:
Bookman, 2008.

TANENBAUM, A. S.; BOS, H. Sistemas operacionais modernos. 4. ed. São Paulo: Pearson,
2016.

TANENBAUM, A. S.; STEEN, M. V. Sistemas distribuídos: princípios e paradigmas. 2. ed. São
Paulo: Pearson, 2007.

TEL, G. Introduction to distributed algorithms. 2. ed. Cambridge: Universidade de Cambridge,2001.

Banco de imagens Shutterstock.
SAGAH, 2020.
