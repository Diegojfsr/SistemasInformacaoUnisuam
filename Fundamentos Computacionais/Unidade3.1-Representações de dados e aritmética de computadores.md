## Apresentação

O computador recebe, processa e transmite grandes volumes de dados provenientes de aplicações e usuários. Para que esse fluxo seja possível, é necessário que os dados sejam convertidos para uma forma compreensível pela máquina, que opera por meio de variações elétricas em seus componentes de hardware. Essas variações são interpretadas e transformadas em valores matemáticos e lógicos que possibilitam sua utilização nos diferentes níveis do sistema, afirma Stallings (2020).

Como os circuitos eletrônicos trabalham apenas com dois estados, ligado e desligado, a matemática computacional utiliza o sistema numérico binário como base para as funções executadas internamente. Nesse sistema, os símbolos zero (0) e um (1), denominados "bits", representam a menor unidade de informação. A partir dessa lógica, torna-se possível representar números, caracteres e demais informações digitais, explicam Tanenbaum e Bos (2022).

Nesta Unidade de Aprendizagem, você vai aprender como os computadores representam internamente os números, as letras e todo tipo de informação. Também vai conhecer o funcionamento e a aritmética desse sistema, que é a base para os computadores atuais.  

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Identificar como os computadores representam os dados internamente.
- Converter números do sistema de numeração decimal para o sistema de numeração binário, sejam eles positivos ou negativos.
- Realizar operações aritméticas básicas no sistema de numeração binário.


## Desafio

Os computadores não armazenam diretamente letras, imagens ou sons como os seres humanos os percebem. Toda informação precisa ser convertida em sequências de 0 e 1, chamadas "bits", que formam códigos binários interpretados de acordo com o contexto. Tanenbaum e Bos (2022) explicam que essa representação digital é a base do funcionamento dos sistemas computacionais modernos, permitindo que símbolos abstratos sejam processados por circuitos eletrônicos de maneira uniforme e previsível.

A partir dessas informações, considere-se parte da situação a seguir:

![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/57774/9125_EXA_DES_V0-2025-08-28T15:44:46-03:00.png)

Como profissional responsável diante desse contexto, responda:

Qual é a explicação para o erro de exibição dos nomes com acentos e cedilha no sistema e qual solução prática pode ser aplicada para garantir que os dados sejam armazenados e apresentados corretamente?

####  ✅ Resposta ao desafio:

O erro de exibição dos nomes com acentos e cedilha ocorre porque o sistema não está tratando corretamente a codificação de caracteres. Em outras palavras, os dados estão sendo armazenados ou lidos em um formato diferente daquele usado para exibir as informações.

Explicação
Codificação de caracteres: define como os símbolos (letras, acentos, cedilhas) são representados em bits (0 e 1).
Se banco de dados, aplicação e interface não usam a mesma codificação, ocorre incompatibilidade.
UTF-8 é hoje o padrão mais utilizado, pois suporta todos os caracteres da língua portuguesa e de outros idiomas.

Solução prática
Padronizar a codificação em todas as camadas do sistema (banco de dados, aplicação e interface).
Configurar o banco de dados para armazenar em UTF-8.
Garantir que a aplicação leia e escreva dados também em UTF-8.
Definir a codificação correta nos arquivos de configuração e no front-end (HTML, APIs etc.).

Migrar os dados já armazenados para a codificação correta, evitando que registros antigos continuem exibindo erros.

Testar com nomes reais contendo acentos e cedilhas para validar que a solução funciona em relatórios e certificados.

O problema é causado por inconsistência na codificação de caracteres. A solução é adotar UTF-8 de ponta a ponta no sistema, garantindo que os nomes sejam armazenados e exibidos corretamente em qualquer contexto.


## Infográfico

As operações aritméticas no sistema binário utilizam apenas os dígitos 0 e 1, manipulados em nível de hardware por meio de circuitos digitais. A soma segue regras de transporte, a subtração utiliza empréstimos, a multiplicação é feita com deslocamentos, e a divisão, com subtrações sucessivas. Segundo Stallings (2020), essa lógica permite que instruções complexas sejam reduzidas a operações básicas implementadas eletronicamente.

A adoção do binário está ligada à estabilidade da eletrônica digital, que trabalha com dois estados de tensão. Tanenbaum e Bos (2022) destacam que essa abordagem garante padronização e confiabilidade na execução de cálculos, tornando possível a construção de arquiteturas escaláveis em sistemas computacionais modernos.

Neste Infográfico, você vai visualizar de forma clara como os cálculos são realizados no sistema binário, desde a aplicação das regras de soma, subtração, multiplicação e divisão até a obtenção dos resultados finais em base 2, que servem de suporte para todo o processamento computacional.

![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/57775/info_ok-2026-03-02T14:34:02-03:00.png)


## Conteúdo do Livro
A representação de dados no interior dos computadores está fundamentada no sistema binário, no qual todos os elementos, sejam números, caracteres ou instruções, são traduzidos em combinações de 0 e 1. Esse modelo de codificação permite que a eletrônica digital opere de forma confiável, já que cada bit corresponde a dois estados possíveis de tensão. Segundo Stallings (2020), a utilização do binário assegura simplicidade na implementação de circuitos e eficiência na execução de operações fundamentais, como leitura, escrita e cálculos básicos.

De acordo com Tanenbaum e Bos (2022), a aritmética binária sustenta a execução das operações fundamentais de soma, subtração, multiplicação e divisão diretamente no hardware. Embora distintas da lógica decimal aplicada no cotidiano, essas operações constituem a base para instruções mais complexas nos processadores modernos. Assim, a matemática discreta se conecta diretamente ao funcionamento interno das máquinas digitais, fornecendo o alicerce para o desenvolvimento de sistemas computacionais atuais.

No capítulo Representações de dados e aritmética de computadores, base teórica desta Unidade de Aprendizagem, você vai estudar como os computadores representam internamente os dados por meio do sistema binário. Além disso, vai aprender os fundamentos das operações aritméticas em base 2, incluindo soma, subtração, multiplicação e divisão.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/02665095-a1f9-4738-9d40-93e292d92d42/a3c78eff-89a5-44de-a034-00a8dc528b2a.jpg)


## Dica do Professor

Os computadores permeiam praticamente todas as atividades humanas, processando vastas quantidades de dados em frações de segundo. Essa capacidade decorre de métodos rigorosos de codificação e manipulação da informação, que permitem converter fenômenos do mundo real em representações compatíveis com o funcionamento dos circuitos digitais (Tanenbaum; Bos, 2022).

Internamente, o sistema binário, formado pelos dígitos 0 e 1, serve como base para codificar qualquer tipo de dado, desde números até instruções complexas. As operações aritméticas (soma, subtração, multiplicação, divisão) executadas nesse sistema permitem que algoritmos simples ou aplicações sofisticadas sejam implementados com alta precisão e desempenho, garantindo a eficiência do processamento digital (Harris; Harris, 2021).

Nesta Dica do Professor, você vai ver como os dados são representados e manipulados internamente pelo computador e como as operações aritméticas básicas são realizadas em linguagem binária. Assim, você vai reconhecer como a lógica matemática sustenta a base de toda a computação moderna.

## Exercícios

#### Questão 1
Os sistemas de numeração constituem um dos fundamentos da matemática aplicada à computação. A forma posicional, utilizada em diferentes bases, organiza os símbolos de acordo com regras que permitem representar e manipular quantidades de maneira estruturada.

Analise a seguinte situação:

Em um ambiente de análise de dados, os engenheiros discutem a confiabilidade da informação quando diferentes sistemas de numeração são utilizados para representar grandezas digitais. O princípio posicional, aplicado a diversas bases, define o valor de cada dígito a partir da interação entre o símbolo utilizado e sua posição dentro da sequência. Esse conceito é fundamental para compreender como computadores manipulam dados e realizam operações aritméticas.

Com base nesse contexto, qual interpretação sobre sistemas de numeração posicional é mais adequada?
Selecione a resposta:
a. O sistema posicional estabelece que cada símbolo recebe um peso definido por potências sucessivas da base, variando de acordo com sua posição na sequência numérica.

b. A variação da base em diferentes sistemas numéricos altera a quantidade de dígitos disponíveis, mas mantém constantes os valores posicionais atribuídos a cada símbolo.

c. O princípio posicional, embora aplicável em diversas bases, encontra limitações em operações digitais, pois nem todos os valores podem ser representados sem perdas de precisão.

d. Em sistemas digitais, a interpretação posicional pode ser flexibilizada, de modo que diferentes símbolos compartilhem pesos iguais quando submetidos a processos de codificação.

e. A aplicação do sistema posicional em arquiteturas computacionais ocorre de forma distinta da teoria matemática, já que a representação digital prioriza circuitos lógicos em detrimento de pesos numéricos.

✅ A alternativa correta é: a) O sistema posicional estabelece que cada símbolo recebe um peso definido por potências sucessivas da base, variando de acordo com sua posição na sequência numérica.


#### Questão 2
Os sistemas de numeração permitem representar quantidades em diferentes bases de forma organizada. Esse princípio matemático garante consistência e precisão nas operações realizadas em diferentes sistemas de numeração.

Dessa forma, analise o seguinte cenário:

Na implementação de um protocolo de comunicação entre módulos de hardware, a equipe de desenvolvimento identificou divergências nos resultados ao converter dados entre diferentes bases numéricas. A investigação revelou que o problema estava relacionado a interpretações incorretas sobre a correlação entre a posição e o valor de cada dígito.

Com base nesse contexto, qual princípio matemático deve ser aplicado para garantir a conversão precisa entre bases numéricas distintas?
Selecione a resposta:
a. Utilização de fatoriais para determinar o peso de cada dígito nas diferentes bases.
b. Aplicação do logaritmo natural para normalização dos valores de cada dígito.
c. Emprego da soma ponderada com base na potência da ordem da base numérica.
d. Uso de coeficientes binomiais para reorganização dos dígitos conforme a base.
e. Conversão direta por substituição simbólica sem operações aritméticas.

✅ A alternativa correta é: c) Emprego da soma ponderada com base na potência da ordem da base numérica.


#### Questão 3
Em sistemas digitais que recebem informações de múltiplos dispositivos, os dados podem ser transmitidos em diferentes formatos numéricos. Compreender como cada sistema representa os números é fundamental para interpretar corretamente os valores e evitar divergências durante a comunicação entre módulos de hardware.

Nesse sentido, analise a situação a seguir:

Durante o desenvolvimento de um sistema que recebe dados de múltiplos sensores digitais, a equipe de engenharia observou que a representação da informação variava conforme a base utilizada para codificação. Alguns sensores transmitiam valores em base 2, outros utilizavam base 8, e, em relatórios técnicos, apareciam valores em base 16 para facilitar a leitura. Foi solicitado que um estagiário explicasse corretamente o papel dos sistemas de numeração binário, octal e hexadecimal na representação de dados, analisando como cada um estabelece a relação entre dígito, posição e base numérica.

Com base nesse cenário, avalie as afirmativas a seguir:
I. No sistema binário, cada posição à esquerda corresponde a um valor duas vezes maior que a posição anterior, e os dígitos possíveis são apenas 0 e 1.
II. No sistema octal, cada posição à esquerda equivale a oito vezes a anterior, e a representação envolve símbolos de 0 até 7, o que torna o processo de conversão direta com o binário mais simples.
III. O sistema hexadecimal utiliza 16 símbolos distintos, e cada posição à esquerda corresponde a um valor dez vezes maior que a posição imediatamente à direita.
IV. A notação posicional garante que, em qualquer uma das bases, o valor do número é obtido pela soma dos produtos de cada dígito pelo peso da posição correspondente.

É correto o que se afirma em:
Selecione a resposta:
a. I e II, apenas.
b. II e III, apenas.
c. III e IV, apenas.
d. I, II e IV, apenas.
e. I, II e III, apenas.

✅ As afirmativas corretas são: I, II e IV. Resposta: d) I, II e IV, apenas.

#### Questão 4
No estudo de aritmética computacional, a representação em complemento de dois é amplamente utilizada para codificar números inteiros com sinal, que permite operações de soma e subtração diretamente em nível binário. Ao considerar um sistema de 8 bits, cada valor é expresso levando em conta o bit mais significativo como indicador de sinal e os demais bits para o valor absoluto ou ajustado pela codificação.

A partir dessas premissas, determine qual é o resultado binário obtido ao efetuar a operação −17 + 15 nesse formato:
Selecione a resposta:
a. 0011000.
b. 00000010.
c. 00100000.
d. 11111110.
e. 00001110.

✅ Resposta correta: d) 11111110.

#### Questão 5
Em aritmética binária com tamanho de palavra fixo, processadores tratam resultados com saturação modular (envolvendo “estouro” por limite de bits) e sinal segundo a representação em complemento de dois. Nessas condições, a interpretação do resultado depende de bandeiras como carry e overflow, das regras que relacionam adição e subtração e das propriedades algébricas sob aritmética módulo 
2n. Entender quando há erro de faixa (overflow) e como a subtração é implementada impacta diretamente a confiabilidade de rotinas de cálculo.

Com base nesse contexto, indique a proposição correta sobre operações em complemento de dois (palavra de 8 bits):
Selecione a resposta:
a. Em complemento de dois, o overflow em A−B coincide com a ocorrência de empréstimo no bit mais significativo.

b. Em 8 bits, implementar A−B como A+ complemento de um de B produz o mesmo resultado binário que a subtração, sem ajustes adicionais.

c. No modo "sem sinal" (unsigned), a presença de carry-out da soma indica overflow apenas quando os operandos têm sinais distintos.

d. Se A+B produz overflow em complemento de dois, então o valor de 8 bits obtido é igual ao valor inteiro matemático da soma em Z.

e. Em 8 bits com complemento de dois, o overflow na soma A+B ocorre exatamente quando os carries que entram e saem do bit mais significativo são diferentes.

✅ A alternativa correta é: e) Em 8 bits com complemento de dois, o overflow na soma A+B ocorre exatamente quando os carries que entram e saem do bit mais significativo são diferentes.

## Na prática

A comunicação digital e o tratamento eficiente de dados dependem diretamente da forma como essas informações são representadas internamente no computador. Cada número, caractere ou sinal transmitido é codificado em sequências binárias que seguem padrões bem definidos de representação e conversão. Essa codificação garante precisão, compatibilidade e integridade das informações durante processamento e transmissão.

Os sistemas digitais modernos utilizam estruturas como o complemento de dois e o sistema de base 2 para lidar com operações aritméticas e representação de sinais. Esses mecanismos permitem que processos computacionais sejam consistentes e escaláveis, facilitando o desenvolvimento de softwares e hardwares complexos (Tanenbaum; Bos, 2022). A adoção dessas normas padronizadas assegura confiabilidade e uniformidade no tratamento de dados em diferentes plataformas.

Neste Na Prática, você vai acompanhar um exemplo aplicado sobre como falhas nesse alinhamento podem gerar resultados incorretos em sistemas reais. Esses erros afetam diretamente a integridade das informações e a tomada de decisão.

  
![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/57779/capa-2025-08-28T15:42:33-03:00.png)


## Saiba mais
Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

#### Sistema de numeração binário – aprenda por que 1+1 = 10
Assista a este vídeo para entender por que no sistema binário 1 + 1 é igual a 10. Em poucos minutos, você vai aprender, de forma clara e divertida, como funciona a lógica da soma em base 2. Esse conceito está fundamentado na ideia de que os sistemas de numeração organizam os símbolos de acordo com regras próprias, o que permite diferentes formas de representar quantidades.
[Mais]([Sistema de numeração binário - Aprenda porque 1+1 = 10 - YouTube](https://www.youtube.com/embed/voTxrVCU3Xk?si=Egg6SZqzQwABFsYj))

#### Sistemas digitais – fundamento e aplicações
Leia o Capítulo 2, "Sistemas de numeração, operações e códigos". Nele, você vai aprofundar o seu entendimento sobre sistemas de numeração e sua aplicação prática em computação. Neste capítulo, confira, de forma detalhada, a base teórica dos números decimais, binários, octais e hexadecimais, além de operações aritméticas, códigos digitais e métodos de conversão entre diferentes sistemas.
[Mais]([Plataforma A](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=59635713&tokenId=26ed9f41-9fd8-4e72-a2b7-cbbd8f004583))

#### Sistemas digitais: projeto, otimização e HDLs
Leia o Capítulo 1, "Introdução", deste livro. A partir desta leitura, você vai compreender os fundamentos iniciais sobre sistemas digitais. O capítulo apresenta uma visão geral sobre o impacto dos sistemas digitais no cotidiano, a importância dos microprocessadores no desenvolvimento de projetos e os elementos essenciais que compõem a base da lógica digital.
[Mais]([Plataforma A](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=59636083&tokenId=26ed9f41-9fd8-4e72-a2b7-cbbd8f004583))


##  REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

HARRIS, D. M.; HARRIS, S. L. Digital design and computer architecture. 2. ed. Amsterdam: Morgan Kaufmann, 2021.

NULL, L.; LOBUR, J. Princípios básicos de arquitetura e organização de computadores. 2. ed. Porto Alegre: Bookman, 2010.

STALLINGS, W. Arquitetura e organização de computadores. 10. ed. São Paulo: Pearson, 2020.

TANENBAUM, A. S.; BOS, H. Sistemas operacionais modernos. 4. ed. São Paulo: Pearson, 2022.

Bancos gratuitos de imagens e Shutterstock. 
SAGAH, 2025
