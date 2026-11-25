# Skill per Claude in italiano

Qui trovi dieci skill gratuite in italiano per Claude, l'assistente di intelligenza artificiale di Anthropic. Una skill è un file di istruzioni che insegna a Claude a fare un lavoro preciso. Per esempio, con la skill sul forfettario Claude stima passo per passo le tasse e i contributi di una partita IVA.

Queste dieci servono per il fisco, la burocrazia, il lavoro, la scuola e il fantacalcio. Le ha scritte [promp.it](https://promp.it), un laboratorio italiano di intelligenza artificiale. Ogni skill chiede a Claude di non inventare niente. Quelle sul fisco, come il forfettario, la fattura elettronica e la successione, gli chiedono anche di controllare soglie, aliquote e scadenze sui siti ufficiali prima di darle per buone.

## Le skill

| Skill | A cosa serve | Scarica | Pagina |
|---|---|---|---|
| Curriculum | Scrive il CV e la lettera di presentazione adattati all'annuncio di lavoro, senza inventare niente. | [zip](zip/cv-italiano.zip) | [promp.it/skill/cv-italiano](https://promp.it/skill/cv-italiano) |
| Dichiarazione di successione | Spiega cosa fare dopo un lutto, entro quando e con quali documenti, una cosa alla volta. | [zip](zip/successione-documenti.zip) | [promp.it/skill/successione-documenti](https://promp.it/skill/successione-documenti) |
| Fantacalcio | Aiuta con l'asta, la formazione e gli scambi, usando solo dati aggiornati. | [zip](zip/fantacalcio.zip) | [promp.it/skill/fantacalcio](https://promp.it/skill/fantacalcio) |
| Fattura elettronica | Aiuta a compilare la fattura giusta al primo colpo. Se il Sistema di Interscambio dell'Agenzia delle Entrate la scarta, spiega perché. | [zip](zip/fattura-elettronica.zip) | [promp.it/skill/fattura-elettronica](https://promp.it/skill/fattura-elettronica) |
| Forfettario | Stima quanto paghi tra tasse e contributi e quanto ti resta, con le soglie e le aliquote dell'anno in corso, controllate sulle fonti ufficiali. | [zip](zip/forfettario.zip) | [promp.it/skill/forfettario](https://promp.it/skill/forfettario) |
| Leggi bando | Riassume in una pagina un bando di gara, un bando per contributi o un avviso pubblico, con le scadenze e l'elenco dei documenti. Alla fine ti dice se puoi partecipare. | [zip](zip/leggi-bando.zip) | [promp.it/skill/leggi-bando](https://promp.it/skill/leggi-bando) |
| Lettore di contratti | Legge contratti di affitto, di lavoro e di servizi. Segna ogni clausola in rosso se va cambiata, in giallo se va chiarita e in verde se è normale. Per le clausole in rosso cita la norma di legge. | [zip](zip/lettore-contratti.zip) | [promp.it/skill/lettore-contratti](https://promp.it/skill/lettore-contratti) |
| Revisore di tesi | Controlla struttura, citazioni e bibliografia di una tesi, come farebbe un relatore paziente. | [zip](zip/revisore-tesi.zip) | [promp.it/skill/revisore-tesi](https://promp.it/skill/revisore-tesi) |
| Scrivere alla PA | Scrive richieste di accesso agli atti, reclami e diffide per la pubblica amministrazione e per le aziende, pronte da mandare via PEC. Ogni lettera sta in una pagina. | [zip](zip/scrivere-alla-pa.zip) | [promp.it/skill/scrivere-alla-pa](https://promp.it/skill/scrivere-alla-pa) |
| Verifiche per la scuola | Prepara verifiche, griglie di valutazione e versioni facilitate per gli alunni con DSA o BES, cioè con disturbi specifici dell'apprendimento o bisogni educativi speciali. | [zip](zip/verifiche-scuola.zip) | [promp.it/skill/verifiche-scuola](https://promp.it/skill/verifiche-scuola) |

Ogni pagina su promp.it spiega la skill con esempi. Le istruzioni che legge Claude sono nel file SKILL.md di ogni cartella dentro [skills](skills).

## Come si installa

**Sul sito claude.ai e nell'app di Claude**
1. Nelle impostazioni di Claude accendi l'esecuzione del codice e la creazione di file. A seconda della versione dell'app, la voce si chiama «Esecuzione di codice nel cloud e creazione di file» oppure «Crea e modifica file». Senza questa opzione le skill non funzionano.
2. Scarica lo zip della skill che ti serve dalla tabella qui sopra. Non aprirlo e non estrarlo, perché Claude vuole il file zip così com'è. Se il Mac lo apre da solo e ti ritrovi una cartella, fai clic con il tasto destro sulla cartella e scegli «Comprimi»: così ottieni di nuovo lo zip.
3. Nelle impostazioni apri Competenze, che è il nome italiano delle skill. Premi «+ Aggiungi», poi «Carica competenza», e scegli lo zip.
4. Controlla che l'interruttore della skill sia acceso.
5. Scrivi la tua richiesta come al solito, per esempio «mi leggi questo contratto?». Claude usa la skill da solo quando serve.

Le skill funzionano con tutti i piani di Claude, anche con quello gratuito. Le voci dei menu possono cambiare un po' con gli aggiornamenti dell'app. La guida completa è su [promp.it/skill/come-installare](https://promp.it/skill/come-installare).

**Su Claude Code**

Claude Code è la versione di Claude per chi programma. Se non lo usi, puoi saltare questa parte.

Copia la cartella della skill in `~/.claude/skills/` per averla in tutti i progetti, oppure in `.claude/skills/` dentro un progetto. Per installarle tutte insieme c'è [tutte-le-skill.zip](zip/tutte-le-skill.zip):

```bash
mkdir -p ~/.claude/skills && unzip tutte-le-skill.zip -d ~/.claude/skills/
```

Se le skill nuove non compaiono, apri una nuova sessione di Claude Code.

## Licenza

Le skill sono pubblicate con la licenza [Creative Commons Attribuzione 4.0 Internazionale (CC BY 4.0)](LICENSE). Puoi usarle, modificarle e condividerle, anche per lavoro. Devi però citare promp.it come autore, con il link a https://promp.it, indicare la licenza e dire se le hai modificate.

## Altre skill e kit

Su [promp.it/skill](https://promp.it/skill) trovi anche le skill per chi investe e gli strumenti gratuiti sulle tasse degli ETF, i fondi quotati in Borsa. Su [promp.it/kit](https://promp.it/kit) ci sono i kit, che ti accompagnano dall'inizio alla fine di una pratica, come l'ISEE o le multe.
