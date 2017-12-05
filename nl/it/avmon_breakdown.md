---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Dashboard Analisi stratificata
{: avmon_view_breakdown}

Il dashboard **Analisi stratificata** visualizza le informazioni statistiche chiave per
i tuoi test. Il dashboard inoltre riepiloga le informazioni sulla disponibilità e sul tempo di risposta, le tendenze storiche
e i dati delle prestazioni del test nelle precedenti 24 ore.
{: shortdesc}

Per visualizzare un'analisi dettagliata di un test, fai clic sul test nel riquadro Test sintetici. Puoi anche aprire il dashboard Analisi stratificata facendo clic su **Analisi stratificata** nella tabella Avviso del riquadro Frequenza avvisi.

Il dashboard di analisi stratificata visualizza quattro pannelli:

## Riepilogo test
{: #avmon_bdown_summary}

![Riquadro Riepilogo test.](images/avmon_bdown_summ.png)

Il pannello **Riepilogo test** visualizza le
seguenti informazioni sul test relative alle 24 ore precedenti:

-   **Stato corrente** visualizza lo stato del test.
-   **Istanze di test** visualizza una percentuale dell'analisi stratificata per le istanze di test normali, di avvertenza e critiche.
-   **Tempo di risposta medio** visualizza il tempo di risposta medio del test.
-   **Tendenze storiche** visualizza le tendenze storiche delle prestazioni del tuo test per il 50°, 95° e 99° percentile
in secondi o millisecondi.

## Istanze di test
{: #avmon_bdown_instances}

![Analisi dell'istanza di test dell'API REST nella tabella Istanze di test.](images/avmon_bdown_apitest_instance.png)

La tabella **Istanze di test** visualizza informazioni dettagliate relative
a ciascuna istanza di test, incluso lo stato, il tempo di risposta, la posizione di esecuzione del test, il numero
di errori e la data/ora di esecuzione del test. Per eseguire il drill down di un'istanza di test, fai clic
su **Espandi**. Vengono visualizzate informazioni di risposta dettagliate per ciascun passo dell'istanza
di test. Puoi ordinare le colonne in modo da poter identificare rapidamente il passo esatto in cui si è verificato
un rallentamento o un errore. La visualizzazione degli errori, della sequenza di test e del tempo di risposta ti consente di
identificare facilmente i problemi.

Le informazioni mostrate dipendono dal tipo di test sintetico che viene monitorato:

### API
Quando fa clic su **Espandi** per un'istanza di test API, viene visualizzato
un riepilogo di alto livello dei seguenti dettagli:

-   **Risposta** visualizza il tempo di risposta totale per l'istanza di test
incluso il tempo di reindirizzamento.
-   **Reindirizzamento** visualizza il tempo totale di reindirizzamento per l'istanza di test.
-   **Dimensione** visualizza la dimensione dell'oggetto.
-   **Velocità di scaricamento** visualizza la velocità con cui viene scaricato ogni oggetto.
-   **Errori** visualizza il numero di errori che si sono verificati durante l'istanza di
test. Per visualizzare i dettagli dell'errore, fai clic sull'icona **Informazioni**.

Una tabella
mostra ogni passo nella chiamata API, insieme al nome del passo, la
sequenza dei passi e il tempo di risposta per ciascun passo. Vengono visualizzati i seguenti nomi dei passi:

-   **Ricerca nome** rappresenta il tempo che l'istanza di test ha impiegato per risolvere
il nome dell'oggetto.
-   **Connessione** rappresenta il tempo che l'istanza di test ha utilizzato dall'inizio del passo
fino al completamento di una connessione a un host o proxy remoto.
-   **Connessione applicazione** rappresenta il tempo che l'istanza di test ha utilizzato dall'inizio del passo
fino al completamento della connessione SSL con l'host remoto.
-   **Pre trasferimento** rappresenta il tempo che l'istanza di test ha utilizzato dall'inizio del passo
fino ad appena prima l'avvio del comando di trasferimento file.
-   **Avvio trasferimento** rappresenta il tempo che l'istanza di test ha utilizzato dall'inizio del passo
fino alla ricezione del primo byte.
-   **Trasferimento** rappresenta il tempo che l'istanza di test ha impiegato per trasferire il
file.

### Pagina Web
![Analisi dell'istanza di test della pagina web nella tabella Istanze di test.](images/avmon_bdown_webpage_instance.png)

Quando fa clic su **Espandi** per un'istanza di test della pagina web, viene visualizzato
un riepilogo di alto livello dei seguenti dettagli:

-   **Risposta** indica il tempo di risposta per l'istanza di test.
-   **Richieste totali (esterne) ** visualizza il numero totale di richieste per l'istanza
di test. Il numero di richieste esterne è tra parentesi.
-   **Dimensione pagina** visualizza la dimensione della pagina web.
-   **Errori** visualizza il numero di errori che si sono verificati durante l'istanza di
test. Per visualizzare i dettagli dell'errore, fai clic sull'icona Informazioni.

Viene anche visualizzata una tabella che elenca i seguenti dettagli per ogni richiesta effettuata dal test:

-   **Tipo** visualizza il tipo di richiesta, ad esempio HTML, CSS, JavaScript o
immagine. Le richieste esterne e interne sono raffigurate da icone.
-   **Percorso file** descrive l'ubicazione dell'oggetto richiesto.
-   **Dimensione** visualizza la dimensione dell'oggetto richiesto.
-   **Sequenza** visualizza la sequenza di richieste effettuate dal
test.
-   **Ora** visualizza l'ora di ogni richiesta.
-   **Codice di stato** visualizza il codice di stato della richiesta HTTP.
-   **Stato** descrive il risultato della richiesta, ad esempio, Completato, Sconosciuto
o Non riuscito.

### Script
![Analisi dell'istanza di test dello script nella tabella Istanze di test.](images/avmon_bdown_script_instance.png)

Quando fa clic su **Espandi** per un'istanza di test dello script, vengono visualizzati
il tempo di risposta, il numero dei passi dello script e il numero di errori. Per visualizzare i dettagli dell'errore, fai clic sull'icona **Informazioni**.

I seguenti dettagli per ogni script vengono visualizzati in una tabella:

-   **Nome** visualizza ogni comando Selenium richiamato dalla tua istanza, ad esempio Open, ClickAt o VerifyBodyText.
-   **Sequenza** visualizza la sequenza dei passi dello script dall'inizio alla fine
dell'istanza di test.
-   **Ora** visualizza l'ora di ogni passo dello script.
-   **Errori** visualizza il numero di errori che si sono verificati durante ogni passo dello script.
-   **Stato** descrive il risultato del passo dello script, ad esempio, Completato, Sconosciuto
o Non riuscito.

Puoi eseguire il drill down e visualizzare i dettagli sulle richieste generate da ogni passo dello script.

![Analisi dei dettagli dei singoli passi per la tua istanza di test dello script nella tabella Istanze di test.](images/avmon_bdown_script_subtrans.png)

Fai clic su **Espandi** per visualizzare una tabella che contiene i seguenti dettagli:

-   **Tipo** visualizza il tipo di richiesta, ad esempio HTML, CSS, JavaScript o
immagine. Le richieste esterne e interne sono raffigurate da icone.
-   **Percorso file** descrive l'ubicazione dell'oggetto richiesto.
-   **Dimensione** visualizza la dimensione dell'oggetto richiesto.
-   **Sequenza** visualizza la sequenza di richieste effettuate dal
test.
-   **Ora** visualizza l'ora di ogni richiesta.
-   **Codice di stato** visualizza il codice di stato della richiesta HTTP.
-   **Stato** descrive il risultato della richiesta, ad esempio, Completato, Sconosciuto
o Non riuscito.

{{site.data.keyword.prf_hubshort}} può creare automaticamente
un'acquisizione schermo quando si verifica un errore di caricamento della pagina o un errore del passo nello script. Ad esempio,
se uno dei passi nello script apre una pagina Web ma questa non viene caricata, {{site.data.keyword.prf_hubshort}} crea automaticamente un'acquisizione schermo. Per visualizzare un'acquisizione schermo della pagina web o dello script, fai clic sull'icona **Errore screenshot** ![Icona Errore screenshot](images/scrnsht_err_icn_white.jpg). Questa funzione è disponibile solo per il monitoraggio delle pagine Web e dei test con script. Non funziona con il monitoraggio delle API REST.

Puoi anche scaricare una registrazione del traffico di rete per una determinata istanza di test in forma di file .har facendo clic sull'icona **Download** ![Icona Download.](images/download_icn_white_smll.jpg). Questa funzione è disponibile per il monitoraggio delle pagine Web e dei test di funzionamento con script.

## Tempo di risposta e Disponibilità
{: #avmon_bdown_rt_avail}
Il riquadro Tempo di risposta e Disponibilità visualizza un grafico dei tempi di risposta e della disponibilità misurati per le istanze del test in un periodo definito. Per ulteriori informazioni, vedi [Tempo di risposta e Disponibilità](avmon_resptime_avail.html "Utilizza il riquadro Tempo di risposta e Disponibilità per visualizzare i tempi di risposta, le tendenze di disponibilità, gli avvisi e le attività nel tempo. La correlazione di metriche, avvisi e attività ti consente di isolare facilmente una specifica modifica dell'applicazione o distribuzione del codice quando rilevi un impatto su un tempo di risposta.").

## Attività
{: #avmon_bdown_activity}
Il riquadro Attività mostra una tabella di tutte le attività nelle ultime 24 ore. Per ulteriori informazioni, vedi [Attività](avmon_activities.html "Le informazioni relative alle attività possono essere visualizzate nel riquadro Attività. Le attività sono azioni che si verificano al di fuori degli eventi definiti dall'utente.").
