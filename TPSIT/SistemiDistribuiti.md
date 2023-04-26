# **Sistemi Distribuiti**
### **Differenza Tra sistemi centralizzati e sistemi distribuiti**
Nei **sistemi centralizzati** le applicazioni girano in un singolo processore o comunque un solo host.
Nei **sistemi distribuiti** le applicazioni sono costituite da più processi, cooperanti, eseguiti in parallelo su un insieme di unità di elaborazione autonome: sono quindi sistemi ottenuti dall'aggregazione di singole CPU.
### **Caratteristiche Sistemi Distribuiti**
Per essere definiti tali, i sistemi distribuiti devono possedere le seguenti caratteristiche:
- Elaborazione distribuita
- Base di dati distribuita

Distribuita in questo contesto significa su più host

### **Ruoli Applicazioni**
Alle applicazioni nei sistemi vengono dati dei nomi che eseguono specifici ruoli:
- Il **Client** è l'utilizzatore di servizi messi a disposizione da altre applicazioni
- Il **Server** è il fornitore di servizi usati da altre applicazioni
- L'**Attore** a seconda del contesto del sistema assume sia il ruolo di client che di server. Un esempio può essere *Booking.com*; quando entriamo nel sito richiediamo dei confronti con altri hotel, di conseguenza *Booking.com* diventa client per cercare le offerte migliori e proporle a noi come server

### **Tipologie Sistemi Distribuiti**
**Sistemi di calcolo:**
- **Cluster**: Insieme di computer omogenei grazie ad una rete allo scopo di parallelizzare l'elaborazione. Un esempio è il mining di cripto valute
>*Vantaggio*: La cooperazione viene gestita da dei sistemi operativi specifici già esistenti<br>
>*Svantaggio*: Se esigiamo delle performance maggiori, c'è la necessità di cambiare tutti i dispositivi, comportando dei costi molto alti
- **Grid**: La cooperazione può essere effettuata anche da computer eterogenei, in questo caso però non è presente un SO che gestisce la distribuzione
>*Vantaggio*: Se vogliamo aumentare le performance della distribuzione non abbiamo bisogno di cambiare tutti i dispositivi<br>
>*Svantaggio*: Non esistono sistemi operativi specifici per la distribuzione, di conseguenza devono essere creati dagli utenti

**Sistemi di informativi:**
Sistemi che integrano sistemi legacy, molto vecchi ma ancora funzionali, con nuove tecnologie. L'esempio d'eccellenza è il Web

**Sistemi pervasivi:**
Nuova generazione di sistemi che hanno tipicamente connessioni wireless che possono servire anche a monitorare la salute in vari aspetti. Degli esempi sono smartwatch e holter cardiaci

### **Classificazione di Flynn**
- **SISD**: Singola Istruzione su singolo dato(Macchina Von Neumann)
- **SIMD**: Singola Istruzione su multipli dati(Scheda Video)
- **MISD**: Multiple Istruzioni su singolo dato(Crittografia)
- **MIMD**: Multiple Istruzioni su multipli dati(Database)
  che si possono suddividere in:
  - **Multiprocessor**: *è presente una memoria soltanto*, condivisa totalmente o parzialmente da tutti i processori.
  - **Multicomputer**: non hanno una memoria condivisa, quindi la condivisione dei dati avviene tramite dei messaggi, effettuati grazie alle procedure di *send* e *recive*.

### **Architetture**
**Architettura WEB-centric**
Sistemi che virano verso la centralità del web rimuovendo sempre più operazioni da eseguire ai client. Degli esempi possono essere il registro elettronico e Google Docs

**Architettura cooperativa**
Viene utilizzato il principio di incapsulamento della programmazione a oggetti per abbattere le differenze tra i prodotti usati nell'infrastruttura hardware, software, di programmazione e di rete di un *sistema distribuito*

**Architettura completamente distribuita**
E' un tipo di architettura in opposizione alla WEB-centric. Gruppi di computer collaborano richiedendo e offrendo servizi spesso ridondati

**Architettura a livelli**
In questa architettura vengono introdotte le applicazioni multilivello, nelle quali avviene la separazione delle funzionalità logiche del software in più livelli.
Si introducono gli strumenti di middleware; troviamo diverse funzionalità:
- Servizi di astrazione e cooperazione
- Servizi per le applicazioni
- Servizi di amministrazione del sistema
- Il Servizio di comunicazione
- L'ambiente di sviluppo applicativo
<br><br>
by **Gioele Falachi** *5B-IA*
