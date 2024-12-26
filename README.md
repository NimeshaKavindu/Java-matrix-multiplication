/* Java-matrix-multiplication
Using 2D arrays multply 2 matrices.*/

import java.util.Scanner;

public class MatricsMultiplication {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        
        System.out.print(" Enter Rows and Columns (saperated by space) :");
        int rows1 = scan.nextInt();
        int cols1 = scan.nextInt();
        
        System.out.print(" Enter Rows and Columns (saperated by space) :");
        int rows2 = scan.nextInt();
        int cols2 = scan.nextInt();

        if (cols1 == rows2) {
            int[][] arr = new int[rows1][cols1];
            int[][] arr2 = new int[rows2][cols2];
            int[][] multipliedArray =  new int[rows1][cols2];

            System.out.println("Enter the elements in array 1 row wise :");

            for (int i = 0; i < rows1; i++) {
                for (int j = 0; j < cols1; j++) {
                    arr[i][j] = scan.nextInt();
                }
            }

            System.out.println("Enter the elements in array 2 row wise :");

            for (int i = 0; i < rows2; i++) {
                for (int j = 0; j < cols2; j++) {
                    arr2[i][j] = scan.nextInt();
                }
            }
            
            for (int i = 0; i < rows1; i++) {
                for(int j=0; j<cols1;j++){
                    for(int k =0;k<cols2; k++){
                        multipliedArray[i][k] += arr[i][j] * arr2[j][k];
                    }
                }
            }

            for(int i =0;i<multipliedArray.length;i++){
                for(int j =0; j<multipliedArray[0].length;j++){
                    System.out.print(multipliedArray[i][j]+" ");
                }
                System.out.println();
            }
        

        }else{
            System.out.println("value of 1st metrics' colum and 2nd metrics row are not equal.");
        }

    }
}
