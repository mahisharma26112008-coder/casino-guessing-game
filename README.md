# casino-guessing-game


#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    int guess, number;
    int points = 100;

    srand(time(0));

    cout << "===== CASINO GAME =====" << endl;
    cout << "Starting Points: " << points << endl;

    cout << "Guess a number (1 to 5): ";
    cin >> guess;

    number = rand() % 5 + 1;

    cout << "Random Number: " << number << endl;

    if (guess == number) {
        points += 10;
        cout << "You Win!" << endl;
    } else {
        points -= 10;
        cout << "You Lose!" << endl;
    }

    cout << "Your Points: " << points << endl;

    return 0;
}
