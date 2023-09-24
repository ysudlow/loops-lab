#loops-lab
import java.util.Scanner;

public class NumberOperations {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        int num1, num2;
        int diff;

        do {
            // Prompt the user to enter two numbers
            System.out.print("Enter the first number: ");
            num1 = input.nextInt();

            System.out.print("Enter the second number: ");
            num2 = input.nextInt();

            // Calculate the difference between the numbers
            diff = Math.abs(num1 - num2);

            if (diff < 200) {
                System.out.println("The difference between the numbers is less than 200. Please try again.");
            }
        } while (diff < 200);

        // Calculate and display the sums based on the criteria
        calculateAndDisplaySums(num1, num2);

        input.close();
    }

    /**
     * Calculates and displays the sums of numbers based on specific criteria.
     *
     * @param num1 The first input number.
     * @param num2 The second input number.
     */
    private static void calculateAndDisplaySums(int num1, int num2) {
        int sumEvenDivisibleBy4 = 0;
        int sumEvenDivisibleBy8 = 0;
        int sumNotEvenNotDivisibleBy5 = 0;

        // Use a for loop to iterate through numbers between num1 and num2
        for (int i = num1; i <= num2; i++) {
            switch (i % 2) {
                case 0: // Even numbers
                    if (i % 4 == 0) {
                        sumEvenDivisibleBy4 += i;
                    }
                    if (i % 8 == 0) {
                        sumEvenDivisibleBy8 += i;
                    }
                    break;
                default: // Not even numbers
                    if (i % 5 != 0) {
                        sumNotEvenNotDivisibleBy5 += i;
                    }
                    break;
            }
        }

        // Display the sums
        System.out.println("Sum of even numbers divisible by 4: " + sumEvenDivisibleBy4);
        System.out.println("Sum of even numbers divisible by 8: " + sumEvenDivisibleBy8);
        System.out.println("Sum of not even numbers not divisible by 5: " + sumNotEvenNotDivisibleBy5);
    }
}
