# Uporabniške zgodbe

---

## US-01 Ustvarjanje stavbe in stanovanj (MVP)

**Funkcionalnost:** F1 Upravnik vnese oziroma ustvari stavbo in stanovanja
**Vloga:** upravnik

**Kot** upravnik **želim** v aplikacijo vnesti stavbo in vsa njena stanovanja, **da** lahko vanjo povabim stanovalce in stavbo začnem upravljati na enem mestu.

**Acceptance criteria:**
- Upravnik ustvari stavbo tako, da vpiše njeno ime in naslov, pri čemer sta obe polji obvezni.
- Vsakemu stanovanju upravnik določi oznako, na primer Stanovanje 7 v drugem nadstropju, dve stanovanji v isti stavbi pa ne moreta imeti enake oznake.
- Na seznamu stanovanj upravnik vidi oznako stanovanja in število ljudi, ki so z njim povezani.
- Stanovanja, ki ima že povezane stanovalce, glasove ali prijave okvar, ni mogoče izbrisati.
- Stavbo lahko vidi in ureja samo upravnik, ki jo je ustvaril.

## US-02 Vabila v stavbo (MVP)

**Funkcionalnost:** F2 Vabila za lastnike, serviserje in najemnike
**Vloga:** upravnik in etažni lastnik

**Kot** upravnik **želim** povabiti lastnike in serviserje v stavbo, **da** se lahko pridružijo brez tega, da bi moral njihove podatke vnašati ročno.

**Acceptance criteria:**
- Ko upravnik vabi lastnika, mora izbrati stanovanje, pri vabilu serviserja pa stanovanja ne izbira.
- Lastnik lahko povabi najemnika samo v stanovanje, ki je v njegovi lasti.
- Vsako vabilo ima svojo kodo, ki jo je mogoče uporabiti samo enkrat in velja sedem dni.
- Kdor je poslal vabilo, vidi, ali vabilo še čaka, je bilo že uporabljeno ali je poteklo, in ga lahko prekliče, dokler ni uporabljeno.

## US-03 Prijava okvare (MVP)

**Funkcionalnost:** F3 Prijava okvare s kategorijo, nujnostjo, lokacijo in fotografijo
**Vloga:** etažni lastnik in najemnik

**Kot** stanovalec **želim** hitro prijaviti okvaro in ji dodati fotografijo, **da** upravnik takoj ve, kaj je narobe in kje se to nahaja.

**Acceptance criteria:**
- Stanovalec mora vpisati naslov, izbrati kategorijo okvare, nujnost in lokacijo, ki je lahko njegovo stanovanje ali skupni del stavbe.
- Kategorije so vodovod, elektrika, dvigalo, ogrevanje in drugo, nujnost pa je lahko nizka, normalna ali nujna.
- Fotografija ni obvezna, če pa jo stanovalec doda, mora biti v formatu JPG ali PNG in manjša od 5 MB.
- Ko stanovalec odda prijavo, ta dobi status prijavljeno in se takoj pojavi na seznamu okvar pri upravniku.
- Stanovalec vidi vse svoje prijave na enem mestu, skupaj z datumom prijave in trenutnim statusom.

## US-04 Potek reševanja okvare (MVP)

**Funkcionalnost:** F4 Potek reševanja okvare z zgodovino sprememb
**Vloga:** prijavitelj okvare, upravnik in serviser

**Kot** stanovalec, ki je prijavil okvaro, **želim** spremljati, kako poteka popravilo, in na koncu potrditi, da je okvara res odpravljena, **da** vem, kdaj bo težava rešena, in da se zadeva ne zaključi prezgodaj.

**Acceptance criteria:**
- Okvara gre skozi statuse prijavljeno, dodeljeno, v delu, zaključeno in potrjeno, vsak status pa lahko nastavi samo oseba, ki je za ta korak odgovorna.
- Serviser vidi samo okvare, ki so dodeljene njemu, in mora ob zaključku dela napisati kratko poročilo o tem, kaj je naredil.
- Ko serviser okvaro zaključi, lahko prijavitelj potrdi, da je odpravljena, ali pa jo z obrazložitvijo vrne v reševanje.
- Vsaka sprememba statusa se zabeleži skupaj z imenom osebe, ki jo je naredila, ter datumom in uro, teh zapisov pa ne more spreminjati nihče.

## US-05 Glasovanje o sklepu (MVP)

**Funkcionalnost:** F5 Glasovanje o sklepih z enim glasom na stanovanje, izbiro praga in rokom
**Vloga:** upravnik in etažni lastnik

**Kot** etažni lastnik **želim** glasovati o predlogih sklepov kar v aplikaciji, **da** lahko sodelujem pri odločitvah v stavbi, ne da bi nekdo hodil od vrat do vrat in zbiral podpise.

**Acceptance criteria:**
- Upravnik pri odprtju glasovanja vpiše naslov, opis, rok in izbere, ali je za sprejem potrebna več kot polovica stanovanj, več kot tri četrtine ali vsa stanovanja.
- Rok za glasovanje mora biti vsaj en dan po odprtju glasovanja.
- Glasuje lahko samo lastnik, in sicer v imenu svojega stanovanja, najemnik pa glasovanja ne vidi.
- Vsako stanovanje lahko odda samo en glas, ki je lahko za, proti ali vzdržan, in ga kasneje ni mogoče spremeniti.
- Število potrebnih glasov se računa glede na vsa stanovanja v stavbi, kar pomeni, da je pri dvajsetih stanovanjih in pragu več kot polovice potrebnih enajst glasov za.

## US-06 Samodejni zaključek glasovanja

**Funkcionalnost:** F6 Samodejni zaključek glasovanja ob roku ali ko je izid že znan
**Vloga:** etažni lastnik in upravnik

**Kot** etažni lastnik **želim**, da se glasovanje zaključi takoj, ko je izid jasen, **da** upravniku ni treba čakati na rok, preden lahko sklep izvede.

**Acceptance criteria:**
- Ko število glasov za doseže potreben prag, se glasovanje zaključi in sklep je sprejet, tudi če rok še ni potekel.
- Ko praga ni več mogoče doseči, tudi če bi vsa preostala stanovanja glasovala za, se glasovanje zaključi in sklep ni sprejet.
- Ko poteče rok, se glasovanje zaključi samo od sebe, ne glede na to, ali ga je kdo odprl.
- Pri vsakem zaključenem glasovanju je zapisano, zakaj se je zaključilo, torej ali zaradi doseženega praga, ker praga ni bilo več mogoče doseči, ali zaradi poteka roka.

## US-07 Obvestila stavbe (MVP)

**Funkcionalnost:** F7 Obvestila stavbe z evidenco, kdo jih je prebral
**Vloga:** upravnik

**Kot** upravnik **želim** objaviti obvestilo za vse stanovalce in videti, kdo ga je že prebral, **da** vem, ali je pomembna informacija prišla do vseh.

**Acceptance criteria:**
- Upravnik objavi obvestilo z naslovom, ki je dolg največ 100 znakov, in besedilom, pri čemer sta obe polji obvezni.
- Obvestilo je takoj vidno vsem lastnikom in najemnikom v stavbi, serviserjem pa ne.
- Stanovalec ima neprebrana obvestila posebej označena kot nova, ko obvestilo prvič odpre, pa se zabeleži, kdo ga je prebral in kdaj.
- Upravnik pri vsakem obvestilu vidi, koliko stanovalcev ga je prebralo, in seznam njihovih imen.


## US-09 Predlog sklepa predstavnika

**Funkcionalnost:** F9 Predstavnik pripravi predlog sklepa, upravnik ga objavi kot glasovanje
**Vloga:** predstavnik etažnih lastnikov

**Kot** predstavnik etažnih lastnikov **želim** pripraviti predlog sklepa, **da** lahko lastniki glasujejo tudi o stvareh, ki jih ne predlaga upravnik.

**Acceptance criteria:**
- Predstavnik vpiše naslov, obrazložitev in predlagani prag, predlog pa nato čaka na objavo.
- Upravnik vidi vse predloge in lahko vsakega objavi kot glasovanje z rokom ali ga zavrne in napiše razlog.
- Predstavnik vidi, kaj se dogaja z njegovim predlogom, in v primeru zavrnitve tudi razlog.
- Predstavnik glasovanja ne more odpreti sam.

## US-10 Pooblastilo za glasovanje

**Funkcionalnost:** F10 Pooblastilo drugemu lastniku za glasovanje
**Vloga:** etažni lastnik

**Kot** etažni lastnik **želim** pooblastiti drugega lastnika, da glasuje namesto mene, **da** se glas mojega stanovanja upošteva tudi takrat, ko sam ne utegnem glasovati.

**Acceptance criteria:**
- Lastnik lahko pri posameznem odprtem glasovanju za pooblaščenca izbere samo drugega lastnika iz iste stavbe.
- Pooblaščenec pri tem glasovanju lahko glasuje tudi v imenu stanovanja, za katerega je dobil pooblastilo.
- Pri glasu, oddanem s pooblastilom, je zabeleženo, kdo je glasoval in v čigavem imenu.
- Lastnik lahko pooblastilo prekliče, dokler pooblaščenec še ni glasoval.

## US-11 Glasovanje o ponudbah izvajalcev

**Funkcionalnost:** F11 Glasovanje o izbiri med ponudbami izvajalcev
**Vloga:** upravnik in etažni lastnik

**Kot** etažni lastnik **želim** primerjati ponudbe različnih izvajalcev in glasovati za eno, **da** skupaj izberemo najboljšo ponudbo za večja dela v stavbi.

**Acceptance criteria:**
- Upravnik h glasovanju doda od dve do pet ponudb, pri čemer ima vsaka ime izvajalca, ceno in priloženo ponudbo v obliki PDF.
- Lastnik vidi vse ponudbe drugo ob drugi in glasuje za natanko eno.
- Izbrana je ponudba, ki dobi največ glasov in hkrati doseže potreben prag, če je nobena ne doseže, ni izbrana nobena.
- Če imata dve ponudbi enako število glasov, aplikacija to prikaže in upravnik lahko odpre novo glasovanje samo med njima.

## US-12 Rezervacija skupnih prostorov

**Funkcionalnost:** F12 Rezervacija skupnih prostorov brez prekrivanj
**Vloga:** etažni lastnik in najemnik

**Kot** stanovalec **želim** rezervirati termin v pralnici ali skupni sobi, **da** lahko prostor uporabim takrat, ko ga potrebujem, brez dogovarjanja s sosedi.

**Acceptance criteria:**
- Stanovalec vidi koledar izbranega prostora za ta in naslednji teden, kjer so prosti in zasedeni termini jasno ločeni.
- Rezervirati je mogoče samo prost termin, pri poskusu rezervacije zasedenega termina pa aplikacija sporoči, da je termin že zaseden.
- Eno stanovanje ima lahko največ tri aktivne rezervacije na teden.
- Stanovalec lahko svojo rezervacijo prekliče najkasneje eno uro pred začetkom termina.

## US-13 Opomniki za redne preglede

**Funkcionalnost:** F13 Opomniki za redne preglede, na primer dvigala in gasilnih aparatov
**Vloga:** upravnik

**Kot** upravnik **želim** imeti pregled nad vsemi obveznimi rednimi pregledi in njihovimi roki, **da** nobenega pregleda ne zamudim.

**Acceptance criteria:**
- Upravnik doda pregled tako, da vpiše njegovo ime, datum zadnjega pregleda in na koliko mesecev se ponavlja.
- Aplikacija sama izračuna datum naslednjega pregleda, pregledi pa so razvrščeni po datumu.
- Trideset dni pred rokom je pregled označen kot bližajoč se, po roku pa kot zamujen.
- Ko upravnik vpiše datum opravljenega pregleda, aplikacija izračuna nov rok.

## US-14 Nadzorna plošča upravnika

**Funkcionalnost:** F14 Nadzorna plošča upravnika z odprtimi okvarami in aktivnimi glasovanji
**Vloga:** upravnik

**Kot** upravnik **želim** na enem mestu videti odprte okvare in aktivna glasovanja v vseh svojih stavbah, **da** hitro ugotovim, kje moram ukrepati.

**Acceptance criteria:**
- Za vsako stavbo je prikazano, koliko okvar je odprtih, koliko od teh je nujnih in koliko glasovanj je aktivnih.
- Odprte okvare so razvrščene najprej po nujnosti in nato po datumu prijave, tako da so najstarejše na vrhu.
- Pri vsakem aktivnem glasovanju je prikazano, koliko glasov je že oddanih, koliko jih je potrebnih in do kdaj traja glasovanje.
- S klikom na okvaro ali glasovanje upravnik odpre njene podrobnosti.

## US-15 Avtentikacija in vloge (MVP)

**Funkcionalnost:** F15 Avtentikacija uporabnikov in dodelitev vlog
**Vloga:** vsi uporabniki

**Kot** uporabnik **želim** ustvariti račun s kodo vabila in se prijaviti z e-pošto in geslom, **da** vidim samo tisto, kar pripada moji vlogi v stavbi.

**Acceptance criteria:**
- Račun je mogoče ustvariti samo z veljavno kodo vabila, ob tem pa uporabnik samodejno dobi vlogo, stavbo in stanovanje, ki so zapisani v vabilu.
- Geslo mora imeti vsaj osem znakov, z istim e-poštnim naslovom pa ni mogoče ustvariti dveh računov.
- Če uporabnik vpiše napačno e-pošto ali geslo, aplikacija sporoči, da podatki niso pravilni, ne pove pa, kateri od njih je napačen.
- Uporabnik, ki ni prijavljen, ne more dostopati do nobenih podatkov, prijavljen uporabnik pa ne more izvesti dejanj, ki niso dovoljena njegovi vlogi, na primer najemnik ne more glasovati.

## US-16 Obveščanje po e-pošti

**Funkcionalnost:** F16 Obveščanje o obvestilih po e-pošti
**Vloga:** etažni lastnik in najemnik

**Kot** stanovalec **želim** prejeti e-pošto, ko upravnik objavi novo obvestilo, **da** za pomembne stvari izvem tudi takrat, ko aplikacije ne odpiram.

**Acceptance criteria:**
- Ko upravnik objavi obvestilo, vsi lastniki in najemniki v stavbi prejmejo e-pošto z naslovom obvestila in povezavo do njega.
- Objava obvestila se zaključi takoj, e-pošta pa se pošilja v ozadju, tako da upravniku ni treba čakati.
- Uporabnik lahko v nastavitvah izklopi obveščanje po e-pošti, obvestila pa še vedno vidi v aplikaciji.
- Če pošiljanje na posamezen naslov ne uspe, se napaka zabeleži, ostali prejemniki pa e-pošto vseeno prejmejo.
