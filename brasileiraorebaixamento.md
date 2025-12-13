---
layout: default
---

# 📉 Decifrando o Rebaixamento: O Que os Gráficos de $xG$ e $xGA$ Revelam

---
*Base de dados:* Campeonato Brasileiro Betano 2025 (Rodadas 29, 30 e 38)

*Sobre o dataset:* Este projeto consiste em uma **Análise Estatística Avançada** baseada em dados de desempenho. O objetivo é mapear a performance e a tendência dos times na luta contra o rebaixamento (Z-4) ao longo das Rodadas 29, 30 e 38, utilizando as métricas de **Gols Esperados ($xG/90$)** e **Gols Esperados Contra ($xGA$)**.

---

# Objetivo
Extrair e comparar a posição dos times no gráfico de **Desempenho Ofensivo** ($xG/90$) vs. **Risco Defensivo** ($xGA$), identificando o **Quadrante de Maior Perigo (Inferior-Esquerdo)** e a correlação entre o desempenho técnico ($xG/xGA$) e o rebaixamento real.

* **Eixo X ($xG/90$):** Eficiência Ofensiva (Quanto mais à direita, melhor).
* **Eixo Y ($xGA$):** Risco Defensivo (Quanto mais para cima/valor menor, melhor).
* **Quadrante de Risco (Inferior-Esquerdo):** Baixo $xG/90$ (Ataque ineficiente) e Alto $xGA$ (Defesa vulnerável).

---

# Ferramentas Utilizadas
* **Interpretação de Dados Visuais** (Gráfico de Dispersão)
* **Métricas Avançadas de Futebol** (Ciência de Dados Esportivos)

---

# Principais Etapas
Utilizamos a interpretação de dados visuais (Gráficos de Dispersão $xG/90$ vs. $xGA$) para mapear a performance.

## 1. Definição das Métricas
Métricas Avançadas:
* **$xG/90$** (Gols Esperados por Jogo)
* **$xGA$** (Gols Esperados Contra)

## 2. Análise Preditiva
O quadrante inferior-esquerdo atua como um forte indicador de **risco de rebaixamento** (vulnerabilidade técnica).

## 3. Análise Comparativa
Comparação das posições dos times nas Rodadas 29, 30 e 38, focando nos times da Z-4 (17º ao 20º).

---

# 🔍 Critérios de Classificação e Resultados

Os resultados foram consolidados em uma visão progressiva da Rodada 29 à Rodada 38, destacando a **Estabilidade no Risco** e a **Performance de Escape**. 

| Time | Rodada 29 (Rk) | Rodada 30 (Rk) | Rodada 38 (Rk) | Status Final | Observação do Desempenho no Gráfico ($xG/xGA$) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Sport Recife** | 20º | 20º | 20º | **REBAIXADO** | Pior Categoria Consistente. Culminou com o pior $xGA$ (cerca de 63,5) e pior $xG/90$ (-0,7). |
| **Juventude** | 18º | 19º | 19º | **REBAIXADO** | Estabilidade no Risco. Sempre no quadrante mais perigoso (baixo $xG/90$, alto $xGA$) nas três rodadas analisadas. |
| **Fortaleza** | 19º | 18º | 18º | **REBAIXADO** | Risco Ofensivo. $xGA$ final (56,7) melhor que Sport/Juventude, mas com $xG/90$ negativo (-0,31). |
| **Ceará** | 13º | 14º | 17º | **REBAIXADO** | Queda por Pontos. Melhor desempenho técnico entre os rebaixados, com $xG/90$ quase zero e $xGA$ relativamente baixo. Caiu pela pontuação acumulada. |
| **Grêmio** | 12º | 11º | 9º | **ESCAPOU** | Alerta Defensivo Extremo. Apresentou o pior $xGA$ do campeonato na R38 (cerca de 59), indicando defesa altamente exposta. |
| **Vitória** | 17º | 17º | 15º | **ESCAPOU** | Escapada Crítica. No limite do quadrante perigoso na R29/R30. $xGA$ alto (53,3). |
| **Internacional** | 14º | 15º | 16º | **ESCAPOU** | Performance Técnica Forte. Desempenho no quadrante Superior-Direito ($xG/90$ positivo na R38). |

---

# Conclusão: Síntese da Análise Gráfica (Rodada 38)

## Rebaixamento por Ineficiência Total (Sport e Juventude)

> O **Sport Recife** e o **Juventude** foram os times com o pior desempenho técnico. Eles ocuparam o quadrante inferior esquerdo com os valores de $xGA$ mais altos e $xG/90$ mais negativos, indicando que sofreram muitas chances de gol e criaram poucas, sendo **consistentemente os mais vulneráveis** do campeonato.

## Rebaixamento por Falta de Pontos (Ceará e Fortaleza)

> **Ceará** e **Fortaleza** caíram com desempenho gráfico melhor do que os lanternas. O Ceará, em particular, tinha uma performance técnica quase mediana. Isso demonstra que, apesar de não serem os piores tecnicamente pelas métricas $xG/xGA$, a **falta de pontuação acumulada** foi o fator decisivo para a queda.

## O "Escape" Técnico e Risco Defensivo Extremo (Grêmio e Vitória)

> O **Grêmio** e o **Vitória** escaparam do rebaixamento pela pontuação. Contudo, ambos flertaram com a zona de perigo no gráfico, principalmente devido ao $xGA$ extremamente alto (Grêmio com o pior da liga na R38). Isso sugere que a segurança na tabela foi garantida por *overperformance* defensiva (goleiro/defesa se saindo melhor que o esperado) ou mérito ofensivo, e não pela **solidez defensiva consistente**.

---
