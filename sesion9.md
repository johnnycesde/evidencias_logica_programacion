<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 

### Ejercicios de Lógica de Programación
 Calculadora de resistencias eléctricas
<!-- Su documentación aquí -->

1. Resolver en parejas el ejercicio asignado por el docente

~~~java
import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

 

class Main {
  public static void main(String[] args) {
   
        // Definir los colores y sus valores
        Map<String, Integer> colores = new HashMap<>();
        colores.put("negro", 0);
        colores.put("marron", 1);
        colores.put("rojo", 2);
        colores.put("naranja", 3);
        colores.put("amarillo", 4);
        colores.put("verde", 5);
        colores.put("azul", 6);
        colores.put("violeta", 7);
        colores.put("gris", 8);
        colores.put("blanco", 9);

        Scanner scanner = new Scanner(System.in);
        String[] bandas = new String[3];

        // Solicitar al usuario los colores de las tres bandas
        for (int i = 0; i < 3; i++) {
            System.out.print("Introduce el color de la banda " + (i + 1) + ": ");
            bandas[i] = scanner.nextLine().toLowerCase();
            if (!colores.containsKey(bandas[i])) {
                System.out.println("Color no válido. Introduce un color válido.");
                i--; // Repetir la entrada si el color no es válido
            }
        }

        // Calcular el valor de la resistencia
        int valor = (colores.get(bandas[0]) * 10 + colores.get(bandas[1])) * (int) Math.pow(10, colores.get(bandas[2]));
    
    /**if (valor >= 1000) { 
       return (valor / 1000) + "k";
    } **/

        System.out.println("El valor de la resistencia es: " + valor / 1000 + "k ohmios");
    }
}
~~~
Se define un **Map** llamado **colores** que asocia nombres de colores con valores numéricos. Cada color representa un número, que se utilizará para calcular el valor de la resistencia.

Se crea un array de Strings llamado **bandas** para almacenar los colores de las tres bandas de la resistencia.

Se utiliza un bucle **for** para solicitar al usuario los colores de las tres bandas. El bucle recorre las tres bandas y utiliza un **Scanner** para obtener la entrada del usuario. Si el color introducido no está en el mapa **colores**, se muestra un mensaje de error y se permite al usuario ingresar un color válido.

Después de obtener los colores de las tres bandas, se realiza el cálculo del valor de la resistencia.

 *El valor se calcula utilizando la fórmula:*

**valor = (colores.get(bandas[0]) * 10 + colores.get(bandas[1])) * (int) Math.pow(10, colores.get(bandas[2]))**

**colores.get(bandas[0])** obtiene el valor numérico de la primera banda.
**colores.get(bandas[1])** obtiene el valor numérico de la segunda banda.
**colores.get(bandas[2])** obtiene el valor numérico de la tercera banda.

Luego, se multiplica el valor de la primera banda por 10 y se suma al valor de la segunda banda.
Finalmente, se eleva 10 a la potencia del valor de la tercera banda y se multiplica por el resultado anterior.
El valor calculado representa la resistencia en ohmios. Si el valor es mayor o igual a 1000, se imprime en kiloohmios (k ohmios) dividiendo el valor entre 1000.

La parte del código que está comentada con /** ... */ parece ser un intento de mostrar el valor en kiloohmios, pero está comentada y no afecta la salida.

En resumen, este programa toma los colores de tres bandas de una resistencia y calcula su valor en ohmios.

