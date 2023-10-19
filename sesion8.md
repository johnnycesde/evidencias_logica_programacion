<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 


<!-- Su documentación aquí -->
### Implementar los siguientes métodos:

 1.Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.

~~~java
public class Main {
    public static void main(String[] args) {
        int numero1 = 10;
        int numero2 = 20;
        
        int mayorNumero = encontrarMayor(numero1, numero2);
        
        System.out.println("El mayor número es: " + mayorNumero);
    }
    
    public static int encontrarMayor(int num1, int num2) {
        if (num1 > num2) {
            return num1;
        } else {
            return num2;
        }
    }
}

~~~

   2.Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.

~~~java
public class Main {
    public static void main(String[] args) {
        String texto = "Hola, este es un ejemplo de conteo de vocales.";
        
        int cantidadVocales = contarVocales(texto);
        
        System.out.println("El número de vocales en el texto es: " + cantidadVocales);
    }
    
    public static int contarVocales(String texto) {
        int contador = 0;
        texto = texto.toLowerCase(); // Convertir el texto a minúsculas para hacer una comparación sin distinción de mayúsculas/minúsculas
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' 
            || caracter == 'i' || caracter == 'o' 
            || caracter == 'u') {
                contador++;
            }
        }
        return contador;
    }
~~~

  3.Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
~~~java


public class Main {
    public static void main(String[] args) {
        String texto = "JohnnY, Este Es Un Ejemplo De Inversión De Mayúsculas Y Minúsculas.";
        
        String textoInvertido = invertirMayusculasMinusculas(texto);
        
        System.out.println("Texto original: " + texto);
        System.out.println("Texto con mayúsculas e minúsculas invertidas: " + textoInvertido);
    }
    
    public static String invertirMayusculasMinusculas(String texto) {
        StringBuilder resultado = new StringBuilder();
        
        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            
            if (Character.isUpperCase(caracter)) {
                resultado.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {
                resultado.append(Character.toUpperCase(caracter));
            } else {
                resultado.append(caracter); // Mantener caracteres que no son letras tal como están
            }
        }
        
        return resultado.toString();
    }
}

~~~

4.Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.

~~~java
public class Main {
    public static void main(String[] args) {
        String texto = "La vaca esta muy pesada para subir la montaña.";
        
        int cantidadPalabras = contarPalabras(texto);
        
        System.out.println("El número de palabras en el texto es: " + cantidadPalabras);
    }
    
    public static int contarPalabras(String texto) {
        String[] palabras = texto.split("\\s+"); // Dividir la cadena en palabras usando espacios en blanco como delimitador
        return palabras.length;
    }
}
~~~

 5.Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

~~~java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        String texto = "zas tiene una alinza con yasid.";
        
        String textoOrdenado = ordenarPalabras(texto);
        
        System.out.println("Texto original: " + texto);
        System.out.println("Texto con palabras ordenadas alfabéticamente: " + textoOrdenado);
    }
    
    public static String ordenarPalabras(String texto) {
        String[] palabras = texto.split("\\s+");
        Arrays.sort(palabras);
        return String.join(" ", palabras);
    }
}


~~~