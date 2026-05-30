## Apresentação

Transações são todas as operações executadas entre o início e o fim de uma operação. Para gerenciar as transações é necessário conhecer as propriedades comumente chamadas de ACID (acrônimo de Atomicidade, Consistência, Isolamento e Durabilidade), que devem ser usadas pelos métodos de controle de concorrência e recuperação do SGBD.
Nesta Unidade de Aprendizagem, vamos analisar as propriedades do gerenciamento de transações, as propriedades ACID e as ferramentas de recuperação de banco de dados.  
Bons estudos.
#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Descrever as propriedades do gerenciamento de transações;
- Relacionar as propriedades ACID (Atomicidade, Consistência, Isolamento e Durabilidade);
- Diferenciar as ferramentas de recuperação de banco de dados.

## Desafio

Imagine que vc é um DBA (Administrador de Banco de Dados) e precisa identificar qual a funcionalidade (ou objetivo) de cada linha marcada na sintaxe abaixo. De sua análise dependem outras tarefas e o sucesso do projeto passa diretamente por seus apontamentos. Atente para o fato de que deve explicar somente as linhas numeradas ao final. Vamos ao trabalho!

START TRANSACTION (1)  
EXIBIR saudações  
OBTER número da conta, numero de identificação pessoal, tipo e quantia  
SELECT número da conta, tipo e saldo (2)  
SE o saldo for positivo ENTÃO  
UPDATE conta lançando o crédito (3)  
UPDATE conta lançando o débito (4)  
INSERT registro de lançamento (5)  
EXIBIR mensagem final e liberar o dinheiro  
SENÃO  
ESCREVER mensagem de erro  
FIM SE  
ERROR: ROLLBACK (6)  
COMMIT (7)

####  ✅ Resposta ao desafio:

(1) START TRANSACTION. Inicia uma transação no banco de dados, Garante que todas as operações subsequentes sejam tratadas como um bloco único, permitindo atomicidade (ou todas as operações são confirmadas, ou nenhuma é).
(2) SELECT número da conta, tipo e saldo. Consulta os dados da conta no banco, Recupera informações necessárias para validar se há saldo suficiente e identificar o tipo de operação.
(3) UPDATE conta lançando o crédito. Atualiza o saldo da conta creditando o valor, Representa a entrada de dinheiro (depósito, transferência recebida, etc.).
(4) UPDATE conta lançando o débito. Atualiza o saldo da conta debitando o valor, Representa a saída de dinheiro (saque, pagamento, transferência enviada).
(5) INSERT registro de lançamento. Insere um registro em uma tabela de movimentações/lançamentos, Serve para manter o histórico contábil da operação, garantindo rastreabilidade.
(6) ROLLBACK. Cancela todas as operações feitas desde o START TRANSACTION, Usado em caso de erro ou inconsistência, garantindo que o banco volte ao estado anterior.
(7) COMMIT. Finaliza a transação com sucesso, Todas as alterações realizadas (UPDATE, INSERT) são persistidas definitivamente no banco.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17213485
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 26/05/26 - 19:17
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

Observe, agora, alguns detalhes que veremos nesta Unidade de Aprendizagem. Vamos conferir!

![](https://statics-marketplace.plataforma.grupoa.education/sagah/b78cf6fc-1f72-47f4-ba37-3ee1fe8a7f68/df958f20-ec72-4ca3-9cc4-a5e9f22901fe.jpg)


## Conteúdo do Livro

O processamento de transações envolve o lado operacional de um banco de dados.  
Enquanto o gerenciamento de operações descreve como os bens materiais são produzidos, o gerenciamento de transações descreve como os bens informacionais ou transações são controlados.

Para entender por que o gerenciamento de transações é extremamente importante para as organizações modernas, acompanhe um trecho da seguinte obra: Projeto, desenvolvimento de aplicações e administração de banco de dados. O livro está na terceira edição e servirá de base teórica para esta Unidade de Aprendizagem.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/775fb429-e7dc-47fa-8258-2e30286cce5d/e30647b8-58e5-4840-b367-6968e1640c9d.jpg)

​​​​​​​
## Dica do Professor

O vídeo a seguir trata do conceito, das propriedades (ACID) e de exemplos de transações, assim como as instruções da linguagem SQL mais importantes para o gerenciamento dessas transações.


## Exercícios

#### Questão 1
Em determinadas transações, existem situações em que uma transação (1) fica na espera de que outra transação (2) seja finalizada para prosseguir com sua execução; isto é negativo, visto que a transação (1) pode ficar em estado de espera por longo tempo ou tempo infinito. A maioria dos SGBDs tem dispositivos e/ou funcionalidades para tratar ou evitar estas situações. Aponte qual das opções a seguir apresenta corretamente que nome se dá a estas situações.

Selecione a resposta:
a. Deadlock
b. Savepoint
c. Log
d. Erro
e. Checkpoint

✅ A alternativa correta é: a. Deadlock.

#### Questão 2
O objetivo do XXXXXXXXXXX é reduzir o tempo de recuperação de falhas em determinadas situações de banco de dados. O registro dos XXXXXXXXXXX é gravado no Log em intervalos específicos para, desse modo, registrar todas as transações ativas. Também neste cenário, o registro do XXXXXXXXXXX pode provocar muitas interrupções no processamento das transações, pois todas as atividades subjacentes dependem deste processo. Aponte qual das opções a seguir apresenta corretamente que nome se dá para XXXXXXXXXXX.

Selecione a resposta:
a. Commit
b. Checkpoint
c. Buffer
d. Backup
e. Rollback

✅ A alternativa correta é: b. Checkpoint.

#### Questão 3
Os XXXXXXXXXXX são também usados por alguns SGBDs corporativos para resolver situações de Deadlock. Em vez de reverter a transação inteira, o SGBD reverte a transação para o seu ultimo estado consistente. O SGBD pode usar pontos implícitos após cada instrução SQL para reduzir a quantidade de trabalho perdido. Aponte qual das opções a seguir apresenta corretamente que nome se dá para XXXXXXXXXXX.
Selecione a resposta:
a. Start Transaction
b. Objetos Distribuídos
c. Savepoint
d. Hot Spots
e. Fluxo de Trabalho

✅ A alternativa correta é: c. Savepoint.

#### Questão 4
Transações são todas as operações executadas entre o início e o fim de uma operação e, para gerenciar as transações, é necessário conhecer as propriedades comumente chamadas de ACID, que devem ser usadas pelos métodos de controle de concorrência e recuperação do SGBD. Aponte qual das opções a seguir apresenta corretamente as propriedades chamadas de ACID.

Selecione a resposta:
a. Atômica Consistente Interna Durável
b. Atômica Controlada Isolada Durável
c. Atômica Consistente Isolada Distribuída
d. Atômica Consistente Isolada Durável
e. Aberta Consistente Isolada Durável

✅ A alternativa correta é: d. Atômica Consistente Isolada Durável. 


#### Questão 5
Os XXXXXXXXXXX são uma forma de impedir que outros usuários acessem um item de dados de um banco que esteja sendo utilizado. Esse item de dados pode ser uma linha, um bloco, um subconjunto de linhas ou mesmo uma tabela inteira. Antes de acessar um item do banco de dados, deve ser obtido um XXXXXXXXXXX. Aponte qual das opções a seguir apresenta corretamente que nome se dá para XXXXXXXXXXX.

Selecione a resposta:
a. Erro
b. Controle
c. Identificador
d. Índice
e. Bloqueio

✅ A alternativa correta é: e. Bloqueio.


## Na prática

A questão do gerenciamento de transações é um dos grandes avanços da tecnologia de banco de dados e, ainda assim, é um assunto que merece atenção especial. No passado, os sistemas de informação atualizavam as informações em arquivos sequenciais indexados ou arquivos de acesso direto que eram mecanismos de armazenamento e consulta de informações bem limitados e sem os recursos de gerenciamento existentes nos sistemas de bancos de dados.

Com o surgimento dos primeiros sistemas multiusuário, onde haviam diferentes usuários acessando e atualizando simultaneamente as informações, surgiu o aspecto da concorrência pelos dados e era necessário administrar todos estes acessos, consultas e atualizações que ocorriam simultaneamente. Os projetistas perceberam rapidamente que todos estes acessos concorrentes poderiam gerar diversos problemas nos dados. Vou citar aqui dois problemas típicos.

1-garantir o isolamento de cada transação para que uma não interferisse na outra, pois haviam situações em que os dados eram atualizados incorretamente.

2-garantir que cada transação fosse atômica de forma a ser concluída integralmente ou não ser efetivada.

![/A imagem mostra uma mulher, vestida de camisa social e terno, segurando um relógio. Desse relógio, através de computação gráfica, saem imagens diversas, como um notebook apresentando gráficos em sua tela; letras, números e cifras; um smartphone; uma lâmpada; um globo terrestre e outras figuras geométricas.](https://statics-marketplace.plataforma.grupoa.education/sagah/3fd84b4b-672a-4ebb-800b-2707609d25b5/450ace9e-8437-4472-bdd0-7d41156713b3.jpg)

Para solucionar estas situações, foram desenvolvidas diversas técnicas chamadas de gerenciamento de transações. Uma transação é uma unidade lógica de operações em um banco de dados. Uma transação pode ser composta de uma ou mais operações de banco de dados, que podem ser de leitura ou de atualização. Estas podem ser operações de inserção (INSERT), atualização (UPDATE) ou exclusão (DELETE). As operações de banco de dados que formam uma transação podem ser embutidas em um programa de aplicação ou podem ser executadas de forma interativa com o uso de SQL em um utilitário de banco de dados. Ou seja, transações podem ser enviadas a partir de programas de aplicação ou por utilitários de banco de dados. Em ambos os casos, devem ser processadas apropriadamente pelo SGBD.


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

 O que é gerenciamento de transações?
[Mais](https://www.ibm.com/br-pt/think/topics/transaction-management#:~:text=Resumidas%20na%20sigla%20ACID%2C%20as,no%20banco%20de%20dados%20mestre.)

O texto a seguir trata do controle de concorrência entre transações em bancos de dados usando técnica de bloqueio em duas fases:
[Mais](https://www.devmedia.com.br/controle-de-concorrencia-entre-transacoes-em-bancos-de-dados/27756)


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





