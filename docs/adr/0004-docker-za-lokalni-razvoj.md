# Docker za lokalni zagon podatkovne baze in pomožnih storitev

## Kontekst in problem

Za razvoj potrebujem delujočo bazo PostgreSQL, kasneje pa tudi orodje Mailpit za testiranje e-pošte. Če bi te storitve nameščal ročno, bi bil projekt težko zagnati na drugem računalniku, na primer pri asistentu, ki bo projekt pregledoval, ali na mojem drugem računalniku. Odločiti sem se moral, kako bom te storitve zaganjal lokalno.

## Obravnavane možnosti

* Docker in Docker Compose
* Ročna namestitev PostgreSQL in ostalih storitev na računalnik
* Podatkovna baza v oblaku

## Odločitev

Izbrana možnost: Docker in Docker Compose, ker lahko vse pomožne storitve opišem v eni datoteki in jih zaženem z enim ukazom. Projekt ima tako na vsakem računalniku enako različico baze z enakimi nastavitvami, kdor ga želi zagnati, pa mu ni treba ničesar nameščati ročno. Docker že dobro poznam.

Pri ročni namestitvi bi bilo treba na vsakem računalniku posebej namestiti in nastaviti pravo različico. Baza v oblaku bi bila odvisna od internetne povezave in morebitnih omejitev brezplačnega paketa.

### Posledice

* Dobro, ker se baza in Mailpit zaženeta z enim ukazom.
* Dobro, ker projekt deluje enako na vsakem računalniku, zato je manj napak, ki se pojavijo samo na enem.
* Dobro, ker lahko kasneje v Docker dodam tudi backend in frontend ter celotno aplikacijo zaženem naenkrat.
* Slabo, ker moram pri težavah razumeti tudi delovanje Dockerja, na primer kje so shranjeni podatki baze.
