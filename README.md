import java.util.Random;

public class MatrixRowSwap {
    public static void main(String[] args) {
        // Виведення прізвища та ініціалів розробника
        System.out.println("Розробник: Яценко Микола");

        // Ініціалізація матриці A(3,3)
        int rows = 3;
        int cols = 3;
        int[][] A = new int[rows][cols];
        Random random = new Random();

        // Заповнення матриці випадковими числами
        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                A[i][j] = random.nextInt(100); 
            }
        }

        // Виведення матриці до перетворення
        System.out.println("\nМатриця А до перетворення:");
        printMatrix(A);

        // Перетворення: останній рядок стає першим, а перший — останнім
        int[] temp = A[0];
        A[0] = A[rows - 1];
        A[rows - 1] = temp;

        // Виведення матриці після перетворення
        System.out.println("\nМатриця А після перетворення:");
        printMatrix(A);
    }

    // Метод для зручного виведення матриці у консоль
    private static void printMatrix(int[][] matrix) {
        for (int i = 0; i < matrix.length; i++) {
            for (int j = 0; j < matrix[i].length; j++) {
                System.out.print(matrix[i][j] + "\t");
            }
            System.out.println();
        }
    }
}
