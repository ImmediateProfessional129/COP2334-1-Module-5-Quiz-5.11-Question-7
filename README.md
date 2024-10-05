# COP2334-1-Module-5-Quiz-5.11-Question-7
This is a repository link of the COP2334-1 Module 5 Quiz 5.11 Question 7

// This program is designed to gain access to a file and review the contents of the file.

// Include the necessary libraries.
#include <fstream>
#include <iostream>
#include <string>
using namespace std;
// Declare the main function.
int main() {
  string name_of_file;
  double revenue = 0, average_revenue = 0.0;
  int count = 0;
  // Declare the input file stream.
  while (true) {
    cout << "Enter the name of the file or 'stop' to exit: ";
    cin >> name_of_file;
  // Check if the user wants to exit.
    if (name_of_file == "stop") {
      break;
    }
  // Open the file.
    ifstream file(name_of_file);
    if (file.is_open()) {
    average_revenue += revenue;
    count++;
    } else {
      cout << "File not found." << endl;
    }
    file.close();
  } // Display the average revenue.
  if (count > 0) {
    average_revenue /= count;
    cout << "Average revenue: $" << average_revenue << endl;
  } else { // Display an error message if no files were found.
    cout << "0, No data found." << endl;
  }
  return 0;
}
