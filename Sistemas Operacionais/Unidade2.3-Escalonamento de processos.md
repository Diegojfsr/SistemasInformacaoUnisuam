## Apresentação

Nos computadores atuais, é comum que, em qualquer tarefa que o usuário executar, diversos processos e threads estejam disputando acesso à unidade de processamento ou outros recursos. Por exemplo, quando um processo espera pela leitura dos dados em um dispositivo de entrada, este não pode bloquear o uso da unidade de processamento para outros processos, logo, ele deve ser substituído pelo próximo.

Essa tarefa de organizar como os processos devem ser executados é responsabilidade do escalonador de processos, que por meio de uma política de decisões, conhecida como algoritmo de escalonamento, define a sequência de execução dos processos, de modo a tentar otimizar a utilização dos recursos.

Nesta Unidade de Aprendizagem, você vai aprender o que é um escalonador de processos, diversos detalhes de seu funcionamento e quais são as principais estratégias utilizadas.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir um escalonador de processos e suas características.
- Diferenciar escalonamento de processos preemptivo e não preemptivo.
- Identificar os tipos de algoritmos utilizados em escalonamento de processos.


## Desafio

Os sistemas operacionais modernos lidam com diversos processos ao mesmo tempo, atribuindo a cada um desses os recursos necessários assim que disponíveis. Saber qual processo escolher para execução é uma decisão difícil, pois depende das características de cada processo, assim como do estado atual do sistema e da estratégia de escalonamento adotada.


![](https://statics-marketplace.plataforma.grupoa.education/sagah/b3ae7f35-c028-46e9-b293-4c8d6e38c6a7/9ffbdee7-17fd-47da-a9b4-e5ecb5b444a3.png)

Recentemente, você começou a receber e-mails de alguns professores se queixando da demora na resposta das requisições enviadas para as pesquisas. Você sabe que os professores precisam ter um certo nível de prioridade, contudo, os alunos não podem deixar de ser atendidos por longos períodos de tempo, porque os trabalhos deles também precisam ser entregues e você sabe como é ter a pressão de prazos como aluno.

Após uma análise do perfil das requisições enviadas, você conseguiu categorizá-las em três grupos com prioridade decrescente, respectivamente:
1 - Requisições de professores
2 - Requisições de alunos para projetos de pesquisa
3 - Requisições de alunos para trabalhos das disciplinas
Sabendo que você pode gerenciar o escalonamento das requisições, qual estratégia seria a melhor solução para esse problema? Por quê?

#### Padrão de resposta esperado
A estratégia que se encaixa como melhor solução é o algoritmo de escalonamento de múltiplas filas. A utilização dessa solução permite que as requisições possam ser categorizadas em diferentes níveis de prioridade, contudo, essa prioridade é flexível, pois, conforme várias execuções das requisições mais importantes, elas caem em nível de prioridade, permitindo que outras sejam executadas e não tomem todo o processamento delas.
Uma opção que pode ter passado em mente é o escalonamento por prioridades, contudo, essa alternativa não é viável, pois, se houver pelo menos uma requisição feita por um professor, as demais categorias de processos nunca serão executadas e essa é uma situação inaceitável.

####  ✅ Resposta ao desafio:

Com base no cenário apresentado e nos objetivos de equilibrar a prioridade dos professores com o atendimento aos alunos, a melhor solução é o algoritmo de escalonamento de múltiplas filas (frequentemente conhecido como Multilevel Queue Scheduling ou Multilevel Feedback Queue).

Por que essa é a melhor solução?
Flexibilidade e Prevenção de Inanição (Starvation): Embora o escalonamento por prioridades estritas pareça atraente à primeira vista, ele causaria um problema grave: se houvesse um fluxo contínuo de requisições de professores, os alunos (tanto de pesquisa quanto de trabalhos de disciplinas) nunca teriam suas requisições atendidas. As múltiplas filas permitem gerenciar os níveis de prioridade de forma dinâmica, garantindo que as requisições de menor prioridade ainda tenham oportunidade de execução após um tempo.

Atendimento Hierárquico Adequado: A estrutura de filas separadas permite alocar cada um dos três grupos (professores, projetos de pesquisa de alunos e trabalhos de disciplinas) em seu respectivo nível, respeitando a ordem de importância sem comprometer a estabilidade geral do sistema do departamento.


## Infográfico

O desempenho de um processo depende muito de quais tarefas esse executa, assim como a eficiência que lida com os recursos disponíveis pelo sistema. De modo geral, o comportamento dos processos tende a alternar entre o processamento e o acesso a recursos, que podem ser de diferentes tipos.

No Infográfico a seguir, você vai conhecer melhor o comportamento de um processo e quando este pode ser escalonado.

![](https://statics-marketplace.plataforma.grupoa.education/sagah/e2ded593-83cc-42ea-a730-abb94ecddc25/0e82864e-7055-46e0-8cd5-4388533e1d9b.jpg)

​​​​​​​

## Conteúdo do Livro

A complexidade de um sistema operacional aumenta com a presença de múltiplos processos ativos. Os computadores modernos são capazes de gerenciar os processos de uma infinidade de tarefas diferentes, permitindo enfileirar vários processos para execução. No entanto, há diferentes estratégias para determinar a ordem em que os processos serão executados.

Dessa forma, no capítulo Escalonamento de processos, base teórica desta Unidade de Aprendizagem, você entenderá quem é o responsável por organizar a ordem de execução dos processos, como estas estratégias são definidas e quais as principais características de um escalonador de processos e seus tipos.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/b49b051e-5ff3-4b1c-a16c-406f7185b62b/cacbd377-1137-4cf2-b91e-377da3b539d3.jpg)


## Dica do Professor

A existência de diversos processos ativos em um sistema operacional trouxe maior complexidade. Quando os computadores eram voltados a tarefas mais específicas, o sistema operacional permitia a existência de múltiplos processos, contudo, somente ficava pronto um por vez, aguardando a sua execução.

Atualmente, os computadores gerenciam também múltiplos processos, porém de tarefas diferentes, o que permite a espera de vários processos prontos em uma fila. Entretanto, estar em uma fila de espera não significa ser executado nessa ordem, necessariamente. A decisão de qual processo executar pode se basear em diferentes estratégias, as quais são conhecidas como algoritmos de escalonamento de processos.

Nesta Dica do Professor, você aprenderá os principais algoritmos de escalonamento e as categorias pertencentes a ele.​​​​​​​


## Exercícios

#### Questão 1
Em um computador de um usuário existem três processos (A, B e C) na fila de escalonamento, respectivamente, competindo pelo uso da unidade de processamento. Sabe-se que o sistema operacional implementa o algoritmo round-robin e também que o quantum é 10ms. Todos os processos são dependentes da unidade de processamento apenas, e o tempo estimado de execução de cada um é, respectivamente, 10ms, 40ms e 60ms.
Depois de quantos milissegundos o processo B estará encerrado?
Selecione a resposta:
A.100ms.
B.80ms.
C.50ms.
D.40ms.
E.10ms.

✅ A alternativa correta é: B


#### Questão 2
Os algoritmos de escalonamento podem ser divididos em duas principais categorias: preemptivos e não preemptivos. A respeito da preempção, assinale a alternativa correta quanto às possíveis consequências que a sua implementação pode ocasionar:
Selecione a resposta:
A.Um algoritmo preemptivo permite que os processos executem por períodos superiores a um dado quantum​​​​​​​, mesmo que haja outros na fila.
B.Um algoritmo não preemptivo sempre interrompe um processo após um determinado quantum.
C.Um algoritmo preemptivo interrompe a execução do processo quando este ainda está em execução, porém consome todo o seu quantum.
D.Um algoritmo preemptivo somente escalona um processo quando este sofre uma interrupção de entrada/saída.
E.Um algoritmo preemptivo somente escalona um processo quando este aciona o bloqueio para entrada/saída.

✅ A alternativa correta é: C

#### Questão 3
Em decorrência da variedade de tipos de processo e usuários, a obtenção de um algoritmo ótimo não é uma tarefa fácil, pois haverá pontos fortes e fracos em cada abordagem. Contudo, existem características essenciais para grupos específicos de usuários ou processos. Quanto aos processos voltados aos sistemas em lote, qual das seguintes características é relevante somente para essa categoria em específico?
Selecione a resposta:
A.Vazão.
B.Justiça.
C.Previsibilidade.
D.Cumprimento de prazos.
E.Tempo de resposta.

✅ A alternativa correta é: A

#### Questão 4
Um aspecto importante no processo de escalonamento é a definição do quantum de cada processo. A definição de um intervalo de tempo maior ou menor pode resultar em pontos positivos ou negativos. Quanto a isso, assinale a alternativa correta:
Selecione a resposta:
A.O processamento de escalonamento não tem uma perda significante de desempenho com um quantum de 4ms e chaveamento de processo de 1ms.
B.O processo de escalonamento de um quantum de 100ms não resulta em grande tempo de espera em filas com 100 processos.
C.A utilização de um quantum grande (maior que 50ms) pode agilizar o tempo de resposta em processos que tomem menos de 10ms.
D.O uso de um quantum pequeno gera uma perda maior pelo chaveamento em relação ao processamento.
E.O tempo de chaveamento de processo é insignificante para qualquer quantum adotado.

✅ A alternativa correta é: D


#### Questão 5
Um sistema operacional A implementa o algoritmo de escalonamento "tarefa mais curta primeiro". Considerando que em um dado momento existem cinco processos na fila, cada um com os respectivos tempos 20ms, 10ms, 15ms, 12ms e 5ms. Qual é o (s) tempo (s) de retorno desse conjunto de processos?
Selecione a resposta:
A.20, 30, 45, 57 e 62.
B.5, 15, 27, 42 e 62.
C.42,8
D.11,4.
E.20, 35, 47, 57, 62.

✅ A alternativa correta é: B


## Na prática

Existem diversos algoritmos de escalonamento, cada qual com uma estratégia específica em busca de resolução do problema. As aplicações podem ter características específicas que façam um algoritmo ser melhor em um cenário e pior em outro. Nesse sentido, realmente é difícil obter um algoritmo que seja ótimo para todos os casos.

Na Prática, você vai conhecer um cenário de aplicação de algoritmos de escalonamento, em que uma escolha errada pode resultar em muitos problemas.


![](https://statics-marketplace.plataforma.grupoa.education/sagah/5eec8d48-6441-470e-845e-c7fd9ce495a5/2a9a78c5-49d4-4c77-9cd7-d58a5e28a2e4.jpg)

​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Projeto de implementação de um escalonador em Java
Neste projeto, você poderá conhecer, de forma didática, a implementação de um escalonador de processos usando a linguagem Java para os algoritmos first-come first-served, shortest job first e round robin.
[Mais](https://github.com/douglasrafael/Escalonador)

Escalonamento de processos
Nesta videoaula da Univesp TV, você poderá aprender quais são os principais algoritmos de escalonamento de processos usados em sistemas operacionais.
[Mais](https://www.youtube.com/embed/MWbPgxOCrFk)

Processos e escalonamento em sistemas operacionais
Nesta videoaula da Univesp TV, você poderá rever os conceitos vistos e algumas categorias de algoritmos de escalonamento.
[Mais](https://www.youtube.com/embed/mVz3s_03GkA)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

DEITEL, H. M.; DEITEL, P.J .; CHOFFNES, D. R. Sistemas Operacionais: tradução A. L.
Marques. 3. ed. São Paulo: Pearson Prentice Hall, 2005. p. 88-97.

GARCIA, Islene C. Escalonamento de Processos e Threads. Disponível em:
<http://www.ic.unicamp.br/~islene/1s2008-mc514/sched/sched.pdf>. Acesso em: 18 dez. 2019.

MELO NETO, Adão. Gerência do Processador. Disponível em:
<https://www.ime.usp.br/~adao/GERENCIADOPROCESSADOR.pdf>. Acesso em: 18 dez. 2019.

TANEMBAUM, Andrew S. Sistemas operacionais modernos. Tradução R. A. L. Gonçalves, L. A.
Consularo, L. A. Teixeira. Processos e threads. 3. ed. São Paulo: Pearson Prentice Hall, 2010. p.87-98.

Banco de imagens Shutterstock.
SAGAH, 2020
