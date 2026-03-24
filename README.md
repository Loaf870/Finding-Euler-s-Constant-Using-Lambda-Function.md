# Finding-Euler-s-Constant-Using-Lambda-Function.md
After many trials and errors, Euler's Constant is defined and it is a specialized term in mathematics fundamental.

Disclaimer: This work is done by using C++ language

/*

Title: Defining Euler's Constant, e
Assigned by: Mun/Fir
Date: 23/3/2026

*/

#include <iostream>
#include <cmath>
using namespace std;

// e = (1 + 1/num)^num:
auto eulerNumber(float exponent){
    return [](long double num){return pow((1 + (1/num)), num);}; // no name function leaves square brackets empty
}

int main()
{
    long double e;
    auto firstEuler = eulerNumber(e); // eulerNumber <- firstEuler, exponent <- e
    auto secondEuler = eulerNumber(e); // eulerNumber <- secondEuler, exponent <- e
    auto thirdEuler = eulerNumber(e); //eulerNumber <-thirdEuler, exponent <- e

    cout<<"The first euler value is "<<firstEuler(999)<<endl; // num <- 999
    cout<<"The second euler value is "<<secondEuler(9999)<<endl; // num <- 9999
    cout<<"The third euler value is "<<thirdEuler(99999)<<endl; // num <- 99999

    system("pause");
    return 0;
}

