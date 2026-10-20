## Apresentação

Atualmente, há uma grande preocupação por parte das organizações em relação a problemas e incidentes causados por falhas de segurança da informação. Qualquer descuido pode gerar prejuízos enormes, incluindo a perda de dados importantes, danos financeiros e impactos negativos na reputação e na imagem da empresa.

A identificação e a solução de problemas reais de segurança da informação são essenciais para mitigar esses riscos. Além disso, o fator humano é uma das principais causas de ataques, destacando a importância de práticas e políticas adequadas para proteger a organização.

Nesta Unidade de Aprendizagem, você vai explorar diversos aspectos importantes para a segurança da informação. Vai conhecer metodologias para identificar e resolver problemas reais de segurança que podem afetar sistemas e dados corporativos. Vai ver o impacto do fator humano como uma das principais causas de ataques, ressaltando a importância de treinamento e conscientização dos usuários. E vai ver os procedimentos de testes de segurança essenciais para garantir a integridade e a proteção das informações contra possíveis ameaças.  

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Identificar e solucionar problemas reais de segurança da informação.
- Reconhecer o fator humano como causa de ataques.
- Definir os procedimentos de testes de segurança da informação.


## Desafio

É fundamental que as organizações determinem com o máximo rigor sua estrutura de segurança da informação para criar uma política específica, identificar vulnerabilidades, definir controles e elaborar estratégias de defesa. Feito isso, é preciso pensar em formas de testes para colocar esses aspectos em prática antes que um indivíduo mal-intencionado efetue uma tentativa de invasão. Dessa forma, a organização pode assegurar que sua estratégia de segurança da informação é eficiente.

Analise o caso descrito a seguir:


![](https://statics-marketplace.plataforma.grupoa.education/sagah/2249c254-ab8f-4b5e-ad0a-8fda6fc65c1c/b492d36f-13b3-4468-8745-84c3b85fe4fb.png)

Diante desse caso, suas tarefas são as seguintes:

**a)** Indicar o método de teste de segurança mais adequado para avaliar o novo sistema considerando as características descritas.

**b)** Definir as etapas para a execução desses testes, identificando potenciais falhas, e propor soluções para corrigir as vulnerabilidades encontradas. Considere também a necessidade de envolver diferentes membros da equipe em diversas fases do processo de teste para garantir uma cobertura completa das possíveis ameaças.

#### Padrão de resposta esperado
a) O método de teste de segurança mais adequado para avaliar o novo sistema é a injeção de código. Esse método é particularmente eficaz para identificar vulnerabilidades em sistemas em que os usuários inserem dados, pois testa como o sistema reage a entradas inesperadas ou maliciosas.

b) Primeiro, reúne-se a equipe para planejar e desenvolver scripts de injeção de código simulando ataques como SQL Injection e XSS. Depois, executam-se esses scripts nas várias telas de entrada de dados do sistema, monitorando a resposta do sistema e documentando as vulnerabilidades encontradas. Em seguida, trabalha-se com os desenvolvedores para corrigir essas falhas, reforçando a validação e sanitização dos dados inseridos pelos usuários. Posteriormente, repetem-se os testes para garantir que as correções foram eficazes.

####  ✅ Resposta ao desafio:

a) Método de teste de segurança mais adequado
O método de teste de segurança mais adequado para avaliar o novo sistema é o teste de injeção de código, especialmente ataques como SQL Injection e Cross-Site Scripting (XSS). Esse método é indicado porque o sistema possui diversas telas de entrada de dados preenchidas pelos usuários, aumentando o risco de exploração de vulnerabilidades relacionadas ao tratamento inadequado das informações inseridas.

b) Etapas para execução dos testes, identificação de falhas e propostas de correção
1.Planejamento dos testes: Inicialmente, a equipe de segurança deve mapear todas as telas e campos de entrada de dados do sistema, identificando pontos críticos como cadastro de clientes, registro de pedidos, controle de vendas e acompanhamento de entregas. Nessa fase, os especialistas em segurança e os desenvolvedores devem definir cenários de teste e elaborar scripts que simulem ataques de SQL Injection e XSS.

2.Execução dos testes: Os scripts criados são executados nas diferentes interfaces do sistema, inserindo dados maliciosos nos campos de entrada para verificar como a aplicação reage. Durante a execução, a equipe monitora logs, mensagens de erro, comportamento do banco de dados e possíveis falhas de validação.
Exemplos de vulnerabilidades que podem ser identificadas:
Ausência de validação adequada dos dados inseridos pelos usuários.
Possibilidade de execução de comandos SQL indevidos.
Exposição de informações sensíveis por meio de mensagens de erro.
Execução de scripts maliciosos no navegador dos usuários.
Falhas de autenticação e autorização em determinadas funcionalidades.

3.Documentação das vulnerabilidades: Todas as falhas encontradas devem ser registradas, classificadas de acordo com seu nível de risco e documentadas detalhadamente, incluindo:
Descrição da vulnerabilidade.
Local onde foi encontrada.
Impacto potencial para a organização.
Evidências obtidas durante os testes.
Recomendações para correção.

4.Correção das vulnerabilidades: Em conjunto com a equipe de desenvolvimento, devem ser implementadas medidas como:
Validação de entrada de dados no cliente e no servidor.
Sanitização e filtragem dos dados fornecidos pelos usuários.
Utilização de consultas parametrizadas (prepared statements) para evitar SQL Injection.
Codificação e escape de caracteres especiais para prevenir XSS.
Implementação de controles de autenticação e autorização mais robustos.
Tratamento adequado de mensagens de erro para evitar exposição de informações sensíveis.

5.Reteste e validação: Após a correção das falhas, os testes devem ser executados novamente para verificar se as vulnerabilidades foram eliminadas e se não foram introduzidos novos problemas no sistema.

6.Participação da equipe: Para garantir uma cobertura completa das ameaças, diferentes profissionais devem participar do processo:
Analistas de segurança: planejamento e execução dos testes.
Desenvolvedores: correção das vulnerabilidades identificadas.
Administradores de banco de dados: análise dos impactos relacionados ao armazenamento das informações.
Equipe de infraestrutura: verificação de configurações de servidores e redes.
Gestores do projeto: acompanhamento dos riscos e validação dos resultados.

Dessa forma, a organização consegue identificar e corrigir vulnerabilidades antes da implantação do sistema, aumentando significativamente sua segurança e reduzindo os riscos de ataques cibernéticos.

## Infográfico

Pessoas representam o fator essencial para que a segurança da informação de uma organização seja bem-sucedida. A maioria está envolvida de alguma maneira com tecnologia da informação e dispositivos de informática, seja para seu lazer, profissão ou finanças. Esse envolvimento constante faz com que a segurança dependa diretamente do comportamento dos usuários.

No entanto, se a tecnologia for utilizada de forma incorreta, as informações podem ficar expostas a ataques. Os indivíduos mal-intencionados muitas vezes exploram falhas humanas para obter acesso a dados sensíveis. Por isso, os usuários precisam estar cientes dos riscos e adotar práticas seguras no uso das tecnologias.

Neste Infográfico, você vai ver como o fator humano pode ser a causa de ataques. Vai compreender os motivos para dar importância às pessoas na segurança da informação e entender a necessidade de conscientização para prevenir ameaças e proteger dados.


![](https://statics-marketplace.plataforma.grupoa.education/sagah/68192c45-ae9a-442f-ad8c-414287003a27/06e266db-1db2-493f-a28f-e065c062f64c.png)

​​​​​​​​​​​​​​
## Conteúdo do Livro

A área de segurança da informação das organizações tem o propósito de preservar as informações da empresa, evitando ou minimizando a possibilidade de ataques bem-sucedidos. Entretanto, é sabido que a criatividade e o empenho de indivíduos mal-intencionados caminham à frente das tecnologias e ferramentas disponíveis para a defesa, o que impede que as chances de ataques sejam eliminadas totalmente.  

Por mais que a organização tenha tecnologia disponível para a segurança, são pessoas que utilizam e desenvolvem os sistemas, e elas são suscetíveis a erros, mal-entendidos e falhas, que podem trazer grandes prejuízos. Por isso, é importante desenvolver uma rigorosa política de segurança da informação e, principalmente, conscientizar e envolver seus usuários para que as chances de sucesso aumentem.  

No capítulo Identificação e solução de problemas reais, base teórica desta Unidade de Aprendizagem, você vai explorar a identificação e a resolução de desafios práticos na segurança da informação. Além disso, o fator humano em incidentes de segurança será abordado, destacando como ações individuais podem comprometer a integridade dos sistemas. Além disso, os métodos e procedimentos para testar a segurança das informações serão examinados, tendo em vista proporcionar uma visão abrangente sobre como proteger efetivamente os dados em um ambiente organizacional.  

Boa leitura.


## Dica do Professor

A execução de testes, mesmo não eliminando os riscos, torna possível antever problemas reais e gerenciar as vulnerabilidades da empresa. Esses testes são fundamentais para identificar pontos fracos e tomar medidas preventivas antes que uma ameaça se concretize, demonstrando a preocupação com a segurança das informações.

A prática contínua de testar e avaliar a segurança da informação ajuda a manter a infraestrutura da empresa protegida contra possíveis invasões e ataques. Além disso, esses testes fornecem insights sobre como aprimorar as políticas e os procedimentos de segurança, garantindo que a empresa esteja sempre um passo à frente dos invasores.

Nesta Dica do Professor, você vai ver os procedimentos de testes de segurança da informação e aprender técnicas e métodos eficazes para proteger os dados da sua organização, garantindo a integridade e a confidencialidade das informações.


## Exercícios

#### Questão 1
A segurança da informação envolve proteger dados e serviços contra diversas ameaças que podem comprometer a integridade, a confidencialidade e a disponibilidade dos sistemas.
Assinale a alternativa que indica corretamente um exemplo de um problema real de segurança da informação.
Selecione a resposta:
A.Disponibilidade de serviços.
B.Roubo de informações.
C.Integridade de informações.
D.Confidencialidade.
E.Restrição de acesso.

✅ A alternativa correta é: B

#### Questão 2
Para solucionar os problemas mais recorrentes relativos à segurança da informação e até mesmo conseguir evitá-los, é primordial adotar medidas preventivas.
Assinale a alternativa que indica corretamente medidas que podem evitar problemas de segurança da informação.
Selecione a resposta:
A.Garantir o sigilo das informações e ter controles de acesso bem-definidos.
B.Dar acesso irrestrito a todos os usuários.
C.Jamais atualizar as ferramentas de segurança para assegurar que vírus não entrem na rede.
D.Envolver somente a gestão da empresa na política de segurança da informação.
E.Liberar acesso a qualquer tipo de site e permitir que usuários instalem programas nos computadores.

✅ A alternativa correta é: A


#### Questão 3
A segurança da informação depende de diversos fatores, incluindo a interação humana com a tecnologia. A importância de manter os profissionais sempre atualizados e treinados está diretamente ligada ao sucesso da segurança dos dados e sistemas.
Por que o fator humano é tão importante para a segurança da informação? Assinale a alternativa correta.
Selecione a resposta:
A.Porque as pessoas costumam não errar quando lidam com tecnologia da informação.
B.Porque as pessoas precisam de treinamento somente uma vez e já se garante que vão fazer tudo corretamente.
C.Porque as pessoas não precisam conhecer a política de segurança da informação.
D.Porque as pessoas somente utilizam, mas não desenvolvem os sistemas de informação.
E.Porque são as pessoas que comandam as organizações e utilizam os sistemas, portanto são elas que garantem o sucesso da segurança da informação.

✅ A alternativa correta é: E

#### Questão 4
O invasor utiliza a persuasão, visando tirar vantagem da ingenuidade, da confiança e da falta de habilidade do usuário, para obter informações que podem ser utilizadas para acessos não autorizados a informações ou a computadores.
Com relação a esse assunto, assinale a alternativa que indica o que é engenharia social.
Selecione a resposta:
A.É a conscientização das empresas a respeito de questões ambientais e sociais.
B.É uma política educacional para conscientizar usuários sobre segurança.
C.É um método de defesa contra ataques de segurança da informação.
D.É um método de ataque à segurança da informação.
E.É uma área da engenharia civil.

✅ A alternativa correta é: D

#### Questão 5
Os métodos de testes de segurança da informação auxiliam na identificação e correção de vulnerabilidades. Esses métodos ajudam a garantir a integridade e a proteção dos sistemas de informação.
Quais são os métodos de testes de segurança da informação? Assinale a alternativa correta.
Selecione a resposta:
A.Ação bruta e ataques de vírus.
B.Injeção de código e força bruta.
C.Injeção de força e análise de acessos.
D.Conscientização de usuários e política de segurança.
E.Envolvimento da alta gestão e sondagem e mapeamento.

✅ A alternativa correta é: B


## Na prática

Apesar de todos os esforços empreendidos na segurança da informação das organizações, o profissional que trabalha na área tem o entendimento de que é impossível eliminar totalmente as vulnerabilidades, as ameaças e as possibilidades de concretização dos ataques.

São incontáveis os casos de ataques bem-sucedidos feitos diariamente contra organizações de todos os setores e portes. Esse tipo de situação transmite, para todas as partes envolvidas com o negócio, um sentimento de insegurança e descrédito, algo como se a empresa não se preocupasse com as informações que mantém em seu poder.

Neste Na Prática, você vai conhecer alguns casos famosos de ataques bem-sucedidos e o que foi feito para solucioná-los.


![](https://statics-marketplace.plataforma.grupoa.education/sagah/c41962f1-0df2-4cec-86c8-c90aa15cc588/bcb6256f-7e41-4ce3-9208-a0665d30bfc7.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Engenharia social, a arte do engano
Observe, neste vídeo, o fator humano na segurança da informação e a engenharia social e veja como ataques de manipulação psicológica podem comprometer a segurança das informações.
[Mais](https://www.youtube.com/embed/fM76uQNpjvk?si=QX3G1WuRcXUFZnOQ)

Análise de vulnerabilidade: o guia definitivo sobre o assunto
Leia este artigo, que aborda problemas reais de segurança da informação. Nele, explora-se detalhadamente o processo de análise de vulnerabilidades, destacando como identificar e corrigir falhas na infraestrutura de TI. É um guia definitivo que oferece insights sobre a importância da análise de vulnerabilidade para proteger os dados e garantir a segurança cibernética nas organizações.
[Mais](https://tivit.com/analise-de-vulnerabilidade-o-guia-definitivo-sobre-o-assunto/)

Conscientização em segurança da informação
Veja, neste vídeo, a importância da conscientização dos usuários com relação à segurança da informação e a importância da promoção de uma cultura de segurança da informação. Nele são destacadas estratégias que visam reduzir vulnerabilidades humanas.
[Mais](https://www.youtube.com/embed/QqKAX4k8vaA?si=bFzFWY3Lhzciyk1r)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

ALBUQUERQUE, R.; RIBEIRO, B. Segurança no desenvolvimento de software. Rio de
Janeiro: Campus, 2002.

FARIA, R. G. L. Fundamentos de segurança da informação. Belo Horizonte: Ânima, 2016.

FONTES, E. L. G. Segurança da informação: o usuário faz a diferença. São Paulo: Saraiva,
2006.

Bancos gratuitos de imagens e Shutterstock.
SAGAH, 2024.

