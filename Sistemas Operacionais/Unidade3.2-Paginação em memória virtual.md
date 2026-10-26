## Apresentação

Todo usuário gostaria que seu computador tivesse memória suficiente para executar todos os seus programas de modo rápido. Infelizmente essa não é a realidade. Por mais que o desenvolvimento de memórias tenha evoluído muito nos últimos anos, proporcionando capacidades maiores, os programas de usuário têm crescido em um ritmo muito rápido, sempre criando a necessidade de alternativas para gerenciamento do espaço para os programas.

Desde a década de 60, com programas científicos e financeiros, a necessidade de executar programas maiores que a memória do computador já era um problema real. Esse problema também pode acontecer quando os programas, mesmo que individualmente sejam menores que a memória, se executados simultaneamente, não podem estar em sua totalidade na memória principal. Dentre as soluções inventadas, tem-se a memória virtual.

Nesta Unidade de Aprendizagem, você vai aprender sobre uma das principais técnicas de memória virtual, a paginação, e entender o funcionamento e os problemas/soluções que podem acontecer.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir a técnica de paginação de memória, explicando seus princípios, vantagens e desvantagens.
- Explicar o processo de troca de páginas em memória virtual.
- Reconhecer problemas em um sistema de paginação e a forma de solucioná-los.


## Desafio

O desenvolvimento de software evoluiu muitos nos últimos tempos, de modo que, hoje, os programas têm cada vez mais funcionalidades e consomem muito mais recursos. Dentre esses recursos está a memória, que, apesar da sua evolução, também precisa ser gerenciada. Quando a memória principal não é suficiente, é comum adotar o uso de memória virtual.

Você trabalha em uma empresa que desenvolve software para equipamentos embarcados, principalmente voltados para indústrias no monitoramento da produção dos equipamentos utilizados. Como os sistemas são embarcados e também na tentativa de redução de custos, os recursos são limitados e devem ser aproveitados o máximo possível.

Dentre os softwares desenvolvidos, além dos programas de análise, é comum desenvolver um sistema operacional para gerenciamento do componente como um todo. Em geral, os programas são bem divididos, em termos de memória quanto a instruções, pilha e áreas de dados.


![](https://statics-marketplace.plataforma.grupoa.education/sagah/833cfe24-2168-4c3f-8c1b-429f43f6bfbd/6570d085-cdec-4e6c-abf2-da2fad668d19.jpg)

Contudo, você tem enfrentado um problema quanto à troca de processos entre a memória e o disco do componente, em que muitas páginas ao serem salvas em discos são reescritas sem necessidade, pois não estão modificadas. Por exemplo, algumas páginas são compostas somente pelas instruções do programa, e geralmente não são modificadas durante a execução, logo, quando essa página for substituída por outra na memória principal, não haverá a necessidade de reescrita, pois esta permanece inalterada. Por outro lado, as páginas que armazenam dados do programa provavelmente são modificadas, e isso só pode ser descoberto durante a execução da página na memória principal.

Com base no cenário descrito, que tipo de informação poderia ser armazenada para indicar se a página precisa ser reescrita ou não em disco? Onde esse dado seria armazenado?

#### Padrão de resposta esperado

A implementação descrita não tem registro indicando se determinada página foi modificada ou não.

A informação que precisa ser adicionada é um bit de verificação de modificação para cada uma das entradas de tabela de páginas, o que permite identificar as páginas que sofreram modificação e precisam ser reescritas em disco. Essa informação precisa ser armazenada na tabela de páginas, juntamente com todas as demais informações de cada uma das páginas.

####  ✅ Resposta ao desafio:

Com base no cenário apresentado e no padrão de resposta esperado, aqui está a solução completa para o problema de gerenciamento de memória:

1.Tipo de Informação Necessária
Bit de Modificação (ou Dirty Bit / Bit de Sujeira): Um bit de controle que indica se a página foi alterada (escrita) desde que foi carregada na memória principal.
Se o bit estiver desligado (0), significa que a página permaneceu inalterada (como páginas de instruções) e, portanto, não precisa ser reescrita no disco quando for substituída.
Se o bit estiver ligado (1), significa que a página sofreu alterações (como áreas de dados ou pilha) e deve ser salva no disco para preservar as modificações.

2.Onde Esse Dado Seria Armazenado
Na Tabela de Páginas: Essa informação deve ser adicionada diretamente a cada entrada da tabela de páginas do processo, ao lado dos campos já existentes que identificam o número da página e o número da moldura (frame).

Resumo Prático
Adicionar o bit de modificação à tabela de páginas resolve o gargalo de desempenho dos sistemas embarcados. Dessa forma, o sistema operacional evita operações desnecessárias de escrita em disco para páginas inalteradas, otimizando o uso do hardware e reduzindo o desgaste do meio de armazenamento.


## Infográfico

A paginação divide os processos em páginas que são armazenadas em uma memória, geralmente disco. Conforme a execução do processo, as instruções são executadas e podem necessitar de páginas que não estão presentes na memória, desse modo, cada página solicitada é carregada em uma moldura em substituição de outra.

No Infográfico, conheça melhor o funcionamento do processo de paginação de um processo.

![](https://statics-marketplace.plataforma.grupoa.education/sagah/4d736f54-f8ab-4076-b11b-17990890a258/70421bf4-994d-49e7-a925-f77cdf900dbf.jpg)

​​​​​​​​​​​​​​​​​​​​​

## Conteúdo do Livro

Olá, alunos! No mundo da computação, é fundamental entender como a memória é gerenciada em um sistema operacional. A memória virtual é uma técnica utilizada para permitir que programas usem mais memória do que realmente está disponível na memória RAM física. Para isso, o sistema operacional aloca espaço em disco rígido para servir como uma extensão da memória RAM.

Uma das técnicas utilizadas no gerenciamento de memória virtual é a paginação. A ideia é dividir a memória física e a memória virtual em blocos de tamanho fixo, chamados de páginas. Quando um programa tenta acessar uma determinada página, o sistema operacional verifica se ela está presente na memória RAM. Se não estiver, o sistema operacional a busca no disco rígido e a coloca na memória RAM. Esse processo é chamado de paginação e é uma técnica importante para gerenciar a memória de um sistema operacional.

No capítulo Paginação em memória virtual, base teórica desta Unidade de Aprendizagem, discutiremos a técnica de paginação, abordando conceitos importantes, como mapeamento de páginas, cálculos de endereçamento virtual e físico, tamanhos de página e algoritmos de substituição de páginas. Além disso, apresentaremos exemplos práticos de como esses conceitos são aplicados em sistemas operacionais reais. A compreensão desses tópicos é fundamental para qualquer desenvolvedor ou administrador de sistemas, pois a gerência de memória é um aspecto crucial do desempenho e da estabilidade do sistema.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/815ad11e-0003-4cc7-bee9-7813516e3810/796456ec-e577-4c1a-a093-8db3c8936ac8.jpg)


## Dica do Professor

A utilização de memória virtual e paginação permite a divisão de programas em páginas, possibilitando que processos maiores (ou quando executados junto com outros) que a memória principal possam ser executados mantendo as páginas necessárias na memória principal e efetuando trocas conforme a execução. Esse mecanismo trouxe grandes benefícios, principalmente por ser independente quanto à programação, estando sob responsabilidade total do sistema operacional.

Contudo, não existem somente benefícios, mas sim problemas e questões que precisam ser decididos e resolvidos. Situações relacionadas ao tamanho do espaço de endereçamento, diferentes arquiteturas e velocidade de mapeamento de endereço são questões relevantes.

Nesta Dica do Professor, conheça um dos principais problemas da paginação, o tamanho do espaço de endereçamento, juntamente com algumas estratégias para solucioná-lo.


## Exercícios

#### Questão 1
Um sistema operacional utiliza a técnica de paginação para o uso de memória virtual. Sabe-se que cada endereço virtual tem 14 bits e os quatro bits mais significativos são responsáveis por identificar a página na memória virtual. Qual o tamanho da página utilizada?
Selecione a resposta:
A.256 bytes.
B.512 bytes.
C.1 KB.
D.2 KB.
E.4 KB.

✅ A alternativa correta é: C

#### Questão 2
A paginação em memória virtual utiliza páginas e molduras de páginas para a divisão do processo tanto na memória física quanto virtual. A respeito do funcionamento e do propósito desses dois elementos, pode-se afirmar que:
Selecione a resposta:
A. as páginas ficam presentes na memória principal, cujas correspondentes molduras estão em disco para serem requisitadas.
B. as molduras de página ficam presentes na memória principal, as quais podem alocar uma ou mais páginas, de modo que não exceda o espaço da moldura e a quantidade seja potência de 2.
C. as molduras de página ficam presentes na memória principal e só podem alocar uma página por vez, a qual tem o mesmo tamanho da moldura.
D. as páginas e molduras podem ter tamanhos diferentes conforme a necessidade, mas a alocação de página na memória deve obedecer à capacidade de espaço.
E. as páginas ficam presentes na memória principal e a divisão é feita pelo programador.

✅ A alternativa correta é: C

#### Questão 3
Um processo de 24 KB foi dividido em partições de 4 KB, numeradas de 1 a 6 em ordem. Quando uma posição de memória é acessada, a página precisa estar alocada em uma moldura na memória principal. Em um dado momento da execução, o endereço 8296 foi acessado. Desse modo, para executar a instrução nesse endereço sem causar uma chamada de sistema de page fault, qual página precisa estar carregada na memória?
Selecione a resposta:
A. Página 1.
B. Página 2.
C. Página 3.
D. Página 4.
E.Página 5.

✅ A alternativa correta é: C

#### Questão 4
O uso de memória virtual requer um mapeamento entre o endereço físico e virtual em tempo adequado para não prejudicar o desempenho do processo. Sobre o processo de mapeamento, pode-se dizer que:
Selecione a resposta:
A. uma solução para agilizar a conversão entre endereços é utilizar uma tabela associativa, também conhecida como TBL, em nível de hardware.
B. o acesso à memória para conversão do endereço virtual ao endereço físico não prejudica o desempenho do processo.
C. as diferenças entre arquiteturas de 32 bits e 64 bits não tem qualquer influência quanto ao endereçamento dos processos.
D.na implementação de tabelas de páginas multinível, as páginas são organizadas em listas encadeadas em pares de página e moldura.
E. na implementação de tabelas de páginas invertidas, as páginas são organizadas de modo hierárquico em blocos, sendo que os níveis superiores apontam para o início dos níveis inferiores, na tentativa de somente alocar as páginas necessárias de cada bloco, e não o bloco de páginas inteiro.

✅ A alternativa correta é: A

#### Questão 5
Um computador de arquitetura de 32 bits trabalha com páginas de 4 KB e tem 1 GB de RAM. Qual é o total de molduras de páginas que podem ser indexadas nessa arquitetura?
Selecione a resposta:
A. 65.536.
B. 1.048.576.
C.16.384 .
D.1.024.
E.268.435.456.

✅ A alternativa correta é: B


## Na prática

O processo de paginação tem diversos fatores que podem influenciar no desempenho. Em uma determinada arquitetura de computador, se for estabelecido que o tamanho da página será pequeno, haverá um grande número de entradas na tabela de página que precisa ser gerenciado. Isso também pode acontecer se a arquitetura puder mapear um grande número de endereços, como em arquiteturas 64 bits. Além disso, também é necessário garantir que o mapeamento de endereços virtuais em físicos seja rápido.

Conheça uma solução em nível de hardware que tem sido utilizada no aprimoramento do processo de paginação.

#### Aprimorando paginação em dispositivos

Renato trabalha como desenvolvedor em uma empresa que cria sistemas multimídia para veículos.
Na empresa, são desenvolvidos sistemas desde pequenos programas para execução de som e vídeo até o sistema operacional do dispositivo.

Explicação
Com o aumento do número de funcionalidades requeridas pelos clientes, mais programas foram adicionados aos dispositivos e, para que todos funcionem corretamente, foi implementada a técnica de paginação, para melhor gerenciamento do uso da memória principal do dispositivo.

Problema
Contudo, após a integração dos novos programas, muitos clientes passaram a relatar maior lentidão para a inicialização dos programas ou mesmo durante a execução.

Investigação
Após uma análise mais precisa, Renato pode observar que a lentidão não estava relacionada a um ou outro programa novo diretamente, mas sim com a maior quantidade.
O processo de paginação está feito somente em software, muitas operações fazem acesso direto à memória e aumentam significativamente o tempo de execução.
Além disso, a maior quantidade de programas faz com que um maior número de páginas disputem as molduras na memória principal e, consequentemente, realizem mais operações de acesso à memória.

Solução
Para amenizar o número de acessos à memória e melhorar o desempenho, Renato propôs que fosse adicionada uma memória associativa em nível de hardware.
Desse modo, antes de acessar a tabela de páginas na memória para carregar uma página, um buffer de páginas mais usadas seria mantido nessa memória associativa, permitindo a identificação das páginas muito mais rápido.

Fluxograma
Processo ➔ Memória associativa: "Buscar uma página"
Encontrou a página?
Sim: Retorna diretamente ao Processo (caminho superior).
Não (traçado pontilhado): Vai para a Tabela de páginas, que por sua vez alimenta a Memória associativa e retorna ao Processo.

Conclusão
A partir da solução proposta por Renato, o carregamento e a execução dos programas obtiveram significante melhoria no desempenho em decorrência da implementação do sistema de memória associativa em hardware.

## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

O que é a memória virtual?
Neste artigo, você entenderá melhor o que é memória virtual e como gerenciá-la por meio de programas no Windows.
[Mais](https://www.infonova.com.br/artigo/o-que-e-a-memoria-virtual)

Sistemas operacionais - paginação
Nesta videoaula da Univesp TV, você conhecerá a fundo o processo de paginação implementado em sistemas operacionais.
[Mais](https://www.youtube.com/embed/4EaBN98dk40)

Como configurar swap no Ubuntu/Debian
Neste artigo, você aprenderá como configurar o swap, também conhecido como memória virtual, em sistemas baseados no Ubuntu/Debian.
[Mais](https://www.kelvinsantiago.com.br/como-adicionar-swap-no-ubuntudebian/)

Técnicas de memória virtual
Nesta videoaula da Univesp TV, você poderá conhecer algumas técnicas de implementação de memória virtual.
[Mais](https://www.youtube.com/embed/QjieJPckuDI)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

DEITEL, H. M.; DEITEL,P. J.; CHOFFNES, D. R. Sistemas operacionais. Tradução: A. L.
Marques. 3. ed. São Paulo: Pearson Prentice Hall, 2005.

TANEMBAUM, A. S. Sistemas operacionais modernos. Tradução: R. A. L. Gonçalves, L. A.
Consularo e L. A. Teixeira. Memória virtual. 3. ed. São Paulo: Pearson Prentice Hall, 2010.

Banco de imagens Shutterstock.
SAGAH, 2020.


