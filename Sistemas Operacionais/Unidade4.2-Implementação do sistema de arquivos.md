## Apresentação

Sistemas de arquivos são essenciais para que os dados consumidos e as informações geradas por sistemas computacionais sejam organizadas. O arquivo é uma das abstrações mais antigas e usadas em sistemas operacionais, além de ser aquela com a qual os usuários têm mais contato e familiaridade. A implementação de sistemas de arquivos necessita de diversas técnicas para prover uma solução útil para os usuários e que consiga ser aplicada aos diversos tipos de memórias secundárias disponíveis. É necessário definir como será realizada a organização (ou alocação) dos dados nos discos para permitir sua leitura. A escolha da abordagem de alocação pode ter impacto na performance de acordo com o modo de leitura dos arquivos, por exemplo, assim como determinar a quantidade de memória principal que será usada pelo sistema operacional para garantir o funcionamento do sistema de arquivos. Permissões de acesso também podem ser de responsabilidade do sistema de arquivos em uso.

Nesta Unidade de Aprendizagem, você aprenderá as principais abordagens de alocação de dados em sistemas de arquivos, suas vantagens e desvantagens e em que sistemas e dispositivos cada uma delas é comumente usada. Também entenderá os mecanismos de controle de acesso aos arquivos que são usados nos principais sistemas operacionais e, por fim, compreenderá as técnicas de verificação e de correção de erro que podem ser usadas para identificar e evitar corrupção de dados.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Identificar os tipos de alocação de arquivos.
- Discutir o gerenciamento de espaço livre e o controle de acesso a arquivos.
- Reconhecer técnicas de proteção de integridade dos dados.

## Desafio

O tipo de alocação de arquivos no disco é, provavelmente, a característica mais marcante e definitiva em um sistema de arquivos. O uso de uma abordagem específica de alocação irá definir diretamente como os arquivos são gravados no disco, mas, indiretamente, tem efeitos na performance e até mesmo no tipo de mídia no qual pode ser adequado usar esse sistema de arquivos.

Apesar de alguns formatos de sistemas de arquivos serem bem aceitos em múltiplos sistemas operacionais, como por exemplo, o sistema de arquivo FAT-32, os principais sistemas operacionais oferecem sistemas de arquivos desenvolvidos sob medida para se adequarem a algumas funcionalidades específicas do sistema operacional. Exemplos disso são abundantes: o sistema de arquivos NTFS, usado no Windows 10 ou o sistema APFS usado no macOS, tendo esses sistemas de arquivo sido projetados observando não apenas as características dos discos, mas principalmente dos sistemas operacionais nos quais seriam utilizados.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/8b775cd1-4092-470f-a5c9-f518ab84ea1b/89610f45-bca2-42a1-9d72-cf78d3914378.png)

Com base nessas informações, faça as decisões para as seguintes características do sistema de arquivos a ser projetado, com as respectivas justificativas:
A) Qual dos seguintes modelos de alocação seria mais adequado: i-nodes, contíguo, lista encadeada ou lista encadeada em memória? Justifique.
B) Onde seriam armazenados os metadados dos arquivos?
C) Seria mais adequado usar blocos pequenos (1KB) ou maiores (8KB)? Essa escolha poderia influenciar na escolha de outro modelo de alocação?
D) Como você projetaria o sistema de permissões desse sistema de arquivos?

#### Padrão de resposta esperado

A) Um modelo baseado em i-nodes seria o mais adequado, pois com a grande quantidade de discos disponíveis no sistema, essa abordagem permitiria menor consumo de memória. Isso ocorre devido ao fato de que apenas os i-nodes dos arquivos em uso estariam carregados, ao invés de toda a tabela de alocação, como seria o caso da lista encadeada em memória. O modelo contíguo não é apropriado para sistemas que permitem leitura e escrita, e o modelo de lista encadeada em memória, mesmo em uma máquina com muita memória RAM, poderia ocupar um espaço muito grande de memória principal devido ao imenso número de discos de alta capacidade exigir que muitas tabelas sejam mantidas na memória principal. O modelo de lista encadeada puro nunca deve ser usado, visto que seu acesso aleatório é muito lento e o uso do final do bloco para armazenar o ponteiro faz com que um bloco deixe de armazenar uma quantidade de dados que seja uma potência de 2, tornando operações de consulta mais complexas.
B) Os próprios i-nodes seriam utilizados para armazenar os metadados, pois são as estruturas adequadas e já associadas a cada arquivo para manter esse tipo de informação.
C) Como os arquivos, em média, são grandes, o uso de blocos maiores pode ser interessante por permitir partições de maior tamanho. Blocos maiores podem fazer a tabela de alocação diminuir, tornando menor o consumo de abordagens de tabela de alocação em memória, mas ainda assim os i-nodes continuam sendo uma opção mais adequada para o sistema em questão.
D) A necessidade de granularidade de usuários, grupos e até mesmo de direitos torna o uso de Listas de Controle de Acesso (Access Control Lists - ACL) a opção mais apropriada, por ser um mecanismo eficiente para essas características.


####  ✅ Resposta ao desafio:

A) Modelo de alocação mais adequado:
Um modelo baseado em i-nodes seria o mais adequado. Com a grande quantidade de discos de alta capacidade conectados simultaneamente ao sistema, essa abordagem permite um menor consumo de memória principal, visto que apenas os i-nodes dos arquivos em uso precisam estar carregados — ao contrário de tabelas de alocação inteiras, como na lista encadeada em memória. O modelo contíguo não é apropriado para sistemas que lidam com operações frequentes de leitura e escrita. O modelo de lista encadeada em memória, mesmo em uma máquina com muita memória RAM, ocuparia um espaço excessivo na memória principal devido ao imenso número de discos e tabelas exigidas. Já a lista encadeada pura nunca deve ser usada, pois seu acesso aleatório é extremamente lento e o uso do final do bloco para ponteiros impede que o tamanho do bloco seja uma potência de 2, complicando operações de consulta.

B) Armazenamento dos metadados:
Os metadados seriam armazenados nos próprios i-nodes, pois essas estruturas são nativamente associadas a cada arquivo e projetadas especificamente para manter esse tipo de informação de forma centralizada e eficiente.

C) Tamanho dos blocos e influência no modelo de alocação:
O uso de blocos maiores (como 8KB) é mais adequado, uma vez que os arquivos gravados no sistema são grandes na média, permitindo partições de maior tamanho e reduzindo o overhead de gerenciamento. Blocos maiores ajudam a diminuir o tamanho de eventuais tabelas de alocação, mas, dado o cenário de múltiplos discos massivos, os i-nodes continuam sendo a opção superior e mais escalável.

D) Projeto do sistema de permissões:
O sistema de permissões deve ser implementado por meio de Listas de Controle de Acesso (Access Control Lists - ACL). Esse mecanismo é o mais apropriado por atender perfeitamente à exigência de um alto nível de granularidade, permitindo gerenciar com precisão direitos complexos para múltiplos usuários e grupos.


## Infográfico

Discos podem ser divididos em unidades lógicas de menor tamanho do que seu espaço total para facilitar o gerenciamento dos arquivos por parte dos usuários. As informações que definem esse particionamento do disco devem estar presentes no próprio disco, pois caso ele seja movido para um computador diferente, é essencial que a mesma organização seja respeitada. Além disso, o computador precisa saber em qual dessas partições há sistemas operacionais instalados. Considerando que mesmo em computadores modernos o software do BIOS (Basic Input/Output System - Sistema Básico de Entrada e Saída) é relativamente simples, é necessária uma organização rígida e bem padronizada para facilitar o início do funcionamento do computador.

No Infográfico a seguir, você poderá compreender como os primeiros setores de um disco são organizados para permitir que o computador seja inicializado e vai entender como o disco está dividido em partições.

#### Inicialização de discos

Confira aqui como é a organização de um disco rígido: como blocos de funções bem definidas são usados para que o BIOS (Basic Input/Output System - Sistema Básico de Entrada e Saída) inicialize um sistema operacional, e os sistemas de arquivos de cada partição do disco.

Partição 3
Bloco de inicialização
Superbloco

Partição 2
Bloco de inicialização
Superbloco

#### Partição 1
Bloco de inicialização
O programa Bootloader do sistema operacional é responsável por iniciar a execução do sistema. Ele deve ser instalado no bloco de inicialização da partição onde o sistema operacional está localizado. Todas as partições, inclusive as que não têm um sistema operacional instalado, começam com um bloco de inicialização.
O programa NTLDR é o bootloader dos sistemas baseados em Windows NT.
No Linux, as outras etapas do GRUB são comumente usadas como bootloader.

Superbloco
Contém informações sobre o sistema de arquivos da partição:
Identificador de sistema de arquivos
Número de blocos
Status do disco
Quais blocos estão ocupados
Quais blocos estão disponíveis
Localização do i-node raiz (se o sistema de arquivos usar i-node)
Geralmente, existem vários backups do superbloco espalhados pela partição, pois perder o superbloco seria catastrófico.

MBR
A MBR (Master Boot Record – Registro Mestre de Inicialização) está no Setor 0 do disco, e nela deve ser armazenado o programa responsável por controlar o boot do sistema (como a primeira etapa do Grub, comum em máquinas com Linux). Esse programa é chamado pelo BIOS logo após o computador estar pronto, e sua função é ler a tabela de partição, escolher uma partição ativa (ou oferecer para o usuário a escolha entre múltiplas partições ativas disponíveis) e disparar o início do sistema operacional instalado na partição selecionada.

Tabela de partições
A tabela de partições é uma estrutura armazenada no final da MBR, cuja função é armazenar dados sobre como o disco foi particionado. Neste exemplo, temos 3 partições no disco. A partição 2 tem um sistema operacional instalado e, por isso, é marcada como uma partição ativa na tabela. Outra informação importante armazenada é o tamanho de cada partição.

| Partição | Tamanho | Ativa? |
| -------- | ------- | ------ |
| 1        | 250GB   | 0      |
| 2        | 290GB   | 1      |
| 3        | 100GB   | 0      |


## Conteúdo do Livro

A implementação de sistemas de arquivos que serão usados em sistemas operacionais requer que os projetistas considerem diversos fatores, os quais poderão ter influência na efetividade do sistema projetado. O projeto de um sistema de arquivos leva em conta o tipo de mídia na qual serão usados, as características dos computadores em que serão usados e o padrão de uso que será feito para os arquivos, tanto em termos de acesso como de tamanho, entre outros detalhes que também são analisados.

Outro aspecto importante no projeto de um sistema de arquivos é a segurança dos dados armazenados. Sistemas operacionais multiusuários comumente precisam compartilhar arquivos entre seus usuários, mas com limites bem estabelecidos, como por exemplo, quais usuários podem ter acesso de escrita, quais devem ser capazes apenas de ler o arquivo ou mesmo usuários que não devem ter acesso algum a um arquivo.

Na seção 5.3 do livro Sistemas operacionais: projeto e implementação, base teória desta Unidade de Aprendizagem, você aprenderá os principais conceitos sobre alocação dos arquivos em memória secundária e seus impactos em performance de acordo com o padrão de leitura dos arquivos, assim como em termos de consumo de memória principal. A seção 5.4 traz os princípios básicos de segurança que podem afetar sistemas de arquivos, e esta é importante para compreender a seção 5.5, que apresenta os mecanismos de proteção que podem ser implementados para garantir que os princípios anteriormente discutidos sejam respeitados.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/91913377-960d-4226-b15d-c9ddb0ed4e78/79a630bc-ccf7-4507-abac-88fc548028ce.jpg)


## Dica do Professor

A escolha da abordagem de alocação dos arquivos em disco é a opção mais decisiva ao projetar um sistema de arquivos. As limitações da abordagem escolhida devem ser toleráveis no contexto de uso que os usuários desse sistema de arquivos enfrentarão no dia a dia, e sua performance deve ser adequada para o tipo de mídia usada como memória secundária.
Nesta Dica do Professor, você verá as principais abordagens utilizadas nos sistemas de arquivos que são aplicados nos sistemas operacionais modernos, como a alocação contígua, lista encadeada, lista encadeada em memória e os i-nodes.


## Exercícios

#### Questão 1
A simplicidade do software utilizado para inicializar computadores pessoais é refletida na organização usada nos discos, em que alguns setores são predefinidos para desempenhar uma função no processo de inicialização. Assinale a alternativa que descreve corretamente o processo de inicialização a partir de um disco.​​​​​​​
Selecione a resposta:
A. O programa armazenado na tabela de partição é executado para iniciar o computador, lendo o MBR (Master Boot Record - Registro Mestre de Inicialização) para identificar a partição ativa. O bootloader do bloco de inicialização da partição ativa é então executado.

B. O programa armazenado no bloco de inicialização é executado para iniciar o computador, lendo a tabela de partição para identificar a partição ativa. O bootloader do MBR (Master Boot Record - Registro Mestre de Inicialização) da partição ativa é então executado.

C. O programa armazenado no MBR (Master Boot Record - Registro Mestre de Inicialização) é executado para iniciar o computador, lendo o bloco de inicialização para identificar a partição ativa. O bootloader do MBR da partição ativa é então executado.

D. O programa armazenado no bloco de inicialização é executado para iniciar o computador, lendo a MBR (Master Boot Record - Registro Mestre de Inicialização) para identificar a partição ativa. O bootloader do bloco de inicialização da partição ativa é então executado.

E. O programa armazenado no MBR (Master Boot Record - Registro Mestre de Inicialização) é executado para iniciar o computador, lendo a tabela de partição para identificar a partição ativa. O bootloader do bloco de inicialização da partição ativa é então executado.

✅ A alternativa correta é: E

#### Questão 2
Sistemas de arquivos têm a função de definir a organização dos arquivos na mídia de destino para permitir sua posterior leitura ou escrita, caso a mídia permita alterações. A maneira usada para alocar os arquivos na mídia define algumas das características mais importantes do sistema de arquivos. Assinale a alternativa correta sobre alocação de arquivos em disco.​​​​​​​
Selecione a resposta:
A. Alocação por lista encadeada tem uma performance fraca em leitura aleatória.
B. Alocação por lista encadeada em memória é a mais eficiente em termos de consumo de memória principal.
C. Alocação contínua em mídias de leitura e escrita evita a ocorrência de fragmentação.
D. O uso de i-nodes faz com que o consumo de memória principal seja mais alto do que em abordagens com tabela de alocação em memória.
E. Duas partições no mesmo disco precisam ser formatadas com sistemas que usem a mesma abordagem de alocação.

✅ A alternativa correta é: A

#### Questão 3
Em sistemas de arquivos hierárquicos, os diretórios têm uma função importante em permitir a organização dos arquivos para seus usuários. A partir do encadeamento de diretórios, é possível criar estruturas complexas, mas que permitem o acesso aos arquivos de forma simplificada para as pessoas. Assinale a alternativa correta sobre como sistemas de arquivo baseados em i-nodes trabalham com diretórios.​​​​​​​
Selecione a resposta:
A. O diretório é uma estrutura à parte, armazenada na tabela de partições, com a lista dos i-nodes dos arquivos.
B. O diretório é um tipo de arquivo especial, cujo conteúdo é a lista de nomes dos arquivos e o número dos seus respectivos i-nodes.
C. O diretório é um arquivo mantido apenas em memória principal, com toda a hierarquia disponibilizada a partir do diretório raiz.
D. Para cada diretório é reservada uma área no disco, onde os arquivos são fisicamente localizados, assim como seus respectivos i-nodes.
E. Para cada diretório é reservada uma área no disco, onde os i-nodes dos arquivos desse diretório são armazenados.

✅ A alternativa correta é: B


#### Questão 4
A manutenção da segurança dos dados é essencial para sistemas operacionais. Alguns problemas em potencial podem ser evitados por um sistema de arquivos bem projetado, mas outras ameaças precisam ser contornadas por meio de outros métodos, como por exemplo, a execução periódica de backups. Sobre segurança dos dados, assinale a alternativa correta.​​
Selecione a resposta:
A. Todas as perdas de dados são intencionais, causadas por indivíduos mal-intencionados que se aproveitam de brechas no sistema.
B. Backups devem ser realizados e armazenados na própria máquina para facilitar sua recuperação em caso de desastre.
C. O software e o hardware do computador operam sempre de acordo com seu projeto, não sendo causadores de erros que levam à perda de dados.
D. Simples erros humanos, como configurações ou entradas de dados de forma incorreta, podem levar a graves problemas de perda de dados.
E. Simples erros humanos como configurações ou entradas de dados de formato incorreta não levam a problemas de perda de dados.

✅ A alternativa correta é: D

#### Questão 5
A maioria dos sistemas operacionais modernos é multiusuário, ou seja, várias pessoas diferentes têm acesso ao mesmo sistema. Isso traz a necessidade de mecanismos de proteção sobre os arquivos para permitir o acesso apenas para usuários que de fato tenham direitos sobre cada um dos arquivos. Várias abordagens para implementação de proteção existem. Sobre a abordagem de listas de controle de acesso (Access Control Lists - ACL), assinale a alternativa correta.​​​​​​​
Selecione a resposta:
A. O uso de ACL consome mais memória do que aplicar uma matriz de proteção.
B. Com uma ACL é possível definir o nível de permissão para usuários específicos e grupos de usuários.
C. Uma ACL pode ter permissões para usuários ou para grupos, mas não pode misturar ambos os tipos.
D. ACLs podem trabalhar apenas com os direitos de leitura, escrita e execução.
E. Processos iniciados por usuários sem permissão na ACL de um arquivo podem ter acesso a esse arquivo.

✅ A alternativa correta é: B

## Na prática

O uso de listas de controle de acesso serve para gerenciar as permissões de direitos para cada arquivo, permitindo aplicar essas permissões para usuários e grupos de usuários. O mecanismo pode ser aplicado diretamente em um sistema de arquivos, mas seu uso pode ser interessante para se espalhar para outras partes de um sistema operacional.

Neste Na Prática, você vai entender como o conceito de listas de controle de acesso foi utilizado pela Microsoft para integrar o sistema de arquivos do Windows com um diretório de usuários que permite que a lista de usuários e de grupos esteja compartilhada em rede, permitindo, dessa forma, o compartilhamento não apenas no próprio sistema operacional, mas entre todos os computadores que compartilham o mesmo domínio de rede.


#### Evolução da atribuição de direitos em arquivos compartilhados

Um administrador de sistemas lidava com uma rede de pequeno porte de uma startup. Essa rede contava com poucos usuários e, com exceção dos três sócios-fundadores que tinham algumas necessidades especiais de proteção para alguns arquivos, todos os outros funcionários podiam ter acesso a todos os arquivos compartilhados no servidor de arquivos da empresa.
Efetivamente, era usado um servidor de arquivos na rede local que qualquer computador na mesma rede teria acesso aos arquivos.

A empresa, no entanto, cresceu rapidamente. Departamentos foram definidos e criou-se a necessidade de controle de acesso."
"O administrador de sistemas decidiu usar o Active Directory (AD), da Microsoft, para gerenciar os usuários da rede (anteriormente os funcionários entravam com usuários locais de seus computadores). Essa escolha, entre outros motivos, ocorreu devido à integração do mecanismo de Lista de Controle de Acesso (ACL – Access Control Lists) do AD com o sistema de arquivos NTFS usado no Windows, sistema operacional do servidor de arquivos usado na rede da empresa.

Foi criada então a seguinte estrutura de grupos de usuário:

Administradores: 
Sysadmins
Sócios
Diretores

Administrativo:
Financeiro -> Compras
RH

Operacional:
Gerentes
Desenvolvimento
Desenvolvimento -> Engenharia
Desenvolvimento -> Testes
Desenvolvimento -> Operação

Com essa estrutura, o administrador de sistemas criou diretórios no servidor de arquivo e aplicou as permissões adequadas para cada grupo. Veja aqui a lista com as permissões que podem ser atribuídas em NTFS.
Uma característica interessante do uso de grupos nesse caso é que, ao fornecer uma permissão de Controle Total para o grupo Administradores, um usuário que seja do grupo Sócios terá essa permissão, já que o grupo Sócios é membro do grupo Administradores.

Permissões disponíveis em NTFS:
Controle total
Percorrer pasta/executar arquivo
Listar pasta/ler dados
Ler atributos
Ler atributos estendidos
Criar arquivos/gravar dados
Criar pastas/acrescentar dados
Gravar atributos
Gravar atributos estendidos
Excluir
Permissão de leitura
Alterar permissões

O administrador de sistemas aproveita muito essa característica para simplificar as listas de controle de acesso.
Outra capacidade importante é que um usuário pode fazer parte de dois grupos diferentes. Por exemplo: um engenheiro, que também trabalha com operação (seguindo a cultura de DevOps), teve seu usuário associado a ambos os grupos, assim, ele tem as permissões de ambos os grupos (Desenvolvimento e Operacional).

O uso adequado das funcionalidades do combo AD + NTFS permitiu que o administrador tivesse seu trabalho simplificado ao montar a estrutura que serviu à situação apresentada.
A simplicidade também contribui para a manutenção da estrutura. Isso tornou as Listas de Controle de Acesso aplicadas aos arquivos e diretórios pequenos e de fácil alteração, pois minimizaram a quantidade de permissões atribuídas para cada usuário, ou grupo de poucos usuários.
A abordagem aplicada também evitou que permissões em excesso fossem concedidas a usuários que deveriam ser restritos.

## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

O princípio da integridade e da confidencialidade dos dados no RGPD
Vídeo com discussão sobre a regulamentação europeia de proteção de dados, sobre os pontos que citam a integridade e a confidencialidade dos dados sob custódia de sistemas eletrônicos. O autor, em alguns momentos, faz paralelos entre a legislação europeia e a brasileira.
[Mais](https://www.youtube.com/embed/z3TvUtHnM_Y)

Integridade - segurança da informação - dicionário de informática
Vídeo com definição sobre o conceito de integridade de dados em segurança de informação, com exemplo de como a integridade pode ser violada.
[Mais](https://www.youtube.com/embed/chBAQxW701U)

Ciência da computação
Para se aprofundar mais em sistemas operacionais, leia este livro, que apresenta o conteúdo pertinente ao que foi estudado nesta Unidade de Aprendizagem.
[Mais](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=69202093&tokenId=2a63deb3-5006-4e01-8241-f6c8785158d9)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

NULL, L.; LOBUR, J. Princípios básicos de arquitetura e organização de computadores. 2.
ed. Porto Alegre: Bookman, 2011.

OLIVEIRA, R. S.; CARISSIMI, A. S.; TOSCANI, S. S. Sistemas operacionais. 3. ed. Porto
Alegre: Bookman : Instituto de Informática da UFRGS, 2008.

TANENBAUM, A. S.; CONSULARO, L. A.; GONÇALVES, R. A. L. Sistemas operacionais
modernos. 3. ed. São Paulo: Prentice Hall do Brasil, 2009.

TANENBAUM, A.; WOODHULL, A. Sistemas operacionais: projeto e implementação. Porto
Alegre: Bookman, 2008.

Banco de imagens Shutterstock.
SAGAH, 2020.
