# Luca Codeluppi · sito personale

Sito personale e portfolio di **Luca Codeluppi**, ingegnere gestionale di Brescia che unisce operations, analisi dei dati e growth marketing.

**Sito online:** https://lucacodeluppi06.github.io/

Progetto realizzato per il corso HTML e CSS del master in Growth Marketing e agenti AI di start2impact University.

## Pagine

| Pagina | Contenuto |
| --- | --- |
| `index.html` | Home: presentazione, numeri chiave, per chi lavoro, chi sono, competenze, progetti in evidenza |
| `cv.html` | Curriculum vitae in HTML, con versione PDF generata dalla stessa pagina (stili di stampa) |
| `progetti.html` | Portfolio con 10 progetti e filtri per categoria realizzati solo in CSS |
| `contatti.html` | Modulo di contatto con campi `required` e validazione visiva in CSS |
| `grazie.html` | Conferma dopo l'invio del modulo |
| `404.html` | Pagina di errore personalizzata (GitHub Pages la usa in automatico) |
| `progetti/depyl/` | Landing page Depyl, il mio primo progetto HTML e CSS |

## Tecnologie

- **HTML5** semantico (landmark, `aria-*`, gerarchia dei titoli, testi alternativi)
- **Bootstrap 5.3**: griglia, navbar, card, form floating label, utility
- **Sass (SCSS)** con architettura a cartelle, variabili, mappe, mixin, funzioni e cicli
- **Flexbox e CSS Grid** per tutti i layout
- **Zero JavaScript**: menu mobile, filtri dei progetti, contatore, animazioni allo scroll e validazione del form sono solo CSS

## Requisiti del progetto

- [x] Almeno due pagine, tra cui il **CV in HTML** e la pagina **Contattami con form**
- [x] Framework front-end: **Bootstrap 5.3**
- [x] **Favicon** (SVG con tema scuro, PNG, ICO, icona Apple)
- [x] **Menu sticky** su tutte le dimensioni di schermo, con hamburger su mobile
- [x] Layout con **Flexbox** e **Grid**
- [x] CSS scritto in **Sass**
- [x] Tag **Open Graph** e Twitter Card su ogni pagina
- [x] Attributi `required` nel form
- [x] Sito **100% responsive** (da 320px a schermi grandi), con tema chiaro e scuro automatico
- [x] Pubblicato con **GitHub Pages**

## Struttura

```
├── index.html, cv.html, progetti.html, contatti.html, grazie.html, 404.html
├── css/
│   ├── style.css            ← CSS compilato da Sass (non modificare a mano)
│   └── vendor/bootstrap.min.css
├── scss/
│   ├── main.scss            ← punto di ingresso
│   ├── abstracts/           ← variabili, funzioni, mixin
│   ├── base/                ← font, tema, tipografia, utility, stampa
│   ├── layout/              ← header, footer
│   ├── components/          ← bottoni, card, chip, timeline, form, marquee
│   └── pages/               ← home, cv, progetti, contatti
├── assets/
│   ├── fonts/               ← Fraunces, Geist, Geist Mono (ospitati in locale)
│   ├── img/                 ← foto, copertine dei progetti, immagine Open Graph
│   ├── icons/               ← favicon e icone dell'app
│   └── docs/                ← PDF dei progetti e del CV
├── progetti/depyl/          ← landing page Depyl
├── favicon.ico, site.webmanifest, robots.txt, sitemap.xml
└── package.json             ← script per compilare Sass
```

## Compilare Sass

Serve [Node.js](https://nodejs.org/). Dalla cartella del progetto:

```bash
npm install      # installa Sass (una volta sola)
npm run build    # compila scss/main.scss in css/style.css
npm run watch    # ricompila a ogni salvataggio
```

In alternativa si può usare l'estensione **Live Sass Compiler** di VS Code puntando l'output su `css/style.css`.

## Modulo di contatto

Il form usa [FormSubmit](https://formsubmit.co/), che inoltra i messaggi via email senza JavaScript e senza server.

1. Alla prima compilazione del modulo dal sito online, FormSubmit invia una mail di attivazione: va confermata.
2. Nella mail di conferma c'è un indirizzo alternativo (una stringa casuale). Va sostituito all'email nell'attributo `action` del form in `contatti.html`, così l'indirizzo non è più leggibile dai bot.

## Pubblicazione

Il repository si chiama `lucacodeluppi06.github.io`: GitHub Pages pubblica il sito su `https://lucacodeluppi06.github.io/` dal branch `main`.

---

© 2026 Luca Codeluppi
