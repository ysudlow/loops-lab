#loops-lab


import java.util.InputMismatchException;
import java.util.Scanner;

public class UserInputScript {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            // Prompt and read user's name
            System.out.print("Please enter your name: ");
            String userName = scanner.nextLine();
            System.out.println("Hello, " + userName + "! ");

            // Prompt and read pet preference
            System.out.print("Do you prefer cats or dogs? ");
            String petPreference = scanner.nextLine();

            // Respond based on pet preference
            if (petPreference.equalsIgnoreCase("dog") || petPreference.equalsIgnoreCase("dogs")) {
                System.out.println("Woof!");
            } else if (petPreference.equalsIgnoreCase("cat") || petPreference.equalsIgnoreCase("cats")) {
                System.out.println("Meow!");
            } else {
                System.out.println("I'm not sure what sound that animal makes.");
            }

            // Read the number of pets (integer input)
            int petCount;
            while (true) {
                try {
                    System.out.print("How many " + petPreference + " do you have? ");
                    petCount = scanner.nextInt();
                    break; // Exit the loop if a valid integer is entered
                } catch (InputMismatchException e) {
                    System.out.println("Invalid input. Please enter a valid integer.");
                    scanner.next(); // Clear the invalid input
                }
            }

            // Respond based on the number of pets
            if (petCount == 1) {
                System.out.println("You have " + petCount + " " + petPreference + ".");
            } else if (petCount == 2) {
                System.out.println("You have " + petCount + " " + petPreference + ".");
            } else if (petCount > 2) {
                System.out.println("You have " + petCount + " " + petPreference + ".");
            } else {
                System.out.println("I'm not sure how many " + petPreference + " you have.");
            }

            // Read years of IT experience (floating-point input)
            double itExperience;
            while (true) {
                try {
                    System.out.println("How many years of IT experience do you have? ");
                    itExperience = scanner.nextDouble();
                    break; // Exit the loop if a valid double is entered
                } catch (InputMismatchException e) {
                    System.out.println("Invalid input. Please enter a valid number.");
                    scanner.next(); // Clear the invalid input
                }
            }

            // Respond based on IT experience
            if (itExperience >= 0) {
                System.out.println("You have " + itExperience + " years of IT experience.");
            } else {
                System.out.println("Invalid input. Years of IT experience cannot be negative.");
            }

            // Ask if the user likes ice cream (boolean input)
            char iceCreamPreference;
            while (true) {
                try {
                    System.out.println("Do you like ice cream? (yes/no): ");
                    iceCreamPreference = scanner.next().charAt(0);
                    if (iceCreamPreference == 'y' || iceCreamPreference == 'n') {
                        break; // Exit the loop if 'y' or 'n' is entered
                    } else {
                        System.out.println("Invalid input. Please enter 'yes' or 'no'.");
                    }
                } catch (InputMismatchException e) {
                    System.out.println("Invalid input. Please enter 'yes' or 'no'.");
                    scanner.next(); // Clear the invalid input
                }
            }

            // Respond based on ice cream preference
            if (iceCreamPreference == 'y') {
                System.out.println("Great! Ice cream is delicious.");
            } else {
                System.out.println("That's okay, not everyone likes ice cream.");
            }

            // Ask if the user has worked on a software development project (boolean input)
            System.out.println("Have you ever worked on a software development project? (true/false): ");
            boolean hasWorkedOnProject = scanner.nextBoolean();
            System.out.println(hasWorkedOnProject ? "That's great! Experience is valuable." : "That's okay, everyone starts somewhere.");

            // Perform arithmetic operations (addition, subtraction, multiplication, division)
            System.out.print("Let's do some math! Enter two numbers separated by a space: ");
            int num1 = scanner.nextInt();
            int num2 = scanner.nextInt();

            int sum = num1 + num2;
            int difference = num1 - num2;
            int product = num1 * num2;
            double quotient = (double) num1 / num2;

            System.out.println("Sum: " + sum);
            System.out.println("Difference: " + difference);
            System.out.println("Product: " + product);
            System.out.println("Quotient: " + quotient);

            // Increase a number by 10 (using assignment operator)
            System.out.println("Enter a number to increase it by 10: ");
            int newNumber = scanner.nextInt();
            newNumber += 10;
            System.out.println("After increasing by 10, the number is: " + newNumber);

            // Compare a number with 50 (using relational operators)
            System.out.println("Enter a number to compare with 50: ");
            int comparisonNumber = scanner.nextInt();

            if (comparisonNumber < 50) {
                System.out.println(comparisonNumber + " is less than 50.");
            } else if (comparisonNumber > 50) {
                System.out.println(comparisonNumber + " is greater than 50.");
            } else {
                System.out.println(comparisonNumber + " is equal to 50.");
            }

        } catch (InputMismatchException e) {
            System.out.println("Invalid input. Please enter a valid value.");
        } finally {
            scanner.close();
        }
    }
}
