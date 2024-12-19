# wcc
#include <iostream>
using namespace std;

void passByValue(int value) {
    value += 10;
    cout << "Inside passByValue: " << value << endl;
}

void passByReference(int &ref) {
    ref += 10;
    cout << "Inside passByReference: " << ref << endl;
}

void staticExample() {
    static int count = 0;
    count++;
    cout << "Static count: " << count << endl;
}

int main() {
    int num;
    cout << "Enter a number: ";
    cin >> num;

    passByValue(num);
    cout << "After passByValue: " << num << endl;

    passByReference(num);
    cout << "After passByReference: " << num << endl;

    staticExample();
    staticExample();

    return 0;
}
