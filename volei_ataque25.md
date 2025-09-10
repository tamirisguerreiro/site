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

(https://raw.githubusercontent.com/tamirisguerreiro/site/main/images/webscrapingvolei.png)

[Python Código - Clique Aqui](https://github.com/tamirisguerreiro/site/blob/main/images/Estatisticas%20Melhores%20Atacantes%20Mundial%20Feminino%2025.md)
