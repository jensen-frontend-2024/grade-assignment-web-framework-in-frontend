# Inlämningsuppgift: Forum för diskussionstrådar

## "Forum för diskussionstrådar – Din fullstack-resa börjar här"

<details open>
  <summary>Innehåll</summary>

- [Bakgrund och Uppdragsbeskrivning](#bakgrund--uppdragsbeskrivning)
- [Krav på Tekniker](#krav-på-tekniker)
- [Kravspec - / Funktionalitet](#kravspecifikation)
- [Kravspec - Kodkvalitet](#kodkvalitet)
- [Bedömning](#bedömning)
- [Inlämning](#inlämning)
- [Tips](#)

</details>

### **Bakgrund – Uppdragsbeskrivning**

Du har fått i uppdrag av ett nytt startup att bygga en webbapplikation för ett forum där användare kan dela idéer och diskutera olika ämnen. Applikationen ska vara enkel och användarvänlig, med funktionalitet som möjliggör skapande av diskussionstrådar och svar.

Företaget ser detta som en grundplattform och behöver följande funktioner:

- Diskussionstrådar visas i en lista och kan öppnas för att se detaljer.
- Användare kan skapa nya trådar och svara på befintliga.

Din uppgift är att bygga denna applikation och säkerställa att den fungerar som en stabil grund för vidare utveckling.

[Tillbaks till toppen](#inlämningsuppgift-forum-för-diskussionstrådar)

---

### **Krav på tekniker**

- **Frontend**: React, React Router, Context API.
- **Backend**: Express.js
- **Databas**: SQLite
- **Integrering**: Better-sqlite3.

[Tillbaks till toppen](#inlämningsuppgift-forum-för-diskussionstrådar)

---

### Kravspecifikation

**_G-Krav_**

- Sida som visar en lista över alla diskussionstrådar.
- Möjlighet att klicka på en diskussionstråd och komma till dess egna sida, för att se dess innehåll och svar.
- En sida med funktionalitet för att skapa nya diskussionstrådar med titel och innehåll.
- Möjlighet att svara på en befintlig diskussionstråd.
- Implementera Routing för att navigera mellan sidor.
- Implementera Context API om det finns behov för "global hantering" av state.
- **All** data ska sparas i databasen

**_VG-Krav_**

- Möjlighet att sortera trådar efter senaste aktivitet eller antal svar.
- Funktionalitet för att redigera och ta bort trådar och svar.
- Möjlighet att filtrera trådar efter specifika kategorier och sökord.

[Tillbaks till toppen](#inlämningsuppgift-forum-för-diskussionstrådar)

---

### Kodkvalitet

**_G-Krav_**

- Koden i både backend och frontend ska vara läsbar och strukturerad, utan onödig komplexitet.
- Funktioner ska hållas inom 20–30 _(Ungefär, kan vara längre om det finns anledning för det)_ rader och följa **Single Responsibility Principle**.
- Försöka att undvika att applikationen krashar.
- Prettier eller ESLint ska användas för korrekt formaterad kod.
- Om ni anser att kommentarer behövs för att förklara kod är det okej, men annars krävs tydliga variabel-, funktions- och komponentnamn.
- I README-filen ska följande finnas:

  - Installationsinstruktioner
  - Startkommandon för backend/frontend
  - Kort beskrivning av projektet
  - Övrig information

**_VG-Krav_**

- Koden i både backend och fronted ska vara välstrukturerad, med tydlig separation av ansvar mellan funktioner, komponenter och filer.
- Komponenter i Frontend bör vara överskådliga och lätta att förstå, ej heller för långa, 100-120 rader bör vara max-gränsen.
- Felhantering ska vara mer omfattande i både backend och fronten och täcka flera typer av möjliga fel, path- och query-parametrar, body-validering, API-anropen i Frontend och användarinmatning i olika inputfält.

[Tillbaks till toppen](#inlämningsuppgift-forum-för-diskussionstrådar)

---

### Bedömning

- **Godkänt (G)**: Uppfyller samtliga G-krav i funktionalitet och kodkvalitet.
- **Väl Godkänt (VG)**: Uppfyller samtliga(?) VG-krav plus samtliga G-krav.

_När det kommer till VG-bedömningen så är den mer öppen och flytande. Man kan få VG utan att uppfylla alla VG-kraven men då ska det finnas god grund för det. Att fylla alla VG-kraven är dock det "enklaste" sättet för att uppnå VG._

[Tillbaks till toppen](#inlämningsuppgift-forum-för-diskussionstrådar)

---

### Inlämning

Deadline: **Tisdagen den 18 Mars 23:59**.

Inlämning sker på ert githubkonto där jag vill **_ett_** repo med både backend och frontend inkluderat - en mapp för backend och en för frontend. Databasfilen kan antingen ligga i repot eller i backendmappen. Ert repo ska även ha en tydligt struktur, till exempel kan denna struktur vara lämplig:

```bash
project-root/
├── backend/
│   ├── package.json        # Backendens beroenden och skript
│   ├── server.js           # Backendens startfil
│   ├── routes/             # API-routes
│   ├── controllers/        # Logik för API-routes
│   ├── types/              # Typer och interfaces (OM ni använder Typescript, valfritt.)
│   ├── middlewares/        # Middleware för autentisering och validering
│   └── utils/              # Utilities
├── frontend/
│   ├── package.json        # Frontendens beroenden och skript
│   ├── vite.config.js      # Vite-konfiguration
│   ├── src/
│   │   ├── main.jsx        # Frontendens startfil
│   │   ├── components/     # React-komponenter, vanliga och återanvändbara
│   │   ├── pages/          # Sidor i applikationen, komponenter som har en route
│   │   ├── context/        # Context API-hantering
│   │   ├── hooks/          # Custom hooks (överkurs, försök om ni vill)
│   │   ├── styles/         # Globala och komponentbaserade css-filer, valfritt, går bra som vi har gjort tidigare. CSS-filen bredvid sin komponent.
│   │   └── assets/         # Bilder
├── database.db             # SQLite-databas
├── README.md               # Instruktioner för att starta applikationen
└── .gitignore              # Filer att ignorera i GitHub
```

Ni får skapa er egen struktur, men allt ska finnas i ett repo och vara tydligt organiserat. Dokumentera era val i README.md.

[Tillbaks till toppen](#inlämningsuppgift-forum-för-diskussionstrådar)

### Tips

Nedan har ni lite tips på hur ni kan komma igång med er uppgift. Jag rekommenderar att sitta ner och "grubbla" lite innan ni kastar er in i kodandet. **Allt här nedan är valfritt givetvis!**

1. Skapa ett ER-Diagram för er Databsstruktur.
2. Sätt upp er databas utifrån ER-Diagrammet.
3. Skapa en Figma för att få en idé om hur er applikation ska se ut.
4. Börja skriva er backend. Tänk igenom vilken data ni kommer att behöva, och vilken data som kan behövas att skapas och ändras under applikationens gång och skapa de nödvändigar endpoints för det. Ha även felhantering i åtanke hela tiden. Försök att förutse de olika felen som kan uppstå och hantera de därefter. Testa era endpoints i postman.
5. Bygg er Frontend och skapa de olika vyerna/sidorna som er applikation kräver.