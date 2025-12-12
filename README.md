# Program--4-.java
import java.util.Arrays;

public class MultiplesCount {
    public static void main(String[] args) {
        int[] arr = {1, 2, 8, 9, 12, 46, 76, 82, 15, 20, 30};
        int[] count = new int[10];
        for (int num : arr) {
            // check divisibility by 1..9
            for (int d = 1; d <= 9; d++) {
                if (num % d == 0) {
                    count[d]++;
                }
            }
        }
        System.out.print("{");
        for (int d = 1; d <= 9; d++) {
            System.out.print(d + ": " + count[d]);
            if (d != 9) {
                System.out.print(", ");
            }
        }
        System.out.println("}");
    }
}
