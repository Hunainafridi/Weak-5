
#include <iostream>

using namespace std;

int main() {

  int turn = 0;
  char a = '1', b = '2', c = '3', d = '4', e = '5', f = '6', g = '7', h = '8', i = '9';

  
  while (true) {
    if (turn % 2 == 0) {
      
      int choice;
      cout << "Player 1: Enter a number (0-9): ";
      cin >> choice;

      switch (choice) {
        case 1: a = 'x'; break;
        case 2: b = 'x'; break;
        case 3: c = 'x'; break;
        case 4: d = 'x'; break;
        case 5: e = 'x'; break;
        case 6: f = 'x'; break;
        case 7: g = 'x'; break;
        case 8: h = 'x'; break;
        case 9: i = 'x'; break;
        default:
          cerr << "Invalid input. Please enter a valid number." << endl;
          turn--;
          break;
      }
    } else {
     
      int choice;
      cout << "Player 2: Enter a number (0-9): ";
      cin >> choice;

      switch (choice) {
        case 1: a = 'y'; break;
        case 2: b = 'y'; break;
        case 3: c = 'y'; break;
        case 4: d = 'y'; break;
        case 5: e = 'y'; break;
        case 6: f = 'y'; break;
        case 7: g = 'y'; break;
        case 8: h = 'y'; break;
        case 9: i = 'y'; break;
        default:
          cerr << "Invalid input. Please enter a valid number." << endl;
          break;
      }
    }

    
    cout << endl;
    cout << "   | " << a << " | " << b << " | " << c << " |" << endl;
    cout << "   | " << d << " | " << e << " | " << f << " |" << endl;
    cout << "   | " << g << " | " << h << " | " << i << " |" << endl;
    cout << endl;

    if (
      (a == 'x' && b == 'x' && c == 'x') ||
      (d == 'x' && e == 'x' && f == 'x') ||
      (g == 'x' && h == 'x' && i == 'x') ||
      (a == 'x' && e == 'x' && i == 'x') ||
      (c == 'x' && e == 'x' && g == 'x') ||
      (a == 'x' && d == 'x' && g == 'x') ||
      (b == 'x' && e == 'x' && h == 'x') ||
      (c == 'x' && f == 'x' && i == 'x')
    ) {
      cout << "Player 1 wins!" << endl;
      break;
    } else if (
      (a == 'y' && b == 'y' && c == 'y') ||
      (d == 'y' && e == 'y' && f == 'y') ||
      (g == 'y' && h == 'y' && i == 'y') ||
      (a == 'y' && e == 'y' && i == 'y') ||
      (c == 'y' && e == 'y' && g == 'y') ||
      (a == 'y' && d == 'y' && g == 'y') ||
      (b == 'y' && e == 'y' && h == 'y') ||
      (c == 'y' && f == 'y' && i == 'y')
    ) {
      cout << "Player 2 wins!" << endl;
      break;
    }

    turn++;
  }
}
