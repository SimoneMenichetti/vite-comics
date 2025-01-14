Un'applicazione per la visualizzazione di fumetti, dove gli utenti possono navigare tra diverse serie e tipi di fumetti. Ogni fumetto è rappresentato da una card con un'immagine di copertura, il prezzo, e il tipo di fumetto.

Funzionalità
Visualizzazione delle card: Ogni card rappresenta un fumetto e contiene:
Un'immagine di copertura.
Il prezzo del fumetto.
La serie a cui appartiene.
Il tipo di fumetto (ad esempio, "comic book" o "graphic novel").
Layout responsive: Le card dei fumetti sono presentate in una griglia che si adatta a dispositivi di diverse dimensioni (desktop, tablet, smartphone).
Tecnologie utilizzate
Vue.js: Il framework JavaScript per costruire l'applicativo.
SCSS: Per la gestione degli stili e la creazione di un design responsive.
Componente personalizzato: AppCard per rappresentare ogni singolo fumetto.
Struttura del progetto
Il progetto è strutturato come segue:

bash
Copia codice
/comic-book-app
/assets
/styles - general.scss # Stili generali per l'app - variables.scss # Variabili SCSS per il tema
/common - AppCard.vue # Componente per ogni card del fumetto

- AppMain.vue # Componente principale, gestisce le card
- main.js # File di ingresso Vue.js
- index.html # HTML di base
- README.md # Questo file
  Come avviare il progetto

1. Clona il repository
   Clona il repository sul tuo computer:

bash
Copia codice
git clone https://github.com/tuo-username/comic-book-app.git 2. Installa le dipendenze
Naviga nella cartella del progetto e installa le dipendenze tramite npm:

bash
Copia codice
cd comic-book-app
npm install 3. Avvia l'applicazione
Una volta installate le dipendenze, avvia l'applicazione in modalità di sviluppo:

bash
Copia codice
npm run serve
L'applicazione sarà disponibile su http://localhost:8080.

Struttura del componente principale (AppMain.vue)
Il componente principale AppMain.vue gestisce l'elenco delle card dei fumetti e visualizza il layout delle card. Include il componente AppCard per ogni fumetto.

Dati dei fumetti
Il componente AppMain.vue contiene un array di oggetti cards che rappresentano i fumetti. Ogni oggetto ha le seguenti proprietà:

thumb: URL dell'immagine di copertura del fumetto.
price: Prezzo del fumetto.
series: Nome della serie del fumetto.
type: Tipo di fumetto (ad esempio, "comic book" o "graphic novel").
Layout e Design
L'applicazione è responsive e si adatta a schermi di diverse dimensioni:

Desktop: Le card vengono visualizzate in una griglia orizzontale.
Tablet: Le card sono disposte in una griglia a due colonne.
Smartphone: Le card sono visualizzate una per volta, in una colonna singola.
Responsive Design
Usato flex e grid per adattare il layout a diverse dimensioni di schermo.
I bottoni sono stilizzati per essere facilmente cliccabili su dispositivi mobili.
