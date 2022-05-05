#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;
int main()
{
	srand(static_cast <unsigned int>(time(0)));
	int randomNumber = rand() % 100 + 1;
	int tries = 0;
	char answer = ' ';
	
	cout << "\tWelcome to Guess My Number\n\n" << randomNumber << " :Random Number ";
	do
	{
		cout << " Enter a guess\n H - high random number \n L - low random number ";
		++tries;
		cin >> answer;
		if (answer == 'H')
		{
			randomNumber = rand() % 50 + 1 ;
			cout << randomNumber << " :Your number";
		
		}
		else if (answer == 'L')
		{
			randomNumber = rand() % 50 - 1;
			cout << randomNumber << " :Your number";
		}
		else
		{
			cout << randomNumber << endl;
			cout << "\nThat's it! You got it in " << tries << " guesses!\n";
		
		}
	} while (answer == 'eq'); {
		
	}
	
	
}

