## Apresentação

Nas organizações atuais, os dados são fundamentais para apoiar decisões e orientar estratégias. Utilizá-los de maneira adequada contribui para melhores resultados e maior eficiência. Nesse contexto, os sistemas de informação e os bancos de dados desempenham um papel essencial ao possibilitarem a organização, o armazenamento e o acesso estruturado às informações, apoiando os processos organizacionais e a tomada de decisão (Laudon; Laudon, 2019).

O gerenciamento de recursos de informação envolve a organização, o tratamento e a disponibilização dos dados dentro da empresa. Seu objetivo é garantir que as informações sejam confiáveis e estejam disponíveis quando necessárias, auxiliando no funcionamento das atividades e na tomada de decisão.

Nesta Unidade de Aprendizagem, você vai conhecer a importância dos bancos de dados no contexto organizacional, as principais ferramentas de administração de bancos de dados e os ambientes de bancos de dados mais utilizados nas organizações.
Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:
- Compreender o papel estratégico dos dados nas organizações.
- Explicar a importância dos bancos de dados para a gestão e a tomada de decisão.
- Aplicar os comandos de DCL para segurança em bancos de dados.


## Desafio

A administração de dados é um elemento que garante que as informações organizacionais sejam armazenadas, protegidas e utilizadas de forma estratégica. Nesse contexto, os sistemas de banco de dados permitem maior controle, integridade e segurança das informações, enquanto os comandos de DCL (Data Control Language) possibilitam gerenciar permissões de acesso, assegurando que cada usuário execute apenas as operações autorizadas (Silberschatz; Korth; Sudarshan, 2020).

Nesse contexto, confira a situação a seguir:

![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/106150/1236_EXA_DES_V4-2026-03-30T10:35:44-03:00.jpg)

Considerando essa situação, elabore uma proposta prática que contemple:
1. a justificativa para a implantação de um banco de dados na empresa, destacando os benefícios para a gestão e a tomada de decisão;
2. a definição de permissões de acesso para cada tipo de usuário (gerente, vendedor e auxiliar), indicando quais operações cada um poderá realizar;
3. a exemplificação de pelo menos dois comandos de DCL (como GRANT e REVOKE) que poderiam ser utilizados para configurar essas permissões;
4. a indicação do ambiente de banco de dados mais adequado (por exemplo, centralizado, distribuído ou em nuvem), com justificativa.


####  ✅ Resposta ao desafio:

1.Justificativa da implantação: A substituição de planilhas isoladas por um sistema de banco de dados traz benefícios claros:
- Centralização das informações: elimina duplicidade e inconsistências.
- Maior integridade e segurança: dados protegidos contra acessos não autorizados.
- Agilidade na tomada de decisão: relatórios e análises podem ser gerados rapidamente.
- Escalabilidade: o sistema acompanha o crescimento da empresa sem perda de eficiência.
- Colaboração eficiente: diferentes setores acessam dados atualizados em tempo real.

2.Definição de permissões: Cada perfil de usuário terá permissões específicas:
- Gerente: Consultar todos os dados (clientes, vendas, funcionários), Inserir e atualizar informações estratégicas e Gerar relatórios completos.
- Vendedor: Consultar dados de clientes e vendas, Inserir novos registros de vendas e Não pode alterar dados de funcionários.
- Auxiliar administrativo: Consultar dados de funcionários e clientes, Atualizar informações cadastrais (endereços, contatos) e Não pode inserir ou excluir registros de vendas.

3.Exemplos de comandos DCL
```sql
-- Concedendo permissão ao gerente para consultar e atualizar dados
GRANT SELECT, INSERT, UPDATE ON Clientes TO Gerente;

-- Revogando permissão de exclusão do vendedor
REVOKE DELETE ON Vendas FROM Vendedor;
```
Esses comandos garantem que cada usuário execute apenas operações autorizadas, reforçando a segurança e integridade dos dados.

4.Ambiente de banco de dados: O ambiente mais adequado seria em nuvem, pelas seguintes razões:
- Acessibilidade: usuários podem acessar de qualquer local, com segurança.
- Escalabilidade: fácil expansão conforme o crescimento da empresa.
- Custos reduzidos: elimina necessidade de infraestrutura física robusta.
- Backup e recuperação automática: maior confiabilidade contra perdas de dados.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 17069363
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 22/05/26 - 19:14
Disciplina: Modelagem e Desenvolvimento de Banco de Dados [TTEC0037] (2026-1-TTEC0037-TRIMESTRAL-EAD0303T)
Tarefa: Desafio
Tentativa: 1 de 1


## Infográfico

Nas organizações atuais, os bancos de dados são fundamentais para a gestão da informação, pois apoiam as atividades do cotidiano e auxiliam nas decisões em diferentes níveis da empresa (Elmasri; Navathe, 2016). Nesse cenário, a administração de dados deixa de ser apenas uma tarefa técnica e passa a fazer parte da gestão organizacional, contribuindo para processos mais eficientes e decisões mais adequadas.

Sob uma abordagem organizacional, o gerenciamento de bancos de dados envolve não apenas a infraestrutura tecnológica, mas também a definição de políticas, normas e responsabilidades relacionadas ao uso e à proteção das informações. Assim, deve ser entendido como parte integrante da estratégia institucional, contribuindo para a governança e para a sustentabilidade da organização, uma vez que o gerenciamento adequado dos dados permite garantir integridade, segurança e disponibilidade das informações utilizadas pela empresa (Heuser, 2009).

Neste Infográfico, você vai compreender as principais ferramentas e práticas utilizadas para garantir a segurança das informações.  Recursos como controle de acesso, definição de permissões e utilização de mecanismos de proteção são essenciais para assegurar que os dados sejam acessados apenas por usuários autorizados, evitando riscos e garantindo a confiabilidade das informações.

![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/106151/1236_EXA_INF_V4-2026-03-30T11:30:36-03:00.jpg)


## Conteúdo do Livro

Em um cenário empresarial cada vez mais orientado por dados, os bancos de dados desempenham papel essencial na organização e no gerenciamento das informações. Eles possibilitam o armazenamento estruturado de grandes volumes de dados, garantindo maior confiabilidade, agilidade no acesso e suporte às decisões organizacionais (Silberschatz; Korth; Sudarshan, 2020).

No contexto das organizações, os bancos de dados operacionais sustentam atividades essenciais, como processamento de pedidos, controle financeiro, gestão de estoques e distribuição de produtos. Além disso, sua administração envolve a definição de políticas, responsabilidades e mecanismos de segurança, assegurando a integridade, a confidencialidade e a disponibilidade das informações (Laudon; Laudon, 2019).

No capítulo Administração de dados e de banco de dados, base teórica desta Unidade de Aprendizagem, você vai compreender como o gerenciamento de bancos de dados se insere no contexto organizacional e quais práticas são adotadas para sua administração e segurança. Será possível identificar como as decisões relacionadas aos dados impactam a eficiência e a segurança das organizações.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/68dbb1ec-ec65-435f-a89b-b9ca94bde78b/751f96c4-40ab-4d31-a131-5f95f52f19df.jpg)


## Dica do Professor

No contexto das organizações contemporâneas, a gestão adequada de informações tornou-se um fator decisivo para o desempenho e a competitividade. Os bancos de dados são ferramentas fundamentais nesse processo, pois permitem armazenar, organizar e disponibilizar dados de forma estruturada, apoiando tanto as atividades operacionais quanto as decisões estratégicas.

Além disso, a administração eficiente de bancos de dados está diretamente relacionada ao papel do administrador de banco de dados (DBA), profissional responsável por planejar, implementar e manter os sistemas de banco de dados de uma organização. Entre suas atribuições, estão a definição de políticas de segurança, a gestão de usuários, a otimização do desempenho e a garantia da disponibilidade das informações, contribuindo para que os dados sejam utilizados de forma confiável e estratégica pelas organizações (Date, 2004). De maneira mais específica, a administração de banco de dados envolve o uso de ferramentas e práticas voltadas ao controle, à manutenção e à segurança das informações. 

Nesta Dica do Professor, você vai compreender como esses conceitos são aplicados na prática e visualizar exemplos relacionados ao gerenciamento e à segurança de bancos de dados.


## Exercícios

#### Questão 1
Em muitas organizações que utilizam sistemas de informação baseados em bancos de dados, diferentes profissionais são responsáveis por atividades relacionadas à gestão e ao uso estratégico dos dados. Essas funções incluem tanto a definição de políticas corporativas de informação quanto a administração técnica dos sistemas que armazenam e processam os dados.
Durante uma reunião de planejamento de tecnologia da informação, a equipe de gestão de dados discutiu as responsabilidades do administrador de dados (DA) e do administrador de banco de dados (DBA). Alguns membros da equipe apresentaram interpretações distintas sobre o papel de cada profissional na organização.
Considerando o contexto organizacional e as responsabilidades associadas a essas funções, assinale a alternativa que descreve corretamente a distinção entre o DA e o DBA.
Selecione a resposta:

a. O DA foca os recursos de informação em um contexto amplo, estabelecendo políticas e padrões, enquanto o DBA lida com SGBDs individuais, monitoramento de desempenho e integridade.

b. O DBA ocupa uma posição de alta gerência focada no planejamento estratégico de dados, enquanto o DA desempenha uma função de suporte técnico voltada exclusivamente para a instalação de hardware.

c. O DBA é responsável por gerenciar todos os tipos de dados da organização, como páginas web e arquivos externos, ao passo que o DA limita-se apenas aos dados armazenados em bancos de dados relacionais.

d. Ambas as funções são exclusivamente técnicas e não têm relação com o suporte à tomada de decisão gerencial nos níveis tático e estratégico da organização.

e. O DA é quem cria as instruções SQL de segurança (como GRANT e REVOKE), enquanto o DBA é responsável por negociar prazos contratuais com fornecedores de TI em nível corporativo.

✅ A alternativa correta é: a.

#### Questão 2
As organizações modernas dependem de uma gestão eficiente de seus ativos de informação para suportar tanto as operações diárias quanto o planejamento estratégico. Nesse cenário, o gerenciamento de recursos de informação busca integrar os ciclos de vida da informação para fornecer dados oportunos e consistentes para a tomada de decisão. Sobre as responsabilidades dos especialistas e os mecanismos de controle de acesso, analise as seguintes opções:
I. O administrador de dados (DA) ocupa uma posição de nível gerencial, com foco no planejamento estratégico e no desenvolvimento do modelo de dados corporativo, enquanto o administrador de banco de dados (DBA) tem uma função de suporte técnico voltada para SGBDs específicos, monitoramento de desempenho e integridade.
II. No controle de acesso discricionário, o uso de visões (views) permite um controle mais refinado da segurança, pois possibilita restringir o acesso a colunas ou linhas específicas de uma tabela, garantindo que usuários visualizem apenas a "matéria-prima" necessária para sua função.
III. O nível gerencial operacional (baixa gerência) fundamenta suas decisões em dados externos resumidos, como previsões econômicas e relatórios industriais, para identificar novos mercados e planejar o crescimento da organização a longo prazo.
IV. A cláusula WITH ADMIN, utilizada na criação de papéis (roles), e a opção WITH GRANT OPTION, em instruções GRANT, permitem que privilégios sejam repassados a outros usuários, devendo ser utilizadas com moderação devido à ampla liberdade de ação que concedem.
É correto o que se afirma em:
Selecione a resposta:
a. I e II, apenas.
b. I, II e IV, apenas.
c. I e III, apenas.
d. II e IV, apenas.
e. I, II, III e IV.

✅ A alternativa correta é: b. I, II e IV, apenas.

#### Questão 3
A gestão eficiente de bancos de dados depende da compreensão dos diferentes ambientes informacionais existentes nas organizações. Cada ambiente tem uma finalidade específica e impacta diretamente o modo como os dados são coletados, armazenados e utilizados. Entre esses ambientes, destaca-se aquele que sustenta as operações diárias, registrando transações e apoiando diretamente os processos organizacionais.
Considerando essa perspectiva, assinale a alternativa que identifica corretamente o ambiente de dados responsável pelo suporte às atividades operacionais da organização.
Selecione a resposta:
a. Banco de dados distribuídos.
b. Datawarehouses.
c. Processamento de transações.
d. Banco de dados orientado a objetos.
e. Banco de dados relacionais.

✅ A alternativa correta é: c) Processamento de transações.


#### Questão 4
Em modelos de segurança aplicados a bancos de dados que armazenam informações altamente sensíveis e com baixo grau de alteração, o controle de acesso é fundamentado na correspondência entre o nível de autorização do usuário e o nível de classificação dos dados. Nesse contexto, o sistema gerenciador de banco de dados (SGBD) utiliza mecanismos da linguagem SQL para implementar políticas de controle de acesso discricionário.
Considerando esse cenário, assinale a alternativa que descreve corretamente as funções das instruções GRANT e REVOKE na administração da segurança de um banco de dados.
Selecione a resposta:

a. GRANT é utilizada para criar perfis de usuários, enquanto REVOKE exclui permanentemente usuários do banco de dados.

b. GRANT define níveis de classificação de dados sensíveis, enquanto REVOKE altera o nível de autorização do usuário no sistema.

c. GRANT criptografa tabelas e visões do banco de dados, enquanto REVOKE descriptografa dados protegidos.

d. GRANT concede privilégios de acesso a usuários ou papéis sobre objetos do banco de dados, enquanto REVOKE remove privilégios anteriormente concedidos.

e. GRANT cria mecanismos de auditoria de acesso, enquanto REVOKE ativa políticas de backup e recuperação.

✅ A alternativa correta é: d.


#### Questão 5
No contexto do gerenciamento organizacional de bancos de dados, o dicionário de dados é considerado um repositório especializado que armazena informações estruturais e descritivas sobre os objetos do banco de dados e seu ambiente. Ele documenta elementos como tabelas, atributos, relacionamentos, restrições e regras de negócio, garantindo padronização, controle e integridade das informações.
Nesse sentido, o dicionário de dados é composto por descritores responsáveis por definir a origem, o uso, o domínio de valores e o significado dos dados no sistema.
Assinale a alternativa que apresenta corretamente a denominação desses descritores.
Selecione a resposta:
a. Instâncias de dados.
b. Registros físicos.
c. Índices primários.
d. Tuplas operacionais.
e. Metadados.

✅ A alternativa correta é: e. Metadados.


## Na prática

A gestão eficiente de dados é o alicerce da computação corporativa moderna, fornecendo o suporte necessário tanto para as funções operacionais diárias quanto para a tomada de decisões em múltiplos níveis organizacionais (Laudon; Laudon, 2019).

Essa gestão é operacionalizada pela colaboração entre o administrador de dados (DA) e o administrador de banco de dados (DBA). Enquanto o DA tem um foco voltado a negócio e gestão, sendo responsável por desenvolver o modelo de dados corporativo e definir políticas globais de compartilhamento, o DBA foca a tecnologia e execução, realizando a modelagem física, monitorando o desempenho e executando os comandos técnicos de segurança no SGBD. Essa sinergia garante que a informação seja tratada como um recurso estratégico, fluindo adequadamente entre os níveis operacional, tático e estratégico da organização (Elmasri; Navathe, 2016).

Neste Na Prática, você vai compreender a importância da integração entre a visão estratégica da administração de dados e a execução técnica da administração de banco de dados para o suporte à decisão.

![Descrição da imagem não disponível](https://creator-files.plataforma.grupoa.education/learning-object/106155/CAPA-2026-03-30T12:14:01-03:00.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Otimização de banco de dados: técnicas e boas práticas para um desempenho aprimorado
Este artigo mostra como os bancos de dados desempenham um papel crucial em praticamente todos os aspectos de nossa vida digital atual. Seja em sistemas empresariais, aplicativos móveis ou serviços web, o acesso eficiente e rápido aos dados é essencial.
[Mais](https://www.dio.me/articles/otimizacao-de-banco-de-dados-tecnicas-e-boas-praticas-para-um-desempenho-aprimorado)

Bancos de dados gratuitos
Os bancos de dados são fundamentais para armazenar e gerenciar informações de forma estruturada. Algumas opções gratuitas oferecem ótimos recursos sem comprometer a eficiência, sendo ideais para projetos de pequeno e médio porte.
[Mais](https://www.devmedia.com.br/banco-de-dados-gratuitos/44139)

Principais desafios na gestão de um banco de dados
Este artigo mostra que a gestão de um banco de dados vai muito além do armazenamento de informações. Envolve segurança, desempenho, escalabilidade e estratégia organizacional.
[Mais](https://horusinfo.com.br/principais-desafios-na-gestao-de-um-banco-de-dados/)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

DATE, C. J. An introduction to database systems. 8. ed. Boston: Pearson Addison Wesley,
2004.

DAVENPORT, T. H. The AI advantage: how to put the artificial intelligence revolution to work.
Cambridge: MIT Press, 2018.

ELMASRI, R.; NAVATHE, S. B. Fundamentals of database systems. 7. ed. Boston: Pearson,
2016.

HEUSER, C. A. Projeto de banco de dados. 6. ed. Porto Alegre: Bookman, 2009.

LAUDON, K. C.; LAUDON, J. P. Management information systems: managing the digital firm. 15. ed. Harlow: Pearson, 2019.

MACHADO, F. N. R. Banco de dados: projeto e implementação. 2. ed. São Paulo: Érica, 2014.

MANNINO, M. V. Projeto, desenvolvimento de aplicações e administração de banco de dados. 3. ed. Rio de Janeiro: LTC, 2014.

RAMAKRISHNAN, R.; GEHRKE, J. Sistemas de gerenciamento de banco de dados. 3. ed. São Paulo: McGraw-Hill, 2011.

SILBERSCHATZ, A.; KORTH, H. F.; SUDARSHAN, S. Database system concepts. 7. ed. New York: McGraw-Hill, 2020.

Bancos gratuitos de imagens e Shutterstock. 
SAGAH, 2026.

