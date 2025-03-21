# PF-Project
#include<iostream>
#include<string>
using namespace std;

void converter(string name[], double rate[], int opt1, int opt2, double amt) {
	int i = opt1 - 1;
	int j = opt2 - 1;

	double convertedAmount = (amt / rate[i]) * rate[j];

	cout << "\n" << amt << " " << name[i] << " = " << convertedAmount << " " << name[j] << endl;
}



int main() {
	string currencyName[5] = { "USD", "GBP", "CHF", "JPY", "AUD"};
	double exchangeRate[5] = { 1.0, 0.75, 0.98, 163.25, 1.42 };
	int option1, option2, amount;

	cout << "Menu: " << endl << endl;

	for (int i = 0; i < 5; i++) {
		cout << (i + 1) << ". " << currencyName[i] << endl;
	}

	cout << "\nChoose the currency to convert from (1 - 5): ";
	cin >> option1;

	cout << endl;

	for (int i = 0; i < 5; i++) {
		cout << (i + 1) << ". " << currencyName[i] << endl;
	}

	cout << "\nChoose the currency to conver to  (1 - 5): ";
	cin >> option2;

	cout << "\nEnter the amount you want to convert: ";
	cin >> amount;

	converter(currencyName, exchangeRate, option1, option2, amount);



}
