## presentação

Empresas e pessoas passaram a utilizar a internet para agilizar processos e atividades que envolvem troca de informações, especialmente as financeiras. No entanto, apesar de proporcionar essa conveniência, ela não garante automaticamente privacidade, confidencialidade ou segurança.​​​​​​​

Para garantir a transmissão segura e confiável das informações, foi necessário desenvolver um método específico. Assim, surgiu a infraestrutura de chaves públicas (ICP).

Nesta Unidade de Aprendizagem, você verá o conceito de infraestrutura de chaves públicas e os desafios relacionados à sua distribuição. Além disso, conhecerá a principal autoridade responsável pelo registro de chaves públicas.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Compreender o que é uma infraestrutura de chaves públicas.
- Identificar o problema da distribuição de chaves.
- Reconhecer a principal autoridade certificadora de chaves públicas.


## Desafio

A criptografia é o processo de aplicação de um algoritmo de codificação em dados que precisam ficar ininteligíveis para aqueles indivíduos que não estão envolvidos nesta transação específica, podendo acontecer de forma simétrica ou assimétrica.

A partir dessa informação, analise o cenário a seguir:

Você é o profissional responsável pela segurança da informação da empresa na qual trabalha, que, apesar de pequena, já executa muitas atividades on-line por meio de certificação digital. Os gestores da empresa, como pagam pelos seus serviços, assim como pelo certificado, pediram para que você esclareça algumas de suas dúvidas.

Diante deste contexto, responda às questões dos gestores:

a) Por que a infraestrutura de chaves públicas utiliza criptografia assimétrica para realizar transações pela internet?

b) As informações sigilosas da empresa estão realmente seguras sendo enviadas e recebidas desta maneira? Justifique a sua resposta.

#### Padrão de resposta esperado

a) O modelo de criptografia assimétrica é adotado pela infraestrutura de chaves públicas porque resolve o problema da distribuição das chaves, comum na criptografia simétrica. Essa adversidade envolve a dificuldade de transmitir a chave, necessária para criptografar e descriptografar os dados, sem que ela seja interceptada por terceiros durante a comunicação.

b) A criptografia assimétrica utiliza um par de chaves distintas para criptografar e descriptografar dados: a chave privada e a chave pública. A chave pública é compartilhada amplamente, enquanto a chave privada é mantida em segredo por uma das partes envolvidas na transação. Essa abordagem garante que apenas o destinatário possa descriptografar os dados, pois a chave privada é necessária para tal operação, sendo extremamente difícil deduzi-la a partir da chave pública. Assim, enquanto qualquer um pode usar a chave pública para criptografar dados, somente a parte com a chave privada correspondente pode efetuar a descriptografia, proporcionando segurança e confiabilidade às comunicações.


####  ✅ Resposta ao desafio:

a) Por que a infraestrutura de chaves públicas utiliza criptografia assimétrica para realizar transações pela internet?

A infraestrutura de chaves públicas (PKI) utiliza a criptografia assimétrica porque ela resolve o problema da distribuição segura das chaves, presente na criptografia simétrica. Nesse modelo, não é necessário compartilhar uma única chave secreta entre as partes. Em vez disso, cada usuário possui um par de chaves: uma chave pública, que pode ser divulgada livremente, e uma chave privada, que permanece em segredo. Dessa forma, elimina-se o risco de interceptação da chave durante sua transmissão pela internet.

b) As informações sigilosas da empresa estão realmente seguras sendo enviadas e recebidas desta maneira? Justifique a sua resposta.

Sim, as informações são protegidas de forma bastante segura quando a criptografia assimétrica é utilizada corretamente. Nesse modelo, os dados são criptografados com a chave pública do destinatário e somente a chave privada correspondente pode realizar a descriptografia. Como a chave privada permanece em posse exclusiva do destinatário e é extremamente difícil obtê-la a partir da chave pública, terceiros não conseguem acessar o conteúdo das informações transmitidas.

Além disso, a infraestrutura de chaves públicas permite o uso de certificados digitais para autenticar as partes envolvidas na comunicação, proporcionando maior confiabilidade às transações eletrônicas. Portanto, desde que as chaves privadas sejam mantidas protegidas e os certificados sejam válidos, as informações sigilosas da empresa podem ser transmitidas com segurança pela internet.


## Infográfico
Em uma era dominada pelas transações digitais, compreender a ICP é essencial. Esse sistema complexo garante a autenticação segura das partes envolvidas em transações on-line por meio da criptografia de chave pública. Essencialmente, ele assegura que as transações sejam conduzidas de maneira segura e confiável, protegendo a integridade e a confidencialidade das informações envolvidas.

A ICP é constituída por vários componentes essenciais, que incluem protocolos de segurança, serviços de certificação e políticas de gerenciamento de chaves. Esses elementos operam de forma integrada para estabelecer um ambiente seguro para a troca de informações digitais, possibilitando que entidades verifiquem a autenticidade e a integridade dos dados durante as transações virtuais. Compreender a interação desses componentes é fundamental para profissionais envolvidos com segurança da informação e gestão de transações digitais.

Neste Infográfico, você vai ver os componentes que formam a ICP, incluindo os protocolos, os serviços e as políticas que possibilitam trocas digitais seguras.  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/b346dcb0-88bc-4ceb-b6e8-6fad56c16f10/e58646fe-674d-436a-8c24-8c9527a82bcb.png)

​​​​​​​
## Conteúdo do Livro
Para acelerar e otimizar processos e atividades, tanto pessoas quanto empresas passaram a realizar operações on-line. No entanto, embora essa abordagem proporcione maior comodidade e rapidez em várias transações, é importante destacar que a internet, por si só, não garante segurança e confiabilidade absolutas.

Por isso, foi necessário desenvolver um método para tornar essas transações mais seguras e confiáveis, resultando na criação dos certificados digitais. Esses documentos eletrônicos são virtualmente assinados por uma autoridade certificadora e têm o papel de garantir a autenticidade e a integridade das informações transmitidas pela rede. No Brasil, esses certificados são emitidos pela ICP-Brasil.

No capítulo Infraestrutura de chaves públicas, base teórica desta Unidade de Aprendizagem, você vai estudar o conceito de infraestrutura de chaves públicas e o problema da distribuição das chaves, além de reconhecer a principal autoridade registradora de chaves públicas.

Bons estudos!

## Dica do Professor
A criptografia é importante para transformar dados claros em códigos cifrados, garantindo que apenas as partes autorizadas possam interpretá-los, especialmente em um mundo no qual a troca digital de informações é cada vez mais comum. Existem duas abordagens principais para codificar mensagens: a criptografia simétrica e a assimétrica, cada uma com métodos e aplicações específicas.

No entanto, a ICP desempenha um papel indispensável na segurança das transações digitais, proporcionando uma autenticação segura das partes envolvidas por meio da criptografia de chave pública. Ela engloba uma série de protocolos, serviços e políticas que garantem a integridade e a confidencialidade das informações no ambiente digital.

Nesta Dica do Professor, você vai aprender sobre o desafio inerente à criptografia: a distribuição segura das chaves.


## Exercícios

#### Questão 1
Em um mundo conectado, a autenticação digital por meio de certificados digitais tornou-se uma necessidade incontornável.
Além de validar a identidade, quais outras funções os certificados digitais podem desempenhar?
Selecione a resposta:
A.Facilitar a troca de chaves privadas entre usuários.
B.Garantir a integridade e a confidencialidade dos dados transmitidos.
C.Executar algoritmos de criptografia diretamente em mensagens.
D.Servir como uma interface gráfica para a autenticação de usuários.
E.Atuar como intermediário em transações financeiras on-line.

✅ A alternativa correta é: B


#### Questão 2
Para navegar com segurança no ambiente digital, é essencial compreender os sistemas que garantem a confiança eletrônica.
Qual é a função de uma ICP?
Selecione a resposta:
A.Gerenciar as transações entre bancos e outras instituições financeiras.
B.Servir como um sistema de backup para documentos digitais críticos.
C.Criptografar todas as comunicações eletrônicas em uma organização.
D.Supervisionar as políticas de segurança interna das empresas.
E.Emitir certificados digitais que autenticam identidades digitais e estabelecem confiança.

✅ A alternativa correta é: E

#### Questão 3
A criptografia é uma peça-chave na segurança de dados digitais.
Qual dos seguintes exemplos melhor descreve uma limitação da criptografia simétrica?
Selecione a resposta:
A.Depende da troca segura da chave secreta entre as partes.
B.Necessita de um par de chaves para a comunicação segura.
C.Utiliza algoritmos mais lentos que a criptografia assimétrica.
D.Não oferece segurança contra ataques de força bruta.
E.Não pode ser utilizada para grandes volumes de dados.

✅ A alternativa correta é: A


#### Questão 4
No cenário atual de segurança cibernética, a criptografia assimétrica desempenha um papel fundamental.
Qual é uma das principais vantagens da criptografia assimétrica em relação à simétrica?
Selecione a resposta:
A.Permite a criptografia e a descriptografia usando a mesma chave.
B.Requer menos poder computacional para processar dados.
C.Usa algoritmos que são menos suscetíveis a ataques de força bruta.
D.Elimina a necessidade de troca segura de chaves.
E.Oferece maior velocidade de processamento de dados.

✅ A alternativa correta é: D


#### Questão 5
A ICP-Brasil desempenha um papel fundamental na segurança digital do país.
Além do Serviço Federal de Processamento de Dados (Serpro) e da Autoridade Certificadora do Ministério da Defesa (AC Defesa), quais outras entidades estão envolvidas na ICP-Brasil?
Selecione a resposta:
A.Ministério da Saúde e Receita Federal.
B.Tribunal de Contas da União (TCU) e Banco Central.
C.Caixa Econômica Federal e Correios.
D.Polícia Federal e Ministério da Justiça.
E.Agência Nacional de Telecomunicações (Anatel) e Instituto Nacional do Seguro Social (INSS).

✅ A alternativa correta é: C


## Na prática
A ICP-Brasil é composta por diversas autoridades certificadoras, cada uma com características distintas, o que torna difícil apontar uma como a mais importante. O certificado digital é um documento eletrônico assinado digitalmente por uma dessas autoridades certificadoras, que associa uma chave pública a uma entidade, podendo ser uma pessoa, um computador ou uma empresa.

O certificado digital atua como uma espécie de identidade virtual, possibilitando a realização segura de transações por meio de computadores. O processo para a obtenção do certificado digital inclui uma série de procedimentos que objetivam assegurar a confidencialidade, a segurança e a integridade das informações trocadas entre as partes envolvidas na transação.

Neste Na Prática, você vai ver como uma pessoa física pode obter um certificado digital para realizar transações on-line de forma segura.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/053787ca-1413-4fc7-acc6-9c60fc65592b/0dba19ff-4534-446e-9556-4873887a3b4b.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Criptografia simétrica e assimétrica: confira a diferença
Este artigo aborda os conceitos de criptografia simétrica e assimétrica, destacando as diferenças entre os dois métodos. Você vai ver os contextos em que cada tipo de criptografia é mais eficiente, facilitando, assim, a escolha adequada para diferentes necessidades de segurança.
[Mais](https://www.totvs.com/blog/gestao-para-assinatura-de-documentos/criptografia-simetrica-e-assimetrica/)

Conheça os tipos de certificados digitais ICP-Brasil
Neste artigo, serão apresentados os diferentes tipos de certificados digitais da ICP-Brasil, com ênfase em como cada um deles contribui para a proteção das informações.
[Mais](https://validcertificadora.com.br/blogs/certificado-digital/conheca-os-tipos-de-certificados-digitais-icp-brasil/)

ICP-Brasil e certificado digital
Neste vídeo, você vai entender como funciona o processo de certificação digital pela ICP-Brasil no contexto da segurança da informação. Além disso, vai explorar a relevância dos certificados digitais emitidos e como eles asseguram a autenticidade e a segurança das transações on-line.
[Mais](https://www.youtube.com/embed/sfZ78441w90?si=zfKk6cJnQgpnymBX)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

BALDAM, R. Gerenciamento de conteúdo empresarial. Rio de Janeiro: Elsevier, 2016.

MARTINI, R. S. Tecnologia e cidadania digital: tecnologia, sociedade e segurança. Rio
de Janeiro: Brasport, 2008.

SILVEIRA, S. A. Criptografia assimétrica... você ainda vai precisar dela. Revista eletrônica
A REDE, n. 10, p. 32-33. 2006.

Bancos gratuitos de imagens e Shutterstock.
SAGAH, 2024.



