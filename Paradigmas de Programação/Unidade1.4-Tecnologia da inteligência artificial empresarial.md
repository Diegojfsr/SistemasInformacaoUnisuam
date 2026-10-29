## Apresentação

A inteligência artificial (IA) representa um dos avanços tecnológicos mais significativos da atualidade, definindo-se pela capacidade de sistemas simularem processos cognitivos humanos, como o raciocínio e o aprendizado. Segundo Russell e Norvig (2013), a IA é o estudo de agentes que recebem percepções do ambiente e executam ações, buscando o sucesso em suas tarefas. Mais do que uma ferramenta, tornou-se um campo multidisciplinar que desenvolve algoritmos capazes de processar volumes massivos de dados para identificar padrões e tomar decisões autônomas.

No contexto corporativo, essa tecnologia transcendeu a teoria para se tornar um diferencial competitivo essencial na transformação digital. As organizações utilizam a IA para otimizar processos operacionais e automatizar tarefas. Isso permite às corporações aumentar a eficiência produtiva, reduzir os custos e tomar as decisões estratégicas baseadas em evidências precisas, convertendo grandes bases de dados em inteligência de mercado aplicada.

Nesta Unidade de Aprendizagem, você vai estudar os conceitos básicos relacionados à IA. Além disso, vai explorar como suas tecnologias podem ser aplicadas nas organizações para auxiliar os processos de tomada de decisão de negócios.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Relacionar a inteligência artificial com negócios organizacionais.
- Identificar as principais características das redes neurais, dos sistemas de lógica fuzzy, dos algoritmos genéticos e da realidade virtual.
- Reconhecer usos práticos das tecnologias de inteligência artificial nas organizações.


## Desafio

A IA transformou a maneira como as organizações se relacionam com seus consumidores. Um dos maiores desafios nos negócios contemporâneos é a retenção de clientes. É significativamente mais caro adquirir um novo consumidor do que manter um atual. Nesse cenário, as empresas utilizam modelos preditivos para identificar padrões de comportamento que sinalizam a intenção de cancelamento, permitindo intervenções preventivas baseadas em dados.

As redes neurais artificiais são especialmente eficazes para essa tarefa. Elas consistem em modelos computacionais inspirados no sistema nervoso central, capazes de aprender a reconhecer correlações complexas e não lineares entre diversas variáveis de entrada para chegar a uma classificação ou previsão precisa.

A partir dessas informações, considere-se parte da situação a seguir.

![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/131646/8900_EXA_DES_V1-2026-02-06T11:27:22-03:00.png)

Diante desse contexto, explique o papel das camadas da rede neural no processamento desses dados e defina uma lógica de classificação para o resultado final gerado pela camada de saída.


####  ✅ Resposta ao desafio:

Como líder de ciência de dados na nossa empresa de SaaS, estruturei a arquitetura da rede neural para processar o risco de churn (cancelamento) considerando as quatro variáveis apresentadas: Frequência de acesso, Tempo de contrato, Engajamento com suporte e Adimplência.
Abaixo, detalho o papel de cada camada da rede neural no fluxo de processamento e a lógica de classificação da saída.

1.Papel das Camadas da Rede Neural no Processamento
Uma rede neural típica para esse tipo de problema tabular é composta por três tipos de camadas: Camada de Entrada, Camada(s) Oculta(s) e Camada de Saída.

A. Camada de Entrada (Input Layer)
Função: Receber os dados brutos e normalizados dos clientes.
Processamento das variáveis:
Frequência de acesso: Entra como a contagem mensal de logins. Valores muito baixos (ex: zero acessos) já pesam como forte indicador de desengajamento.
Tempo de contrato: Medido em meses. Clientes novos costumam ter uma curva de aprendizado e risco de cancelamento diferente de clientes consolidados há anos.
Engajamento com suporte: Quantidade de tickets recentes. Um volume alto pode indicar frustração crônica com o produto, enquanto a ausência total de tickets pode significar que o cliente desistiu de reclamar (uso silencioso rumo ao cancelamento).
Adimplência: Histórico de pagamentos em atraso. Inadimplência recorrente é um sinal crítico de atrito financeiro ou insatisfação com o valor entregue.

B. Camadas Ocultas (Hidden Layers)
Função: Aprender as correlações complexas e não lineares entre as variáveis, conforme mencionado no enunciado. Uma única variável isolada pode não significar nada, mas a combinação delas revela padrões ocultos.
Exemplos de interações não lineares que a camada oculta descobre:
Um cliente com baixo tempo de contrato E baixa frequência de acesso tem um risco de cancelamento exponencialmente maior do que um cliente antigo com a mesma frequência baixa.
Um cliente com muitos tickets de suporte E frequência de acesso alta pode ser um "advogado da marca" engajado tentando resolver problemas para usar mais, enquanto muitos tickets combinados com queda drástica de acesso indicam frustração que leva ao cancelamento.
Processamento: Os neurônios dessas camadas aplicam pesos sinápticos e funções de ativação (como ReLU) para transformar essas combinações de variáveis em representações internas cada vez mais abstratas do risco de churn.


2.Lógica de Classificação da Camada de Saída (Output Layer)
A camada de saída é responsável por transformar o aprendizado das camadas ocultas em uma decisão acionável para a equipe de negócios.

Estrutura: A camada de saída possui um único neurônio utilizando a função de ativação Sigmoid.
Faixa de Valores: A função Sigmoid esmaga qualquer número real recebido para o intervalo entre 0 e 1. Esse valor representa a probabilidade estimada de o cliente cancelar a assinatura nos próximos 30 dias ($P(\text{churn}) \in [0, 1]$).
Definição da Lógica de Decisão (Limiar / Threshold): Para transformar essa probabilidade contínua em uma classificação binária (Cancelar vs. Não Cancelar), definimos um limiar de corte (threshold), tipicamente ajustado em 0.5 (50%), embora possa ser calibrado de acordo com a estratégia comercial da empresa:
P(\text{churn}) < 0.3: Cliente Saudável (Baixo Risco). O padrão de uso, suporte e pagamentos indica estabilidade. Nenhuma ação imediata é necessária além do relacionamento padrão.
0.3 \le P(\text{churn}) < 0.7: Cliente em Zona de Alerta (Médio Risco). O modelo detectou sinais iniciais de desengajamento (ex: queda gradual de acessos ou aumento de tickets). Ação preventiva: O sistema dispara um alerta automatizado para o time de Customer Success (CS) oferecer suporte proativo ou materiais educativos.
P(\text{churn}) \ge 0.7: Cliente em Alto Risco de Cancelamento. A combinação de variáveis aponta uma alta probabilidade de rescisão iminente. Ação preventiva prioritária: O sistema aciona um protocolo de retenção urgente como um contato direto do gerente de contas com ofertas especiais, extensão de testes ou resolução prioritária de tickets pendentes para evitar a perda da receita.

#### Versão simplificada

1.O Papel das Camadas da Rede Neural
Pense na rede neural como uma equipe dividida em três etapas de trabalho:
A. Camada de Entrada (Recepção dos Dados)
É a porta de entrada. Ela apenas recebe as informações do cliente e as ajusta para que o sistema consiga ler:
Frequência de acesso: Quantas vezes o cliente usou o sistema no mês (pouco uso = alerta).
Tempo de contrato: Há quantos meses ele é cliente (novatos se comportam diferente de antigos).
Atendimentos no suporte: Quantos chamados ele abriu (muita reclamação indica insatisfação; nenhuma pode indicar que ele nem usa mais).
Histórico de pagamento: Se ele atrasa ou paga em dia (atrasos constantes indicam risco).

B. Camadas Ocultas (O "Cérebro" do Sistema)
É onde a mágica acontece. Em vez de olhar cada dado sozinho, esta camada junta as peças do quebra-cabeça para encontrar padrões:
Exemplo: Um cliente novo que quase não acessa o sistema tem uma chance muito maior de cancelar do que um cliente antigo que também acessa pouco.
O sistema cruza todas as informações ao mesmo tempo para entender o cenário real do cliente.

2.Camada de Saída (O Resultado Final)
Esta camada pega todo o cruzamento de dados feito anteriormente e entrega uma nota de risco de 0% a 100% indicando a chance de o cliente cancelar nos próximos 30 dias.
A empresa usa essa nota para tomar atitudes práticas:
Risco Baixo (abaixo de 30%): Cliente satisfeito. Não precisa de nenhuma ação especial.
Risco Médio (entre 30% e 70%): Cliente dando sinais de desinteresse. O sistema avisa a equipe de suporte para mandar um e-mail de ajuda ou oferecer um treinamento.
Risco Alto (acima de 70%): Cliente prestes a cancelar. Um gerente entra em contato imediatamente para entender o problema, resolver pendências ou oferecer um desconto para mantê-lo.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 21817985
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 29/10/26 - 19:43
Disciplina: Paradigmas de Programação [TTEC0038] (2026-2-TTEC0038-TRIMESTRAL-EAD0301T)
Tarefa: Desafio
Tentativa: 1 de 1


## Infográfico

A IA consolidou-se como um diferencial estratégico fundamental para as organizações ao simular funções cognitivas humanas. De acordo com Castro (2016), esses sistemas buscam mimetizar a capacidade de aprender e resolver problemas. Eles atuam como o pilar da transformação digital e permitem que empresas criem vantagens competitivas ao otimizar processos complexos.

Para alcançar esses resultados, a IA utiliza um conjunto diversificado de ferramentas com propriedades técnicas específicas. As redes neurais artificiais destacam-se pelo aprendizado profundo e reconhecimento de padrões em dados não estruturados. Já os sistemas de lógica fuzzy permitem que computadores processem conceitos subjetivos e imprecisos, indo além da lógica binária tradicional. Os algoritmos genéticos, por sua vez, aplicam princípios de seleção natural e mutação para encontrar soluções otimizadas em problemas de alta complexidade. Por fim, a realidade virtual proporciona ambientes sintéticos imersivos para simulações e interações em tempo real.

Neste Infográfico, você vai explorar as principais características das redes neurais artificiais, lógica fuzzy, algoritmos genéticos e realidade virtual. Assim, você vai compreender como cada uma dessas ferramentas contribui para o funcionamento e a aplicação prática da inteligência artificial.

![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/131647/8900_EXA_INF_V1-2026-02-06T11:47:33-03:00.png)


## Conteúdo do Livro
A IA emergiu como um dos pilares tecnológicos mais disruptivos da atualidade. Ela fundamenta-se na capacidade de máquinas simularem processos cognitivos humanos, como o raciocínio e a aprendizagem. Conforme destaca Rezende (2005), a IA permite que o conhecimento seja processado de forma a sustentar a resolução de problemas complexos e a geração de inteligência competitiva.

Para as empresas, a integração dessas tecnologias é um diferencial estratégico essencial para a transformação digital. Isso permite a criação de vantagens competitivas por meio de suporte especializado à decisão e otimização de processos. O uso corporativo de ferramentas, como redes neurais artificiais para reconhecimento de tendências, sistemas de lógica fuzzy para tratar incertezas e algoritmos genéticos para a busca de soluções otimizadas, permite que as empresas aumentem a eficiência produtiva e reduzam os custos, adaptando-se com agilidade às demandas do mercado (Russel; Norving, 2013).

No capítulo Tecnologia da inteligência artificial empresarial, base teórica desta Unidade de Aprendizagem, você vai conhecer os conceitos básicos relacionados com a IA e a abrangência da sua área de atuação, com foco no ambiente corporativo. Assim, você vai compreender como as tecnologias de IA se aplicam aos processos organizacionais, suas principais áreas de aplicação, características e benefícios para a tomada de decisão, a automação e a inovação nas empresas.

Boa leitura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/784d3213-04d0-4e5a-af1b-0f93d18169fc/bf3171f9-b984-4646-95e7-be2c9b677d76.jpg)


## Dica do Professor

O artigo de Alan Turing, intitulado Computing Machinery and Intelligence (1950), juntamente com o seu subsequente Teste de Turing, estabeleceram o objetivo e a visão fundamentais da inteligência artificial (IA). Esse marco histórico não apenas propôs um desafio técnico, mas também definiu o horizonte filosófico da computação. Turing questionou se as máquinas seriam capazes de exibir um comportamento inteligente indistinguível do humano.

Em sua essência técnica, a IA visa responder afirmativamente à pergunta original de Turing. Ela representa o esforço contínuo e metódico para replicar ou simular a inteligência humana em máquinas. Dessa forma, permite que sistemas computacionais executem tarefas complexas de raciocínio, aprendizagem e tomada de decisão que, anteriormente, eram exclusivas aos seres biológicos.

Nesta Dica do Professor, você vai explorar conceitos básicos relacionados à IA. Vai entender de que forma essa tecnologia é aplicada atualmente, principalmente em organizações.


## Exercícios

#### Questão 1
A aceleração da transformação digital nas indústrias modernas fomenta um debate crítico sobre a substituição de funções humanas por sistemas autônomos e as reais capacidades de decisão dessas tecnologias em níveis organizacional.
Avalie as asserções a seguir e a relação proposta entre elas. 
I. O uso de tecnologias de inteligência artificial (IA) acaba com a maioria dos empregos das pessoas em fábricas ou unidades produtoras que utilizam robótica e sistemas especialistas.
PORQUE
II. A partir do momento em que são instalados no ambiente corporativo, os sistemas baseados em IA passam a ser responsáveis por toda e qualquer decisão tomada em nível estratégico.
A respeito dessas asserções, assinale a alternativa correta.
Selecione a resposta:



#### Questão 2
O objetivo central da inteligência artificial (IA) é imitar capacidades e comportamentos humanos em arquiteturas computacionais, organizando-se em três pilares fundamentais: a ciência cognitiva, as interfaces naturais e a robótica. Cada um desses domínios fornece ferramentas especializadas que permitem aos sistemas de informação processar dados, interagir com usuários e executar tarefas motoras, traduzindo a complexidade do raciocínio e da percepção humana em execuções técnicas eficientes e integradas.
Analise os itens a seguir e assinale a alternativa que apresenta somente exemplos de aplicações da ciência cognitiva. 
Selecione a resposta:




#### Questão 3
A evolução da IA impulsionou o desenvolvimento de sistemas de aprendizado de máquina e aprendizado profundo especializados no reconhecimento de padrões complexos. Esses algoritmos estruturam-se em camadas de processamento (entrada, ocultas e saída), ompostas por nós que funcionam de maneira análoga a interruptores biológicos, ativando-se conforme a alimentação dos dados. Nesse fluxo sequencial, a saída de cada camada torna-se instantaneamente a entrada para a camada subsequente, permitindo que a informação seja refinada progressivamente desde a recepção dos dados iniciais até o resultado final. Seus algoritmos também dependem de dados de treinamento para aprender e melhorar sua precisão ao longo do tempo.
Qual tecnologia IA está sendo mencionada aqui?​​​​​​​
Selecione a resposta:





#### Questão 4
A inteligência artificial (IA) consolidou-se como um pilar de transformação digital nas organizações contemporâneas, simulando processos cognitivos como o raciocínio e a aprendizagem para otimizar a tomada de decisão estratégica. No ambiente corporativo, a aplicação dessas ferramentas abrange diversos domínios funcionais.
Sobre a aplicação de tecnologias de IA no ambiente organizacional, analise as afirmações a seguir.
I. A lógica fuzzy é aplicada em sistemas de automação para lidar com variáveis imprecisas e incertas, permitindo que processos industriais tomem decisões baseadas em graus de pertinência, o que simula de forma mais próxima o raciocínio humano em cenários de incerteza.
II. Os algoritmos genéticos são utilizados pelas empresas para resolver desafios complexos de otimização, como gerenciamento de estoque de suprimentos, operando por meio de processos de seleção, cruzamento e mutação para identificar a solução mais eficiente entre milhares de possibilidades.
III. A realidade virtual, quando integrada a sistemas inteligentes, é empregada em treinamentos corporativos imersivos, permitindo simulações de voos para treinamento de pilotos, minimizando riscos operacionais e custos.
É correto o que se afirma em:
Selecione a resposta:




#### Questão 5
A inteligência artificial (IA) atua como um pilar de inovação nas organizações ao buscar replicar ou simular a inteligência humana em máquinas. Entre suas áreas de aplicação, destaca-se a de interfaces naturais, em que a realidade virtual apresenta-se como uma de suas tecnologias. 
Sobre a aplicação e as características da tecnologia de realidade virtual nas empresas, analise as afirmações a seguir.
I. A realidade virtual é definida como uma interface avançada que permite ao usuário navegar e interagir em tempo real, sendo caracterizada primordialmente pela imersão, que é a percepção do usuário de estar fisicamente presente em um mundo não físico.
II. Por ser uma tecnologia de interface voltada exclusivamente para o entretenimento e jogos eletrônicos, a realidade virtual ainda não tem aplicações práticas validadas em setores como manutenção técnica automotiva ou pesquisas de mercado no varejo.
III. No ambiente corporativo, casos de sucesso incluem a empresa Mitchell, que utiliza óculos de realidade virtual para reparo de carros sem manuais impressos, e a Kellogg's, que utilizou a realidade virtual com rastreamento ocular para reduzir o tempo e custo de pesquisas de mercado.
É correto o que se afirma em:
Selecione a resposta:





## Na prática
As tecnologias relacionadas à inteligência artificial (IA) são um diferencial estratégico essencial para as organizações modernas, uma vez que permitem a criação de vantagens competitivas reais. Ao simular funções associadas à inteligência humana, como raciocínio, aprendizagem e solução de problemas, a IA oferece um suporte especializado indispensável para a tomada de decisão. Esse suporte contribui para a otimização de diversos processos organizacionais.

Uma das tecnologias relacionadas à IA é a lógica fuzzy. De acordo com Simões e Shaw (2007), ela também é conhecida por lógica nebulosa, ou por teoria de possibilidades em alguns casos, e tem uma característica especial: a capacidade de representar uma forma inovadora de manuseio de informações imprecisas, de modo distinto da teoria das probabilidades. Nesse contexto, a lógica fuzzy permite traduzir expressões verbais vagas, imprecisas e qualitativas, frequentes na comunicação humana, em valores numéricos, possibilitando a conversão da experiência humana em uma forma compreensível e processável pelos computadores.

Neste Na Prática, você vai acompanhar o caso de um engenheiro de automação que implementou um controlador baseado em lógica fuzzy. A partir dessa implementação, ele transformou a eficiência energética e a segurança operacional de uma grande indústria.

  
![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/131651/8900_EXA_NAP_V1-2026-02-06T13:11:27-03:00.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Redes neurais — principais arquiteturas de redes neurais
As arquiteturas de redes neurais definem a organização e o fluxo de informações entre camadas de neurônios artificiais, sendo o projeto estrutural que determina a capacidade do modelo de extrair características e aprender representações complexas a partir de dados brutos. Assista a este vídeo para conhecer as principais arquiteturas das redes neurais.
[Mais](https://www.youtube.com/embed/eicACKayXbE?si=u-xb5i4U_0bV1MwG)


Substituição do trabalho repetitivo por máquinas "inteligentes"
A inteligência artificial (IA) tem redefinido o mercado de trabalho ao delegar o processamento de rotinas operacionais a sistemas inteligentes, tornando a eficiência produtiva um padrão. Leia o Capítulo 3 desta obra para explorar uma discussão sobre como o trabalho repetitivo tem sido substituído por máquinas inteligentes.
[Mais](https://unisuamgrad.grupoa.education/plataforma/lti-launch/?type=library&id=69292406&tokenId=950cc09a-68bb-4c57-ad1f-9e7961062194)


Realidade virtual no teletrabalho colaborativo: aplicações, oportunidades e desafios — uma revisão da literatura
A realidade virtual potencializa o teletrabalho ao romper a barreira das telas bidimensionais. Ela possibilita criar ambientes imersivos em que equipes geograficamente dispersas podem colaborar em tempo real, como se estivessem no mesmo espaço físico. Neste artigo, confira uma revisão da literatura sobre a aplicação de tecnologias de realidade virtual no contexto do teletrabalho colaborativo.
[Mais]()


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

ALSHARE, K. A. et al. Development and determinants of end-user intention: usage of
expert systems. Journal of Systems and Information Technology, v. 21, n. 2, p. 166-
185, 2019.

CASTRO, L. N. Introdução à inteligência computacional: fundamentos, técnicas e
aplicações. Rio de Janeiro: LTC, 2016.

DIAGRAMA simplificado de uma rede neural. Wikipédia, 2021. Disponível em:
https://pt.wikipedia.org/wiki/Rede_neural_artificial#/media/Ficheiro:Neural_network.svg.
Acesso em: 5 fev. 2026.

FGV ONLINE. Regras de negócio. Biblioteca online. Disponível em: http://ead2.fgv.br/ls5/centro_rec/pag/textos/regras_negocio_1.htm. Acesso em: 25 nov.2020.

GLOVER, E. What is artificial intelligence (IA)? Built In, 12 dez. 2025. Disponível em:
https://builtin.com/artificial-intelligence. Acesso em: 5 fev. 2026.

MENDES, R. D. Inteligência artificial: sistemas especialistas no gerenciamento da
informação. Ciência da Informação, v. 26, n. 1, 1997.

O’BRIEN, J. A.; MARAKAS, G. M. Administração de sistemas de informação. 15. ed.
Porto Alegre: McGraw-Hill, 2012.

REZENDE, S. O. Sistemas inteligentes: fundamentos e aplicações. Barueri: Manole,
2005.

RUSSELL, S. J.; NORVIG, P. Inteligência artificial: uma abordagem moderna. 3. ed. Rio
de Janeiro: Elsevier, 2013.
SHAW, S. Warm fuzzy logic member function. Wikipédia, 2024. Disponível em:
https://commons.wikimedia.org/wiki/File:Warm_fuzzy_logic_member_function.gif. Acesso
em: 3 fev. 2026.

SIMÕES, M. G.; SHAW, I. S. Controle e modelagem fuzzy. 2. ed. São Paulo: Blucher,
2007.

SIMPLE neural network. Wikipédia, 2025. Disponível em: https://commons.wikimedia.org/wiki/File:Neural_network_example.svg. Acesso em: 3 fev.2026.

TURING, A. M. Computing machinery and intelligence. Mind, v. 59, n. 236, p. 433-460,
1950.

YE, L. R.; JOHNSON, P. E. The impact of explanation facilities on user acceptance of
expert systems advice. MIS Quarterly, v. 19, n. 2, p. 57-72, 1995.

Bancos gratuitos de imagens e Shutterstock.
SAGAH, 2026.
