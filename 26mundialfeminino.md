---
# Análise do 26º Campeonato Mundial Feminino de IHF
---
#### Base de dados: Top Goalkepper - Most Saves

#### Sobre o dataset: 
Este conjunto de dados abrange informações detalhadas sobre o desempenho das goleiras durante o 26º Campeonato Mundial Feminino de Handebol, realizado na Dinamarca, Noruega e Suécia. 
Contendo métricas de eficiência individual, número de jogos disputados (e como titular), total de defesas realizadas e dados biométricos como a altura das atletas. O conjunto foi desenvolvido para análises de desempenho esportivo,
identificando as goleiras e países de maior sucesso defensivo, e para estudos sobre a influência de diferentes variáveis no sucesso da posição.


# Objetivo
Identificar os fatores determinantes para a alta eficiência de goleiras no handebol feminino em nível de Campeonato Mundial, analisar o desempenho defensivo médio das seleções 
e correlacionar características das atletas (como altura e volume de jogo) com o sucesso na posição, visando otimizar estratégias de treinamento e seleção de atletas.


# Ferramentas Utilizadas
* Power BI
* Power Query


# Principais Etapas
Utilizei o método ETL para tratamento dos dados.

## 1. Extração (Extract)
Fonte de dados: Base obtida do site IHF (em inglês).

Ações realizadas:
* Importação do dataset original em PDF
* Verificação inicial da estrutura, qualidade e tipo dos dados

## 2. Transformação (Transform)
Padronização de dados:

Tradução de colunas (inglês → português) usando Replace Values
Ajuste de tipos de dados

## 3. Carregamento (Load)
Modelagem no Power BI:

Criação de novas colunas:
* Difereciando colunas e extraindo novas medidas para criação de colunas para melhor detalhamento do dataset.
* Criação de Medidas Calculadas: Utilizei bastante da função COUNT, AVERAGE, FILTER entre outras.


# Visualização e Insights
Dashboard:

* Gráficos de Treemap: Top EficiÊncia
* Gráficos de Dispersão: Dipersão Altura e Eficiência
* Gráficos de Tabela: Analise de Dados Físicos
* Gráficos de Barras: Eficiência por País
* Cartões: Média de Eficiência


# Resultados Obtidos

## **Visão Geral do Campeonato**

A eficiência geral das goleiras no torneio está em 32,43%, indicando a média de desempenho. As métricas de "Eficiência (%)" 
e "Defesas" focam no desempenho individual dessas atletas, e a coluna "Principal" serve para identificar as goleiras que foram titulares ou tiveram maior tempo de jogo.

## **Análise por País**

Existe uma disparidade entre a gama de eficiência entre os países é notável, variando de 42% (Montenegro) a 25% (Congo). Isso indica diferentes níveis de competitividade e, provavelmente, de força defensiva geral das equipes, além da qualidade individual das goleiras.
Média como Divisor: A média de 32,43% atua como um bom ponto de corte, com os países acima dela demonstrando um desempenho de goleiras superior à média do campeonato.

## **Análise das Atletas**

#### Eficiência Excepcional (40%+):

* BATINOVIC Marta (Montenegro): 51% de eficiência com 40 defesas. Líder clara e isolada, seu desempenho é um fator chave para a alta média de Montenegro.
SOLBERG
* Silje Margaretha (Noruega): 40% de eficiência com 65 defesas. Excelente desempenho, contribuindo significativamente para a Noruega.

#### Alta Eficiência (35% - 39%):

* TEN HOLTE Yara (Holanda): 38% de eficiência com 79 defesas. Apresenta alto volume de defesas e alta eficiência, mostrando consistência.
* PUJEVIĆ Tea (Croácia): 37% de eficiência com 41 defesas.
* BÖDE-BIRÓ Blanka (Hungria): 36% de eficiência com 58 defesas.
* BUNDSEN Johanna (Suécia): 36% de eficiência com 74 defesas.
* NOVOTNÁ Sabrina (República Tcheca): 36% de eficiência com 43 defesas.
* REINHARDT Althea Rebecca (Dinamarca): 36% de eficiência com 52 defesas.
* WACHTER Sarah (Alemanha): 36% de eficiência com 48 defesas.
* ARENHART Bárbara (Brasil): 35% de eficiência com 36 defesas. A goleira brasileira com o melhor desempenho detalhado nas tabelas.
* KUDLÁČKOVÁ Petra (República Tcheca): 35% de eficiência com 87 defesas. Um número impressionante de defesas, indicando que foi extremamente exigida em seus jogos.

#### Eficiência Média (30% - 34%):

* LUNDE Katrine (Noruega): 34% de eficiência com 46 defesas.
* SAKO Hatadou (França): 34% de eficiência com 44 defesas.
* RAJIC Marinela (Montenegro): 33% de eficiência com 71 defesas. Curiosamente, outra goleira de Montenegro com uma eficiência menor que Marta, mas com um alto número de defesas. Isso sugere que mesmo com uma goleira de 51%, Montenegro ainda pode ter sofrido muitos arremessos em outros momentos ou com outras goleiras.
* CASTELLANOS SOANEZ Mercedes (Espanha): 33% de eficiência com 40 defesas.
* CORTES FUENZALIDA Madeleine Noelia (Chile): 33% de eficiência com 72 defesas. Alto volume de trabalho para o Chile, indicando que sua defesa pode ter sido bastante exposta.
* RENÓTUDÓTTIR Hafdis (Islândia): 33% de eficiência com 37 defesas.
* GLAUSER Laura (França): 33% de eficiência com 65 defesas.
* GONÇALVES DIAS MORESCHI Gabriela (Brasil): 32% de eficiência com 36 defesas. Outra goleira brasileira, com eficiência um pouco abaixo de Bárbara Arenhart.
* THORSTEINDÓTTIR Elín Jóna (Islândia): 32% de eficiência com 43 defesas.
* TOFT Sandra (Dinamarca): 32% de eficiência com 49 defesas.
* ALBERTO Marta Samuel (Angola): 30% de eficiência com 63 defesas.
* PANODZIĆ Amra (Eslovênia): 30% de eficiência com 38 defesas.
* TOUBISSA ELBECO Justicia (Senegal): 30% de eficiência com 55 defesas.

#### Baixa Eficiência (Abaixo de 30%):

* CARRATU Marisol (Argentina): 29% de eficiência com 44 defesas.
* HOSU Daciana (Romênia): 29% de eficiência com 35 defesas.
* HU Yunuo (R.P. da China): 29% de eficiência com 31 defesas.
* KHALILI BEHFAR Fatemeh (Irã): 29% de eficiência com 65 defesas. Alto número de defesas para uma eficiência baixa, indicando equipe muito exposta e com dificuldades defensivas.
* MBEN BEDIANO Isabelle Noelle (Camarões): 29% de eficiência com 44 defesas.
* FILTER Katharina (Alemanha): 28% de eficiência com 55 defesas.
* ČOLIĆ Marija (Sérvia): 27% de eficiência com 31 defesas.
* OCAMPOS MOREL Fatima (Paraguai): 27% de eficiência com 46 defesas.
* PŁACZEK Adrianna (Polônia): 26% de eficiência com 35 defesas.
* KODIA Ruth (Congo): 25% de eficiência com 45 defesas.
* LU Chang (R.P. da China): 22% de eficiência com 34 defesas. A menor eficiência observada, refletindo um desafio significativo para a China na posição.

## Dispersão Altura e Eficiência (%):

O gráfico de dispersão permanece consistente em todas as visualizações. Ele mostra que não há uma correlação linear forte entre a altura da goleira e sua eficiência.
Enquanto as goleiras de alta eficiência tendem a ter alturas entre 1,75m e 1,90m, há exceções e muita variação. Goleiras mais baixas (como CORTES FUENZALIDA Madeleine Noelia com 1,64m) podem ter um bom volume de defesas, mesmo que com menor eficiência percentual em comparação com as tops, sugerindo que outros atributos como agilidade e posicionamento são cruciais.
Interpretação de "Qtd Jogos" e "Principal":

A hipótese de "Qtd Jogos" ser o número de partidas disputadas (ou com minutos em campo) e "Principal" indicar a quantidade de jogos como goleira titular (ou com a maioria dos minutos) é altamente provável.
Quando "Qtd Jogos" e "Principal" são iguais ou muito próximos (ex: 9 e 9, 7 e 7), isso indica que a goleira foi a escolha principal em quase todas as partidas.
O número de defesas por "Qtd Jogos" pode dar uma ideia da média de arremessos que a goleira enfrentou por partida, o que reflete o quão exposta sua equipe estava defensivamente.

## Conclusões Abrangentes:

Há um claro grupo de elite em termos de eficiência de goleiras, liderado por Montenegro (Marta Batimovic). 
Esses países e atletas têm uma vantagem defensiva notável que pode ser um diferencial competitivo.

#### O Papel da Goleira e da Defesa

A eficiência da goleira é um indicador crítico, mas precisa ser contextualizada com o desempenho defensivo da equipe. Goleiras com alto número de defesas, mas eficiência média/baixa, podem estar em equipes que cedem muitos arremessos ao gol, indicando fragilidades na defesa como um todo.

#### Variação Interna de Países

Alguns países possuem goleiras com eficiências bastante distintas (e.g., Noruega com Solberg e Lunde; França com Sako e Glauser), o que pode indicar rotação ou hierarquia de desempenho definida pela comissão técnica.
Desafios para Países de Baixa Eficiência: Os países no final da lista (Congo, R.P. da China, Polônia, etc.) provavelmente enfrentam desafios tanto na eficiência de suas goleiras quanto, possivelmente, na capacidade de suas defesas de limitar os arremessos dos adversários, necessitando de um olhar mais aprofundado na estratégia defensiva.

#### Altura vs. Desempenho

A altura não é o fator primordial para a eficiência da goleira. Isso reforça que atributos como técnica de defesa, agilidade, posicionamento e capacidade de leitura do jogo são mais relevantes para o sucesso na posição.
