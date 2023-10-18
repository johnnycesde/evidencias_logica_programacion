<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->

## Actividad: Ejercicios de Lógica de Programación
1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

~~~java

public class Ejercicio1 {

 public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 5, 3};

        // Creamos una variable para almacenar el número que aparece más de una vez
        int numeroRepetido = 0;

        // Recorremos el conjunto de números
        for (int i = 0; i < numeros.length; i++) {
            // Comprobamos si el número actual ya ha aparecido
            for (int j = 0; j < i; j++) {
                if (numeros[i] == numeros[j]) {
                    // El número actual ya ha aparecido
                    numeroRepetido = numeros[i];
                    break;
                }
            }
        }

        // Si el número repetido es distinto de 0, lo imprimimos
        if (numeroRepetido != 0) {
            System.out.println("El número repetido es: " + numeroRepetido);
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
    }
}
~~~

1. Comprender como se pasa de decimal a binario.
~~~java
Escribe el número decimal.

Divide el número decimal por 2 y registra el cociente y el residuo (resto).

Continúa dividiendo el cociente obtenido en el paso anterior por 2 y registra el nuevo cociente y el nuevo residuo.

Repite este proceso hasta que el cociente sea igual a 0.

Lee los residuos de abajo hacia arriba para obtener la representación binaria.

Aquí tienes un ejemplo de cómo convertir el número decimal 14 a binario:
~~~
~~~java
Paso 1: Escribe el número decimal.
Decimal: 14

Paso 2: Divide 14 por 2.
14 ÷ 2 = 7 con un residuo de 0

Paso 3: Divide 7 (el cociente) por 2.
7 ÷ 2 = 3 con un residuo de 1

Paso 4: Divide 3 (el nuevo cociente) por 2.
3 ÷ 2 = 1 con un residuo de 1

Paso 5: Divide 1 (el nuevo cociente) por 2.
1 ÷ 2 = 0 con un residuo de 1

El cociente ha llegado a 0, por lo que hemos terminado.

Leyendo los residuos de abajo hacia arriba, obtenemos la representación binaria: 1110

~~~
1.1 Desarrollar un algoritmo que realice la conversión de binario a decimal.

Para convertir un número binario, como "1000," a su equivalente en decimal, puedes utilizar el siguiente proceso:
~~~java
Escribe el número binario. "1000"

Asigna un valor a cada dígito binario, comenzando desde la derecha y aumentando en potencias de 2. Comienza con 2^0 y aumenta en una unidad para cada dígito que te desplazas hacia la izquierda.

Multiplica cada dígito binario por el valor correspondiente y suma los resultados.

Aquí tienes un ejemplo con "1000" en binario:


  1  0  0  0
  |  |  |  |
2^3 2^2 2^1 2^0
Ahora, realiza las multiplicaciones y sumas:

1 * 2^3 = 1 * 8 = 8
0 * 2^2 = 0 * 4 = 0
0 * 2^1 = 0 * 2 = 0
0 * 2^0 = 0 * 1 = 0
Luego, suma los resultados:

8 + 0 + 0 + 0 = 8

Por lo tanto, "1000" en binario es igual a "8" en decimal.
~~~
~~~java
public class BinarioADecimal {

    public static void main(String[] args) {
        // Definimos el número binario como una cadena
        String binario = "1000";
        
        // Inicializamos la variable para almacenar el resultado en decimal
        int decimal = 0;
        
        // Recorremos los dígitos binarios desde el más a la izquierda
        for (int i = 0; i < binario.length(); i++) {
            // Obtenemos el dígito binario actual
            char digito = binario.charAt(i);
            
            // Convertimos el carácter en un valor numérico (0 o 1)
            int valorDigito = Character.getNumericValue(digito);
            
            // Calculamos el valor en decimal y lo sumamos al resultado
            decimal = decimal * 2 + valorDigito;
        }
        
        // Imprimimos el resultado en decimal
        System.out.println("El número binario " + binario + " en decimal es: " + decimal);
    }
}
~~~