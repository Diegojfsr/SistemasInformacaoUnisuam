## Apresentação

O envio e o recebimento de mensagens sigilosas são uma necessidade. Em função disso, a criptografia se tornou uma ferramenta essencial com a finalidade de que apenas o emissor e o receptor tenham acesso a tais informações. Nas agências espaciais de inteligência e no período de guerras, há exemplos de utilização da criptografia para evitar que mensagens importantes fossem interceptadas e lidas.

Além da criptografia tradicional, conhecida como "criptografia simétrica", a criptografia assimétrica surge como uma abordagem inovadora e eficaz para proteger a comunicação sensível. Diferentemente da criptografia simétrica, em que o remetente e o destinatário compartilham uma chave comum para codificar e decodificar mensagens, a criptografia assimétrica opera com um par de chaves distintas: uma chave pública e uma chave privada.

Esse método de criptografia permite que qualquer pessoa possa criptografar uma mensagem usando a chave pública do destinatário e garante que apenas o destinatário possa descriptografá-la – usando sua chave privada correspondente.  

Nesta Unidade de Aprendizagem, você vai aprender o que é a criptografia assimétrica, suas características e seus tipos. Vai identificar suas propriedades únicas e examinar exemplos práticos em diferentes contextos. Com esse estudo, você vai desenvolver um entendimento sólido sobre a criptografia assimétrica e conhecer sua aplicabilidade em cenários reais de segurança de dados.  

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir criptografia assimétrica.
- Descrever criptografia assimétrica.
- Explicar os diferentes tipos de criptografia assimétrica.


## Desafio

A criptografia é uma técnica de segurança da informação que visa proteger dados sensíveis durante a transmissão e o armazenamento de dados. Um dos métodos mais antigos e conhecidos é a cifra de César, que consiste em deslocar cada letra do texto original por um número fixo de posições no alfabeto.

No entanto, o algoritmo inicialmente proposto apresentava algumas limitações. Por exemplo, ele não tratava adequadamente espaços, pontuações e caracteres especiais, além de não fornecer uma funcionalidade para decifrar o texto. Portanto, foi necessário aprimorar o algoritmo para garantir sua eficácia e usabilidade.

Sobre esse assunto, considere a situação a seguir:

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/b9fc963d-82a6-4385-a134-e8b2497fa317/ab849021-fb02-41e8-8772-27f83e854343.png)

  
Sendo assim, responda:
Como você realizaria essa alteração? Escreva um código que responda a essa modificação corretamente.

####  ✅ Resposta ao desafio:


Para melhorar o algoritmo, é necessário corrigir algumas limitações da implementação original:

Permitir a cifragem e decifragem do texto.
Tratar corretamente letras maiúsculas e minúsculas.
Manter espaços, números e caracteres especiais inalterados.
Utilizar uma lógica mais simples e eficiente com o operador módulo (%).
Evitar erros quando a chave ultrapassar o tamanho do alfabeto.
Código Melhorado em C

``` c
#include <stdio.h>

#include <string.h>

#include <ctype.h>

void cifraCesar(char texto[], int chave) {

    int i;

    for (i = 0; texto[i] != '\0'; i++) {

        if (texto[i] >= 'A' && texto[i] <= 'Z') {

            texto[i] = ((texto[i] - 'A' + chave) % 26) + 'A';

        }

        else if (texto[i] >= 'a' && texto[i] <= 'z') {

            texto[i] = ((texto[i] - 'a' + chave) % 26) + 'a';

        }

    }

}

void decifraCesar(char texto[], int chave) {

    int i;

    for (i = 0; texto[i] != '\0'; i++) {

        if (texto[i] >= 'A' && texto[i] <= 'Z') {

            texto[i] = ((texto[i] - 'A' - chave + 26) % 26) + 'A';

        }

        else if (texto[i] >= 'a' && texto[i] <= 'z') {

            texto[i] = ((texto[i] - 'a' - chave + 26) % 26) + 'a';

        }

    }

}

int main() {

    char texto[100] = "Adriana, teste da cifra de Cesar!";

    int chave = 3;

    printf("Texto original: %s\n", texto);

    cifraCesar(texto, chave);

    printf("Texto cifrado: %s\n", texto);

    decifraCesar(texto, chave);

    printf("Texto decifrado: %s\n", texto);

    return 0;

}
```

Saída Esperada
``` bash
Texto original: Adriana, teste da cifra de Cesar!
Texto cifrado: Dguldqd, whvwh gd fliud gh Fhvdu!
Texto decifrado: Adriana, teste da cifra de Cesar!
```

Explicação

A solução utiliza a Cifra de César para deslocar as letras do alfabeto pela quantidade definida na chave. O algoritmo de cifragem soma a chave ao caractere, enquanto o de decifragem subtrai a mesma chave. Espaços, números e caracteres especiais permanecem inalterados, tornando a aplicação mais robusta e adequada para uso prático. Além disso, o uso do operador % 26 garante o retorno ao início do alfabeto quando o deslocamento ultrapassa a letra "Z" ou "z".


#### Sua atividade foi entregue com sucesso!
Confira abaixo os detalhes do seu envio. Uma cópia deste recibo também será enviada para o seu e-mail.

ID do envio: 20837974
Atividade enviada por: Diego Jefferson da Silva Rosa
Data e hora do envio: 29/09/26 - 19:43
Disciplina: Fundamentos de Segurança da Informação [TTEC0023] (2026-2-TTEC0023-TRIMESTRAL-EAD0301T)
Tarefa: Desafio
Tentativa: 1 de 1


## Infográfico

Atualmente, a informação está cada vez mais digital. Por isso, é importante que esta seja protegida, de modo a evitar sua interceptação por pessoas mal-intencionadas. Assim, a criptografia é de suma importância nesse contexto.

Com o aumento das ameaças cibernéticas e a crescente sofisticação dos ataques, a implementação de algoritmos criptográficos robustos torna-se ainda mais crucial para garantir a confidencialidade e a autenticidade das informações em um mundo digital cada vez mais interconectado.

A digitalização da informação é uma realidade inevitável, impulsionada pela constante evolução da tecnologia. Essa mudança tem trazido inúmeros benefícios, mas também expõe dados sensíveis a riscos cada vez maiores de interceptação por indivíduos mal-intencionados. Nesse cenário, a criptografia surge como uma ferramenta para proteger a integridade, a confidencialidade e a autenticidade das informações digitais.

Neste Infográfico, acompanhe as principais características da criptografia assimétrica e simétrica, bem como a combinação de ambas.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/0a47dde6-050c-4a33-aac4-736ef9761b23/fdb71c52-9f45-404b-8128-93e827c93f55.png)


## Conteúdo do Livro

A criptografia assimétrica representa uma evolução significativa na segurança da informação e introduz um paradigma em que duas chaves distintas, uma pública e outra privada, são empregadas para cifrar e decifrar dados.  

Esse método oferece uma camada adicional de segurança, pois a chave privada, mantida em posse exclusiva do destinatário, garante que apenas ele possa decifrar as mensagens criptografadas com sua chave pública correspondente. Além disso, a criptografia assimétrica é amplamente utilizada em cenários em que a autenticidade e a integridade dos dados são críticas, como em transações financeiras on-line e na assinatura digital de documentos eletrônicos.  

A interoperabilidade e a escalabilidade da criptografia assimétrica a tornam uma escolha preferencial em sistemas distribuídos e redes de comunicação de grande escala. A capacidade de cada usuário ter seu próprio par de chaves pública e privada permite uma troca segura de informações em ambientes nos quais os participantes não confiam totalmente uns nos outros.  

No capítulo Criptografia assimétrica, base teórica desta Unidade de Aprendizagem, você vai aprofundar seus conhecimentos sobre a criptografia assimétrica, sua funcionalidade e seus tipos.  

Boa leitura.​​​​​​​
​​​

## Dica do Professor

A criptografia assimétrica vai além da simples proteção da informação durante a transmissão, pois ela possibilita também a verificação da autenticidade dos dados. Por meio da assinatura digital, é possível confirmar se a informação foi realmente gerada pela entidade que alega tê-la produzido, oferecendo, assim, uma camada adicional de confiança e segurança.

Com a criptografia assimétrica, além de resguardar a informação na sua transmissão, é possível comprovar a autenticidade, ou seja, verificar se realmente foi criada por quem diz ter feito isso. Para tanto, utiliza-se a assinatura digital, em que a verificação é feita com o uso de chaves.

Nesta Dica do Professor, você vai compreender como o algoritmo de criptografia assimétrica pode autenticar o remetente de determinada mensagem.



## Exercícios


#### Questão 1
A escolha do método de criptografia adequado é importante para a proteção de dados sensíveis. Uma das abordagens mais comuns é aquela em que a chave utilizada tanto para cifrar quanto para decifrar os dados é compartilhada entre o remetente e o destinatário.
Assinale a alternativa que indica o tipo de criptografia na qual a chave para cifrar e decifrar é compartilhada entre remetente e destinatário.
Selecione a resposta:
a. Criptografia assimétrica.
b. Criptografia WEP.
c. Criptografia quântica.
d. Criptografia simétrica.
e. Criptografia RSA.

✅ A alternativa correta é: D


#### Questão 2
Na criptografia assimétrica, o modo de utilização das chaves difere da abordagem simétrica, pois envolve o uso de duas chaves distintas: uma chave pública e uma chave privada. Essas chaves são utilizadas de maneira específica.
Marque a alternativa que corresponde ao modo de utilização das chaves na criptografia assimétrica.
Selecione a resposta:
a. Usa-se uma única chave para encriptar e decriptar mensagens.
b. Apenas a chave de encriptação é compartilhada.
c. Não existe relação entre as duas chaves, e é isso que garante a segurança de tal tipo de criptografia.
d. Por ser de conhecimento de todos, a chave pública só pode ser usada uma única vez.
e. Se o titular perder sua chave privada, pode utilizar a chave pública para decriptar as mensagens.

✅ A alternativa correta é: B

#### Questão 3
A criptografia assimétrica é uma abordagem inovadora na proteção de dados sensíveis e emprega um par de chaves distintas para cifrar e decifrar informações. Essas chaves, conhecidas como "chave pública" e "chave privada", têm funções complementares na garantia da segurança e autenticidade das comunicações digitais.
No contexto da criptografia assimétrica, uma variedade de algoritmos pode ser empregada para garantir a segurança e a eficácia do processo de cifragem e decifragem.
Marque a alternativa que corresponde aos algoritmos usados na criptografia assimétrica.
Selecione a resposta:
a. PKI e DES.
b. DSS e RSA.
c. TCP e MD5.
d. DMZ e Imap.
e. AES e Raid.

✅ A alternativa correta é: B

#### Questão 4
A criptografia assimétrica, também conhecida como "criptografia de chave pública", é fundamentada em princípios matemáticos complexos que garantem a segurança da comunicação digital. Essa abordagem utiliza um par de chaves distintas: uma chave pública e uma chave privada.
Analise o seguinte contexto:
"O usuário Antônio quer enviar um e-mail para Ana de modo seguro. Para isso, ele utilizará a criptografia assimétrica a fim de cifrar o conteúdo da mensagem".
Marque a alternativa que descreve o processo a ser efetuado por ambos a fim de realizar a operação.
Selecione a resposta:
a. Antônio deve criptografar a mensagem utilizando a chave pública dele. Por sua vez, Ana precisa descriptografar a mensagem empregando a chave pública de Antônio.
b. Antônio deve criptografar a mensagem utilizando a chave privada dele. E Ana precisa descriptografar a mensagem usando a chave privada de Antônio.
c. Antônio deve criptografar a mensagem utilizando a chave privada de Ana. E Ana precisa descriptografar a mensagem usando a chave privada dela.
d. Antônio deve criptografar a mensagem utilizando a chave pública de Ana. Por sua vez, Ana precisa descriptografar a mensagem usando a chave pública dela.
e. Antônio deve criptografar a mensagem utilizando a chave pública de Ana. Por sua vez, Ana deve descriptografar a mensagem usando a chave privada dela.

✅ A alternativa correta é: E

#### Questão 5
Compreender os fundamentos da criptografia assimétrica é essencial para entender como ela se tornou uma peça-chave na segurança da informação. Ao contrário da criptografia simétrica, que depende de uma única chave compartilhada entre remetente e destinatário, a criptografia assimétrica opera com um par de chaves distintas: uma chave pública, conhecida por todos, e uma chave privada, mantida em segredo pelo proprietário.
Considere uma empresa de tecnologia que está planejando implementar um sistema de comunicação seguro para trocar informações confidenciais entre os funcionários. Eles consideram a utilização da criptografia assimétrica para garantir a confidencialidade e a integridade das mensagens.
Os desenvolvedores propuseram o seguinte cenário para o sistema:
• Cada funcionário terá um par de chaves pública e privada gerado exclusivamente para ele.
• As chaves públicas serão armazenadas em um diretório centralizado acessível a todos os funcionários.
• Quando um funcionário deseja enviar uma mensagem para outro funcionário, ele vai cifrar a mensagem usando a chave pública do destinatário.
• O destinatário vai poder decifrar a mensagem utilizando a chave privada correspondente dele.
Com base nesse cenário, marque a alternativa correta que descreve uma vantagem da utilização da criptografia assimétrica nesse sistema de comunicação.
Selecione a resposta:
a. Garante que apenas o destinatário possa decifrar a mensagem.
b. Dificulta a distribuição segura das chaves entre os funcionários.
c. Oferece uma velocidade superior na cifragem e decifragem das mensagens.
d. Requer menos recursos computacionais em comparação com a criptografia simétrica.
e. Permite que múltiplos destinatários possam decifrar a mensagem, se desejado.

✅ A alternativa correta é: A

## Na prática

A criptografia é uma disciplina fundamental na segurança da informação e está voltada para garantir a confidencialidade, a integridade e a autenticidade dos dados em comunicações digitais. Seu objetivo é proteger as informações contra acessos não autorizados e garantir que apenas as partes autorizadas possam acessá-las.

A criptografia é amplamente utilizada em uma variedade de contextos, desde comunicações pessoais até transações financeiras e governamentais, situações em que a privacidade e a segurança dos dados são essenciais.

Neste Na Prática, veja como o aplicativo de mensagens WhatsApp tem utilizado a criptografia para assegurar a privacidade dos usuários.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/bb0ca27d-4716-4f1f-8b3b-98386ce65f9c/f8e8ebc8-54fe-4563-9a1e-905556ad30cf.png)


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

O que é criptografia de ponta a ponta?
Neste vídeo, veja o conceito e a importância da criptografia de ponta a ponta. Essa técnica de segurança é fundamental para proteger a privacidade das comunicações digitais e garantir que apenas o remetente e o destinatário possam acessar o conteúdo das mensagens.
[Mais](https://www.youtube.com/embed/sKqcwh5OlKY)

Entendendo a criptografia assimétrica
Este vídeo apresenta uma base conceitual e aplicações da criptografia assimétrica e elucida os conceitos de chave privada e chave pública. Na criptografia assimétrica, a chave privada é mantida em segredo pelo usuário e é usada para decifrar mensagens criptografadas com a chave pública correspondente. Por outro lado, a chave pública é compartilhada livremente e é usada para cifrar mensagens destinadas ao proprietário da chave privada.
[Mais](https://www.youtube.com/embed/UEymC7VE724?si=m2bSKtIX1hO2772-)

Blockchain na gestão do acervo acadêmico de instituições federais de ensino superior. uma proposta de implementação
Esta dissertação concebeu e colocou em prática uma aplicação que faz uso da blockchain para garantir a permanência, a integridade e a acessibilidade de um recurso do acervo acadêmico originado de uma instituição de ensino superior.
[Mais](http://www.repositorio.ufjf.br/jspui/bitstream/ufjf/16139/1/thiagomarquesfernandesdemello.pdf)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

AMARO, G. Criptografia simétrica e criptografia de chaves públicas: vantagens e desvantagens. Revista Negócios e Tecnologia da Informação, v. 2, n. 1, p. 1-11, 2007. Disponível em: http://publica.fesppr.br/index.php/rnti/issue/download/4/33. Acesso em: 10 ago. 2018.

BOY, M. Entenda como um ransomware funciona e como se prevenir. Perallis, 2018. Disponível em: https://www.perallis.com/news/entenda-como-um-ransomware-funciona-e-como-se-prevenir. Acesso em: 10 ago. 2018.

CURRY, I. An introduction to cryptography. Addison, TX: Entrust Technologies, 1997.

WIKIWAND. Cifra de substituição. Wikiwand, [20--]. Disponível em: http://www.wikiwand.com/pt/Cifra_de_substituição. Acesso em: 10 ago. 2018.

Bancos gratuitos de imagens e Shutterstock.
SAGAH, 2024
