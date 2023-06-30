#   APPUNTI GENERALI TPSIT

## I SOCKET
I socket sono basati sul livello ISO/OSI livello 4 anche detto Trasporto, sono dei canali per far comunicare i processi tra due host.
I socket sono composti dall'IP del destinatario, l'IP sorgente, la porta del destinatario e la porta sorgente.

Esistono tre tipi di socket:
**-Datagram Socket:** che lavora sul protocollo di livello 4 UDP e quindi comunica in modo connectionless.
Visto che il datagram socket implementa il protocollo UDP ha la possibilità di comunicare anche in multicast, un metodo di comunicazione one-to-many.

{ collegare multicast con (sistemi e reti: DNS), DNS usa UDP e multicast. }

**-Stream Socket:** che lavora sul protocollo di livello 4 TCP e di conseguenza instaura una connessione prima di iniziare a comunicare 

**-Raw Socket:** è un socket che non implementa nessun protocollo ed è altamente personalizzabile.

Primitive:
I socket utilizzano delle primitive per funzionare come accept, listen, read, write, connect, close, ecc...

Server Socket:
Un server TCP mette a disposizione solitamente sulla porta 80 un server socket,
quando un client instaura una connessione con questo socket il server "sposterà" 
questa connessione su un'altra porta instanziando un secondo stream socket, lasciando
la porta iniziale libera cosicché altri client possano richiedere una connessione con il server.
Il primo socket che è sempre in ascolto è detto server socket mentre il canale di comunicazione è detto data socket.

{ collegare le porte usate dai socket con (sistemi e reti: porte) }


## HTTP/HTTPS:
Il protocollo HTTP è un protocollo che lavora al livello 7 della pila ISO/OSI detto anche Applicazione,
è basato sul protocollo TCP di livello 4 usando la porta 80 (HTTPS: 443).

{ collegare HTTPS con (sistemi e reti: crittografia) }

Versioni: 
 - 1.0: GET, HEAD, POST
 - 1.1: GET, POST, PUT, DELETE, HEAD, OPTION, TRACE

Header: 
 - HTTP Request:
GET /example/url HTTP/1.1
HOST: google.com

{/* body */}

HTTP Response:
 - HTTP/1.1 200 OK
Date: Thu, 09 Dec 2004 12:07:48 GMT
Cache-Control: s-maxage=60, stale-while-revalidate=600

{/* body */}


##  MODELLO CLIENT-SERVER
Il modello client server è un modello per costruire e organizzare applicazioni ed è organizzato a livelli.
I livelli o "tier" di questo modello sono:
 - data layer
 - buisness logic
 - user interface

Questo modello può essere organizzato in più architetture, come:

 **- one tier:** tutti i layer sono gestiti da una singola macchina (caso di terminali stupidi)
 
 **- thin two tier:** il server gestisce data layer e buisness logic (si, senza DB), il client gestise la user interface. (nessun caso fa cagr)
 
 **- thick tow tier:** il server gestisce solo il data layer, il client gestisce sia buisness logic che user interface. (caso angular, CSR)
 
 **- three tier:** il database gestisce il data layer, il server gestisce la buisness logic e il client gestisce la user interface. (caso php, SSR)

## XML & JSON
Serializzazione: rappresentazione di un dato in un certo formato.
XML: si utilizza tra aziende diverse, è presente un file di configurazione che definisce i campi dell'oggetto.
JSON: nella stezza azienda


## REST & SOAP:
REST e SOAP sono due modi con cui un web server può comunicare con un client.
REST utilizza lo standard JSON e tutti i metodi di HTTTP/1.1, mentre SOAP usa lo standard XML.
Visto che il modello SOAP utilizza XML per strutturare dati deve definire questa struttura con un'ulteriore
file WLSD tipico del formato XML.


## SISTEMI DISTRIBUITI:
I sistemi distribuiti sono applicazioni costituite da più processi, cooperanti ed eseguiti in parallelo, differenziandosi quindi dai sistemi centralizzati.
I sistemi distribuiti portano ad alcuni vantaggi e svantaggi:
 - Vantaggi: Economicità, Scalabilità, Affidabilità, Prestazione, Integrazione, Trasparenza, Apertura,
 - Svantaggi: Complessità, Sicurezza, Comunicazione

I sistemi distribuiti devono possedere almeno una delle seguenti caratteristiche:
 - Base di dati condivisa
 - Elaborazione distribuita

Nei sistemi distribuiti i vari processi svolgono uno o più ruoli ciascuno (se svolgono più ruoli vengono chiamati anche attori):
 - Client: colui che usufruisce di un servizio che viene offerto da un alttro processo
 - Server: colui che offre il servizio che viene sfruttato da altri processi

Tipologie di Sistemi distribuiti:
I sistemi distribuiti si suddividono in 3 categorie:

 **- Sistemi di calcolo:** <br>
	I sistemi di calcolo servono ad aumentare la potenza di calcolo di un sistema e si dividono in due sottocategorie: <br>
	*-Cluster:* Insieme di macchine omogenee che svolgono lo stesso compito per aumentare la potenza di calcolo.<br>
	 *-Grid:* Macchine non omogenee coordinate, ma hanno bisogno di un OS per coordinarsi (deve essere creato pk non esiste).

 **- Sistemi Informativi:** sistemi legacy ma ancora funzionali (???) (letteralmente tutto il resto).

 **- Sistemi Pervasivi:** sistemi di nuova generazione, solitamente wireless come smart watch o smart tv.


## Classificazione di Flynn:
I sistemi distribuiti possono essere categorizzati in molti modi, uno di questi è la classificazione di Flynn.
S: Single | M: Multiple | I: Instruction | D: Data

 **- SISD:** Macchina di Vonn Neumann che esegue una singola istruzione alla volta su un singolo dato (PC con CPU a 1 core).
 
 **- SIMD:** Macchina specializzata sull'eseguire un'istruzione su matrici di dati (GPU).
 
 **- MISD:** Esecuzione molte istruzioni su un singolo dato (Crittografia).
 
 **- MIMD:** Esecuzione di molte istruzioni su multipli dati (Database).<br>
			*- Multiprocessor:* La memoria è condivisa tra tutti i processori del sistema<br>
			*- Multicomputer:* La memoria non è condivisa quindi i dati devono essere trasmessi tramite messaggi tra processi.

## Architetture:
Le più importanti architetture di sistemi distribuiti sono:
###  Architettura a terminali remoti:
Il sistema è composto da una serie di terminali "stupidi" e un mainframe che esegue tutte le operazioni di calcolo.

### Architettura client-server:
Il sistema è composto da un server e uno o più client, il sevrer mette a disposizione un servizio e i client ne usufruiscono. (qualsiasi sito/web api)

 ###  Architettura WEB-centric:
Il sistema sposta parte significativa delle sue funzionalità sul WEB. (Google docs, Word online)

 ###  Architettura cooperativa:
è un evoluzione dell'architettura client-server, i server che offrono servizi utilizzano servizi a loro volta da altri server ulteriori.
	
 ###  Architettura completamente distribuita:
Anche detto Peer2Peer Architecture sono una serie di servizi offerti e sfruttati da molti attori in contemporanea, anche in modo ridondante. (emule, utorrent)


<br><br>

By: Alessandro Somigli💀, Leonardo Canu🐕, Enrico Marinelli👼.
