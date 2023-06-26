# Le VPN (Virtual Private Network)
## Introduzione
Per un’azienda con varie sedi, dislocate anche a grande distanza tra loro, l’ideale sarebbe trattare l’intero gruppo come un’unica rete locale aziendale, realizzando una WAN privata per il proprio business.<br>
Mediante la realizzazione delle reti private, ogni LAN non è più isola in mezzo all’oceano (Internet) ma si collega con le altre isole per costituire un arcipelago (WAN) avente regole comuni e condivise.

**Le reti private** “vere e proprie” collegano più siti di una rete aziendale
attraverso canali dedicati, a uso esclusivo, pagandone l’affitto al
proprietario o al gestore.

|PRO|CONTRO|
|---|---|
|larghezza di banda sempre disponibile|alti costi di installazione|
|nessun problema di accesso|ricorrenti costi di manutenzione|
|nessuna congestione del traffico a livello di rete|lunghi tempi per la configurazione e riconfigurazione|
|prestazioni garantite|mancanza di scalabilità|
|sicurezza garantita|rischio di blocco della rete in caso di grave guasto su un canale (non c’è ridondanza)|

## Virtual Private Network

Pertanto, per garantire l’efficienza della rete e un buon rapporto costi/benefici (punti deboli delle reti private), si ricorre alle **reti private virtuali**:
contrariamente alle normali reti private, sono configurabili e riconfigurabili rapidamente e facilmente, sono scalabili e offrono un valido rapporto costi/funzionalità. Una Virtual Private Network è una rete creata all’interno di un’infrastruttura di rete pubblica, per esempio Internet. All’interno di una stessa VPN l’indirizzamento deve essere univoco. Il rischio di blocco di un VPN è pressoché nullo, dato che si utilizza una rete pubblica che garantisce un altro grado di ridondanza.
<br><br>
In commercio esistono due principali tipi di VPN:
- **remote-access VPN**: porta praticamente qualsiasi applicazione  emulando il desktop dell’ufficio.
- **site-to-site VPN**:  consente alle aziende di ampliare le risorse di rete alle filiali, agli uffici domestici e ai siti dei partner.

## Remote-access VPN
Gli utenti che utilizzano una **Remote-access VPN** possono accedere dalla rete locale come se fossero direttamente collegati ai server della rete della propria azienda. Neccessitano però di 2 componenti indispensabili:
- *Network Access Server*
    - è un server che permette l’accesso alla rete.
    - può essere un server dedicato oppure un’applicazione software in esecuzione su un  server condiviso.
    - richiede credenziali valide per accedere, utilizzando un proprio processo di autenticazione.
    - fornisce Authentication, Authorization e Accounting. :)
- *sfotware VPN client*
    - software pensato ad hoc necessario per stabilire e mantenere una connessione alla rete VPN.
    - è necessario anche un firewall che fornisca una barriera.

## Site-to-site VPN
Una site-to-site VPN permette, anche ad aziende con tante reti LAN, di stabilire connessioni sicure attraverso una rete pubblica. Con la site-to-site VPN la rete aziendale viene estesa rendendo disponibili alle sedi secondarie dell’azienda le risorse della sede principale.<br>
Ci sono due tipi di site-to-site VPN:
- **Intranet-based**: una VPN intranet per collegare ogni LAN separata di una singola rete WAN. 
- **Extranet-based**: una VPN extranet che collega le LAN di diverse imprese.

## Tre grossi problemi delle VPN
La natura condivisa delle VPN implica dover affrontare tre grossi problemi:
- variabilità del **tempo** di trasferimento
- controllo degli **accessi** (autenticazione)
    - Le reti VPN sono reti private, dunque per potervi accedere occorre autenticarsi.
    Il primo passo per accedere alla rete occorre autenticarsi attraverso un login, costituito da username e password.
- **sicurezza** delle trasmissioni (cifratura e tunneling)
    - Le VPN utilizzano un’ampia gamma di algoritmi di crittografia (3-DES, CAST, IDEA ecc.) per cifrare il traffico in rete. Sia l’algoritmo da usarsi sia le chiavi segrete che l’algoritmo stesso utilizza sono concordate e scambiate tra mittente e destinatario attraverso protocolli di sicurezza. Nello specifico caso delle reti VPN,viene soprattutto utilizzato il protocollo **Internet Key Exchange (IKE)**, il cui compito principale è proprio implementare lo “scambio delle chiavi” per cifrare i pacchetti.
    - Lo scopo dei protocolli di tunneling è aggiungere un livello di sicurezza al fine di proteggere ogni pacchetto nel suo “viaggio” su Internet. *E' il processo di immissione di un intero pacchetto all’interno di un altro pacchetto prima di essere trasportato su Internet*. Il pacchetto esterno protegge il contenuto dalla vista del pubblico e assicura che il pacchetto si muova all’interno di un tunnel virtuale. Tale stratificazione viene chiamata *incapsulamento*.

- Le VPN possono essere realizzate in:
    - *modalità trasporto*: in questo caso i software impiegati ricoprono un ruolo fondamentale. 
    - *modalità tunnel*: in questo caso sono gli apparati, in particolare router e firewall, a ricoprire un ruolo fondamentale.

## Classificazione VPN
Le reti VPN possono essere classificate in base ai protocolli che utilizzano e al
grado di sicurezza che garantiscono, in tre categorie:
- **Trusted VPN**: si affida molto al proprio Internet Service Provider
    - non utilizzano protocolli che permettano la cifratura e il conseguente tunneling dei dati trasmessi, pertanto la riservatezza dei dati è controllata dall'ISP.
    - L’ISP assicura una qualità del servizio garantendo che nessun altro possa usufruire del canale assegnato a una determinata VPN in un determinato momento.
    - L’ISP si fa carico anche della configurazione e della responsabilità dei dati e della progettazione della rete VPN richiesta dall’azienda.
- **Secure VPN**: si affida molto ai protocolli per la sicurezza
    - Le Secure VPN utilizzano protocolli che consentono la cifratura e il tunneling, utilizzano uno o più tunnel, ognino dei quali da soltanto 2 estremità.
    - Garantiscono quindi:
        - un sistema di autenticazione;
        - che i dati viaggino criptati;
        - che il livello di cripting dei dati sia elevato e modificabile nel tempo.
- **Hybrid VPN**: si affida tanto all’ISP quanto ai protocolli per la sicurezza
    - Lo scenario tipico è quello di un’azienda che ha già una Trusted VPN e desidera sicurezza su una parte della VPN e dunque crea una Hybrid VPN.

## Protocolli VPN
I principali protocolli per la sicurezza sono IPsec, SSL/TLS e BGP/MPLS (*Ancora non fatto*)

### IPsec
E' un gruppo di protocolli che garantisce autenticazione, segretezza, integrità:
- **IKE(Internet Key Exchange)**: Implementa autenticazione e scambio delle chiavi per realizzare il flusso crittografato
- **AH(Authentication Header)**: Garantisce l'autenticazione e l'integrità del messaggio, ma non offre la confidenzialità. Autentica l'intero pacchetto IP a eccezione dei campi variabili nell'header
- **ESP(Encapsulating Security Payload)**: Fornisce autenticazione, segretezza ed integrità del messaggio
AH e ESP sono alternativi, si possono utilizzare o uno o l'altro dal momento che la confidenzialità è un fattore critico nelle VPN, infatti viene utilizzato di più ESP
#### IKE
IKE è un protocollo di livello 7 ed opera sulla porta UDP 500; agisce in due fasi:
1. Inizialmente i due capi si autenticano con lo scambio delle chiavi. Appena si conclude viene condivisa una chiave segreta simmetrica per cifrare le comunicazioni successive
2. Viene stabilita una SA(Security Association) comune che permette di condividere i meccanismi di sicurezza da utilizzare
*Abbiamo detto che IKE utilizza UDP, tuttavia sfrutta un servizio affidabile, quando non riceve risposta, ritrasmette*
L'SA contiene i seguenti elementi:
- IP di destinazione
- Il protocollo IPsec utilizzato
- SPI(Security Parameter Index): specifica il protocollo di hashing
Le SA sono unidirezionali, quindi ci devono essere due SA per garantire la comunicaziuone tra due host. Quando sono attive su un host sono condivise su un database detto SA Database o SAD. Inoltre è presente un'ulteriore database, detto SPD che contiene le politiche di sicurezza. Con questi due strumenti riusciamo a decidere se dobbiamo scartare un pacchetto, elaborarlo tramite IPsec o se lasciarlo passare.

#### AH
Oltre a ciò scritto prima, AH garantisce anche la difesa da attacchi di tipo replay. Nelle modalità tunnel l'intero pacchetto originale viene incapsulato in un nuovo pacchetto, venendo quindi autenticato. Il campo dell'header AH prende il nome di SPI.

#### ESP
Pure questo protegge da attacchi di tipo replay. La differenza con AH sta nel fatto che l'autenticazione non copre anche l'header IP esterno. Aggiunge un header e un trailer perché incapsula tutti i dati che protegge. Anche nell'header ESP è presente il campo SPI, in più è presente un campo authentication che contiene i dati per autenticare il pacchetto.
Nella modalità tunnel il pacchetto viene completamente cifrato con algoritmo e chiave stabiliti da IKE

### SSL/TLS
E' un protocollo che opera al di sopra del livello TCP e deriva dal protocollo SSL. SSL/TLS è composto da due livelli:
1. Record Protocol: Livello 4, crea i pacchetti dei dati di applicazione con cifratura simmetrica ed integrità. I pacchetti saranno incapsulati in TCP
2. Handshake Protocol: Livello 7, si occupa della fase di negoziazione. E' necessario stabilire una chiave di sessione per cifrare la comunicazione
SSL/TLS è un semplice protocollo client-server che ha lo scopo di autenticare il server da parte del client; opzionalmente anche il contrario. TLS fornisce l'autenticazione tramite certificati digitali detti CA(Certification Authority).
La fase di record non fa altro che applicare le operazioni negoziate e frammenta i pacchetti; opzionalmente li comprime.
### TLS vs IPsec
SSL/TLS consente l'autenticazione asimmetrica, autenticare il server senza autenticare il client, mentre IKE di IPsec costringe l'autenticazione reciproca.
SSL/TLS protegge la comunicazione tra applicazioni, IPsec rende sicuro il traffico tra host o tra intere sottoreti.
IPsec protegge tutto ciò che sta sopra IP, mentre SSL/TLS funziona solo per proteggere il traffico TCP






![Ale144p](https://github.com/Canu-leonardo-principal/Appunti5BIA/assets/94641181/e252d7ca-ff7a-4273-b3b7-7f53c0c91c8e)
<br><br>
by ***Leonardo Canu*** & ***Gioele Falaschi*** *5B-IA*
feat ***Davide Cazzato***
