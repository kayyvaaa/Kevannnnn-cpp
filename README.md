#include <iostream>
#include <cmath>
#include <iomanip>
using namespace std;

int main () {
    double PV, FV, r, n;

    cout << "==================================" << endl;
    cout << "|         PRESENT VALUE          |" << endl;
    cout << "==================================" << endl;

    cout << "masukan Future Value (FV): Rp ";
    cin >> FV;

    cout << "masukan Suku Bunga (r) Dalam %: " << endl;
    cin >> r;

    cin.ignore();

    cout << "masukan Waktu (n) dalam tahum: " << endl;
    cin >> n;

    // simpan nilai asli unuk di tampilkan
    double r_input = r;

    r = r /100;
    PV = FV * pow(1 + r, -n);

    cout << endl;
    cout << "     Hasil Perhitungan     " << endl;
    cout <<"----------------------------" << endl;
    cout << fixed << setprecision(2);
    cout << "Future Value   : Rp " << FV <<  endl;
    cout << "Suku Bunga     : " << r_input << "%" << endl;
    cout << "Waktu          : " << n  << "Tahun" << endl;
    cout << endl;

    cout << "      Cara Pengerjaan     " << endl;
    cout <<"---------------------------" << endl;
    cout << "Rumus Menentukan Present Value =" << endl;
    cout << " PV = FV (1 + r)^-n" << endl;
    cout << endl;

    cout << " r = " << r_input << " % / 100" <<" = " << r << endl;
    cout << " 1 + r = 1 + " << r << " = " << r << ( 1 + r) << endl;
    double pangkat = pow(1 + r, -n);

    cout << " ( 1 + r )^-n = (" << ( 1 + r ) << ")^-n" << " = " << pangkat << endl;
    cout << endl;
    cout << "PV = " << FV << " x " << pangkat << endl;
    cout << "PV = " << PV << endl;
    cout << endl;

    cout << "Hasil Dari Present Value" << endl;
    cout << fixed << setprecision(2);
    cout << "Present Value (PV): Rp " << PV << endl;
    cout << endl;

    return 0;
}
