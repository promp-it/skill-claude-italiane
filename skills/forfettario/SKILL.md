---
name: forfettario
description: Stima tasse e contributi di una partita IVA in regime forfettario italiano e spiega le regole (coefficiente di redditività per codice ATECO, imposta sostitutiva, contributi INPS gestione separata o artigiani/commercianti, acconti e saldo, soglie di ricavi e cause di esclusione). Usala quando l'utente chiede "quanto pago di tasse col forfettario", "conviene il forfettario", "quanto mi resta netto", "quando si pagano acconti", "posso restare nel forfettario se supero", oppure confronta forfettario e ordinario.
---

# Regime forfettario: stime e spiegazioni

Fai stime chiare, non consulenza fiscale. Ogni numero normativo lo verifichi prima di usarlo.

## Regola d'oro
**Non usare mai a memoria soglie, aliquote o coefficienti.** Prima del calcolo cerca e cita la fonte aggiornata:
- soglia ricavi e cause di esclusione → `agenziaentrate.gov.it` (scheda regime forfetario);
- coefficienti di redditività per gruppo ATECO → allegato alla legge istitutiva, riportato dall'Agenzia;
- aliquote e minimali contributivi dell'anno → circolari INPS dell'anno in corso.
Riporta in testa al calcolo: "Parametri verificati il <data> su <fonte>". Se non riesci a verificare, fermati e dillo.

## Dati da chiedere
1. Codice ATECO (o descrizione dell'attività, e tu proponi il codice da confermare).
2. Ricavi/compensi incassati nell'anno (il forfettario segue il principio di cassa).
3. Anno di apertura (per l'aliquota agevolata delle nuove attività, se ne ha diritto: verifica i requisiti).
4. Cassa previdenziale: gestione separata INPS, artigiani/commercianti, o cassa professionale.
5. Contributi già versati nell'anno (sono deducibili dal reddito).

## Calcolo (mostralo passo per passo)
1. Reddito lordo = ricavi × coefficiente di redditività.
2. Reddito imponibile = reddito lordo − contributi previdenziali versati nell'anno.
3. Imposta sostitutiva = imponibile × aliquota (agevolata o ordinaria).
4. Contributi: gestione separata in percentuale sul reddito lordo; artigiani/commercianti = fissi sul minimale + percentuale sull'eccedenza (segnala la riduzione opzionale prevista per i forfettari, se ancora in vigore).
5. Netto stimato = ricavi − imposta − contributi.
Usa uno script (Python o calcolo in tabella) per i conti, non il calcolo a mente.

## Scadenze
Spiega il meccanismo saldo + primo acconto (giugno) e secondo acconto (novembre), con il metodo storico, ma le date esatte dell'anno le verifichi sul calendario fiscale dell'Agenzia.

## Output
Tabella: voce → importo → fonte. Poi 3 righe: quanto accantonare al mese, la prossima scadenza, cosa chiedere al commercialista.

## Mai
- Promettere che una scelta "conviene" senza confrontare anche il regime ordinario con dati reali.
- Dimenticare di dire che la stima non tiene conto di situazioni personali (altri redditi, detrazioni, crediti).
