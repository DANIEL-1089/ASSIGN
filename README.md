#include <iostream>
#include <ctime>
#include <wchar.h>
#include <Windows.h>
#include <algorithm>
#include <vector>
#include <string>
#include <string.h>
#include <stdlib.h>
#include <cstring>
#include <conio.h>
#include <iomanip>
#include <process.h>
#include <ctime>
#include <cstdlib>



using namespace std;
class alpha {
private:
    int data;
public:
    alpha()
    {}
    alpha(int d) {
        data = d;
    }
    void display() {
        cout << data;
    }
    alpha operator = (alpha& a) {
        data = a.data;
        cout << "\nThe assignment operator is started";
        return alpha(data);
    }
};


int main()
{
    alpha a1(37);
    alpha a2;

    a2 = a1;
    cout << "\na2 = ";
    a2.display();

    alpha a3 = a2;
    cout << "\na3 = ";
    a3.display();
    cout << endl;

    return 0;
}
