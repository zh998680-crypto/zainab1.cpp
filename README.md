#include <iostream>
using namespace std;
int main() {
    int consumption;
    int pricePerUnit;
    long long totalBill;
    cout << "Enter electricity consumption (in KW): \n";
    cin >> consumption;
    if (consumption <= 100) {
        pricePerUnit = 250;
    } 
    else if (consumption > 100 && consumption <= 300) {
        pricePerUnit = 300;
    } 
    else {
        pricePerUnit = 350;
    }
    totalBill = consumption * pricePerUnit;
    cout << "\n--- Bill Summary ---" << endl;
    cout << "Consumption:    " << consumption << " units" << endl;
    cout << "Price per unit: " << pricePerUnit << " IQD" << endl;
    cout << "Total Bill:     " << totalBill << " IQD" << endl;
    cout << "Evaluation:     ";
    if (totalBill > 100000) {
        cout << "High consumption - Please reduce usage" << endl;
    } else {
        cout << "Normal consumption" << endl;
    }
    return 0;
}