## Apresentação

Os bancos de dados, assim como outras aplicações, necessitam de um cuidado especial. Esse cuidado exige manutenções programadas, emergenciais e, até mesmo, manutenções automatizadas. Assim, em um ambiente organizado é muito menor a incidência de problemas não previstos e o tempo de manutenção melhor controlado e otimizado.

Nesta Unidade de Aprendizagem, você vai compreender as necessidades das políticas de manutenção de banco de dados.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Reconhecer as necessidades de manutenção do banco de dados.
- Aplicar métodos de manutenção do banco de dados.
- Identificar formas de ofertar a manutenção do banco de dados.

## Desafio

Márcia, que é o SysDba da loja Eletrônicos Billy, depara-se com um imenso problema ocasional: após determinado número de produtos serem colocados em promoção no site da loja, percebeu-se que, além deles, outros produtos também apareciam com desconto para os clientes, de forma incorreta.

Diversos clientes aproveitaram o "bug" do site da loja para comprar produtos com valores bem reduzidos. Considere que cada minuto do site online gera mais prejuízos para a empresa.

Marcia pode realizar as seguintes operações de manutenção:

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/5c6aba64-2ce1-4561-a5cb-36d8a685dd87/e6ff229b-6f5e-422c-a990-7a1cb914e85b.jpg)

​​​​​​​Com o objetivo de evitar prejuízos para a empresa, qual o procedimento Márcia deverá adotar para solucionar o problema imediatamente? Descreva como Márcia deve agir considerando as opções existentes dentro dos conceitos de manutenção de banco de dados e justifique o motivo da sua escolha.

####  ✅ Resposta ao desafio:

Diante do cenário descrito, em que cada minuto online gera prejuízos para a loja, Márcia precisa adotar uma ação rápida e eficaz para corrigir os dados incorretos sem comprometer ainda mais o funcionamento do sistema.

A alternativa mais adequada é:
Deixar toda a loja e o banco de dados offline por alguns instantes e aplicar uma correção nos dados.

Justificativa:
Rapidez: Colocar o sistema offline imediatamente evita que mais clientes aproveitem o erro e comprem com desconto indevido.
Correção direta: Permite que Márcia ajuste apenas os registros afetados, sem necessidade de restaurar backups antigos que poderiam apagar dados válidos (como vendas legítimas realizadas após o backup).
Controle do prejuízo: Ao aplicar a correção diretamente nos dados, o sistema volta a funcionar com integridade e sem descontos indevidos, reduzindo perdas financeiras.

Como Márcia deve agir:
Colocar o site e banco em modo offline temporário para impedir novas transações.
Identificar os registros de produtos com desconto incorreto.
Aplicar correções diretamente nas tabelas de produtos e promoções, ajustando os preços e regras.
Testar o sistema em ambiente controlado para garantir que os erros foram eliminados.
Reativar o site e o banco após validação.
Registrar logs e realizar um backup atualizado após a correção, garantindo segurança futura.

Assim, Márcia resolve o problema imediatamente, evita maiores prejuízos e mantém a consistência dos dados sem perder transações legítimas.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17299147
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 28/05/26 - 19:24
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

Acompanhe o infográfico e compreenda as necessidades das políticas de manutenção de banco de dados.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/0c7505c4-e377-4674-bfd3-b1d71a7d5a73/dafe1e23-c499-41db-b8d8-a4c0717bcc66.png)


## Conteúdo do Livro

Sistemas pessoais, empresariais, multinacionais, até mesmo acadêmicos, quando utilizam algum tipo de banco de dados, necessariamente, é preciso ter uma política de manutenção/gerenciamento visando segurança e facilidade nas tarefas relacionadas a este gerenciamento. Por isso, é importante planejar adequadamente qualquer tipo de manutenção, seja ela para realização de alteração de dados, exclusão de registros impróprios e, principalmente, backup e restauração.

Neste capítulo você verá algumas das políticas de manutenção de banco de dados necessárias para a correta e íntegra manipulação e gerenciamento de seus dados, bem como prevenção e/ou recuperação de qualquer tipo de adversidade (como uma queima de um servidor, por exemplo), mantendo, mesmo assim, o banco íntegro e disponível.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/9f7020c4-dab1-4c59-9459-56d3f6a2197a/85a7d684-372d-4a0c-8208-bb1c8ade3ba1.jpg)

## Dica do Professor

Na Dica do Professor, você estudará aspectos relacionados à manutenção de banco de dados, tais como as necessidades do banco de dados, a manutenção em tabelas, a manutenção em SGDBs e as políticas de backup. Assista!

## Exercícios

#### Questão 1
São exemplos de rotinas de manutenção em banco de dados:
Selecione a resposta:
a. Rotina de limpeza e rotina de rede.
b. Rotina de reindexação e rotina de rede.
c. Rotina de manutenção de arquivos e rotina de backup.
d. Rotina de backup e rotina de criação de novos bancos de dados.
e. Rotina de limpeza e rotina de ocupação de espaço em disco.

✅ A alternativa correta é: c. Rotina de manutenção de arquivos e rotina de backup.

#### Questão 2
Em um banco de dados sem manutenção corretiva e preventiva, o banco de dados da empresa passou a apenas aceitar ações de leitura dos dados. O que poderia ocasionar isso?
Selecione a resposta:
a. Espaço do banco sem capacidade de expansão.
b.Uma manutenção em alguma tabela.
c. Uma atualização de sistema.
d. Alguma alteração feita pelo usuário.
e. Uma manutenção feita pelo programador.

✅ A alternativa correta é: a. Espaço do banco sem capacidade de expansão.

#### Questão 3
Em um banco de dados MySQL, quais são os comandos que fazem manutenção em tabelas do banco de dados?
Selecione a resposta:
a. Check table, repair table, analyze table.
b. Check table, repair table, drop table e analyze table.
c. Check table, repair table, optimize table e analyze table.
d. Check table, repair table, create table.
e. Repair table e analyze table.

✅ A alternativa correta é: c. Check table, repair table, optimize table e analyze table.

#### Questão 4
Uma forma de fazer manutenção no banco de dados, sem afetar os usuários, seria?
Selecione a resposta:
a.Acessar o banco de dados e efetuar um check no banco.
b.Copiar o banco de dados em produção e efetuar sua manutenção.
c.Identificar o erro e fazer a manutenção em uma base de testes, gerada por meio da restauração de backup.
d.Identificar o erro e efetuar a manutenção no banco de dados em produção.
e.Informar o programador para bloquear a aplicação.

✅ A alternativa correta é: c. Identificar o erro e fazer a manutenção em uma base de testes, gerada por meio da restauração de backup.


#### Questão 5
Atualmente, temos uma praga virtual chamada ransomware que efetua o sequestro dos dados. Seria uma forma plausível de fazer a manutenção preventiva do banco evitando a destruição causada por esta praga?
Selecione a resposta:
a. Ter o backup do banco de dados em outra partição do disco.
b. Efetuar o backup do banco de dados em um HD USB conectado ao host.
c. Efetuar o backup do banco de dados dentro do próprio disco.
d. Efetuar o backup na nuvem com um aplicativo que fica conectado full time.
e. Efetuar um backup na nuvem periodicamente, porém, não manter o acesso disponível.

✅ A alternativa correta é: e. Efetuar um backup na nuvem periodicamente, porém, não manter o acesso disponível.

## Na prática

As políticas de manutenção de banco de dados, como o uso de backup local e replicação na nuvem, são fundamentais para garantir a confiabilidade, disponibilidade e integridade dos dados empresariais. O backup local assegura a rápida recuperação de informações em caso de falhas de hardware ou erros humanos, enquanto a replicação na nuvem proporciona uma camada adicional de segurança, protegendo contra desastres naturais e problemas locais.

Veja neste Na Prática, o caso de um administrador de banco de dados, que ao implementar tais medidas, pode minimizar o risco de perda de dados críticos e assegurar a continuidade operacional da empresa onde trabalha.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/2753d748-ce27-45a6-9962-3f952e24ceac/95df89f1-df39-4630-91e9-db1351942e89.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Que tal conhecer um pouco do dia-a-dia dos profissionais que trabalham com manutenção de banco de dados? No podcast seguinte são discutidas algumas situações sobre a manutenção de banco de dados.
[Mais](https://fabriciolima.net/blog/2017/03/10/podcast-databasecast-76-manutencao-de-banco-de-dados/)

Veja, a seguir, algumas explicações de tarefas de manutenção SQL Server, importantes para compreender na prática como são realizadas algumas tarefas de manutenção.
[Mais](technet.microsoft.com/pt-br/library/ms140255(v=sql.105).aspx)

Veja mais sobre as tarefas de Manutenção que são usadas, regularmente, em planos de manutenção de banco de dados.
[Mais](https://learn.microsoft.com/pt-br/previous-versions/sql/sql-server-2008-r2/ms140255(v=sql.105)?redirectedfrom=MSDN)

Confira, a seguir, 4 comandos MySQL relacionados à manutenção dos seus bancos de dados.
[Mais](https://elias.praciano.com/2014/03/mysql-comandos-para-manutencao-do-banco-de-dados/)


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


