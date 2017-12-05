---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Blocco e filtro con la whitelist e la blacklist
{: #avmon_filters}

Utilizza la whitelist e la blacklist per determinare a quali risorse inviare le richieste e quali risorse contribuiscono alle metriche e allo stato dei test dell'applicazione. Le whitelist e le blacklist sono disponibili solo per i test delle pagine web e del funzionamento con script.
{: shortdesc}

I campi **Whitelist** e **Blacklist** definiscono le risorse a cui il test può o non può accedere e le risorse che contribuiscono alle metriche e allo stato dei tuoi test. La Whitelist e la Blacklist possono controllare quali dipendenze e risorse contribuiscono ai tempi di risposta delle tue applicazioni web testate, come le metriche di terze parti. Puoi configurare le tue Whitelist e Blacklist quando crei un test della pagina web o del funzionamento con script.

Puoi utilizzare la **Whitelist** per definire i domini e gli URL consentiti e puoi quindi utilizzare la **Blacklist** per bloccare specifici elementi delle tue ubicazioni consentite.

## Sintassi

Utilizza le virgole (,) per separare le voci nella blacklist e whitelist. Utilizza il carattere jolly (\*) per filtrare gli elementi di ogni URL o dominio.

## Whitelist

Aggiungi gli URL o i domini che vuoi includere nei calcoli di richieste e metriche al campo Whitelist. Nella tua Whitelist puoi elencare un massimo di 10 voci. Ogni voce non può contenere più di 200 caratteri. Tutti i domini e gli URL che non corrispondono alle voci presenti nella tua whitelist vengono bloccati.

Ad esempio:
```
ibm.com, *developerworks*, *.s81c.com/*
```
{: codeblock}

## Blacklist

Aggiungi gli URL o i domini che vuoi escludere dai calcoli di richieste e metriche al campo Blacklist. Nella tua Blacklist puoi elencare un massimo di 20 voci. Ogni voce non può contenere più di 200 caratteri. 

Ad esempio:
```
*.profile.*.cloudfront.net/*.png
```
{: codeblock}

## Funzionamento di filtro e blocco

I test possono avere sia una whitelist che una blacklist. Quando si determinano le ubicazioni consentite o bloccate, la blacklist sovrascrive sempre la whitelist. La seguente tabella mostra il funzionamento di filtro e blocco per tutti gli scenari che riguardano la whitelist e la blacklist.

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>Tabella 1. Funzionamento di filtro e blocco per la whitelist e la blacklist</caption>
<thead>
<tr>
<th>Blacklist</th>
<th>Whitelist</th>
<th>Funzionamento</th>
<th>Motivo</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vuota</td>
<td>Vuota</td>
<td>Consenti accesso </td>
<td>Nessuna regola di filtro immessa.</td>
</tr>
<tr>
<td>Vuota</td>
<td>L'URL non corrisponde alla voce dell'elenco</td>
<td>Blocca accesso</td>
<td>L'URL non è presente nella whitelist.</td>
</tr>
<tr>
<td>Vuota</td>
<td>L'URL corrisponde alla voce dell'elenco</td>
<td>Consenti accesso </td>
<td>L'URL è presente nella whitelist. Nessuna voce della blacklist per bloccare l'accesso.</td>
</tr>
<tr>
<td>L'URL non corrisponde alla voce dell'elenco</td>
<td>Vuota</td>
<td>Consenti accesso </td>
<td>L'URL non è presente nella blacklist. Nessuna voce della whitelist per bloccare l'accesso.</td>
</tr>
<tr>
<td>L'URL corrisponde alla voce dell'elenco</td>
<td>Vuota</td>
<td>Blocca accesso</td>
<td>L'URL è presente nella blacklist.</td>
</tr>
<tr>
<td>L'URL non corrisponde alla voce dell'elenco</td>
<td>L'URL non corrisponde alla voce dell'elenco</td>
<td>Blocca accesso</td>
<td>L'URL non è presente nella whitelist.</td>
</tr>
<tr>
<td>L'URL non corrisponde alla voce dell'elenco</td>
<td>L'URL corrisponde alla voce dell'elenco</td>
<td>Consenti accesso </td>
<td>L'URL è presente nella whitelist. L'URL non è presente nella blacklist. </td>
</tr>
<tr>
<td>L'URL corrisponde alla voce dell'elenco</td>
<td>L'URL non corrisponde alla voce dell'elenco</td>
<td>Blocca accesso</td>
<td>L'URL non è presente nella whitelist. L'URL è presente nella blacklist.</td>
</tr>
<tr>
<td>L'URL corrisponde alla voce dell'elenco</td>
<td>L'URL corrisponde alla voce dell'elenco</td>
<td>Blocca accesso</td>
<td>L'URL è presente nella blacklist. La voce della blacklist sovrascrive la voce della whitelist.</td>
</tr>
</tbody>
</table>
