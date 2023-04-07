# 1. Tipos de dados primitivos

No Java, os tipos de dados primitivos são os blocos de construção fundamentais para trabalhar com variáveis e armazenar 
informações. Esses tipos são predefinidos pela linguagem e são utilizados para representar valores simples, como números 
inteiros, números de ponto flutuante, caracteres e valores booleanos. Neste conteúdo aprofundado, vamos explorar os 
tipos de dados primitivos em Java e fornecer exemplos para ajudar você a entender melhor como utilizá-los.

## 1.1. Tipos numéricos inteiros

No Java, existem quatro tipos de dados primitivos para representar números inteiros: `byte`, `short`, `int` e `long`.

### 1.1.1. `byte`

O tipo `byte` é um número inteiro de **8 bits**, com sinal, que pode armazenar valores no intervalo de -128 a 127. É útil 
quando se deseja economizar memória em arrays grandes.

```java
byte age = 28;
byte numberOfMonths = 12;
```

### 1.1.2. `short`

O tipo `short` é um número inteiro de **16 bits**, com sinal, que pode armazenar valores no intervalo de -32.768 a 32.767. 
É útil quando se deseja economizar memória e o intervalo de valores é suficiente.


```java
short monthlySalary = 32000;
short daysInYear = 365;
```

### 1.1.3. `int`

O tipo `int` é um número inteiro de **32 bits**, com sinal, que pode armazenar valores no intervalo 
de -2.147.483.648 a 2.147.483.647. É o tipo numérico inteiro mais comum usado no Java.


```java
int population = 987654321;
int maxInteger = 2147483647;
```

### 1.4. `long`

O tipo `long` é um número inteiro de **64 bits**, com sinal, que pode armazenar valores no intervalo 
de -9.223.372.036.854.775.808 a 9.223.372.036.854.775.807. É útil quando se trabalha com números inteiros muito grandes.


```java
long distanceInMeters = 384400000L;
long maxLongValue = 9223372036854775807L;
```

## 1.2. Tipos numéricos de ponto flutuante

No Java, existem dois tipos de dados primitivos para representar números de ponto flutuante: `float` e `double`.

### 1.2.1. `float`

O tipo `float` é um número de ponto flutuante de _precisão simples_ de **32 bits**, que segue o padrão _IEEE 754_. 
É útil quando se deseja economizar memória e a precisão é suficiente.


```java
float pi = 3.1415926F;
float earthRadius = 6371.0F;
```

### 1.2.2. `double`

O tipo `double` é um número de ponto flutuante de _precisão dupla_ de **64 bits**, que segue o padrão _IEEE 754_. 
É o tipo numérico de ponto flutuante mais comum usado no Java.


```java
double speedOfLight = 299792458.0;
double electronMass = 9.10938356E-31;
```


## 1.3. Tipo `char`

O tipo `char` é um valor Unicode de **16 bits** que representa um caractere. Pode armazenar valores no intervalo 
de 0 a 65.535. É utilizado para representar caracteres individuais, como letras, dígitos e símbolos.

```java
char letterA = 'A';
char digit9 = '9';
char symbol = '#';
```


## 1.4. Tipo `boolean`

O tipo `boolean` é um valor lógico que representa **verdadeiro** ou **falso**. É utilizado para representar condições e 
resultados de operações lógicas.

```java
boolean isJavaFun = true;
boolean isNegative = false;
```

## 1.5. Autoboxing e unboxing

A partir do Java 5, o processo de conversão automática entre tipos primitivos e seus equivalentes de classes 
wrapper (objetos) é chamado de **autoboxing** e **unboxing**. Por exemplo, `Integer` é a classe wrapper para o tipo primitivo `int`. 
O compilador cuida dessas conversões automaticamente, facilitando a manipulação de tipos primitivos e objetos em 
determinadas situações, como em coleções genéricas.

Exemplo de autoboxing e unboxing:

```java
// Autoboxing: o compilador converte int para Integer automaticamente
int intValue = 42;
Integer integerObject = intValue;

// Unboxing: o compilador converte Integer para int automaticamente
Integer anotherIntegerObject = 84;
int anotherIntValue = anotherIntegerObject;
```

## 1.6. Operações bitwise

Os tipos numéricos inteiros (`byte`, `short`, `int` e `long`) suportam operações bitwise, que são operações realizadas 
diretamente nos bits que compõem os valores. Essas operações incluem AND bitwise (`&`), OR bitwise (`|`), 
XOR bitwise (`^`), deslocamento à esquerda (`<<`), deslocamento à direita (`>>`) e deslocamento à direita 
sem sinal (`>>>`). Essas operações são importantes para manipulação de bits e otimizações em algoritmos específicos.

Exemplo de operações bitwise:

```java
int a = 0b1100; // 12 em decimal
int b = 0b1010; // 10 em decimal

int andResult = a & b; // 0b1000 (8 em decimal)
int orResult = a | b; // 0b1110 (14 em decimal)
int xorResult = a ^ b; // 0b0110 (6 em decimal)
int leftShiftResult = a << 1; // 0b11000 (24 em decimal)
int rightShiftResult = a >> 1; // 0b0110 (6 em decimal)
int unsignedRightShiftResult = a >>> 1; // 0b0110 (6 em decimal)
```

## 1.7. Literais de tipos primitivos

É possível escrever literais de tipos primitivos de diferentes maneiras, usando diferentes bases numéricas ou 
notações científicas. Por exemplo, para `int`, `long`, `float` e `double`, você pode usar a notação decimal **(base 10)**, 
a notação hexadecimal **(base 16)** com o prefixo `0x` ou `0X`, a notação octal **(base 8)** com o prefixo `0`, ou a notação 
binária **(base 2)** com o prefixo `0b` ou `0B`. Para float e double, também é possível usar a notação científica.

Exemplo de literais de tipos primitivos:

```java
int decimalInt = 42;
int hexInt = 0x2A;
int octalInt = 052;
int binaryInt = 0b101010;

long decimalLong = 9876543210L;
long hexLong = 0x240C_A1B9AL;
long octalLong = 043_142_073_532L
long binaryLong = 0b10010000110010100001101110011010L;

float decimalFloat = 3.1415926F;
float scientificNotationFloat = 3.1415926E0F;
float hexFloat = 0x1.921FB4p1F;

double decimalDouble = 3.141592653589793;
double scientificNotationDouble = 3.141592653589793E0;
double hexDouble = 0x1.921FB54442D18p1;
```

## 1.8. Conversão e promoção de tipos primitivos

É possível converter e promover tipos primitivos em Java, o que permite a realização de operações entre diferentes 
tipos de dados. A promoção de tipos ocorre automaticamente em certas situações, como quando um tipo de dado menor é 
atribuído a um tipo de dado maior. No entanto, a conversão de tipos _(casting)_ é necessária quando se deseja 
converter explicitamente um tipo de dado maior para um tipo menor ou um tipo de dado com maior precisão para um 
tipo de dado com menor precisão.

Exemplo de promoção de tipos:

```java
int intValue = 42;
double doubleValue = intValue; // Promove automaticamente intValue de int para double
```

Exemplo de conversão de tipos (casting):
```java
double doubleValue = 42.5;
int intValue = (int) doubleValue; // Converte explicitamente doubleValue de double para int, truncando a parte decimal
```

## 1.9. Overflow

O overflow é uma condição que ocorre quando uma operação matemática resulta em um valor que excede o limite superior 
(ou inferior) do tipo de dado primitivo em questão. Quando ocorre um overflow, o valor armazenado geralmente é 
incorreto, pois ele "enrola" para o início (ou final) do intervalo permitido do tipo de dado. É importante estar 
ciente das possibilidades de overflow ao realizar operações matemáticas com tipos de dados primitivos.

### **Operações aritméticas:**

As operações aritméticas, como adição, subtração, multiplicação e divisão, podem causar overflow se o resultado 
exceder o intervalo permitido do tipo de dado. No entanto, em Java, o overflow não gera exceções nem erros de 
compilação ou tempo de execução. É responsabilidade do programador verificar se há possíveis condições de overflow 
e lidar com elas adequadamente.

```java
int maxValue = Integer.MAX_VALUE; // 2147483647
int overflow = maxValue + 1; // Ocorre um overflow, e o resultado é -2147483648

```

### **Conversão de tipos (casting):**

Ao converter explicitamente um tipo de dado maior ou de maior precisão para um tipo de dado menor ou de menor 
precisão, você deve estar ciente do risco de overflow. Nesses casos, a parte do valor que excede o intervalo 
permitido do tipo de destino será truncada, resultando em um valor possivelmente incorreto.

Exemplo de overflow ao converter tipos:
```java
long bigLongValue = 2_147_483_648L;
int overflowedIntValue = (int) bigLongValue; // Ocorre um overflow, e o resultado é -2_147_483_648
```

### **Prevenção de overflow:**

Para evitar o overflow, você pode adotar várias estratégias, como verificar os valores antes de realizar operações 
matemáticas, utilizar tipos de dados maiores (por exemplo, usar `long` em vez de `int`), ou utilizar a 
classe `java.math.BigInteger` ou `java.math.BigDecimal` para realizar operações matemáticas com precisão arbitrária.

A partir do **Java 8**, você pode utilizar os métodos `Math.addExact`, `Math.subtractExact` e `Math.multiplyExact` 
para realizar operações matemáticas que geram uma exceção `ArithmeticException` caso ocorra um overflow.

Exemplo de prevenção de overflow usando métodos Math:
```java
int maxValue = Integer.MAX_VALUE;
try {
    int result = Math.addExact(maxValue, 1);
} catch (ArithmeticException e) {
    System.out.println("Ocorreu um overflow");
}
```

## 1.10. Tabela de tipos primitivos

| Tipo primitivo | Tipo                  | Valor mínimo               | Valor máximo              | Valor padrão |
|----------------|-----------------------|----------------------------|---------------------------|--------------|
| byte           | 8-bit integral        | -128                       | 127                       | 0            |
| short          | 16-bit integral       | -32,768                    | 32,767                    | 0            |
| int            | 32-bit integral       | -2,147,483,648             | 2,147,483,647             | 0            |
| long           | 64-bit integral       | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 | 0L           |
| float          | 32-bit floating-point | ~-3.4028235E+38            | ~3.4028235E+38            | 0.0f         |
| double         | 64-bit floating-point | ~-1.7976931348623157E+308  | ~1.7976931348623157E+308  | 0.0          |
| char           | 16-bit Unicode        | 0                          | 65,535                    | '\u0000'     |
| boolean        | true ou false         | N/A                        | N/A                       | false        |
