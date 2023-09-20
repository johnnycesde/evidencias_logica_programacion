<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 


<!-- Su documentación aquí -->

# Actividad 3: 
## Ejercicios de operaciones básicas en Java.
1.  Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.
## Respuestas a operaciones básicas en Java.
# 1. 
~~~ java

import java.util.Scanner;
class Main {

	public String toString() {
		return "Main []";
	}

public static void main(String[] args) {
    Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Ingrese el primer entero:");
        int entero1 = entradaDatos.nextInt();

        System.out.println("Ingrese el segundo entero:");
        int entero2 = entradaDatos.nextInt();

        int suma = entero1 + entero2;
        int multiplicacion = entero1 * entero2;

        System.out.println("El resultado de la suma de los dos enteros es: " + suma);
        System.out.println("El resultado de la multipliccion de los dos enteros es: " + multiplicacion);
  }
}
~~~

2. Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.


~~~ java
import java.util.Scanner;
class Main {
  public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Ingrese el primer entero:");
        int entero1 = entradaDatos.nextInt();

        System.out.println("Ingrese el segundo entero:");
        int entero2 = entradaDatos.nextInt();

        int Resta = entero1 - entero2;
        int Division = entero1 / entero2;

        System.out.println("El resultado de la Resta de los dos enteros: " + Resta);
        System.out.println("El resultado de la Division de los dos enteros: " + Division);
  }
}
~~~
3. Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

~~~ java
import java.util.Scanner;
class Main {
  public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);
     System.out.println("Ingrese el primer entero:");
        int ent1 = entradaDatos.nextInt();

        System.out.println("Ingrese el segundo entero:");
        int ent2 = entradaDatos.nextInt();
        
        System.out.println("Ingresa el tercer entero: ");
        int ent3 = entradaDatos.nextInt();
        
        int operacion1 = ent1 + ent2 + ent3;
        int operacion2 = (ent1*ent2)/ent3;
        
        System.out.println("El resultado de la suma de los tres enteros es : " +operacion1);
        System.out.println("El resultado de la multiplicacion del primer entero por el segundo y division por el tercer entero es: "+operacion2);
  }
}
~~~

4. Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.
~~~ java

import java.util.Scanner;
class Main {
  public static void main(String[] args) {
    Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Ingrese el primer entero decimal:");
        float ent1 = entradaDatos.nextFloat();

        System.out.println("Ingrese el segundo entero decimal:");
        float ent2 = entradaDatos.nextFloat();
        
        float suma = ent1+ ent2;
        float resta = ent1-ent2;
        float multiplicacion = ent1*ent2;
        float division = ent1/ ent2;
        
        System.out.println("El resultado de la suma es: "+suma);
        System.out.println("El resultdo de la resta es: "+resta);
        System.out.println("El resultdo de la multuplicacion es: "+multiplicacion);
        System.out.println("El resultdo de la division es: "+division);
  }
}
~~~
5. Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

~~~ java
class Main {
  public static void main(String[] args) {
      int entero = 22;
        
         entero += 1;
        
         System.out.println("el resultado de incremento del entero es: "+numero);
       numero -=2;
        System.out.println("el resultado del decremento del entero es: "+numero);
  }
}
~~~


6. Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

~~~java
class Main {
  public static void main(String[] args) {
    int entero = 30;
        entero +=5;
        System.out.println("El resultado de la asignacion compuesta mas 5 es:"+entero);
  }
}
~~~


7. Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.
~~~java


class Main {
  public static void main(String[] args) {
     
int edad = 27;
        
        
    boolean esMayor = true;
    boolean esDiaLaboral = false;
    boolean esVacaciones = true;

    boolean resultado1 = (edad > 30) && esMayor;
    boolean resultado2 = esDiaLaboral || esVacaciones;
    boolean resultado3 = !esDiaLaboral;

        
            System.out.println("el resultado 1 es: " + resultado1);
      System.out.println("el resultado 2 es: " + resultado2);
    System.out.println("el resultado 3 es: " + resultado3);
  }
}
~~~

8. Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.
   
 ~~~java
 import java.util.Scanner;
class Main {
  public static void main(String[] args) {
     Scanner entradaDatos = new Scanner(System.in);

        System.out.println("Por favor ingresa un numero: ");
        int entero = entradaDatos.nextInt();

        if (entero == 0) {
            System.out.println("el numero es neutro");
        }
        else if (entero<=0){System.out.println("el numero es negativo");
        }else { System.out.println("el numero es positivo");}
  }
}
~~~




