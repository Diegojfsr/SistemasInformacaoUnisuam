## Apresentação

Você sabia que os problemas relacionados à memória impactam diretamente na performance das aplicações utilizadas pelos usuários? O gerenciador de memória do sistema operacional tem como função manter o controle de quais partes da memória estão em uso e quais não estão, alocando memória aos processos, quando necessário, e liberando-a quando os processos forem encerrados. Além disso, o gerenciador de memória coordena a troca de processos entre a memória e o disco (quando a memória principal não é suficiente).  

Nesta Unidade de Aprendizagem, você vai conhecer os diferentes modos de gerenciar as atividades da memória e suas características, além de identificar a hierarquia de armazenamento de um computador.  

Bons estudos.

#### Ao final desta Unidade de Aprendizagem, você deve apresentar os seguintes aprendizados:

- Definir a hierarquia de armazenamento de um computador.
- Identificar os modos de gerenciamento de memória e suas características.
- Reconhecer o funcionamento da memória virtual.


## Desafio

Marcos Paulo é o Analista de Tecnologia da Informação da empresa BonaTech. Suas atribuições variam desde o suporte aos usuários até a configuração e manutenção de servidores e ativos de rede. Além disso, a empresa possui um pequeno data center que hospeda um servidor da aplicação de e-commerce da BonaTech.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/bc84110a-b7d1-4f47-8562-e5a2d0d3e022/1b4f6f95-44ec-451c-92da-a4b83b645f1d.png)

Marcos Paulo não tem muita familiaridade com o Linux, mas está desconfiado de que essa lentidão está relacionada com a quantidade de memória RAM. Como ele não era o funcionário na época em que o servidor foi instalado, ele não sabe qual a quantidade de memória instalada no equipamento.

Diante do exposto, Marcos necessita saber a quantidade de memória instalada e a quantidade de memória utilizada na hora de pico. Como ele pode solucionar esse problema?

#### Padrão de resposta esperado

Inicialmente, Marcos Paulo deverá observar os relatórios do sistema para identificar o horário em que mais clientes estão acessando o e-commerce. Nesse horário, ele poderá acessar o servidor remotamente e rodar o comando “cat /proc/meminfo” .

Esse comando irá apresentar as informações relacionadas à memória instalada no computador. O resultado do comando deverá ser uma tela parecida com a figura abaixo:

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/9257d224-86bb-41c2-926e-71ff78790085/33fd6c52-822f-4ea6-b3a1-66729046dad4.png)

Observando no retorno do comando, as duas primeiras linhas fornecem a quantidade de memória total e a quantidade de memória livre.

É recomendável que fique livre no mínimo 20% do total da memória para que não ocorram travamentos.


####  ✅ Resposta ao desafio:

Para solucionar o problema de Marcos Paulo no servidor Linux (Ubuntu), ele pode utilizar comandos específicos do sistema para verificar tanto a memória total instalada quanto o uso de memória em tempo real ou durante o horário de pico.

Aqui está a solução detalhada que ele pode aplicar:

1.Identificação do Horário de Pico
Inicialmente, Marcos deve analisar os logs de acesso da aplicação de e-commerce ou os relatórios do servidor web (como Nginx ou Apache) para identificar o horário de pico exato em que há maior volume de acessos dos clientes.

2.Verificação da Memória Instalada e Utilizada
No horário de pico, Marcos deve acessar o servidor remotamente (via SSH) e utilizar comandos do Linux para inspecionar os recursos de hardware:
Comando cat /proc/meminfo:
Permite visualizar informações detalhadas sobre o uso atual da memória do sistema. Conforme o exemplo fornecido:
MemTotal: Indica a quantidade total de memória RAM instalada no equipamento (ex: 8196912 kB, que equivale a aproximadamente 8 GB).
MemFree / Buffers / Cached: Mostram como a memória está livre, em buffer ou em cache naquele instante.
SwapTotal / SwapFree: Indicam a quantidade de memória de troca (swap) configurada e disponível.
Comando free -h (Alternativa prática):
Para uma visualização mais rápida e amigável em formato legível por humanos (megabytes ou gigabytes), Marcos pode executar o comando free -h, que exibe imediatamente o total de RAM, a quantidade usada, livre e o status do Swap.


## Infográfico

A técnica de swapping com partições variáveis permite que, a cada instante de tempo, a memória possa alocar e desalocar processos cujos tamanhos são diferentes. O número e o tamanho das partições na memória variam conforme os processos são alocados/desalocados.

Acompanhe, no próximo infográfico, os 7 instantes de tempo e o processo de swapping com partições variáveis.

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/d9d681af-29ab-43c2-b0f1-e0f8db1e509e/3d110e42-6a93-4758-8b14-1a1d1b5cd62e.gif)



## Conteúdo do Livro

O capítulo Gerência de Memória, da obra "Sistemas Operacionais", apresenta os diferentes modos de gerenciar as atividades da memória de um computador. Acompanhe!

![Descrição da imagem não disponível](https://statics-marketplace.plataforma.grupoa.education/sagah/ac05fb6d-2637-411b-876e-b434980e988f/969defb5-5272-43bc-a74a-70ff44e132a1.jpg)



## Dica do Professor

O vídeo seguinte apresenta o funcionamento da memória virtual, bem como mostra um exemplo de configuração da memória virtual no sistema operacional Windows.


## Exercícios

#### Questão 1
Qual a função dos registradores que ficam localizados dentro da CPU?
Selecione a resposta:
A. Acelerar a execução dos programas e processos trabalhando em conjunto com o processador.
B. Aumentar a capacidade de memória simulando memória no disco rígido.
C. Armazenar informações do processo que está sendo executado.
D. Armazenar os dados permanentemente no sistema, sem a necessidade de energia elétrica.
E. Armazenar informações do aplicativo Java que está sendo executado.

✅ A alternativa correta é: C


#### Questão 2
Qual a característica do gerenciamento de memória baseado na técnica de monoprogramação?
Selecione a resposta:
A. Essa técnica consiste em ter somente um processo na memória durante toda sua execução.
B. Esta técnica consiste na execução de múltiplos processos aumentando a utilização da CPU.
C. Essa técnica consiste em dividir a memória em partições de tamanho fixo.
D. Essa técnica consiste em dividir a memória em partições com tamanhos variáveis.
E. Consiste na divisão da memória em unidades de alocação com um bit indicando se a unidade está livre ou ocupada.

✅ A alternativa correta é: A

#### Questão 3
O que é a memória Virtual?
Selecione a resposta:
A. É uma técnica utilizada para simular memória cache no pendrive, aumentando a capacidade de memória do computador.
B. É uma memória somente de leitura, também conhecida como memória ROM.
C. É uma técnica utilizada para dividir o disco em partições fixas que funcionam como memória RAM.
D. É uma técnica que aloca 50% do espaço do disco rígido para simular memória RAM.
E. É uma técnica utilizada para simular memória RAM no disco rígido, aumentando a capacidade de memória do computador.

✅ A alternativa correta é: E

#### Questão 4
Qual comando do linux permite verificar a quantidade de memória RAM instalada no computador?
Selecione a resposta:
A. ls -la.
B. Quota.
C. Netstat.
D. Cat/proc/meminfo
E. Kill.

✅ A alternativa correta é: D

#### Questão 5
Qual aplicativo do Windows permite acompanhar a quantidade de memória alocada por processo?
Selecione a resposta:
A.Desfragmentador de disco.
B. Scandisk.
C. Gerenciador de Tarefas.
D. Painel de controle.
E. Barra de tarefas.

✅ A alternativa correta é: C


## Na prática

Características como quantidade de memória disponível, tempo de acesso e custo, são fundamentais para o funcionamento adequado do sistema operacional. O ideal é que se tenha sempre uma grande quantidade de memória para evitar problemas na performance, porém o custo da memória é elevado.

Um grande desafio na relação custo-benefício para compra de memória é tentar equilibrar o custo por bit armazenado, a velocidade de acesso da memória, e a capacidade.

Acompanhe como problemas de memória podem atrapalhar o desempenho do computador impactando na produtividade.

João Antônio é um funcionário do setor de compras de uma empresa de tecnologia e utiliza um computador com 2 gigabytes de memória durante 8 horas diárias para realizar suas atividades na empresa. Ele teve alguns problemas como lentidão no computador e algumas falhas aleatórias que fazem o sistema operacional reinicializar. Um colega de faculdade de João Antônio disse a ele que esse pode ser um problema relacionado à memória do computador.

#### VEJA COMO JOÃO ANTÔNIO PESQUISOU E RESOLVEU REALIZAR UM DIAGNÓSTICO DE MEMÓRIA DO WINDOWS, SEGUINDO OS SEGUINTES PASSOS:

1.Acesse o Painel de controle do Windows – Opção Ferramentas Administrativas.
2.Na janela de Ferramentas Administrativas, acesse a opção Diagnóstico de Memória do Windows.
3.Aparecerá uma janela pequena cujo título é "Diagnóstico de Memória do Windows", nessa janela, escolha a opção "Reiniciar agora e verificar se há problemas
4.Depois de o computador reiniciar, será realizado pelo sistema operacional o diagnóstico de memória do computador. É possível escolher diferentes tipos de testes.
5.Uma vez que o diagnóstico de memória estiver completo, o sistema operacional irá reiniciar a máquina automaticamente. Se não houver nenhum erro, o Windows exibirá uma mensagem informando isso, assim que iniciar.
Sendo assim, ele solicitou ao setor responsável a compra de um módulo de 2 gigabytes de memória para melhorar a performance do computador.

## Saiba mais

Para ampliar o seu conhecimento a respeito desse assunto, veja abaixo as sugestões do professor:

Gerência de Memória. [Mais](https://www.youtube.com/watch?v=Q2yRR1SmdK4)

Outra função do sistema operacional é controlar a gerência de memória. No próximo vídeo, você poderá ampliar seus conhecimentos sobre o tema. [Mais](https://www.youtube.com/embed/5vI-P1j4uJs)

Amplie seus conhecimentos sobre as técnicas de gerenciamento de memória, acessando a próxima dica de leitura. [Mais](https://www.academia.edu/7265703/Relatorio_03_Gerenciamento_de_Memoria)


## REFERÊNCIAS BIBLIOGRÁFICAS E CRÉDITOS DE IMAGENS

TANENBAUM, Andrew S. Sistemas operacionais modernos. São Paulo: Pearson Prentice
Hall, 3ª Edição, 2009.

TANENBAUM, A. S.; WOODHULL, A. S. Sistemas operacionais: projeto e implementação. 3.
ed. Porto Alegre: Bookman, 2008.

MACHADO, F. B., & Maia, L. P. Arquitetura de sistemas operacionais (Vol. 4). LTC. 2004.
SITE VIVA O LINUX. Obtendo informações sobre seu processador e memória RAM.

Disponível em: https://www.vivaolinux.com.br/dica/Obtendo-informacoes-sobre-seu-
processador-e-memoria-RAM. Acesso em Maio de 2017.

Banco de imagens Shutterstock.
SAGAH, 2017.
