package Estudiantes;

import java.util.Scanner;

/**
 *
 * @author 1061717293
 */
public class gestionEstudiantes {
    private estudiante[] estudiantes;
    private int cantidadActual;
    private static final int capacidad_maxima = 4;

    public gestionEstudiantes() {
        estudiantes = new estudiante[capacidad_maxima];
        cantidadActual = 0;
    }

    public void agregarEstudiante() {
        if (cantidadActual >= capacidad_maxima) {
            System.out.println("No se pueden agregar mas estudiantes");
            return;
        }

        Scanner sc = new Scanner(System.in);

        System.out.print("Ingrese el nombre del estudiante: ");
        String nombre = sc.nextLine();

        System.out.print("Ingrese la edad del estudiante: ");
        int edad = sc.nextInt();

        System.out.print("Ingrese el promedio del estudiante: ");
        double promedio = sc.nextDouble();

        
        estudiantes[cantidadActual] = new estudiante(nombre, edad, promedio);
        cantidadActual++;

        System.out.println("Estudiante agregado exitosamente");
    }

    
    public void mostrarEstudiantes() {
        if (cantidadActual == 0) {
            System.out.println("No hay estudiantes registrados");
            return;
        }

        System.out.println("Lista de Estudiantes: ");
        for (int i = 0; i < cantidadActual; i++) {
            System.out.println((i + 1) + ". " + estudiantes[i]);
        }
    }

    public void buscarPorNombre(String nombre) {
        boolean encontrado = false;
        for (int i = 0; i < cantidadActual; i++) {
            if (estudiantes[i].getNombre().equalsIgnoreCase(nombre)) {
                System.out.println("Estudiante encontrado: " + estudiantes[i]);
                encontrado = true;
                break;
            }
        }

        if (!encontrado) {
            System.out.println("No se encontro ningun estudiante con el nombre: " + nombre);
        }
    }

    public void calcularPromedioGeneral() {
        if (cantidadActual == 0) {
            System.out.println("No hay estudiantes registrados.");
            return;
        }

        double sumaPromedios = 0;
        for (int i = 0; i < cantidadActual; i++) {
            sumaPromedios += estudiantes[i].getPromedio();
        }

        double promedioGeneral = sumaPromedios / cantidadActual;
        System.out.printf("Promedio general: ", promedioGeneral);
    }
