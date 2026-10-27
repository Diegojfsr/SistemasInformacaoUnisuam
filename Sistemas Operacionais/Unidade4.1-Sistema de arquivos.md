## Apresentação

Todo usuário de computador, independentemente do sistema operacional utilizado, já interagiu com arquivos, que são um componente fundamental da estruturação de um computador. Alguns exemplos de arquivos são: documentos de texto, imagens, áudios, além daqueles utilizados para instalação e utilização de softwares em geral. Você já olhou, por exemplo, no sistema operacional Windows, a pasta arquivos de programas? Se não olhou ainda, faça esse exercício e verá que todos os programas que você instala em seu computador são baseados em arquivos.

Tecnicamente, os arquivos são unidades lógicas de informação, criadas por processos, porém a existência deles independe da execução do processo. Ou seja: os arquivos ainda irão existir quando o processo que os criou for encerrado.

Nesta Unidade de Aprendizagem, você irá estudar o sistema de arquivos dos sistemas operacionais Windows e Linux. Além disso, entenderá os conceitos de arquivo e de sistemas de arquivos, bem como aprenderá a reconhecer os componentes de sistemas de arquivos.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir a hierarquia de dados em um computador.  
- Conceituar arquivo e sistemas de arquivos.  
- Reconhecer os componentes de sistemas de arquivos.


## Desafio

Existem vários sistemas de arquivos que podem ser utilizados no momento da formatação de um disco. Alguns exemplos conhecidos são FAT e NTFS. Cada tipo de sistema de arquivo apresenta características próprias que podem impactar a forma de armazenamento, a capacidade e o tipo de arquivo suportado.

![Na parte esquerda da imagem, há um bloco de texto. O conteúdo diz: Imagine que você seja funcionário de uma empresa e trabalhe com infraestrutura. Em determinado momento, um colega o procura dizendo que estava tentando fazer uso de um pen-drive de 32gb para transportar os arquivos do computador do escritório para a produção. Contudo, embora o pen-drive esteja vazio, o Windows está apontando como disco cheio. Como você foi o responsável pela compra deste e de outros pen-drives na empresa, precisa justificar esse funcionamento indevido. À direita, dentro de um recorte circular, há uma fotografia. Nela, uma mão segura um pen-drive e o aproxima da porta USB de um notebook apoiado sobre uma mesa. Parte do teclado do notebook aparece no canto superior direito da fotografia.](https://statics-marketplace.plataforma.grupoa.education/sagah/c89323f9-961a-438c-8f6c-2db21e63fe69/fd776654-0baf-449f-9db6-0b8541ec1e61.png)

​​​​​​
Considerando esse contexto, elabore um relatório técnico para a sua empresa. No documento, deverão constar o motivo da ocorrência do problema e uma solução para que todo o espaço do pen-drive seja utilizado.

#### Padrão de resposta esperado
O problema de disco cheio não está relacionado à capacidade de armazenamento do pen-drive, onde foi diagnosticado o problema. Na verdade, ele tem relação com a forma como esse pen-drive foi formatado.

Existem dois tipos de formatação de disco: FAT e NTFS. Quando um disco é formatado como FAT, os arquivos dentro dele não podem ter mais de 4gb. Ou seja, o usuário pode usar todo o dispositivo, mas os arquivos precisam ser de, no máximo, 4gb.

A solução adotada, portanto, deve ser formatar o pen-drive utilizando o formato NTFS, que não limita o tamanho de arquivo.


####  ✅ Resposta ao desafio:

1.Resumo Executivo
Este relatório tem como objetivo apresentar a justificativa técnica para um incidente reportado por um colaborador da área de produção, o qual constatou que um pen-drive recém-adquirido de 32 GB, embora vazio, era apontado pelo sistema operacional Windows como sem espaço disponível para o transporte de determinados arquivos. A análise constatou que o comportamento não decorre de defeito físico no hardware, mas sim das características do sistema de arquivos utilizado na formatação original do dispositivo.

2.Diagnóstico do Problema
O aviso de "disco cheio" em um dispositivo totalmente vazio está diretamente relacionado ao sistema de arquivos empregado na formatação do pen-drive.

Muitos dispositivos removíveis vêm formatados de fábrica no padrão FAT32 (frequentemente referido apenas como FAT) por questões de compatibilidade com sistemas legados ou outros equipamentos. As principais limitações desse formato compreendem:

Tamanho máximo por arquivo individual: O sistema FAT32 impõe um limite estrito de 4 GB para qualquer arquivo isolado.

Impacto operacional: Caso a equipe tente transferir um arquivo único superior a esse limite (como imagens de máquinas virtuais, vídeos de alta resolução ou grandes pacotes de dados compactados), o Windows pode interpretar incorretamente a operação ou gerar conflitos de alocação, resultando em mensagens de erro relativas ao armazenamento, mesmo com o pen-drive fisicamente livre.

3.Solução Proposta
Para sanar o problema de forma definitiva e permitir que todo o espaço de 32 GB seja utilizado sem restrições severas ao tamanho dos arquivos transportados, a diretriz técnica recomendada é a reformatação do pen-drive utilizando o sistema de arquivos NTFS (ou exFAT, caso haja necessidade de compatibilidade nativa com sistemas macOS).

Procedimento para Reformatação (Windows):
Conecte o pen-drive à porta USB do computador.
Abra o Explorador de Arquivos e clique em Este Computador.
Localize o pen-drive, clique com o botão direito sobre ele e selecione Formatar...
Na janela que se abrir, no campo Sistema de arquivos, altere de FAT32 para NTFS.
Mantenha os demais padrões (como o tamanho da unidade de alocação) e clique em Iniciar.
Confirme o aviso de exclusão de dados. O processo será concluído em poucos segundos.

4.Conclusão
Com a adoção do formato NTFS, o limite de 4 GB por arquivo individual deixa de existir, viabilizando o transporte de qualquer tipo e tamanho de arquivo compatível com a capacidade total de 32 GB do pen-drive. O setor de infraestrutura seguirá aplicando esse padrão de formatação em futuras aquisições de mídias removíveis para evitar novos chamados semelhantes na produção.

## Infográfico

Diariamente, muitos arquivos são criados e utilizados em um computador. Contudo, um arquivo não é, necessariamente, igual ao outro em relação ao seu tipo e estrutura. O modo como o computador vai ler e interpretar cada arquivo irá depender da forma de armazenamento.

No Infográfico a seguir, conheça as principais formas estruturais de arquivos e as características de cada uma delas.

![](https://statics-marketplace.plataforma.grupoa.education/sagah/dd3b5574-cac3-43a0-839b-a27b4d3d6265/9862f0a7-5a07-475d-9bcf-9237ef1c22a0.png)

​​​​​​​

## Conteúdo do Livro

A estruturação eficiente dos dados em um computador é essencial para otimizar o acesso a informações, levando em consideração fatores como velocidade, capacidade de armazenamento e custo. A hierarquia de dados desempenha um papel fundamental nesse processo, fornecendo uma estrutura organizada de armazenamento.

Os sistemas de arquivos são os alicerces da organização de dados em dispositivos de armazenamento, como discos rígidos, dispositivos flash e unidades ópticas. Eles desempenham um papel fundamental ao permitir que os usuários armazenem, gerenciem e acessem arquivos e pastas de maneira eficiente e organizada.

Este capítulo irá explorar os conceitos básicos dos sistemas de arquivos e destacar sua importância no gerenciamento de dados. Compreenderemos como os sistemas de arquivos estruturam as informações e como isso contribui para a eficiência no acesso e manipulação dos dados. Além disso, examinaremos a hierarquia de dados em um computador, analisando os diferentes níveis de armazenamento e comparando seu uso em diversos sistemas operacionais.

No capítulo Sistema de arquivos, base teórica desta Unidade de Aprendizagem, você será apresentado a um conjunto de princípios e técnicas fundamentais para o entendimento e a utilização eficaz dos sistemas de arquivos. Ao compreender os aspectos essenciais dessa estrutura, você estará preparado para gerenciar dados de forma mais eficiente, seja em um ambiente pessoal ou em um contexto empresarial.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/076d8450-e0e5-457f-9add-62f37f8ec525/fb0d2f81-c956-443e-905c-29e6f96b6df0.jpg)



## Dica do Professor

Sistemas gerenciadores de arquivos são utilizados todos os dias por todos os usuários de computadores, e, independentemente do sistema operacional utilizado, estará acoplado um gerenciador de arquivos. O gerenciador de arquivo tem como papel criar e organizar arquivos dentro do disco.

Na Dica do Professor, veja dois dos principais sistemas gerenciadores de arquivos: o Explorador de Arquivos (Windows Explorer) e o Nautilus, utilizados pelo Windows 10 e pelo Ubuntu, respectivamente. Você irá conhecer as características individuais de cada um e terá embasamento para fazer uma comparação entre eles.

A computação está tão presente em nosso cotidiano que algumas de suas tarefas mais simples podem passar completamente batidas. Porém, quando estudamos seu funcionamento, temos um vislumbre fascinante de como hardware e software trabalham juntos em harmonia.  

No vídeo a seguir, você verá um exemplo disso: afinal, você sabe exatamente o que acontece quando deleta um arquivo de seu computador?

## Exercícios

#### Questão 1
Uma das principais formas de organizar e identificar os arquivos armazenados em um computador é por meio da nomenclatura deles. Além disso, também é por meio da nomenclatura e do local de armazenamento que o sistema operacional identifica e distingue os arquivos.
Sobre a nomenclatura de arquivos, analise as afirmativas a seguir e assinale a afirmativa correta.
Selecione a resposta:
A. Nenhum sistema operacional é capaz de identificar letras maiúsculas e minúsculas, ou seja, uma palavra escrita com letra maiúscula e a mesma palavra escrita com letra minúscula são interpretadas como a mesma palavra.
B. Muitos sistemas permitem a separação do nome do arquivo em duas partes separadas por ponto. A parte escrita após o ponto é chamada de extensão do arquivo e é utilizada para identificar seu tipo (se é um texto ou uma imagem, por exemplo).
C. Na nomenclatura de um arquivo, o único caractere especial permitido, independentemente do sistema operacional, é o ponto.
D. Por padrão, todos os sistemas operacionais permitem nomes de arquivos de até 255 letras.
E. Em sistemas baseados em UNIX, como, por exemplo, as diversas distribuições do Linux, letras maiúsculas e minúsculas não são diferenciadas. Já em sistemas baseados em MS-DOS, como, por exemplo, as diversas versões do Windows, letras maiúsculas e minúsculas são consideradas letras diferentes.

✅ A alternativa correta é: B


#### Questão 2
Dentro de um computador, os arquivos armazenados podem ser estruturados de diversas formas. Essa estruturação é transparente para o usuário, mas não é transparente para o computador. A estruturação define a forma como o arquivo será armazenado e interpretado pelo computador.
Sobre as formas de estruturação de arquivos, marque a única alternativa correta:
Selecione a resposta:
A. Na sequência estruturada de bytes, o sistema operacional identifica e trata o que existe no arquivo. Contudo, o sistema operacional é capaz de ver apenas bytes. Qualquer significado deve ser imposto pelos programas em nível de usuário.
B. Na sequência de registros, o arquivo é uma sequência de registros de tamanho dinâmico. Nessa estrutura, uma operação de leitura sobrescreve ou anexa apenas um registro, e uma operação de escrita retorna apenas um registro.
C. Na árvore, um arquivo consiste em uma árvore de registros, não necessariamente todos do mesmo tamanho, mas cada um contendo um campo de chave em uma posição ﬁxa no registro.
D. Na sequência de diretórios, os arquivos são organizados como grupos de diretórios de arquivos.
E. Na pilha, há uma estrutura muito similar à de árvore. Porém, a estrutura é como uma pilha, em que o primeiro registro inserido é o último a ser removido.

✅ A alternativa correta é: C


#### Questão 3
Muitos sistemas operacionais suportam vários tipos de arquivos — por exemplo, arquivos normais, arquivos especiais e diretórios.
Sobre os tipos de arquivos suportados pelos sistemas operacionais, analise as afirmativas a seguir e assinale a única correta.
Selecione a resposta:
A. Os diretórios são arquivos utilizados pelo sistema para armazenar os metadados.
B. Os arquivos normais são aqueles que contêm informações do usuário.
C. Os arquivos especiais de caracteres são usados para modelar discos.
D. Os arquivos especiais de bloco são relacionados à entrada/saída e usados para modelar dispositivos de E/S seriais, como terminais, impressoras e redes.
E. Arquivos especiais são arquivos que, necessariamente, contêm metadados e são escritos utilizando a linguagem ASCII.

✅ A alternativa correta é: B


#### Questão 4
Embora os arquivos possam ter estruturas diferentes, todos eles apresentam, obrigatoriamente, um nome e um conteúdo (dados). Além dessas informações básicas, os sistemas operacionais podem enriquecer esses arquivos com outras informações, que são chamadas de atributos ou de metadados. Um exemplo disso é a data e a hora em que o arquivo foi criado e o tamanho dele.
Sobre os atributos que podem ser adicionados em arquivos, analise as afirmativas a seguir e classifique-as em verdadeiro ou falso, considerando o nome do atributo e sua definição.
I. Flag de temporário: indica se o arquivo é definitivo ou se deve ser excluído ao final do processo. 0 é um arquivo normal, e 1 é um arquivo que será excluído.
II. Flag de arquivamento: indica se o arquivo é interno de um processo e deve ser arquivado na pasta do processo ou se é um arquivo do usuário, que pode ser salvo em qualquer diretório.
III. Flag de proteção: indica se o arquivo está disponível para edição ou apenas para leitura.
IV. Flag de acesso aleatório: 0 indica que o acesso a esse arquivo é sequencial, e 1 que o acesso é aleatório.
V. Flag de sistema: indica que 0 é um arquivo normal e que 1 é um arquivo do sistema.
Selecione a resposta:
A. As afirmativas I, II e III são verdadeiras.
B. Apenas as afirmativas I, IV e V são verdadeiras.
C. Apenas as afirmativas IV e V são verdadeiras.
D. Apenas as afirmativas I e IV são verdadeiras.
E. Apenas as afirmativas I e III são verdadeiras.

✅ A alternativa correta é: B


#### Questão 5
Considerando que os arquivos são parte de grande relevância em um sistema operacional, é necessário que possam ser efetuadas operações sobre eles, ou seja, que esses arquivos possam, por exemplo, ser criados ou excluídos. Contudo, além dessas duas operações, diversas outras operações podem ser feitas com arquivos.
Sobre essas operações, analise as afirmativas a seguir e classifique-as em verdadeiras ou falsas.
I. Append: é uma forma restrita de escrita (write), em que só podem ser adicionados dados ao final do arquivo.
II. Seek: é utilizada por arquivos de acesso aleatório para definir especificamente onde os dados de um arquivo serão extraídos.
III. Lock: é utilizado para impedir a existência de acessos simultâneos por diversos processos a um mesmo arquivo ou parte de arquivo.
IV. Save: é utilizado no momento da criação de um arquivo para anunciar que o arquivo está sendo criado e configurar alguns atributos
V. Get Attributes: é utilizado para alterar os atributos de um arquivo —por exemplo, alterar a flag de backup.
Selecione a resposta:
A. São verdadeiras apenas as afirmativas II, III, V.
B. São verdadeiras apenas as afirmativas I, III e V.
C. São verdadeiras apenas as afirmativas I, II, III, IV.
D. São verdadeiras apenas as afirmativas I, II e III.
E. São verdadeiras apenas as afirmativas I e II.

✅ A alternativa correta é: D


## Na prática

Além da estrutura utilizada por arquivos normais em um computador, é de extrema importância estar atento à estrutura utilizada por diretórios ou arquivos de diretórios, porque os diretórios interferem diretamente na forma como são salvos os arquivos, podendo, por exemplo, replicar o nome de um arquivo em diretórios diferentes ou não.

Conhecer essa diferença entre os tipos de diretórios é de extrema importância no momento da utilização de seu sistema de arquivos, uma vez que garante que não irá acontecer sobrescrita de arquivos, por exemplo.

A seguir, você irá conhecer a diferença entre diretório simples e diretório com estrutura hierárquica. A partir disso, poderá entender qual tipo de diretório é mais adequado ao contexto empresarial da atualidade e por que a estrutura de diretórios interfere na sobrescrita ou não de arquivos.

#### Sistemas de diretórios para criação de arquivo com o mesmo nome para dois usuários diferentes

Paulo e Maria são professores universitários que ministram a mesma disciplina em turmas diferentes. Os dois utilizam a mesma máquina, porém cada um tem o seu usuário.
Em determinado dia, quando Maria chegou à universidade, percebeu que os seus arquivos haviam sido substituídos pelos de Paulo.

Esse problema aconteceu porque o computador estava configurado com uma estrutura diretório simples, ou seja, existe um único diretório compartilhado entre todos os usuários.
No momento em que Paulo utilizou o mesmo nome de arquivo que Maria, os arquivos foram sobrescritos.

Diretório -> Arquivo(vinculado a Maria)
Diretório -> Arquivo(vinculado a Paulo)

Para resolver essa situação, os computadores podem ser estruturados utilizando o sistema de arquivos hierárquicos. Nele, existe um diretório maior compartilhado, e, a partir dele, cada usuário tem seu próprio diretório. Além disso, um usuário também pode criar subdiretórios.

Diretório Central -> Diretório de Maria -> Arquivo -> Maria
Diretório Central -> Diretório de Paulo -> Arquivo -> Paulo

Diante dessa possibilidade, a máquina de Paulo e Maria foi formatada, e um novo sistema de arquivos passou a ser utilizado.
Agora, cada um dos professores pode acessar o seu próprio diretório e nomear os arquivos como quiser, uma vez que não haverá interferência direta entre os usuários.

## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Sistema de arquivos - AlfaCon
Neste vídeo, o professor João Paulo explica a diferença entre os sistemas de arquivo FAT e NTFS de forma prática.
[Mais](https://www.youtube.com/embed/I4ySrYDWVTk)

Visão geral dos sistemas de arquivo FAT, HPFS e NTFS
Neste artigo, é apresentada uma visão mais detalhada sobre os sistemas de arquivo FAT, HPFS e NTFS. São destacadas, por exemplo, as vantagens e as desvantagens de cada um, além dos padrões de nomenclaturas utilizados por eles.
[Mais](https://learn.microsoft.com/pt-br/troubleshoot/windows-client/backup-and-storage/fat-hpfs-and-ntfs-file-systems)

Visão geral dos sistemas de arquivos FAT, HPFS e NTFS
Veja aqui a Visão geral dos sistemas de arquivos FAT, HPFS e NTFS
[Mais](https://learn.microsoft.com/pt-br/troubleshoot/windows-client/backup-and-storage/fat-hpfs-and-ntfs-file-systems)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

DELFINO, Pedro. Linux: 10 gerenciadores de arquivos que devemos conhecer. E-TINET. Disponí-vel em: https://e-tinet.com/linux/linux-10-gerenciadores-de-arquivos-que-devemos-conhecer/.Acesso em: 15 fev. 2020.

MANUAL do Ubuntu/Navegador de arquivos Nautilus. Wikilivros, Livros abertos por um mundoaberto, 21 set. 2014. Disponível em:https://pt.wikibooks.org/wiki/Manual_do_Ubuntu/Navegador_de_arquivos_Nautilus. Acesso em: 15 fev. 2020.

SILVA, José Vitor Lopes. Nautilus. Disponível em: http://wiki.ubuntu-br.org/Nautilus. Acesso em:15 fev. 2020.

TANENBAUM, A.; WOODHULL, A. Sistemas operacionais: projeto e implementação. Porto
Alegre: Bookman, 2008.

Windows 10. Disponível em: https://en.wikipedia.org/wiki/Windows_10#/. Acesso em: 20 fev.2020.

Banco de imagens Shutterstock.
SAGAH, 2020.


