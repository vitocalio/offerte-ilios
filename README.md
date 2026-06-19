# Generatore Offerte Tecnico-Commerciali — ILIOS S.r.l.

App web in un unico file (`index.html`) per redigere offerte tecnico-commerciali nello stile ILIOS ed esportarle in **PDF pronto da inviare**. Nessun server, nessuna installazione: gira interamente nel browser, quindi è perfetta per **GitHub Pages**.

## Cosa fa

- Modulo a sinistra (dati offerta, cliente, revisione) e **anteprima A4 live** a destra.
- **Catalogo servizi** con 5 sezioni predefinite (A pre-fattibilità, B progettazione definitiva, C attività prodromiche, D piano tecnico opere, E assistenza iter autorizzativo): spunti quelle che servono e inserisci gli onorari. Le attività e le note IVA vengono inserite automaticamente.
- Calcolo del **totale offerta** (netto IVA).
- Testi standard precompilati e modificabili: lettera di presentazione, modalità di pagamento, esclusioni, validità (30 gg), tempi di consegna (45 gg), firma digitale.
- **Salva bozza** nel browser, **Esporta/Importa** i dati in JSON per riprendere un'offerta su un altro PC.
- **Genera PDF**: apre la stampa del browser → scegli *Salva come PDF* (formato A4, due pagine: copertina + contenuto).

## Come usarla in locale
Apri `index.html` con un doppio clic. Funziona offline.

## Pubblicazione su GitHub Pages

1. Crea un nuovo repository su GitHub (es. `offerte-ilios`).
2. Carica il file `index.html` nella **root** del repository (puoi trascinarlo nella pagina "Add file → Upload files", poi *Commit*).
3. Vai su **Settings → Pages**.
4. In *Build and deployment* → *Source*: scegli **Deploy from a branch**.
5. *Branch*: seleziona `main` e cartella `/ (root)`, poi **Save**.
6. Dopo circa un minuto l'app sarà online all'indirizzo:
   `https://<tuo-utente>.github.io/offerte-ilios/`

Per aggiornarla in futuro, basta ricaricare un nuovo `index.html` con un commit: GitHub Pages si aggiorna da solo.

## Personalizzazione rapida

Tutto è dentro `index.html`:

- **Dati ILIOS** (indirizzi, contatti, P.IVA): oggetto `FORNITORE` all'inizio dello `<script>`.
- **Catalogo servizi** (titoli, descrizioni, elenco attività): array `CATALOGO`.
- **Testi standard** (pagamenti, esclusioni, validità): le costanti `DEFAULT_*`.
- **Colori/logo**: variabili CSS `--brand` in cima al file e il badge "IL".

## Note
- Il PDF è generato dalla funzione di stampa del browser (consigliato Chrome/Edge): imposta *Margini → Predefiniti* e *Grafica di sfondo → attiva* per riprodurre i colori delle intestazioni.
- I dati restano sul tuo dispositivo; nulla viene inviato online.
