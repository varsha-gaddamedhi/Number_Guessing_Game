#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int secret_number, guess;
    int attempts = 0, max_attempts;
    int level;

    srand(time(0));   // Random seed

    printf("===== NUMBER GUESSING GAME =====\n");
    printf("Choose Difficulty Level:\n");
    printf("1. Easy\n");
    printf("2. Medium\n");
    printf("3. Hard\n");
    printf("Enter your choice: ");
    scanf("%d", &level);

    if (level == 1) {
        secret_number = rand() % 50 + 1;
        max_attempts = 10;
        printf("\nEasy Mode: Guess between 1 and 50\n");
    } 
    else if (level == 2) {
        secret_number = rand() % 100 + 1;
        max_attempts = 7;
        printf("\nMedium Mode: Guess between 1 and 100\n");
    } 
    else if (level == 3) {
        secret_number = rand() % 100 + 1;
        max_attempts = 5;
        printf("\nHard Mode: Guess between 1 and 100\n");
    } 
    else {
        printf("Invalid difficulty selection!\n");
        return 0;
    }

    // Guessing loop
    while (attempts < max_attempts) {
        printf("\nEnter your guess: ");
        scanf("%d", &guess);
        attempts++;

        if (guess == secret_number) {
            printf("\n🎉 Correct Answer!\n");
            printf("You guessed the number %d in %d attempts.\n", secret_number, attempts);
            return 0;
        } 
        else {
            printf("❌ Wrong guess!\n");

            if (guess < secret_number)
                printf("Hint: Your guess is too LOW.\n");
            else
                printf("Hint: Your guess is too HIGH.\n");

            printf("Attempts left: %d\n", max_attempts - attempts);
        }
    }

    // Out of attempts
    printf("\n🚫 OUT OF ATTEMPTS!\n");
    printf("The correct number was: %d\n", secret_number);
    printf("Better luck next time!\n");

    return 0;
}