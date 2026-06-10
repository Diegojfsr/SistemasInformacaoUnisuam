## Apresentação

Nesta Unidade de Aprendizagem, será analisado o contexto de um cenário real em relação à necessidade de um futuro sistema de informação, identificando o modelo conceitual para atender ao Estudo de Caso e construindo este modelo utilizando a ferramenta brModelo.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Detalhar o contexto de um cenário real de necessidade de sistema de informação.
- Identificar o modelo conceitual para atender o Estudo de Caso.
- Construir o modelo conceitual utilizando a ferramenta brModelo.


## Desafio

Imagine que você faz parte de uma equipe de TI que terá que desenvolver um sistema de informação baseado em banco de dados para atender a um determinado cliente. Este cliente é uma empresa de rádio táxi que atende de forma on-line e tem, de maneira geral, as seguintes características:  

- A empresa possui, aproximadamente, 100 veículos (táxis) cadastrados.
- O cadastro do veículo requer um conjunto pré-definido de informações.
- O veículo pode ser próprio ou de taxistas parceiros.
- Os motoristas devem ter um cadastro junto à empresa.
- A empresa de rádio táxi possui uma central única de atendimento e atende determinadas cidades.
- A empresa mantém cadastro de empresas (clientes) conveniadas e pessoas autorizadas a solicitar os serviços.
- A realização dos chamados se dá via telefone.
- O pagamento dos serviços se dá via boleto bancário.
- Após receber a chamada, a central de atendimento verifica e determina qual táxi/motorista irá atender.
- O valor final das faturas são o somatório das corridas/serviços utilizados durante o mês.
- Após a automatização do sistema, a empresa de rádio táxi espera agilizar as tarefas de manutenção de dados e dispor de diversos relatórios para apoio na gestão.

Agora, a partir das informações expostas e do modelo em anexo, você precisa criar o esquema conceitual na ferramenta brModelo.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/e1773206-cb1a-444d-b928-6fcb7a30a90f/ea20b14f-f624-4192-8855-3feee11def53.jpg)


####  ✅ Resposta ao desafio:

Entidades principais:
**VEÍCULO**
Atributos: Número do veículo, Placa, Marca, Ano de fabricação, Ano do modelo, Tipo (próprio/parceiro).

**MOTORISTA**
Atributos: Número do motorista, Nome, Data de nascimento, Sexo, Telefone.
Relacionado a ENDEREÇO e CARTEIRA HABILITAÇÃO.

**ENDEREÇO**
Atributos: Logradouro, Número, CEP, Bairro, Cidade, Estado.

**CARTEIRA HABILITAÇÃO**
Atributos: Número da CNH, Categoria, Data de emissão, Data de validade.

**CHAMADO**
Atributos: Número do chamado, Data, Hora, Telefone de contato, Local de origem, Local de destino.

**CLIENTE**
Atributos: Código do cliente, Nome, Tipo (empresa/pessoa), Telefone, Endereço.
Empresas conveniadas e pessoas autorizadas entram aqui.

**BOLETO**
Atributos: Número do boleto, Empresa conveniada, Valor, Data de emissão, Data de vencimento.

**FATURA**
Atributos: Número da fatura, Período de referência, Valor total.
Representa o somatório dos boletos/corridas no mês.

Relacionamentos
**CHAMADO → CLIENTE**
Um cliente realiza chamados (1.N).

**CHAMADO → VEÍCULO**
Um chamado é atendido por um veículo (1.1).

**VEÍCULO → MOTORISTA**
Um veículo é dirigido por um motorista (1.1).

**MOTORISTA → CARTEIRA HABILITAÇÃO**
Cada motorista possui uma carteira de habilitação (1.1).

**MOTORISTA → ENDEREÇO**
Cada motorista tem um endereço (1.1).

**CHAMADO → BOLETO**
Cada chamado gera um boleto (1.1).

**CLIENTE → FATURA**
Cada cliente recebe uma fatura mensal (1.N).
A fatura é composta pelo somatório dos boletos.

Observações importantes
O CLIENTE é central, pois pode ser pessoa física ou empresa conveniada.
O CHAMADO é o ponto de partida: gera vínculo com veículo, motorista e boleto.
A FATURA é uma entidade derivada, que consolida os boletos de um cliente em determinado período.
O atributo “Tipo de veículo” diferencia táxis próprios dos parceiros.




#### Descrição textual estruturada.
Usado diretamente para montar o esquema conceitual no brModelo:

Entidades e atributos
VEÍCULO
Número do veículo
Placa
Marca
Ano de fabricação
Ano do modelo
Tipo (próprio/parceiro)

MOTORISTA
Número do motorista
Nome
Data de nascimento
Sexo
Telefone

ENDEREÇO
Logradouro
Número
CEP
Bairro
Cidade
Estado

CARTEIRA HABILITAÇÃO
Número da CNH
Categoria
Data de emissão
Data de validade

CHAMADO
Número do chamado
Data
Hora
Telefone de contato
Local de origem
Local de destino

CLIENTE
Código do cliente
Nome
Tipo (empresa/pessoa)
Telefone
Endereço

BOLETO
Número do boleto
Empresa conveniada
Valor
Data de emissão
Data de vencimento

FATURA
Número da fatura
Período de referência
Valor total

Relacionamentos
CLIENTE realiza CHAMADO - 1 cliente pode realizar vários chamados (1:N).
CHAMADO é atendido por VEÍCULO - cada chamado é atendido por um veículo (1:1).
VEÍCULO é dirigido por MOTORISTA - cada veículo é associado a um motorista (1:1).
MOTORISTA possui CARTEIRA HABILITAÇÃO - todo motorista tem uma carteira de habilitação (1:1).
MOTORISTA tem ENDEREÇO - cada motorista possui um endereço (1:1).
CHAMADO gera BOLETO - cada chamado gera um boleto (1:1).
CLIENTE recebe FATURA - cada cliente recebe várias faturas (1:N).
FATURA consolida BOLETOS - uma fatura é composta pelo somatório dos boletos do período (N:1).

Observações
O CLIENTE pode ser pessoa física ou empresa conveniada.
O CHAMADO é o ponto inicial do processo, conectando cliente, veículo, motorista e boleto.
A FATURA é uma entidade derivada, consolidando os boletos mensais.
O atributo “Tipo” em VEÍCULO diferencia táxis próprios dos parceiros.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17822984
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 10/06/26 - 20:21
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

Uma ação comum de refinamento de um DER é dividir os atributos compostos em atributos menores. Um atributo composto contém vários tipos de dados. Observe, no infográfico a seguir, um exemplo do que veremos nesta Unidade de Aprendizagem.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/a8774f05-961d-4b9a-9b87-ccf5abb75f4d/1b96ffb0-c771-4ac6-a209-e1306f6401ac.jpg)


## Conteúdo do Livro

Geralmente, a modelagem de dados é um processo interativo ou repetitivo. Você constrói um modelo de dados preliminar e, então, o refina várias vezes. No refinamento de um modelo de dados, você deve gerar alternativas viáveis e avaliá-las de acordo com as necessidades do usuário.

Aprenda mais sobre esse processo lendo o trecho do livro Projeto, desenvolvimento de aplicações e administração de banco de dados, base teórica para esta Unidade de Aprendizagem.
​​​​​​​

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/db84bad9-fd30-4f07-9139-3c440025493e/e58a8dca-a37f-405d-83d7-4f4d11b7d6e6.jpg)


## Dica do Professor

No vídeo a seguir, você poderá observar como é utilizada a ferramenta de modelagem de dados brModelo 3.0 para o desenvolvimento de um esquema/modelo conceitual de dados. 

​​​​​​​
## Exercícios

#### Questão 1
Quando tratamos de modelos/esquemas conceituais e lógicos, existem processos chamados de refinamentos de Diagrama Entidade e Relacionamento (DER). Estes refinamentos são, na verdade, transformações. Estas transformação podem tornar mais fácil referenciar um tipo de entidade após a conversão em tabelas. Após a conversão, uma referência a uma entidade fraca envolverá uma chave estrangeira combinada com mais de uma coluna. A partir do exposto, qual das opções a seguir aponta corretamente este processo de refinamento?
Selecione a resposta:
a. Transformando uma entidade fraca em uma entidade forte.
b. Dividindo atributos compostos.
c. Expandindo tipos de entidades.
d. Adicionando histórico.
e. Adicionando hierarquias de generalização.

✅ A alternativa correta é: a.

#### Questão 2
Quando utilizamos a ferramenta de modelagem brModelo 3.0, há vários tipos de atributos que podemos usar. Quando da montagem de uma entidade, podemos definir as chamadas chaves primárias no contexto de um modelo/esquema conceitual. Aponte qual das alternativas a seguir trata corretamente do nome que se dá ao atributo que representa a chave primária.
Selecione a resposta:
a. Atributo (somente).
b. Atributo identificador.
c. Atributo multivalorado.
d. Atributo composto.
e. Atributo opcional.

✅ A alternativa correta é: b.


#### Questão 3
Uma ação comum de refinamento de um DER é dividir os atributos XXXXXXXX em atributos menores. Este tipo de atributo contém vários tipos de dados. Por exemplo, o tipo de entidade Consumidor possui um atributo de endereço que contém dados sobre rua, cidade, estado e código postal dos consumidores. A divisão de atributos XXXXXXXX pode facilitar a busca por dados embutidos. A partir do exposto, aponte qual das alternativas a seguir trata corretamente da nomenclatura do tipo de atributo citado.
Selecione a resposta:
a. Atributo identificador.
b. Atributo opcional.
c. Atributo composto.
d. Atributo multivalorado.
e. Atributo (somente).

✅ A alternativa correta é: c.


#### Questão 4
Quando tratamos de modelos/esquemas conceituais e lógicos, existem processos chamados de refinamentos de Diagrama Entidade e Relacionamento (DER). Estes refinamentos são, na verdade, transformações, como, por exemplo, dividir um tipo de entidade em dois tipos de entidades e relacionamentos. Esta transformação pode ser útil ao registrar um nível mais fino de detalhamento sobre uma determinada entidade. A partir deste exposto, qual das opções a seguir aponta corretamente o nome deste processo de refinamento?
Selecione a resposta:
a. Dividindo atributos compostos.
b. Transformando atributos em tipos de entidades.
c. Adicionando histórico.
d. Expandindo tipos de entidades.
e. Adicionando hierarquias de generalização.

✅ A alternativa correta é: d.


#### Questão 5
Quando utilizamos a ferramenta de modelagem brModelo 3.0, há uma funcionalidade que permite fazer o link entre entidades e relacionamentos. Aponte qual das alternativas a seguir trata corretamente do nome que se dá a esta funcionalidade.
Selecione a resposta:
a. Conectar objetos.
b. Refinar objetos.
c. Atribuir objetos.
d. Identificar objetos.
e. Ligar objetos.

✅ A alternativa correta é: e.

## Na prática

Projeto Conceitual:  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/eb298e01-a6b9-4db2-8fbb-53d24b2c1d2d/3170f532-a72d-47c5-bf3a-4a868ee72129.jpg)

O Projeto Conceitual é baseado na especificação de requisitos criada anteriormente. É gerado um esquema conceitual do banco de dados, partindo do conjunto de informações. Esquema conceitual é, de modo geral, uma visão macro do banco de dados, uma descrição de alto nível da estrutura e das necessidades. Os modelos de Entidade-Relacionamento são bastante utilizados para descrever estes esquemas conceituais.

Importante:
Nesta fase, descreve-se o conteúdo de informação, não a estrutura onde elas serão armazenadas (tabelas, colunas, visões, etc).

## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Para reforçar seu conhecimento sobre criação de um banco de dados, iniciando pela modelagem e incluindo uma entidade fraca até a criação de um formulário, assista ao vídeo a seguir, que mostra o funcionamento na prática.
[Mais](https://www.youtube.com/embed/DHT4nYWsve8)

Aprenda como criar um projeto de banco de dados conferindo o artigo a seguir.
[Mais](https://www.dicasdeprogramacao.com.br/como-criar-um-projeto-de-banco-de-dados/)

Assista ao vídeo a seguir para entender como construir um modelo de banco de dados conceitual utilizando BRModelo. O vídeo exemplifica todas as etapas da construção, desde construir entidades com chave primária, especialização ou generalização.
[Mais](https://www.youtube.com/embed/sItFiqAN5YY)

Projeto, Desenvolvimento de Aplicações e Administração de Banco de Dados
Mannino, Michael V.
[Mais](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=63862526&tokenId=291615ed-85e2-45e0-a516-b3cfa2f728df)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

MANNINO, Michael V. Projeto, Desenvolvimento de Aplicações & Administração de Banco de Dados. 3ª ed. 2014.

PUGA, Sandra; FRANÇA, Edson; GOYA, Milton. Banco de dados: implementação em SQL,
PL/SQL e Oracle 11g. São Paulo. Pearson Education do Brasil, 2013.

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
