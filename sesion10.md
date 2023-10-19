<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->

## Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

1. Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno.

~~~java
import java.util.Scanner;

public class MRU {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidad, tiempo, distancia;
      
      // Solicita la velocidad y el tiempo
      System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();

      // Calcula la distancia recorrida
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
   }
}
~~~


~~~java
import java.util.Scanner;    // Importamos la clase Scanner para la entrada de datos.

public class MRU {    // Declaramos una clase llamada "MRU".

   public static void main(String[] args){       // Declaramos el método main, que es el punto de entrada del programa.

      Scanner input = new Scanner(Systemin);     // Creamos un objeto Scanner llamado "input" para recibir entrada del usuario.

      double velocidad, tiempo, distancia;      // Declaramos variables para almacenar la velocidad, el tiempo y la distancia.

      
      // Solicita la velocidad y el tiempo al usuario.
    System.out.print("Ingrese la velocidad en metros por segundo");                          
    // Muestra un mensaje en la consola.

      velocidad = input.nextDouble(); // Lee la velocidad ingresada por el usuario y la almacena en la variable "velocidad".

      System.out.print("Ingrese el tiempo en segundos: "); // Muestra otro mensaje en la consola.
      tiempo = input.nextDouble(); // Lee el tiempo ingresado por el usuario y lo almacena en la variable "tiempo".

      // Calcula la distancia recorrida usando la fórmula de MRU (Movimiento Rectilíneo Uniforme).
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola.
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia); 
      // Muestra la distancia calculada con dos decimales.

   }
}
~~~

### 1. Cálculo del consumo diario en kilovatios-hora (kWh):

- Se toma la potencia del electrodoméstico (en vatios) ingresada por el usuario.
y se multiplica por el tiempo de uso diario (en horas) ingresado por el usuario.
 Esto se hace para calcular la cantidad de energía consumida en un día.
- Dado que la potencia se mide en vatios y se necesita el resultado en kilovatios, se divide el resultado por 1000 para realizar la conversión.

### 2.Cálculo del consumo mensual en kilovatios-hora (kWh):

- El consumo diario calculado anteriormente se multiplica por el número de días en el mes ingresado por el usuario. Esto se hace para calcular el consumo de energía eléctrica durante un mes.

 ### 3.Cálculo del costo mensual de energía eléctrica:

- El consumo mensual en kilovatios-hora se multiplica por el precio por kilovatio-hora ingresado por el usuario. Esto se realiza para calcular el costo total de la energía eléctrica consumida en el mes.
- Dado que el precio se proporciona en pesos por kilovatio-hora y se necesita el costo en pesos, se divide el resultado por 1000 para realizar la conversión.
- En resumen, se realizan cálculos matemáticos para determinar el consumo diario y mensual de energía eléctrica y el costo mensual. Estos cálculos involucran multiplicaciones, divisiones y conversiones de unidades de medida (de vatios a kilovatios y de kilovatios-hora a pesos).

~~~java

import java.util.Scanner;

public class CalculoCostoEnergiaElectrica {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      // Solicitar datos al usuario
      System.out.print("Ingrese la potencia del electrodoméstico (en vatios): ");
      double potencia = input.nextDouble();
      
      System.out.print("Ingrese el tiempo de uso diario (en horas): ");
      double tiempoUsoDiario = input.nextDouble();
      
      System.out.print("Ingrese el precio por kilovatio-hora (en pesos): ");
      double precioKwh = input.nextDouble();
      
      System.out.print("Ingrese el número de días del mes: ");
      int díasDelMes = input.nextInt();
      
      // Cálculo del consumo mensual en kilovatios-hora
      double consumoDiarioKwh = (potencia * tiempoUsoDiario) / 1000; // Convertimos de vatios a kilovatios
      double consumoMensualKwh = consumoDiarioKwh * díasDelMes;
      
      // Cálculo del costo mensual de energía eléctrica
      double costoEnergíaEléctrica = consumoMensualKwh * precioKwh / 1000; // Dividimos entre 1000 para convertir el precio a pesos por kilovatio-hora
      
      // Imprimir el resultado en pantalla
      System.out.printf("El costo mensual de energía eléctrica es de: $%,.2f pesos", costoEnergíaEléctrica);
   }
}
~~~

