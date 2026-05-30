## Apresentação

Nesta Unidade de Aprendizagem, trataremos dos modelos de programação utilizados em duas arquiteturas de processadores: arquitetura baseada em pilhas e arquitetura baseada em registradores de propósito geral. Um modelo de programação de processadores define como as instruções estão descritas na linguagem de montagem e como elas buscam os seus operandos. Essas instruções podem realizar operações aritméticas, de comparação, de memória e de controle.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Conhecer os diferentes tipos de operações existentes na maioria dos processadores.
- Reconhecer a arquitetura baseada em pilhas e a baseada em registradores.
- Escrever programas em linguagem de montagem para arquiteturas baseadas em pilhas e em registradores de propósito geral.

## Desafio

Priscila é uma aluna muito interessada e sempre busca melhorar a eficiência dos sistemas que desenvolve. Atualmente, está envolvida em um projeto de robótica. Ela não gostaria de utilizar processadores existentes no mercado, e sua ideia é projetar um processador para seu robô.

  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/a1c48d09-c1f4-4b58-b951-e336af01bbc6/8dcd6d4b-4251-4325-9f26-2dd20eda0953.jpg)

Escreva o que a professora de Priscila pode ter respondido.

####  ✅ Resposta ao desafio:

A professora poderia ter respondido algo assim para Priscila:

A escolha da arquitetura depende muito das necessidades do sistema embarcado. 
Em arquiteturas baseadas em pilha, as operações são simples e diretas, pois os dados são manipulados sempre no topo da pilha.
Isso pode reduzir a complexidade do hardware, mas limita a flexibilidade.
Já as arquiteturas baseadas em registradores de uso geral oferecem maior desempenho e versatilidade, porque permitem acessar diretamente diferentes registradores, otimizando cálculos e manipulação de dados.
Em sistemas embarcados como robôs, onde eficiência e velocidade são importantes, normalmente se adota a arquitetura baseada em registradores, pois ela facilita o desenvolvimento de algoritmos de controle e processamento de sinais.
No entanto, se o objetivo for simplicidade e baixo custo de implementação, a arquitetura de pilha pode ser considerada.
O ideal é analisar os requisitos do robô, consumo de energia, velocidade de resposta e complexidade das operações para decidir qual arquitetura se encaixa melhor.

Assim, a professora mostra que não existe uma resposta única, a decisão depende do equilíbrio entre simplicidade e desempenho que o projeto exige.


## Infográfico
O infográfico apresenta os modelos de programação.


![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/b2ab8446-9741-4c41-b917-efc89030ac6d/4a7cbe7a-4a7a-43c7-a281-4a011f9c54ed.jpg)


## Conteúdo do Livro

Leia o capítulo Modelos de programação, do livro Arquiteturas de Computadores, base teórica desta unidade

Boa leitura!

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/7d49bbc1-0aae-48e5-a611-82efb732b0e7/452d849a-331b-4f63-90ba-2c2d5b9c59ef.jpg)

​​​​​​​​​​​​​​
## Dica do Professor

 Acompanhe, no vídeo a seguir, uma síntese dos conceitos desta Unidade de Aprendizagem.


## Exercícios

#### Questão 1
Qual é o conteúdo da pilha depois que a sequência a seguir for completada?

PUSH #2
PUSH #4
PUSH #6
ADD
PUSH #2
MUL
SUB

Selecione a resposta:
a. -18.
b. 18.
c. -14.
d. 24.
e. 40.

✅ Esta é a resposta correta: a -18.


#### Questão 2
Qual o valor do registrador r3 depois que a seguinte sequência for executada?

MOV r1, #31
MOV r3, #12
MOV r2, #14
SUB r3, r3,r2
MUL r2,r2,r2
ADD r3,r1,r2

Selecione a resposta:
a. -2.
b. 12.
c. 227.
d. 59.
e. 225.

✅ Resposta correta: c) 227.

#### Questão 3
Qual valor permanece na pilha depois da seguinte sequência de execução?

PUSH #1
PUSH #2
POP
PUSH #3
POP
POP

Selecione a resposta:
a. 1.
b. 8.
c. 3.
d. 5.
e. Vazia.

✅ Resposta correta: e) Vazia.


#### Questão 4
Na arquitetura de pilha, o processador controla um conjunto de registradores organizados como uma pilha, e esta é utilizada como fonte de dados para o trabalho da unidade lógica e aritmética. Sobre as características do modelo de programação baseado em pilha, analise as afirmações a seguir:

I. No modelo de programação baseado em pilha, devemos especificar onde a fonte e o destino da operação estão localizados.
II. O banco de registradores em um modelo de programação baseado em pilha é invisível ao programador.
III. No modelo de programação baseado em pilha, há o gerenciamento automático dos registradores.
É correto o que se afirma em:
Selecione a resposta:
a. I, II e III.
b. I e III, apenas.
c. I, apenas.
d. II e III, apenas.
e. I e II, apenas.

✅ Resposta: d) II e III, apenas.


#### Questão 5
É uma das vantagens do modelo de programação baseado em registradores de uso geral, quando comparado com um modelo de programação baseado em pilha:
Selecione a resposta:
a. Ler um registrador em um arquitetura RUG não afeta seu conteúdo.
b. Ter o banco de registradores invisível para o programador.
c. Poder executar uma nova implementação de um programa escrito para o processador antigo, mesmo contendo números diferentes de registradores.
d. O conjunto de instruções não muda se o tamanho do banco de registradores mudar.
e. Não precisa de muita memória para ser implementada.

✅ A vantagem correta é: a. Ler um registrador em uma arquitetura RUG não afeta seu conteúdo.


## Na prática

Aline é uma estudante de Computação e, por isso, usa muito a tecnologia para ajudá-la nas tarefas do dia a dia. Ela utiliza vários aplicativos no celular para se organizar na hora dos estudos, além do navegador da internet, para pagar a mensalidade dos cursos que faz, e de codificatr diversos programas.

A estudante começou a pensar nessas aplicações, cada uma escrita em determinada linguagem, e perguntou-se: como será que essas linhas de código são interpretadas pelo hardware do celular ou do notebook?
  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/d37e5b18-17b6-4bd1-a9c2-289ad7dfb0ef/c9006b83-a574-4f51-9143-568c586cb8a1.jpg)

  

De posse dessa informação, ficou mais fácil para Aline escolher um aplicativo mais eficiente ou, até mesmo, escrever a linguagem de programação adequada para o modelo de programação do sistema no qual a aplicação está sendo executada.

## Saiba mais
Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

#### Processador CISC e RISC
Neste vídeo você entenderá uma explicação básica sobre a diferença entre CISC e RISC.
[Mais]([Processador CISC e RISC - YouTube](https://www.youtube.com/embed/m1uKe6GdjOE))

#### Entenda os diferentes tipos de processadores
Qual o processador ideal para melhorar o desempenho de seu computador? Existem inúmeros tipos de modelos disponíveis nas lojas com características e potências diferentes. veja a seguir
[Mais](https://razorcomputadores.com.br/blog/tecnologia/entenda-os-diferentes-tipos-de-processadores/)

#### Engenharia de Software: uma abordagem profissional
Para se aprofundar mais em arquiteturas de computadores, leia este livro, que apresenta o conteúdo pertinente ao que foi estudado nesta Unidade de Aprendizagem.
[Mais]([Plataforma A](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=56838188&tokenId=26ed9f41-9fd8-4e72-a2b7-cbbd8f004583))


##  REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

Banco de Imagens: Shutterstock.

NULL, L.; LOBUR, J. Princípios básicos de arquitetura e organização de computadores. 2.ed. Porto Alegre: Bookman, 2010

SAGAH, 2014.

