//# code Nexus 





#include <iostream>
using namespace std;

int main() {
    int N;
    cout << "Enter number of days: ";
    cin >> N;

    int sunbuds = 0, moonblossoms = 0, starroots = 0, crystals = 0, wildleaf = 0, resting = 0;

    for (int day = 1; day <= N; day++) {
        bool div2 = (day % 2 == 0);
        bool div3 = (day % 3 == 0);
        bool div4 = (day % 4 == 0);

        if (div2 && div3 && div4) {
            resting++;
        } 
        else if (div2 && div3) {
            crystals++;
        } 
        else if (div2) {
            sunbuds += 2;
        } 
        else if (div3) {
            moonblossoms += 3;
        } 
        else if (div4) {
            starroots += 4;
        } 
        else {
            wildleaf++;
        }
    }

    int total = sunbuds + moonblossoms + starroots + crystals + wildleaf;

    cout << "Sunbuds: " << sunbuds << "\n";
    cout << "Moonblossoms:  << moonblossoms << "\n";
    cout << "Starroots: " << starroots << "\n";
    cout << "Crystal Flowers: " << crystals << "\n";
    cout << "Wildleaf: " << wildleaf << "\n";
    cout << "Resting soil days: " << resting << "\n";
    cout << "Total flowers planted: " << total << "\n";

    return 0;
}