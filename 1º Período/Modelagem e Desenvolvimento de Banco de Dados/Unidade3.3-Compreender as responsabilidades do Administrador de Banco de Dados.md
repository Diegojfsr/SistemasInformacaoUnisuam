## Apresentação

Os bancos de dados são de suma importância para as empresas no mundo moderno. Para ter sucesso em mercados tão competitivos como os atuais, é preciso evitar possíveis problemas, e isso perpassa a organização das informações por meio de um banco de dados.

Para que o banco de dados mantenha-se em pleno funcionamento e com a performance desejada, o Administrador de Banco de Dados (DBA) deverá compreender e implementar cada item pertinente a sua responsabilidade para garantir o devido funcionamento do banco.

Nesta Unidade de Aprendizagem, você vai conhecer as responsabilidades do administrador de banco de dados.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Identificar as responsabilidades do administrador de banco de dados.
- Reconhecer os comandos SQL que auxiliam o administrador de banco de dados.
- Diferenciar as responsabilidades do administrador de banco de dados e do administrador de dados.

## Desafio

Em um banco de dados de uma empresa de logística, Daniela, a DBA da empresa, tem um problema. Ela precisa que alguns usuários de cada departamento da empresa, via sistema, consigam efetuar algumas rotinas SQL no banco. Esse pedido veio da parte dos programadores do sistema. Portanto, os usuários (funcionários) da empresa, Marcos, Lais, Sandro e Ramirez, necessitam ter privilégios diferenciados nas tabelas de produtos e estoque. Descreva os procedimentos que Daniela deverá realizar para resolver o problema na empresa.
####  ✅ Resposta ao desafio:

Daniela, como DBA, precisa estruturar os procedimentos de concessão de privilégios no banco de dados de forma organizada e segura. Aqui está um passo a passo claro do que ela deve realizar:
Etapas para resolver o problema:
- Criação de usuários, Daniela deve criar contas específicas para Marcos, Lais, Sandro e Ramirez no banco de dados, vinculando cada uma ao sistema da empresa.
- Definição de papéis, em vez de conceder privilégios diretamente a cada usuário, é recomendável criar grupos de permissões para cada departamento ou tipo de acesso. Isso facilita a manutenção.
- Concessão de privilégios, Daniela deve usar comandos `GRANT` para liberar apenas os privilégios necessários nas tabelas produtos e estoque. 
- Exemplos:
	`GRANT SELECT, INSERT ON produtos TO role_vendas;`
	`GRANT SELECT, UPDATE ON estoque TO role_logistica;`
- Associação de usuários aos privilégios, Marcos, Lais, Sandro e Ramirez devem ser adicionados aos papéis correspondentes de acordo com suas funções no sistema.
- Revisão de segurança, Daniela deve garantir que nenhum usuário receba privilégios além do necessário, princípio do menor privilégio.
- Também é importante auditar acessos periodicamente.

Resultado esperado
Cada funcionário terá acesso apenas às operações que precisa realizar.
Os programadores do sistema poderão executar as rotinas SQL sem comprometer a segurança do banco.
A manutenção futura será simplificada, pois basta ajustar os roles em vez de cada usuário individualmente.

#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17297245
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 28/05/26 - 18:47
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

Acompanhe o infográfico e compreenda as responsabilidades do administrador de banco de dados, que é o responsável pela instalação, administração e manutenção dos sistemas gerenciadores de banco de dados, e do administrador de dados.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/dfc15dec-b395-4411-af96-154927860aad/7f2bff8e-fcff-488d-aa0b-52c84316eb12.png)

​​​​​​​
## Conteúdo do Livro

O DBA, administrador de banco de dados, tem um papel importante no funcionamento do banco de dados, pois o ele deverá definir a modelagem, configurar e complementar o banco. Contudo, o DBA tem muitas responsabilidades no projeto e execução do banco de dados.

Acompanhe o trecho Administração de Dados e de Banco de Dados, da obra "Projeto, Desenvolvimento de Aplicações e Administração do Banco de dados", de Michael V. Manino, que aborda o estudo das responsabilidades do administrador de banco de dados.

Boa Leitura!  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/16836b21-f254-4a1b-81e7-8260ac5ca4e6/644a7b26-ad50-4ab5-87f2-a6b166910040.jpg)

​​​​​​​​​​​​​
## Dica do Professor

Veja, na Dica do Professor, as responsabilidades do administrador de bancos de dados, profissional que deve manter a segurança, disponibilidade e eficiência da base de dados.

## Exercícios

#### Questão 1
Com relação ao administrador de banco de dados é correto afirmar que:
Selecione a resposta:
a. Desenvolve modelo de dados corporativo.
b. Negocia prazos contratuais.
c. Desenvolve aplicação para o banco.
d. Define as etapas do projeto do desenvolvimento da solução completa.
e. Cria instruções de segurança, integridade e processamento de regras.

✅ A alternativa correta é: e. Cria instruções de segurança, integridade e processamento de regras.


#### Questão 2
Com relação à segurança do banco de dados, o controle de acessos discricionário é:
Selecione a resposta:
a. Controle que o DBA tem quando acessa o banco.
b. Definição que todos usuários terão o mesmo acesso.
c. O Controle e a definição de descrição dos campos do banco.
d. Nível de privilégio de acesso a partes específicas do banco.
e. Recurso para descriminar tabelas do banco.

✅ A alternativa correta é: d. Nível de privilégio de acesso a partes específicas do banco.


#### Questão 3
Entre as alternativas abaixo, identifique as que definem responsabilidades do administrador de banco de dados.
Selecione a resposta:
a. Modelagem do banco e backup do banco de dados.
b. Modelagem da aplicação e backup do banco.
c. Administração das instâncias do banco e gerenciamento do projeto.
d. Treinar os usuários finais e documentar o banco de dados.
e. Administração do SGBD e configuração do sistema operacional.

✅ A alternativa correta é: a. Modelagem do banco e backup do banco de dados.


#### Questão 4
Comando SQL para regras de autorização discricionária:
Selecione a resposta:
a. CREAT ROLE e DROP GRANT.
b. DROP ROLE e CREAT GRANT.
c. DROP ROLE e REVOKE.
d. CREAT ROLE e DROP REVOKE.
e. INVOKE ROLE e REVOKE SELECT.

✅ A alternativa correta é: c. DROP ROLE e REVOKE.

#### Questão 5
Sabendo que é necessário criar uma ROLE para os administradores de uma empresa. Qual o comando que cria a ROLE administradores?
Selecione a resposta:
a. CREATE ROLE ADMINISTRADORES
b. CREATE TABLE ADMINISTRADORES.
c. CREATE DATABASE ADMINISTRADORES.
d. GRANT ALL ON TO ADMINISTRADORES.
e. GRANT TABLE ADMINISTRADORES.

✅ A alternativa correta é: a. CREATE ROLE ADMINISTRADORES.

## Na prática

Uma empresa agrícola do ramo de sementes está expandindo seus negócios por todo o território nacional. As informações pertinentes ao negócio, até então, estavam armazenadas em planilhas eletrônicas. No entanto, com a expansão, as planilhas passaram a não ser eficientes na organização das informações.

Para solucionar o problema, o administrador de banco de dados elaborou um banco de dados que armazenará as mesmas informações que as planilhas eletrônicas, porém, em uma gama maior e disponibilizando os dados para onde desejarem.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/6b31e8f5-76dc-436e-8c69-335e98effa84/0f5d534e-0d08-4828-a66d-a00e3a84350f.png)

​​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Você já sabe da importância do DBA para armazenar os dados de forma eficiente e segura, certo? Mas o que fazer para ser um DBA? Veja no próximo link.
[Mais](http://aprendaplsql.com/dba/o-que-fazer-para-ser-um-dba/)

Qual a função de um administrador de banco de dados?
[Mais](https://dataunique.com.br/dba/)

Saiba mais sobre as características, tecnologias utilizadas, atuação no mercado e responsabilidades de um Administrador de Banco de Dados, acessando o próximo link.
[Mais](https://targettrust.com.br/)

ADMINISTRANDO BANCO DE DADOS
[Mais](https://docente.ifrn.edu.br/josecunha/disciplinas/adbd/pdfs/apostila-de-banco-de-dados)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

MANNINO, Michael V. Projeto, desenvolvimento de aplicações e administração de banco de dados. 3. ed. Porto Alegre: AMGH, 2014.

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


