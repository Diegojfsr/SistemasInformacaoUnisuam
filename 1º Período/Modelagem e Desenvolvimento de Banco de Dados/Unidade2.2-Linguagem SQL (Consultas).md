## Apresentação

Uma das principais funções de um sistema de banco de dados é proporcionar recursos para armazenamento, manutenção e consulta de dados de maneira correta e eficaz.
Nesta Unidade de Aprendizagem, vamos tratar das opções de consulta utilizando a instrução SELECT, assim como suas variações e possibilidades.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Descrever as instruções de consulta e suas variações;
- Comparar as opções de consulta a partir da instrução SELECT;
- Construir notações de consulta utilizando a instrução SELECT e suas variações.


## Desafio

Imagine que você faz parte de uma equipe de profissionais de banco de dados e lhe foi designada a tarefa de criar determinadas consultas utilizando a instrução SELECT. Sua função como DBA (Administrador de Banco de Dados) é, a partir das necessidades abaixo, escrever a sintaxe em linguagem SQL para as referidas consultas. Utilizaremos como base a Tabela, conforme figura abaixo:
As consultas solicitadas à equipe de banco de dados são:
1- Consultar todos os veículos (num_veiculo) que são oriundos da UF (Unidade da Federação) Rio Grande do Sul.
2- Consultar todos os veículos (num_veiculo) cujo ano de fabricação for 2012 e 2014.
3- Consultar os veículos (num_veiculo) e as placas (num_placa) dos veículos cujo modelo seja 2014, ordenados por data de cadastro.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/ed0d1559-bf7f-47d2-abf9-315d01353ddf/9cdc53d3-8125-4025-8da0-021d6e73783d.png)

####  ✅ Resposta ao desafio:

Consultas SQL conforme solicitado, usando a tabela veículo.

1.Veículos oriundos da UF Rio Grande do Sul
```sql
SELECT num_veiculo
FROM veiculo
WHERE uf_veiculo = 'RS';
```

2.Veículos cujo ano de fabricação seja 2012 ou 2014
```sql
SELECT num_veiculo
FROM veiculo
WHERE ano_fabricacao IN (2012, 2014);
```

3.Veículos e placas cujo modelo seja 2014, ordenados por data de cadastro
```sql
SELECT num_veiculo, num_placa
FROM veiculo
WHERE ano_modelo = 2014
ORDER BY data_cadastro;
```

Essas consultas seguem a lógica da tabela e atendem exatamente às três necessidades descritas.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17035608
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 21/05/26 - 19:22
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

Recuperar linhas do banco de dados e permitir a seleção de uma ou várias linhas ou colunas de uma ou várias tabelas com a instrução Select. A sintaxe completa desta instrução é complexa, mas as cláusulas principais podem ser assim resumidas:

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/9145c3fa-1041-4b04-9a78-321704735ef3/ea5c7bb2-3684-4642-af97-cf6004dbb0ae.png)



## Conteúdo do Livro

A consulta de dados é uma pesquisa realizada no banco de dados, cujo propósito é recuperar os registros que atendem às condições preestabelecidas.

Para entender melhor como é realizada a consulta de dados, leia o trecho a seguir, do livro MANNINO, M.V. Projeto, desenvolvimento de aplicações e administração de banco de dados. 3.ed. Porto Alegre: AMGH, 2008, base teórica para esta Unidade de Aprendizagem.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/a7e16ca4-59fb-4cf7-93db-0fed24301913/09fadecc-76cc-4789-947d-189c6dd7ee0f.jpg)

​​​​​​​

## Dica do Professor

No vídeo da Dica do Professor a seguir, você conhecerá como é feita a consulta em um banco de dados. Confira os detalhes e os principais comandos para consultar dados utilizando a linguagem SQL.


## Exercícios


#### Questão 1
Quando da utilização da instrução SELECT para consultas em banco de dados, podemos utilizar vários argumentos de sintaxe para compor e estruturar a consulta das informações as quais são necessárias. Um destes argumentos é o BETWEEN-AND, um operador de atalho para testar uma coluna de data ou numérica em relação a uma gama de valores. Aponte qual das opções a seguir contém a sintaxe SQL correta para a "saída" conforme a figura abaixo, onde o objetivo é listar o Nome e a Data de contratação dos professores, contratados entre 1999 e 2000.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/b233175b-fa0c-4478-bb74-86d6fa946104/f0ace71f-08c7-4825-9098-e2ad972d2d2f.png)

Selecione a resposta:
a. SELECT NomeProf, SobrenomeProf, DataAdmProf
FROM Professor
WHERE DataAdmProf BETWEEN #1/1/1999# AND #31/12/2000#

b. SELECT NomeProf, SobrenomeProf, DataAdmProf
FROM Professor
WHERE DataAdmProf BETWEEN #1/1/1999# AND #31/12/2005#

c. SELECT NomeProf, SobrenomeProf, DataAdmProf
FROM Professor
WHERE DataAdmProf BETWEEN #1/1/1997# AND #31/12/2000#

d. SELECT NomeProf, SobrenomeProf, DataAdmProf
WHERE DataAdmProf BETWEEN #1/1/1999# AND #31/12/2000#

e. SELECT NomeProf, SobrenomeProf, DataAdmProf
FROM Professor
WHERE DataAdmProf #1/1/1999# AND #31/12/2000#

✅ A alternativa correta é: a. Seleciona os professores com datas entre 1999 e 2000, exatamente como solicitado.


#### Questão 2

O argumento GROUP BY pode ser utilizado junto à instrução SELECT para consultas em banco de dados quando se deseja agrupar informações a partir de determinadas colunas. Aponte qual das opções a seguir contém a sintaxe SQL correta para a "saída" conforme a figura abaixo, onde o objetivo é consultar a média geral de notas dos estudantes, agrupados por especialização.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/59351500-8470-495f-afd0-13a5e6cac0f6/a295f130-46da-4da4-8b55-d3e93a4bddce.png)
Selecione a resposta:

a. SELECT Especialização, AVG(MediaAluno) AS MediaGeral
GROUP BY Especialização

b. SELECT Especialização, AVG(MediaAluno) AS MediaGeral
FROM Aluno
GROUP BY Especialização

c. SELECT Especialização, AVG(MediaAluno) AS MediaGeral
FROM Aluno
GROUP BY MediaGeral

d. SELECT Especialização, AVG(MediaAluno) AS MediaGeral
FROM Aluno
GROUP BY Aluno

e. SELECT Especialização, AS MediaGeral
FROM Aluno
GROUP BY Especialização

✅ A alternativa correta é: b. Seleciona a especialização, calcula a média das notas e agrupa por especialização. É exatamente o que a saída pede.


#### Questão 3
O argumento GROUP BY pode ser utilizado junto a instrução SELECT para consultas em banco de dados; junto a este argumento, podemos utilizar também a instrução HAVING, que serve para aplicar uma determinada condição de seleção junto aos registros agrupados. Aponte qual das opções a seguir contém a sintaxe SQL correta para a "saída" conforme a figura abaixo, onde o objetivo é consultar a quantidade e o valor das faturas de cada conveniada, porém, somente quando o valor da fatura for superior a 30.000.

**![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/bd4da986-e3ad-4fc5-9f6e-bb900f5de360/f7fa6ef8-91c8-4890-bad7-6b5f49f1f5ef.png)**

Selecione a resposta:
a. SELECT cod_conveniada, count (num_fatura), sum(vlr_fatura)  
FROM Fatura  
GROUP BY cod_conveniada  
HAVING sum (vlr_fatura) > 50000

b. SELECT cod_conveniada, count (num_fatura), sum(vlr_fatura)  
GROUP BY cod_conveniada  
HAVING sum (vlr_fatura) > 30000

c. SELECT cod_conveniada, count (num_fatura), sum(vlr_fatura)  
FROM Fatura  
GROUP BY cod_conveniada  
HAVING sum (vlr_fatura) > 30000

d. SELECT cod_conveniada, count (num_fatura), sum(vlr_fatura)  
FROM Fatura  
GROUP BY num_fatura  
HAVING sum (vlr_fatura) > 30000

e. SELECT cod_conveniada, count (num_fatura), sum(vlr_fatura)  
FROM Fatura  
GROUP BY cod_conveniada

✅ A alternativa correta é: c. Contém todas as cláusulas necessárias (SELECT, FROM, GROUP BY, HAVING) e aplica o filtro corretamente.


#### Questão 4
Quando da utilização da instrução SELECT para consultas em banco de dados, podemos utilizar vários argumentos de sintaxe para compor e estruturar a consulta das informações as quais são necessárias. Um destes argumentos é o NULL (IS NULL ou IS NOT NULL) que é utilizado para consultar valores nulos ou não nulos. Aponte qual das opções a seguir contém a sintaxe SQL correta para a "saída" conforme a figura abaixo, onde o objetivo é consultar o código (num_pessoa_pf) das pessoas cujo estado civil NÃO foi cadastrado (nulo).

**![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/ce2c70fe-fa2c-4ce0-bf38-ab8e198dc4c6/6da3186e-2f9e-461d-a1b8-4b07ae3dd9b2.png)**

Selecione a resposta:
a. SELECT num_pessoa_pf  
FROM pessoa_juridica  
WHERE cod_estado_civil IS NULL

b. SELECT num_pessoa_pf  
FROM pessoa_fisica  
WHERE num_pessoa_pf IS NULL

c. SELECT num_pessoa_pf  
FROM pessoa_fisica  
WHERE cod_estado_civil IS NOT NULL

d. SELECT num_pessoa_pf  
FROM pessoa_fisica  
WHERE cod_estado_civil IS NULL

e. SELECT num_pessoa_pf  
WHERE cod_estado_civil IS NULL

✅ A alternativa correta é: d. Consulta a tabela certa (pessoa_fisica) e aplica o filtro correto para estado civil nulo.


#### Questão 5
Quando utilizamos a instrução SELECT para consultas em banco de dados, podemos utilizar também os argumentos de sintaxe MIN (mínimo), MAX (máximo) e AVG (média). Aponte qual das opções a seguir contém a sintaxe SQL correta para a "saída" conforme a figura abaixo, onde o objetivo é consultar a fatura com maior valor, a fatura com menor valor e o valor médio entre todas as faturas.

**![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/b186f4c2-5af8-414a-9f04-7fbc077986f5/abea4dfa-e92b-417a-ba9a-50cb104cb7d7.png)**

Selecione a resposta:
a. SELECT MAX (vlr_fatura) AS MENOR,  
MIN (vlr_fatura) AS MAIOR,  
AVG (vlr_fatura) AS MEDIA  
FROM fatura;

b. SELECT MAX (vlr_fatura) AS MAIOR,  
AVG (vlr_fatura) AS MEDIA  
FROM fatura;

c. SELECT MAX (vlr_fatura) AS MAIOR,  
MIN (vlr_fatura) AS MENOR,  
FROM fatura;

dSELECT MAX (vlr_fatura) AS MAIOR,  
MIN (vlr_fatura) AS MENOR,  
AVG (vlr_fatura) AS MEDIA;

e. SELECT MAX (vlr_fatura) AS MAIOR,  
MIN (vlr_fatura) AS MENOR,  
AVG (vlr_fatura) AS MEDIA  
FROM fatura;

✅ A alternativa correta é: e. Contém todas as funções de agregação e a tabela correta, com aliases coerentes.


## Na prática

Ordem de processamento lógico da instrução SELECT:
Quando da utilização da instrução SELECT, há uma ordem de processamento lógico ou a ordem de associação de uma instrução SELECT. Essa ordem determina quando os objetos definidos em uma etapa são disponibilizados para as cláusulas em etapas subsequentes.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/ac29dbb4-b389-4af7-a503-6520ea40aff7/f30dc06b-5ea7-46c3-835d-a10f3145de67.jpg)

Por exemplo, se o processador de consulta puder ser associado (acessar) a tabelas ou exibições definidas na cláusula FROM, esses objetos e suas colunas serão disponibilizados para todas as etapas subsequentes. De modo oposto, como a cláusula SELECT é a etapa 8, qualquer alias de coluna ou coluna derivada definida naquela cláusula não poderá ser referenciada por cláusulas precedentes. Porém, poderão ser referenciadas por cláusulas subsequentes, como a cláusula ORDER BY. Observe que a execução física real da instrução é determinada pelo processador de consulta e a ordem pode variar desta lista.

1. FROM  
2. ON  
3. JOIN  
4. WHERE  
5. GROUP BY  
6. WITH CUBE (ou WITH ROLLUP)  
7. HAVING  
8. SELECT  
9. DISTINCT  
10. ORDER BY  
11. TOP


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Para entender as principais instruções na linguagem SQL, acompanhe o site a seguir:
[Mais](https://www.devmedia.com.br/principais-instrucoes-em-sql/37262)

A Instrução SELECT é utilizada para especificar quais os campos de quais tabelas farão parte da consulta, quais os critérios de pesquisa serão utilizados, qual a ordem de classificação, entre outros.
Para reforçar o conceito e as formas de uso da instrução SELECT na linguagem SQL, confira o link a seguir:
[Mais](https://juliobattisti.com.br/artigos/office/nocoessqlconsultas.asp)

Para se combinar tabelas, é primordial conhecer como estas tabelas foram modeladas e se relacionam.
No artigo a seguir você conhecerá as difersas formas da instrução JOIN e como ela lhe ajudará nesse processo.
[Mais](https://www.devmedia.com.br/entendendo-a-instrucao-join/32936)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS


MANNINO, Michael V. Projeto, Desenvolvimento de Aplicações & Administração de Banco de Dados. 3ª ed. 2014.

RAMAKRISHNAN, Raghu; GEHRKE, Jahannes. Sistemas de Gerenciamento de Banco de
Dados. 3ª ed. 2011.

Banco de imagens Shutterstock
SAGAH, 2015

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


