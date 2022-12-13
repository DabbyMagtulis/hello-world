# hello-world
4/25/2022 The Year of Awakening | The Alchemist Project (My First Repository)

#include <iostream>
#include <string>
#include <bitset>
#include <algorithm>

using namespace std;

int main()
	{
		string answer;
		string identity;

		cout << "Are you ready to exit the Matrix?" << endl;
		cout << "Yes" << " | " << "No" << endl;
		cin >> answer;

		transform(answer.begin(), answer.end(), answer.begin(), toupper);

		if (answer == "YES")
			{
				cout << "Confirm your identity: ";
				cin.ignore();
				getline(cin, identity);
			}
		else if (answer == "NO")
			{
				cout << "Goodbye." << endl;
				return 0;
			}

		cout << "Hello,";

		for (int i = 0; i < identity.size(); i++)
			{
				cout << " " << bitset<8>(identity.c_str()[i]);
			}
		
		cout << ". It's nice to finally meet you." << endl << endl;
		cout << "This is where your journey begins." << endl;

		cout << " . . ." << endl;

		srand((unsigned)time(NULL));
		int godparticle = (rand() % 999) + 1;
		int number = rand();

		cout << "Remember this number: " << number * godparticle << ". You will know what it means when the time comes." << endl;

		return 0;
	}
