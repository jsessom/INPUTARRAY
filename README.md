# INPUTARRAY
INPUTS NUMBERS FROM FILE INTO ARRAY 
#include <iostream>
#include <fstream>
#include <string>
using namespace std;

int main()
{
	int sum = 0;
	int intarray[6];




	//ifstream inputfile("Z:\\CS-246\\ConsoleApplication3Average\\Average.txt");
	ifstream inputfile("Z:\\CS-246\\ConsoleApplication4\\Studentdatafile.txt");
	//inputfile.open("Studentdatafile.txt");

	if (!inputfile)
	{
		cerr << "File is not open." << endl;
		exit(1);
	}

	/*while (inputfile)
	{
	int data = 0;
	inputfile >> data;
	sum = sum + data;
	cout << "the current number =" << sum << endl;
	}
	*/
	for (int i = 0; i < 6; i++)
	{
		//cout << "Please enter each number." << endl;
		inputfile >> intarray[i];
		sum = sum + intarray[i];
		cout << "The current number = " << sum << endl;
	}
	
	//cout <<"The average is "<< sum/6 << endl;


	return 0;
}
