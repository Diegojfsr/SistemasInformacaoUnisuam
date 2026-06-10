## Apresentação

O volume de dados está aumentando em proporções exponenciais no mundo. Os Estados Unidos é o país em que mais circulam dados, ficando a China em segundo lugar. Também merece destaque em tráfego de dados a América Latina, o Oriente Médio e a África.
E como lidar com tanta informação? Os bancos de dados de modelos relacionais estão preparados?
Você verá, nesta Unidade de Aprendizagem, um novo conceito de banco de dados para trabalhar com grandes volumes de dados, o NoSQL.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Descrever o que são bancos de dados NoSQL.
- Listar os principais tipos e características dos bancos de dados NoSQL.
- Diferenciar o modelo relacional (SQL) e o NoSQL.



## Desafio

Para desenvolvermos uma aplicação, é necessário fazermos um levantamento de requisitos, ou seja, escrever quais as necessidades e objetivos que ela deverá atingir. Com isso, estamos construindo o domínio da aplicação, que define para que estamos criando esta solução.

O cliente Xy Ltda possui uma empresa com 50 filiais espalhadas no Brasil. Ele deseja uma aplicação que possa registrar todos os problemas e soluções encontradas em seu processo produtivo, pois haverá aumento no volume de dados.

Processo: o colaborador que se deparar com um problema pesquisará no sistema a melhor solução. Caso resolva, fará o registro da ação, ou registrará uma nova solução. Um banco de dados relacional, respeitando as formas normais, poderá conter muitos joins, com isso causando lentidão nas buscas, considerando o uso excessivo nas unidades. Pensando no desafio que é a recuperação da informação, analise o seguinte:

Você é consultor na empresa Soluções em TI e foi destinado a atender o cliente Xy Ltda. Qual solução de banco de dados recomendaria, considerando o grande volume de dados e a necessidade de performance na recuperação da informação? Indique o modelo e um banco de dados que a empresa Xy Ltda possa implantar.

#### Faça um relatório técnico que contenha os seguintes dados:
- Empresa, contato  
- Empresa consultora, consultor  
- Diagnóstico  
- Problema  
- Recomendações

####  ✅ Resposta ao desafio:

**Relatório Técnico – Levantamento de Requisitos e Recomendação de Banco de Dados**

**Dados da Empresa:**
Empresa Cliente: Xy Ltda
Contato: Diretoria de Operações

**Empresa Consultora:**
Empresa: Soluções em TI
Consultor: Seu Nome

**Diagnóstico:**
A empresa Xy Ltda possui 50 filiais distribuídas pelo Brasil, com grande volume de dados gerados diariamente no processo produtivo. O sistema solicitado deverá permitir:
- Registro de problemas encontrados no processo produtivo.
- Pesquisa de soluções já registradas.
- Inclusão de novas soluções quando não houver resposta adequada.
- O modelo relacional tradicional, embora robusto, pode apresentar lentidão nas consultas devido ao excesso de joins e ao alto volume de acessos simultâneos em múltiplas unidades.

**Problema:**
- Crescimento exponencial do volume de dados.
- Necessidade de alta performance na recuperação da informação.
- Limitações de bancos relacionais em cenários de consultas complexas e massivas.
- Risco de gargalo de desempenho e baixa escalabilidade.

**Recomendações:**
Modelo de Banco de Dados: NoSQL (orientado a documentos).
Banco de Dados Recomendado: MongoDB.

**Características:**
- Armazenamento orientado a documentos (JSON/BSON).
- Índices poderosos para busca rápida.
- Suporte a replicação e sharding (distribuição de dados).
- Comunidade ampla e suporte corporativo.

**Justificativa:**
- Melhor desempenho em consultas de grandes volumes de dados.
- Flexibilidade para armazenar problemas e soluções sem depender de esquemas rígidos.
- Escalabilidade horizontal (possibilidade de distribuir dados entre servidores).
- Redução da necessidade de joins complexos.

**Benefícios para Xy Ltda:**
- Consultas mais rápidas e eficientes.
- Facilidade de integração com aplicações modernas.
- Suporte a ambientes distribuídos, ideal para múltiplas filiais.
- Redução de custos com infraestrutura devido à escalabilidade horizontal.



Conclusão
A solução proposta é a adoção de um banco de dados NoSQL, especificamente o MongoDB, para garantir alta performance, escalabilidade e flexibilidade na recuperação das informações de problemas e soluções do processo produtivo da Xy Ltda.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17818516
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 10/06/26 - 19:17
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1


## Infográfico

Observe, no infográfico, um esquema que representa os tipos de bancos de dados NoSQL e um exemplo de banco de dados para cada modelo.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/277375f6-100e-4e46-acee-210524847bb7/ebc5056f-5e53-48a7-8eaf-21b04ec3d469.png)


## Conteúdo do Livro

No capítulo Analisar e compreender a utilização do banco de dados NoSQL, da obra Administração de Banco de Dados, você verá a diferença entre dados, informação e conhecimento, e a relação desses conceitos com o banco de dados. Além disso, aprenderá sobre Big Data e verá as principais características dos bancos de dados NoSQL.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/e851b4b7-1e83-4418-a151-f45cbb19a6cd/1422fad3-4395-4110-9410-76f4eb1c34e4.jpg)


## Dica do Professor

O banco de dados NoSQL é uma nova alternativa para solução de problemas relacionados a grandes volumes de dados, quando há a exigência de performance. Saiba mais no vídeo da Dica do Professor.


## Exercícios

#### Questão 1
Com relação a bancos de dados NoSQL, marque a afirmativa correta.
Selecione a resposta:
a. Veio para substituir os bancos de dados relacionais.
b. Os banco de dados NoSQL têm como característica a organização dos dados em tabelas.
c. O Modelo NoSQL é um tipo de gerenciador de banco de dados que conecta os registros em forma de árvore e cada tipo de registro tem apenas uma raiz.
d. NoSQL (não somente SQL), refere-se à solução de banco de dados que possibilita o armazenamento de uma grande variedade de dados existentes, não se limitando apenas a modelos relacionais.
e. As empresas que optam pelo uso de NoSQL devem eliminar o trabalho com outros modelos de bancos de dados.

✅ A alternativa correta é: d.


#### Questão 2
Marque a alternativa correta referente a bancos de dados NoSQL.
Selecione a resposta:
a. O modelo NoSQL normaliza dados em estruturas tabulares.
b. Sistemas de gerenciamento de bancos de dados NoSQL são compatíveis com um conjunto de propriedades definido pela sigla ACID.
c. Bancos de dados não relacionais (NoSQL) normalmente não aplicam um schema.
d. Bancos de dados NoSQL são mais fáceis de aumentar a escala "verticalmente" com hardware mais rápido.
e. Em bancos de dados NoSQL as solicitações para armazenar e recuperar dados são comunicadas usando consultas compatíveis com structured query language (SQL).

✅ A alternativa correta é: c.


#### Questão 3
De acordo com as características dos bancos de dados NoSQL, pode-se afirmar que:
Selecione a resposta:
a. A característica ausência de esquema (Schema-free) ou esquema flexível é outra forma de prover a escalabilidade em bancos de dados NoSQL.
b. Ausência de esquema garante a integridade dos dados.
c. Na consistência eventual, o foco não está no armazenamento dos dados e sim como recuperar estes dados de forma eficiente.
d. Map/reduce suporta mecanismos de armazenamento e recuperação, onde a quantidade de sites está em constante mudança.
e. Vector clocks cria um vetor para o armazenamento de dados.

✅ A alternativa correta é: a.


#### Questão 4
Referente aos tipos de bancos de dados NoSQL. Marque a afirmativa correta.
Selecione a resposta:
a. Bancos de dados colunares são projetados para armazenar dados como documentos.
b. Chave/Valor são projetados para armazenar dados como documentos.
c. Banco de dados orientado a documentos armazenam vértices e links direcionados chamados de bordas.
d. O banco de dados orientado a documentos armazena pedaços críticos de dados na memória para acesso de baixa latência.
e. Bancos de dados orientado a grafos podem ser construídos em ambos os modelos de bancos de dados, relacionais e NoSQL.

✅ A alternativa correta é: e.

#### Questão 5
Existem muitos bancos de dados para se trabalhar com NoSQL, cada banco está associado a um determinado tipo do NoSQL. Marque a alternativa em que todos os bancos de dados estão associados ao seu respectivo tipo.
Selecione a resposta:
a. Baseado em documentos: MongoDB, CouchDB, BigCouch e RavenDB.
b. Baseado em grafos: Cassandra e Hypertable.
c. Baseado em chave-valor: Neo4J e Infinite Graph.
d. Baseado em documentos: Dynamo, Azure Table Storagee e Couchbase Server.
e. Baseado em coluna: Amazon SimpleDB, Cloudata, Cloudera, SciDB, HPCC e Stratosphere.

✅ A alternativa correta é: a.



## Na prática

Veja na prática, a construção de um banco de dados em MongoDB, que trata-se de um banco de dados NoSQL orientado a documentos. Para a apresentação de um exemplo prático, será feito um cadastro para professores, guardando dados referentes ao nome, e-mail e telefone.

No intuito de fazer uma comparação com o modelo relacional, primeiramente este cenário será aplicado em um banco de dados SQL.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/c0e5c758-eea8-4227-94dd-565f527ab25a/584c316d-e75f-44c7-a6dd-60b568e2d7db.png)

​​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:


Acompanhe, a seguir, uma entrevista com Eduardo Morelli, coordenador do curso de Pós-graduação em Big Data do Instituto Infnet, do Rio de Janeiro, falando sobre NoSQL e Bigdata.
[Mais](https://www.youtube.com/embed/DVRs_UEIBg8)

Você sabe o que é MongoDB e para o que serve? Veja mais clicando no próximo link.
[Mais](https://codigosimples.net/2016/03/01/o-que-e-mongodb-e-porque-usa-lo)

Neste vídeo você poderá saber mais sobre aplicações com um banco de dados NoSQL.
[Mais](https://www.youtube.com/embed/Xk0flFHMRDg)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

Não tem referências:

RELATÓRIO TÉCNICO 
Empresa avaliada: Xy ltda 
Contato: José 
Empresa consultora: Soluções em TI 
Consultor: Nome aluno 
Diagnóstico:
Analisando os processos da empresa percebe-se o grande fluxo de dados em suas rotinas diárias. A empresa trabalha com estrutura de armazenamento baseado em modelos relacionais. 
Problema:
O modelo de bancos de dados relacional, apesar de suas características estarem disseminadas e aceitas no mercado por tratar-se de um paradigma consolidado no processo de armazenamento e manipulação de dados, apresenta lentidão no momento de tráfego intenso por parte dos colaboradores que utilizam a rede da empresa. Portanto, é crucial o uso de novas técnicas e ferramentas para que se possa obter uma melhor escalabilidade. 
Recomendações:
Recomendamos o uso de bancos de dados NoSQL, por possuir técnicas de escalabilidade horizontal, com isso reduzindo custos e aumentando a velocidade na recuperação de dados. Entre os modelos, recomendamos o modelo “Orientado a documentos” por ser um modelo que suporta as consultas com maior eficiência. Exemplo de indicação de banco: MongoDB. Por tratar-se de um dos bancos de dados orientados a documentos mais popular do mercado. É uma ferramenta Open Source, com isso diminuindo custos de aquisição de licenças. Possui vasta documentação.



