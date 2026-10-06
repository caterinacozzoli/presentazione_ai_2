# README — Workshop AI S1 · "Che tipo di AI sei?"

**Brief operativo per generare la rivista-presentazione in HTML e lo script del conduttore.**

Questo file è destinato a un agente che lavora in locale (Antigravity). Non è una descrizione del progetto: è l'insieme di regole da seguire per produrre i deliverable. Va letto per intero prima di generare. In fondo c'è una checklist: ogni voce deve poter essere spuntata.

---

## 0. Cosa c'è in questa cartella

| Elemento | Cos'è |
|---|---|
| `README.md` | Questo file. Le regole. Si legge per primo. |
| `slide_inspo_contenuto/` | **La bibliografia.** Il nome inganna: non sono spunti grafici, sono le fonti di contenuto. Vanno lette per intero. |
| Output attesi | `workshop_s1.html` (la rivista) · `SCRIPT_S1.md` (il parlato del conduttore) · `FONTI_S1.md` (la pagina fonti) |

I file di contenuto noti in `slide_inspo_contenuto/`:

| File | Contenuto | Serve per |
|---|---|---|
| `slide_ai_prompt_design.md` | Definizioni AI/GenAI/prompt design, mindset, tipi di prompt, regole, tecniche avanzate, tool | Blocchi token/prompt |
| `slide_ai_inclusivity.md` | Inclusive vs universal vs accessible design, bias nei dataset (fonte Sketchin) | Blocco immagini/bias |
| `dove_inclusive_prompt_images.md` | Playbook operativo di prompting inclusivo per immagini: struttura, do's & don'ts, glossario descrittori (fonte Dove) | Blocco immagini/bias — è la fonte più operativa, va sfruttata, non citata di sfuggita |

**Regola sui contenuti.** L'agente legge i file interi e seleziona le parti pertinenti a ciascun blocco secondo il criterio della sezione 7. Ogni affermazione di fatto nella rivista deve risalire a un file della cartella o a una fonte della sezione 9. Se un dato non ha fonte, si taglia: non si colma con una stima plausibile.

---

## 1. L'idea in una riga

Una rivista interattiva in stile primi anni Duemila — il test "che tipo sei?" — in cui il lettore scopre il proprio **archetipo AI**, e ogni archetipo corrisponde a un pregiudizio sull'AI che la sessione smonta. **L'indice della presentazione è la copertina della rivista. I pregiudizi sono i titoli degli articoli.**

Il filo rosso che tiene tutto insieme: **il limite nel prompting non è lo strumento, è la nostra immaginazione.** Ogni blocco dimostra questa idea applicata a un problema diverso.

---

## 2. Tono e registro

**Ironico, alla mano, un po' 2000 un po' 2026.**

- **Il contenitore è vintage**: estetica da rivista per ragazzi dei primi Duemila — test della personalità, oroscopo che ti parla come se ti conoscesse, fustelle "vai a pagina X", box con filetti spessi, strilli di copertina.
- **La battuta dentro è di oggi**: ironia secca da internet 2026, tono da caption che sa di essere una caption.
- Funziona per contrasto: cornice retrò, lingua contemporanea.

**Due assi da non confondere.** Uno è il volume dell'ironia, l'altro è il bersaglio. Volume al massimo, bersaglio mai su una persona reale. L'ironia colpisce l'**archetipo** (una caricatura scritta da noi), mai chi lo riceve. Nessuno, scegliendo le risposte, sta dichiarando "sono stupido": sta scegliendo una maschera divertente. È il meccanismo di sicurezza che regge anche con l'ironia alzata al massimo.

**Riferimento di fondo per il modo di spiegare: Alberto Manzi.** Frasi brevi e scandite, mai condiscendenza, il pubblico è intelligente e capace, l'astratto si rende visibile con un esempio o una dimostrazione dal vivo. L'ironia è la superficie; sotto, la pazienza e il rispetto di Manzi. Nessuno è "indietro".

**Test del registro.** Una battuta si legge ad alta voce. Se inciampa o suona come una slide letta, si riscrive. Se fa ridere ma lascia a qualcuno il permesso di disconnettersi ("tanto non fa per me"), si riscrive: l'ironia non deve mai autorizzare l'abbandono. All'archetipo con poca attenzione non si dà il permesso di andarsene, si dà il percorso più corto ("per te la versione in tre mosse, sta nel blocco X, il resto è bonus").

---

## 3. Gli archetipi

Il cuore della sessione. Ogni archetipo = un pregiudizio reale sull'AI = un blocco di contenuto che lo smonta.

**Come si ricavano.** Usare la skill `last30days` per osservare come parla davvero la gente dell'AI su Reddit e forum: lessico, lamentele ricorrenti, tono. Da quella ricerca si scrivono **citazioni verosimili con username inventati e divertenti** (`u/pixel_pusher_99`, `u/nonhotempo`, `u/BrickMaxxer`). Non si riportano mai post reali né username reali: le persone sullo schermo non devono essere identificabili. L'effetto "gente vera" resta; il rischio di esporre qualcuno no.

**Set di partenza** (l'agente può raffinare i nomi e il numero — da 4 a 5 — ma non la logica: ogni archetipo deve agganciare un blocco):

| Archetipo | Pregiudizio che incarna | Blocco che lo smonta | Ha ragione in parte? |
|---|---|---|---|
| **Cassandra del Server Farm** (complottista ambientale) | "Consuma un'enormità, è un disastro" | Token & consumi | Sì: il consumo esiste, è solo molto più basso della percezione. Non smontarlo del tutto. |
| **L'Analogico Diffidente** | "Scrivo meglio io, non mi serve" | File, struttura, Markdown | Sì: senza materiale strutturato l'output è scadente davvero. |
| **Ci Provo Ma Boh** | "L'output viene sempre piatto" | Prompt optimization | Sì: con un prompt generico l'output *è* piatto. La colpa non è dello strumento. |
| **Prompt Boomer** (presunto esperto) | "Le immagini AI sono tutte uguali" | Bias & prompting inclusivo | Sì: lo sono, finché non sai chiedere altro. È il colpo di scena finale: ribalta chi si credeva avanti. |

Ogni esito del quiz è scritto nel tono della sezione 2 e **rimanda al blocco corrispondente come una fustella di rivista** ("Pagina 3 per i numeri che ti spezzano il cuore").

Esempi di tono per gli esiti (da rifinire, danno la misura):
- *"Risultato: Cassandra del Server Farm. Hai ragione che consuma, hai torto su quanto. Pagina 3 per i numeri che ti spezzano il cuore."*
- *"Risultato: Prompt Boomer. Pensi che le AI generino sempre la stessa ragazza con la pelle perfetta. Hai ragione — se non sai come chiederle altro. Pagina 9, prima che qualcuno se ne accorga."*

**Esito e dato collettivo.** Ognuno risponde sul proprio device; l'archetipo appare in pagina. In parallelo scrive la lettera scelta nella chat di Teams, così il conduttore ha anche il dato di sala ("siamo per metà Cassandre, partiamo da voi").

**Calcolo dell'archetipo.** Risposta dominante: si conta la lettera data più volte. In caso di parità vince l'ultima risposta. Semplice da spiegare a voce, impossibile da sbagliare.

---

## 4. Il conduttore

**Una sola persona conduce l'intera sessione.** Lo script è scritto per una voce sola: niente stacchi tra relatori, niente "passo la parola".

Conseguenze per la scrittura:
- Il ritmo lo tiene la varietà dei formati (quiz, rebus, dimostrazione, video), non il cambio di voce.
- Le micro-interazioni sono le pause che spezzano il monologo meglio di un secondo relatore.
- Il conduttore non recita: conversa con la sala e con la chat.

---

## 5. Struttura della sessione

40 minuti netti. Il quiz è l'indice; ogni blocco smonta un archetipo. Il filo (immaginazione > strumento) attraversa tutto.

| # | Momento | Minuti | Interazione |
|---|---|---|---|
| 0 | Copertina + quiz "che tipo di AI sei?" | 6' | Quiz sul device, lettera in chat |
| 1 | **Token & consumi** — smonta la Cassandra | 7' | Tokenizer dal vivo: stesso prompt, due scritture, il numero scende |
| 2 | **File & Markdown** — smonta l'Analogico | 7' | Mini-rebus: com'è fatto un `.md` (mostrato) + avvertenza convertitori online/riservatezza |
| 3 | **Prompt optimization + Test del Mattone** — smonta il Ci Provo Ma Boh | 11' | Test di Guilford in chat (2'), poi prima/dopo del prompt a schermo |
| 4 | **Bias & immagini inclusive** — smonta il Prompt Boomer | 7' | Prima/dopo di un prompt immagine: generico vs inclusivo |
| 5 | Chiusura + aggancio S2 | 2' | Annuncio agenda futura |

Regole di tempo: nessun blocco di solo parlato supera i ~5 minuti senza un'interazione in mezzo. Se un blocco sfora, si taglia dentro quel blocco, non si ruba tempo agli altri.

### Il filo dei token (collega blocco 1 e 3)

La catena da rendere esplicita: il consumo si misura in token → i token li determini tu con come scrivi → scrivere meglio non è solo qualità, è anche misura. Così il dato ambientale smette di essere curiosità inerte e diventa la motivazione del prompt optimization. Tokenizer dal vivo = il "carboncino di Manzi": due prompt che chiedono la stessa cosa, uno sciatto e uno pulito, il numero scende a schermo in 90 secondi.

### Il Test del Mattone (dentro il blocco 3)

Test degli Usi Alternativi di Guilford (1967), misura del pensiero divergente. Si introduce con voce da rivista ("test psicologico vero, 1967, prestato dalla scienza seria per scopi non seri"). **Si fa fare a tutta la sala in chat, anonimo, timer 2 minuti** — mai pescare una persona a sorpresa (rompe il registro Manzi e in remoto aggiunge solo imbarazzo). Il conduttore conta a voce quante idee diverse (fluidità) e quante categorie distinte (flessibilità) emergono: di solito poche, tutte dentro "costruzione". Poi la stessa domanda all'AI, a schermo: prima prompt neutro (converge come gli umani), poi prompt che chiede divergenza ("rompi la categoria ovvia", "uno per ogni senso", "uno impossibile ma logico") e il numero esplode.

**Punto da far atterrare:** non è l'AI che sblocca il pensiero laterale, è il prompt scritto con pensiero laterale che lo fa — e l'AI lo esegue in scala. Chiude il cerchio col blocco token: prompt povero costa poco e rende poco, prompt divergente costa un filo di più e moltiplica.

I quattro parametri di Guilford (fluidità, flessibilità, originalità, elaborazione) si nominano en passant come griglia di lettura, non come lezione.

---

## 6. La rivista HTML — come si costruisce

Un unico file `workshop_s1.html`, autosufficiente, che ciascuno apre sul proprio device.

**Estetica.** Fanzine dei primi Duemila: filetti spessi, bold colorati su bianco sporco/carta, occhielli e strilli, box con bordo marcato, numeri di pagina, fustelle "→ vai a pagina X". Ornamenti in **ASCII art** dove serve caratterizzare (divisori, cornici, loghi finti). Sopra questa ossatura, moduli interattivi in **stile card alla Reddit** per le citazioni degli archetipi (username finto, finti upvote, finto "3h fa").

**Struttura a pagine di rivista.** La copertina è l'indice: titoli-pregiudizio come strilli di giornale. Ogni "articolo" è un blocco. La navigazione imita lo sfogliare.

**Interazioni ammesse** (piccole, nel punto giusto, mai una grande a parte):
- Quiz archetipi (copertina)
- Tokenizer dal vivo — spazio per embed o link a `https://platform.openai.com/tokenizer`
- Rebus / mini-cruciverba sul Markdown (blocco 2)
- Test del Mattone con timer (blocco 3)
- Prima/dopo di un prompt (blocchi 3 e 4)
- Spazi per **embeddare video ed esercizi**: predisporre contenitori chiari e commentati (`<!-- EMBED: descrizione -->`) dove inserire iframe o link.

**Regola fonti — vincolante.** Ogni blocco di contenuto che proviene da una slide inspo o da una fonte esterna porta **la fonte in basso a destra, come hyperlink, quando la fonte c'è.** Formato discreto, carattere piccolo, allineato a destra. Se non c'è fonte, niente nota.

**Tecnica.** Un solo file HTML con CSS e JS inline. Nessuna dipendenza esterna obbligatoria oltre a font di sistema e, se servono, librerie da CDN affidabili. Deve aprirsi con doppio clic, offline, su qualunque browser. Mobile-friendly: molti apriranno da telefono.

---

## 7. Criterio di selezione dei contenuti dalle slide

L'agente legge ogni file di `slide_inspo_contenuto/` per intero, poi tiene solo ciò che:
1. **Smonta uno dei pregiudizi** — se un contenuto non serve a un archetipo, è fuori.
2. **È operativo** — una regola applicabile lunedì batte una definizione. Il playbook Dove ha priorità sulle definizioni teoriche.
3. **Si può mostrare** — se un concetto diventa un prima/dopo, un rebus o una dimostrazione, si privilegia quella forma.
4. **Sta nel tempo del blocco** (sezione 5).

Si scarta senza rimpianti: spiegazioni accademiche del funzionamento degli LLM (basta "predice la parola successiva"), tassonomie esaustive, tutto ciò che non cambia il comportamento di chi ascolta.

---

## 8. Lo script del conduttore — come si scrive

File `SCRIPT_S1.md`, una voce sola, nel tono della sezione 2.

Formato per ogni pagina/blocco:

```
## PAGINA N — TITOLO-STRILLO

[schermo] <cosa si vede nella rivista>

<parlato del conduttore, frasi brevi, tono 2000+2026>

*(regia: pausa — serve a far arrivare X)*

[INTERAZIONE — N minuti]
Qui si farebbe l'esercizio, che consiste in: <descrizione operativa completa>
In chat: <cosa scrive la sala>
Chi è pratico: <cosa fa>  ·  Chi preferisce seguire: <cosa guarda>
Domanda di chiusura: "<testo>"

[→ pagina successiva]
```

Regole:
- Le pause sono scritte, con la ragione.
- Ogni esercizio dichiara entrambe le modalità (fare / seguire), ogni volta.
- Nessun placeholder: ciò che è previsto è scritto per intero.
- Dove un dato ha una fonte, la fonte è indicata anche nello script.

---

## 9. Fonti

Pagina `FONTI_S1.md`, autonoma e leggibile anche da chi non ha sentito il talk: per ogni voce, titolo/autore/testata, anno, link, una riga sul perché è rilevante. Nella rivista, le stesse fonti compaiono come hyperlink in basso a destra del blocco che le usa.

**Consumi ed energia**
- Studio primario — Harding A. R., Moreno-Cruz J., IOPscience, 2025 → https://iopscience.iop.org/article/10.1088/1748-9326/ae0e3b/pdf *(fonte scientifica da citare per il dato)*
- SciTechDaily, nov. 2025 → https://scitechdaily.com/study-debunks-major-myth-ais-energy-usage-is-significantly-less-than-feared/ *(lettura di accesso)*
- The Bunker — AI vs attività quotidiane → https://www.the-bunker.it/rubrica/lia-inquina-ma-piu-o-meno-di-altre-attivita-quotidiane/

**File & Markdown**
- Medium — perché il Markdown è la lingua di lavoro dell'AI (E. McDowell) → https://medium.com/@erinmcdowell/why-markdown-became-the-working-language-of-ai-5c4be43bf45f

**Tool**
- OpenAI Tokenizer → https://platform.openai.com/tokenizer *(dimostrazione dal vivo, blocco 1)*
- Caveman — compressione testo per AI → https://github.com/JuliusBrussee/caveman

**Video**
- *Comizi d'Amore*, Pasolini, 1964 → https://www.youtube.com/watch?v=A5-kvHUcJw8 *(campione di dati e chi resta fuori dalla fotografia; mantenere come nelle slide)*

**Contenuti interni** — i tre file in `slide_inspo_contenuto/` (prompt design; inclusività/Sketchin; playbook immagini/Dove).

**Regola dato sui consumi:** dirlo sempre con ordine di grandezza e anno ("circa 5-10 ricerche Google, dato 2025"), mai con precisione finta. È un numero che invecchia in fretta.

**Dati da reinserire a cura dell'autrice** (non noti all'agente): data e piattaforma della sessione, macro-temi e date delle sessioni S2+, eventuali esempi interni reali da usare al posto di casi generici.

---

## 10. Checklist finale

**Idea e filo**
- [ ] L'indice è la copertina della rivista; i pregiudizi sono i titoli
- [ ] Il filo "immaginazione > strumento" attraversa tutti i blocchi
- [ ] Ogni archetipo ha il suo blocco che lo smonta, e ha ragione "in parte"

**Tono**
- [ ] Ironia 2000+2026, cornice retrò e lingua di oggi
- [ ] L'ironia colpisce l'archetipo, mai una persona reale
- [ ] Nessuna battuta autorizza l'abbandono
- [ ] Ogni battuta regge la lettura ad alta voce

**Reddit / archetipi**
- [ ] Citazioni verosimili, username inventati, zero post reali
- [ ] Calcolo per risposta dominante, parità all'ultima
- [ ] Esito con fustella verso il blocco + lettera in chat Teams

**Struttura**
- [ ] 40 minuti, una voce sola che conduce
- [ ] Nessun parlato oltre ~5' senza interazione
- [ ] Tokenizer dal vivo nel blocco 1
- [ ] Test del Mattone anonimo in chat, mai persona pescata a sorpresa
- [ ] Rebus Markdown + avvertenza convertitori/riservatezza nel blocco 2
- [ ] Prima/dopo prompt nei blocchi 3 e 4

**Rivista HTML**
- [ ] File unico, offline, mobile-friendly
- [ ] Estetica fanzine + card Reddit + ASCII
- [ ] Contenitori per embed di video ed esercizi
- [ ] Fonte in basso a destra come hyperlink dove esiste

**Contenuti e fonti**
- [ ] Solo contenuti che smontano un pregiudizio (criterio sez. 7)
- [ ] Playbook Dove usato in modo operativo
- [ ] Ogni dato risale a una fonte; niente stime di riempimento
- [ ] Spiegazione statistica degli LLM ridotta a una riga
- [ ] `FONTI_S1.md` autonomo e completo
- [ ] Zero placeholder nei file finali
