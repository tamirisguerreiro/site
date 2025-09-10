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

html_content = """<table class="vbw-o-table vbw-tournament-player-statistic-table vbw-stats-scorers"a class="vbw-muplayer" href="/volleyball/competitions/women-world-championship/players/163939">Weske</a></td>"""

table = soup.find('table', class_='vbw-o-table vbw-tournament-player-statistic-table vbw-stats-scorers')

headers = [th.get_text(strip=True) for th in table.find('thead').find_all('th')]

data_rows = []
for row in table.find('tbody').find_all('tr'):
    row_data = [td.get_text(strip=True) for td in row.find_all('td')]
    data_rows.append(row_data)

voley = pd.DataFrame(data_rows, columns=headers)

voley = voley.rename(columns={
    '% de Sucesso% de Sucesso': '% de Sucesso',
    'Nome do atletaAtleta': 'Nome da Atleta',
    'TeamTeam': 'Equipe',
    'Pontosattacks': 'Pontos',
    'ClassificaçãoClass.': 'Classificação',
    'ErrosSE': 'Erros',
    'Tentativasshots': 'Tentativas',
    'Média por partidaaverage-per-match': 'Média por partida',
    'TotalTA': 'Total'
})

voley['Erros'] = pd.to_numeric(voley['Erros'], errors='coerce')
voley['Total'] = pd.to_numeric(voley['Total'], errors='coerce')
voley['Pontos'] = pd.to_numeric(voley['Pontos'], errors='coerce')
voley['Média por partida'] = pd.to_numeric(voley['Média por partida'], errors='coerce')
voley['% de Sucesso'] = pd.to_numeric(voley['% de Sucesso'], errors='coerce')
voley['Classificação'] = pd.to_numeric(voley['Classificação'], errors='coerce')
voley['Tentativas'] = pd.to_numeric(voley['Tentativas'], errors='coerce')


voley['%_erros'] = ((voley['Erros'] / voley['Total']) * 100).round(2)
voley['%_tentativas'] = ((voley['Tentativas'] / voley['Total']) * 100).round(2)


voley_top10 = voley[voley['Total'] >= 170]
voley_top10 = voley_top10.dropna()

melhores = voley_top10.nlargest(40,'% de Sucesso')

melhores.to_csv('melhores_atletas.csv', encoding='utf-8')

print('Executado com Sucesso!')

