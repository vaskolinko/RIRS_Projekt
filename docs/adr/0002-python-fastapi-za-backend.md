# Python s FastAPI za izdelavo backenda

## Kontekst in problem

Backend vsebuje vso poslovno logiko aplikacije. Preverja, kaj sme posamezna vloga narediti, skrbi za pravilen vrstni red statusov okvare, šteje glasove in ugotavlja izid glasovanja ter pošilja e-pošto. Frontendu mora te podatke ponuditi prek REST API-ja. Odločiti sem se moral, v katerem jeziku in s katerim ogrodjem bom backend napisal.

## Obravnavane možnosti

* Python s FastAPI
* Python z Djangom
* Node.js z Expressom

## Odločitev

Izbrana možnost: Python s FastAPI, ker Python dobro poznam, FastAPI pa je narejen prav za izdelavo REST API-jev. Vhodne podatke preverja sam s pomočjo knjižnice Pydantic, zato mi je treba manj preverjati ročno, na primer ali ima prijava okvare izpolnjena vsa obvezna polja. Poleg tega samodejno ustvari dokumentacijo API-ja, ki jo lahko uporabim pri razvoju frontenda.

Django je zmogljiv, vendar prinaša veliko stvari, ki jih ne potrebujem, na primer lastne predloge za strani, in je za čisti API težji. Express bi pomenil, da imam na obeh straneh JavaScript, vendar Python poznam bolje.

### Posledice

* Dobro, ker Python poznam in lahko hitro napišem poslovno logiko.
* Dobro, ker FastAPI sam preverja podatke in ustvari dokumentacijo API-ja.
* Dobro, ker FastAPI podpira opravila v ozadju, kar uporabim za pošiljanje e-pošte, ne da bi uporabnik čakal.
* Slabo, ker FastAPI nima vgrajene administracije in upravljanja uporabnikov, kot ju ima Django, zato moram prijavo in vloge narediti sam.
* Slabo, ker frontend in backend nista v istem jeziku, zato tipov podatkov ne morem deliti med njima.
