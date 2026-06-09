## Apresentação

Quando são realizadas consultas em um Data Warehouse, para que se tenha um resultado efetivo, é necessária uma complexidade maior na modelagem das tabelas. O foco dessa modelagem é a coleção de medidas numéricas. Cada medida depende de um conjunto de dimensões. A modelagem baseada em dimensões, chamada de Modelagem de Dados Multidimensional, permite uma busca de resultados mais clara e específica.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Identificar o conceito de Modelagem Multidimensional.
- Aplicar as ferramentas de OLAP.
- Reconhecer os objetivos da utilização de Fatos e Dimensões.


## Desafio

Modelagem Dimensional é uma técnica de projeto lógico normalmente usada para data warehouses que contrasta com a Modelagem Entidade-Relacionamento. A Modelagem Dimensional é a única técnica viável para bancos de dados que devem responder consultas em um Data Warehouse. A Modelagem Entidade-Relacionamento é útil apenas para registro de transações e para fase de administração da construção de um Data Warehouse, mas não na entrega dos dados para o usuário final.

Você é profissional da área de TI e ficou responsável por explicar a sua equipe a diferença entre as modelagens. Construa um quadro traçando um paralelo das atividades do Modelo Dimensional com o Modelo Entidade-Relacionamento, levando em consideração os diagramas, usuários, junções, dados e consultas.

####  ✅ Resposta ao desafio:

Quadro comparativo traçando o paralelo entre Modelagem Dimensional e Modelagem Entidade-Relacionamento.

| Aspecto   | Modelo Dimensional                                                                         | Modelo Entidade-Relacionamento                                                       |
| --------- | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| Diagramas | Usa esquema estrela ou floco de neve, com tabelas fato e dimensões.                        | Usa diagramas ER com entidades, atributos e relacionamentos.                         |
| Usuários  | Voltado para analistas de negócio e usuários finais que precisam de relatórios e insights. | Voltado para desenvolvedores e administradores, focado em transações e consistência. |
| Junções   | Poucas junções, geralmente entre fato e dimensões, otimizadas para performance.            | Muitas junções complexas entre várias entidades, típicas de sistemas transacionais.  |
| Dados     | Dados históricos e agregados, preparados para análise multidimensional.                    | Dados operacionais e detalhados, usados para registrar transações do dia a dia.      |
| Consultas | Consultas ad hoc complexas, com agregações, filtros e análises por intervalos.             | Consultas simples e transacionais, como inserir, atualizar e buscar registros.       |

1.Diagramas
Modelo Dimensional: Usa esquema estrela ou floco de neve, com tabelas fato e dimensões.
Modelo Entidade-Relacionamento: Usa diagramas ER com entidades, atributos e relacionamentos.

2.Usuários
Modelo Dimensional: Voltado para analistas de negócio e usuários finais que precisam de relatórios e insights.
Modelo Entidade-Relacionamento: Voltado para desenvolvedores e administradores, focado em transações e consistência.

3.Junções
Modelo Dimensional: Poucas junções, geralmente entre fato e dimensões, otimizadas para performance.
Modelo Entidade-Relacionamento: Muitas junções complexas entre várias entidades, típicas de sistemas transacionais.

4.Dados
Modelo Dimensional: Dados históricos e agregados, preparados para análise multidimensional.
Modelo Entidade-Relacionamento: Dados operacionais e detalhados, usados para registrar transações do dia a dia.

5.Consultas
Modelo Dimensional: Consultas ad hoc complexas, com agregações, filtros e análises por intervalos.
Modelo Entidade-Relacionamento: Consultas simples e transacionais, como inserir, atualizar e buscar registros.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17774645
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 09/06/26 - 19:37
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1


## Infográfico

O projeto de Modelagem Multidimensional utiliza a ferramenta On-Line Analytical Processing (OLAP), que possui também variações específicas de acordo com as necessidades identificadas. Veja, no infográfico seguinte, as características das ferramentas OLAP.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/41b7d949-1b5f-4f28-8843-f0e5f0239a51/675c6438-4fde-40ef-8da9-d86e0f694d40.png)


## Conteúdo do Livro

Veja, no trecho disponibilizado do livro "Sistemas de Gerenciamento de Banco de Dados" as características da Modelagem de Dados Multidimensional. Inicie a leitura no tópico OLAP: Modelo de dados multidimensional, siga em Projeto de Banco de Dados Multidimensional e Consultas de agregação multidimensionais. E, por fim, leia o tópico Técnicas de implementação de OLAP.
Boa leitura!

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/d7c22909-eb82-4b62-8f81-699a2b35d4dc/3766de17-ad08-45eb-af34-06d0eca6489d.jpg)


## Dica do Professor

O vídeo a seguir oferece uma breve apresentação da abordagem dos conceitos de Modelagem de Dados Multidimensional. Além disso, identifica os exemplos de modelos de Dados Multidimensionais.


## Exercícios

#### Questão 1
Que forma é utilizada para demonstrar a Modelagem Multidimensional?
Selecione a resposta:
a. Quadrado.
b. Cubo.
c. Octógono.
d. Pirâmide.
e. Estrela.

✅ A alternativa correta é: b. Cubo.


#### Questão 2
Qual a principal função do OLAP?
Selecione a resposta:
a. Acessar e alterar dados corporativos.
b. Importar dados de SGBDs Diversos.
c. Verificar dados pessoais pelo usuário.
d. Consultar e analisar dados corporativos com alta performance.
e. Transformar os dados importados para um formato mais amigável.

✅ A alternativa correta é: d. Consultar e analisar dados corporativos com alta performance.


#### Questão 3
São componentes de um modelo multidimensional OLAP:
Selecione a resposta:
a. Fatos, Histórico e Métodos.
b. Metodologia, Dimensões e Arquivos.
c. Dimensões, Medidas e Recursividade.
d. Fatos, Ponteiros e Hipóteses.
e. Fatos, Dimensões e Medidas.

✅ A alternativa correta é: e. Fatos, Dimensões e Medidas.


#### Quetão 4
São exemplos de esquemas de dados multidimensionais:
Selecione a resposta:
a. Estrela, Cubo e Pirâmide.
b. Floco de Neve e Constelação de Estrelas.
c. Estrela, Floco de Neve e Constelação de Fatos.
d. Quadrada, Circular e Linear.
e. Estrela, Bola de Neve e Galáxia.

✅ A alternativa correta é: c. Estrela, Floco de Neve e Constelação de Fatos.


#### Questão 5
Qual a função de um Slice and Dice?
Selecione a resposta:
a. Fatiar os dados em porções menores.
b. Modificar a posição de uma informação, alterando linhas por colunas.
c. Aumentar a velocidade do Data Warehouse.
d. Atualizar os dados de um usuário específico.
e. Não existe essa função Slice and Dice.

✅ A alternativa correta é: b. Modificar a posição de uma informação, alterando linhas por colunas.

## Na prática

Felipe é responsável por gerar o relatório de vendas de uma loja de artigos esportivos que possui vendas tanto na loja física quanto vendas on-line. Através dos resultados obtidos com Dados Multidimensionais, é possível obter com muito mais clareza e objetividade as informações a respeito das vendas, tais como volume de vendas simples, região da venda, mês e dia da semana de maior volume, perfil dos clientes, vendedor destaque e prazos de entregas.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/6d272c63-947e-4ca1-8d52-62b16ed08264/6752d4de-4f69-4e54-b4d2-559fa3aba0ca.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

O que são Fatos e Dimensões?
Neste link você poderá saber o que são fatos e dimensões, suas principais características e exemplos de como identificar os conceitos em um modelo completo. Confira!
[Mais](https://www.youtube.com/embed/GmdiE61MBgs)

Sobre a modelagem dimensional do Data Warehouse usando um esquema em estrela
Veja, a seguir, um artigo sobre os conceitos de modelagem dimensional do Data Warehouse, a partir de um esquema em estrela.
[Mais](https://learn.microsoft.com/pt-br/previous-versions/system-center/system-center-2012-R2/hh916547(v=sc.12)?redirectedfrom=MSDN)

As 10 Regras Essenciais para a Modelagem de Dados Dimensional
Conheça as 10 Regras Essenciais para a Modelagem de Dados Dimensional, clicando no link a seguir.
[Mais](https://www.ambientelivre.com.br/tutoriais-pentaho-bi/kimball-university-as-10-regras-essenciais-para-a-modelagem-de-dados-dimensional.html)

Sistemas de gerenciamento de banco de dados
Ramakrishnan, Raghu; Gehrke, Johannes. Sistemas de Gerenciamento de Bancos de Dados, Bookman, 2011.
[Mais](https://bibliotecaa.grupoa.com.br/lti/launch.php?bookid=9788563308771)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

RALPH, Kimball. The Data Warehouse Etl Toolkit - Practical Techniques For Extracting
Cleaning Conforming And Delivering Data. Indianápolis: Wiley Publishing, Inc., 2004.

RAMAKRISHNAN, R.; GEHRKE, J. Sistemas de gerenciamento de bancos de dados. 3. ed.
São Paulo: McGraw-Hill, 2008. 

Banco de imagens Shutterstock.
SAGAH, 2017.


#### EQUIPE SAGAH

Coordenador(a) de Curso
Roberto Litel

Professor(a)
Márcio Motta

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
