# To-check-whether-a-number-is-armstrong-or-not-in-c-
#include <iostream>
#include <cmath>
#include <string>

bool isArmstrongNumber(int num) {
    std::string strNum = std::to_string(num);
    int numDigits = strNum.length();
    int total = 0;

    for (char digit : strNum) {
        int digitValue = digit - '0';
        total += std::pow(digitValue, numDigits);
    }

    return num == total;
}

int main() {
    int number;
    
    std::cout << "Enter a number: ";
    std::cin >> number;

    if (isArmstrongNumber(number)) {
        std::cout << number << " is an Armstrong number." << std::endl;
    } else {
        std::cout << number << " is not an Armstrong number." << std::endl;
    }

    return 0;
}
