# Relacijska podatkovna baza PostgreSQL

## Kontekst in problem

Podatki v aplikaciji so med seboj tesno povezani. Stavba ima stanovanja, stanovanja imajo lastnike in najemnike, okvare se nanašajo na stavbo in stanovanje, glasovi pa na glasovanje in stanovanje. Nekatera pravila morajo veljati vedno, tudi če dva uporabnika hkrati naredita isto stvar. Najpomembnejše je, da lahko vsako stanovanje pri posameznem glasovanju odda samo en glas. Odločiti sem se moral, kakšno podatkovno bazo bom uporabil.

## Obravnavane možnosti

* PostgreSQL
* MySQL
* MongoDB

## Odločitev

Izbrana možnost: PostgreSQL, ker so moji podatki po naravi relacijski in jih je najlažje opisati s tabelami in tujimi ključi. Pravila, kot je en glas na stanovanje, lahko zapišem kar v bazo kot omejitev, zato veljajo tudi takrat, ko bi koda zaradi napake ali hkratnih zahtevkov to dovolila. PostgreSQL podpira tudi transakcije, ki jih potrebujem pri oddaji glasu in zaključku glasovanja. Za kasnejšo rezervacijo skupnih prostorov zna sam preprečiti prekrivanje terminov.

MySQL bi bil prav tako primeren, vendar nima vseh naprednih možnosti, ki jih bom potreboval pri rezervacijah. MongoDB je dokumentna baza, ki ne zagotavlja povezav med podatki, zato bi moral vsa pravila preverjati v kodi.

### Posledice

* Dobro, ker baza sama skrbi za povezanost podatkov in za pravila, kot je en glas na stanovanje.
* Dobro, ker lahko s transakcijami zagotovim, da se glas in izid glasovanja vedno zapišeta pravilno.
* Dobro, ker je PostgreSQL brezplačen in zelo razširjen.
* Slabo, ker moram vsako spremembo strukture tabel narediti z migracijo.
* Slabo, ker moram bazo za razvoj namestiti in zagnati, za kar uporabljam Docker.
