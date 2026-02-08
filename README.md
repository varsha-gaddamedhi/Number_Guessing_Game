🎮 Number Guessing Game (C)

A simple console-based Number Guessing Game developed using the C programming language. The game generates a random number, and the player must guess it correctly within a limited number of attempts based on the selected difficulty level. Hints are provided after each wrong guess to guide the player.

✨ Features

Random number generation using rand()

Three difficulty levels:

Easy: Guess between 1–50 with 10 attempts

Medium: Guess between 1–100 with 7 attempts

Hard: Guess between 1–100 with 5 attempts

Hints for incorrect guesses (Too High / Too Low)

Displays remaining attempts after each guess

Shows the correct number when all attempts are exhausted

🧰 Technologies Used

Programming Language: C

Compiler: GCC

Libraries Used: stdio.h, stdlib.h, time.h

▶️ How to Run the Program
Compile the program
gcc number_guessing_game.c -o game
Run the program
./game

(On Windows, use game instead of ./game)

📂 Project Structure
Number_Guessing_Game/
├── number_guessing_game.c
└── README.md
🎯 How to Play

Run the program.

Select a difficulty level.

Enter your guesses within the allowed number of attempts.

Use the hints to adjust your guesses.

Win by guessing the correct number before attempts run out.

📌 Author

Developed as a beginner-friendly C programming project.