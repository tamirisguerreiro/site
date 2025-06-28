---
layout: default
---

# Análise do 26º Campeonato Mundial de Handebol Feminino

---
*Base de dados:* Top Goalkepper - Most Saves

*Sobre o dataset:* Este conjunto de dados abrange informações detalhadas sobre o desempenho das goleiras durante o 26º Campeonato Mundial Feminino de Handebol, realizado na Dinamarca, Noruega e Suécia. 
Contendo métricas de eficiência individual, número de jogos disputados (e como titular), total de defesas realizadas e dados biométricos como a altura das atletas. O conjunto foi desenvolvido para análises de desempenho esportivo, identificando as goleiras e países de maior sucesso defensivo, e para estudos sobre a influência de diferentes variáveis no sucesso da posição.


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
* Gráficos de Treemap: Top Eficiência
* Gráficos de Dispersão: Dipersão Altura e Eficiência
* Gráficos de Tabela: Analise de Dados Físicos
* Gráficos de Barras: Eficiência por País
* Cartões: Média de Eficiência


# Resultados Obtidos

A eficiência geral das goleiras no torneio está em 32,43%, indicando a média de desempenho. As métricas de "Eficiência (%)" 
e "Defesas" focam no desempenho individual dessas atletas, e a coluna "Principal" serve para identificar as goleiras que foram titulares ou tiveram maior tempo de jogo.

## **Análise por País**

Existe uma disparidade entre a gama de eficiência entre os países é notável, variando de 42% (Montenegro) a 25% (Congo). Isso indica diferentes níveis de competitividade e, provavelmente, de força defensiva geral das equipes, além da qualidade individual das goleiras. Média como Divisor: A média de 32,43% atua como um bom ponto de corte, com os países acima dela demonstrando um desempenho de goleiras superior à média do campeonato.

## **Análise das Atletas**

A análise da eficiência das goleiras revela desempenhos variados, com Marta Batinovic (Montenegro) liderando com impressionantes 51% de eficiência em 40 defesas, sendo um fator crucial para sua equipe. Silje Margaretha Solberg (Noruega) também se destaca, com 40% de eficiência e um maior volume de 65 defesas. Na alta eficiência (35% a 39%), Yara Ten Holte (Holanda) demonstra consistência com 38% em 79 defesas, e Petra Kudláčková (República Tcheca) impressiona com 87 defesas a 35%, indicando alta exigência. Bárbara Arenhart (Brasil) é a brasileira de melhor desempenho nesta faixa, com 35% em 36 defesas. A categoria de eficiência média (30% a 34%) inclui goleiras com alto volume de trabalho, como Marinela Rajic (Montenegro) (33% em 71 defesas) e Madeleine Noelia Cortes Fuenzalida (Chile) (33% em 72 defesas), sugerindo defesas expostas. Gabriela Gonçalves Dias Moreschi (Brasil) também está nesta faixa (32% em 36 defesas). Por fim, na baixa eficiência (abaixo de 30%), casos como Fatemeh Khalili Behfar (Irã) (29% em 65 defesas) apontam para equipes com dificuldades defensivas. A menor eficiência é de Lu Chang (R.P. da China), com 22% em 34 defesas, refletindo um grande desafio para a China na posição.

## Dispersão Altura e Eficiência (%):

O gráfico de dispersão permanece consistente em todas as visualizações. Ele mostra que não há uma correlação linear forte entre a altura da goleira e sua eficiência.
Enquanto as goleiras de alta eficiência tendem a ter alturas entre 1,75m e 1,90m, há exceções e muita variação. Goleiras mais baixas (como CORTES FUENZALIDA Madeleine Noelia com 1,64m) podem ter um bom volume de defesas, mesmo que com menor eficiência percentual em comparação com as tops, sugerindo que outros atributos como agilidade e posicionamento são cruciais. A hipótese de "Qtd Jogos" ser o número de partidas disputadas (ou com minutos em campo) e "Principal" indicar a quantidade de jogos como goleira titular (ou com a maioria dos minutos) é altamente provável. Quando "Qtd Jogos" e "Principal" são iguais ou muito próximos (ex: 9 e 9, 7 e 7), isso indica que a goleira foi a escolha principal em quase todas as partidas. O número de defesas por "Qtd Jogos" pode dar uma ideia da média de arremessos que a goleira enfrentou por partida, o que reflete o quão exposta sua equipe estava defensivamente.

## Conclusão:

Há um claro grupo de elite em termos de eficiência de goleiras, liderado por Montenegro (Marta Batimovic). Esses países e atletas têm uma vantagem defensiva notável que pode ser um diferencial competitivo. A eficiência da goleira é um indicador crítico, mas precisa ser contextualizada com o desempenho defensivo da equipe. Goleiras com alto número de defesas, mas eficiência média/baixa, podem estar em equipes que cedem muitos arremessos ao gol, indicando fragilidades na defesa como um todo. Alguns países possuem goleiras com eficiências bastante distintas (e.g., Noruega com Solberg e Lunde; França com Sako e Glauser), o que pode indicar rotação ou hierarquia de desempenho definida pela comissão técnica. Desafios para Países de Baixa Eficiência: Os países no final da lista (Congo, R.P. da China, Polônia, etc.) provavelmente enfrentam desafios tanto na eficiência de suas goleiras quanto, possivelmente, na capacidade de suas defesas de limitar os arremessos dos adversários, necessitando de um olhar mais aprofundado na estratégia defensiva. A altura não é o fator primordial para a eficiência da goleira. Isso reforça que atributos como técnica de defesa, agilidade, posicionamento e capacidade de leitura do jogo são mais relevantes para o sucesso na posição.

[Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNzljMWYwYzEtYTMzMC00ZDA3LTliZjktY2I3OTRhMTk0N2NjIiwidCI6ImE5MWY1ZjM3LThmMzMtNDNlMi04MGJhLThkNzQ5YTVkZWQ1MSJ9)

![Campeonato Mundial Feminino](images/26%20mundial%20feminino.png)

[Home](https://tamirisguerreiro.github.io/site)
