---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Frequenza avvisi
{: #avmon_alert_freq}

Il pannello Frequenza avvisi contiene una mappa che visualizza gli avvisi più recenti. Gli avvisi sono raggruppati per ubicazione ed elencati nella tabella Avvisi.
{: shortdesc}

## Mappa Frequenza avvisi
{: #avmon_alertmap}

La mappa Frequenza avvisi visualizza delle informazioni immediate per tutti i PoP (point of presence) per i tuoi test.

Utilizza la funzione di ingrandimento per ingrandire qualsiasi area dell'associazione o per ripristinarla alla sua dimensione originale. Passa con il mouse
su ogni ubicazione per visualizzare il nome dell'ubicazione e il numero di avvertenze e di avvisi critici
nell'ubicazione. Puoi filtrare gli avvisi visualizzati nell'associazione selezionando
**Tutti**, **Apri** o **Chiudi** dall'elenco a discesa
**Avvisi**.

![Mappa Frequenza avvisi che visualizza i test in quattro PoP.](images/alert_freq_map2.png)

### Ubicazione host
L'icona **Ubicazione host** ![Icona Ubicazione host.](images/icn_host_crit_whtbackground30.jpg) rappresenta l'ubicazione del server in cui è in esecuzione l'applicazione che stai monitorando. Il colore dell'icona **Ubicazione host** rappresenta la severità dell'avviso più recente in quella ubicazione: Normale ![Icona Ubicazione host con bordo verde che indica nessun avviso in quella ubicazione.](images/icn_host_normal_whtbckgrnd_30x38.jpg), Avvertenza ![Icona Ubicazione host con bordo giallo che indica un avviso in quella ubicazione.](images/icn_host_warning_whtbackground30.jpg) o Critico ![Icona Ubicazione host con bordo rosso che indica un avviso in quella ubicazione.](images/icn_host_crit_whtbackground30.jpg). Un'icona **Ubicazione host** animata indica che questa ubicazione ha il numero maggiore di avvisi con il livello massimo di severità tra tutte le ubicazioni per le istanze di test.

### Ubicazioni PoP
Le icone **Ubicazione PoP** ![Icona ubicazione PoP.](images/icn_pop_normal_whtbckgrnd30x30.jpg) indicano le ubicazioni PoP per i tuoi test. Il colore di ogni icona **Ubicazione PoP** rappresenta la severità dell'avviso più recente in ciascuna ubicazione: Normale ![Icona Ubicazione PoP con bordo verde che indica nessun avviso in quella ubicazione.](images/icn_pop_normal_whtbckgrnd30x30.jpg), Avvertenza ![Icona Ubicazione PoP con bordo giallo che indica un avviso in quella ubicazione.](images/icn_pop_warning_whtbckgrnd30x30.jpg) o Critico ![Icona Ubicazione PoP con bordo rosso che indica un avviso in quella ubicazione.](images/icn_pop_crit_whtbckgrnd30x30.jpg). Un'icona **Ubicazione PoP** animata indica che questa ubicazione ha il numero maggiore di avvisi
con il livello massimo di severità tra tutte le ubicazioni per le istanze di test.

Aggiungi le ubicazioni PoP al test selezionato posizionando il puntatore del mouse su un'icona **Ubicazione PoP non attiva** ![Ubicazione PoP non attiva](images/icn_avbl_pop.jpg) e facendo clic su **Esegui test qui**. Viene visualizzata la pagina Modalità di modifica del test per il test selezionato. Puoi selezionare un test dal menu a discesa **Test** nel pannello
**Tempo di risposta** e **Disponibilità**.

<!--
Private PoP locations are represented by **Private PoP location** icons ![Private PoP location icon that indicates 2 alerts with one or more critical alerts at that location.](images/avmon_private_pop.png).
-->
### Numero di avvisi
L'icona **Ubicazione host** e le icone **Ubicazione PoP** visualizzano il numero di avvisi aperti, chiusi o complessivi generati in ogni ubicazione. Le icone Critico, Avvertenza e Normale ![Icone Critico, Avvertenza e Normale.](images/fltr_alrts_tbl.jpg) visualizzano il numero di avvisi di ogni severità per le tue ubicazioni. 

### Test non riusciti
Le ubicazioni in cui si verificano istanze di test non riuscite sono indicate da un'icona **Ubicazione host** o da un'icona **Ubicazione PoP** con un bordo tratteggiato ![Icona Ubicazione PoP con un bordo rosso che indica 10 avvisi e uno o più test non riusciti in quella ubicazione.](images/avmon_pop_fail_32x33.png).

## Tabella degli avvisi
{: #avmon_alertstable}

Gli avvisi per tutte le ubicazioni vengono visualizzati in una tabella.

![Tabella Avvisi che mostra gli avvisi per tutte le ubicazioni PoP.](images/alert_table.jpg)

La tabella visualizza le seguenti informazioni
sui tuoi avvisi:

-   **Severità** descrive l'avviso come critico o avvertenza.
-   **Data/ora** mostra l'ora in cui è stato creato l'avviso.
-   **Descrizione** riepiloga le prestazioni della tua istanza di test.
-   **Attivato da** mostra il nome del test che ha attivato l'avviso.
-   **Ubicazione** indica dove si è verificato il problema.
-   **Stato** mostra se l'avviso è aperto o chiuso.

### Visualizzazione dei dettagli dell'avviso
Ogni avviso nella tabella contiene un link al dashboard **Analisi stratificata**. Utilizza il dashboard Analisi stratificata come ausilio per risolvere il problema.

### Filtro di avvisi
Per filtrare gli avvisi per una determinata ubicazione, fai clic su un'icona **Ubicazione host** o **Ubicazione PoP** nella mappa. Per visualizzare gli avvisi per tutte le ubicazioni, fai clic in qualsiasi punto della mappa che non sia un'icona **Ubicazione host** o **Ubicazione PoP**.

Per filtrare gli avvisi nella tabella in base alla severità, fai clic sull'icona **Critico**, **Avvertenza** o **Normale** ![Icone Critico, Avvertenza e Normale.](images/fltr_alrts_tbl.jpg). Per rimuovere il filtro e includere gli avvisi di ogni severità nella tabella, fai di nuovo clic
sull'icona selezionata.

### Modifica delle soglie di avviso
Gli avvisi vengono attivati dalle soglie che specifichi durante la creazione di un test. Nella maggior parte dei
casi, vengono generati in seguito a errori di disponibilità o tempi di risposta lenti. Per modificare le impostazioni di soglia, fai clic sull'icona **Azioni** ![Icona Azioni.](images/actions_icn_white_smll.jpg) sul test che ha generato l'avviso nel riquadro Test sintetici e seleziona **Modifica**.
