# Access List

## Cos'è un Access List?
Un ACL **è una serie di comandi** che vengono utilizzati per filtrare i pacchetti in base ad un controllo effettuato sull'header. Quando un ACL viene applicata a un adeterminata interfaccia, il router esegue l'attività di controllo per ogni pachhetto che passa per quell'interfaccia.<br>
Un ACL utilizza un elenco sequenziale di istruzioni autorizzate o negate, note come access control entries (ACE).<br>
Quando il traffico di rete passa attraverso un'interfaccia configurata con un ACL, il router confronta le informazioni all'interno del pacchetto con ogni ACE, *in ordine sequenziale*, per determinare se il pacchetto corrisponde a uno degli ACE. Questo processo è chiamato filtraggio pacchetti. <br>

Diverse attività eseguite dai router richiedono l'uso di ACL per identificare il traffico: 
- Limitare il traffico di rete per aumentare le prestazioni della rete
- Fornire il controllo del flusso di traffico
- Fornire un livello di sicurezza di base per l'accesso alla rete
- Filtrare il traffico in base al tipo di traffico
- Esaminare l'host per consentire o negare l'accesso ai servizi di rete
- Fornire priorità a determinate classi di traffico di rete

Prima di andare a dire i due tipi di ACL prncipali è giusto andare ad introdurre un'altra tipologia importante:
**-ACL Whitelist:** scrivi la gente che vuoi abbia accesso.
**-ACL Blacklist:** scrivi la gente che vuoi "bloccare"/filtrare, ed una regola in fondo che permette tutto il resto.


## Tipi di ACL
I router Cisco supportano due tipi di ACL:
- **ACL standard**: Gli ACL filtrano solo al livello 3 controllando solo l'indirizzo IPv4 di origine.
- **ACL estesi**: filtri al livello 3 che controllano sia l'indirizzo IPv4 di origine che quello di destinazione. Possono anche effettuare controlli al livello 4 controllando le
porte TCP, UDP.

## Funzionamento delle ACL
Gli ACL definiscono l'insieme di regole per eseguire un controllo aggiunto sui i pacchetti in entrata nelle interfacce in ingresso e i pacchetti in uscita dal il router.<br> 
Gli ACL possono essere configurati per essere applicati al traffico in ingresso e al traffico in uscita.<br>
Un ACL in ingresso filtra i pacchetti prima che vengano instradati verso l'interfaccia in uscita questo tipo di ACL è molto efficiente perché salva il sovraccarico del router.<br>
Un ACL in uscita filtra i pacchetti dopo essere stati instradati, indipendentemente dall'interfaccia in ingresso.<br>
Quando un ACL viene applicata a un'interfaccia, segue una procedura operativa ben specifica. Ecco i passaggi operativi utilizzati quando il traffico è entrata in un'interfaccia:
- router con un ACL IPv4 standard in ingresso configurato.
- Il router estrae l'indirizzo IPv4 di origine dall'intestazione del pacchetto.
- Il router inizia nella parte superiore dell'ACL e confronta l'indirizzo IPv4 di origine con ogni ACE in ordine sequenziale.
- Quando viene effettuata una corrispondenza, il router esegue l'istruzione, consentendo o negando il pacchetto, e gli ACE rimanenti nell'ACL, se presenti, non vengono analizzati.
- Se l'indirizzo IPv4 di origine non corrisponde ad alcun ACE nell'ACL, il pacchetto viene scartato perché è presente un ACE di negazione implicita applicato automaticamente a tutti gli ACL.

**!!!NOTA IMPORTANTE:!!!** L'ultima istruzione ACE di un ACL è sempre una negazione implicita che blocca tutto il
traffico. È nascosto e non visualizzato nella configurazione.

## La Maschera Jolly (wildcard)

Una maschera jolly è simile a una subnet mask in quanto utilizza il processo ANDing per identificare i bit di un indirizzo IPv4 da controllare. A differenza di una subnet mask, in cui binario 1 è uguale a una corrispondenza e binario 0 non è una corrispondenza, in una maschera jolly è vero il contrario.<br>
Un ACE IPv4 utilizza una maschera jolly a 32 bit per determinare quali bit dell'indirizzo esaminare.<br>
Le maschere jolly utilizzano le seguenti regole per abbinare 1 e 0:
- **Maschera jolly bit 0** - controlla il valore del bit corrispondente nell'indirizzo.
- **Maschera caratteri jolly bit 1** - Ignora il valore del bit corrispondente nell'indirizzo.

<br><br>
by ***Leonardo Canu*** *5BIA*
