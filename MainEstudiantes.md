package Estudiantes;

import java.util.Scanner;

/**
 *
 * @author 1061717293
 */
public class MainEstudiantes {

    
    public static void main(String[] args) {
        gestionEstudiantes gestion = new gestionEstudiantes();
        Scanner sc = new Scanner(System.in);
        int opcion;

        do {
            System.out.println(" Edu pilo S.A. ");
            System.out.println("1. Agregar estudiante");
            System.out.println("2. Mostrar estudiantes");
            System.out.println("3. Buscar estudiante por nombre");
            System.out.println("4. Calcular promedio general");
            System.out.println("5. Salir");
            System.out.print("Ingrese su opcion: ");

            opcion = sc.nextInt();
            sc.nextLine(); 

            switch (opcion) {
                case 1:
                    gestion.agregarEstudiante();
                    break;
                case 2:
                    gestion.mostrarEstudiantes();
                    break;
                case 3:
                    System.out.print("Ingrese el nombre a buscar: ");
                    String nombreBuscar = sc.nextLine();
                    gestion.buscarPorNombre(nombreBuscar);
                    break;
                case 4:
                    gestion.calcularPromedioGeneral();
                    break;
                case 5:
                    System.out.println("Saliendo del programa");
                    break;
                default:
                    System.out.println("Opción invalida");
            }
        } while (opcion != 5);
    }
}
   
