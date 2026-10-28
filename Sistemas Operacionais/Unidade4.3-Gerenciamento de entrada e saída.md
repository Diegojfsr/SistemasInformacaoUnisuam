## Apresentação

Você sabia que, dentre as funções de um sistema operacional, o controle dos dispositivos de entrada/saída (E/S) é uma das principais?  

O sistema operacional deve interagir com os dispositivos de E/S por meio de comandos e interrupções e a gerência dos dispositivos de E/S tem relação direta com o hardware utilizado no computador. Como existe uma grande variedade de dispositivos de E/S, também existe uma dificuldade dos desenvolvedores em implementar soluções de fácil gerenciamento.  

Para que os recursos possam ser acessados de maneira segura, os processos não podem acessar diretamente os dispositivos de E/S. Sendo assim, cabe ao sistema operacional, por meio das chamadas de sistema, coordenar a leitura e escrita de dados. O gerenciamento de E/S é segmentado em questões relacionadas ao hardware do computador e questões relacionadas ao software.  

Nesta Unidade de Aprendizagem, você vai conhecer as características de gerenciamento de dispositivos de E/S.  

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir as características de hardware de Entrada e Saída.
- Identificar as características de software de Entrada e Saída.
- Reconhecer o conceito de deadlocks.


## Desafio

Imagine que você é o Analista de Suporte da empresa BaitaTech, que possui um servidor de arquivos utilizando o sistema operacional Linux.

Você está fazendo uma análise na utilização das quotas de disco para cada usuário e, nessa análise, foi possível perceber que o usuário "Roberto" está utilizando bastante o servidor de arquivos e o limite de quota foi excedido.

Você irá para uma reunião de gestão pleitear investimentos em discos para expandir o servidor de arquivos e deseja usar o caso do usuário "Roberto" como exemplo. Para tanto, você terá que redirecionar o comando que mostra a quota excedida para um periférico de saída, que é a impressora, para apresentar na reunião essa informação.

Diante do exposto, como você resolveria esse problema? Qual comando deve usar?

#### Padrão de resposta esperado
Para que seja possível visualizar a quota excedida no Linux, deve-se utilizar o seguinte comando:

```
# quota -v roberto Disk quotas for user roberto (uid 1000): Filesystem blocks quota limit grace files quota limit grace /dev/hda4 10028 12000 13000 6* 5 6.

Note que o “*” asterisco ao lado do número 6 indica que a quota foi ultrapassada.

Para que o resultado desse comando seja encaminhado para o dispositivo de saída impressora, deverá ser executado o seguinte comando: # quota -v roberto > /dev/lp0.

O dispositivo “/dev/lp0” é a identificação da impressora para o sistema operacional Linux e pode variar. O caractere “>” inserido no comando indica que a saída (resultado) do comando será encaminhado para o dispositivo “/dev/lp0”, que é a impressora.
```


####  ✅ Resposta ao desafio:

Como Analista de Suporte da BaitaTech, para solucionar essa demanda e preparar a documentação física para a reunião de gestão, o procedimento envolve verificar a situação do usuário e realizar o redirecionamento da saída para a impressora.
A solução detalhada segue o padrão esperado:
Para que seja possível visualizar a quota excedida no Linux, deve-se utilizar o seguinte comando:
```
quota -v roberto
```

Exemplo de retorno esperado do comando:

```
`Disk quotas for user roberto (uid 1000):` `Filesystem blocks quota limit grace files quota limit grace` `/dev/hda4 10028 12000 13000 6* 5 6`
```

Note que o “ * ” (asterisco) ao lado do número indica que o limite de arquivos ou blocos da quota foi ultrapassado.
Para que o resultado desse comando seja encaminhado diretamente para o dispositivo de saída (impressora), deverá ser executado o seguinte comando:

```
# quota -v roberto > /dev/lp0
```

Detalhes técnicos da operação:
/dev/lp0: É a identificação padrão da primeira porta de impressora (paralela) para o sistema operacional Linux (este valor pode variar para outras interfaces, como /dev/usb/lp0 em impressoras USB modernas).
Caractere >: O operador de redirecionamento de saída instrui o shell a enviar o resultado (stdout) do comando para o arquivo ou dispositivo especificado à direita, em vez de exibi-lo na tela do terminal.

## Infográfico

Gerenciar dispositivos de Entrada e Saída (E/S) é uma das principais funções do Sistema Operacional. No infográfico, a seguir, você poderá visualizar o mapa conceitual do gerenciamento de dispositivos de Entrada/Saída.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/55babe4f-a32c-48fd-9bc2-e377754e7624/82a2fabc-b249-4769-995e-3a04d4372cec.png)


## Conteúdo do Livro

Acompanhe a leitura do capítulo Gerenciamento de Entrada e Saída da obra Sistemas Operacionais, que apresenta as características que envolvem o gerenciamento dos dispositivos de Entrada/Saída de um computador.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/6beb9742-e1f7-44d4-96f2-84cdfce5f36a/57c8341a-9fb6-4218-829b-b98be393a7f2.jpg)


## Dica do Professor

O vídeo apresenta o funcionamento do Gerenciador de Dispositivos do Windows, cujo principal objetivo é fornecer uma interface para a gerência dos dispositivos de entrada e saída do computador. Acompanhe!


## Exercícios

#### Questão 1
O que faz um dispositivo de Entrada/Saída de um computador?
Selecione a resposta:
A. São dispositivos responsáveis pela abstração de um programa que está sendo executado.
B. São os dispositivos responsáveis por armazenar dados de processamento.
C. São dispositivos que permitem a interação entre o computador e o mundo externo.
D. São pequenos programas que trabalham como "subprogramas" independentes de um programa maior, executando alguma tarefa específica.
D. Permite a interação entre o computador e a memória.

✅ A alternativa correta é: C

#### Questão 2
O que é a técnica de pooling?
Selecione a resposta:
A. É uma verificação periódica realizada nas operações de entrada e saída para diminuir a lentidão no processamento.
B. É a interconexão física dos dispositivos de E/S.
C. É a padronização do acesso aos dispositivos.
D. Conjunto de comandos que permite o funcionamento de um dispositivo de entrada e saída.
E. É um tipo de dispositivo que utiliza a interface serial para comunicação.

✅ A alternativa correta é: A

#### Questão 3
Qual dos comandos do linux representa o envio de um arquivo para impressora?
Selecione a resposta:
A. # ls -la administrativo .
B. # cat relatorio.txt > /dev/lp0 .
C. # cat relatorio.txt .
D. # df -h .
E. # ps -aux .

✅ A alternativa correta é: B

##### Questão 4
Qual o nome da interface disponibilizada pelo Windows para instalação de drivers dos dispositivos de entrada e saída?
Selecione a resposta:
A. Gerenciador de tarefas.
B. Área de trabalho.
C. Painel de controle.
D .Gerenciador de dispositivos.
E. Browser.

✅ A alternativa correta é: D

#### Questão 5
Qual a função dos drivers de dispositivos de entrada e saída?
Selecione a resposta:
A. Encerrar os processos que estejam ocupando muita memória.
B. Traduzir a linguagem de máquina do dispositivo para linguagem do sistema operacional.
C. Os drivers controlam o escalonamento de processos.
D. Os drivers permitem a transferência de dados diretamente entre o processador e a memória.
E. Os drivers implementam funções genéricas de serviços de entrada e saída.

✅ A alternativa correta é: B

## Na prática

Marcos Paulo é o analista de suporte de TI da empresa BonaTech e sempre foi usuário do sistema operacional Linux. No entanto, em função da compatibilidade dos sistemas utilizados na empresa, resolveu instalar o Windows 10 no seu notebook.

##### Veja como a instalação de uma ferramenta de gerenciamento de entrada e saída de dispositivos otimiza a utilização de um novo sistema operacional.

Após realizar a instalação do Windows 10, Marcos Paulo notou que alguns drivers de dispositivos não foram instalados, diferentemente do que acontecia quando utilizava o sistema operacional Linux.

Ele então descobriu que existem softwares para Windows que fazem uma varredura no sistema operacional à procura de dispositivos que não possuem os drivers corretamente instalados.

Ele realizou o download do software Slim Drivers, que é gratuito.

Após instalar o software, o próprio software faz uma varredura no sistema e lista os drivers que necessitam ser instalados.

Na lista de dispositivos que o software identificou estarem sem os drivers, basta solicitar o download, que o Slim Drivers busca na internet o driver mais atualizado para o dispositivo.

Com a utilização desse software, o Marcos Paulo, que não tem muita experiência com o sistema operacional Windows, conseguiu instalar corretamente todos os dispositivos do computador.


## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Como funcionam os dispositivos de entrada e saída
Os dispositivos de entrada e saída podem ser divididos em um modo genérico como dispositivos de bloco e caractere.
[Mais](https://www.devmedia.com.br/como-funcionam-os-dispositivos-de-entrada-e-saida/28275)

Gerenciamento de Dispositivos de Entrada e Saída no Linux e Windows
Amplie seus conhecimentos sobre o gerenciamento de dispositivos de entrada e saída no Linux e Windows, sendo que para cada dispositivo existe um driver responsável pelo elo entre o sistema operacional e o dispositivo.
[Mais](https://www.youtube.com/embed/62x8s3n9U5A)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

TANENBAUM, Andrew S. Sistemas operacionais modernos. São Paulo: Pearson Prentice
Hall, 3ª Edição, 2009.

TANENBAUM, A. S.; WOODHULL, A. S. Sistemas operacionais: projeto e implementação. 3.
ed. Porto Alegre: Bookman, 2008.

OLIVEIRA, R. S.; CARISSIMI, A. S.; TOSCANI, S. S. Sistemas Operacionais. v. 11. Série Livros
Didáticos Informática UFRGS. Bookman Editora, 2009.

TECHNET. Visão geral do Gerenciador de Dispositivos. Disponível em:
https://technet.microsoft.com/pt-br/library/cc725876(v=ws.11).aspx. Acesso em Maio de
2017.

TECHTUDO. Como usar o Slim Drivers e manter seu PC sempre atualizado. Disponível em:
http://www.techtudo.com.br/dicas-e-tutoriais/noticia/2015/03/como-usar-o-slim-drivers-e-
manter-seu-pc-sempre-atualizado.html. Acesso em Maio de 2017.

COMANDOS LINUX. COM. Lista Rápida de Comandos para Linux/UNIX. Disponível em:
http://www.comandoslinux.com/. Acesso em Maio de 2017.

Banco de imagens Shutterstock.
SAGAH, 2017.


