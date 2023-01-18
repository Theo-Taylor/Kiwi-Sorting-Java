import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

public class Height_Sorting {
    public static void main(String[] args) {
        double[] height = readData("data.csv");

        System.out.println("Unsorted:");
        for(int i = 0; i < height.length; i++)
            System.out.println(height[i]);

        insertionSort(height);
        System.out.println("Sorted:");
        for(int i = 0; i < height.length; i++)
            System.out.println(height[i]);
    }

    public static double[] readData(String fileName) {
        try {
            File file = new File(fileName);
            Scanner sc = new Scanner(file);
            int rows = 0;
            while (sc.hasNextLine()) {
                rows++;
                sc.nextLine();
            }
            sc.close();
            sc = new Scanner(file);
            double[] data = new double[rows];
            int i = 0;
            sc.nextLine();
            while (sc.hasNextLine()) {
                var nextLine = sc.nextLine();
                var height = nextLine.split("\",\"")[3];
                System.out.println(height);
                data[i++] = Double.parseDouble(height);
            }
            sc.close();
            return data;
        } catch (FileNotFoundException e) {
            System.out.println("File not found");
            return null;
        }
    }

    public static void insertionSort(double[] A) {
        int n = A.length;
        for (int i = 1; i < n; i++) {
            double a = A[i];
            int j = i - 1;
            while (j >= 0 && A[j] > a) {
                A[j + 1] = A[j];
                j--;
            }
            A[j + 1] = a;
        }
    }
}
