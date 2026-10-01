## Apresentação

Atualmente, ataques cibernéticos, invasão de sistemas e vazamento de dados na rede são assuntos tratados por pessoas ou noticiados no dia a dia. Isso tem se tornado comum, pois, hoje em dia, tudo tem algum tipo de conexão ou armazena algum dado ou até mesmo uma localização.

O objetivo por trás da varredura de portas e de redes é identificar a organização de endereços IP, hosts e portas para determinar adequadamente locais de servidores abertos ou vulneráveis e diagnosticar níveis de segurança. A varredura de rede e de porta pode revelar a presença de medidas de segurança, como um firewall entre o servidor e o dispositivo do usuário.

Nesta Unidade de Aprendizagem, você vai conhecer os assuntos relacionados à varredura de portas e serviços, etapa crucial para que uma invasão ou ataque possa ocorrer. Primeiramente, você vai conferir conceitos básicos. Depois, vai aprender a identificar portas e serviços e, por fim, saber como implementar técnicas de varredura.

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir varredura de porta.
- Identificar as portas e os serviços.
- Implementar técnicas de varredura.

## Desafio

A segurança da informação é um campo multidisciplinar que se concentra na proteção dos dados contra acesso não autorizado, uso indevido, divulgação, interrupção, modificação, destruição ou roubo. Ela abrange uma série de medidas técnicas, políticas, procedimentos e práticas para garantir a confidencialidade, a integridade e a disponibilidade das informações.

A proteção das redes de computadores contra acesso não autorizado, interrupções de serviço e outras ameaças envolve a configuração adequada de firewalls, detecção de intrusões e segmentação de rede. Além disso, devem ser feitas identificação, avaliação e mitigação de vulnerabilidades em sistemas e aplicativos por meio de testes de segurança, patches de software e outras medidas corretivas.

A partir dessas informações, considere o seguinte cenário:

A empresa ABC contratou você, analista de segurança de redes, para gerenciar a equipe de segurança da informação e suporte de redes.  

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/d3cc1e9b-02c7-4584-81ff-edb702ff0eac/abf91ad1-2d4f-44cd-a875-45e4b50f4644.png)

​​​​​​​Considerando sua nova função, você deve listar medidas para que esse tipo de situação não volte a se repetir, com precauções a serem adotadas pela empresa.


####  ✅ Resposta ao desafio:

  
Como analista de segurança de redes, eu recomendaria que a empresa ABC adotasse as seguintes medidas preventivas para evitar novos ataques cibernéticos:

- Manter todos os sistemas operacionais e softwares atualizados, corrigindo vulnerabilidades conhecidas.  
- Instalar e manter antivírus e antimalware atualizados em todos os equipamentos.  
- Implementar firewalls para controlar e monitorar o tráfego da rede.  
- Utilizar sistemas de detecção e prevenção de intrusões (IDS/IPS).  
- Adotar autenticação multifator (MFA) para acesso aos sistemas críticos.  
- Criar políticas de senhas fortes, exigindo combinações complexas e trocas periódicas.  
- Restringir privilégios de acesso, concedendo apenas as permissões necessárias a cada colaborador.  
- Realizar backups periódicos dos dados e testar os procedimentos de recuperação.  
- Criptografar informações sensíveis armazenadas e transmitidas pela rede.  
- Monitorar continuamente os logs e eventos de segurança.  
- Segmentar a rede para limitar a propagação de ataques.  
- Realizar auditorias e testes de vulnerabilidade regularmente.  
- Desenvolver um plano de resposta a incidentes de segurança.  
- Promover treinamentos periódicos de conscientização sobre segurança da informação para os funcionários.  
- Estabelecer políticas claras para o uso de dispositivos pessoais (BYOD) e recursos corporativos.

Com a adoção dessas medidas, a empresa reduzirá significativamente os riscos de infecção por vírus, vazamento de informações e exploração de falhas de segurança, fortalecendo a confidencialidade, a integridade e a disponibilidade dos dados corporativos.


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 20947947
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 01/10/26 - 19:39
Disciplina: Fundamentos de Segurança da Informação [TTEC0023] (2026-2-TTEC0023-TRIMESTRAL-EAD0301T)
Tarefa: Desafio
Tentativa: 1 de 1

## Infográfico

A intrusão pode ser realizada por um usuário legítimo que tenta obter acessos adicionais aos que já tem, ou até mesmo por um usuário que pretende agir de forma maliciosa – na maioria das vezes, com finalidades financeiras.

Além disso, é importante ressaltar que as intrusões podem ocorrer não apenas por usuários internos, mas também por agentes externos, como hackers, crackers e outros indivíduos mal-intencionados. Esses invasores podem tentar não apenas obter informações confidenciais, mas também interromper operações comerciais, causar danos à reputação da empresa ou até mesmo extorquir fundos por meio de ransomware ou outras formas de ataques cibernéticos.

Neste Infográfico, você vai compreender o que é a intrusão e como ela ocorre.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/6781abb0-fc6e-45cf-af53-303908120669/69127fdb-eb1a-4d9b-b868-96460aac58a8.png)


## Conteúdo do Livro

Geralmente, a varredura de portas e serviços antecede a etapa de enumeração para que haja um ataque cibernético, o qual pode atingir não apenas um computador, mas toda a rede. Dessa forma, a identificação das portas ocorre para que as vulnerabilidades da rede sejam reveladas, facilitando a execução de ataques maliciosos.

Varredura de portas e serviços é uma etapa crucial no processo de preparação para um ataque cibernético. Ao identificar as portas abertas e os serviços em execução em um sistema ou rede, os invasores podem determinar quais pontos de entrada estão disponíveis para explorar. Isso permite que eles encontrem vulnerabilidades específicas nos serviços em execução e usem técnicas de enumeração para obter informações detalhadas sobre os sistemas-alvo.

No capítulo Varredura de portas e serviços, base teórica desta Unidade de Aprendizagem, você vai compreender melhor o contexto que envolve a varredura de portas e serviços e conhecer suas definições. Além disso, vai entender como as portas são identificadas e conhecer as principais formas de realizar uma varredura.

Boa leitura.

## Dica do Professor

A utilização constante de computadores para a execução das mais variadas atividades acabou atraindo o interesse não apenas pelo lado positivo de suas funcionalidades, mas também pela quantidade de informações valiosas contidas nesses recursos. Dessa forma, a confidencialidade é um dos principais fatores ligados à segurança da informação.

Com efeito, a crescente dependência dos computadores para uma ampla gama de atividades despertou o interesse pelas suas capacidades positivas e também pela abundância de informações sensíveis que residem nesses sistemas. Nesse contexto, a confidencialidade emerge como um dos pilares fundamentais da segurança da informação.

Nesta Dica do Professor, você vai saber mais sobre a confidencialidade, que objetiva a proteção dos interesses das organizações e dos indivíduos e também fortalece a confiança do público nas operações on-line e na economia digital como um todo.


## Exercícios

#### Questão 1
O sistema de detecção de intrusão (intrusion detection system – IDS) é utilizado para detecção de atividades maliciosas em uma rede ou até mesmo em um computador específico, podendo este ser pessoal ou corporativo.
Assinale a alternativa que traz uma das possíveis ameaças que o IDS é capaz de detectar.​​​​​​​
Selecione a resposta:
a. Um falso ataque utilizando uma identificação com o objetivo de ter acesso a determinado sistema denomina-se usuário clandestino.
b. O bloqueio ou a eliminação de arquivos do sistema caracterizam a ação de um infrator.
c. Um impostor encobre suas ações eliminando registros do sistema.
d. Um usuário clandestino é aquele que realiza diversos testes de bloqueio do sistema por meio de tentativas de erros e acertos de senha de acesso.
e. O acesso a funcionalidades do sistema – que não condizem com o perfil do usuário – caracteriza a ação de um infrator.

✅ A alternativa correta é: E

#### Questão 2
No decorrer dos anos, os sistemas computacionais passaram por diversas mudanças. Entretanto, deve-se ter em mente que algumas características acabaram sendo herdadas. Uma delas é o acesso à internet. Contudo, muitos ainda acreditam que todos os sistemas são sempre confiáveis.
Assinale a alternativa que traz o conceito da etapa de reconhecimento de perfil.
Selecione a resposta:
a. É um processo que pode ser realizado em uma base de dados do tipo WHOIS, em que o hacker busca informações de domínio, contatos e endereços IP.
b. É uma série de ataques a redes com o objetivo de sobrecarregar um host e impedir acessos legítimos.
c. São diversos ataques de softwares maliciosos que se replicam, como cavalos de Troia, vermes de computadores, vírus, entre outros.
d. É uma ação voltada para a divulgação das informações confidenciais financeiras do cliente na rede.
e. É a tentativa de bloquear registros do sistema, impedindo o acesso tanto aos softwares como aos recursos de hardware.

✅ A alternativa correta é: A 

#### Questão 3
Conforne Goodrich et al. (2013, p. 302), "qualquer técnica que permita a um usuário enumerar quais portas em uma máquina estão aceitando conexões é conhecida como varredura de porta".
Assinale a alternativa cujo conceito se relaciona a um ponto de contato entre a internet e a aplicação que está ouvindo essa porta particular.​​​​​​​
Selecione a resposta:
a. Portas ociosas.
b. Portas abertas.
c. Portas ​​​​​​​fechadas.
d. Portas ​​​​​​​semiabertas.
e. Portas bloqueadas.

✅ A alternativa correta é: B 


#### Questão 4
Como é difícil encontrar uma máquina "zumbi" com números de sequência previsíveis, essa varredura não é frequentemente utilizada na prática, porém é uma maneira eficaz de fazer uma varredura em um alvo sem deixar qualquer registro do endereço IP do atacante na rede-alvo.
A qual tipo de varredura o texto se refere?​​​​​​​
Selecione a resposta:
a. Varredura SYN.
b. Varredura TCP.
c. Varredura ociosa.
d. Varredura UDP.
e. Varredura Honeypots.

✅ A alternativa correta é: C

#### Questão 5
A fase de reconhecimento é um componente crucial em qualquer ataque malicioso. Durante essa etapa, os invasores realizam uma série de atividades destinadas a obter informações sobre os sistemas-alvo e a infraestrutura de rede. Isso pode incluir a identificação de hosts disponíveis na rede, a análise de serviços em execução nesses hosts e a verificação de vulnerabilidades conhecidas.
A possibilidade de se conectar ao(s) host(s)-alvo, a análise de host-alvo para descobrir serviços que estão armazenados e estão sendo executados nele, bem como a verificação de vulnerabilidades conhecidas são características de qual etapa de um ataque malicioso?
Selecione a resposta:
a. Serviços de FTP.
b. Serviços de SMTP.
c. Serviços de enumeração.
d. Serviços de varredura/escaneamento.
e. Serviços de DNS.

✅ A alternativa correta é: D


## Na prática

A segurança da informação é uma preocupação evidente para todas as empresas, sobretudo em um mundo cada vez mais conectado digitalmente. Os protocolos de segurança desempenham um papel fundamental na proteção dos ativos de uma organização contra ameaças cibernéticas, garantindo a confidencialidade, a integridade e a disponibilidade dos dados. Esses protocolos estabelecem diretrizes e procedimentos para proteger os sistemas de informação contra acessos não autorizados, ataques maliciosos e outras vulnerabilidades.

Uma das práticas essenciais no âmbito dos protocolos de segurança é a realização de varreduras de portas. Essas varreduras são procedimentos que visam a identificar quais portas de comunicação estão abertas em um sistema, possibilitando a detecção de possíveis pontos de entrada para ataques.

Acompanhe, Na Prática, como se dá o processo de varredura de portas.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/13414248-05c5-418c-8d38-ac956115284d/3dcf8283-e89e-46c1-9044-d7246bbd78c6.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Realizando varreduras de rede com NMAP – HackerSec
Confira, neste vídeo, uma visão prática e detalhada de como usar a ferramenta NMAP para realizar varreduras de rede de forma eficiente. Veja práticas e insights sobre como utilizar o NMAP para descobrir dispositivos, serviços e potenciais vulnerabilidades em uma rede.
[Mais](https://www.youtube.com/embed/Wn8d9zwYPzg?si=P16a3PPKoQkbCCOz)

Uma abordagem para identificação e análise forense de ataques DNS
Leia este artigo, que apresenta uma abordagem inovadora em informática forense, visando a identificar automaticamente a presença de ataques de envenenamento de cache DNS. Integrando os elementos essenciais desse tipo de ataque ao contexto legal, o objetivo é detectar e documentar de forma precisa e eficaz a ocorrência desse crime cibernético.
[Mais](https://www.nucleodoconhecimento.com.br/ciencia-da-computacao/analise-forense)

A melhor ferramenta de um hacker – NMAP
Assista a este vídeo para saber mais sobre uma das ferramentas amplamente utilizadas no arsenal de um hacker: NMAP. Abreviação de Network Mapper, trata-se de uma ferramenta de código aberto projetada para explorar redes, descobrir dispositivos, serviços e vulnerabilidades, fornecendo aos hackers uma visão detalhada da infraestrutura de rede de um alvo.
[Mais](https://www.youtube.com/embed/Z0ICyS9g958?si=wJd7djgx2Oe2UhC8)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

GOODRICH, M. T.; TAMASSIA, R. Introdução à segurança de computadores. Tradução
de Maria Lúcia Blanck Lisbôa. Revisão técnica de Raul Fernando Weber. Porto Alegre:
Bookman, 2013.

MORAES, A. F. Segurança em redes: fundamentos. São Paulo: Érica, 2010.

Banco de imagens Shutterstock.
SAGAH, 2024.

