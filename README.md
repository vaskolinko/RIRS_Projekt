# NašBlok

NašBlok je spletna aplikacija za upravljanje večstanovanjske stavbe. Stanovalci v njej prijavljajo okvare in spremljajo njihovo reševanje, lastniki glasujejo o sklepih stavbe, upravnik pa objavlja obvestila in okvare dodeljuje serviserjem. Tako komunikacija v bloku ne poteka več na papirju, po telefonu in v WhatsApp skupinah, ampak na enem mestu.

Uporabniške vloge: etažni lastnik, najemnik, predstavnik lastnikov, upravnik in serviser.

## Tehnologije

- **Frontend:** React, Vite, Tailwind CSS
- **Backend:** Python, FastAPI
- **Podatkovna baza:** PostgreSQL, SQLAlchemy, Alembic
- **Avtentikacija:** JWT, bcrypt
- **E-pošta:** fastapi-mail, Mailpit (razvoj), Brevo
- **Lokalni razvoj:** Docker, Git in GitHub

## Struktura projekta

```
├── frontend/   React aplikacija
├── backend/    FastAPI strežnik
└── docs/       dokumentacija projekta
```

## Dokumentacija

- [Zasnova rešitve](docs/01-zasnova-resitve.md)
- [Funkcionalnosti in obseg](docs/02-funkcionalnosti-in-obseg.md)
- [Podatkovni model](docs/03-podatkovni-model.md)
- [Arhitektura in tehnološki sklad](docs/04-arhitektura-in-tehnoloski-sklad.md)
- [Uporabniške zgodbe](docs/05-uporabniske-zgodbe.md)
- [Wireframi](docs/06-wireframes.md)
- [Arhitekturne odločitve (ADR)](docs/adr/)
