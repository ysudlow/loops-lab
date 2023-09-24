#loops-lab
import java.util.Scanner;

public class LoopExamples {
    public static void main(String[] args) {
        // Task 1: Display a string 99 times
        String message = "This is the string to be displayed 99 times.";
        for (int i = 0; i < 99; i++) {
            System.out.println(message);
        }
        
        // Task 2: Display every odd number from 0 to 99
        for (int i = 1; i <= 99; i += 2) {
            System.out.print(i + " ");
        }
        System.out.println(); // Newline
        
        // Task 3: Display every even number from 0 to 99
        for (int i = 0; i <= 99; i += 2) {
            System.out.print(i + " ");
        }
        System.out.println(); // Newline
        
        // Task 4: Display even numbers in a different way
        for (int i = 2; i <= 99; i += 2) {
            System.out.print(i + " ");
        }
        System.out.println(); // Newline
        
        // Task 5: Sum up and print odd numbers from 0 to 99
        int oddSum = 0;
        for (int i = 1; i <= 99; i += 2) {
            oddSum += i;
        }
        System.out.println("Sum of odd numbers: " + oddSum);
        
        // Task 6: Sum up and print even numbers from 0 to 99
        int evenSum = 0;
        for (int i = 0; i <= 99; i += 2) {
            evenSum += i;
        }
        System.out.println("Sum of even numbers: " + evenSum);
        
        
        // Task 7: Sum of two numbers given by the user
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter the first number: ");
        int num1 = scanner.nextInt();
        
        System.out.print("Enter the second number: ");
        int num2 = scanner.nextInt();
        
        int sum = num1 + num2;
        System.out.println("Sum of " + num1 + " and " + num2 + " is: " + sum);
        
        
        // Close the scanner to release resources
        scanner.close();
    }
}
