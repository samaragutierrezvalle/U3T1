# U3T1
import java.util.Scanner;

public class ClasePrincipal {
    public static void main(String[] args) {
        Scanner leer = new Scanner(System.in);
        int [] Arreglo1 = new int[5]; //Declaramos Arreglo
        int valor =0;
         int cont=0;// Declaramos contador

        //Menu
        do {
            System.out.println("************************MENU************************");
            System.out.println("[1] Insertar Datp");
            System.out.println("[2] Eliminar Dato");
            System.out.println("[3] Mostrar");
            System.out.println("[4] Salir");
            valor = leer.nextInt();
            switch (valor){
                case 1:
                    System.out.println("Insertando datos");
                    if (cont < 5){ //Condicional para decir que nuestro arreglo esta lleno
                        Arreglo1[cont]= leer.nextInt(); //Se le asigna el valor en la posicion del contador
                        cont++; //Aumentamos el contador
                    }else {
                        System.out.println("El arreglo esta lleno");
                    }
                    break;
                case 2:
                    if(cont == 0){ //Nos dice si nuestro arreglo esta vacio
                        System.out.println("Tu arreglo esta vacio");
                    }else {
                        System.out.println("Eliminando dato");
                        Arreglo1[cont-1]= 0;//Asignamos el valor de 0 a la posicion del contador
                        cont--; //Disminuimos el contador
                    }
                    break;
                case 3:
                    System.out.println("Mostrando Datos");
                    for (int j = Arreglo1.length-1; j>=0; j--) {
                        System.out.println(Arreglo1[j]);
                    }
                    break;
                default:
                    System.out.println("Ingrese un numero valido");
            }
        }while (valor!=4);
        System.out.println("Saliendo");
    }
}
