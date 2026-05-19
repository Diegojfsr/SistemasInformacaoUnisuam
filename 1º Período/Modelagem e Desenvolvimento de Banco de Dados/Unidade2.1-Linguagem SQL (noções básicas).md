## Apresentação

A linguagem SQL é dividida em duas: Linguagem de Definição de Dados (DDL) e Linguagem de Manipulação de Dados (DML). As DDLs são utilizadas para montar o banco de dados e suas tabelas, enquanto que as DMLs são utilizadas para manipular os dados armazenados no banco. Nesta Unidade de Aprendizagem, vamos tratar das principais instruções da linguagem SQL, assim como da finalidade de cada uma e sua aplicação no contexto de banco de dados.   
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Identificar as principais instruções da linguagem SQL.
- Relacionar as principais instruções SQL com a finalidade de cada uma delas.
- Construir instruções básicas utilizando a linguagem SQL.


## Desafio

Imagine que você faz parte de uma equipe de profissionais de banco de dados e lhe foi designada a tarefa de criar uma tabela para um determinado sistema de banco de dados. Sua função como DBA (Administrador de Banco de Dados) é, a partir das informações da fase de análise de requisitos (figura abaixo), criar a referida tabela, com seus campos e os tipos de dados que cada campo irá utilizar.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/10c44fb8-f32a-4f0f-bc66-5520fd540937/aa49398a-1b7a-4150-aced-9ca98b714977.png)

​​​​​A partir das informações da análise de requisitos, desenvolva o código SQL para a criação da referida tabela, campos e tipos de dados. Vamos ao trabalho!




####  ✅ Resposta ao desafio:

Considerando os tipos de dados e tamanhos especificados, aqui está um exemplo de como ficaria:

CREATE TABLE veiculo (
    num_veiculo        NUMBER(5)       NOT NULL,
    uf_veiculo         CHAR(2)         NOT NULL,
    cod_marca_veiculo  NUMBER(3)       NOT NULL,
    cod_modelo_veiculo NUMBER(5)       NOT NULL,
    num_placa          VARCHAR2(7)     NOT NULL,
    num_chassi         VARCHAR2(21)    NOT NULL,
    ano_fabricacao     NUMBER(4)       NOT NULL,
    ano_modelo         NUMBER(4)       NOT NULL,
    data_cadastro      DATE            DEFAULT SYSDATE,
    CONSTRAINT pk_veiculo PRIMARY KEY (num_veiculo)
);

Detalhes importantes:
PRIMARY KEY: Defini num_veiculo como chave primária, já que parece ser o identificador único do veículo.
VARCHAR2: Em bancos Oracle, o tipo correto é VARCHAR2. Se for outro SGBD (como MySQL ou PostgreSQL), pode ser apenas VARCHAR.
DEFAULT SYSDATE: Para data_cadastro, defini que o valor padrão seja a data atual do sistema.
NOT NULL: Coloquei restrição de obrigatoriedade nos campos que claramente não podem ficar vazios.

#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 16958642
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 19/05/26 - 19:11
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1


## Infográfico

Observe, agora, alguns conceitos que veremos nesta Unidade de Aprendizagem. Vamos conferir!

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/453fcd3a-bf3e-467c-9d88-27037aae534b/c10f6c8f-8f1a-4461-a0e5-1e2f4b6b8ad0.jpg)



## Conteúdo do Livro

O SQL teve inicio como a linguagem SQUARE do projeto "System R" da IBM. Esse projeto foi uma resposta ao interesse em banco de dados relacionais desencadeado pelo Dr. Ted Codd, pesquisador da IBM, que elaborou um artigo famoso, em 1970, sobre o tema. Atualmente, o SQL é um padrão internacional, embora nem sempre o tenha sido. Com a força da IBM por detrás do SQL, muitos imitadores usavam algumas variantes do SQL original.

Para entender melhor sobre o escopo do SQL, leia o trecho Sistemas de Gerenciamento de Banco de Dados, base teórica para esta Unidade de Aprendizagem.
Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/76dac503-d314-4120-b3e3-990c039aa05c/a5a988ed-7ada-43dd-b750-f303fb59ec4c.jpg)


## Dica do Professor

Conheça melhor o histórico da linguagem SQL, sua finalidade e principais instruções assistindo ao vídeo da Dica do Professor a seguir, que lhe auxiliará a dar seguimento a seus estudos.

​​​​​​​
## Exercícios

#### Questão 1
Sabemos que a SQL (Linguagem de Consulta Estruturada) está dividida em categorias, sendo que uma dessas categorias é a DCL (Data Control Language ou Linguagem de Controle de Dados). A DCL é uma subcategoria de instruções utilizada para o controle dos privilégios de usuários, de forma, que o administrador do banco de dados possa determinar o nível de acesso de um usuário ou objeto do banco de dados. Aponte qual das opções a seguir contém somente instruções (comandos) de DCL.​​​​​​
Selecione a resposta:
a. Create, Grant
b. Revoke, Commit
c. Drop, Revok
d. Delete, Grant
e. Grant, Revoke

✅ A alternativa correta é: e. Pois os comandos de DCL em SQL são apenas GRANT e REVOKE, usados para conceder e revogar privilégios de acesso a usuários e objetos do banco de dados.


#### Questão 2
A instrução Select faz parte da categoria DML (Linguagem de Manipulação de Dados), sendo uma instrução básica para recuperar informações de uma ou mais tabelas de um banco de dados. Existem muitas opções e tipos de instruções Select em SQL, de modo que podemos utilizar estas opções de forma gradual e conforme o cenário e a necessidade. Aponte qual das opções a seguir contém somente palavras-chave válidas para utilizar junto à instrução Select.​​​​​​
Selecione a resposta:
a. FROM, SHOW, ORDER BY
b. CREATE, WHERE, ORDER BY
c. FROM, WHERE, DESCRIBE
d. FROM, WHERE, ORDER BY
e. FROM, MODIFY, ORDER BY

✅ A alternativa correta é: d. 


#### Questão 3
A TCL (Transact Control Language ou Linguagem de Controle de Transações) é uma categoria de instruções utilizada para o controle de transações considerando um conjunto de uma ou mais operações de manipulação de dados (DML) realizadas em um banco de dados. Aponte qual das opções a seguir contém somente instruções (comandos) de TCL.​​​​
Selecione a resposta:
a. Update, Commit
b. Drop, Rollback
c. Commit, Rollback
d. Alter, Commit
e. Rollback, Delete

✅ A alternativa correta é: c. 


#### Questão 4
A partir da figura a seguir, que traz a estrutura da Tabela Pessoa_Física (simplificada), onde estão indicadas as colunas, tipo de dados e tamanho do campo, podemos imaginar qual a sintaxe de código SQL equivalente e que dará forma a tal Tabela. Aponte qual das opções a seguir contém o código/sintaxe correto para tal situação.

**![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/7c0df2f9-f967-4b13-8357-b9745430b1d5/9495d184-3ae0-452b-9f05-681084dc7709.png)**

​Selecione a resposta:
a. (num_pessoa_pf NUMBER (5),  nom_pessoa VARCHAR (30),  num_CPF NUMBER (11), dat_nascimento DATE,  idt_sexo CHAR (1));

b. CREATE TABLE Pessoa_Fisica (num_pessoa_pf NUMBER (5), nom_pessoa VARCHAR (30), num_CPF NUMBER (11), dat_nascimento DATE, idt_sexo CHAR (1));

c. CREATE TABLE Pessoa_Fisica (nom_pessoa VARCHAR (30),  num_CPF NUMBER (11),  dat_nascimento DATE,  idt_sexo CHAR (1));

d. CREATE TABLE Pessoa_Fisica (num_pessoa_pf NUMBER (5),  nom_pessoa VARCHAR (30), dat_nascimento DATE, idt_sexo CHAR (1));

e. CREATE TABLE Pessoa_Fisica (num_pessoa_pf NUMBER (5), nom_pessoa VARCHAR (30), num_CPF NUMBER (11), idt_sexo CHAR (1));

✅ A alternativa correta é: b.


#### Questão 5
Em determinadas situações, há necessidade de adicionarmos um novo campo a uma Tabela já existente. Na figura abaixo (Tabela Pessoa_Fisica), precisamos de mais um campo, onde será armazenada a UF (Unidade da Federação, ou Estado) onde a pessoa nasceu. Aponte qual das opções a seguir contém o código/sintaxe correto para tal situação.​​​​​
Selecione a resposta:
a. ALTER TABLE Pessoa_Fisica, ADD (UF_pessoa CHAR (2));
b. ALTER TABLE Pessoa_Fisica, MODIFY (UF_pessoa CHAR (2));
c. ALTER TABLE Pessoa_Fisica, DROP (UF_pessoa CHAR (2));
d. ALTER TABLE Pessoa_Fisica, DELET (UF_pessoa CHAR (2));
e. ALTER TABLE Pessoa_Fisica, CREATE (UF_pessoa CHAR (2));

✅ A alternativa correta é: a.

## Na prática

SQL é uma linguagem de banco de dados abrangente: tem instruções para definição de dados, consultas e atualizações. Logo, é uma DDL (Linguagem de Definição de Dados ) e uma DML (Linguagem de Manipulação de Dados ). Além, disso ela tem facilidades para definir visões sobre o banco de dados, para especificar segurança, autorização, para definir restrições de integridade e para especificar controles de transação.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/e6de02f1-f76c-464b-96c5-5f1de1f097ef/a0bb6710-97ed-4c47-b6c9-a7378c7874b5.jpg)

​​​​​​​Os padrões SQL mais recentes (começando com SQL:1999) são divididos em uma especificação núcleo mais extensões especializadas.

O núcleo deve ser implementado por todos os fornecedores de SGBDs que sejam compatíveis com SQL; já as extensões podem ser implementadas como módulos opcionais a serem adquiridos independentemente para aplicações de banco de dados específicas, como mineração de dados, dados espaciais, dados temporais, data warehousing e dados multimídia, entre outros.



## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

SQL Básico - Parte I
Para entender melhor, e por meio de exemplos, como é feita uma consulta SQL, acompanhe o vídeo a seguir, focado em sintaxe e operadores.
[Mais](https://www.youtube.com/embed/gFjQVLM_0Dk)

SQL Básico - Parte II
Para saber mais sobre funções embutidas na linguagem SQL, assista ao vídeo a seguir, que dá continuidade à exemplificação de uma consulta SQL.
[Mais](https://www.youtube.com/embed/hD8bmyXY494)

Introdução a Linguagem SQL: Comandos Básicos e Avançados – Parte 1
Neste artigo de Introdução à Linguagem SQL, você poderá entender que o SQL é uma linguagem simples, com um número limitado de comandos, todos estruturados e de leitura fácil, muito similar ao inglês.
[Mais](https://www.diegomacedo.com.br/introducao-a-linguagem-sql-comandos-basicos-e-avancados-parte-1/)

DDL e DML, o que é, e qual a diferença?
Para elucidar quanto à diferença entre DDL e DML, realize a leitura do texto a seguir.
[Mais](https://devtools.com.br/blog/ddl-e-dml-o-que-e-e-qual-a-diferenca/)

SQL Básico - Parte III
Confira o vídeo a seguir para aprender um pouco mais sobre expressões de ordenação e agrupamento na linguagem SQL.
[Mais](https://www.youtube.com/embed/p5Gd6u48Dn0)


Tutorial de SQL
Conheça melhor os comandos SQL utilizados mais frequentemente acessando o tutorial a seguir.
[Mais](https://www.1keydata.com/pt/sql/)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

MANNINO, Michael V. Projeto, Desenvolvimento de Aplicações & Administração de Banco de Dados. 3ª ed. 2014.

RAMAKRISHNAN, Raghu; GEHRKE, Jahannes. Sistemas de Gerenciamento de Banco de
Dados. 3ª ed. 2011.

Banco de imagens Shutterstock
SAGAH, 2015.

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
Franciane de Freitas
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



