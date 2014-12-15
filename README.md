updatedproject
==============
#include <iostream>
#include <cstdlib>
#include <time.h>
#include <fstream>
#include <string>
#include <iomanip>
using namespace std;

const int NUM_STUDENTS = 29;
const int NUM_QUIZZES = 10;
const int NUM_EXAMS = 5;
int user;

struct Student
{
	string firstName;
	string lastName;
	int quizzes[NUM_QUIZZES];
	int exams[NUM_EXAMS];
};

int main()
{
	ifstream inputFile;

	inputFile.open("C:/Users/Nathalie/Desktop/finalGrades.txt");

	if (!inputFile)
	{
		cout << "Could not open file." << endl;
		exit(2);
	}

	const int NUM_STUDENTS = 2;
	Student cop1334[NUM_STUDENTS];

	cout << "\tWelcome to Gradebook \n"
		<< "\n1. Course Grade for a particular student"
		<< "\n2. Average for particular Quiz"
		<< "\n3. Average for particular Test"
		<< "\n4. The lowest quiz average"
		<< "\n5. Summary"
		<< "\n6. Breakdown of letter grades"
		<< "\n~Any other character to exit program~"
		<< "\n\nPlease choose an option from the menu: ";
	cin >> user;

		if (user == 1)
		{
			string firstname;
			cout << "Please enter the first name of the particular student:" << endl;
			cin >> firstname;
			string line;
			while (getline(inputFile, firstname))
			{
				cout << firstname << endl;
			}
			//not done!!!!!!!
		}
		else if (user == 2)
		{
			string quizzes;
					cout << "\nYou have choosen option 2" << "\nPlease choose Quiz # 1 - 10 for specific quiz average: ";
					cin >> quizzes;

			while (getline(inputFile, quizzes))
			{
				for (int i = 0; i < NUM_STUDENTS; i++)
						{
					cout << quizzes[i] << endl;
				}
			}
					//not done
		}
		else if (user == 3)
		{
			string test;
			cout << "\nYou have choosen option 3" << "\nPlease choose Test #1 - 5 for average" << endl;

			//not done
		}
		else if (user == 4)
		{
			cout << "\nYou have choosen option 4" << "\nThe lowest quiz average is" << endl;
			//connect to file
		}
		else if (user == 5)
		{
			cout << "\nYou have choosen option 5" << "\nSummary: " << endl;

//course grade for every student 

			//just connect to file
		}
		else if (user == 6)
		{
			cout << "\nYou have choosen option 6" << "\nCourse Breakdown: " << endl;
			int grade;
			if (grade >= 0 && grade <= 100)
			{
				if (grade >= 90)
					cout << "Letter Grade = A" << endl;
				else if (grade >= 80)
					cout << "Letter Grade = B" << endl;
				else if (grade >= 70)
					cout << "Letter Grade = C" << endl;
				else if (grade >= 60)
					cout << "Letter Grade = D" << endl;
				else
					cout << "Letter Grade = F" << endl;
			}

		}
		
		else
		{
			cout << "You are exiting the program. Thank you!" << endl;
			system("pause");
			exit(0);
		}
	
	system("pause");
	return 0;
}
