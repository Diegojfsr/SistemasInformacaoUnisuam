## Apresentação

Mecanismos de paginação de memória resolvem o problema da escassez de memória principal no computador, estendendo o espaço de endereçamento além da capacidade instalada na máquina. A paginação, no entanto, é uma abordagem limitada por oferecer um único espaço de endereçamento linear. Isso pode causar problemas quando programas crescem na memória e precisam alocar muito mais espaço do que outros programas em execução.

Os mecanismos de segmentação visam a permitir a existência de múltiplos espaços de endereçamento que possam crescer de forma independente, sem interferir ou sofrer interferência dos espaços de outros processos. O uso de segmentação também pode fazer com que a memória disponível seja usada de forma mais eficiente, pois é possível contar com propriedades de proteção de memória que permitem o compartilhamento seguro de segmentos de memória para usos específicos.

Nesta Unidade de Aprendizagem, você aprenderá o conceito de segmentação de memória, como as abordagens desse tipo funcionam e como elas se diferenciam do modelo de paginação de memória. Com a implementação de segmentação pura, você será apresentado ao problema da fragmentação de memória.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Explicar o funcionamento de segmentação.
- Comparar paginação e segmentação.
- Discutir a implementação de segmentação pura.

## Desafio

A aplicação de mecanismos de memória virtual, como a paginação e a segmentação, exige que, a cada leitura de memória efetuada pelo processador, um tipo de tradução seja realizado da posição de memória virtual indicada pela instrução que o processador está executando para a posição na memória física onde os dados referenciados pela memória virtual realmente estão presentes.

Na segmentação, cada posição de memória pode ser referenciada a partir de um par de informações: o número do segmento X e a posição de memória dentro do segmento Y. Ao receber o valor X,Y, o sistema deve verificar se o segmento X está carregado em memória. Se o segmento ainda não está disponível, ele deve carregá-lo (a depender do nível de fragmentação, antes de carregar pode ser necessário efetuar uma compactação).

Com o segmento X na memória, a tradução pode ocorrer para obter a posição real do dado a ser acessado. Obtém-se a posição base do segmento X na memória principal, e é somado Y a esse valor. O resultado desse processo é a posição na memória física relativa ao par X,Y informado, e com esse valor é possível obter os dados e retorná-los ao processador para que o processo continue a sua execução.  
  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/25b4da6b-e742-485c-bc96-985004aef324/98b59bfd-961b-4289-add1-0a2131de9eb7.jpg)

A partir das informações acima, responda aos seguintes questionamentos:

a) Se o processador tentar acessar a posição 256 do segmento 2, qual posição na memória principal precisaria ser acessada?

b) Se o processador tentar acessar a posição 4224 do segmento 1, qual posição na memória principal precisaria ser acessada? O acesso a essa posição de memória teria sucesso? Explique a sua resposta.

c) Com base na observação do cenário descrito, explique por que os dados de um segmento precisam ser carregados completos e de forma contínua na memória principal.

#### Padrão de resposta esperado

a) A base para o segmento 2 será a posição 9216, a primeira que está livre, então, a posição 256 do segmento 2 será igual a 9216+256 = posição 9472 na memória principal.

b) Seguindo o mesmo raciocínio acima, a posição será 5504+4224 = 9728. O acesso não seria permitido. Isso se deve ao fato de que a posição 9728 não faz parte do segmento 1, que vai da posição 5504 até a posição 9215. Ao tentar acessar uma posição fora do segmento, o acesso deveria ser barrado e falhar, provavelmente lançando uma exceção.

c) Os cálculos efetuados para descobrir a posição de memória real são dependentes apenas do valor da posição base da memória principal onde o segmento está alocado e do deslocamento dentro do segmento. Se o segmento não estivesse alocado de forma contínua, essa conta iria resultar em uma posição errada.

####  ✅ Resposta ao desafio:

Com base no cenário apresentado e no padrão de resposta esperado, aqui estão as respostas detalhadas para cada um dos questionamentos:a) Se o processador tentar acessar a posição 256 do segmento 2, qual posição na memória principal precisaria ser acessada?Resposta: A base para o segmento 2 inicia-se na posição 9216 (primeira posição livre após os segmentos 1 e 3). Portanto, a posição 256 do segmento 2 corresponderá à seguinte posição na memória principal:$$\text{Posição} = 9216 + 256 = 9472$$Dessa forma, a posição 9472 na memória principal precisaria ser acessada.   b) Se o processador tentar acessar a posição 4224 do segmento 1, qual posição na memória principal precisaria ser acessada? O acesso a essa posição de memória teria sucesso? Explique a sua resposta.   Resposta: Calculando com base na posição base do segmento 1 (5504), teríamos:$$\text{Posição} = 5504 + 4224 = 9728$$O acesso não teria sucesso. Isso ocorre porque o segmento 1 ocupa o espaço de endereçamento da memória física que vai da posição 5504 até a 9215 (conforme o limite dos segmentos anteriores que terminavam em 9215). Como a posição 9728 está fora dos limites alocados para o segmento 1, o acesso deve ser bloqueado pelo sistema de proteção, resultando em uma falha ou exceção de violação de segmento.c) Com base na observação do cenário descrito, explique por que os dados de um segmento precisam ser carregados completos e de forma contínua na memória principal.Resposta: Os cálculos de tradução de endereços na segmentação pura dependem exclusivamente de uma operação aritmética simples: somar o deslocamento solicitado (Y) diretamente à posição base do segmento na memória principal (\text{Base} + Y). Se o segmento estivesse fragmentado ou não fosse contínuo, essa conta linear resultaria em uma posição física incorreta, corrompendo os dados ou apontando para áreas pertencentes a outros processos.


## Infográfico

A fragmentação de memória ocorre quando lacunas vão sendo acumuladas na memória principal na medida em que os segmentos, que têm tamanho variável, são carregados, removidos e substituídos. Em casos extremos, a memória principal pode ter espaço suficiente para carregar um segmento, mas não ser capaz de suportá-lo, pois esse espaço é não contínuo, ou seja, está fragmentado. Nessa situação, é necessário executar rotinas de desfragmentação da memória, como a compactação, fazendo movimentações na memória para que haja espaço contínuo livre na memória principal.

No Infográfico a seguir, você poderá compreender visualmente o que é a fragmentação de memória, em que situação ela ocorre e qual procedimento pode ser tomado para resolver esse problema.

  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/3f82acff-da91-44af-a0d3-636517c569f2/a83fde65-9161-43ba-9651-5dff56eb7153.jpg)

​​​​
## Conteúdo do Livro

A segmentação de memória é uma abordagem para lidar com a memória virtual, que permite que existam vários espaços de endereçamento separados. Essa implementação de memória virtual, na qual cada programa tem conhecimento de seu próprio espaço de endereçamento, é muito útil para o desenvolvimento de sistemas mais complexos.

Como cada segmento tem a sua própria posição zero, e toda a sua memória é indexada a partir dessa posição, os programas podem crescer sem causar problemas para outros dados que são armazenados na memória do computador. Isso também permite que o programa seja carregado em qualquer posição de memória inicial fisicamente.

Leia o capítulo Memória virtual: segmentação, da obra Sistemas Operacionais, no qual você irá aprender o funcionamento dos mecanismos de segmentação de memória e entenderá como ele se difere das estratégias de paginação.

  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/82aafb67-84e2-4851-9dcd-5bbd783c99d6/3ed49473-b232-4e90-9062-c252b19cc946.jpg)


## Dica do Professor

Apesar de tanto a segmentação como a paginação serem abordagens para implementação de memória virtual em sistemas operacionais, cada uma delas contém motivações diferentes, e, dessa forma, são implementadas seguindo abordagens distintas. É possível usar ambos os mecanismos em conjunto, de forma que os objetivos tanto da paginação como da memória virtual sejam atendidos no sistema. Inclusive, processadores, como os Intel da família Intel64 e IA-32, dão suporte via hardware para abordagens de uso misto de paginação com segmentação.

Nesta Dica do Professor, você poderá conferir as principais diferenças existentes entre segmentação e paginação de memória. Serão apresentadas questões técnicas e práticas do ponto de vista de programadores, assim como princípios que orientaram a criação de cada um desses mecanismos.


## Exercícios

#### Questão 1
A carga de trabalho de alguns tipos de programa faz com que sua alocação de memória seja imprevisível em tempo de desenvolvimento. Dependendo da entrada repassada para o programa, em uma execução pode ser necessário que a estrutura X tenha uma quantidade de memória alocada maior que a estrutura Y, mas outra entrada pode exigir do mesmo programa exatamente o contrário, ou seja, mais memória para a estrutura Y do que para a estrutura X.
Assinale a alternativa que explica corretamente como a segmentação permite que um programa tenha estruturas em memória que possam crescer de forma independente, sem causar interferência umas nas outras:​​​​​​
Selecione a resposta:
A. A segmentação permite que a memória seja dividida em partes de tamanhos iguais, que podem ser alocadas individualmente.
B. A segmentação permite que existam vários espaços de endereçamento de tamanhos diferentes e independentes.
C. A segmentação permite que um único espaço de endereçamento seja compartilhado por várias estruturas.
D. A segmentação permite a criação de múltiplos espaços de endereçamento, todos com o mesmo tamanho, porém independentes.
E. A segmentação evita a ocorrência de fragmentação externa na medida em que os segmentos são carregados na memória.

✅ A alternativa correta é: B

#### Questão 2
Bibliotecas compartilhadas são muito usadas para permitir a modularização de sistemas operacionais e aplicações. Elas permitem a evolução do software sem a necessidade de uma recompilação completa, por exemplo. Mesmo sistemas operacionais que não têm suporte à segmentação implementam alternativas para permitir o uso do conceito de bibliotecas compartilhadas.
Assinale a alternativa que descreve corretamente como o uso de segmentação otimiza o uso de bibliotecas compartilhadas:​​​​​
Selecione a resposta:
A. Espaços de endereçamento independentes, cada um com uma base zero, permitem que a biblioteca compartilhada seja carregada apenas uma vez na memória.
B. Bibliotecas compartilhadas podem ser carregadas em fragmentos separados, permitindo uma maior distribuição do código na memória principal.
C. A memória unidimensional oferecida pelo modelo de segmentação permite que a biblioteca compartilhada tenha endereços fixos sem a necessidade de alteração para uso por outros processos.
D. A disponibilidade de mecanismos de proteção no modelo de segmentação permite que a biblioteca compartilhada tenha endereços fixos sem a necessidade de alteração para uso por outros processos.
E. O espaço de endereçamento único, com apenas uma base zero, permite que a biblioteca compartilhada seja carregada apenas uma vez na memória, sendo essa mesma instância usada por todos os processos.

✅ A alternativa correta é: A


#### Questão 3
Paginação e segmentação são abordagens diferentes para a implementação de memória virtual, cada uma com seus objetivos, vantagens e desvantagens. Apesar do mecanismo de paginação ser mais presente nos principais sistemas operacionais contemporâneos, as ideias gerais do mecanismo de segmentação de memória também são aplicadas.
Assinale a alternativa correta sobre as características dos mecanismos de paginação e segmentação:​​​​​​
Selecione a resposta:
A. Ao contrário da paginação, na segmentação, não é possível definir níveis de proteção distintos para cada segmento.
B. Ao contrário da segmentação, a paginação exige que o desenvolvedor projete o sistema ciente de que há um mecanismo de paginação.
C. A segmentação não permite que cada segmento cresça de forma independente, sem interferir em outros segmentos.
D. A paginação exige que páginas sequenciais sejam carregadas de forma contínua na memória principal.
E. Tanto a paginação como a segmentação permitem que o espaço de endereçamento total seja maior que a memória principal disponível.

✅ A alternativa correta é: E


#### Questão 4
A fragmentação de memória é um problema sério, que pode causar redução de performance do sistema ou impossibilitar o seu uso. Identificar a sua ocorrência nem sempre é uma tarefa simples.
Assinale a alternativa que contém a afirmação correta sobre fragmentação de memória:​​​​​​​
Selecione a resposta:
A. Não é possível ocorrer fragmentação de memória com o uso de paginação, apenas com segmentação.
B. A fragmentação externa, quando não tratada, tem sintomas similares à falta de memória principal disponível.
C. A fragmentação interna é o principal tipo de fragmentação possível com o uso de segmentação.
D. A fragmentação não ocorre se há memória principal disponível no sistema.
E. A fragmentação interna tem resolução mais simples do que a externa.

✅ A alternativa correta é: B


#### Questão 5
Apesar de ser um problema sério, a fragmentação de memória tem na compactação da memória uma solução relativamente simples, apesar de computacionalmente cara.
Assinale a alternativa correta sobre o uso de compactação para resolver a fragmentação externa de memória.​​​​​​​
Selecione a resposta:
A. A compactação reduz o tamanho de cada segmento, liberando mais espaço livre na memória principal.
B. A compactação escolhe o segmento menos usado para ser removido da memória principal.
C. A compactação move os segmentos na memória principal para aumentar o espaço livre contínuo.
D. A compactação transfere dados entre os segmentos, para aumentar o espaço livre na memória.
E. A compactação executa um algoritmo de substituição de segmento quando não há espaço livre contínuo.

✅ A alternativa correta é: C

## Na prática

Problemas relacionados à fragmentação de memória tendem a ser difíceis de se identificar. Um sistema sofrendo com alto nível de fragmentação terá sintomas similares ao de um computador, no qual não há memória principal disponível. No entanto, o sistema pode indicar que há muita memória livre, induzindo o profissional, que está analisando o problema, ao erro de acreditar que não há nada de errado com a memória. Nesse caso, apesar de haver memória disponível, ela não é contínua, e não poderá ser alocada para um processo caso seja solicitado um espaço maior do que o maior bloco de memória livre contínuo.

Na Prática, você verá um caso real de análise de um problema de fragmentação de memória em um servidor de grande porte focado na disponibilização de um serviço de banco de dados.  
  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/76cbb061-0278-4ee1-8e3d-5b0d5e99693a/3a98e7a5-404d-470d-a51d-e58bc5af6697.jpg)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Gerência de memória
Este vídeo apresenta três estratégias para alocar um bloco de memória em um sistema baseado em uma abordagem que permita a ocorrência de fragmentação externa, como a segmentação. Cada uma das estratégias discutidas tenta minimizar os efeitos da fragmentação externa de uma forma diferente.
[Mais](https://www.youtube.com/embed/Q2yRR1SmdK4)

De volta ao passado: memória virtual com segmentação para máquinas com memória RAM “infinita”
Leia a dissertação de mestrado de Lauri P. Laux Jr., com informações sobre os mecanismos de paginação e segmentação. Nela, é realizada uma comparação sobre o uso de ambas as abordagens em computadores com enorme quantidade de memória principal instalada para a realidade atual, mas que pode se tornar viável no futuro, e, por fim, é proposto o uso de segmentação para a melhora da performance do sistema nessa situação.
[Mais](https://www.inf.ufpr.br/hexsel/dissLauri.pdf)

Segmentação e paginação combinada com segmentação
Nestas seções do livro Princípios Básicos de Arquitetura e Organização de Computadores, você poderá aprender mais detalhes sobre o mecanismo de segmentação, assim como de sua implementação em conjunto ao uso de paginação.
[Mais](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=69202073&tokenId=c802cd97-11e3-419b-99b1-4a793a2018ea)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

DEITEL, H. M.; DEITEL, P. J.; CHOFFNES, D. R. Sistemas operacionais. 3. ed. São Paulo:
Prentice Hall do Brasil, 2005.

LAUX JR., L. P.; HEXSEL, R. A. Back to the Past: When Segmentation Is More Efficient Than
Paging. Anais do XVII Workshop em Desempenho de Sistemas Computacionais e de
Comunicação, 2018.

SAVVINOV, N. Memory Fragmentation: the silente performance killer. Oracle Diagnostician. 14 de Outubro de 2019. Disponível em: <https://savvinov.com/2019/10/14/memory-fragmentation-the-silent-performance-killer/>. Acesso em: 22 jan. 2020.

TANENBAUM, A; WOODHULL, A. Sistemas Operacionais: projeto e implementação. Porto
Alegre: Bookman, 2008.

Banco de imagens Shutterstock.
SAGAH, 2020.

