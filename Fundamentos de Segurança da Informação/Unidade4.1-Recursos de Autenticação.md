## Apresentação
Adotar ou ser certificado pelas normas ISO representa um marco significativo para qualquer organização, elevando seu prestígio tanto internamente quanto externamente. As normas ISO abrangem uma ampla gama de áreas, incluindo aspectos econômicos e técnicos, com especial foco em segurança da informação. Elas fornecem um conjunto de diretrizes que as organizações devem seguir para gerenciar riscos de maneira eficaz, garantindo, assim, uma abordagem robusta à segurança de dados e informações, crucial em um ambiente de negócios cada vez mais digital e interconectado.

Implementar essas normas não apenas aumenta a confiabilidade das operações empresariais, mas também fortalece a confiança dos stakeholders em relação à capacidade da empresa de proteger informações vitais contra ameaças e vulnerabilidades. A adesão a essas diretrizes demonstra um compromisso com a excelência operacional e a governança corporativa, aspectos cada vez mais valorizados em mercados globais competitivos.

Nesta Unidade de Aprendizagem, você vai conhecer os detalhes das normas ISO 27000, 27005, 31000 e 22301, explorando como cada uma contribui especificamente para a construção de uma infraestrutura de segurança da informação sólida e adaptada às necessidades contemporâneas das organizações. Você vai entender como essas normas podem ser aplicadas para melhorar continuamente os processos de segurança e gestão de risco, essenciais para a proteção de ativos de informação.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Compreender o que são recursos de autenticação.
- Identificar o processo de controle de acesso.
- Reconhecer os principais recursos de autenticação.


## Desafio

O processo de controle de acesso é formado pela união de métodos ou serviços de identificação, autenticação, autorização e auditoria de usuários para entrada em um sistema. O objetivo é permitir ou negar a utilização de um objeto – que pode ser uma funcionalidade, um arquivo ou um sistema – por um sujeito – que pode ser um usuário, um processo ou até mesmo outro sistema.

A partir dessas informações, considere o seguinte cenário:

Você trabalha na área de desenvolvimento de sistemas de uma grande empresa de logística. Você atua em um sistema que libera pequenos valores para funcionários que estão trabalhando remotamente, a fim de que eles possam suprir despesas de combustível, alimentação, materiais de escritório e outras que se façam necessárias para o desempenho de suas atividades enquanto ausentes.

Você, como desenvolvedor, sabendo que foram definidos perfis de administrador, chefe de área e funcionário para utilização do sistema, precisa definir qual será o melhor tipo de controle de acesso a ser implementado para autenticação de usuários nesse sistema entre os tipos discricionário e obrigatório, explicando a sua decisão.

#### Padrão de resposta esperado

O melhor controle para esse sistema é o discricionário, para que o próprio gestor do sistema decida quais usuários terão acesso ou não a cada recurso do sistema.

Como a premissa do modelo discricionário é a de que todo recurso deve ter um proprietário, todos os usuários deverão pertencer ao perfil administrador, chefe de área ou funcionário.

● O perfil administrador pode ter autorização para popular todas as tabelas básicas, como cidades, funcionários, estoque, entre outras.
● O perfil chefe de área pode ter autorização para acessar recursos que liberam valores para funcionários.
● O perfil funcionário pode ser autorizado a pedir valores para seu chefe de área.


####  ✅ Resposta ao desafio:

O tipo de controle de acesso mais adequado para esse sistema é o controle de acesso discricionário (DAC - Discretionary Access Control).

A escolha pelo modelo discricionário se justifica porque o sistema possui perfis de usuários bem definidos (administrador, chefe de área e funcionário) e exige que as permissões sejam atribuídas de acordo com as responsabilidades de cada função. Nesse modelo, o responsável pela administração do sistema pode determinar quais usuários ou grupos terão acesso a cada recurso disponível.

Além disso, no controle discricionário, cada recurso possui um proprietário ou responsável pela sua administração, permitindo maior flexibilidade na concessão e revogação de permissões conforme as necessidades da empresa.

Dessa forma, os perfis podem ser configurados da seguinte maneira:

Administrador: possui acesso total ao sistema, podendo cadastrar e manter tabelas básicas, como cidades, funcionários, centros de custo, estoque e demais informações necessárias ao funcionamento da aplicação.
Chefe de área: possui autorização para analisar, aprovar ou rejeitar solicitações de valores realizadas pelos funcionários de sua equipe.
Funcionário: possui permissão para solicitar valores destinados a despesas relacionadas ao trabalho remoto, como combustível, alimentação, materiais de escritório e outras necessidades aprovadas pela empresa.

Portanto, o controle de acesso discricionário é a melhor opção para esse cenário, pois oferece a flexibilidade necessária para que os gestores e administradores definam as permissões de acesso de acordo com as funções e responsabilidades de cada usuário dentro do sistema.


## Infográfico
A série de normas ISO 27000 desempenha um papel crítico no estabelecimento de sistemas de gestão de segurança da informação (SGSI), abrangendo a proteção de dados em diversas formas. Essas normas são projetadas para garantir que as práticas de segurança da informação de uma organização estejam alinhadas com os princípios de confidencialidade, autenticidade, disponibilidade e integridade, fundamentais para a segurança de informações digitais e não digitais.

As diretrizes fornecidas pelas normas ISO 27000 e 27005 ajudam as organizações a avaliar riscos, gerenciar vulnerabilidades e implementar medidas de proteção de forma estruturada e consistente, melhorando a segurança geral dos dados. A ISO 27000 estabelece os requisitos para um SGSI, fornecendo um modelo para implementação, operação, monitoramento, revisão, manutenção e melhoria contínua da gestão de segurança da informação. Já a ISO 27005 é focada na gestão de riscos, oferecendo orientações detalhadas sobre identificação, avaliação e tratamento de riscos. Juntas, essas normas permitem uma abordagem sistemática para proteger informações críticas, garantindo que a segurança dos dados seja mantida em todo o ciclo de vida da informação.

Neste Infográfico, você vai entender como as normas são aplicadas para estabelecer e manter um SGSI eficaz, explorando as funções específicas e as inter-relações dessas normas dentro do SGSI. Dessa forma, você vai compreender como elas podem ser utilizadas para fortalecer a segurança da informação em diversos contextos organizacionais.

![](https://statics-marketplace.plataforma.grupoa.education/sagah/3dfbbbf5-3e9b-4cdc-8779-b7d5a4096690/c743b68c-4fe5-4707-954c-2c50a91893ce.png)

​​​​​​​
## Conteúdo do Livro
A segurança da informação envolve a utilização de uma série de ferramentas, técnicas e processos na tentativa de diminuir a incidência ou mitigar o efeito negativo de ataques maliciosos. Isso se deve ao fato de que o profissional de segurança da informação deve estar ciente de que é quase impossível eliminar totalmente as invasões de indivíduos mal-intencionados.

O controle de acesso é utilizado na segurança da informação para permitir ou negar o acesso dos sujeitos envolvidos com os sistemas a objetos específicos que eles estejam autorizados a acessar.
O processo de controle de acesso é formado por etapas menores de identificação, autenticação, autorização e auditoria.

No capítulo Recursos de autenticação, base teórica desta Unidade de Aprendizagem, você vai compreender o conceito de recursos de autenticação, o processo de controle de acesso e, ainda, os principais tipos de recursos de autenticação.

Boa leitura.


## Dica do Professor
Todas as organizações, sejam elas privadas ou públicas, independentemente de seu tamanho ou tipo, enfrentam uma variedade de riscos que podem impactar desde a sua reputação até a segurança física e cibernética. É essencial, portanto, que essas organizações implementem uma gestão de riscos eficaz, organizando e planejando recursos humanos e materiais para minimizar os efeitos adversos.

Esse processo envolve o uso de técnicas e ferramentas específicas para mitigar riscos que podem afetar pessoas, projetos, processos e o ambiente organizacional interno e externo. Uma gestão de riscos bem estruturada permite às organizações identificar, avaliar e tratar potenciais ameaças de maneira proativa, garantindo, assim, a continuidade das operações e a proteção dos ativos da empresa.

Nesta Dica do Professor, você vai estudar a norma ISO 31000, que fornece as diretrizes essenciais para a gestão de risco. Você vai ver que esse padrão ajuda as organizações a estabelecerem uma estrutura que assegura que todos os tipos de risco sejam identificados, analisados e devidamente tratados. Você ainda vai descobrir como aplicar essas diretrizes para fortalecer a resiliência organizacional e garantir uma abordagem sistemática para lidar com incertezas.


## Exercícios

#### Questão 1
A autenticação é um processo crítico na segurança da informação, pois verifica a identidade de um usuário antes de permitir o acesso aos sistemas.
Quais são os métodos comuns de autenticação utilizados para verificar a identidade de um usuário?
Selecione a resposta:
A.Senhas, reconhecimento facial e autorização.
B.Senhas, impressões digitais e cartões inteligentes.
C.Impressões digitais, leitura de íris e auditoria.
D.Cartões inteligentes, tokens e autorização.
E.Reconhecimento facial, leitura de íris e auditoria.

✅ A alternativa correta é: B

#### Questão 2
A autenticação multifator (MFA) é uma abordagem de segurança que utiliza vários métodos de autenticação para verificar a identidade de um usuário.
O que é uma autenticação multifator?
Selecione a resposta:
A.É o uso de múltiplos métodos de autenticação para verificar a identidade de um usuário.
B.É o uso de vários sistemas operacionais.
C.É o uso de várias senhas para um único login.
D.É o uso de um único método de autenticação para vários usuários.
E.É o uso de métodos de autenticação baseados em software.

✅ A alternativa correta é: A


#### Questão 3
A autorização é um componente essencial em um sistema de segurança da informação, pois determina quais recursos um usuário autenticado pode acessar.
Qual é o papel do processo de autorização em um sistema de segurança da informação?
Selecione a resposta:
A.Verificar a identidade do usuário.
B.Monitorar e registrar atividades dos usuários.
C.Manter a integridade dos dados armazenados.
D.Implementar políticas de segurança em toda a organização.
E.Conceder ou negar acesso aos recursos com base nas permissões do usuário.

✅ A alternativa correta é: E


### Questão 4
A MFA é uma abordagem que combina diferentes tipos de fatores para verificar a identidade de um usuário, proporcionando uma camada extra de segurança além do uso de apenas um fator.
Quais são os três fatores usados em MFA?
Selecione a resposta:
A.O que o usuário sabe, o que o usuário possui e onde o usuário está.
B.O que o usuário possui, o que o usuário vê e onde o usuário está.
C.O que o usuário é, o que o usuário escreve e o que o usuário vê.
D.O que o usuário sabe, o que o usuário possui e o que o usuário é.
E.Onde o usuário está, o que o usuário possui e o que o usuário ouve.

✅ A alternativa correta é: D


#### Questão 5
A auditoria em segurança da informação é um processo que envolve monitorar, registrar e revisar atividades do sistema para garantir que todas as operações estejam em conformidade com as políticas de segurança.
Quais são os principais componentes do processo de auditoria em segurança da informação?
Selecione a resposta:
A.Identificação, autenticação e monitoramento de usuários.
B.Autorização, controle de acesso e verificação de dados.
C.Monitoramento, registro e revisão de atividades do sistema.
D.Verificação de identidade, concessão de acesso e implementação de políticas.
E.Controle de acesso, revisão de permissões e atualização de credenciais.

✅ A alternativa correta é: C

## Na prática
Em um ambiente corporativo cada vez mais volátil, a norma ISO 31000 emerge como um farol para navegar as águas turbulentas da gestão de riscos. Essa norma é fundamental para empresas que desejam se manter resilientes diante das incertezas e dos desafios contemporâneos. Ao estabelecer um conjunto de padrões bem definidos, a ISO 31000 orienta as organizações na identificação de possíveis ameaças, permitindo que antecipem problemas e se preparem adequadamente para enfrentá-los.

Além disso, a ISO 31000 ajuda não apenas na identificação de riscos, mas também na avaliação e na mitigação desses riscos, proporcionando uma metodologia confiável para salvaguardar os ativos mais valiosos das organizações. Implementar essa norma permite que as empresas adotem uma abordagem sistemática e proativa na gestão de riscos, melhorando a tomada de decisões e fortalecendo a confiança dos stakeholders. Dessa forma, a ISO 31000 se torna um elemento essencial na estratégia de governança corporativa e sustentabilidade organizacional.

Acompanhe, Na Prática, como uma conhecida rede de lojas de vestuário infantojuvenil adotou as diretrizes da ISO 31000 após enfrentar desafios significativos no mercado. Ao perceber uma notável perda de clientes e o fechamento de várias filiais, a alta gestão reconheceu a necessidade de uma abordagem estratégica para a gestão de riscos, de modo a fortalecer a posição da empresa e conter o avanço da concorrência.

![](https://statics-marketplace.plataforma.grupoa.education/sagah/43b7d1be-dc52-4676-b119-a0bcc753032a/6aaee908-b010-4be7-92e8-8fc392fe9b2d.png)

​​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Segurança da informação em pequenas empresas: elaboração da cartilha de segurança
Neste estudo, você vai entender a importância da segurança de dados nas pequenas empresas e aprender a elaborar uma cartilha de segurança eficaz. Esse guia oferece conhecimento essencial para proteger as informações e fortalecer a segurança na sua organização.
[Mais](https://rsdjournal.org/index.php/rsd/article/view/41304/33793https://rsdjournal.org/index.php/rsd/article/view/41304/33793)

Entenda de vez o processo de gestão de riscos da norma ISO 31000
Neste artigo, você vai entender como a norma ISO 31000 estrutura o processo de gestão de riscos. Você vai aprender a identificar, avaliar e mitigar riscos de maneira eficaz, de modo a proteger os ativos e garantir a continuidade dos negócios.
[Mais](https://iso31000.net/processo-de-gestao-de-riscos/)

Conheça a ISO 22301:2019 – Sistemas de gestão de continuidade de negócios
Neste vídeo, você vai descobrir como a ISO 22301 pode ajudar a proteger os ativos da sua organização e garantir a continuidade das operações em situações de crise. Aprenda a implementar práticas eficazes de continuidade de negócios e assegure a resiliência da sua empresa.
[Mais](https://www.youtube.com/embed/f0a-utdK7FE?si=Nriy9qRb_hSGsTs-)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

BRASIL. Tribunal de Contas da União. Boas práticas em segurança da informação. 4.
ed. Brasília: TCU, 2012.

FONSECA, W. O que é token? 2009. Disponível em: <https://www.tecmundo.com.br/
senha/3077-o-que-e-token-.htm>. Acesso em: 12 jun. 2018.

NASCIMENTO, H. B. Segurança da informação para concursos. Rio de Janeiro: Ciência
Moderna, 2014.

TANENBAUM, A. S.; WETHERALL, D. J. Redes de computadores. São Paulo: Pearson, 2011.

TEIXEIRA FILHO, S. A. Segurança da informação descomplicada. São Paulo: Cultura, 2017.

Bancos gratuitos de imagens e Shutterstock.
SAGAH, 2024.

