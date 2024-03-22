<h1 align="center">Resoluções</h1>

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17;
let y = 5;
let z = 8;

resultadoBooleano = (x < y && z > x) || x - y > z;
console.log(resultadoBooleano);

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);
```

Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime o resultado `false`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

<s>B) O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.</s>

C) O código avalia a expressão booleana, imprime o resultado `true` e verifica se o número 5 está presente na lista de números.

D) O código avalia a expressão booleana, imprime o resultado `false` e ordena a lista de números em ordem crescente.

**Resposta: b)**

---

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [1800, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento() {
  var gastos = [1800, 950, 620, 38];
  var totalGastos = gastos[0];
  var salario = 3500;
  var saldo = 0;
  var statusSaldo = "positivo";
  var i = 1;

  do {
    totalGastos += gastos[i];
    i++;
  } while (salario >= totalGastos && i < gastos.length);

  saldo = salario - totalGastos;

  if (saldo < 0) {
    statusSaldo = "negativo";
  }
  console.log(`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2() {
  var gastos = [1800, 950, 620, 38];
  var totalGastos = gastos[0];
  var salario = 3500;
  var statusSaldo = "positivo";
  var saldo = 0;
  var i = 1;

  while (salario >= totalGastos && i < gastos.length) {
    totalGastos += gastos[i];
    i++;
  }

  saldo = salario - totalGastos;
  if (saldo < 0) {
    statusSaldo = "negativo";
  }
  console.log(`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

A) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -1050.'

<s>B) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'</s>

C) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -100.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -1050.'

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

**Resposta: b)**

---

**3)** Considere o seguinte trecho de código em JavaScript:

```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

Qual das seguintes alternativas é a descrição mais precisa do que o código faz?

A) O código verifica se o número é divisível por 3 e, se for, exibe a mensagem "O número é divisível por 3!".

B) O código verifica se o número é par ou ímpar. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!".

C) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!". Se for ímpar, exibe a mensagem "O número é ímpar e não é divisível por 3!".

<s>D) O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".</s>

**Resposta: d)**

---

**4)** Qual será o resultado impresso no console após a execução desse código?

```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
  var valorCompra = valorCompras[i];

  if (valorCompra <= saldo) {
    console.log(
      "Compra " +
        (i + 1) +
        " aprovada. Saldo restante: " +
        (saldo - valorCompra)
    );
    saldo -= valorCompra;
  } else if (valorCompra <= saldo + limiteCredito) {
    console.log(
      "Compra " +
        (i + 1) +
        " aprovada com limite de crédito. Saldo restante: " +
        (saldo + limiteCredito - valorCompra)
    );
    saldo = 0;
    limiteCredito -= valorCompra - saldo;
  } else {
    console.log(
      "Compra " +
        (i + 1) +
        " negada. Saldo insuficiente e limite de crédito excedido."
    );
  }
}
```

Escolha a opção que responde corretamente:

A)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 aprovada. Saldo restante: -200

B)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

C)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

<s>D)

Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada. Saldo restante: 0

Compra 3 aprovada com limite de crédito. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.</s>

**Resposta: d)**

---

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

A) Setup -> Update -> Draw

<s>B) Preload -> Create -> Update</s>

C) Load -> Initialize -> Render

D) Begin -> Play -> End

**Resposta: b)**

---

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Renderizar gráficos 3D para jogos em HTML5.

<s>B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.</s>

C) Criar efeitos de áudio para melhorar a experiência do usuário em jogos.

D) Gerenciar a lógica do jogo e a sincronização de eventos em jogos multiplayer.

---

# Questões dissertativas

**7)** Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem.
![Uma imagem](assets/image.png)

**Resposta:**

```
Algoritmo "Fluxograma"

var idade <- 0

inicio

leia idade

se idade < 16:<br>
    escreva("Não pode votar!")<br>
senão se idade >= 16 e idade < 18:<br>
    escreva("Voto facultativo")<br>
senão:<br>
    escreva("Voto obrigatório")<br>
fimse

fimalgoritmo
```

---

**8)** Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

```
Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

```

**Resposta:**

```
Algoritmo "Geometria"

Classe Circulo extendido de FormaGeometrica:
    Atributos:
        - pi = 3.14

    Método Construtor(cor):
        chama o Construtor da classe pai com o parâmetro cor
    fimmetodo

    Método CalcularArea(raio):
        retorna pi * raio * raio
    fimmetodo
fimclasse

Classe Retangulo extendido de FormaGeometrica:
    Atributos:
        - base
        - altura

    Método Construtor(cor):
        chama o Construtor da classe pai com o parâmetro cor
    fimmetodo

    Método CalcularArea(base, altura):
        retorna base * altura
    fimmetodo
fimclasse

// Criando uma instância da classe Circulo
var circulo1 = novo Circulo("vermelho")
var raio_circulo1 = 5
var area_circulo1 = circulo1.CalcularArea(raio_circulo1)
imprimir("Área do círculo:", area_circulo1)

// Criando uma instância da classe Retangulo
var retangulo1 = novo Retangulo("azul")
var base_retangulo1 = 4
var altura_retangulo1 = 6
area_retangulo1 = retangulo1.CalcularArea(base_retangulo1, altura_retangulo1)
imprimir("Área do retângulo:", area_retangulo1)

fimalgoritmo
```

---

**9)** Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

Considere a fórumla de atualização velocidade:

```
Algoritmo Simulador_Carro_Elétrico
    // Entradas
    velocidade_inicial = Ler_Velocidade_Inicial()
    taxa_aceleracao = Ler_Taxa_Aceleracao()
    distancia = Ler_Distancia()
    velocidade_maxima = Ler_Velocidade_Maxima()
    tempo_maximo = Ler_Tempo_Maximo()

    // Variáveis
    velocidade_atual = velocidade_inicial
    tempo = 0
    distancia_percorrida = 0

    Enquanto (distancia_percorrida < distancia) E (tempo <= tempo_maximo) E (velocidade_atual < velocidade_maxima) faça
        // Calcular nova velocidade e distância percorrida
        velocidade_atual = velocidade_atual + taxa_aceleracao * tempo
        distancia_percorrida = distancia_percorrida + velocidade_atual * tempo
        tempo = tempo + 1 // Incrementar tempo em minutos
    Fim Enquanto

    Se (distancia_percorrida >= distancia) Então
        Escrever "O carro completou a corrida em ", tempo, " minutos."
    Senão
        Se (tempo > tempo_maximo) Então
            Escrever "O carro não completou a corrida dentro do tempo máximo permitido."
        Senão
            Escrever "O carro atingiu a velocidade máxima permitida."
        Fim Se
    Fim Se

FimAlgoritmo
```

---

**10)** Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.

```
Função SomaDeMatrizes(matrizA, matrizB):
    # Verifica se as duas matrizes têm o mesmo número de linhas e colunas
    Se tamanho(matrizA) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser somadas. Elas têm dimensões diferentes."
    Senão:
        linhas <- tamanho(matrizA)
        colunas <- tamanho(matrizA[0]) # Considerando que todas as linhas têm o mesmo número de colunas
        matrizResultado <- novaMatriz(linhas, colunas)

        # Loop para percorrer cada elemento das matrizes e calcular a soma
        Para i de 0 até linhas-1 faça:
            Para j de 0 até colunas-1 faça:
                matrizResultado[i][j] <- matrizA[i][j] + matrizB[i][j]

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizSoma <- SomaDeMatrizes(matrizA, matrizB)
Escrever("Soma das matrizes:")
ImprimirMatriz(matrizSoma)
```

```
Algoritmo Multiplicacao_de_matrizes

Função MultiplicaçãoDeMatrizes(matrizA, matrizB):
    # Verifica se o número de colunas em matrizA é igual ao número de linhas em matrizB
    Se tamanho(matrizA[0]) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser multiplicadas. Dimensões incompatíveis."
    Senão:
        linhasA <- tamanho(matrizA)
        colunasA <- tamanho(matrizA[0])
        colunasB <- tamanho(matrizB[0])
        matrizResultado <- novaMatriz(linhasA, colunasB)

        # Loop para percorrer cada elemento da matriz resultado
        Para i de 0 até linhasA-1 faça:
            Para j de 0 até colunasB-1 faça:
                # Inicializa o elemento da matriz resultado como 0
                matrizResultado[i][j] <- 0
                Para k de 0 até colunasA-1 faça:
                    # Calcula o produto da linha i de matrizA com a coluna j de matrizB
                    matrizResultado[i][j] <- matrizResultado[i][j] + (matrizA[i][k] * matrizB[k][j])

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizProduto <- MultiplicaçãoDeMatrizes(matrizA, matrizB)
Escrever("Produto das matrizes:")
ImprimirMatriz(matrizProduto)

fimalgoritimo
```