## Apresentação

No processo de desenvolvimento de qualquer software, é essencial para o sucesso do projeto a definição de uma arquitetura sólida que permita o desenvolvimento, a manutenção e a evolução do programa de forma adequada. Em Sistemas Operacionais, a definição da sua estrutura básica é ainda mais importante, visto o impacto que a arquitetura tem tanto no sistema operacional quanto no software que será executado.

De forma geral, existem alguns modelos arquiteturais que são seguidos no desenvolvimento de sistemas operacionais, dos quais três se destacam: arquitetura monolítica, em que todas as partes do sistema operacional podem interagir diretamente entre si; arquitetura em camadas, em que há uma definição mais clara de quais componentes podem trocar informações diretamente; e arquitetura de micronúcleo ou microkernel, que visa minimizar a quantidade de código do sistema operacional que precisa rodar com alto privilégio na máquina. A maioria dos sistemas operacionais existentes aderem a algum desses modelos, seja seguindo à risca uma das arquiteturas, seja de forma híbrida, mesclando as melhores propriedades de cada uma delas.

Nesta Unidade de Aprendizagem, você vai aprender as características da arquitetura monolítica em camada e de micronúcleo. Também será capaz de diferenciar cada um dos modelos e discutir suas vantagens e desvantagens.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Explicar a arquitetura monolítica de um sistema operacional.
- Identificar a abordagem de arquitetura em camadas de um sistema operacional.
- Discutir a arquitetura de um sistema operacional micronúcleo.


## Desafio

O desenvolvimento de qualquer software requer um planejamento bem feito, com questões arquiteturais definidas de acordo com os requisitos do sistema. Os sistemas operacionais têm um vasto conjunto de requisitos em comum, devido à sua função principal de gerenciar o hardware do computador e a execução de aplicativos nele. Apesar disso, esse tipo de software tem requisitos ligados ao hardware, ao ambiente de execução e ao tipo de aplicações que nele serão executadas, o que gera diferenças entre os sistemas disponíveis.  

Considere a seguinte situação:

![](https://statics-marketplace.plataforma.grupoa.education/sagah/7dd43ca6-4800-413f-bc0b-d69e6af26eaf/3973962e-0926-4243-ba46-d30cefda49a0.png)

Diante do caso apresentado, indique em quais modelos arquiteturais você se baseou e quais são as características deles que fazem com que essa seja uma boa opção para o cenário descrito.

#### Padrão de resposta esperado
Uma abordagem híbrida entre o modelo monolítico e o micronúcleo seria uma opção interessante para o projeto desse sistema.

O computador limitado computacionalmente precisaria de uma arquitetura que prezasse pela performance, algo em que a arquitetura monolítica se destaca.

Caso fosse projetado um micronúcleo com as funcionalidades de sistema que não podem ser afetadas por falhas de outros módulos, e as outras partes do sistema fossem escritas ainda para rodar em espaço de núcleo, mas fora do núcleo do sistema em si o requisito da resistência a falhas seria atendido sem prejudicar tanto a performance.

Esse sistema seria inspirado na arquitetura usada no Windows NT, mas com implementação mais simplificada devido às restrições do hardware.

####  ✅ Resposta ao desafio:

Para atender simultaneamente aos requisitos de baixo poder computacional, alta performance/resposta rápida e resistência a falhas, a melhor abordagem é propor uma arquitetura híbrida, combinando características dos modelos Monolítico e Micronúcleo.
A escolha fundamenta-se nos seguintes aspectos:

Abordagem Monolítica (Foco em Performance): Como o computador veicular possui recursos e poder computacional limitados, o sistema operacional precisa ser altamente eficiente e rápido. O modelo monolítico se destaca justamente por sua performance, permitindo que os serviços rodem em um único espaço de endereço, o que evita a sobrecarga causada por trocas constantes de contexto (context switches).

Abordagem Micronúcleo (Foco em Resistência a Falhas): Sistemas puramente monolíticos são vulneráveis, pois a falha em um único módulo (como um driver) pode derrubar o sistema inteiro. Para mitigar isso, inspira-se no micronúcleo isolando funções críticas do sistema. As funcionalidades que não podem ser afetadas por falhas de outros módulos são separadas, garantindo robustez.

Características e Inspiração: Para não sacrificar o desempenho exigido pelo hardware limitado, os módulos protegidos e as demais partes do sistema são mantidos para rodar de forma otimizada (como uma implementação simplificada inspirada na arquitetura usada no Windows NT). Dessa forma, obtém-se a estabilidade e a resistência a falhas de um micronúcleo sem perder a velocidade de resposta essencial para o ambiente automotivo.


## Infográfico

Sistemas operacionais são geralmente software de grande porte com centenas de componentes interagindo entre si para prover o gerenciamento do computador, permitindo a execução de programas sem que haja interferências, garantindo a consistência das informações armazenadas e o bom funcionamento da máquina como um todo. Cada modelo de arquitetura define como esses módulos devem ser organizados e como deve ser permitida a comunicação entre eles.  

No Infográfico a seguir, você vai compreender a organização interna do sistema operacional de acordo com a arquitetura usada para estruturá-lo em seu projeto de desenvolvimento, por meio da interação entre as partes que compõem o sistema.

![](https://statics-marketplace.plataforma.grupoa.education/sagah/2ca7efd6-7cf1-4c4d-a30c-cabc341b0bef/396ac9d2-72f3-4c06-9aad-75f6ceecd2b2.png)


## Conteúdo do Livro

O modelo de arquitetura aplicado durante a construção de um sistema operacional irá definir a maneira com que seus componentes são organizados, podendo contribuir para sua performance, capacidade de expansão e facilidade de manutenção. A definição da arquitetura de um sistema é uma decisão importante, pois alterá-la num momento posterior seria sinônimo de reescrever praticamente todo o sistema.

A arquitetura monolítica é bastante livre praticamente não impõe nenhuma estrutura rígida para o sistema. Nesse caso, o sistema é apenas um conjunto de módulos, que podem livremente fazer referência uns aos outros. A arquitetura em camadas, por sua vez, define uma organização em que alguns módulos fazem parte de cada camada, e módulos de uma camada podem chamar diretamente apenas outros módulos da camada imediatamente inferior. Por fim, a arquitetura de micronúcleo isola as responsabilidades que não são essenciais para o gerenciamento do computador para processos à parte, que não fazem parte do núcleo do sistema, minimizando o risco de que, em caso de falhas, todo o sistema pare de funcionar.

No trecho da obra Sistemas Operacionais: Projeto e Implementação, você vai aprender mais sobre os sistemas monolíticos em camadas e o modelo cliente-servidor, usado no desenvolvimento de sistemas que seguem a arquitetura de micronúcleo.


## Dica do Professor

Cada modelo de arquitetura existente para a organização e estruturação de sistemas operacionais possui um conjunto de vantagens que pode ser explorada por seus projetistas, assim como desvantagens que devem ser mitigadas. Além dos profissionais que trabalham na criação dos sistemas operacionais, conhecer essas características das arquiteturas é importante para que profissionais de TI possam tomar decisões acertadas na escolha de sistemas operacionais para situações distintas.

Nesta Dica do Professor, veja as principais vantagens e desvantagens de sistemas implementados seguindo o modelo monolítico, em camadas e de micronúcleo.


## Exercícios

#### Questão 1
Sistema monolíticos são caracterizados por não impor uma estrutura fixa para seus componentes, sendo o sistema um grande conjunto de módulos, sem regras que limitem a comunicação entre eles. Sobre a execução de sistemas monolíticos, assinale a alternativa correta:​​​​​​​
Selecione a resposta:
A.Todo o sistema é executado em Espaço de Usuário, assim como suas aplicações.
B.Todo o sistema é executado em Espaço de Núcleo, assim como suas aplicações.
C.Parte do sistema e das aplicações são executadas em Espaço de Núcleo, o resto do sistema em Espaço de Usuário.
D.O sistema é executado em Espaço de Núcleo, mas suas aplicações são executadas em Espaço de Usuário
E.O sistema é executado em Espaço de Usuário, mas suas aplicações são executadas em Espaço de Núcleo.

✅ A alternativa correta é: D


#### Questão 2
Ao definir uma arquitetura em camadas, os projetistas de um sistema operacional optam por uma organização mais restrita, com uma definição clara de quais módulos podem ter acesso direto aos outros. Caso uma aplicação necessite de um serviço, de uma funcionalidade do sistema a qual não tem acesso direto, ela deve solicitar o serviço por meio de uma chamada para algum dos módulos com os quais ela pode se comunicar, que irá encaminhar para as camadas inferiores e o processo se repetirá até que a chamada chegue na funcionalidade desejada. Sobre este mecanismo em sistemas em camadas, assinale a alternativa correta:​​​​​​​
Selecione a resposta:
A.Sistemas em camadas são mais lentos, devido à necessidade de repassar as chamadas entre as camadas.
B.Sistemas em camadas são mais difíceis de evoluir, devido ao excesso de código.
C.Sistemas em camadas são mais difíceis de manter, devido à estrutura rígida aplicada.
D.Sistemas em camadas são mais resilientes, pois pouco código executa em espaço de núcleo.
E.Sistemas em camadas são mais simples pois são baseados em micronúcleo.

✅ A alternativa correta é: A


#### Questão 3
A arquitetura de micronúcleo orienta a organização do sistema operacional de forma que apenas as funções de mais baixo nível sejam executadas em Espaço de Núcleo, minimizando o risco de erros críticos durante a execução do sistema. Sobre o relacionamento entre arquitetura de micronúcleo e o modelo cliente-servidor, assinale a alternativa correta:​​​​​​​
Selecione a resposta:
A.O modelo cliente-servidor define que o sistema operacional de micronúcleo deve oferecer chamadas de sistema para acesso às suas funcionalidades internas.
B.Sistemas de micronúcleo usam processos servidores executando em Espaço de Usuário como intermediários para as funcionalidades do sistema. As aplicações são os processos clientes.
C.Sistemas de micronúcleo usam processos servidores executando em Espaço de Núcleo como intermediários para as funcionalidades do sistema. As aplicações são os processos clientes.
D.Sistemas de micronúcleo usam processos clientes executando em Espaço de Usuário como intermediários para as funcionalidades do sistema. As aplicações são os processos servidores.
E.Sistemas de micronúcleo usam processos clientes executando em Espaço de Núcleo como intermediários para as funcionalidades do sistema. As aplicações são os processos servidores.

✅ A alternativa correta é: B

#### Questão 4
Sistemas operacionais de grande porte e com múltiplos usos, como Windows e Linux, executam uma grande quantidade de código em Espaço de Núcleo, uma característica de sistemas monolíticos. Assinale a alternativa que melhor define o motivo dessa decisão de projeto nesses sistemas.​​​​​​​
Selecione a resposta:
A.Com o passar do tempo não se consegue manter e evoluir arquiteturas mais rígidas, migrando os sistemas para a arquitetura monolítica.
B.Funções executando em Espaço de Núcleo são mais seguras, logo o sistema se beneficia por ter menos aplicações executando em Espaço de Usuário.
C.Mesmo com uma redução da performance, as vantagens de ter todo o sistema operacional executando em Espaço de Núcleo compensam a migração.
D.Sistemas modernos possuem um número maior de funções, então o risco de uma função executando em Espaço de Usuário quebrar todo o sistema é muito grande.
E.Com mais funções executando em Espaço de Núcleo, a performance do sistema tende a ser melhor, por necessitar de menos comunicação entre processos.

✅ A alternativa correta é: E


#### Questão 5
Considere um sistema operacional que deve permitir a integração de várias peças de hardware de diferentes fabricantes, inclusive componentes que nem existam durante o desenvolvimento do sistema. O ambiente de execução desse sistema não tem uma necessidade de performance ótima, mas é necessário que o sistema seja bastante resistente a erros, não falhando devido a um problema em uma aplicação ou driver isolado. A partir do cenário descrito, assinale a alternativa que descreve o modelo arquitetural mais adequado para um novo sistema que será desenvolvido para esse ambiente.
Selecione a resposta:
A.Monolítico.
B.Em Camadas.
C.Micronúcleo.
D.Máquina Virtual.
E.Híbrido entre Monolítico e Em Camadas.

✅ A alternativa correta é: C


## Na prática

É difícil encontrar sistemas operacionais reais que sejam totalmente aderentes a apenas um dos possíveis modelos arquiteturais disponíveis. O mais comum é que os projetistas desses sistemas busquem mesclar características positivas de cada um desses modelos para chegar a uma solução ideal para as necessidades do sistema operacional que estão criando.  

Neste Na Prática, você verá como se deu a evolução da arquitetura do sistema operacional Windows.

![](https://statics-marketplace.plataforma.grupoa.education/sagah/94d405b8-f67c-46f6-9027-219470c5669e/35edb391-4982-4cc8-af57-8543ff6bc5f1.png)



## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Sistemas Operacionais – Tipos e Estruturas de SO
Acesse esta videoaula do curso de Sistemas Operacionais da Universidade Virtual do Estado de São Paulo, que apresenta explicação detalhada do modelo monolítico, de microkernel e em camadas.
[Mais](https://www.youtube.com/embed/_J4CVHgXQ1c)

Projeto de Sistemas Operacionais
A seção 8.2.2 do Livro Princípios Básicos de Arquitetura e Organização de Computadores (Null e Lobur) possui um resumo sobre os modelos de arquitetura geralmente usados em sistemas operacionais, incluindo alguns exemplos de sistemas reais que seguem as arquiteturas de microkernel e monolítica. Acesse para saber mais.
[Mais](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=69202089&tokenId=bd9a5477-3161-4803-8fd3-beb8011166aa)

Sistema operacional monolítico e em camadas
Clique para assistir a este vídeo, que apresenta explicação sobre o conceito de núcleos baseados em arquitetura monolítica e em camadas.
[Mais](https://www.youtube.com/embed/SXTZVHr13hQ)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

DEITEL, H. M.; DEITEL, P. J.; CHOFFNES, D. R. Sistemas operacionais. 3. ed. São Paulo: PrenticeHall do Brasil, 2005.

PAPADIMITRIOU, S; MOUSSIADES, L. A Comparative Evaluation of Core Kernel Features of theRecent Linux, FreeBSD, Solaris and Windows Operating Systems. Proceedings of the WorldCongress on Engineering (WCE 2016), IAENG, Londres, 2016.

RAM, M.; RAJKUMAR, B.; KRISHNAN, V.; BALAJI, S.; RAO, S. A Microkernel Based Operating
System for PARAM 9000. Proceedings of the Fourth International Conference on Advanced
Computing (ADCOMP'96), Tata McGraw Hill Publications, Bangalore - India, 1996. 
Disponível em:http://www.cloudbus.org/papers/mkernel.pdf. Acessado em: 03 jan. 2020.

TANENBAUM, A; WOODHULL, A. Sistemas Operacionais: projeto e implementação. Porto Alegre:Bookman, 2008.

TEIXEIRA, M. A. Sistemas Operacionais: Estrutura de Sistemas Operacionais. Disponível em:
http://ctd.ifsp.edu.br/~marcio.andrey/images/estrutura_so-ifsp-catanduva.pdf. Acessado em:03 jan. 2020. 

Windows NT. Disponível em: https://commons.wikimedia.org/wiki/File:NT4_logo.svg. Acesso em 15 jan. 2020.

Banco de imagens Shutterstock.
SAGAH, 2020.

