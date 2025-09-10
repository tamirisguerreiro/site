---
layout: default
---

# 💡 Chega de treinar no escuro!

Pare de adivinhar seu treino de corrida. Fiz uma calculadora de zonas de treinamento de corrida através da Velocidade Aeróbica Máxima (VAM) para facilitar a vida do Profissional de Educação Física que queira utilizá-la. A ferramenta te permite ter um treino mais preciso e baseado em dados. 

Essa métrica auxilia a ter um melhor direcionamento na prescrição de treinos quando bem empregada e colabora para impulsionar a performance. Com essa ferramenta, você foca em conhecer e aprender um pouco mais sobre sua velocidade em cada zona de treinamento de maneira totalmente individualizada.

Atenção: A calculadora é uma excelente ferramenta de apoio, mas lembre-se que o único profissional habilitado a prescrever treinos e a interpretar esses dados de forma individualizada é o Profissional de Educação Física.

---

###  Como o Código Acontece

O código abaixo usa a VAM para calcular seis zonas de treinamento, cada uma com um objetivo específico (da recuperação à velocidade de pico). Mas, para que a calculadora funcione de forma confiável, combinamos a lógica de cálculo com as ferramentas de tratamento de erros do Python, como o **`try`** e o **`except`**.

1.  #### O Bloco `try`

O bloco `try` busca executar um pedaço do código que pode falhar.

**O que está no `try`:**

* **Entrada de Dados:** O programa pede a sua VAM. O Python tenta converter a sua resposta para um número decimal (`float`).
* **O Cálculo:** Se a conversão for bem-sucedida, o código calcula as faixas de velocidade para cada uma das seis zonas de treino (Zona 1 a Zona 6), multiplicando a sua VAM por porcentagens predefinidas.
* **Exibição dos Resultados:** Por fim, o programa exibe todas as zonas de treinamento em um formato amigável.

2.  #### O Bloco `except`

O `except` é para resolver problemas se algo der errado no bloco `try`.

`except ValueError:`

* Este bloco é programado para capturar especificamente um erro do tipo `ValueError`.
* O `ValueError` acontece quando você tenta converter um valor que não é um número para `float`. Por exemplo, se você digitar "dez" em vez de "10", a conversão falha, e o erro é ativado.
* Quando o `ValueError` é capturado, o programa interrompe a execução do `try` e executa o código dentro do `except`.

**O Resultado:**

Em vez de o programa travar e exibir uma mensagem técnica de erro, o usuário recebe uma mensagem clara e objetiva para resolver o problema apresentado: `print("Erro: Por favor, insira um valor numérico para a VAM.")`.

[Calcule suas Zonas de Treinamento por sua Velocidade Aeróbica Máxima](https://colab.research.google.com/drive/1va0C7A1hZIgFH8lKwo9zjTtMp2hQLSkJ?usp=sharing)

[Página Inicial](https://tamirisguerreiro.github.io/site)
