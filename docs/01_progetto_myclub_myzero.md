# myClub (myZero) — Documento Progetto Completo

## 1) Visione del prodotto

**myClub (myZero)** è una piattaforma mobile per locali/eventi che unisce in un unico ecosistema:

- vendita ticket,
- vendita consumazioni,
- controllo accessi e redemption QR,
- verifica età,
- ruoli operativi,
- loyalty/fidelity,
- notifiche push,
- wallet pass (Apple/Google, dove abilitato),
- dashboard amministrativa multi-ruolo.

L’obiettivo è **aumentare conversione, controllo operativo e retention** riducendo attività manuali e sprechi.

---

## 2) Problemi che risolve

### Per il locale/organizzatore

- Elimina fogli/elenchi manuali all’ingresso e al bar.
- Riduce errori di cassa e incongruenze su omaggi/premi.
- Centralizza vendite, scansioni, rimborsi, notifiche e gestione ruoli.
- Consente campagne push e gestione contenuti in autonomia.
- Aumenta tracciabilità e audit trail (chi ha fatto cosa e quando).

### Per l’utente finale

- Acquisto rapido ticket/drink da app.
- QR sempre disponibili e pronti all’uso.
- Notifiche sullo stato degli ordini/verifiche.
- Esperienza fedeltà gamificata (punti, livelli, premi, wheel quando attiva).
- Profilo unico con storico e documenti/consensi.

---

## 3) Funzionalità chiave lato utente

## Home ed eventi

- Listing eventi con card visuale e CTA acquisto.
- Dettaglio evento con informazioni estese (descrizione, artisti, pricing uomo/donna, policy acquisto).
- Carosello gestito da backoffice (titolo, descrizione, immagine, link).

## Ticket

- Regola business: **1 ticket per evento per utente**.
- Stato ticket (da usare/usato/scaduto).
- QR pronto all’uso.
- Rimborso con motivazione e regole temporali (fino a 2 ore prima dell’inizio evento).

## Drink

- Acquisto multiprodotto e multiquantità.
- Generazione token QR per unità (1 prodotto = 1 QR).
- Stato utilizzo (da usare/usato).

## Verifica età

- Flusso documentale con invio documento.
- Revisione da ruoli autorizzati.
- In caso di rifiuto: modalità limitata (app consultativa).

## Fidelity / gamification

- Accumulo punti su acquisti validi.
- Livelli e progressione.
- Premi disponibili in base alle regole attive.
- Ruota della fortuna quando abilitata dagli admin.

## Notifiche

- Centro notifiche in app con dettaglio.
- Eventi push principali:
  - richiesta verifica età,
  - esito verifica,
  - passaggio livello,
  - pagamento riuscito/fallito,
  - comunicazioni marketing (su consenso).

## Profilo

- Dati anagrafici.
- Gestione avatar.
- Sezioni dedicate a punti/stato/fatture (a seconda della configurazione front-end).

---

## 4) Ruoli e permessi

Il sistema è role-based con separazione operativa:

- `super_admin`
- `marketing_comms`
- `analyst`
- `entry_operator`
- `bar_operator`

## Super Admin

- Governance completa piattaforma.
- Assegna ruoli agli utenti.
- Gestisce eventi, drink, carosello, loyalty, wheel, push, verifiche età.

## Marketing & Comunicazione

- Dashboard marketing.
- Push notification targettizzate.
- Gestione contenuti (eventi, carosello).
- Supporto fidelity.

## Analyst

- Accesso focalizzato alla revisione verifica età.

## Operatore Ingresso

- Interfaccia semplificata con scanner QR.
- Verifica validità ticket/omaggi ingresso.
- Vista ingressi registrati e possibilità di annullamento scansione.

## Operatore Bar

- Interfaccia semplificata con scanner QR.
- Redemption drink/omaggi drink.
- Vista ordini/redeem recenti e annullamento scansione.

---

## 5) Pannello Admin

Copre i domini principali:

- gestione utenti/ruoli,
- gestione eventi,
- gestione drink,
- gestione carosello,
- gestione push,
- gestione fidelity,
- revisione età,
- gestione wheel (enable/disable, segmenti, probabilità, cap premi).

Punti forti:

- controllo centralizzato,
- operatività in tempo reale,
- riduzione dipendenze tecniche per attività quotidiane.

---

## 6) Sicurezza, compliance e controllo abuso

- Autenticazione Firebase.
- Regole Firestore/Storage con accesso per ruolo/owner.
- Funzioni server-side per validazioni critiche (pagamento, uso ticket/drink, rimborsi, scansioni).
- Tracciabilità azioni via documenti di stato e timestamp.
- Separazione canali operativi (utente, ingresso, bar, admin).

Ambiti da mantenere sempre governati:

- policy privacy/cookie/marketing consent,
- retention documenti verifica età,
- hardening continuo regole e callable.

---

## 7) Perché conviene adottarla

## 1. Più ricavi

- Checkout rapido.
- Push mirate e campagne frequenti.
- Loyalty e premi che aumentano ritorno cliente.

## 2. Meno costi operativi

- Meno gestione manuale ingressi/consumazioni.
- Meno errori su omaggi, ticket e ordini.
- Meno supporto interno su “chi ha pagato/cosa è stato usato”.

## 3. Più controllo manageriale

- Dati centralizzati e ruoli separati.
- Governance su contenuti, promozioni, flussi operativi.

## 4. Migliore esperienza cliente

- Esperienza mobile uniforme, veloce e moderna.
- Informazioni e asset (QR/notifiche/stato) sempre disponibili.

---

## 8) KPI consigliati da monitorare

- Tasso conversione evento (view → checkout → paid).
- Ticket sold-out rate per evento.
- Consumo medio drink per utente/evento.
- Redemption premi e impatto su ritorno in venue.
- % pagamenti falliti e recovery rate.
- Tempo medio verifica età (richiesta → esito).
- Ticket/drink fraud prevention rate (scan invalidi bloccati).
- Retention 7/30/60 giorni.

---

## 9) Conclusione

myClub (myZero) non è solo un’app di ticketing: è una **piattaforma operativa completa** per il locale. Unisce vendita, controllo, marketing e fidelizzazione in un sistema unico, scalabile e misurabile.

Il vantaggio competitivo principale è la combinazione tra:

- esperienza utente forte,
- automazione operativa,
- controllo business in tempo reale.

