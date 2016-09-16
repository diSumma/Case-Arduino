<style>
  .titolo{
    text-align:center;
    font-size:30px;
    color:white;
  }
</style>
<div class="titolo">
Case Arduino
</div>

1. [Introduzione](#introduzione)

  - [Informazioni sul progetto](#informazioni-sul-progetto)

  - [Abstract](#abstract)

  - [Scopo](#scopo)

1. [Analisi](#analisi)

  - [Analisi del dominio](#analisi-del-dominio)

  - [Analisi e specifica dei requisiti](#analisi-e-specifica-dei-requisiti)


## Introduzione

### Informazioni sul progetto


Scuola: SAMT - Scuola Arti e Mestieri Trevano

Sezione: Informatica

Matera: Progetti

Titolo del progetto: Arduino Case

Docenti responsabili: Luca Muggiasca & Adriano Barchi

Classe: I3AC

Anno scolastico: 2016/2017

Data di inizio: 09.09.2016

Data di consegna: 21.10.2016


### Abstract
<!--
_Do you need a coffee but you don't have with for buy it? Don't worry: with the new dispenser you can buy every type of coffee pod trought your account!
You just have to log in, add your credit to your account and you can buy coffee pod when you want, everywhere you are.
With the new dispenser you could buy coffee pod from your phone without go to the coffe maker !
What are you waiting for? Take your preferred coffee pod!_
-->
Hai bisogno di un case per proteggere al meglio il tuo Arduino? Questo è ciò che fa per te, protezione e comodità in una sola scatola

### Scopo

<!--
  Lo scopo del progetto (scopi didattici/scopi operativi). Dovrebbe
  descrivere il mandato, ma non vanno ricopiate le informazioni del
  quaderno dei compiti (che va invece allegato).
-->

  Lo scopo principale del progetto è quello di far capire all'alunno come si redige una documentazione, come si progetta e si crea un nuovo progetto.



  Questo sistema viene utilizzato principalmente da tre tipologie di utenti:
  - Amministratore: ha il pieno controllo del sistema
  - Responsabile: si occupa della gestione dei crediti e degli utenti
  - Utente generico: acquista le capsule e consulta il suo credito e storico
    degli acquisti

Vi è un sito del prodotto dove il cliente tramite la postazione fisica oppure
tramite un applicazione android può acquistare le capsule.
Il responsabile si collega al sito per visualizzare le statistiche riguardanti
gli utenti e le capsule e per ricaricare il saldo.

<!-- sezione non finita -->

## Analisi

### Analisi del dominio

<!--
  Questo capitolo dovrebbe descrivere il contesto in cui il prodotto verrà
  utilizzato, da questa analisi dovrebbero scaturire le risposte a quesiti
  quali ad esempio:

  -   Background/Situazione iniziale

  -   Quale è e come è organizzato il contesto in cui il prodotto dovrà
      funzionare?

  -   Come viene risolto attualmente il problema? Esiste già un prodotto
      simile?

  -   Chi sono gli utenti? Che bisogni hanno? Come e dove lavorano?

  -   Che competenze/conoscenze/cultura posseggono gli utenti in relazione
      con il problema?

  -   Esistono convenzioni/standard applicati nel dominio?

  -   Che conoscenze teoriche bisogna avere/acquisire per poter operare
      efficacemente nel dominio?

  -   …
-->
Al momento coloro che usufruiscono della macchinetta del caffé sono solo i docenti.
Non esiste nulla di simile al momento, chi vuole usare la macchinetta del caffé deve comprarsi le proprie capsule.
Per utilizzare questo prodotto non bisogna avere competenze particolari.


### Analisi e specifica dei requisiti


|ID |REQ-001                                       |
|---|------------------------------------------------|
|**Nome**    |Struttura hardware |
|**Priorità**|1                     |
|**Versione**|1.0                   |
|            |**Sotto requisiti** |
|**001**      |Deve essere modulabile.  |
|**002**      |Deve essere riempito con le capsule.|
|**003**      |Il ricaricamento deve essere facilitato, senza compromettere il funzionamento della struttura.                  |
|**004**      |Deve avere un metodo di espulsione delle capsule a dipendenza della scelta effettuata.|
|**006**      |Deve comunicare al server gli acquisti.|
|**007**      |Le capsule devono essere gestite da un servomotore controllato dall’Arduino.|


|ID |REQ-002                                       |
|---|------------------------------------------------|
|**Nome**    |Riconoscimento |
|**Priorità**|1                     |
|**Versione**|1.0                   |
|            |**Sotto requisiti** |
|**001**      |Deve essere presente un metodo di riconoscimento univoco dell’utente per chi vuole usufruire dell’apparecchio.  |
|**002**      |Bisogna avere una server dove memorizzare gli utenti.|
|**003**      |In caso di server down, bisogna avere un riconoscimento locale.                 |
|**004**      |In caso di server down, bisogna avere un metodo di memorizzazione temporaneo in locale.|

|ID |REQ-003                                       |
|---|--------------------------------------------------------|
|**Nome**    |Amministratore |
|**Priorità**|1                     |
|**Versione**|1.0                   |
|            |**Sotto requisiti** |
|**001**      |Amministratore gestisce il sito.  |
|**002**      |Deve poter dare permessi.|
|**003**      |Deve poter aggiungere i moduli.        |

|ID |REQ-004                                       |
|---|------------------------------------------------|
|**Nome**    |Responsabile |
|**Priorità**|1                     |
|**Versione**|1.0                   |
|            |**Sotto requisiti** |
|**001**      |Si preoccupa della gestione dei crediti di ogni singolo utente.  |
|**002**      |Ricaricare il distributore di capsule. |
|**003**      |Avere la possibilità di creare utenti.    |
|**004**      |Deve poter gestire gli utenti.|
|**005**      |Deve poter creare i grafici dei acquisti.|
|**006**      |Deve poter caricare credito agli utenti.|
|**007**      |Dovrà avere la possibilità di vedere le capsule vendute.|

|ID |REQ-005                                      |
|---|--------------------------------------------------------|
|**Nome**    |Utente comune |
|**Priorità**|1                     |
|**Versione**|1.0                   |
|            |**Sotto requisiti** |
|**001**      |Ogni utente deve poter consultare il proprio credito.  |
|**002**      |Ha a disposizione informazioni riguardanti i propri acquisti quali storico e quantità di capsule.|

|ID |REQ-006                                     |
|---|--------------------------------------------------------|
|**Nome**    |Raspberry |
|**Priorità**|1                     |
|**Versione**|1.0                   |
|            |**Sotto requisiti** |
|**001**      |Hosta un sito che permette la gestione del prodotto: utenti, capsule, configurazioni |
|**002**      |Comunica con altri dispositivi|
|**003**      |Comunica con componenti esterni|
