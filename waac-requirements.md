# Sommario {#sommario .TOC-Heading}

[**INBOUND** [1](#inbound)](#inbound)

[**Gestione Ricevimento**
[1](#gestione-ricevimento)](#gestione-ricevimento)

[**Putaway / Stock Confirm:**
[2](#putaway-stock-confirm)](#putaway-stock-confirm)

[**OUTBOUND** [2](#outbound)](#outbound)

[**Gestione Spedizione**
[2](#gestione-spedizione)](#gestione-spedizione)

[**Picking Wave:** [2](#picking-wave)](#picking-wave)

[**Tipologie di Picking:**
[2](#tipologie-di-picking)](#tipologie-di-picking)

[**Modalità di Picking:**
[2](#modalità-di-picking)](#modalità-di-picking)

[**Metodi di Picking:** [3](#metodi-di-picking)](#metodi-di-picking)

[**PACKING PROCEDURE** [3](#packing-procedure)](#packing-procedure)

[**LOADING PROCEDURE** [4](#loading-procedure)](#loading-procedure)

[**Cross-Docking:** [4](#cross-docking)](#cross-docking)

[**MASTER DATA** [5](#master-data)](#master-data)

# **INBOUND**

## **Gestione Ricevimento**

Il processo di gestione del ricevimento è cruciale per garantire un
flusso regolare di merci in entrata e l'accuratezza dei dati registrati
nel sistema. Le funzionalità richieste includono l\'uso di dispositivi a
radiofrequenza (RF) per la scansione e il controllo.

-   **Con ASN (Advance Shipping Notice):** In presenza di un avviso di
    spedizione anticipato, il sistema deve gestire la registrazione
    delle unità di stock (SSC) e la creazione di nuove unità di handling
    (HD). Questo approccio migliora l\'efficienza e riduce gli errori
    umani.

-   **Senza ASN:** Quando manca un avviso di spedizione, il sistema deve
    supportare diverse modalità di scansione:

    -   PZ/QT: Per la registrazione dei pezzi e delle quantità.

    -   PZ/PZ: Per il conteggio dettagliato pezzo per pezzo.

    -   Numero seriale: Per la tracciabilità di articoli con numero
        seriale.

## **Putaway / Stock Confirm:**

La gestione dello stoccaggio e della conferma è fondamentale per
ottimizzare l'utilizzo dello spazio e garantire che le merci siano
posizionate nei luoghi corretti. Il sistema deve supportare:

-   Stoccaggio pezzo per pezzo (PZ/PZ).

-   Stoccaggio per cartoni (Carton).

-   Stoccaggio di pallet interi (Pallet).

-   Stoccaggio organizzato per zone (By Zone), per semplificare il
    processo di recupero successivo.

# **OUTBOUND**

## **Gestione Spedizione**

Le funzionalità outbound sono progettate per garantire che le spedizioni
siano pianificate e gestite in modo accurato ed efficiente, riducendo i
ritardi e migliorando la soddisfazione del cliente.

## **Picking Wave:**

La creazione di \"onde di picking\" è una funzione avanzata che consente
di ottimizzare il processo di prelievo:

1.  Supporto sia per onde automatiche che manuali, a seconda delle
    esigenze operative.

2.  Possibilità di selezionare gli ordini da includere nell\'onda di
    picking.

3.  Filtri per l'organizzazione delle onde basati su diversi criteri,
    come vettore, metodo di spedizione e orario di partenza del camion.

4.  Suddivisione per tipo di ordine, per gestire richieste particolari.

5.  Gestione delle trattenute (Retention Management) per ordini che
    richiedono verifiche o autorizzazioni prima della spedizione.

## **Tipologie di Picking:**

Il WMS deve supportare diverse tipologie di picking per adattarsi alle
esigenze del magazzino:

1.  Picking fisso o dinamico, per gestire stazioni di prelievo fisse o
    mobili.

2.  Preparazione di ordini bulk o prelievo di pallet interi.

3.  Gestione di articoli \"Out of Gauge\" (dimensioni fuori standard).

4.  Picking meccanizzato, per magazzini con automazione avanzata.

## **Modalità di Picking:**

Per garantire flessibilità operativa, il sistema deve supportare:

1.  Picking multi-ordini, per ottimizzare i tempi e i percorsi.

2.  Ventilazione pick-up, per gestire articoli destinati a più ordini.

3.  Picking per ordini singoli, quando richiesto.

4.  Ventilazione pallet intero, per gestire rapidamente grandi quantità.

## **Metodi di Picking:**

La varietà di metodi disponibili permette di adattarsi a diverse
configurazioni operative:

1.  Utilizzo di dispositivi a radiofrequenza (RF).

2.  Picking vocale con dispositivi RF vocalizzati.

3.  Sistemi \"Pick to Light\" e \"Put to Light\", per aumentare
    l\'efficienza e ridurre gli errori.

4.  Modalità cartacea, per operazioni in ambienti con bassa tecnologia.

5.  Picking tramite triangolazione, per ottimizzare i percorsi
    all'interno del magazzino.

## **PACKING PROCEDURE**

La procedura di imballaggio è una fase critica per garantire che i
prodotti siano pronti per la spedizione e arrivino al cliente in
condizioni ottimali. Le funzionalità richieste includono:

1.  **Consolidamento degli ordini:**

    -   Raccolta di tutti gli articoli di un ordine in un\'unica
        postazione.

    -   Verifica della completezza dell\'ordine mediante dispositivi RF
        o sistemi automatizzati.

2.  **Imballaggio:**

    -   Suggerimento automatico del tipo di imballaggio più adatto in
        base alle dimensioni, peso e fragilità degli articoli.

    -   Stampa di etichette di spedizione con barcode per
        l\'identificazione univoca.

    -   Aggiunta di materiali protettivi per garantire l\'integrità
        durante il trasporto.

3.  **Controllo finale:**

    -   Scansione dell\'etichetta per confermare l\'imballo.

    -   Assegnazione della spedizione al vettore corretto.

4.  **Stoccaggio temporaneo:**

    -   Posizionamento degli ordini imballati nell\'area di staging in
        attesa del carico.

## **LOADING PROCEDURE**

La procedura di caricamento dei mezzi assicura che le spedizioni siano
caricate correttamente e consegnate in modo puntuale. Le funzionalità
richieste includono:

1.  **Pianificazione del carico:**

    -   Generazione di un piano di carico basato su sequenze di
        consegna, tipo di veicolo e volume disponibile.

    -   Ottimizzazione del posizionamento delle merci per facilitare il
        processo di scarico.

2.  **Assegnazione dei vettori:**

    -   Identificazione del mezzo corretto tramite tabelle di routing o
        istruzioni di consegna specifiche.

3.  **Controllo del carico:**

    -   Scansione dei barcode degli imballaggi per garantire che ogni
        articolo sia correttamente assegnato al mezzo.

    -   Verifica del peso e delle dimensioni per rispettare i limiti di
        carico.

4.  **Conferma di spedizione:**

    -   Generazione automatica della documentazione di trasporto (es.
        DDT, bolle di accompagnamento).

    -   Notifica al cliente dell\'avvenuta spedizione con eventuale
        tracking number.

5.  **Chiusura del carico:**

    -   Scansione finale per confermare la chiusura del mezzo.

    -   Aggiornamento in tempo reale dello stato di spedizione nel WMS.

## **Cross-Docking:**

Il cross-docking è una funzionalità essenziale per magazzini con flussi
elevati e operazioni rapide:

1.  Gestione di pallet allocati per spedizioni dirette.

2.  Allocazione di colli singoli.

3.  Trattamento di referenze sconosciute con controlli aggiuntivi.

4.  Gestione di flussi ventilati, per ordini suddivisi in più
    destinazioni.

5.  Flusso controllato, per garantire l'accuratezza e il controllo delle
    spedizioni.

# **MASTER DATA**

La gestione del Master Data rappresenta la base di un sistema WMS ben
strutturato. Questo modulo deve consentire l'archiviazione, la gestione
e l'aggiornamento dei dati principali relativi agli articoli, ai
fornitori, ai clienti e alle ubicazioni del magazzino.

**Dati degli Articoli:**

-   Codici articolo univoci.

-   Descrizioni, specifiche tecniche e dimensioni.

-   Classificazione per categorie, gruppi merceologici e famiglie di
    prodotto.

-   Peso, volume e altre caratteristiche fisiche rilevanti.

**Dati dei Fornitori e dei Clienti:**

-   Dettagli anagrafici completi.

-   Informazioni di contatto e indirizzi.

-   Condizioni di fornitura o consegna.

-   Restrizioni o preferenze specifiche.

**Dati delle Ubicazioni:**

-   Definizione delle zone di magazzino (ricevimento, stoccaggio,
    picking, spedizione).

-   Capacità delle ubicazioni, suddivise per tipo (scaffale, pallet,
    bulk).

-   Mapping delle ubicazioni, per facilitare i processi di navigazione.

Una gestione efficiente del Master Data consente di ridurre al minimo
gli errori, migliorare la tracciabilità e garantire una maggiore
coerenza nei processi operativi.

# **EDI Integration**

L'integrazione EDI (Electronic Data Interchange) è fondamentale per
garantire uno scambio rapido e affidabile di informazioni tra il WMS e i
sistemi esterni, come quelli dei fornitori, clienti e vettori logistici.
Le funzionalità richieste includono:

1.  **Supporto ai principali standard EDI:**

    -   ANSI X12, EDIFACT, XML, JSON, o altri formati utilizzati nel
        settore logistico.

2.  **Integrazione con flussi inbound e outbound:**

    -   Importazione automatica di ASN (Advance Shipping Notices) per il
        ricevimento merci.

    -   Invio di notifiche di spedizione (DESADV) ai clienti.

3.  **Automazione delle transazioni:**

    -   Ordini di acquisto (PO), conferme d'ordine (POA) e avvisi di
        spedizione generati automaticamente.

    -   Integrazione con sistemi di fatturazione per l'emissione delle
        invoice (INVOIC).

4.  **Tracciabilità e auditing:**

    -   Log dettagliati per monitorare tutte le transazioni EDI.

    -   Notifiche di errore o incongruenze nel flusso dati.

5.  **Scalabilità:**

    -   Possibilità di integrare nuovi partner commerciali senza
        interruzioni operative.

6.  **Sicurezza:**

    -   Protezione dei dati con protocolli di comunicazione sicuri (es.
        AS2, SFTP).

Con queste funzionalità, il sistema potrà comunicare in modo efficiente
e automatizzato, riducendo gli errori manuali e migliorando i tempi di
risposta.