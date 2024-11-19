package Estudiantes;

/**
 *
 * @author 1061717293
 */
public class estudiante {
    private int edad;
    private String nombre;
    private Double promedio;
    

    public estudiante(String nombre, int edad, double promedio) {
        this.edad = edad;
        this.nombre = nombre;
        this.promedio = promedio;
    }

    public int getEdad() {
        return edad;
    }

    public void setEdad(int edad) {
        this.edad = edad;
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public Double getPromedio() {
        return promedio;
    }

    public void setPromedio(Double promedio) {
        this.promedio = promedio;
    }

    @Override
    public String toString() {
        return "estudiante{" + "edad=" + edad + ", nombre=" + nombre + ", promedio=" + promedio + '}'; 
    }
    
    
}


