<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->

2. Crear un ejemplo de Array y otro de ArrayList para visualizar sus diferencias.
## - Array
~~~java
class Main {
    public static void main(String[] args) {
        // Declarar un array de enteros
        int[] numeros;

        // Inicializar el array con un tamaño específico (en este caso, 5)
        numeros = new int[5];

        // Asignar valores a los elementos del array
        numeros[0] = 10;
        numeros[1] = 100;
        numeros[2] = 1000;
        numeros[3] = 10000;
        numeros[4] = 100000;

        // Acceder y mostrar los valores del array
        System.out.println("Elemento 1: " + numeros[0]);
        System.out.println("Elemento 2: " + numeros[1]);
        System.out.println("Elemento 3: " + numeros[2]);
        System.out.println("Elemento 4: " + numeros[3]);
        System.out.println("Elemento 5: " + numeros[4]);
    }
}
~~~

## - ArrayList
~~~java
 import java.util.ArrayList;

class Main {
    public static void main(String[] args) {
        // Crear un ArrayList de enteros
        ArrayList<Integer> numeros = new ArrayList<>();

        // Agregar elementos al ArrayList
        numeros.add(10);
        numeros.add(20);
        numeros.add(30);
        numeros.add(40);
        numeros.add(50);

        // Acceder a elementos del ArrayList
        System.out.println("Elemento en la posición 2: " + numeros.get(2));

        // Modificar un elemento
        numeros.set(3, 45);

        // Recorrer y mostrar todos los elementos del ArrayList
        System.out.println("Elementos en la lista:");
        for (Integer numero : numeros) {
            System.out.println(numero);
        }

        // Obtener el tamaño del ArrayList
        System.out.println("Tamaño del ArrayList: " + numeros.size());

        // Verificar si el ArrayList está vacío
        System.out.println("¿El ArrayList está vacío? " + numeros.isEmpty());

        // Eliminar un elemento del ArrayList
        numeros.remove(1);

        // Verificar si un elemento está en el ArrayList
        System.out.println("¿Contiene el valor 30? " + numeros.contains(30));

        
    }
}
~~~







