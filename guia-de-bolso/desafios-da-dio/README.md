<div align="center">
    <img src="banner.png" width="500px" />
</div><br>

&nbsp;&nbsp;&nbsp;&nbsp;Vou explicar como funcionam alguns mecanismos de entrada dos desafios da plataforma.

## Entradas

&nbsp;&nbsp;&nbsp;&nbsp;Todos os desafios possuem maneiras diferentes de entrada de dados, ou seja, todos os valores que o desafio mostra em cada teste:

-	Entram por alguma função (método) de entrada;
-	Passam pelo nosso código;
-	Saem por alguma função (método) de saída.

## Métodos de entrada

&nbsp;&nbsp;&nbsp;&nbsp;Dependendo da linguagem de programação que você esteja aprendendo o método de entrada é diferente. Aqui abaixo tem uma pequena lista com a linguagem e o método de entrada.

### JavaScript `gets()`
~~~javascript
const entrada = gets();
~~~
##

### Java `new Scanner(System.in)`
~~~java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);        
    }
}
~~~
##

### Kotlin `readLine()`
~~~kotlin
fun main() {
    val entrada = readLine()!! // Forma assertiva
}
~~~
~~~kotlin
fun main() {
    val entrada = readLine() ?: "" // Forma assegurada
}
~~~


&nbsp;&nbsp;&nbsp;&nbsp;Lembrando que `gets( )` é uma função que funciona apenas na plataforma para Javascript.

<br>

## Exemplos de entrada

&nbsp;&nbsp;&nbsp;&nbsp;Supondo que tenhamos um arquivo de entrada:
~~~txt
abacaxi
banana
cereja
~~~

&nbsp;&nbsp;&nbsp;&nbsp;Onde precisamos pegar os valores de cada linha e guardar em uma variável, como faríamos?

### JavaScript
~~~javascript
const entrada1 = gets(); // abacaxi
const entrada2 = gets(); // banana
const entrada3 = gets(); // cereja
~~~
##
### Java
~~~java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        String entrada1 = entrada.nextLine(); // abacaxi
        String entrada2 = entrada.nextLine(); // banana
        String entrada3 = entrada.nextLine(); // cereja
        entrada.close();
    }
}
~~~
##
### Kotlin
~~~kotlin
fun main() {
    val entrada1 = readLine() ?: "" // abacaxi
    val entrada2 = readLine() ?: "" // banana
    val entrada3 = readLine() ?: "" // cereja
}
~~~
<br>

## Exemplo com o código de soma
&nbsp;&nbsp;&nbsp;&nbsp;A partir de agora vamos fazer um código de soma simples e entender alguns comportamentos de entrada e de saída.

### Entrada
~~~txt
15
20
7
~~~

### Algoritmo
~~~txt
INÍCIO DO PROCESSO
    > Armazenar a primeira entrada.
    > Não armazenar a segunda entrada.
    > Armazenar a terceira entrada.
    > Armazenar a soma da primeira com a terceira entrada.
    > Exibir o resultado do cálculo.
FIM DO PROCESSO
~~~

&nbsp;&nbsp;&nbsp;&nbsp;Para que possamos "pular" a segunda entrada basta executar a função de entrada sem nunca atribui-la a uma variável, dessa maneira a entrada é obtida, porém nunca armazenada.

### JavaScript
~~~javascript
const entrada1 = Number(gets()); // 15
gets(); // "20"
const entrada2 = Number(gets()); // 7

const soma = entrada1 + entrada2;
console.log(soma); // 22
~~~
##
### Java
~~~java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        int entrada1 = entrada.nextInt(); // 15
        entrada.nextInt(); // 20
        int entrada3 = entrada.nextInt(); // 7
        entrada.close();

        System.out.println(entrada1 + entrada3); // 22
    }
}
~~~
##
### Kotlin

~~~kotlin
fun main() {
    val entrada1 = readLine()?.toInt() ?: 0 // 15
    readLine() // "20"
    val entrada3 = readLine()?.toInt() ?: 0 // 7

    println(entrada1 + entrada2) // 22
}
~~~

&nbsp;&nbsp;&nbsp;&nbsp;Caso mudemos a entrada o nosso código deverá exibir a saída esperada para cada ocasião.

### Exemplos
&nbsp;&nbsp;&nbsp;&nbsp;Considerando o algoritmo acima que "pula" a segunda entrada temos:

<span align="center">

***Teste 1***

</span>

*Entrada*
~~~txt
10
20
30
~~~
*Saída esperada*
~~~txt
40
~~~

##

<span align="center">

***Teste 2***

</span>

*Entrada*
~~~txt
55
4890
15
~~~
*Saída esperada*
~~~txt
70
~~~

&nbsp;&nbsp;&nbsp;&nbsp;Logo o código feito para cada linguagem daria certo em ambos os testes, pois sempre entrariam a primeira e a terceira linha de entrada, faria-se a soma e seria por fim exibido o resultado que é igual a saída esperada por cada teste.

### Observações
&nbsp;&nbsp;&nbsp;&nbsp;Existem maneiras diferentes de obter dados numéricos em cada linguagem é sempre interessante que você pesquise as várias formas que não foram abordadas aqui, pois a finalidade é explicar da forma mais simples.

<br>

<div align="center">
    
Feito com ❤️ por mim.

**Josélio de S. C. Júnior - 2021**

</div>
