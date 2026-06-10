## Apresentação

As organizações têm uma grande preocupação em armazenar seus dados, dada a importância que os mesmos representam para seu negócio. No entanto, dados armazenados são como tesouro escondido, é preciso recuperá-los de forma que gerem informação para construção do conhecimento empresarial. Portanto, a linguagem SQL possui alguns subconjuntos carregados com comando que auxiliam este processo. Mas utilizá-los de qualquer forma pode trazer grandes problemas de desempenho para a sua aplicação. É muito importante conhecer o DML (Linguagem de Manipulação de Dados), cujo subconjunto pertence o comando SELECT. O comando SELECT é utilizado para recuperação dos dados, uma consulta. Contudo, existem inúmeras maneiras de escrevermos consultas com o comando SELECT! Em algumas formas, essas consultas podem demorar mais que as outras. Então, você irá estudar não somente como criar essas consultas, mas como melhorar o desempenho das consultas e criar sistemas mais rápidos.

Nesta Unidade de Aprendizagem, você acompanhará o processo de criação de consultas avançadas referenciando problemas de junção externa, interna, união e consultas aninhadas. Além disso, conhecerá as técnicas utilizadas para melhorar o desempenho e realizar tunning no banco de dados.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Desenvolver consultas avançadas com a linguagem SQL.
- Aplicar comandos e cláusulas em consultas a banco de dados.
- Resolver problemas de desempenho e realizar tunning de banco de dados.

## Desafio

Imagine que você é desenvolvedor de sistemas e precisa realizar uma consulta no banco de dados através do seu sistema para verificar a existência de um registro. Você está trabalhando no sistema de gerenciamento de funcionários e no sistema existe a tabela Funcionário. Você precisa saber se existe um registro na Tabela funcionário que contenha o ID 0063.
Você utilizou o seguinte comando no seu sistema.
IF (SELECT COUNT(1) FROM FUNCIONARIO WHERE ID LIKE ‘0063’) > 0       PRINT 'Funcionário encontrado!'
Você utiliza esse comando SQL constantemente dentro do sistema, e notou que a função que realiza essa chamada está demorando muito.
Como forma de melhorar o desempenho e reduzir o tempo utilizado nessa consulta, qual o comando que você deveria utilizar?

####  ✅ Resposta ao desafio:

O comando (COUNT(1)) realmente funciona, mas não é a forma mais eficiente para verificar a existência de um registro. Isso porque o banco precisa contar todas as ocorrências antes de retornar o resultado, mesmo que você só queira saber se existe pelo menos uma linha.
A forma mais adequada é usar o EXISTS, que interrompe a busca assim que encontra o primeiro registro correspondente. O comando ficaria assim:

``` sql
IF EXISTS (SELECT 1 FROM FUNCIONARIO WHERE ID = '0063')
	PRINT 'Funcionário encontrado!'
```

Por que é melhor?
EXISTS retorna verdadeiro assim que encontra uma linha, sem precisar percorrer toda a tabela.
Evita o custo de contagem desnecessária.
É mais performático em tabelas grandes, especialmente quando há índices sobre a coluna pesquisada.

#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17820342
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 10/06/26 - 19:45
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

Observe, no infográfico seguinte, uma descrição das palavras-chave LEFT JOIN, HIGHT JOIN, INNER JOIN e UNION, utilizadas na Junção Interna, Junção Externa, União ou Combinação.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/3b7c1b58-ec1d-47cb-b73e-b94e720a203e/ed5b0ee2-5e05-4044-8780-bf02afb4e2ee.png)

​​​​​​​
## Conteúdo do Livro

Conhecer recursos avançados de consulta em banco de dados é fundamental para que você possa extrair a informação consistente e satisfatória, auxiliando o processo de análise e tomada de decisão na organização. Contudo, para elaboração destas queries é necessário conhecimentos aprofundados neste fundamento.

Acompanhe o capítulo Formulação de Consulta Avançada com SQL, da obra "Projeto, Desenvolvimento de Aplicações e Administração de Banco de Dados", livro que serve de base teórica para esta Unidade de Aprendizagem, e traz uma abordagem sobre problemas de junção externa, interna e união ou combinação.

Boa leitura!

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/cd47b043-a8c6-4398-99c2-f0ee978df9c7/5fa01b66-9529-42ab-b0e2-d00550187e7f.jpg)

​​​​​​
## Dica do Professor

Na dica do professor, você verá os recursos avançados de consultas em bancos de dados: otimização e tunning, bem como as técnicas utilizadas para melhorar o desempenho das buscas.
Confira!

##  Exercícios

#### Questão 1
Marque a alternativa correta:
Selecione a resposta:
a. As junções, formuladas no estilo produto cartesiano, utilizam as palavras-chave INNER JOIN e ON.
b. Nas junções formuladas no estilo de operador de junção, as tabelas são escritas diretamente na cláusula FROM e as condições na cláusula WHERE.
c. Nas junções formuladas no estilo de produto cartesiano, as tabelas são listadas na cláusula WHERE.
d. Nas formuladas no estilo produto cartesiano, as tabelas são listadas na cláusula FROM.
e. A vantagem do estilo produto cartesiano é que podemos formular problemas envolvendo o operador de junção externa.

✅ A alternativa correta é: d.

#### Questão 2
Marque a alternativa correta:
Selecione a resposta:
a. LEFT JOIN retorna todas as linhas da tabela à esquerda.
b. RIGHT JOIN retorna todas as linhas das tabelas relacionadas.
c. FULL JOIN retorna linhas das duas tabelas apenas quando houver correspondência nas duas tabelas.
d. INNER JOIN, representa junção interna, retorna todas as linhas correspondentes nas duas tabelas.
e. UNION é uma cláusula que substitui a cláusula ON.

✅ A alternativa correta é: a.


#### Questão 3
Analise o código abaixo e marque a afirmativa correta. SELECT cliente.primeiro_nome As Nome, cliente.primeiro_nome As sobrenome, pagamento.valor FROM cliente INNER JOIN pagamento ON cliente.cliente_id = pagamento.cliente_id WHERE pagamento.valor IN (SELECT valor from pagamento WHERE valor > 5.00 );
Selecione a resposta:
a. O código é referente a uma consulta de junção interna que retorna todas as linhas da tabela da direita.
b. O código é referente a uma consulta de junção externa que retorna todas as linhas da tabela da esquerda.
c. O código é referente a uma consulta de junção interna.
d. O código não executa.
e. O código é referente a uma consulta aninhada que retorna linhas que possuem o valor do campo maior que 5.00.

✅ A alternativa correta é: e.

#### Questão 4
Observe o seguinte código e marque a afirmativa correta.

SELECT CPFProf, NomeProf, SobrenomeProf, SalarioProf
FROM Professor LEFT JOIN Aluno
ON Professor.CPFProf = Aluno.CPFAluno
WHERE Aluno.CPFAluno IS NULL

Selecione a resposta:
a. O código refere-se a uma união externa entre as consultas professor e aluno.
b. O operador ON faz referência às tabelas utilizadas na consulta.
c. O código refere-se a uma consulta aninhada.
d. O código retorna os dados dos professores que não são alunos.
e. O código acima retorna todas as colunas da tabela aluno.

✅ A alternativa correta é: d.

#### Questão 5
Existem diferentes recursos que podem nos ajudar a formular consultas avançadas, usando SQL. Em relação às alternativas abaixo, marque a afirmativa correta:
Selecione a resposta:
a. A consulta aninhada Tipo I avalia várias vezes e produz a tabela.
b. A consulta aninhada Tipo II é executada repetidas vezes.
c. A aplicação de operadores de diferença é totalmente compatível com a união.
d. Todos os problemas de diferença podem ser formulados utilizando a consulta aninhada Tipo II.
e. Para a junção externa de um lado, as palavras-chave completas do SQL são LEFT JOIN e RIGHT JOIN.

✅ A alternativa correta é: b.


## Na prática

SQL é uma importante linguagem criada na década de 70 pela IBM com base em conceitos de álgebra relacional. Com essa linguagem, podemos criar estruturas para armazenamento de dados e manipular esses dados: excluir, inserir, consultar e atualizar.

As consultas são instruções desenvolvidas para o retorno de dados. Portanto, quanto melhor especificadas, melhores serão os resultados de retorno.

Veja uma aplicação prática de consulta SQL, utilizando algumas cláusulas. Para tanto, será utilizado o SGBD MySql com o Banco de dados SAKILA, que é específico para estudos.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/e3ca7ed7-5b76-42da-bdf0-f5870f6bae53/09a74041-d609-42a4-93cd-779eae5b1738.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

No link seguinte, você verá o que é e como realizar um plano de execução de SQL Server, iniciando pela criação de uma tabela até a construção do plano de execução.
[Mais](https://www.youtube.com/embed/XRLhREk4qNQ)

Acompanhe, a seguir, um treinamento sobre SQL Server para desenvolvedores, onde serão tratados os fundamentos, estrutura e usabilidade dos índices.
[Mais](https://www.youtube.com/embed/r-0CV82OYak)

Você sabia que o principal objetivo do SQL Tunning é minimizar o tempo de resposta e recuperação de dados? Para saber mais, clique na dica seguinte.
[Mais](https://www.youtube.com/embed/YHbBDH2j-iw)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

MANNINO, M. V. Projeto, desenvolvimento de aplicações e administração de banco de
dados. 3. ed. São Paulo: McGraw-Hill, 2008.

Banco de imagens Shutterstock.
SAGAH, 2017.

#### EQUIPE SAGAH

Coordenador(a) de Curso
Roberto Litel

Professor(a)
Jorge Campos

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
















