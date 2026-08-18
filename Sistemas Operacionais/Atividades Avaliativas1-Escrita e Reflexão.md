Professor: Carlos Alberto de Oliveira
Disciplina: Sistemas Operacionais [TTEC0051]

## Contextualização
A unidade um de nossa disciplina, faz menção em alguns momentos sobre um
componente de extrema importância para o funcionamento do sistema, que é o seu
núcleo(kernel). Vamos aprofundar nossos conhecimentos neste componente muito
importante do sistema operacional.

## Proposta de Trabalho
Estudo sobre o Núcleo do Sistema Operacional (Kernel)
#### Tema:
O núcleo do sistema operacional (kernel) é a parte central do sistema que gerencia
os recursos do hardware e oferece serviços básicos aos demais componentes e
aplicações. O objetivo deste trabalho é realizar um estudo detalhado sobre o kernel,
abordando os tipos existentes (monolítico, microkernel, híbrido, exokernel) e explorar
o kernel dos principais sistemas operacionais da atualidade: Windows, Linux, MacOS
e Android. O trabalho deve apresentar uma comparação entre esses sistemas,
destacando suas características, vantagens e desvantagens.
#### Objetivo:
Desenvolver um trabalho acadêmico que analise o papel do kernel em sistemas
operacionais, destacando suas diferentes arquiteturas e especificidades nos
principais sistemas operacionais utilizados atualmente. O trabalho deverá também
abordar as funcionalidades e a evolução do kernel ao longo do tempo

#### Estrutura do Trabalho:
O trabalho deverá ser desenvolvido seguindo as normas da ABNT (Associação
Brasileira de Normas Técnicas) e conter as seguintes seções:

1.Capa: Incluir o nome da instituição, curso, nome do aluno, título do trabalho,
nome do orientador, local e ano.

2.Folha de Rosto: Repetir as informações da capa e adicionar a finalidade do
trabalho e o nome da disciplina.
Sumário: Listar todas as seções e subseções do trabalho com a numeração
das páginas.

4.Introdução: Apresentação geral do tema, justificativa da escolha do tema,
objetivos do trabalho e estrutura do documento.

5.Revisão de Literatura: Descrição detalhada sobre o que é o kernel, seus tipos
(monolítico, microkernel, híbrido, exokernel), e uma breve história e evolução
do kernel nos sistemas operacionais.

6.Desenvolvimento:
a) Descrição do Kernel nos Principais Sistemas Operacionais:
▪ Windows: Características do kernel NT.
▪ Linux: Estrutura do kernel monolítico modular.
▪ MacOS: Arquitetura do kernel XNU.
▪ Android: Kernel baseado em Linux e suas modificações específicas.
b) Comparação entre os diferentes kernels:
▪ Análise comparativa das arquiteturas, desempenho, segurança e
adaptabilidade dos kernels mencionados

7.Referências: Listar todas as fontes bibliográficas consultadas e citadas no
trabalho, seguindo as normas da ABNT. 

## Regras e Normas ABNT:
a) Formatação Geral:
• Fonte Times New Roman ou Arial, tamanho 12, com espaçamento 1,5 entre
linhas.
• Margens: 3 cm (superior e esquerda) e 2 cm (inferior e direita).
• Alinhamento justificado.
• Sumário.
• Citações diretas curtas (até três linhas) devem ser inseridas no parágrafo,
entre aspas duplas. Citações diretas longas (mais de três linhas) devem ser
destacadas com recuo de 4 cm da margem esquerda, sem aspas, com fonte
tamanho 10.
• Parágrafos com recuo de 1,25 cm na primeira linha.

b) Elementos Pré-Textuais
• Introdução, Desenvolvimento e Conclusão conforme detalhado nas
instruções de construção do trabalho.

c) Elementos Pós-Textuais
• Referências: Citar todas as fontes seguindo o padrão autor-data, conforme as
normas ABNT.
• Anexos: Caso necessário, incluir anexos para informações adicionais.

## Avaliação
A avaliação do trabalho será baseada nos seguintes critérios:
• Conteúdo e Originalidade: Profundidade da análise, pertinência das
informações, e demonstração de compreensão do tema.
• Organização e Estrutura: Coerência e coesão na organização das ideias,
clareza na exposição do conteúdo, e correta divisão em seções.
• Conformidade com as Normas da ABNT: Correta aplicação das normas de
formatação, citações e referências.
• Apresentação e Linguagem: Uso adequado da linguagem acadêmica,
correção gramatical e ortográfica, e apresentação visual do trabalho.


## Links de apoio:

#### 1.Núcleo do Sistema Operacional e seus Tipos
O foco aqui é a diferenciação teórica entre as arquiteturas de núcleo.
Arquiteturas de Sistemas Operacionais: Monolítica, Microkernel e Híbrida
Resumo: Analisa detalhadamente as diferenças, vantagens e desvantagens de
cada modelo.
https://www.hostragons.com/pt/blog/arquiteturas-de-sistemasoperacionais-microkernel-monolitico-e-estruturas-hibridas/
Kernel Monolítico, Híbrido e MicroKernel: O que são?
Resumo: Um guia visual e explicativo sobre como o núcleo gerencia o
hardware e os serviços de usuário.
https://linuxuniverse.com.br/linux/kernel-mono-hib-micro
Entendendo a Estrutura de um Sistema Operacional
Resumo: Explora a interface de chamadas de sistema (system calls) e como o
kernel se organiza em camadas.
https://dev.to/nfo94/entendendo-a-estrutura-de-um-sistema-operacional-i1n

#### 2.Evolução do Kernel nos Sistemas Operacionais
Artigos que traçam a linha do tempo, desde o "bare metal" até os sistemas
modernos.
A Evolução e Classificação da Arquitetura do Kernel
Resumo: Explora a jornada histórica dos núcleos e como as demandas de
performance moldaram os designs atuais.
https://www.allelcoelec.pt/blog/The-Evolution-and-Classification-of-KernelArchitecture.html
O Linux e a Importância do seu Kernel: Uma História de Evolução
Resumo: Foca na evolução específica do kernel Linux, que é a base para o
ensino de SO nos curso de Computação.
https://www.dio.me/articles/sistemas-operacionais-o-linux-e-a-importanciado-seu-kernel-210ff252caf4
História do Desenvolvimento do Núcleo (Kernel)
Resumo: Uma seção detalhada sobre o desenvolvimento histórico, desde os
anos 50 até os sistemas de tempo real.
https://www.researchgate.net/publication/390836794_Historia_dos_Sistemas_Operacionais
Modo usuário versus modo kernel: explicações sobre sistemas
operacionais
Resumo: O modo kernel existe para impedir que aplicativos do usuário
interrompam funções críticas do sistema.
https://www.techtarget.com/searchsoftwarequality/tip/User-mode-vs-kernel-modeOSes-explained

#### 3.Kernel nos Principais Sistemas Operacionais

Material voltado para a aplicação prática no Windows, Linux, macOS e Android.
Arquitetura do Windows: Modo Usuário e Modo Kernel
Resumo: Este artigo explora a estrutura interna do sistema operacional Windows,
detalhando a separação de privilégios entre o modo utilizador e o modo núcleo
(kernel). O texto explica como o sistema protege a integridade dos dados e do
hardware, além de descrever os componentes essenciais como o Executive, o
Microkernel e a Camada de Abstração de Hardware (HAL).
https://didatica.tech/sistemas-operacionais-diferenca-entre-windows-macos-elinux/
Sistemas Operacionais: Diferenças entre Windows, MacOS e Linux
Resumo: Comparação direta entre os núcleos NT, XNU (Darwin) e Monolítico/Modular
do Linux.
https://didatica.tech/sistemas-operacionais-diferenca-entre-windowsmacos-e-linux/
Arquitetura da Plataforma Android: O Kernel Linux no Mobile
Resumo: Guia oficial para desenvolvedores que explica por que o Android utiliza
o kernel Linux e como funciona a HAL.
https://developer.android.com/guide/platform?hl=pt-br

#### Vídeos

https://youtu.be/GxPEyNIAYsQ

#### Regras ABNT
Links de apoio referente de como fazer um trabalho acadêmico de acordo com
a ABNT:

https://www.pucsp.br/sites/default/files/download/biblioteca/2025/manual-para-elaboracaodo-trabalho-academico-com-citacoes-e-referencias-em-padrao-abnt.pdf
https://www.todamateria.com.br/normas-abnt-trabalhos/
https://blog.mettzer.com/normas-abnt/


Obs.: Postagem de arquivos somente com a extensão PDF.


Prazo de envio: 25/09/2026 - 23:59
Tentativas: 0/2
Tentativa válida: Maior nota
Vale: 3 pontos

A escrita e reflexão é uma atividade pontuada e que compõe a sua nota final.
Acesse o anexo para visualizar a proposta de sua avaliação. Leia com atenção as orientações do seu Professor-Tutor e em caso de dúvidas, não hesite em procurá-lo.
Cabe reforçar que você precisa desenvolver a atividade sem cópias da internet, Inteligência Artificial ou trabalhos prontos. Observe a seguir o que será levado em consideração na hora da correção.
Boa atividade!

##  Critério de avaliação

| Indicadores                              | Pontuação |
| ---------------------------------------- | --------- |
| Formatação, ABNT e citações              | 0.5       |
| Resposta ao que é solicitado             | 1.5       |
| Entendimento acerca do conteúdo estudado | 1.0       |
| Pontuação máxima                         | 3.0       |


##  ✅ Resposta:


