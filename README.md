# ROCK-PAPER-SCISSOR-

#include <iostream>
#include <cstdlib>
using namespace std;

class Game {
private:
    string choices[3] = {"Rock", "Paper", "Scissors"};  // THINGS ARE REMAINS PRIVATE

public:
    void play() {
        int user, comp = rand() % 3;
        cout << "Enter 0: Rock, 1: Paper, 2: Scissors: ";
        cin >> user;
        
        cout << "You: " << choices[user] << " | Computer: " << choices[comp] << endl;

        if (user == comp) cout << "It's a Draw!\n";
        else if ((user == 0 && comp == 2) || (user == 1 && comp == 0) || (user == 2 && comp == 1))
            cout << "You Win!\n";
        else cout << "Computer Wins!\n";      // SHOWS OUTPUT ON SCREEN
    }
};

int main() {
    Game g;
    g.play();
}
