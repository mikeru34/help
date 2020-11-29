# help

#include <iostream>
#include <conio.h>
#include <string>
using namespace std;

int main() {
	system("cls");

	struct str { string s; };
	str name[300], IDno[300];
	float mp1[300], mp2[300], mp3[300], ml1[300], ml2[300], ml3[300], me[300], cstand[300], mtg[300], gpa[300];
	int stcr, stc;

	cout << "Input number of students:";
	cin>> stcr;
	system("cls");

	for (stc = 1; stc <= stcr; stc + 1)
	{
		cout << "input first name:";
		getline(cin, name[stcr].s);
		cout << "input ID number:";
		getline(cin, IDno[stcr].s);
		system("cls");


	D:	cout << "input the grade for midterm quiz 1:";
		cin >> mp1[stcr];

		if (mp1[stcr] >= 60)
		{
			if (mp1[stcr] <= 100)
			{
				system("cls");
			}
			else
			{
				system("cls");
				cout << "error input is too high!";
				goto D;
			}
		}
		else
		{
			system("cls");
			cout << "error input is too low!";
			goto D;
		}
	dee:	cout << "input the grade for midterm quiz 2:";
		cin >> mp2[stcr];

		if (mp2[stcr] >= 60)
		{
			if (mp2[stcr] <= 100)
			{
				system("cls");
			}
			else
			{
				system("cls");
				cout << "error input is too high!";
				goto dee;
			}
		}
		else
		{
			system("cls");
			cout << "error input is too low!";
			goto dee;
		}
	deee:	cout << "input the grade for midterm quiz 3:";
		cin >> mp3[stcr];

		if (mp3[stcr] >= 60)
		{
			if (mp3[stcr] <= 100)
			{
				system("cls");
			}
			else
			{
				system("cls");
				cout << "error input is too high!";
				goto deee;
			}
		}
		else
		{
			system("cls");
			cout << "error input is too low!";
			goto deee;
		}




	Fe:	cout << "input the grade for Lab 1:";
		cin >> ml1[stcr];

		if (ml1[stcr] >= 60)
		{
			if (ml1[stcr] <= 100)
			{
				system("cls");
			}
			else
			{
				system("cls");
				cout << "error input is too high!";
				goto Fe;
			}
		}
		else
		{
			system("cls");
			cout << "error input is too low!";
			goto Fe;
		}
	Fee:	cout << "input the grade for Lab 2:";
		cin >> ml2[stcr];

		if (ml2[stcr] >= 60)
		{
			if (ml2[stcr] <= 100)
			{
				system("cls");
			}
			else
			{
				system("cls");
				cout << "error input is too high!";
				goto Fee;
			}
		}
		else
		{
			system("cls");
			cout << "error input is too low!";
			goto Fee;
		}
	Feee:	cout << "input the grade for Lab 3:";
		cin >> ml3[stcr];

		if (ml3[stcr] >= 60)
		{
			if (ml3[stcr] <= 100)
			{
				system("cls");
			}
			else
			{
				system("cls");
				cout << "error input is too high!";
				goto Feee;
			}
		}
		else
		{
			system("cls");
			cout << "error input is too low!";
			goto Feee;
		}
	
	
	De:	cout << "input the grade for Midterm Exam:";
		cin >> me[stcr];

		if (me[stcr] >= 60)
		{
			if (me[stcr] <= 100)
			{
				system("cls");
			}
			else
			{
				system("cls");
				cout << "error input is too high! \n";
				goto De;
			}
		}
		else
		{
			system("cls");
			cout << "error input is too low! \n";
			goto De;
		}

		cstand[stcr] = (((mp1[stcr] + mp2[stcr] + mp3[stcr]) / 3) * 2 / 3) + (((ml1[stcr] + ml2[stcr] + ml3[stcr]) / 3) / 3);
		mtg[stcr] = (cstand[stcr] * 2 / 3) + (me[stcr] / 3);
		if (100 >= mtg[stcr] && mtg[stcr] >= 98)
		{
			gpa[stcr] = 1.00;
		}
		else if (97 >= mtg[stcr] && mtg[stcr] >= 95)
		{
			gpa[stcr] = 1.25;
		}
		else if (94 >= mtg[stcr] && mtg[stcr] >= 92)
		{
			gpa[stcr] = 1.50;
		}
		else if (91 >= mtg[stcr] && mtg[stcr] >= 89)
		{
			gpa[stcr] = 1.75;
		}
		else if (88 >= mtg[stcr] && mtg[stcr] >= 86)
		{
			gpa[stcr] = 2.00;
		}
		else if (85 >= mtg[stcr] && mtg[stcr] >= 83)
		{
			gpa[stcr] = 2.25;
		}
		else if (82 >= mtg[stcr] && mtg[stcr] >= 80)
		{
			gpa[stcr] = 2.50;
		}
		else if (79 >= mtg[stcr] && mtg[stcr] >= 77)
		{
			gpa[stcr] = 2.75;
		}
		else if (76 >= mtg[stcr] && mtg[stcr] >= 75)
		{
			gpa[stcr] = 3.00;
		}
		else if (74 >= mtg[stcr] && mtg[stcr] >= 72)
		{
			gpa[stcr] = 4.00;
		}
		else
		{
			gpa[stcr] = 5.00;
		}
	}
	for (stc = 1; stc <= stcr; stc++)
	{
		cout << "name: " << name[stcr].s << " \n ID no,: " << IDno[stcr].s << "\n\n mq1, mq2 mq3:";

		cout << mp1[stcr] << ", "<<mp2[stcr] << ", "<<mp3[stcr] << ", ";

		cout << "\n\nLab1, Lab2, Lab3:";

		cout << ml1[stcr] << ", " << ml2[stcr] << ", " << ml3[stcr] << ", ";

		cout << "\n\n Midterm Grade: " << mtg[stcr] << "\n";
		cout << "Midterm Grade Point:" << gpa[stcr] << "\n";
		if (gpa[stcr] >= 3.00)
		{
			cout << "remarks: PASSED";
		}
		else
		{
			cout << "remarks: FAILED";
		}
	}
	
	_getch();
	return 0;

}
