
## REFERENTE A UNIDADE 1
Professor: Carlos Alberto de Oliveira
Disciplina: Paradigmas de Programação

A escrita e reflexão é uma atividade pontuada e que compõe a sua nota final.
Acesse o anexo para visualizar a proposta de sua avaliação. Leia com atenção as orientações do seu Professor-Tutor e em caso de dúvidas, não hesite em procurá-lo.
Cabe reforçar que você precisa desenvolver a atividade sem cópias da internet, Inteligência Artificial ou trabalhos prontos. Observe a seguir o que será levado em consideração na hora da correção.
Boa atividade!

Prazo de envio: 04/12/2026 - 23:59
Tentativas: 0/2
Tentativa válida: Maior nota
Vale: 3 pontos

#### Critérios avaliativos
Formatação, ABNT e citações: 16.66666667% da nota total
Resposta ao que é solicitado: 50% da nota total
Entendimento acerca do conteúdo estudado: 33.33333333% da nota total


## Contextualização
Na unidade um de nossa disciplina, tivemos duas competências que abordam
importante recurso no desenvolvimento front-end, que é o CSS. Um dos grandes
desafios de todos os desenvolvedores front-end é o posicionamento de elementos
em uma página WEB. Uma ferramenta muito importante e utilizada para resolver o
problema relatado é o conceito de caixa flexível – FLEXBOX, que será nosso objeto
de estudo.


## Proposta de Trabalho
Sua tarefa avaliativa será desenvolver uma pesquisa sobre a ferramenta apresentada
acima, proporcionando o desenvolvimento de uma produção textual rica em conteúdo,
que explique:
O que é FlexBox?
Principais conceitos
Principais elementos e propriedades


## Orientações
Seu trabalho, poderá ser entregue em formato de documento ou escrito na própria
plataforma, seguindo as regras de formatação e citações (reprodução de algo) da
ABNT. A opção por arquivo(documento), implica em adicionar capa e contracapa e
todas as regras de desenvolvimento de trabalhos acadêmicos seguindo as normas
da ABNT a tarefa avaliativa. Lembrando, que o objetivo da atividade é o
desenvolvimento da escrita autoral e, por isso, não será tolerado cópia na
integra de textos utilizados como fonte de pesquisa.

#### Links de apoio:

https://www.alura.com.br/artigos/css-guia-do-flexbox
https://www.devmedia.com.br/css3-flexbox-funcionamento-e-propriedades/29532
https://www.youtube.com/watch?v=KbjLtEgmZ_E
https://www.youtube.com/watch?v=hjz6ezV9_uc

Links de apoio referente de como fazer um trabalho acadêmico de acordo com a ABNT:
https://ead.ucs.br/blog/regras-abnt
http://site.ufvjm.edu.br/revistamultidisciplinar/files/2011/09/NBR_14724_atualizada_abr_2011.pdf

Tamanho do texto: Entre 250 e 400 palavras, sem contar a referência bibliográfica.
Obs.: Postagem de arquivos somente com a
extensão PDF.

##  ✅ Resposta ao desafio:

#### O Dominio do Layout Flexível no Desenvolvimento Front-End: Uma Análise Abrangente do CSS Flexbox

#### 1.Introdução
O desenvolvimento de interfaces web modernas exige dos desenvolvedores front-end um controle preciso sobre o posicionamento, o alinhamento e a distribuição de espaço entre os elementos de uma página. Historicamente, tarefas de layout dependiam de propriedades legadas como float, position e manipulações complexas de margens e tabelas, métodos que frequentemente resultavam em código frágil e de difícil manutenção, especialmente em cenários de design responsivo (W3C, 2018).
Para solucionar esses desafios estruturais, a especificação do Flexible Box Layout (comumente abreviado como Flexbox) foi introduzida pelo W3C como um modelo de layout unidimensional. O Flexbox foi desenhado para otimizar o espaço e alinhar itens dentro de um contêiner, mesmo quando suas dimensões são desconhecidas ou dinâmicas (MDN Web Docs, 2024).

#### 2.O que é o Flexbox?
O Flexbox é um módulo de layout CSS que confere ao contêiner a capacidade de alterar a largura e a altura de seus itens para preencher o espaço disponível da melhor maneira possível, adaptando-se a diferentes tamanhos de tela e resoluções.
Diferente dos modelos de layout tradicionais baseados em blocos (block) e linhas (inline), que são bidimensionais ou focados no fluxo documental padrão, o Flexbox opera em uma única dimensão por vez — seja em formato de linha (horizontal) ou de coluna (vertical). Essa característica o torna extremamente poderoso para o desenho de componentes de interface, barras de navegação, galerias de cartões (cards) e alinhamentos complexos centralizados.

#### 3.Principais Conceitos do Flexbox
Para compreender o funcionamento do Flexbox, é fundamental dominar a relação entre o elemento pai e seus elementos filhos, além de seus eixos direcionais:

Contêiner Flex (Flex Container): É o elemento pai que recebeu a propriedade display: flex; ou display: inline-flex;. Ele passa a gerenciar diretamente o comportamento de layout de todos os seus filhos diretos.
Itens Flex (Flex Items): São os elementos filhos diretos posicionados dentro do contêiner flex.

Eixo Principal (Main Axis) e Eixo Transversal (Cross Axis):
O Main Axis é o eixo primário ao longo do qual os itens flexíveis são colocados. Sua direção é definida pela propriedade flex-direction.
O Cross Axis é o eixo perpendicular ao eixo principal. Se o eixo principal for horizontal (linha), o eixo transversal será vertical (coluna), e vice-versa.

#### 4.Principais Elementos e Propriedades
O poder do Flexbox reside na divisão clara de suas propriedades entre aquelas aplicadas ao Contêiner e aquelas aplicadas aos Itens.

4.1. Propriedades do Contêiner Flex
flex-direction: Define a direção do eixo principal. Os valores comuns são row (padrão, da esquerda para a direita), row-reverse, column (de cima para baixo) e column-reverse.
flex-wrap: Por padrão, os itens flexíveis tentam caber em uma única linha. A propriedade flex-wrap permite que eles quebrem em múltiplas linhas, aceitando os valores nowrap, wrap e wrap-reverse.
justify-content: Alinha os itens ao longo do Eixo Principal. Seus principais valores incluem flex-start, flex-end, center, space-between (espaço igual entre os itens), space-around e space-evenly.
align-items: Controla o alinhamento dos itens ao longo do Eixo Transversal. Valores frequentes: stretch (padrão), flex-start, flex-end, center e baseline.

4.2. Propriedades dos Itens Flex
flex-grow: Define a capacidade de um item flexível crescer se necessário, atuando como um fator proporcional em relação aos demais itens (Mozilla Contributors, 2024).
flex-shrink: Define a capacidade de um item encolher caso o espaço disponível no contêiner seja insuficiente.
flex-basis: Define o tamanho padrão (inicial) de um item antes que o espaço restante seja distribuído de acordo com os fatores de crescimento e encolhimento.
align-self: Permite que um item específico sobrescreva o alinhamento definido pelo align-items do contêiner para o eixo transversal.


#### 5.Considerações Finais
O advento do Flexbox representou um marco na evolução do desenvolvimento front-end, mitigando gargalos históricos de alinhamento e posicionamento na web. Ao compreender seus conceitos fundamentais de eixos, contêineres e propriedades direcionais, o desenvolvedor ganha autonomia para construir layouts robustos, limpos e totalmente responsivos, atendendo com excelência aos requisitos técnicos exigidos em projetos modernos.

## Referências

MDN WEB DOCS. CSS Flexible Box Layout. Disponível em: https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_flexible_box_layout. Acesso em: 10 nov. 2026.

MOZILLA CONTRIBUTORS. Basic concepts of flexbox. MDN Web Docs, 2024. Disponível em: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox. Acesso em: 10 nov. 2026.

W3C. CSS Flexible Box Layout Module Level 1. W3C Recommendation, 2018. Disponível em: https://www.w3.org/TR/css-flexbox-1/. Acesso em: 10 nov. 2026.

