<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->
## Actividad 4:
## Ejercicios de control de flujo con expresiones compuestas

 // Variables de tipo String

 ```java
  

String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;  


```
~~~

### Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.
2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
5. Mostrar toda la información del estudiante si está matriculado en el Cesde.
6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
0.0 - 3.4: El estudiante no recibe beca.
3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
4.5 - 5.0: El estudiante recibe una beca completa.


```java

class Main {
  public static void main(String[] args) {
  // Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;

    System.out.println("________________________");
      System.out.println("ejercicio1");
    if (edad >= 18 && esActivo) {
      System.out.println("El estudiante tiene " + edad + " y esta activo");
          }
      System.out.println("________________________");
      System.out.println("ejercicio2");
if(carrera.equals("Desarrollo de Software") || becado ){
  System.out.println("Es becado o estudia desarrollo de software ");
}
 System.out.println("________________________");
      System.out.println("ejercicio3");
    if (semestre == 3 && esActivo ) {
       System.out.println("está en el último semestre de su carrera y tiene un estado activo.");
    } else {
            System.out.println("no está en el último semestre de su carrera o no tiene un estado activo."); 
    } 
System.out.println("________________________");
      System.out.println("ejercicio4");
 if (carrera.equals("Desarrollo de Software") && promedio >4.0  ){
   System.out.println("tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0."); 
 }
System.out.println("________________________");
      System.out.println("ejercicio5");
    if( universidad.equals("Cesde")){
  System.out.println(nombre);
System.out.println(apellido);
System.out.println(identificación);
System.out.println(correo);
System.out.println(carrera);
      System.out.println(universidad);
      System.out.println(edad);
System.out.println("esta activo");
System.out.println("no esta becado");
     System.out.println(género); 
System.out.println("elpromedio es = " + promedio); 
      System.out.println("esta en el semestre " + semestre); 
    } 
     System.out.println("________________________");
      System.out.println("ejercicio6");
    if(universidad == "Cesde" && promedio >4.0 && esActivo ){
      System.out.println(" se otorga una beca del 50%");
    }


 System.out.println("________________________");
      System.out.println("ejercicio7");
     if (promedio >= 9 && promedio <= 10) {
            System.out.println("El estudiante no recibe beca.");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            System.out.println("El estudiante recibe una beca parcial del 25%.");
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante recibe una beca parcial del 50%.");

        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante recibe una beca completa.");
        } else {
            System.out.println("Error, verifique la nota");
        }
    System.out.println("________________________");
      System.out.println("ejercicio8");
     if (carrera.equals("Desarrollo de Software") && promedio >4.0  ){
   System.out.println("se le obsequiara un computador personal"); 
 }
  System.out.println("________________________");
      System.out.println("ejercicio9");
    if(universidad == "Cesde" && promedio >4.0 ){
      System.out.println(" se otorgara un uniforme de la institucion cesde");
    }
System.out.println("________________________");
      System.out.println("ejercicio8");
     if (carrera.equals("Desarrollo de Software") && promedio >4.0  ){
   System.out.println("se le ayudara con un subsidio de transporte mensual de 150.000"); 
 }
 


    
  }
}

```



