Atualmente vemos uma quantidade sem precedentes de dados trafegando pelas redes de computadores. Diante desse cenário, a proteção dos dados sensíveis contra ataques é crucial tanto para indivíduos quanto para empresas. As funções hash, nesse contexto, oferecem uma abordagem simples para garantir a integridade das informações.

Os algoritmos de hash transformam dados de tamanho arbitrário em valores de tamanho fixo, conhecidos como hashes, de forma que qualquer alteração nos dados originais resulta em um hash completamente diferente. Essa propriedade torna os hashes ideais para verificar a integridade dos dados durante o armazenamento ou a transmissão. No entanto, é fundamental escolher algoritmos de hash robustos e atualizados, uma vez que vulnerabilidades podem comprometer a eficácia dessa proteção.

Nesta Unidade de Aprendizagem, você vai explorar o conceito das funções hash, vai entender a estrutura por trás do código hash e examinar os diferentes tipos de ataques.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Conceituar uma função hash.  
- Compreender a estrutura do código hash.
- Identificar os tipos de ataque.


## Desafio
Um algoritmo de hash consiste em uma função matemática aplicada a um conjunto de dados que vai gerar um outro número aleatório, bem menor, conhecido como hash ou “resumo”. As funções hash mais utilizadas recentemente são algoritmos que geram resumos de 16 bytes ou de 128 bits. Os mais comuns são os algoritmos das famílias MD e SHA.

Esses algoritmos são amplamente empregados em uma variedade de aplicações, desde garantir a integridade de arquivos até autenticar senhas de usuários. O MD5 e o SHA-1, por exemplo, são algoritmos mais antigos, amplamente utilizados no passado, mas agora considerados inseguros devido a vulnerabilidades descobertas. Por outro lado, o SHA-256 e o SHA-3 são exemplos de algoritmos mais modernos e considerados mais seguros, capazes de lidar com os desafios de segurança contemporâneos.

Diante disso, considere a situação a seguir.  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/6682aba5-b33a-47c8-9dde-07b008044278/d014d724-53e1-4c25-bbd4-9004c037f121.jpg)

  
Qual algoritmo de hash você utilizaria para fazer esse tipo de operação em seu site? Como funciona?

#### Padrão de resposta esperado
O MD5t opera de forma semelhante ao MD5 padrão, aplicando uma função de dispersão criptográfica nos dados de entrada para gerar um resumo ou hash. No entanto, a especificação "t" sugere que esse algoritmo seja adaptado para fins específicos, como verificação de integridade de arquivos baixados.

No contexto de um site, o MD5t seria usado da seguinte maneira:

• Quando o site disponibiliza um arquivo para download, ele calcula o hash MD5t do arquivo e o disponibiliza junto com o arquivo para que os usuários possam verificar a integridade do arquivo após o download.
• Os usuários que baixaram o arquivo podem calcular o hash MD5t do arquivo baixado e compará-lo com o hash fornecido pelo site. Se os hashes coincidirem, isso indica que o arquivo foi baixado com sucesso e sem alterações.
• No caso de autenticação de usuários, o site pode usar o MD5t para armazenar os hashes das senhas dos usuários em seu banco de dados.

Quando um usuário tenta fazer login, o site calcula o hash MD5t da senha inserida e compara-o com o hash armazenado em seu banco de dados para autenticar o usuário.

####  ✅ Resposta ao desafio:

Embora o padrão de resposta esperado cite o MD5t, tecnicamente a melhor escolha atualmente para verificar a integridade de arquivos disponibilizados em um site é o SHA-256, pois o MD5 e o SHA-1 possuem vulnerabilidades conhecidas e não são mais considerados seguros para aplicações modernas.

Resposta:

Eu utilizaria o algoritmo SHA-256 para realizar a verificação de integridade dos arquivos disponibilizados no site.

O SHA-256 funciona aplicando uma função matemática criptográfica ao arquivo, gerando um código único, chamado de hash, composto por 256 bits. Esse código representa o conteúdo do arquivo de forma resumida. Mesmo uma pequena alteração no arquivo gera um hash completamente diferente.

No contexto do site, o processo ocorreria da seguinte forma:

Quando um arquivo é disponibilizado para download, o servidor calcula o hash SHA-256 e o publica junto ao link do arquivo.
Após concluir o download, o usuário calcula o hash do arquivo recebido utilizando alguma ferramenta compatível com SHA-256.
O usuário compara o hash gerado localmente com o hash fornecido pelo site.
Se os dois códigos forem idênticos, isso indica que o arquivo foi baixado corretamente e não sofreu alterações durante a transferência.
Caso os hashes sejam diferentes, isso significa que o arquivo pode ter sido corrompido ou modificado.

Dessa forma, o uso do SHA-256 garante maior confiabilidade na verificação da integridade dos arquivos disponibilizados para download, oferecendo mais segurança do que algoritmos antigos, como MD5 e SHA-1.


## Infográfico

A cada dia surgem novas maneiras para que indivíduos maliciosos roubem ou extraviem dados de pessoas ou de empresas. Por isso, deve-se assegurar que os dados mais essenciais, como as senhas, não possam ser descobertos facilmente por esses indivíduos.

Uma boa prática para garantir a segurança dos dados é o uso de técnicas de criptografia, como a criptografia de ponta a ponta e o armazenamento seguro de senhas por meio de funções hash e técnicas de salting. Além disso, a conscientização dos usuários sobre boas práticas de segurança, como a criação de senhas fortes e a não divulgação de informações confidenciais, é importante para a proteção contra ameaças cibernéticas.

Neste Infográfico, veja o conceito de função hash e sua utilização.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/9e37e7be-fa5b-4100-8776-28ebbcd7eec7/7b0c2ba3-d019-48bf-a352-876f7ef88393.jpg)


## Conteúdo do Livro

Devido à grande quantidade de dados que circulam na rede mundial de computadores, é comum que servidores e bancos de dados sejam invadidos, roubados ou que tenham suas informações comprometidas de alguma forma.

Portanto, é preciso assegurar que os dados importantes para usuários e empresas, tais como senhas e dados confidenciais de clientes, não sejam descobertos por indivíduos maliciosos. As funções hash são relevantes em situações como essas, pois se apresentam como ferramentas simplificadas para garantir a integridade das informações.

No capítulo Funções hash, base teórica para esta Unidade de Aprendizagem, você vai estudar o conceito de função hash, a estrutura do código hash e os tipos de ataques.

Boa leitura.

​
## Dica do Professor

Muitos ataques contra os algoritmos de hash são realizados simplesmente para provar que a tecnologia que utilizam está obsoleta, que é hora de mudar e que é necessário passar a utilizar um outro algoritmo para uma determinada aplicação.

Esses ataques servem como um alerta para a comunidade de segurança cibernética sobre a importância de permanecer vigilante e adaptável às mudanças tecnológicas. Ao reconhecer as limitações e vulnerabilidades dos algoritmos, os profissionais de segurança são incentivados a buscar constantemente novas soluções e algoritmos mais fortes.

Nesta Dica do Professor, conheça os tipos de ataque​ e a importância da função hash em algumas prevenções.


## Exercícios

#### Questão 1
O conceito de função hash está intrinsecamente relacionado à noção de unicidade e uniformidade dos hashes gerados. Idealmente, uma boa função hash deve garantir que diferentes conjuntos de dados resultem em hashes distintos, e qualquer modificação mínima nos dados originais leve a um hash completamente diferente.
Qual é o conceito fundamental de uma função hash?
Selecione a resposta:
A.Algoritmo matemático que transforma dados de hash, de tamanho variável, em dados originais, de tamanho fixo.
B.Algoritmo matemático que ordena dados originais em ordem crescente e compara com dados de hash.
C.Algoritmo matemático que transforma dados de resumo com tamanho fixo em dados de tamanho variável.
D.Algoritmo matemático que transforma dados originais, de tamanho variável, em dados menores, de tamanho fixo.
E.Algoritmo matemático que ordena dados de hash em ordem decrescente.

✅ A alternativa correta é: D

#### Questão 2
Considere a importância das funções hash na segurança de dados e na criptografia moderna. Essas funções auxiliam na transformação de dados originais em resumos de tamanho fixo. Elas envolvem uma série de características que garantem a integridade, a autenticidade e a confidencialidade das informações.
Dessa forma, assinale a alternativa que apresenta corretamente as características de uma função hash.
Selecione a resposta:
A.Direcionalidade, resistência à colisão e diferenciação.
B.Bidimensionalidade, resistência à ordenação e recorrência.
C.Unidirecionalidade, resistência à colisão e recorrência.
D.Bidirecionalidade, resistência à colisão e recorrência.
E.Unidirecionalidade, colisão zero e repetência.

✅ A alternativa correta é: C

#### Questão 3
Considere um sistema de autenticação que armazena senhas dos usuários como hashes em um banco de dados. Quando um usuário cria uma nova senha, ela é convertida em um hash usando uma função de hash antes de ser armazenada. Mais tarde, quando o usuário tenta fazer login, a senha fornecida é novamente convertida em um hash e comparada com o hash armazenado no banco de dados.
Qual das seguintes afirmações descreve corretamente uma propriedade relevante das funções hash nesse contexto?
Selecione a resposta:
A.As funções hash podem recuperar os dados originais a partir do hash gerado.
B.As funções hash garantem que, sempre que dados diferentes são inseridos, o mesmo hash será gerado.
C.As funções hash garantem que, sempre que os mesmos dados são inseridos, um novo hash será gerado.
D.As funções hash podem gerar hashes de tamanho variável, dependendo do tamanho dos dados originais.
E.As funções hash são suscetíveis a colisões, em que dois conjuntos de dados diferentes produzem o mesmo hash.

✅ A alternativa correta é: C


#### Questão 4
Entre os algoritmos de hash mais conhecidos e amplamente utilizados, destacam-se diversas famílias, cada uma com suas próprias características e aplicabilidades. Esses algoritmos, muitas vezes padronizados e continuamente aprimorados, favorecem a proteção e a verificação de dados em ambientes digitais.
Assim, assinale a alternativa que apresenta algoritmos de hash conhecidos.
Selecione a resposta:
A.MB11 e CHA1.
B.MD5 e SHA-1.
C.MD0 d SHA-5.
D.ND5 e CHA-2.
E.ND4 e SHA-1.

✅ A alternativa correta é: B


#### Questão 5
A segurança da informação tornou-se uma preocupação para indivíduos e organizações. Entre as várias técnicas e ferramentas utilizadas para proteger dados sensíveis, as funções hash destacam-se. Esses algoritmos matemáticos são frequentemente empregados para garantir a integridade e a autenticidade dos dados e fornecer resumos únicos e irreversíveis das informações originais. No entanto, apesar de sua importância na segurança cibernética, as funções hash não estão isentas de vulnerabilidades e são frequentemente alvo de ataques por indivíduos mal-intencionados.
O principal motivo para os ataques às funções hash é:
Selecione a resposta:
A.provar que os algoritmos utilizados estão obsoletos.
B.provar que as funções de hash são infalíveis.
C.provar que não há necessidade de elaborar novos algoritmos de hash.
D.provar que não há possibilidade de que existam colisões em funções de hash.
E.provar que as funções de hash são bidirecionais.

✅ A alternativa correta é: A

## Na prática

No vasto campo da segurança cibernética, os algoritmos de hash são elementos essenciais para garantir a integridade, a autenticidade e a confidencialidade dos dados. No entanto, mesmo essas ferramentas não estão imunes a ataques maliciosos, muitos dos quais são realizados com o objetivo de demonstrar a obsolescência dos algoritmos existentes.

Os ataques aos algoritmos de hash podem ocorrer de várias formas, mas sua motivação subjacente muitas vezes é provar que a tecnologia empregada está desatualizada e vulnerável a explorações maliciosas. Esses ataques servem como um alerta para a comunidade de segurança cibernética e destaca a necessidade premente de adoção de soluções mais modernas para proteger os dados digitais.

Neste Na Prática, você vai ver como a criptografia de hash pode ser uma ferramenta poderosa na proteção de dados sensíveis em ambientes digitais. A história de Sarah, uma talentosa profissional de segurança cibernética, ilustra como a implementação cuidadosa de algoritmos robustos, como o SHA-256, pode fortalecer significativamente a segurança de aplicativos e sistemas.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/546d0f47-3fd2-4c3d-9737-9083cab338fd/eedba65f-f200-42ec-a031-d68f1dc112f8.jpg)

​​​​​​​
## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:
​​​
Hash criptográfico: passo a passo: MD5, SHA1, SHA512
Assista a este vídeo, que funciona como um guia para compreender os conceitos por trás dos algoritmos de hash criptográfico mais comuns: MD5, SHA1 e SHA512. Esses algoritmos são apresentados ao longo do vídeo, com explicações detalhadas sobre como funcionam e as diferenças entre eles.
[Mais](https://www.youtube.com/watch?si=v0AddoAYHTC4W1XS&v=H5__Qgtlg6k&feature=youtu.be)

Garantindo a integridade dos dados com códigos hash
Esse artigo mostra exemplos de criação de códigos hash utilizando linguagem de programação em C#, por meio de algoritmos como o hash SHA-256
[Mais](https://learn.microsoft.com/pt-pt/dotnet/standard/security/ensuring-data-integrity-with-hash-codes)

Validação de dados através de hashes criptográficos
Leia, no artigo indicado, sobre a aplicação de funções de hash na área Forense Computacional, na tentativa de combater o crime cibernético nesse meio.
[Mais](https://repositorio.ufpe.br/bitstream/123456789/15966/1/Mestrado%20-%20CIn-UFPE%20-%20Jos%c3%a9%20Paulo.pdf)

Algoritmos de hash e assinatura
Neste artigo da Microsoft, são exploradas as implicações e aplicações dessas duas técnicas fundamentais na segurança da informação. Discute-se a importância dos algoritmos de hash na verificação da integridade dos dados e na geração de resumos criptográficos únicos.
[Mais](https://learn.microsoft.com/pt-br/windows/win32/seccrypto/hash-and-signature-algorithms)

## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

CABRAL, C.; CAPRINO, W. Trilhas em segurança da informação. Rio de Janeiro: Brasport, 2015.

NAKAMURA, E. T.; GEUS, P. L. Segurança de redes em ambientes cooperativos. São Paulo:
Novatec, 2007.

ROHR, A. Com 'cálculo de 6,5 mil anos', Google quebra segurança da fórmula SHA-1. G1, 28 fev.2017. Disponível em: http://g1.globo.com/tecnologia/blog/seguranca-digital/post/com-calculo-de-65-mil-anos-google-quebra-seguranca-da-formula-sha-1.html. Acesso em: 15 maio 2024.

STALLINGS, W.; BROWN, L. Segurança de computadores: princípios e práticas. Rio de Janeiro:Elsevier, 2017.

Bancos gratuitos de imagens e Shutterstock.
SAGAH, 2024.



