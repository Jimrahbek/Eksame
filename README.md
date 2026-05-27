# Teknisk dokumentation for 2.semester eksamen sommer 2026 (grp.4)

Denne case er lavet på baggrund af 2.semester eksamen. Til denne case har vi fået til opgave at lave en hjemmeside for psykologen Anne Louise Hjort, som for nyligt etableret sig som en privat praktiserende psykolog, med base på Nørreport og hendes privathjem i Dragør.
Vi har tænkt os at opsætte projektet i astro og lave siden dynamisk via. Supabase, så i denne dokumentation vil vi vise hvordan vi tænkt os at sætte vores projekt op og gennemgår hvordan fordeler vores arbejde.

## Links

- GitHub repository: [https://www.figma.com/design/JTCLmNz77TwwVXmraNdjVL/2.-semester-eksamen?node-id=50-4&p=f&t=Z5eOnUXyIoJDaSSj-0]
- GitHub Pages: []
- Figma: [https://www.figma.com/design/JTCLmNz77TwwVXmraNdjVL/2.-semester-eksamen?node-id=50-4&t=DPLhIzECSXqwCH8g-1]

## Projektstruktur

```
/
├── public/
    └──billeder/
├── src/
    └── assets/
    └── components/
        └── forside-adresser.astro
        └── forside-erfaring.astro
        └── forside-hero.astro
        └── forside-priser.astro
        └── forside-adresser.astro
        └── om_mig-components.astro
        └── ydelser_details.astro
        └── ydelser-book.astro
        └── ydelser-cards.astro
        └── ydelser-info.astro
    └── layout/
        └── layout.astro
    └── pages/
            ydelser
                [slug].astro
        └── booking.astro
        └── index.astro
        └── om-mig.astro
        └── ydelser_details.astro
        └── ydelser.astro
└── .env
└── .gitignore
└── astro.config.mjs
└── package-lock.json
└── package.json
└── README.md
└── tsconfig.json

```

Astro søger efter `.astro`- eller `.md`-filer i `src/pages/`-mappen. Hver side vises som en rute baseret på dens filnavn.

`src/components/` er der, vi placerer alle Astro komponenter.

Alle billeder placeres i `assets/`-mappen, bortset fra favikon som placeres i public.

## Navngivning:

For at sikre en ensartet struktur og for at undgå forvirring vil vi følge disse regler:

- **Små bogstaver** - Alle mapper og filer navngives med små bogstaver
- **Ingen mellemrum** - Vi undgår mellemrum i filnavne, da det kan skabe problemer i kodning.
- **Bindestreg** - Vi bruger bindestreg til at adskille ord som f.eks. om_mig.

## Git branches:

Vi aftaler hvem der arbejder på hvilke components og pusher kun ting ind i main når vi sidder sammen eller når vi har sagt det i vores fælles skrive kannel. Branches bliver navngivet efter hvad der bliver lavet i dem for at skabe et bedre overskud.

## Arbejdsflow:

For at arbejde effektivt i gruppen og undgå konflikter i koden følger vi nogle fælles regler for vores arbejdsproces.

**Fordeling af arbejde**

Vi fordeler arbejdet ved at give hvert gruppemedlem ansvar for bestemte sider/komponenter på hjemmesiden. På den måde arbejder vi som regel i forskellige filer og undgår, at flere redigerer i de samme filer på samme tid. Hvis to personer skal arbejde på samme funktion, aftaler vi det først i gruppen, så der ikke skabes konflikter i branches.

**Commit-beskeder**

For at sikre tydelige commit-beskeder skriver vi korte og præcise beskrivelser af, hvad der er blevet ændret. En commit-besked skal fx forklare hvilken fil eller funktion der er blevet ændret.

**Kommunikation om ændringer i main**

Når en feature branch bliver merged til **main**, informerer vi resten af gruppen via vores fælles kommunikationskanal som enten er Messenger, Teams eller når vi mødes på skolen. På den måde ved alle, at der er kommet nye ændringer, og de kan opdatere deres lokale version af projektet, før de fortsætter arbejdet.

## env fil

En env fil bruges i dette dokument til at indlæse dataen fra supabase.

Eksempel:

SUPABASE_URL

SUPABASE_PUBLISHABLE_KEY

## Kode:

**Håndtering af data**

En vigtig del af vores kode er arbejdet med data. Vi har lavet vores egen database i supabase. Denne database har vi derefter hentet data fra som bruges til ydelser siderne. Dette gør det simpelt at lave mange ensartet sider uden at skulle skrive den samme kode igen og igen.

**Css selectors**

Vi har valgt at bruge classes som selectors både i HTML og JavaScript. Det giver en fleksibel løsning, hvor flere elementer kan dele samme styling og funktionalitet.

**Kommentarer i koden**

Kommentarer i koden er brugt der, hvor det passer bedst for eksempel ved fetch-kald, funktioner og mere komplekse dele af CSS som layout eller responsive regler. Vi har valgt at ikke kommentere helt åbenlyse koder, så koden stadig fremstår ren og overskuelig, men samtidig nem at forstå for andre.

Her er et eksempel på hvordan kommentarer i koden hjælper med at skabe overblik ved at forklarer kort hvad koden handler om.

## Commands

Alle kommandoer køres fra fra en terminal:

| Command         | Action                               |
| :-------------- | :----------------------------------- |
| `npm install`   | Installerer afhængigheder            |
| `npm run dev`   | Starter lokal udviklerserver         |
| `npm run build` | Byg dit produktionssted til`./dist/` |

### api

for at få vores data har vi hentet det fra vores egen database. Dette er gjort via denne kode

```

```
