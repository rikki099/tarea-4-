# tarea-4-
import java.util.Scanner;

public class MatrizCuadrada {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el tamaño de la matriz cuadrada : ");
        int N = scanner.nextInt();

        int[][] matriz = new int[N][N];

        for (int i = 0; i < N; i++) {
            for (int j = 0; j < N; j++) {
                matriz[i][j] = (int) (Math.random() * 90) + 10; 
            }
        }

        System.out.println("Matriz:");
        for (int i = 0; i < N; i++) {
            for (int j = 0; j < N; j++) {
                System.out.print(matriz[i][j] + "\t");
            }
            System.out.println();
        }

        int sumaDiagonalPrincipal = 0;
        for (int i = 0; i < N; i++) {
            sumaDiagonalPrincipal += matriz[i][i];
        }

        int sumaDiagonalSecundaria = 0;
        for (int i = 0; i < N; i++) {
            sumaDiagonalSecundaria += matriz[i][N - 1 - i];
        }
        system.out.println("resultados");
        System.out.println("Suma de la diagonal principal: " + sumaDiagonalPrincipal);
        System.out.println("Suma de la diagonal secundaria: " + sumaDiagonalSecundaria);
    }
}
