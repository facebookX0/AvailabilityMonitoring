---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Utilizzo del servizio
{: #avmon_usage}

Puoi visualizzare i dettagli sul tuo utilizzo di {{site.data.keyword.prf_hubshort}} nella scheda **Monitoraggio** della tua applicazione e nel dashboard principale di {{site.data.keyword.prf_hubshort}}.

Per visualizzare una panoramica del tuo utilizzo {{site.data.keyword.prf_hubshort}}
dalla tabella **Tutte le applicazioni**, fai clic sul tuo nome applicazione; quindi, fai clic sulla scheda
**Monitoraggio** nel tuo pannello dell'applicazione. Viene visualizzata la tua percentuale di **Utilizzo**
in un grafico di misurazione, con il piano che stai utilizzando.

Per visualizzare una panoramica del tuo utilizzo dal dashboard principale di {{site.data.keyword.prf_hubshort}}, fai clic sull'icona **Configura** ![Icona Configura](images/config_icn_white_smll.jpg). Se sei un utente del piano {{site.data.keyword.prf_hubshort}} Lite,
il tuo utilizzo viene visualizzato come un grafico a barre e come una percentuale, con il numero di test
in utilizzo. Se sei un utente del piano a Pagamento, il tuo utilizzo viene visualizzato in punti dati. Puoi visualizzare i dettagli di utilizzo per ogni singolo test nel riquadro Test sintetici.

Il tuo utilizzo viene misurato in punti dati. Il numero stimato di punti dati viene calcolato dalla
seguente formula:

Numero stimato di punti dati = T \* L \* (60/M \* 24 \* 30) al mese

Dove T = numero di test sintetici eseguiti, L = numero di ubicazioni e M = intervallo
tra i test (minuti).

I test semplici come i test pagina web e API REST utilizzano 1 punto dati per ogni test. I test avanzati
come gli script Selenium e API REST utilizzano 100 punti dati per ogni test.

Puoi visualizzare l'utilizzo effettivo sul Dashboard di utilizzo nella pagina Account {{site.data.keyword.Bluemix_notm}}. Fai clic su **Account**, quindi seleziona **Dashboard di utilizzo** e scorri fino alla sezione **Costi del servizio**. Fai clic sull'icona **Freccia** per il servizio
{{site.data.keyword.prf_hubshort}} per visualizzare quanti punti dati
hai utilizzato. Per ulteriori informazioni sui piani tariffari e di utilizzo di {{site.data.keyword.prf_hubshort}}, consulta i piani dei prezzi nella pagina del catalogo [Monitoraggio della disponibilità](https://console.{DomainName}/catalog/services/availability-monitoring/ "(Si apre in una nuova scheda o finestra)"){: new_window}.
