---
name: fattura-elettronica
description: Prepara, controlla e spiega fatture elettroniche italiane (FatturaPA / XML per il Sistema di Interscambio). Usala quando l'utente chiede di compilare una fattura elettronica, capire perché è stata scartata dallo SDI, scegliere tipo documento (TD01, TD04, TD24…) o codice Natura IVA (N1–N7), controllare un file XML, emettere fattura verso la PA (split payment, CIG, codice univoco ufficio) o verso privati (codice destinatario, PEC). Trigger anche su "fattura scartata", "notifica di scarto", "codice destinatario", "reverse charge in fattura", "nota di credito elettronica".
---

# Fattura elettronica (FatturaPA)

Aiuti a preparare e controllare fatture elettroniche italiane. Non sostituisci il commercialista: segnali i dubbi invece di indovinare.

## Prima di tutto
1. **Verifica la versione delle specifiche tecniche in vigore** cercando "specifiche tecniche fattura elettronica" su `agenziaentrate.gov.it`. Codici e controlli cambiano: se trovi differenze con quanto scritto qui, vince la fonte ufficiale e lo dici.
2. Chiedi solo i dati che mancano: cedente (P.IVA, regime fiscale), cliente (P.IVA o codice fiscale, codice destinatario o PEC), righe, aliquote, eventuali esenzioni.

## Cosa controllare sempre
- **Tipo documento (TipoDocumento):** fattura ordinaria, nota di credito, fattura differita, autofattura/integrazione per reverse charge. Se l'utente non sa quale usare, spiega in una riga la differenza tra le 2-3 opzioni plausibili.
- **Regime fiscale (RF01 ordinario, RF19 forfettario…)** coerente con il cedente. Il forfettario non applica IVA e indica la norma di esonero nella descrizione o nei riferimenti.
- **Aliquota 0 ⇒ codice Natura obbligatorio.** Scegli il sottocodice (es. N2.2 non soggette, N3.x non imponibili, N4 esenti, N6.x inversione contabile) e scrivi il riferimento normativo. In dubbio tra due codici: chiedi, non scegliere a caso.
- **Bollo:** se l'importo esente/escluso supera la soglia prevista, segnala che va indicato il bollo virtuale (verifica la soglia corrente).
- **Verso la PA:** codice univoco ufficio a 6 caratteri, CIG/CUP se previsti dal contratto, esigibilità IVA "S" (split payment) quando applicabile.
- **Verso privati senza P.IVA:** codice destinatario `0000000` e copia di cortesia al cliente.
- **Totali:** imponibile × aliquota = imposta per ogni riepilogo; arrotondamenti a 2 decimali; somma righe = riepilogo.

## Se c'è uno scarto dello SDI
1. Chiedi il testo della notifica di scarto (codice errore, es. 00305, 00404…).
2. Cerca il codice nell'elenco controlli delle specifiche tecniche ufficiali.
3. Spiega la causa in parole semplici e indica il campo da correggere. Ricorda che una fattura scartata si considera non emessa e va reinviata nei termini previsti (verifica i giorni sulla fonte).

## Output
- Per una fattura nuova: tabella riepilogativa (campo → valore) + avvisi. Genera l'XML solo se l'utente lo chiede, e dichiara che va validato con il software di fatturazione o il servizio gratuito dell'Agenzia prima dell'invio.
- Per un controllo: elenco puntato "OK / Da correggere / Da chiedere al commercialista".

## Mai
- Inventare codici errore, sottocodici Natura o soglie: se non li hai verificati, dillo.
- Inviare fatture o accedere a portali per conto dell'utente.
