# React za izdelavo uporabniškega vmesnika

## Kontekst in problem

NašBlok je spletna aplikacija, ki jo uporabniki odprejo v brskalniku. Vmesnik mora biti odziven, da se lepo prikaže tako na računalniku kot v brskalniku na telefonu. Poleg tega mora prikazovati različne zaslone glede na vlogo uporabnika, sproti posodabljati podatke, kot so statusi okvar in stanje glasovanja, in ostati pregleden, ko bo aplikacija dobivala nove funkcionalnosti. Odločiti sem se moral, s čim bom frontend gradil.

## Obravnavane možnosti

* React
* Vue
* Strežniško generirane strani s predlogami v Pythonu (Jinja2) brez ločenega frontenda

## Odločitev

Izbrana možnost: React, ker z njim že imam izkušnje, zato bom hitreje prišel do delujoče različice. React omogoča razdelitev vmesnika na manjše komponente, na primer kartico okvare ali obrazec za glasovanje, ki jih lahko uporabim na več zaslonih. Skupaj s Tailwind CSS lahko enostavno naredim odziven vmesnik, ki se na ožjem zaslonu prilagodi, na primer stranski meni se skrije, stolpci pa se zložijo eden pod drugega.

Vue bi bil tehnično enako primeren, vendar z njim nimam izkušenj. Strežniško generirane strani bi bile za začetek preprostejše, a bi težje dosegel interaktivne zaslone, kot je sprotno glasovanje, in ne bi imel ločenega API-ja za kasnejše nadgradnje.

### Posledice

* Dobro, ker React poznam in lahko takoj začnem z delom.
* Dobro, ker obstaja veliko knjižnic, ki jih potrebujem, na primer za koledar, zemljevid in obrazce.
* Dobro, ker je frontend ločen od backenda, zato ju lahko razvijam in testiram neodvisno.
* Dobro, ker ena spletna aplikacija deluje na računalniku in telefonu, zato ne potrebujem ločene mobilne aplikacije.
* Slabo, ker moram vzdrževati dva ločena projekta in skrbeti, da se frontend in backend ujemata.
* Slabo, ker moram posebej poskrbeti za prijavo in varno pošiljanje žetonov med frontendom in backendom.
