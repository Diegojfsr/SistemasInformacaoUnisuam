## Apresentação

A abordagem de memória virtual estende uma memória principal de tamanho limitado para um espaço maior utilizando a memória secundária disponível no computador. A performance do mecanismo de paginação usado para permitir o uso de memória virtual será tão bom quanto o algoritmo usado para substituir as páginas na memória principal. Isso irá ocorrer sempre que o espaço livre se esgota na memória principal e uma aplicação em execução precisa de uma página que ainda não está carregada.

Vários algoritmos existem para essa finalidade, cada um com seus pontos fortes e fracos. Um algoritmo ótimo, que removesse a página que levará mais tempo para ser acessada novamente, é conhecido; no entanto, não pode ser implementado, pois não é possível identificar com precisão quando uma página será necessária novamente para um programa. Outros algoritmos, então, foram desenvolvidos e, ainda que não sejam perfeitos, conseguem aproveitar características de como os programas são executados para identificar as páginas com maior probabilidade de serem usadas no futuro próximo, dando preferência para remover as páginas em que essa chance é menor.

Esses algoritmos usados para a substituição de página de memória virtual em sistemas operacionais encontram uso em outros domínios em que é usado algum tipo de memória cache ou hierarquia de memórias. Um exemplo é a cache de proxies para servidores Web, usados para minimizar a carga em serviços Web muito solicitados. Esse tipo de sistema usa algoritmos derivados dos mesmos algoritmos que são aplicados para substituição de página de memória virtual, como o algoritmo de substituição da página menos recentemente usada (LRU: Least Recently Used).

Nesta Unidade de Aprendizagem, você vai entender o princípio de um algoritmo ótimo para a seleção de página a ser substituída e qual o motivo que o faz ser inviável na prática. Além disso, você aprenderá o funcionamento de algoritmos que podem ser usados no mundo real para esse objetivo, como o algoritmo de substituição de página não usada recentemente (NRU — Not Recently Used), o algoritmo baseado no conceito de fila FIFO (First-In, First-Out, ou primeiro a entrar, primeiro a sair), o algoritmo da segunda chance, o algoritmo do relógio e o algoritmo LRU.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Analisar o funcionamento dos algoritmos de substituição de páginas Ótimo (OPT) e Not Recently Used (NRU).
- Descrever os algoritmos First-In, First-Out (FIFO) e Segunda Chance. 
- Comparar o algoritmo de substituição de páginas do Relógio (Clock) com o algoritmo Least Recently Used (LRU).


## Desafio
O mecanismo de paginação pode ser considerado um caso de uso de cache, aplicado para estender a quantidade de memória disponível para os programas, efetivamente usando a hierarquia de memórias de um computador para esse fim. Resumidamente, pode-se definir que uma cache é qualquer mecanismo que tente armazenar dados de forma volátil para permitir que futuros acessos ao dado sejam mais rápidos do que o acesso direto à memória durável, em que o dado se encontra permanentemente. 

Os algoritmos usados para paginação de memória geralmente podem ser aplicados para outros problemas de cache, como cache do sistema de arquivos do sistema operacional. Outra área em que mecanismos de cache são vastamente usados é na Web, principalmente devido à alta latência existente ao necessitar acessar um servidor para obter arquivos e dados em geral. Nessa área, é recorrente o uso dos algoritmos mais comumente usados para substituição de páginas em memória virtual, com pequenas adaptações para funcionarem com arquivos.

  
![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/e6f9fc1c-f82f-471c-98dc-118935a2e14d/780fb68d-e643-4a17-8394-1688c437cdb2.png)

Com essas informações:

Escolha um algoritmo de substituição que seja adequado para o cenário descrito para o browser. Justifique sua escolha, comparando o algoritmo escolhido com pelo menos outro algoritmo de substituição para cada ponto apresentado em seu argumento.

#### Padrão de resposta esperado

O algoritmo LRU é adequado para a situação descrita. Ele precisa de mais memória do que outros algoritmos, como FIFO, NRU ou segunda chance, mas isso não é um problema, dado que os computadores-alvo do browser têm muita memória, conforme descrito no cenário.

Sua principal vantagem é conseguir manter arquivos usados mais recentemente, substituindo os arquivos que foram acessados menos recentemente, ao contrário do FIFO, que substitui simplesmente o arquivo mais antigo da cache. Essa característica do LRU aumenta a chance de que arquivos que são mais usados estejam na cache quando forem solicitados, evitando um lento download do arquivo pela Internet.


####  ✅ Resposta ao desafio:

Escolha do Algoritmo e Justificativa
Para o cenário de um browser moderno que precisa gerenciar uma cache de arquivos da Web (limitada a 1.000 itens) e que será executado em computadores com recursos abundantes de memória, o algoritmo mais adequado é o LRU (Least Recently Used - Menos Recentemente Usado).

Comparação e Argumentação
Consumo de Recursos vs. Restrições de Hardware:

LRU: Requer estruturas de dados adicionais (como listas duplamente encadeadas associadas a tabelas hash) para rastrear a ordem de acesso dos 1.000 arquivos, o que demanda um pouco mais de memória e processamento para atualização dos ponteiros a cada acesso.

FIFO (First-In, First-Out) / NRU / Segunda Chance: São algoritmos mais leves que consomem menos metadados e processamento de controle.

Justificativa: Como o enunciado destaca que o navegador rodará em computadores modernos com abundância de memória principal e secundária, o custo computacional e de memória extra do LRU é totalmente desprezível frente aos benefícios de desempenho.

Eficácia na Taxa de Acertos (Hit Rate) e Redução de Latência:

LRU: Substitui os arquivos que foram acessados há mais tempo no passado, baseando-se no princípio da localidade temporal (arquivos usados recentemente tendem a ser reutilizados em breve). Isso maximiza a chance de reter arquivos populares ou frequentemente requisitados (como folhas de estilo, scripts e imagens recorrentes), evitando o custo alto de um novo download pela Internet.

FIFO: Descarta simplesmente o arquivo que entrou primeiro na cache, independentemente de ele ser acessado constantemente. Isso pode causar o fenômeno em que um arquivo altamente popular, porém antigo na cache, seja removido e precise ser baixado novamente da rede.

NRU / Segunda Chance: Usam aproximações baseadas em bits de referência (geralmente limpos ou resetados periodicamente por interrupções) para tentar adivinhar páginas não utilizadas recentemente. No entanto, o NRU possui uma granularidade grosseira (dividindo as páginas em categorias fixas) e a Segunda Chance pode sofrer com o efeito FIFO caso muitas páginas tenham o bit de acesso ativado. O LRU oferece uma precisão muito maior por ordenar estritamente o histórico temporal de uso, o que é ideal para o comportamento de navegação na Web, onde determinados recursos são reutilizados exaustivamente durante a sessão do usuário.

## Infográfico

O algoritmo da segunda chance é muito simples, mas tem alto custo ao ser implementado, devido à necessidade de movimentação da página da primeira para a última posição da fila, caso a primeira página da fila esteja marcada como lida. O algoritmo do relógio resolve esse problema, armazenando as páginas como uma lista circular e mantendo um ponteiro para indicar, nessa lista, quem é a página mais antiga. Seu nome se deve ao fato de que o ponteiro, ao navegar na lista, é equivalente ao ponteiro de um relógio analógico, avançando nas horas.  

No Infográfico a seguir, veja um exemplo do funcionamento do algoritmo do relógio e entenda a equivalência do seu resultado com a saída do algoritmo da segunda chance.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/8c366f67-def2-4067-bc77-e6f6b62280f4/94e64283-2645-4f01-a51a-1a94288d1639.png)

​​​​​
## Conteúdo do Livro
A memória virtual é um mecanismo fundamental dos sistemas operacionais para ampliar a capacidade aparente de memória disponível aos processos, permitindo que programas sejam executados mesmo quando seu espaço de endereçamento excede a capacidade da memória física. Para isso, o sistema operacional realiza o gerenciamento da memória principal e do armazenamento secundário, utilizando mecanismos como a paginação para organizar e movimentar as informações conforme a necessidade de execução dos processos (Tanenbaum; Bos, 2023).

Quando ocorre uma falta de página e não há quadros livres disponíveis, o sistema operacional precisa selecionar uma página que será retirada da memória para dar lugar à nova página. Essa decisão é realizada por meio de algoritmos de substituição de páginas, como Ótimo, NRU (Not Recently Used), FIFO (First-In, First-Out), Segunda Chance, Relógio e LRU (Least Recently Used). Cada estratégia utiliza diferentes critérios para selecionar a página candidata à substituição, buscando equilibrar eficiência, desempenho e custo de gerenciamento da memória (Silberschatz; Galvin; Gagne, 2021).

No capítulo Memória Virtual e algoritmos de substituição de páginas, base teórica desta Unidade de Aprendizagem, você vai compreender os fundamentos da memória virtual e seu papel no gerenciamento da memória dos sistemas operacionais, além de analisar o funcionamento dos algoritmos Ótimo e NRU, conhecer as estratégias FIFO e Segunda Chance e comparar o algoritmo do Relógio com o LRU. Ao longo do capítulo, serão apresentados exemplos e sequenciamentos que permitirão compreender como diferentes critérios influenciam a escolha das páginas a serem substituídas.

Boa Leitura.

## Dica do Professor

A fila é uma estrutura de dados muito utilizada em diversos algoritmos computacionais e em vários sistemas operacionais para escalonamento de processos e outras atividades. É possível propor também seu uso para efetuar a substituição de página em memória virtual, apesar de que, sem alterações, seu uso não resulta em um algoritmo interessante. Com algumas modificações no funcionamento de filas, no entanto, é possível chegar a algoritmos simples e com características mais interessantes para esse objetivo.

Nesta Dica do Professor, você irá aprender como o conceito puro de filas pode ser usado para selecionar a página a ser substituída na memória com o algoritmo FIFO e quais as limitações dessa abordagem. Depois, você conhecerá o algoritmo da segunda chance, que é baseado em fila, mas com modificações que tornam a seleção de páginas mais adequada para o modelo de funcionamento de memória virtual em computadores.

## Exercícios

#### Questão 1
O algoritmo de substituição de páginas FIFO, utilizando o conceito de filas, é simples de implementar e não requer uso excessivo de memória ou processamento. Seu resultado final é, no entanto, limitado por essa simplicidade, visto que o algoritmo não utiliza o padrão de acesso a páginas que já estão na memória para definir qual página será substituída quando ocorre falta de página.
Considere que há espaço na memória principal para manter 4 páginas em dado instante de tempo. As páginas são solicitadas na seguinte ordem: 9, 5, 9, 7, 6, 9, 6, 9, 1. Usando-se o algoritmo FIFO puro, assinale a alternativa que contém as páginas que estão na memória principal após essa sequência de solicitações.
Selecione a resposta:
A. 5, 7, 6, 1.
B. 7, 6, 9, 1.
C. 9, 6, 9, 1.
D. 5, 7, 9, 1.
E. 5, 6, 9, 1.

✅ A alternativa correta é: A


#### Questão 2
O algoritmo da segunda chance é uma evolução do algoritmo FIFO puro para seleção de página a ser substituída, usando pelo menos a informação de que a página foi ou não usada desde a última rodada de substituição. Sua implementação é ineficiente devido à necessidade de mover a página do início para o final da fila, caso a página tenha sido usada. O algoritmo do relógio tem o mesmo resultado do algoritmo da segunda chance, mas com uma performance melhor, por meio do uso de um ponteiro em vez da movimentação das páginas.
Assinale a alternativa que explica o uso do ponteiro no algoritmo do relógio.​​​​​​​
Selecione a resposta:
A. O ponteiro aponta sempre para a página a ser removida, tornando trivial a substituição da página que está sendo apontada. A página existente é removida, e a nova página passa a ser apontada pelo ponteiro.
B. O ponteiro aponta sempre para a página a ser removida, tornando trivial a substituição da página que está sendo apontada. A página existente é substituída pela nova página, e o ponteiro aponta para a próxima página.
C. Considerando a memória como uma lista circular, o ponteiro aponta para o início da lista. Ao iterar na lista devido ao uso das páginas, apenas o ponteiro se move para indicar qual é o novo início da lista.
D. Considerando a memória como uma lista circular, o ponteiro aponta para o final da lista. Ao iterar na lista devido ao uso das páginas, o ponteiro indica o destino da nova página.
E. Ao inserir uma nova página na memória, é criado um ponteiro para indicar a sua posição. Esse ponteiro é mantido fixo para acesso imediato a cada uma das páginas.

✅ A alternativa correta é: C

#### Questão 3
O algoritmo LRU usa a informação de qual página foi menos recentemente utilizada para poder efetuar a decisão da página que será substituída. Dessa forma, espera-se que páginas que recentemente foram lidas sejam mantidas, pois provavelmente serão lidas outra vez em breve. O algoritmo utiliza uma estrutura de dados auxiliar que mantém a informação da ordem em que as páginas atualmente em memória foram utilizadas.
Assinale a alternativa que explica corretamente o motivo do algoritmo LRU geralmente selecionar páginas mais adequadas do que o algoritmo da segunda chance.​​​​​​​
Selecione a resposta:
A. O algoritmo LRU mantém a ordem de uso de todas as páginas atualmente em memória, enquanto os algoritmos da segunda chance ou do relógio perdem a informação de leitura de uma página quando movem a página para o fim da fila.
B. O algoritmo LRU usa menos memória do que o algoritmo da segunda chance ou o algoritmo do relógio, fazendo com que sobre memória para auxiliar na escolha da página mais adequada.
C. O algoritmo da segunda chance também mantém a ordem de uso de todas as páginas, mas o uso da estrutura de dados auxiliar no algoritmo LRU permite antever qual página será a próxima a ser usada, evitando sua remoção precoce.
D. O algoritmo LRU seleciona páginas tão boas quanto o algoritmo do relógio, mas melhores que o algoritmo da segunda chance, pois mantém a ordem de uso de todas as páginas atualmente em memória.
E. Os algoritmos do relógio e da segunda chance não aproveitam a informação de utilização recente das páginas que estão na memória, enquanto o algoritmo LRU a usa para selecionar a página a ser substituída.

✅ A alternativa correta é: A

#### Questão 4
O algoritmo de substituição de página ótimo seleciona a página que irá demorar mais a ser usada novamente para ser substituída, garantindo o menor número possível de faltas de página durante a execução. Esse algoritmo, no entanto, não é utilizado em nenhuma situação.
Assinale a alternativa que explica o motivo de esse algoritmo não ser usado.​​​​​​​
Selecione a resposta:
A. O algoritmo ótimo tem custo de processamento muito alto para ser viável.
B. O algoritmo ótimo tem custo de memória muito alto para ser viável.
C. O algoritmo ótimo é de difícil implementação, não tendo custo-benefício vantajoso.
D. É impossível saber exatamente quando todas as páginas serão usadas novamente.
E. É impossível identificar quando uma página que está na memória foi usada e mantê-la.

✅ A alternativa correta é: D


#### Questão 5
O algoritmo NRU é simples de entender e implementar, não precisando de armazenamento extra relevante; em várias situações, tem um desempenho de escolha das páginas aceitável. Ele leva em consideração, separadamente, as marcações de leitura e escrita das páginas que estão em memória, podendo ser justo ao selecionar a página a ser substituída.
Escolha a alternativa correta sobre a ordem de escolha usada pelo algoritmo NRU.​​​​​​​
Selecione a resposta:
A. Páginas recentemente lidas e escritas serão as primeiras a serem substituídas.
B. Páginas recentemente lidas, mas não recentemente escritas, serão selecionadas para substituição antes das páginas que não foram nem lidas, nem escritas.
C. Páginas não recentemente lidas nem escritas serão as últimas a serem substituídas.
D. Páginas recentemente lidas, mas não recentemente escritas, serão selecionadas para substituição antes das páginas não recentemente lidas, mas recentemente escritas.
E. Páginas não recentemente lidas, mas recentemente escritas, serão selecionadas para substituição antes das páginas recentemente lidas, mas não recentemente escritas.

✅ A alternativa correta é: E

## Na prática

O algoritmo LRU geralmente apresenta excelente eficiência na escolha da página a ser substituída. Essa análise, com base em um comportamento médio de programas em relação ao acesso de memória, é muito válida no contexto de memória virtual. A implementação de memória virtual do núcleo do sistema operacional Linux, por exemplo, utiliza o algoritmo LRU para permitir a substituição de páginas.  

Nesta Na Prática, você vai entender como arquitetos de software do Dropbox optaram por usar o algoritmo LRU para a implementação dos algoritmos de substituição de conteúdo da cache dos seus aplicativos para smartphone.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/99e44bbe-8ffb-4d48-a50d-b2bc7cd09a41/d1a3cb70-eaf0-4912-92cc-b15a0c141104.png)

​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Técnicas de web caching e prefetching com prioridades
Este trabalho tem como objetivo a definição de uma estratégia de busca antecipada de informação aliada a um sistema de web caching para aumentar a disponibilidade de sistemas que operam em modo desconectado ou semiconectado. No capítulo 5, você verá um levantamento de várias técnicas usadas para substituição de conteúdo de cache, com foco em Web, e, no final, uma tabela com o resumo das vantagens e desvantagens de cada tipo de algoritmo.
[Mais](http://www.igor.pro.br/publica/papers/TI.pdf)

Algoritmo adaptativo de substituição de páginas LRU-WAR: exploração do modelo LRU com detecção de acessos sequenciais
Este artigo mostra uma proposta de melhoria ao algoritmo LRU para aprimorar sua performance em casos específicos de padrão de acesso à memória sem piorar significativamente a performance no caso médio.
[Mais](http://www.hugohc.com.br/publicacoes/WSO2004.pdf)

Sistemas operacionais - Aula 20 - Algoritmos de substituição de páginas
A memória principal está cheia, e é preciso retirar uma página. Qual página retirar? Para isso existem os algoritmos de substituição de páginas, tema desta videoaula.
[Mais](https://www.youtube.com/embed/j6RMVMUxYmc)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

CASSETARI, H. H.; MIDORIKAWA, E. T. Algoritmo adaptativo de substituição de páginas LRU-
WAR: exploração do modelo LRU com detecção de acessos sequenciais. I Workshop de
Sistemas Operacionais (WSO’2004), Salvador. Anais do XXIV Congresso da SBC, v. 1, 2004.

DEITEL, H. M.; DEITEL, P. J.; CHOFFNES, D. R. Sistemas operacionais. 3. ed. São Paulo:
Prentice Hall do Brasil, 2005.

PANCHENKHA, P. Caching in Theory and Practice. Dropbox, 16 out. 2012. Disponível em:
https://blogs.dropbox.com/tech/2012/10/caching-in-theory-and-practice/. Acesso em: 8 jan. 2020.

STEINMACHER, I. F. Técnicas de web caching e prefetching com prioridades. Universidade
Federal do Rio Grande do Sul, 2004.

TANENBAUM, A; WOODHULL, A. Sistemas operacionais: projeto e implementação. Porto
Alegre: Bookman, 2008.

Banco de imagens Shutterstock.
SAGAH, 2020.

