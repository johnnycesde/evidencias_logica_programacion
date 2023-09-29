<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->
# Ejercicios - while

1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.



```java
import java.util.Scanner;
public class Johnnyactiv5log {
 public static void main(String[] args) {
        
        
        Scanner scanner = new Scanner(System.in);

        
        System.out.print("Ingrese un número: ");
        int numero = scanner.nextInt();

        
        System.out.println("Tabla de multiplicar del " + numero + ":");
        int i = 1;
        
        while (i <= 10) {
            int resultado = numero * i;
            System.out.println(numero + " x " + i + " = " + resultado);
            i++;
        }

        
    }
}
~~~
2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.
 
 ~~~java
 import java.util.Scanner;
public class Johnnyactiv5log {
 public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Ingrese una cadena de caracteres: ");
        String cadena = scanner.nextLine();
        
        int contador = 0;
        int i = 0;
        
        while (i < cadena.length()) {
            char caracter = cadena.charAt(i);
            
            
            if (Character.isDigit(caracter)) {
                contador++;
            }
            
            i++; 
        }
        
        System.out.println("La cantidad de caracteres que son números es: " + contador);
        
        
    }
}
```

# Ejercicios - do while
1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.
```java
import java.util.Scanner;
public class Johnnyactiv5log {
public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int numero = 1;
        
        do {
            System.out.println(numero);
            numero++;
            
            System.out.print("Introduce un número negativo para detener el programa: ");
            int entrada = scanner.nextInt();
            
            if (entrada < 0) {
                System.out.println("Programa detenido.");
                break;
            }
        } while (numero <= 100);
        
        
    }
}
```

2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

~~~java
import java.util.Scanner;

public class Johnnyactiv5log {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        int numero;

        do {
            System.out.print("Ingrese un número entero (0 para salir): ");
            numero = scanner.nextInt();

            if (numero != 0) {
                System.out.println("Tabla de multiplicar de " + numero + ":");
                for (int i = 1; i <= 10; i++) {
                    System.out.println(numero + " x " + i + " = " + (numero * i));
                }
            }
        } while (numero != 0);

        System.out.println("Programa finalizado.");
        
    }
}
~~~
## Ejercicios - for
1. Imprimir los números impares del 1 al 50.
```java
public class Johnnyactiv5log {

    public static void main(String[] args) {

       
        
for (int i = 1; i <= 50; i++) {
            if (i % 2 != 0) {
                System.out.println(i);
            }
        }
    }
}
```

2.Imprimir los números primos del 1 al 100.
 ```java
class Main {
  public static void main(String[] args) {
    
    
        for (int i = 2; i <= 100; i++) {
            int contadorDivisores = 0;
            
            for (int j = 1; j <= i; j++) {
                if (i % j == 0) {
                    contadorDivisores++;
                }
            }
            
            if (contadorDivisores == 2) {
                System.out.println(i);
            }
        }
    }
}
```