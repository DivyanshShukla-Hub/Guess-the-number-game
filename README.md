# Guess-the-number-game
a small Game (little little changes lead to big step)

     #include <stdlib.h>
     #include <time.h>

     int main() {
     int number, guess, attempts = 0;
       
    // Use current time as seed for random number
    srand(time(0));
    number = rand() % 100 + 1; // Random number between 1 and 100

    printf("🎯 Welcome to the Guess the Number Game!\n");
    printf("I have chosen a number between 1 and 100.\n");
    printf("Can you guess it?\n\n");

    // Loop until the user guesses the number
    do {
        printf("Enter your guess: ");
        scanf("%d", &guess);
        attempts++;

        if (guess > number) {
            printf("Too high! Try again.\n");
        } else if (guess < number) {
            printf("Too low! Try again.\n");
        } else {
            printf("🎉 Congratulations! You guessed it in %d attempts.\n", attempts);
        }

    } while (guess != number);

    return 0;
    }
THANK YOU FOR GIVING YOUR TIME
