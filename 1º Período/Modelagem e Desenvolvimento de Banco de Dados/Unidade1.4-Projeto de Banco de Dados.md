## Apresentação

Nessa Unidade de Aprendizagem, vamos tratar das etapas de construção de um projeto de banco de dados. Além disso, vamos abordar os conceitos do modelo ER e os principais elementos que o compõem.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Identificar os principais conceitos do modelo ER.
- Reconhecer a terminologia utilizada em um banco de dados relacional.
- Relacionar quais são as principais etapas da construção de um projeto de banco de dados.

## Desafio

Imagine que você é um analista de negócios de uma organização. Você terá que analisar a representação a seguir e, a partir dela, separar os itens adicionais em dois grupos: entradas e saídas. Veja que, da sua análise, se dará a etapa inicial do projeto de banco de dados –a análise de requisitos. Essa será a base para o desenvolvimento de todo o restante do projeto. Vamos ao trabalho!

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/2ee65fae-9a45-4003-8758-6b3a5a126e9e/29af61fa-f63d-495c-b2a9-71b001844577.jpg)

Itens (lembre que você terá que separá-los em entradas e saídas):  
- Endereço do estudante.  
- Resultado da análise de dados cadastrais.  
- Boleto para pagamento.  
- Endereço para cobrança.  
- Renda familiar.  
- Solicitação de mais informações sobre o estudante.  
- Curso pretendido pelo estudante.  
- Retorno negativo à proposta do estudante.  
- Universidade pretendida pelo estudante.  
- Notificação de aceite para a universidade.

####  ✅ Resposta ao desafio:


Como analista de negócios, a primeira etapa da análise de requisitos é justamente separar os itens em entradas e saídas. Aqui está a classificação dos elementos adicionais:
Classificação de Entradas e Saídas:

As entradas são dados fornecidos pelo estudante ou coletados no ambiente externo, que alimentam o sistema.
Endereço do estudante, Renda familiar, Curso pretendido pelo estudante e Universidade pretendida pelo estudante.

As saídas são informações ou documentos gerados pelo sistema após o processamento, retornando ao ambiente externo.
Resultado da análise de dados cadastrais, Boleto para pagamento, Endereço para cobrança, Solicitação de mais informações sobre o estudante, Retorno negativo à proposta do estudante e Notificação de aceite para a universidade.

Essa separação é fundamental porque define quais dados precisam ser armazenados no banco e quais processos devem gerar resultados para os usuários e instituições.

#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 16841616
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 15/05/26 - 18:58
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1


## Infográfico

Veja agora um esquema resumido do que veremos nesta Unidade de Aprendizagem. Vamos conferir!

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/4b352477-6b6b-421e-9ff4-98ebd52e89a0/fd5242b6-8466-4410-8d4c-e307c3c21601.png)


## Conteúdo do Livro

Iniciamos nossa discussão sobre projeto de banco de dados observando que esta é, tipicamente, apenas uma parcela – embora seja uma parte central nos aplicativos que fazem uso intensivo de dados – de um projeto maior de sistema de software.  
  
Entenda melhor lendo o trecho do livro Sistemas de gerenciamento de banco de dados, base teórica para essa Unidade de Aprendizagem.

Boa leitura.  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/15344045-e39c-4f28-8311-a987cba1096c/e5e68427-ff28-4351-b3ce-05ff9db032b8.jpg)

​​​​​​
## Dica do Professor

O vídeo a seguir trata das etapas de um projeto de banco de dados: análise de requisitos, projeto conceitual, projeto lógico e projeto físico. Além disso, traz uma visão de negócio do projeto de banco de dados.


## Exercícios

#### Questão 1
Um projeto de banco de dados é subdividido em etapas em que o objetivo é a criação de um banco de dados otimizado que atenda às expectativas do cliente. Nesse contexto, os modelos de dados são muito importantes para a transmissão de ideias entre o cliente e o projetista, assim como para facilitar a manutenção do banco de dados no futuro. A primeira etapa é chamada de Análise de Requisitos. Aponte qual das opções a seguir melhor define essa etapa.
Selecione a resposta:
a. A primeira etapa do projeto de banco de dados é o esquema conceitual, que nada mais é do que uma visão macro do banco de dados, uma descrição de alto nível da estrutura. Os modelos de entidade-relacionamento (ER) são muito utilizados para descrever os esquemas conceituais.

b. A primeira etapa do projeto de banco de dados é a identificação dos requisitos que este deve atender. Nessa fase, realizam-se entrevistas com as pessoas envolvidas no processo e cria-se uma descrição textual macro do processo. Este é o momento em que as regras de negócio devem ser identificadas.

c. A primeira etapa do projeto de banco de dados é a modelagem de dados, onde são definidas questões técnicas, como o tipo de SGBD e a estrutura de hardware a ser utilizada no projeto.

d. A primeira etapa é a que mapeia o conceito dos modelos de entidade-relacionamento em objetivos de bancos de dados. Nesta fase, criamos os modelos internos de bancos de dados, com detalhes sobre tabelas, relacionamentos, regras, metadados das colunas (tipo, tamanho, obrigatoriedade, entre outros), visões, etc.

e. A primeira etapa é a que se definem detalhes técnicos da implementação do banco de dados como, por exemplo a forma como os dados serão armazenados, os scripts para a criação dos objetos no banco de dados (tabelas, visões, colunas, funções, entre outros), permissão de acesso de usuário, etc.

✅ A alternativa correta é: b.


#### Questão 2
O projeto de banco de dados é, basicamente, dividido em projeto conceitual, projeto lógico e projeto físico – além de uma etapa anterior, normalmente chamada de análise de requisitos. A partir dessa estrutura, aponte qual das opções a seguir melhor define a etapa Projeto Conceitual.
Selecione a resposta:
a. O Projeto Conceitual trata das entrevistas com as pessoas envolvidas no processo. Cria-se uma descrição textual macro do processo e modelos externos (que devem ser entendidos por todos). Este é o momento em que as regras de negócio devem ser identificadas.

b. O Projeto Conceitual é a etapa em que mapeamos o conceito dos modelos de entidade-relacionamento em objetivos de bancos de dados. Nesta fase, criamos os modelos internos de bancos de dados, com detalhes sobre tabelas, relacionamentos, regras, metadados das colunas (tipo, tamanho, obrigatoriedade, entre outros), visões, etc.

c. O Projeto Conceitual baseia-se na especificação de requisitos criada na etapa anterior. A partir deste insumo de informações, é gerado um esquema conceitual do banco de dados. Esquema conceitual é uma visão macro do banco de dados, uma descrição de alto nível da estrutura.

d. O Projeto Conceitual é a parte final do projeto de banco de dados. Nesta etapa, definem-se detalhes técnicos da implementação do banco de dados e são realizadas entrevistas com os usuários. Além disso, se define qual SGBD será utilizado.

e. O Projeto Conceitual é a parte final do projeto de banco de dados. Nesta etapa, definem-se detalhes técnicos da implementação do banco de dados como, por exemplo, a forma como os dados serão armazenados, os scripts para a criação dos objetos no banco de dados, a permissão de acesso de usuário, etc.

✅ A alternativa correta é: c.


#### Questão 3
`__________` é a etapa em que mapeamos o conceito dos modelos de entidade-relacionamento em objetivos de bancos de dados. Nesta fase, criamos os modelos internos de bancos de dados, com detalhes sobre tabelas, relacionamentos, regras, metadados das colunas (tipo, tamanho, obrigatoriedade, entre outros), visões, etc. Ao final, o resultado é um esquema do banco de dados próximo ao modelo conceitual. Qual das opções a seguir melhor define esta etapa?
Selecione a resposta:
a. Projeto Lógico.
b. Projeto Físico.
c. Projeto Conceitual.
d. Análise de Requisitos.
e. Análise de necessidades dos usuários.

✅ A alternativa correta é: a.


#### Questão 4
No ano de 2013, surgiu o termo Big Data, que rapidamente se popularizou e trouxe novidades ao mundo da tecnologia da informação. O Big Data representa uma infinidade de informações não estruturadas que, quando usadas com inteligência, tornam-se uma arma poderosa para empresas analisarem cenários e tomarem decisões com probabilidade de sucesso cada vez maior. A partir dessas informações, aponte a seguir a opção que NÃO representa o conceito de Big Data.
Selecione a resposta:
a. Facebook.
b. Twitter.
c. Instagram.
d. YouTube.
e. Sistema de Gerenciamento do Relacionamento com Clientes (CRM) de uma determinada empresa.

✅ A alternativa correta é: e.

#### Questão 5
Uma determinada etapa de um projeto de banco de dados representa a parte final do projeto. Nesta etapa, definem-se detalhes técnicos da implementação do banco de dados como, por exemplo, a forma de os dados serem armazenados, os scripts para a criação dos objetos no banco de dados (tabelas, visões, colunas, funções, entre outros), a permissão de acesso de usuário, etc. Esta etapa é fortemente ligada ao Sistema Gerenciador de Banco de Dados (SGBD) que será utilizado. Qual das opções a seguir define corretamente o nome desta etapa?
Selecione a resposta:
a. Análise de Requisitos.
b. Projeto Conceitual
c. Projeto Lógico.
d. Projeto Físico.
e. Análise de ER.

✅ A alternativa correta é: d.


## Na prática

Em relação a um projeto de banco de dados:  
Na prática, convencionou-se iniciar o processo de estruturação de um novo banco de dados com a construção de um modelo dos objetos da organização (empresa) que será atendida por ele, ao invés de partir diretamente para o projeto de banco de dados propriamente dito.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/8b1581f3-1665-4ca1-8234-1782330bb53a/adff15a0-6299-4386-ac67-9d766594a92c.jpg)

Esta forma de proceder permite envolver o usuário na especificação do banco de dados. Sabe-se da prática da Engenharia de Software_,_ em que o envolvimento do usuário na especificação do software aumenta a qualidade do programa/aplicativo produzido. A ideia é de que o usuário é quem melhor conhece a organização e suas rotinas e, portanto, é aquele que melhor domina os requisitos que o software deve preencher. Modelos conceituais são modelos que descrevem a organização, sendo mais simples de serem compreendidos por usuários leigos em práticas de projeto da área de Tecnologia da Informação (TI).


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

O Modelo Relacional de Dados
Para entender melhor o projeto de banco de dados e a importância de fazer a Modelagem do Banco de Dados antes de partir para a implementação prática, confira o artigo a seguir.
[Mais](https://juliobattisti.com.br/artigos/office/modelorelacional_p5.asp)

Projeto de Banco de Dados
Para uma visão geral do processo e dos conceitos necessários para a compreensão do banco de dados, acompanhando a apresentação a seguir:
[Mais](https://docente.ifrn.edu.br/josecunha/disciplinas/banco-de-dados/material-de-aula/introducao-bd)

Banco de Dados
Para aprofundar seus estudos sobre como construir, definir e manipular um banco de dados, assista ao vídeo a seguir.
[Mais](https://www.youtube.com/embed/p0zCY9cKrJM)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

MANNINO, Michael V. Projeto, Desenvolvimento de Aplicações & Administração de Banco de Dados. 3ª ed. 2014.

RAMAKRISHNAN, Raghu; GEHRKE, Jahannes. Sistemas de Gerenciamento de Banco de Dados. 3ª ed. 2011.

Imagens utilizadas na UA
CAPA 
ALPHASPIRIT/Shutterstock SAGAH, 2014.

Figura 1 
RAMAKRISHNAN, Raghu; GEHRKE, Jahannes. Sistemas de Gerenciamento de Banco de Dados. 3ª Ed. Porto Alegre. McGraw Hill/Bookman. 2011. SAGAH, 2014.

Figura 2
BARROS, Maurício. 2014.
SAGAH, 2014.

Figura 3
SERGEY NIVENS/Shuttertock

Imagens utilizadas no vídeo
RAMAKRISHNAN, Raghu; GEHRKE, Jahannes. Sistemas de Gerenciamento de Banco de Dados. 3ª Ed. Porto Alegre. McGraw Hill/Bookman. 2011.
SAGAH, 2014.

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





