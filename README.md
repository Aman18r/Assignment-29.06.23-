# Assignment-29.06.23-

Assignment 1:-

import java.util.Scanner;
public class Main{

    static void strictlyIncreasing(int[] arr1, int[] arr2, int[] arr3){
        int i=0, j=0, k=0;

        while(i<arr1.length && j<arr2.length && k<arr3.length){
             if(arr1[i] == arr2[j] && arr2[j] == arr3[k]){
                 System.out.println(arr1[i] + " ");
                 i++;
                 j++;
                 k++;
             }
             else if(arr1[i] < arr2[j])
                 i++;
             else if(arr2[j] < arr3[k])
                 j++;

             else
                 k++;
        }
    }
    public static void main(String[] args) {

        int arr1[] = {1,5,10,20,40,80};
        int arr2[] = {6,7,20,80,100};
        int arr3[] = {3,4,15,20,30,70,80,120};

            System.out.println("Common elements are: ");
            strictlyIncreasing(arr1, arr2, arr3);

    }
}


Assignment:- 3

import java.util.Scanner;
public class Main{

        static void printMatrix(int[][] matrix){
            for(int i = 0; i < matrix.length; i++){
                for(int j = 0; j < matrix.length; j++){
                    System.out.println(matrix[i][j] + " ");
                }
                System.out.println();
            }
        }

        static int[][] findTranspose(int[][] matrix, int r, int c){
            int[][] ans = new int[c][r];

            for(int i = 0;i < c; i++){
                for(int j = 0; j < r; j++){
                    ans[i][j] = matrix[j][i];
                }
            }
            return ans;
        }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number of rows and columns:");
        int r = sc.nextInt();
        int c = sc.nextInt();
        int[][] arr = new int[r][c];
        int totalElements = r * c;
        System.out.println("Enter " + totalElements + " values:");
        for(int i = 0; i < r; i++){
            for(int j = 0; j < c; j++){
                arr[i][j] = sc.nextInt();
            }
        }
        System.out.println("Input Matrix");
        printMatrix(arr);

        System.out.println("Transpose of Matrix");
        int[][] ans = findTranspose(arr, r, c);
        printMatrix(ans);
    }
}

Assignment:- 6

import java.util.*;
import java.io.*;

class Main {

    public static void sortSquares(int arr[])
    {
        int n = arr.length;


        for (int i = 0; i < n; i++)
            arr[i] = arr[i] * arr[i];

        Arrays.sort(arr);
    }


    public static void main(String[] args)
    {
        int arr[] = { -4,-1,0,3,10 };
        int n = arr.length;

        System.out.println("Before sort ");
        for (int i = 0; i < n; i++)
            System.out.print(arr[i] + " ");

        sortSquares(arr);
        System.out.println("");
        System.out.println("After Sort ");
        for (int i = 0; i < n; i++)
            System.out.print(arr[i] + " ");
    }
}
