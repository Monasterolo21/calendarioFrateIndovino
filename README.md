# Esercitazione "Calendario di Frate Indovino"

### Consegna:

Clona il repository al commit "esercizio studenti" e completa il codice sorgente fornito per creare un'applicazione Vue.js che simula la scelta dell'outfit giusto in base alle condizioni meteorologiche giornaliere.
N.B. Non è necessario modificare funzioni già implementate. Ti basta seguire i TODO all'interno del codice, se rimani bloccato puoi consultare la soluzione al commit successivo o in questo README.

### Obiettivo:

Questa esercitazione è dedicata a studenti di terza e quarta superiore con lo scopo di insegnare le basi della programmazione ad eventi utilizzando il framework Vue.js. L’esercizio proposto consente di mettere in pratica tale concetto attraverso la creazione di una piccola web application che simula la scelta dell’outfit giusto in base alle condizioni meteorologiche giornaliere.

### Introduzione a Vue.js:

Vue.js è un framework progressivo per la costruzione di interfacce utente. Contrariamente ad altri monolitici framework, Vue è progettato da zero per essere adottabile in modo incrementale. La libreria si concentra solo sulla view layer (parte visiva), ed è facile da imparare e integrare con altre librerie o progetti esistenti. D'altra parte, Vue è perfettamente capace di potenziare sofisticate Single-Page Applications quando utilizzato in combinazione con strumenti moderni e librerie di supporto. Per ora comunque ti basta sapere che puoi fare dei siti interattivi con Vue.js.

### Struttura dell’Applicazione:

Il codice sorgente fornito definisce una semplice applicazione Vue.js. L'applicazione tiene traccia del `punteggio` dell'utente, del `giorno` corrente e delle `condizioniMetereologiche`. La logica dell’app permette di simulare il cambiamento del meteo e la scelta dell’outfit appropriato per quel meteo. Alla scelta giusta segue un incremento di punteggio.

### I tuoi compiti:

Per completare quest'esercitazione, dovrai implementare alcune funzioni tramite la programmazione di event handler che risponderanno a determinate azioni (click su button).

#### 1. Implementa la funzione `maglioncino`:

Quando l'utente clicca sul bottone con il maglioncino, dovrai verificare che l'outfit scelto sia appropriato per il meteo attuale.

```javascript
maglioncino: function () {
  var self = this;
  self.controllaOutfit("🧥");
},
```

#### 2. Implementa la funzione `ombrello`:

Stessa logica della funzione `maglioncino`, ma in questo caso, verifichiamo se ci vuole l'ombrello.

```javascript
ombrello: function () {
  var self = this;
  self.controllaOutfit("☂️");
},
```

#### 3. Completa la funzione `controllaOutfit`:

Questa funzione deve aggiornare il punteggio e il giorno, e generare le nuove condizioni metereologiche.

```javascript
controllaOutfit: function (outfit) {
  var self = this;
  if (
    (self.meteoDiOggi == "☀️" && outfit == "😎") ||
    (self.meteoDiOggi == "☁️" && outfit == "🧥") ||
    (self.meteoDiOggi == "🌧️" && outfit == "☂️")
  ) {
    self.punteggio += 1;
    alert("Hai indovinato l'outfit!");
  } else {
    alert("Hai sbagliato outfit!");
  }
  self.giorno += 1;
  self.nuovoMeteo();
},
```

### Esecuzione:

Ogni volta che gli utenti dell'applicazione cliccano su uno dei bottoni per scegliere l'outfit (`occhiali`, `maglioncino` o `ombrello`), le funzioni corrispondenti saranno eseguite. Queste funzioni utilizzeranno la programmazione ad eventi per gestire la logica della app.

### Conclusione:

Al termine di questa esercitazione avrai compreso come gestire la logica di un'applicazione usando la programmazione ad eventi con Vue.js.

Continua a sperimentare con la tua applicazione e prova a implementare nuove funzionalità!
