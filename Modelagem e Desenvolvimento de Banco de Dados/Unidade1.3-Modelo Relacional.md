## Apresentação

Nesta Unidade de Aprendizagem vamos tratar como os dados são representados em um Modelo Relacional, qual a terminologia utilizada neste modelo e a estrutura básica deste tipo de modelo.
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Explicar como os dados são representados no modelo Relacional;
- Reconhecer a terminologia utilizada em um banco de dados relacional;
- Demonstrar a utilização básica de um modelo relacional.


## Desafio

Imagine que você é um DBA (Administrador de Banco de Dados) e está analisando e projetando um banco de dados para atender a uma Escola e/ou Universidade, onde existem alunos e estes estão cadastrados em um sistema de gestão (que utiliza banco de dados).  

A cada ano ou semestre estes alunos (Entidade ALUNOS) precisam fazer sua rematrícula para o período seguinte, e esta rematricula dá-se a partir da oferta (Entidade OFERTAS) de uma relação de disciplinas. Ambas as entidades (ALUNOS e OFERTAS) têm determinadas informações que farão parte (nem todas) do Relacionamento MATRÍCULA (relação entre as entidades Alunos e Ofertas).

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/08fb403f-9cdc-4148-93be-d817dcc87c39/b8da9d72-5982-419e-9443-1a0ab6d8aae9.png)

​​​​
Analise a situação acima e aponte quais os campos das duas entidades (Alunos e Ofertas) devem fazer parte do Relacionamento MATRÍCULAS.

####  ✅ Resposta ao desafio:

Como DBA, ao projetar o relacionamento MATRÍCULAS entre ALUNOS e OFERTAS, precisamos selecionar apenas os campos que fazem sentido para identificar e registrar a matrícula, sem carregar atributos redundantes.

Campos que devem compor a entidade-relacionamento MATRÍCULAS
Cod_Matricula: Chave primária da tabela de matrículas (novo campo criado para identificar cada matrícula de forma única).
Cod_Aluno: Referência ao aluno que está se matriculando (FK para ALUNOS).
Cod_Oferta: Referência à disciplina ofertada em que o aluno se matricula (FK para OFERTAS).
Data_Matricula: Data em que a matrícula foi realizada.
Status_Matricula: Situação da matrícula (ativa, trancada, cancelada, concluída).
Nota_Final (opcional): Campo que pode ser incluído para registrar o desempenho do aluno na disciplina.
Frequencia (opcional): Percentual de presença do aluno na disciplina.

Justificativa
Da entidade ALUNOS, só precisamos do Cod_Aluno como chave estrangeira. Os demais dados (nome, endereço, CPF etc.) permanecem na tabela ALUNOS.

Da entidade OFERTAS, só precisamos do Cod_Oferta como chave estrangeira. Informações como professor, sala e turno ficam na tabela OFERTAS.

A tabela MATRÍCULAS funciona como uma tabela associativa (N:N), já que um aluno pode se matricular em várias ofertas e cada oferta pode receber vários alunos.

#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 16813333
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 14/05/26 - 19:21
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

O Modelo Relacional é um modelo físico que representa os dados de um banco de dados como uma coleção de tabelas (relações), enquanto o modelo Entidade-Relacionamento (ER) é um modelo conceitual que é utilizado para descrever as entidades e as suas características –  os atributos – ilustrando como esses elementos se relacionam entre si. Veja, no Infográfico, uma forma facilitada para converter o Modelo ER para o Modelo Relacional.

​​​​​​​

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/fee52c09-af7d-45d0-b29f-e58bc8eb2830/9cb7ae6e-393c-4fea-90b3-fb76a3ef4ef5.png)

​​​​​​​
## Conteúdo do Livro

Atualmente, o Modelo Relacional é, de longe, o modelo de dados dominante e serve de base para os SGBDs líderes do mercado, incluindo a família DB2 da IBM, Oracle, Sybase e o SQLServer, da Microsoft.

Conheça melhor sobre esse modelo de banco de dados lendo o trecho do capítulo 3 O modelo relacional do livro Sistemas de gerenciamento de banco de dados de Ramakrishnan & Gerhke, base teórica para a Unidade de Aprendizagem.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/cd203eb2-b99f-4b51-9a0b-c85bdfe050d6/bc774395-aee8-4bf4-b8cd-a6ef43bdb5dd.jpg)


## Dica do Professor

Assista ao vídeo da Dica do Professor a seguir para conhecer o conceito e a aplicação do Modelo Relacional, e a estrutura de uma instância (ou relação) e dos relacionamentos que podem ser estruturados a partir dessas informações.

​​​​​​​
## Exercícios

#### Questão 1
Quando utilizamos a linguagem SQL (padrão da indústria para banco de dados), existem vários tipos de dados que podemos utilizar na maioria dos SGBDs relacionais. Como os exemplos abaixo:
- CHAR: para entradas de texto com comprimento fixo, como por exemplo, siglas de estados, CEP e números de CPF.
- DATE/TIME: para entradas contendo valor de data e hora.
Seguindo esta relação de tipos de dados, escolha a opção a seguir que melhor descreve o tipo de dado FLOAT.
Selecione a resposta:
a. Float - para entradas que irão receber dados com dois valores, como sim e não ou verdadeiro e falso.
b. Float - para entradas que irão receber dados numéricos com precisão flutuante, como cálculo de taxas de juros e cálculos científicos.
c. Float - para entradas que irão receber dados numéricos com precisão fixa, por exemplo valores monetários.
d. Float - para entradas que irão receber dados de texto com comprimento fixo, como por exemplo, Fone e CPF.
e. Float - para entradas que irão receber dados de texto com comprimento variável, por exemplo nomes e endereços.

✅ A alternativa correta é: b: Float - para entradas que irão receber dados numéricos com precisão flutuante, como cálculo de taxas de juros e cálculos científicos.

#### Questão 2
Quando estamos analisando e projetando um banco de dados, temos de definir que tipo de dado será utilizado para cada campo de uma determinada tabela. No exemplo abaixo, temos os campos da Tabela ALUNO. Aponte qual das opções a seguir melhor descreve os tipos corretos de dados para os referidos campos da tabela:

1- Nome do aluno, 2- CPF do aluno, 3- Endereço do aluno, 4- Estado (UF), 5- Data Nascimento

Selecione a resposta:
a. Tipos: 1-VARCHAR, 2-CHAR, 3-VARCHAR, 4-CHAR, 5-DATE
b. Tipos: 1-VARCHAR, 2-FLOAT, 3-VARCHAR, 4-CHAR, 5-DATE
c. Tipos: 1-VARCHAR, 2-CHAR, 3-VARCHAR, 4-CHAR, 5-BOOLEAN
d. Tipos: 1-VARCHAR, 2-DECIMAL, 3-VARCHAR, 4-CHAR, 5-DATE
e. Tipos: 1-VARCHAR, 2-CHAR, 3- NTEGER, 4-CHAR, 5-DATE

✅ A alternativa correta é: a.


#### Questão 3
Em uma tarefa de análise, você tem de analisar uma determinada tabela de um banco de dados. Neste caso, a tabela Alunos é composta por cinco campos, sendo:  
1- id_aluno, que terá propriedade auto-incremento, 2- nome, 3- login, 4- idade, 5- média.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/abeaf40b-2031-4767-8501-145da4b40843/ab4cecbe-4d94-416b-a614-48d6f5781809.png)

Agora você precisa apontar qual das opções abaixo melhor descreve os tipos de dados corretos para cada um dos campos da tabela Alunos.
Selecione a resposta:
- a. 1-STRING  2-VARCHAR  3-VARCHAR  4-INTEGER  5-BOOLEAN
- b. 1-FLOAT   2-VARCHAR  3-VARCHAR  4-INTEGER  5-REAL
- c. 1-VARCHAR  2-VARCHAR  3-VARCHAR  4-INTEGER  5-REAL
- d. 1-INTEGER  2-VARCHAR  3-VARCHAR  4-INTEGER  5-FLOAT
- e. 1-STRING  2-VARCHAR  3-VARCHAR  4-INTEGER  5-VARCHAR

✅ A alternativa correta é: d.


#### Questão 4
Modelo Relacional retrata os dados como sendo armazenados em tabelas, similares ao formato no qual a informação é demonstrada por programas em planilhas, e seu elemento principal são as relações entre essas tabelas. Neste contexto, existem mecanismos que permitem ao modelo relacional reconhecer relações semânticas ou de utilização, como:

Selecione a resposta:
a. A restrição de chave primária (primary key), também designada de entidade
referencial, utiliza-se para, mediante o mecanismo de chaves primárias, ligar relações de bases de dados.

b. A chave estrangeira é usada para declarar um atributo ou um conjunto de atributos como chave primária de uma relação, identificando cada tupla da relação

c. A restrição de unicidade (unique) permite definir chaves alternativas fazendo com que valores de vários atributos possam se repetir em diferentes tuplos
​​​​​​​de uma relação.

d. A integridade referencial indica que os valores de uma chave estrangeira de uma
relação filha não necessita responder aos valores da chave primária da relação pai, mas necessita ter o mesmo nome que os atributos de uma chave primária
​​​​​​​a qual estes se relacionam.

e. A restrição de obrigatoriedade (não nulo ou not null) permite declarar se um ou
vários atributos de uma relação devem tomar um valor, isto é, não podem tomar
valores nulos.

✅ A alternativa correta é: a.


#### Quetão 5
Quando utilizamos a linguagem SQL (padrão da indústria para banco de dados) existem vários tipos de dado que podemos utilizar na maioria dos SGBDs relacionais. Como os exemplos abaixo:
- CHAR: para entradas de texto com comprimento fixo, como por exemplo, siglas de estados, CEP e números de CPF.
- DATE/TIME: para entradas contendo valor de data e hora.
Seguindo esta relação de tipos de dados, escolha a opção a seguir que melhor descreve o tipo de dado INTEGER.
Selecione a resposta:
a. Integer - para entradas que irão receber dados numéricos com precisão flutuante, como cálculo de taxas de juros e cálculos científicos.
b. Integer - para entradas que irão receber dados com dois valores, como sim e não ou verdadeiro e falso.
c. Integer - para entradas que irão receber dados com números inteiros, ou seja, sem vírgula.
d. Integer - para entradas que irão receber dados de texto com comprimento fixo, como por exemplo, Fone e CPF.
e. Integer - para entradas que irão receber dados numéricos com precisão fixa, por exemplo valores monetários.

✅ A alternativa correta é: c.

## Na prática

O Modelo Relacional é muito simples e elegante: um banco de dados é uma coleção de uma ou mais relações, em que cada relação é uma tabela com linhas e colunas. Essa representação tabular simples permite que até os usuários iniciantes entendam o conteúdo de um banco de dados e possibilita o uso de linguagens de alto nível para consultar os dados. As principais vantagens do modelo relacional em relação aos modelos de dados mais antigos são sua representação de dados simples e a facilidade com que mesmo consultas complexas podem ser expressas.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/cbfb71dd-4617-4c60-86ad-2923d05fef4b/7d7a9a35-421e-4071-8e5d-56b774a427fb.jpg)

​​​​​​​Embora nos concentremos nos conceitos subjacentes, também podemos citar os recursos de Data Definition Language (DDL - Linguagem de definição de dados) da SQL, a linguagem padrão para criar, manipular e consultar dados em um Sistema Gerenciando Banco de Dados (SGBD) relacional. Isso nos permite basear a discussão firmemente em termos de sistemas de banco de dados reais.


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

 Modelo Relacional
Veja mais sobre o modelo relacional como modelo lógico e conceitos de relação (tabela), atributo (coluna), tupla (linha), esquema, instância do banco, superchave, chave, chave primária e estrangeira. Além do Modelo relacional e sua base na teoria dos conjuntos, veja noções de integridade.
[Mais](https://www.youtube.com/embed/2FXgrH4h5q4)

Ramakrishnan, Raghu. Sistemas de Gerenciamento de Bancos de Dados
[Mais](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=63862509&tokenId=5a3e5b22-13ad-46cf-8802-0f084c134afc)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

Costa, Rogério Luís de Carvalho. SQL Guia Prático. 2ª edição . Brasport, 2007.

Costa, C. J. Desenvolvimento para web . ITML press/Lusocredito. 2007.

Brookshear, J. G. Ciência da Computação: Uma Visão Abrangente . Bookman Editora. 2013.

MANNINO, Michael V. Projeto, Desenvolvimento de Aplicações & Administração de Banco de Dados. 3ª ed. 2014.

RAMAKRISHNAN, Raghu; GEHRKE, Jahannes. Sistemas de Gerenciamento de Banco de Dados. 3ª ed. 2011.

Imagens utilizadas na UA
CAPA ALEXWHITE/Shuttertock SAGAH, 2014.

Figura 1 BARROS, Maurício. 2014. SAGAH, 2014.

Figura 2 RAMAKRISHNAN, Raghu; GEHRKE, Jahannes. Sistemas de Gerenciamento de Banco de Dados. 3ª Ed. Porto Alegre. McGraw Hill/Bookman. 2011.

Figura 3 ISAK55/Shuttertock


Imagens utilizadas no vídeo 
RAMAKRISHNAN, Raghu; GEHRKE, Jahannes. Sistemas de GerenciamentodeBancodeDados3ªEdPortoAlegreMcGraw

#### EQUIPE SAGAH

Coordenador(a) de Curso
Alexandre Baroni

Professor(a)
Mauricio S. de Barros

Gerente
Rodrigo Severo

Analista de Projetos
Fernanda Osório

Analistas Metodológicas
Daniela Stieh
Fernanda Zimpel

Designers Instrucionais
Cristina Perrone
Ezequiel Alves
Luana Cavalcanti
Luciana Helmann
Marcelo Steffen

Designers Gráficos
Carol Becker
Kaka Silocchi
Juarez Menegassi
Lisi Medeiros
Marcio Castellan
Rafael Zago
Thais Gliosci
Vinicius Rafael Cárcamo

