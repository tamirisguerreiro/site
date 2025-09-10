---
layout: default
---

# Decifrando o Ataque: O Que os Números Revelam - Utilizando Web Scraping 🏐👧

Este projeto consiste em um **Web Scraping** da página Volleyballworld - Estatísticas, com o objetivo de coletar e analisar dados das atletas que competiram na Tailândia jogando o Mundial de Vôlei Feminino 2025.

---

### Objetivo

Extrair, limpar e classificar dados estatísticos de uma tabela online, gerando um ranking das melhores atacantes com base na sua eficiência:

- **Top melhores atacantes** (Critério: `>= 170` no Total de Tentativas em relação ao `% de Sucesso`)
- **Percentual de erros** (`%_erros` em relação ao total)
- **Percentual de tentativas** (`%_tentativas` em relação ao total)

---

### Critérios de Classificação e Resultados

Aplicamos um filtro rigoroso para selecionar apenas as atletas com um volume de ataque significativo, considerando aquelas com um total de tentativas igual ou superior a 170. Essa filtragem garante que a análise de desempenho seja representativa e focada em jogadoras com maior participação ofensiva.

O ranking final foi gerado ordenando as atletas selecionadas com base na métrica de **% de Sucesso**. As informações foram consolidadas em um arquivo CSV, `melhores_atletas.csv`, facilitando o compartilhamento e a visualização dos resultados. Esta análise demonstra como a aplicação de ferramentas de **ciência de dados** pode transformar dados brutos da web em informações valiosas e estruturadas.

---

### Ferramentas Utilizadas

- **Python** (Bibliotecas: `BeautifulSoup`, `Pandas`)

---

### Código Web Scraping

### Análise de Desempenho de Atletas de Voleibol 🏐

---

Este notebook demonstra a coleta e análise de dados de desempenho de atletas de voleibol, utilizando **Web Scraping** para extrair estatísticas de uma página web e **análise de dados** para gerar um ranking de eficiência.

---

### **Etapa 1: Importar Bibliotecas**

Importamos as bibliotecas necessárias: `pandas` para manipulação de dados e `BeautifulSoup` para web scraping.

```python
import pandas as pd
from bs4 import BeautifulSoup

html_content = """<table class="vbw-o-table vbw-tournament-player-statistic-table vbw-stats-scorers" data-enable-sorting="true" data-pagination="20"><thead class="vbw-o-table_header"><tr class="vbw-o-tableheader-group"><th class="vbw-o-tableheader rank" scope="col"><span class="full-text">Classificação</span><span class="abbreviated-text">Class.</span></th><th class="vbw-o-tableheader playername" scope="col"><span class="full-text">Nome do atleta</span><span class="abbreviated-text">Atleta</span></th><th class="vbw-o-tableheader federation" scope="col"><span class="full-text">Team</span><span class="abbreviated-text">Team</span></th><th class="vbw-o-tableheader attacks" scope="col"><span class="full-text">Pontos</span><span class="abbreviated-text">attacks</span></th><th class="vbw-o-tableheader faults" scope="col"><span class="full-text">Erros</span><span class="abbreviated-text">SE</span></th><th class="vbw-o-tableheader shots" scope="col"><span class="full-text">Tentativas</span><span class="abbreviated-text">shots</span></th><th class="vbw-o-tableheader average-per-match" scope="col"><span class="full-text">Média por partida</span><span class="abbreviated-text">average-per-match</span></th><th class="vbw-o-tableheader success-perc" scope="col"><span class="full-text">% de Sucesso</span><span class="abbreviated-text">% de Sucesso</span></th><th class="vbw-o-tableheader total-attempts" scope="col"><span class="full-text">Total</span><span class="abbreviated-text">TA</span></th></tr></thead><tbody class="vbw-o-tablebody"><tr class="vbw-o-tablerow vbw-o-tablerow--scorer vbw-stats-player-4" data-player-no="143339"><td class="vbw-o-tablecell rank">1</td><td class="vbw-o-tablecell playername"><a class="vbw-muplayer" href="/volleyball/competitions/women-world-championship/players/143339">Vargas</a></td><td class="vbw-o-tablecell federation">TUR</td><td class="vbw-o-tablecell attacks">134</td><td class="vbw-o-tablecell faults">28</td><td class="vbw-o-tablecell shots">110</td><td class="vbw-o-tablecell average-per-match">19.14</td><td class="vbw-o-tablecell success-perc">49.26</td><td class="vbw-o-tablecell total-attempts">272</td></tr><tr class="vbw-o-tablerow vbw-o-tablerow--scorer vbw-stats-player-4" data-player-no="162218"><td class="vbw-o-tablecell rank">2</td><td class="vbw-o-tablecell playername"><a class="vbw-muplayer" href="/volleyball/competitions/women-world-championship/players/162218">Ishikawa</a></td><td class="vbw-o-tablecell federation">JPN</td><td class="vbw-o-tablecell attacks">128</td><td class="vbw-o-tablecell faults">53</td><td class="vbw-o-tablecell shots">153</td><td class="vbw-o-tablecell average-per-match">18.29</td><td class="vbw-o-tablecell success-perc">38.32</td><td class="vbw-o-tablecell total-attempts">334</td></tr><tr class="vbw-o-tablerow vbw-o-tablerow--scorer vbw-stats-player-10" data-player-no="136896"><td class="vbw-o-tablecell rank">3</td><td class="vbw-o-tablecell playername"><a class="vbw-muplayer" href="/volleyball/competitions/women-world-championship/players/136896">Gabi</a></td><td class="vbw-o-tablecell federation">BRA</td><td class="vbw-o-tablecell attacks">125</td><td class="vbw-o-tablecell faults">34</td><td class="vbw-o-tablecell shots">109</td><td class="vbw-o-tablecell average-per-match">17.86</td><td class="vbw-o-tablecell success-perc">46.64</td><td class="vbw-o-tablecell total-attempts">268</td></tr><tr class="vbw-o-tablerow vbw-o-tablerow--scorer vbw-stats-player-18" data-player-no="150840"><td class="vbw-o-tablecell rank">4</td><td class="vbw-o-tablecell playername"><a class="vbw-muplayer" href="/volleyball/competitions/women-world-championship/players/150840">Egonu</a></td><td class="vbw-o-tablecell federation">ITA</td><td class="vbw-o-tablecell attacks">106</td><td class="vbw-o-tablecell faults">28</td><td class="vbw-o-tablecell shots">106</td><td class="vbw-o-tablecell average-per-match">15.14</td><td class="vbw-o-tablecell success-perc">44.17</td><td class="vbw-o-tablecell total-attempts">240</td></tr><tr class="vbw-o-tablerow vbw-o-tablerow--scorer vbw-stats-player-1" data-player-no="168983"><td class="vbw-o-tablecell rank">5</td><td class="vbw-o-tablecell playername"><a class="vbw-muplayer" href="/volleyball/competitions/women-world-championship/players/168983">Cazaute</a></td><td class="vbw-o-tablecell federation">FRA</td><td class="vbw-o-tablecell attacks">96</td><td class="vbw-o-tablecell faults">32</td><td class="vbw-o-tablecell shots">86</td><td class="vbw-o-tablecell average-per-match">19.20</td><td class="vbw-o-tablecell success-perc">44.86</td><td class="vbw-o-tablecell total-attempts">214</td></tr><tr class="vbw-o-tablerow vbw-o-tablerow--scorer vbw-stats-player-26" data-player-no="189193"><td class="vbw-o-tablecell rank">6</td><td class="vbw-o-tablecell playername"><a class="vbw-muplayer" href="/volleyball/competitions/women-world-championship/players/189193">Yoshino</a></td><td class="vbw-o-tablecell federation">JPN</td><td class="vbw-o-tablecell attacks">92</td><td class="vbw-o-tablecell faults">41

