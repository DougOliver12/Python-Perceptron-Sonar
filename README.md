# Python-Perceptron-Sonar
O algoritmo Perceptron é o tipo mais simples de rede neural artificial.  É um modelo de um único neurônio que pode ser usado para problemas de classificação de duas classes e fornece a base para o desenvolvimento posterior de redes muito maiores.
Descrição
Esta seção fornece uma breve introdução ao algoritmo Perceptron e ao conjunto de dados do Sonar ao qual o aplicaremos posteriormente.

# Algoritmo de Perceptron

O Perceptron é inspirado no processamento de informações de uma única célula neural chamada neurônio.
Um neurônio aceita sinais de entrada através de seus dendritos, que passam o sinal elétrico para o corpo da célula.
De maneira semelhante, o Perceptron recebe sinais de entrada de exemplos de dados de treinamento que pesamos e combinamos em uma equação linear chamada ativação.
A ativação é então transformada em um valor ou previsão de saída usando uma função de transferência, como a função de transferência por etapas.
Dessa maneira, o Perceptron é um algoritmo de classificação para problemas com duas classes (0 e 1), onde uma equação linear (como ou hiperplano) pode ser usada para separar as duas classes.
Está intimamente relacionado à regressão linear e à regressão logística que fazem previsões de maneira semelhante (por exemplo, uma soma ponderada de entradas).
Os pesos do algoritmo Perceptron devem ser estimados a partir dos seus dados de treinamento usando a descida estocástica do gradiente.

# Descida de gradiente estocástico (stochastic gradient descent)

A descida do gradiente é o processo de minimizar uma função seguindo os gradientes da função de custo.
Isso envolve conhecer a forma do custo e da derivada, para que, a partir de um determinado ponto, você conheça o gradiente e possa se mover nessa direção, por exemplo, descendo em direção ao valor mínimo.
No aprendizado de máquina, podemos usar uma técnica que avalia e atualiza os pesos de cada iteração chamada descida de gradiente estocástico para minimizar o erro de um modelo em nossos dados de treinamento.
A maneira como esse algoritmo de otimização funciona é que cada instância de treinamento seja mostrada no modelo, uma de cada vez. O modelo faz uma previsão para uma instância de treinamento, o erro é calculado e o modelo é atualizado para reduzir o erro para a próxima previsão.
Este procedimento pode ser usado para encontrar o conjunto de pesos em um modelo que resulta no menor erro do modelo nos dados de treinamento.
Para o algoritmo Perceptron, a cada iteração, os pesos ( w ) são atualizados usando a equação:

w = w + learning_rate * (expected - predicted) * x

Onde w está otimizando o peso, learning_rate é uma taxa de aprendizado que você deve configurar (por exemplo, 0,01), (esperado - previsto) é o erro de previsão para o modelo nos dados de treinamento atribuídos ao peso e x é o valor de entrada.

# Conjunto de dados do sonar

O conjunto de dados que usaremos neste tutorial é o conjunto de dados do Sonar.
Este é um conjunto de dados que descreve retornos sonoros retornando de serviços diferentes. As 60 variáveis de entrada são a força dos retornos em diferentes ângulos. É um problema de classificação binária que requer um modelo para diferenciar rochas de cilindros metálicos.
É um conjunto de dados bem compreendido. Todas as variáveis são contínuas e geralmente na faixa de 0 a 1. Portanto, não precisamos normalizar os dados de entrada, o que geralmente é uma boa prática com o algoritmo Perceptron. A variável de saída é uma string "M" para mines e "R" para rock, que precisará ser convertida nos números inteiros 1 e 0.
Ao prever a classe com mais observações no conjunto de dados (M ou minas), o algoritmo de regra zero pode atingir uma precisão de 53%.
Você pode aprender mais sobre esse conjunto de dados no repositório do UCI Machine Learning . Você pode baixar o conjunto de dados gratuitamente e colocá-lo em seu diretório de trabalho com o nome de arquivo sonar.all-data.csv.
