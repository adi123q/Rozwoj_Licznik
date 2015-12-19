#include <iostream>
#include <fstream>
#include <conio.h>

using namespace std;

int podliczenie (int a)
{

    fstream plik;
   plik.open("Czas.txt",ios::out|ios::app);
            int str;// tyle stron teraz
            int sprawdza=0,suma=0,zPliku;// sprawdza czy w pliku cos jest, liczy sume, przechowuje tymczasow¹ liczbe
            cout<< "ILE MINUT ZMARNOWALES ... PRZYZNAJ SIE\n LICZBA MINUT:  ";
            cin >> str;
            plik << str<< " "; // zapisuje do pliku !!!!

            plik.close();

    if(plik.good()==false) cout<<"Nie mozna otworzyc pliku!";

    else
{


    suma += a;

}
    plik.close();
    return suma;
}

int main()
{
    int selection;
    cout<< "WITAM CIESZE SIE ZE JESTES, WYBIERZ CO CIE INTERESUJE: "<<endl;
    cout<< "1. ZMARNOWANY CZAS "<<endl;
    cout<< "2. ILE STRON PRZECZYTALES "<<endl;
    cout<< "3. ILE SLOWEK POZNALES "<<endl<< endl << "WYBRALES: ";
   // cout<< "4. PRZYPILNUJE CIE ZEBYS SIE NAUCZYL"<< endl << "WYBRALES: ";
    cin>> selection;

    int wastedTime=0,tmp;


string a;
     switch (selection)
    {
        case 1:
            {
            fstream plik1;
            cout << "TO TY DECYDUJESZ JAK WYKORZYSTAC KAZDA MINUTE ... NIE ZMARNUJ JEJ !!!\n";
            plik1.open("Czas.txt",ios::out|ios::app);
            int str;// tyle stron teraz
            int sprawdza=0,suma=0,zPliku=0;// sprawdza czy w pliku cos jest, liczy sume, przechowuje tymczasow¹ liczbe
            cout<< "ILE MINUT ZMARNOWALES ... PRZYZNAJ SIE\n LICZBA MINUT:  ";
            cin >> str;
            plik1 << str<< " "; // zapisuje do pliku !!!!

            plik1.close();

            plik1.open("czas.txt",ios::in);

            if (plik1.good())
            {
                while (!plik1.eof())
                {
                    sprawdza ++; // sprawdza ile jest lini
                    plik1>>zPliku;// zapisuje z pliku do zmiennej
                    suma += zPliku;

                }
                cout << "LENIU ZMARNOWALES JUZ: "<< suma/2 << "  MINUT";
            }

                else
            {
                cout << "BRAK PLIKU "<<endl;
            }
             plik1.close();

             cin>> a;


             break;
            }
        case 2:
            {

                fstream plik2;

            plik2.open("Strony.txt",ios::out|ios::app);
            int str;// tyle stron teraz
            int sprawdza=0,suma=0,zPliku;// sprawdza czy w pliku cos jest, liczy sume, przechowuje tymczasow¹ liczbe
            cout<< "W KSIAZKACH ZNAJDZIECIE ODPOWIEDZI NA WSZYSTKIE PYTANIA \nILE STRON PRZECZYTALES?\nLICZBA STRON:  ";
            cin >> str;
            plik2 << str<< " "; // zapisuje do pliku !!!!

            plik2.close();

            plik2.open("Strony.txt",ios::in);

            if (plik2.good())
            {
                while (!plik2.eof())
                {
                    sprawdza ++; // sprawdza ile jest lini
                    plik2>>zPliku;// zapisuje z pliku do zmiennej
                    suma += zPliku;

                }
                cout << "GRATULACJE PRZECZYTALES JUZ: "<< suma/2 << " STRONY!!!";
            }

                else
            {
                cout << "BRAK PLIKU "<<endl;
            }

            cin>> a;
             plik2.close();

           /* if (sprawdza==0)
            {
              plik2 << str << endl;
              cout <<  "W sumie przeczytales juz: " << str<< " stron.\n";
            }
            else
            {
                podliczenie (str);
                cout << "W  przeszytales: "<< podliczenie(str)<< " stron.\n";
            }  */

            plik2.close();
                break;
            }
        case 3:
            {
                fstream plik3;
                 cout << "GRANICE MOJEGO JEZYKA SA GRANICAMI MOJEGO SWIATA\nPOZNAWAJ JE NIEUSTANNIE!!!\n";
            plik3.open("Slowa.txt",ios::out|ios::app);
            int str;// tyle stron teraz
            int sprawdza=0,suma=0,zPliku;// sprawdza czy w pliku cos jest, liczy sume, przechowuje tymczasow¹ liczbe
            cout<< "ILE SLOW TERAZ POZNALES:  ";
            cin >> str;
            plik3 << str<< " "; // zapisuje do pliku !!!!

            plik3.close();

            plik3.open("Slowa.txt",ios::in);

            if (plik3.good())
            {
                while (!plik3.eof())
                {
                    sprawdza ++; // sprawdza ile jest lini
                    plik3>>zPliku;// zapisuje z pliku do zmiennej
                    suma += zPliku;

                }
                cout << "GRATULACJE POZNALES JUZ: "<< suma/2 << "  SLOW\n MOWIA ZE TYSIAC SLOW WYSTARCZY BY POROZUMIEC SIE W DOWOLNYM JEZYKU"<<endl;
                if (suma/2<1000)
                {
                    int cel;
                    cel = 1000 - (suma/2);
                    cout<< "DLATEGO UCZ SIE DALEJ. BRAKUJE CI JESZCZE: "<<cel;1
                }
                else
                {
                    cout<< "DLATEGO POWINIENES JUZ DAC RADE";
                }

            }

                else
            {
                cout << "BRAK PLIKU "<<endl;
            }
             plik3.close();
             cin>> a;
             break;
            }

        case 4:
            {




             break;


            }


    }


    return 0;
    }

