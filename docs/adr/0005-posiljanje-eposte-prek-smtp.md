# Pošiljanje e-pošte prek SMTP s knjižnico fastapi-mail

## Kontekst in problem

Aplikacija mora stanovalce po e-pošti obvestiti o novih obvestilih stavbe. Med razvojem ne smem pošiljati prave e-pošte, pošiljanje pa ne sme upočasniti objave obvestila. Odločiti sem se moral, kako bo backend pošiljal e-pošto.

## Obravnavane možnosti

* fastapi-mail prek SMTP, z Mailpitom za razvoj in Brevom za pravo pošiljanje
* Neposredna uporaba Brevo API-ja
* Vgrajena Python knjižnica smtplib

## Odločitev

Izbrana možnost: fastapi-mail prek SMTP, ker SMTP podpirajo skoraj vsi ponudniki, zato je koda vedno enaka in med razvojem in pravim pošiljanjem zamenjam samo nastavitve. Mailpit vsa sporočila prikaže v brskalniku, Brevo pa ima brezplačen paket, ki mi zadošča. Knjižnica podpira pošiljanje v ozadju, zato uporabnik ne čaka.

Brevo API bi me vezal na enega ponudnika, smtplib pa ni asinhron in bi moral več stvari narediti sam.

### Posledice

* Dobro, ker lahko ponudnika zamenjam brez spreminjanja kode.
* Dobro, ker med razvojem z Mailpitom ne pošiljam prave e-pošte.
* Dobro, ker se e-pošta pošilja v ozadju.
* Slabo, ker ne morem uporabljati posebnih možnosti Brevo API-ja, na primer statistike odprtih sporočil.
* Slabo, ker moram paziti, da SMTP ključ ostane v datoteki .env in ne pride na GitHub.