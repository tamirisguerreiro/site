---
layout: default
---

# 📉 Decifrando o Rebaixamento: O Que os Gráficos de xGD/90 e xGA Apresentam

---
*Base de dados:* Campeonato Brasileiro Betano 2025 (Rodadas 29, 30 e 38)

*Sobre o dataset:* Este projeto consiste em uma **Análise Estatística Avançada** baseada em dados de desempenho. O objetivo é mapear a performance e a tendência dos times na luta contra o rebaixamento (Z-4) ao longo das Rodadas 29, 30 e 38, utilizando as métricas de **Gols Esperados (xGD/90)** e **Gols Esperados Contra (xGA)**.


---

# Objetivo
Extrair e comparar a posição dos times no gráfico de **Desempenho Ofensivo** (xGD/90) vs. **Risco Defensivo** (xGA), identificando o **Quadrante de Maior Perigo (Inferior-Esquerdo)** e a correlação entre o desempenho técnico (xGD/90/xGA) e o rebaixamento real.

* **Eixo X (xGD/90):** Eficiência Ofensiva (Quanto mais à direita, melhor).
* **Eixo Y (xGA):** Risco Defensivo (Quanto mais para cima/valor menor, melhor).
* **Quadrante de Risco (Inferior-Esquerdo):** Baixo xGD/90 (Ataque ineficiente) e Alto xGA (Defesa vulnerável).

---


# Ferramentas Utilizadas

* **R Studio**
* **Power BI**
* **Power Query**

Utilizei o método **ETL** para tratamento dos dados e a interpretação de dados visuais (Gráficos de Dispersão xGD/90 vs. xGA) para mapear a performance..

## 1. Extração (Extract)
Fonte de dados: Scraping em R da página FBref.

Ações realizadas:
* Importação do dataset em CSV
* Verificação inicial da estrutura, qualidade e tipo dos dados

## 2. Transformação (Transform)
Padronização de dados:

* Tradução de colunas (inglês → português) usando `Replace Values`
* Ajuste de tipos de dados

## 3. Carregamento (Load)
Modelagem no Power BI:

Criação de novas colunas:
* Diferenciando colunas e extraindo novas medidas para criação de colunas para melhor detalhamento do dataset.
* Criação de Medidas Calculadas: Utilizei a função `SUM`.

## Visualização e Insights

Dashboard:
* **Interpretação de Dados Visuais**  Gráficos de Dispersão: Dispersão xGD/90 e xGA
* **Métricas Avançadas de Futebol** Gráficos de Tabela: Tabela de Classifiação e Métricas Avançadas 

---


# Principais Etapas

## 1. Definição das Métricas
Métricas Avançadas:
* **xGD/90** (Gols Esperados por 90 minutos)
* **xGA** (Gols Esperados Contra)
* **Diferença GA - xGA** (Diferencial de Desempenho Defensivo)

## 2. Análise Preditiva
O quadrante inferior-esquerdo atua como um forte indicador de **risco de rebaixamento** (vulnerabilidade técnica).

## 3. Análise Comparativa
Comparação das posições dos times nas Rodadas 29, 30 e 38, focando nos times da Z-4 (17º ao 20º).

---


# 🔍 Critérios de Classificação e Resultados

Os resultados foram consolidados em uma visão progressiva da Rodada 29, Rodada 30, Rodada 38, destacando a **Estabilidade no Risco** e a **Performance de Escape**. 

| Time | Rodada 29 (Rk) | Rodada 30 (Rk) | Rodada 38 (Rk) | Status Final | Observação do Desempenho no Gráfico (xGD/90/xGA) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Sport Recife** | 20º | 20º | 20º | **REBAIXADO** | Pior Categoria Consistente. Culminou com o pior xGA (cerca de 63,5) e xGD/90 (-0,7). |
| **Juventude** | 18º | 19º | 19º | **REBAIXADO** | Estabilidade no Risco. Sempre no quadrante mais perigoso (baixo xGD/90, alto $xGA$) nas três rodadas analisadas. |
| **Fortaleza** | 19º | 18º | 18º | **REBAIXADO** | Risco Ofensivo. xGA final (56,7) melhor que Sport/Juventude, mas com xGD/90 negativo (-0,31). |
| **Ceará** | 13º | 14º | 17º | **REBAIXADO** | Queda por Pontos. Melhor desempenho técnico entre os rebaixados, com xGD/90 quase zero e xGA relativamente baixo. Caiu pela pontuação acumulada. |
| **Grêmio** | 12º | 11º | 9º | **ESCAPOU** | Alerta Defensivo Extremo. Apresentou um dos piores xGA do campeonato na R38 (cerca de 59), indicando defesa altamente exposta. |
| **Vitória** | 17º | 17º | 15º | **ESCAPOU** | Escapada Crítica. No limite do quadrante perigoso na R29/R30. xGA alto (53,3). |
| **Internacional** | 14º | 15º | 16º | **ESCAPOU** | Performance Técnica Forte. Desempenho no quadrante Superior-Direito (xGD/90 positivo na R38). |

---


# Síntese da Análise Gráfica 

## Rebaixamento por Ineficiência Estatística 

O **Sport Recife** e o **Juventude** foram os times com o pior desempenho técnico. Eles ocuparam o quadrante inferior esquerdo com os valores de xGA mais altos e xGD/90 mais negativos, indicando que sofreram muitas chances de gol e criaram poucas, sendo **consistentemente os mais vulneráveis** do campeonato.

## Rebaixamento por Falta de Pontos 

**Ceará** e **Fortaleza** caíram com desempenho gráfico melhor do que os lanternas. O Ceará, em particular, tinha uma performance técnica quase mediana. Isso demonstra que, apesar de não serem os piores tecnicamente pelas métricas xGD/90/xGA, a **falta de pontuação acumulada** foi o fator decisivo para a queda.

## Pontos Acumulados vs. Risco Defensivo

O **Grêmio** garantiu a permanência pela pontuação acumulada, desafiando suas próprias métricas técnicas. Esteve consistentemente no quadrante de risco (alto xGA, baixo xGD/90), com o pior $xGA$ da liga na R38. Sua segurança foi fruto de overperformance em momentos cruciais, e não de uma solidez defensiva esperada (xGA). O time fugiu da Z-4 apesar dos números.

## O "Escape" na Margem e Risco Defensivo 

O **Vitória** flertou de perto com o rebaixamento (17º lugar nas rodadas 29 e 30). No gráfico, situou-se no quadrante de risco (inferior esquerdo) com alto xGA, o que confirmou a fragilidade defensiva. Sua permanência foi um "escape" pela margem da tabela, onde as métricas técnicas indicavam um forte risco de queda. 

## Anomalia de Alta Performance 

O **Internacional** é a principal anomalia estatística, ocupando o quadrante de melhor desempenho técnico (alto xGD/90, baixo xGA). Contraditoriamente, flertou com o rebaixamento (16º na R38). O time gerou qualidade de chances para estar no topo do gráfico, mas falhou ao final do campeonato. Provando que uma métrica de qualidade não substitui a finalização.

---


# 🔎 Conclusão: Dados Quantitativos vs. Qualitativos no Futebol

A análise apresentada focou estritamente em métricas avançadas quantitativas (xGA, xGD/90, Diferença GA - xGA), onde os dados brutos nos fornecem informações valiosas sobre a performance estatística e o risco técnico das equipes, revelando o que "deveria" ter acontecido. Contudo, é crucial reconhecer que o esporte é igualmente moldado por dados qualitativos — como motivação, impacto da comissão técnica, erros de arbitragem, e momentos de pura genialidade ou falha individual —, fatores que não foram reportados nesta análise, mas que inegavelmente influenciam a pontuação final e a realidade da tabela.


[**Clique Aqui para Ver o Dashboard do Campeonato Brasileiro Rebaixamento 2025**](https://app.powerbi.com/view?r=eyJrIjoiYjE0ZjllZjMtOGFjMy00MDdlLThiN2MtMTM0MDI2ZTQwYjg4IiwidCI6ImE5MWY1ZjM3LThmMzMtNDNlMi04MGJhLThkNzQ5YTVkZWQ1MSJ9)

![Rebaixamento](https://raw.githubusercontent.com/tamirisguerreiro/site/main/images/Powerbirebaixamento.png) 

[Página Inicial](https://tamirisguerreiro.github.io/site)
