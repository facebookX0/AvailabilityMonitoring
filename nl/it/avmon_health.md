---

copyright:
  years: 2015, 2017
lastupdated: "2017-9-28"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Integrità dell'applicazione
{: #avmon_health}

Il riquadro Integrità dell'applicazione fornisce un'istantanea delle prestazioni della tua applicazione in base alla disponibilità, alla soddisfazione degli utenti e alla velocità effettiva dell'applicazione.
{: shortdesc}

Se {{site.data.keyword.prf_hubshort}} rileva che per la tua applicazione è configurato un raccoglitore di dati, il riquadro Integrità dell'applicazione è disponibile per la visualizzazione.

**Limitazione:** inizialmente, un raccoglitore di dati è disponibile solo per le applicazioni Node.js. Per ulteriori informazioni sulla configurazione del raccoglitore di dati Node.js, vedi la [documentazione del raccoglitore di dati Node.js](https://www.npmjs.com/package/ibmapm "(Si apre in una nuova scheda o finestra)"){: new_window}.

Il riquadro visualizza tre metriche: **Disponibilità**, **Punteggio di soddisfazione** e **Volume di richieste**.
![Riquadro Integrità dell'applicazione che mostra il livello di disponibilità, la soddisfazione degli utenti e la velocità effettiva delle transazioni della tua applicazione.](images/avmon_app_health_ui.jpg)
 Il calcolo della metrica **Disponibilità** si basa sui dati delle transazioni degli utenti simulati forniti dai test sintetici. Al contrario, le metriche **Punteggio di soddisfazione** e **Volume di richieste** si basano sui dati delle transazioni degli utenti reali e simulati forniti dai raccoglitori di dati.

Le etichette numeriche mostrano l'ultimo valore di ogni metrica. Ad esempio, l'ultimo valore per **Disponibilità** è ![L'ultimo valore della metrica Disponibilità.](images/avmon_app_health_latest.jpg). I grafici a linee temporali descrivono le prestazioni della tua applicazione su ogni metrica nel corso del tempo. Puoi impostare l'espansione temporale dei grafici della cronologia selezionando le ultime **24 ore** o gli ultimi **7 giorni** nel menu a discesa Tempo. Quando passi con il mouse sulla linea del grafico, il valore per ciascun punto dati viene visualizzato in una descrizione a comparsa, ad esempio ![Una descrizione a comparsa sul grafico a linee della cronologia.](images/avmon_app_health_hover.jpg). Quando fai clic su un punto dati nel grafico a linee, l'etichetta numerica visualizza il valore per quel punto dati. Fai clic su un'area qualsiasi al di fuori dei grafici a linee per reimpostare le etichette numeriche sui loro ultimi valori. Passando il mouse o facendo clic su un grafico si aggiornano gli altri due grafici nel riquadro **Integrità dell'applicazione**.

Fai clic su ![Menu Visualizza contributi che puoi espandere per visualizzare transazioni o test di contribuzione.](images/avmon_view_contrib.jpg) per vedere le prime cinque transazioni o test che hanno contribuito all'integrità attuale dell'applicazione.![Riquadro Integrità dell'applicazione che mostra il livello di disponibilità, la soddisfazione degli utenti e la velocità effettiva delle transazioni della tua applicazione.](images/avmon_app_health_expanded.jpg)

## Disponibilità
{: #avmon_health_availability}
**Disponibilità** mostra il grado di operatività della tua applicazione. La disponibilità è determinata dalla percentuale di istanze di test sintetici superate correttamente. Ad esempio, se tutti i tuoi test sintetici sono stati eseguiti correttamente durante l'ultimo intervallo, il valore di disponibilità corrente per la tua applicazione è 100%.

Puoi configurare come {{site.data.keyword.prf_hubshort}} calcola la disponibilità dalla scheda Monitoraggio selezionando i test da includere nel calcolo della disponibilità. Per ulteriori informazioni, vedi [Accesso a Monitoraggio della disponibilità](avmon_tab.html "Puoi accedere al dashboard Monitoraggio della disponibilità dalla scheda **Monitoraggio**. La scheda Monitoraggio per la tua applicazione Cloud Foundry visualizza informazioni di riepilogo sulla disponibilità e sullo stato dei test e i dettagli e l'utilizzo della sottoscrizione del servizio.").

{{site.data.keyword.prf_hubshort}} calcola la percentuale delle istanze di test disponibili all'ora. Passa il mouse sopra la linea del grafico per visualizzare il valore per ogni intervallo di ore durante le ultime 24 ore o gli ultimi 7 giorni.

Vengono mostrati i primi cinque test sintetici che hanno contribuito al livello di disponibilità corrente della tua applicazione. La tabella visualizza le seguenti informazioni su ciascun test.

-   **Test** visualizza il nome del test che hai assegnato.
-   **Istanze** mostra il numero di istanze di test che sono state eseguite per ciascun test.
-   **Frequenza di errore** visualizza la percentuale di istanze di test non riuscite per ciascun test.


## Punteggio di soddisfazione
{: #avmon_health_satscore}
Il **Punteggio di soddisfazione** è un indicatore della soddisfazione degli utenti rispetto alla reattività della tua applicazione. Imposta un valore di soglia di soddisfazione (**T**) per la tua applicazione. Determina il tempo di risposta necessario per le richieste dell'utente affinché gli utenti siano soddisfatti.

I tempi di risposta delle richieste dell'utente vengono convertiti in un valore di indice compreso tra 0,0 e 1,0, dove 1,0 è un punteggio perfetto con tutti gli utenti soddisfatti. Per calcolare il punteggio di soddisfazione, gli esempi utente sono classificati come:

-   Soddisfatto - le richieste dell'utente con un tempo di risposta inferiore o uguale alla soglia di soddisfazione sono considerate soddisfatte.
-   Tollerato - le richieste dell'utente che rientrano tra Soddisfatto e Frustrato sono considerate tollerate.
-   Frustrato - le richieste dell'utente con un tempo di risposta superiore a 4**T** che comportano un errore, sono considerate frustrate.

Il punteggio di soddisfazione viene quindi calcolato come il rapporto tra [richieste utente soddisfatte  + (richieste utente tollerate /2)] / [numero totale di richieste utente].

{{site.data.keyword.prf_hubshort}} calcola il punteggio di soddisfazione in base ai dati della transazione per ciascun intervallo di ore. Passa il mouse sopra la linea del grafico per visualizzare il punteggio per ogni intervallo di ore durante le ultime 24 ore o gli ultimi 7 giorni.

Nella tabella vengono visualizzate le seguenti informazioni sulle prime cinque transazioni che hanno contribuito al punteggio di soddisfazione corrente della tua applicazione:

-   **Transazioni** visualizza il nome della transazione utente.
-   **Punteggio** mostra il punteggio di soddisfazione calcolato per la singola transazione.
-   **Insoddisfazione** mostra il contributo della transazione ai livelli di insoddisfazione correnti dell'utente. Se la soddisfazione dell'utente non è ottimale, utilizza la percentuale **Insoddisfazione** per valutare quanto ogni transazione abbia influenzato i livelli di insoddisfazione.


## Volume di richieste
{: #avmon_health_reqvol}
La metrica Volume di richieste è il volume corrente delle istanze di transazione utente. La metrica indica la velocità effettiva della tua applicazione.

Sotto l'etichetta viene visualizzato anche il tempo medio di riposta delle transazioni per la tua applicazione, ad esempio ![L'ultimo valore del tempo medio di risposta.](images/avmon_app_health_response.jpg) e i valori del tempo medio di risposta vengono tracciati nel grafico. Puoi cercare correlazioni tra gli aumenti della velocità effettiva e l'aumento dei tempi di risposta medi.

I dati non elaborati del volume di richieste vengono aggregati e visualizzati nel grafico ogni ora. Passa il mouse sopra la linea del grafico per visualizzare la velocità effettiva della tua applicazione per ogni intervallo di ore durante le ultime 24 ore o gli ultimi 7 giorni.

Nella tabella vengono visualizzate le seguenti informazioni sulle prime cinque transazioni che contribuiscono maggiormente al volume di richieste corrente. Se la tua applicazione sta riscontrando dei volumi elevati di traffico utente, utilizza la **Percentuale del totale** per valutare quanto ogni transazione contribuisce al volume di traffico complessivo.

-   **Transazione** visualizza il nome della transazione utente.
-   **Volume** mostra il numero di istanze di transazione per ogni transazione.
-   **Percentuale del totale** visualizza la percentuale del volume totale di richieste.
