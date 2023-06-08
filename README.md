# Another-queries

Problema 4 - Queries again...

    Modularizam problema cu ajutorul headerului intitulat "function4.h"

        Incepem prin citirea dimensiunii a unui careu si citirea numarului de operatii
    pe care urmeaza sa le facem. Citim si continutul sudokului.
        Operatiile sunt numerotate de la 1 la 6 si structura de decizie "switch" ne permite
    sa le accesam intr un mod elegant. Totodata fiecare operatie in parte este modularizata
    prin functiile:
        -posibilitati_linie (operatia 1)
        -posibilitati_coloana (operatia 2)
        -posibilitati_careu (operatia 3)
        -posibilitati_coordonate (operatia 4) Trebuie sa verificam ce numere exista atat pe 
    linia, coloana si careul corespunzatoare coordonatelor introduse de la tastatura.
    Astfel ne putem da seama ce numere putem pune.
        -adaugare_numar (operatia 5)
        -stare_curenta (operatia 6) Pentru a stabili daca tabla de Sudoku se afla intr o pozitie
    invalida, am luat fiecare linie, coloana si careu in parte, iar intr un vector de frecventa
    am memorat aparitiile fiecarui numar. Daca frecventa >= 2 inseamna ca este o configuratie
    invalida. (daca gasim acelasi numar de doua ori pe o linie / coloana / careu, inseamna ca nu e ok)
        Pentru a stabili daca configuratia tablei mai poate fi continuata, verificam daca exista
    patrate egale cu 0 (adica goale). Daca aceasta conditie se indeplineste si tabela nu e invalida
    inseamna ca mai poate fi continuata.
        Daca tabla nu e invalida si nu se poate continua, inseamna ca jocul este castigat.
