## Apresentação

A linguagem SQL possui algumas estruturas que permitem a criação de lógicas avançadas. Por exemplo, os comandos IF-ELSE, WHILE e CASE. Além disso, o uso de rotinas na programação de banco de dados fornece grandes benefícios em termos de segurança, modularidade e desempenho. Stored Procedures são blocos de código PL/SQL armazenados no servidor, que não retorna valor. Eles permitem que aplicações façam chamadas desses blocos, sem precisar descrever todos os comandos. Já as Functions, diferentemente das Stored Procedures, retornam valores. Da mesma forma, devem ser chamadas pela aplicação. Além dessas duas estruturas, temos as Triggers, que são os "gatilhos" que disparam comandos após determinados eventos.  

Nesta Unidade de Aprendizagem você vai ver o uso dessas estruturas na prática e entenderá melhor a importância, bem como os melhores momentos de utilizá-los.
Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir a estrutura de programação de tabela.
- Aplicar estruturas avançadas do SQL (IF-ELSE, WHILE, CASE, procedures, triggers, functions).
- Reconhecer a sintaxe da linguagem SQL.


## Desafio

Quando trabalhamos com o armazenamento de dados em um Banco de Dados, é muito comum a utilização de dados numéricos dos mais diversos tipos, com mais ou menos dígitos, com casas decimais ou não. A escolha correta do tipo de dado impacta no tamanho do espaço ocupado no banco de dados. Mesmo que o número seja pequeno, se a tabela espera um número grande, ocupará um espaço maior na memória e no disco.

Você é profissional da área de TI e ficou resposável de treinar um novo profissional na empresa em que trabalha. Liste para esse colega os tipos de dados numéricos possíveis de serem trabalhados em um Banco de Dados, colocando ao lado de cada um o tamanho dos dados que podem receber.

####  ✅ Resposta ao desafio:

SMALLINT, número inteiro binário com uma precisão de 15 bits.
INTEGER, número inteiro binário com uma precisão de 31 bits.
BIGINT, número inteiro binário com precisão de 63 bits.
REAL, número de ponto flutuante curto 32 bits.
DOUBLE ou FLOAT, número de ponto flutuante longo 64 bits.
DECIMAL ou NUMERIC, número decimal compactado com um ponto decimal implícito.
DECFLOAT, número de ponto flutuante decimal é de 34 dígitos.


Os principais tipos de dados numéricos em bancos de dados SQL são TINYINT, SMALLINT, INT, BIGINT, DECIMAL/NUMERIC, FLOAT, DOUBLE e REAL. Cada um possui tamanhos e faixas diferentes, e a escolha correta evita desperdício de espaço e garante precisão nos cálculos.

TINYINT - 1 byte
SMALLINT -	2 bytes
INT - 4 bytes
BIGINT - 8 bytes
DECIMAL/NUMERIC - Dependente da precisão definida(DECIMAL(10,2) até 10 dígitos, 2 decimais)
FLOAT - 4 bytes
DOUBLE - 8 bytes
REAL - 4 bytes (Varia conforme SGBD)


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17255722
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 27/05/26 - 19:13
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

Veja, no infográfico a seguir, alguns exemplos práticos do uso de Procedure, Triggers e Functions, a partir dos comandos e sua descrição.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/da0a9f08-d652-40a2-83b4-f067846f08a0/161430b2-9c98-476d-96ef-3240dc416180.jpg)

​​​​​​​
## Conteúdo do Livro

Quando utilizamos a Structured Query Language, mais conhecida como a linguagem SQL, somos capazes de estipular a estrutura de armazenamento em bancos de dados, incluindo operações de inserção, consulta, alteração e remoção de informações. Tais ações são inestimáveis para sustentar toda a integridade e dinâmica dos dados em um sistema.

No capítulo Práticas de programação em banco de dados, base teórica desta Unidade de Aprendizagem, você vai explorar os alicerces da linguagem SQL voltados a criar e manipular dados em bancos relacionais. Por meio de exemplos práticos no MySQL Workbench, você vai observar a execução dos comandos essenciais CREATE, INSERT, SELECT, UPDATE e DELETE, conhecimento este que fortalece habilidades indispensáveis ao profissional de tecnologia.

Boa leitura.
​​​​​​
![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/76152/Pa_ginas_de_11506_Praticas_programacao_bancos_dados_FINAL-2025-12-18T17:14:02-03:00.jpg)


## Dica do Professor

O vídeo a seguir apresenta exemplos práticos do uso de estruturas de SQL como IF ELSE, WHILE, CASE, Procedures, Funcions e Triggers.

## Exercícios

#### Questão 1
Como se chama a linguagem de Banco de Dados para a criação e modificação das tabelas?
Selecione a resposta:
a. DML (Linguagem de Manipulação de Dados).
b. SSL (Linguagem de Segurança de Dados).
c. WIFI (Linguagem de Dados Sem Fio).
d. DDL (Linguagem de Definição de Dados).
e. DLC (Linguagem de Cálculo de Dados).

✅ A alternativa correta é: d. DDL (Linguagem de Definição de Dados).


#### Questão 2
O que são Constraints?
Selecione a resposta:
a. Comandos para fusão de duas ou mais tabelas na consulta.
b. Restrições estabelecidas em uma coluna.
c. Dados pré-definidos para data e hora.
d. Recurso de atualização de dados de um campo.
e. Implementação de performance no Banco de Dados.

✅ A alternativa correta é: b. Restrições estabelecidas em uma coluna.


#### Questão 3
Qual a diferença entre Primary Key e Foreign Key?
Selecione a resposta:
a. Primary Key é sempre a primeira coluna de uma tabela e a Foreign Key a última.
b. Primary Key é a senha de segurança primária do Banco de Dados e Foreign Key é a senha exportada.
c. Primary key são os dados importados e Foreign Key os dados exportados.
d. Primary Key é utilizada como índice da tabela e Foreign Key é utilizada para relacionamento entre tabelas.
e. Primary Key é utilizada apenas para caracteres de texto e Foreign Key para números nos valores dos dados.

✅ A alternativa correta é: d. Primary Key é utilizada como índice da tabela e Foreign Key é utilizada para relacionamento entre tabelas.


#### Questão 4
Qual a função de Identity ou Auto Increment?
Selecione a resposta:
a. Fazer o relacionamento entre duas tabelas.
b. Gerar a numeração automática das linhas.
c. Fazer a validação dos dados das colunas.
d. Realizar as rotinas automáticas de manutenção de Banco de Dados.
e. Armazenar números com mais de três casas decimais.

✅ A alternativa correta é: b. Gerar a numeração automática das linhas.

#### Questão 5
O que ocorre quando se utiliza o parâmetro Not Null na construção das colunas?
Selecione a resposta:
a. Impede a atualização de valor.
b. Permite apenas caracteres de texto.
c. Atualiza sempre para a data atual.
d. Não permite números negativos.
e. Impede que cadastre um campo vazio.

✅ A alternativa correta é: e. Impede que cadastre um campo vazio.


## Na prática

Lucas é DBA em uma empresa. Para que o desenvolvimento e a programação de um Banco de Dados seja estável e produtiva, o profissional adota uma série de boas práticas nessa programação. Através das boas práticas, uma série de problemas podem ser evitados e a manutenção dos dados se torna bem mais simples.

Vejas as boas práticas adotadas pelo DBA, clicando nas palavras:

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/dfb748cf-ba7b-45a6-ad69-ff7d47361b29/313a1bb7-ae3d-42d4-850e-bf6a45be1074.jpg)

​​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Desenvolvendo um plano de banco de dados
Saiba como desenvolver um Plano de Banco de Dados, que é a primeira etapa para a criação de um banco de dados e serve como um guia a ser utilizada na implementação.
[Mais](https://learn.microsoft.com/pt-br/previous-versions/sql/sql-server-2008-r2/ms177460(v=sql.105))

Sistemas de Gerenciamento de Bancos de Dados
Ramakrishnan, Raghu; Gehrke, Johannes
[Mais](https://bibliotecaa.grupoa.com.br/lti/launch.php?bookid=9788563308771)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

RAMAKRISHNAN, R.; GEHRKE, J. Sistemas de gerenciamento de bancos de dados. 3. ed.
São Paulo: McGraw-Hill, 2008. 

Banco de imagens Shutterstock.
SAGAH, 2017.

#### EQUIPE SAGAH

Coordenador(a) de Curso
Roberto Litel

Professor(a)
Rubens Albuquerque

Gerente Unidade de Negócios
Rodrigo Severo

Núcleo de Projetos
Fernanda Osório
Luciana Bolzan

Núcleo de Marketing
Juliana Ulbrich Santos

Núcleo de Implementação
Maurício Robson Ribeiro
Taila Messias Vanzelloti

Núcleo Metodológico
Daniela da Graça Stieh

Núcleo de Design Instrucional
Adriana Ferreira Cardoso
Bianca Basile Parracho
Daniela Polycarpy
Ezequiel Alves
Fernanda Flores
Franciane de Freitas
Luciana Helmann
Marcelo Steffen

Núcleo de Design Gráfico
Carol Becker
Eduardo Reis
Juarez Menegassi
Kaka Silocchi
Luis Carlos Thomaz
Renata Goulart
Vinicius Rafael Cárcamo


