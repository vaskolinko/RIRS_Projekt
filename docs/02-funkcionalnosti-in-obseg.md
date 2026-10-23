# Funkcionalnosti in obseg

## Uporabniške vloge

| Vloga | Lahko | Ne more |
|---|---|---|
| **Etažni lastnik** | prijavi okvaro, potrdi njeno odpravo, glasuje v imenu svojega stanovanja, bere obvestila, povabi najemnika | dodeljevati serviserjev, odpirati glasovanj, videti, kako so glasovali drugi |
| **Najemnik** | prijavi okvaro, potrdi njeno odpravo, bere obvestila | glasovati, vabiti uporabnikov |
| **Predstavnik lastnikov** | vse kot lastnik, poleg tega predlaga sklepe in vidi vse okvare v stavbi | sam odpreti glasovanja, dodeljevati serviserjev |
| **Upravnik** | ureja stavbo in stanovanja, vabi uporabnike, dodeljuje okvare serviserjem, odpira glasovanja, objavlja obvestila | glasovati namesto lastnikov, spreminjati oddanih glasov ali zgodovine okvar |
| **Serviser** | vidi njemu dodeljene okvare, spreminja njihov status, doda poročilo in fotografijo | videti drugih okvar, glasovanj in obvestil, sam zapreti okvare kot potrjene |

## Predvidene funkcionalnosti

| # | Funkcionalnost | MVP |
|---|---|---|
| 1 | Upravnik vnese/ustvari stavbo in stanovanja | **MVP** |
| 2 | Vabila: upravnik povabi lastnike in serviserje, lastnik povabi najemnika | **MVP** |
| 3 | Prijava okvare s kategorijo, nujnostjo, lokacijo in fotografijo | **MVP** |
| 4 | Potek reševanja okvare: prijavljeno → dodeljeno serviserju → v delu → zaključeno → potrjeno, z zgodovino sprememb  | **MVP** |
| 5 | Glasovanje o sklepih: en glas na stanovanje, izbira praga (več kot polovica, tri četrtine, vsa stanovanja) in roka  | **MVP** |
| 7 | Obvestila stavbe z evidenco, kdo jih je prebral | **MVP** |
| 6 | Samodejni zaključek glasovanja ob roku ali ko je izid že gotov  |  |
| 8 | Združevanje podvojenih prijav iste okvare  | |
| 9 | Predstavnik pripravi predlog sklepa, upravnik ga objavi kot glasovanje | |
| 10 | Pooblastilo drugemu lastniku za glasovanje  | |
| 11 | Glasovanje o izbiri med ponudbami izvajalcev  | |
| 12 | Rezervacija skupnih prostorov (pralnica, skupna soba) brez prekrivanj  | |
| 13 | Opomniki za redne preglede (dvigalo, gasilni aparati)  | |
| 14 | Nadzorna plošča upravnika: odprte okvare in aktivna glasovanja | |
| 15 | Avtentikacija uporabnikov (dodelitev roles) | MVP |
| 16 | Email sporočanje o obvestilih | MVP |

MVP vsebuje 6 funkcionalnosti.

## Kasnejše nadgradnje

- e-poštna obvestila ob spremembah
- izvoz zapisnika glasovanja v PDF
- prijava z državno e-identiteto (SI-PASS)
- statistika časa reševanja okvar
- QR koda v stavbi za hitro prijavo okvare

## Izven obsega

- pravno zavezujoče elektronsko glasovanje
- plačila, položnice in knjigovodstvo
- izvorna mobilna aplikacija
- klepet med stanovalci
