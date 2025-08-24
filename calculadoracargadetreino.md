---
layout: default
---

# 💪 📒Calculadora de Carga de Treino: 1RM Preditivo com o Teste de Munaro (2002)

Se você treina força, já deve ter ouvido falar alguma vez sobre o teste de uma **Repetição Máxima** (RM), que é a carga máxima que você consegue levantar apenas uma única vez — um risco que não vale a pena testar em grande parcela da população.

Felizmente, a ciência do esporte tem métodos para **predizer essa carga máxima com segurança**. Existem vários testes preditivos; o que iremos utilizar é o teste baseado na pesquisa do brasileiro **Munaro (2002)**.

---

# A Regra de Ouro do Munaro

A fórmula usada é uma variação da famosa equação de Epley:

$$RM_{preditivo} = (0.0333 \times número_{repetições} \times carga_{utilizada}) + carga_{utilizada}$$

⚠️ **Atenção à Regra de Validade:** De acordo com o estudo, essa predição só é válida se a carga utilizada permitir um número de repetições **menor ou igual a 20!** Acima disso, não será possível realizar o cálculo como previsto.

Para garantir que a calculadora funcione de forma segura e científica, combinamos a precisão da fórmula com o tratamento de erros da linguagem **Python**, usando as poderosas funções **`try`**, **`if`** e **`except`**.

Veja como a mágica do código acontece!

---

# 🚀 Passo a Passo:

## 1. O Bloco `try` (Tentativa e Risco)

O `try` é o ponto de partida. Ele tenta executar um bloco de código que pode gerar erros.

O que está no `try`:

* **Entrada de Dados:** Pedi ao usuário a `carga_utilizada` e o `numero_rep`. Se o usuário digitar, por exemplo, a palavra "cem" em vez de "100", a conversão para `float()` falha.
* **O Cálculo:** A fórmula de Munaro (2002) é executada.
* **A Validação:** O código verifica se a regra das 20 repetições foi violada.

## 2. A Função `if`

A função `if` é a validade científica do cálculo.

if numero_rep > 20:
    raise ValueError("A carga não pode ser maior que 20 repetições.")
    O Teste: O **if** verifica estritamente: Se o número de repetições for maior que 20, a regra é violada.

O Resultado: Se a condição for Verdadeira, o **if** aciona o... **raise**.

---
## 3. O Comando `raise` (Forçando um Erro Lógico)

O comando **`raise`** é usado para interromper o código e criar um erro proposital.

Quando o **if** detecta que `numero_rep > 20`, o **`raise ValueError`** é ativado.

* **Por que `raise`?** O cálculo matemático em si não tem erro, mas o resultado **não será cientificamente válido** (segundo Munaro, 2002). O **`raise`** transforma esse erro lógico/científico em um **erro de programação**.

---

## 4. O Bloco `except` (O Tratamento Amigável)

O **`except`** só é ativado quando o `try` falha (seja por um erro nativo ou forçado).

except ValueError:
    print("Erro: Por favor, insira um valor válido.")
O except ValueError é inteligente, pois ele captura dois tipos de erro com a mesma resposta amigável:

---
Erro de Digitação: Captura o erro nativo que ocorre quando o float(input()) tenta converter um texto não numérico.

Erro de Validação: Captura o erro que você forçou (raise ValueError) quando o número de repetições ultrapassou 20.

Resultado: Em vez de o programa "quebrar", o usuário recebe uma mensagem amigável informando que ele precisa seguir as regras do teste para ter um resultado preciso.

Calculadora de Treino (Abrir no Colab)
