# code-nexus
#include <iostream>
using namespace std;

int main() {
    int N;
    cout << "Enter number of days (N): ";
    cin >> N;

    // Counters for each flower type
    int sunbuds = 0;
    int moonblossoms = 0;
    int starroots = 0;
    int crystalFlowers = 0;
    int wildleaf = 0;
    int restingDays = 0;

    for (int day = 1; day <= N; day++) {
        bool div2 = (day % 2 == 0);
        bool div3 = (day % 3 == 0);
        bool div4 = (day % 4 == 0);

        if (div2 && div3 && div4) {
            restingDays++;
        }
        else if (div2 && div3) {
            crystalFlowers++;
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

    // Calculating total flowers
    int totalFlowers = sunbuds + moonblossoms + starroots + crystalFlowers + wildleaf;

    // Output results
    cout << "\n--- Gardener's Flower Report ---\n";
    cout << "Sunbuds: " << sunbuds << endl;
    cout << "Moonblossoms: " << moonblossoms << endl;
    cout << "Starroots: " << starroots << endl;
    cout << "Crystal Flowers: " << crystalFlowers << endl;
    cout << "Wildleaf: " << wildleaf << endl;
    cout << "Resting Days: " << restingDays << endl;
    cout << "Total Flowers Planted: " << totalFlowers << endl;

    return 0;
}