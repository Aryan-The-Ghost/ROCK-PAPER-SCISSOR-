# ROCK-PAPER-SCISSOR-
#include <iostream>
using namespace std;

class Game {
private:
    string choices[3] = {"Rock", "Paper", "Scissors"};
    
public:
    void showChoices() {
        cout << "Enter 0: Rock, 1: Paper, 2: Scissors: ";
    }

    string getChoice(int x) {
        return choices[x];
    }

    string checkWinner(int user, int comp) {
        if (user == comp) return "It's a Draw!";
        if ((user == 0 && comp == 2) || (user == 1 && comp == 0) || (user == 2 && comp == 1))
            return "You Win!";
        return "Computer Wins!";
    }
};

int main() {
    Game game;
    int user, comp;

    game.showChoices();
    cin >> user;
    cout << "Enter Computer Choice (0-2): ";
    cin >> comp;

    cout << "You: " << game.getChoice(user) << " | Computer: " << game.getChoice(comp) << endl;
    cout << game.checkWinner(user, comp) << endl;
}
