import java.util.Scanner;
import java.util.Random;

public class GuessingGame {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        int maxAttempts = 5;
        int score = 0;

        System.out.println("Welcome to the Guessing Game!");
        System.out.println("I'm thinking of a number between 1 and 100. You have " + maxAttempts + " attempts to guess it.");

        do {
            int secretNumber = random.nextInt(100) + 1; // Generate random number between 1 and 100 (inclusive)
            int attemptsLeft = maxAttempts;

            while (attemptsLeft > 0) {
                System.out.print("Enter your guess: ");
                int guess = scanner.nextInt();
                attemptsLeft--;

                if (guess == secretNumber) {
                    System.out.println("Congratulations! You guessed the number in " + (maxAttempts - attemptsLeft) + " attempts.");
                    score++;
                    break;
                } else if (guess < secretNumber) {
                    System.out.println("Too low, try again!");
                } else {
                    System.out.println("Too high, try again!");
                }
            }

            if (attemptsLeft == 0) {
                System.out.println("Sorry, you ran out of attempts. The number was " + secretNumber + ".");
            }

            System.out.print("Do you want to play again? (yes/no): ");
        } while (scanner.nextLine().toLowerCase().equals("yes"));

        System.out.println("Thanks for playing! Your final score is " + score + ".");
        scanner.close();
    }
}
