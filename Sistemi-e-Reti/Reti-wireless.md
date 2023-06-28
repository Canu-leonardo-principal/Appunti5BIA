# Reti wireless

## Introduzione
Le reti wireless possono utilizzare
onde radio o segnali infrarossi
per comunicare attraverso l’etere
e, così come le reti wired, possono
essere classificate in base all’estensione
dell’area fisica che sono in grado di coprire.

## WPAN 
- Zona di 10-15 metri
- Adatte a reti domestiche o piccoli uffici
- Utilizzano onde radio (Bluetooth) o segnali infrarossi
- Utilizzata per la domotica

## WLAN
- Simili alle tradizionali Lan Ethernet cablate
- Standard più diffusi IEEE 802.11
- Composte da Wireless Terminal (dispositivi con interfaccia 802.11) ed 
Access Point(fanno da bridge o gateway)

L’insieme formato dall’Access Point
e dalle stazioni poste
nella sua zona di copertura
è detto Basic Service Set (BSS),
ovvero insieme di servizi di base,
e costituisce una cella.

I parametri di configurazione di un Access Point in questa rete sono:
- SSID
- Potenza
- Canale
- Crittografia
- Incapsulamento
- NAT e DHCP

## WMAN 
Consentono di distribuire dati
su di un agglomerato di case
tramite una potente antenna.

### Il collegamento può essere:
- point-to-point, una coppia di bridge wireless collegati
alla rete aziendale e a un’antenna direzionale;
- point-to-multipoint, un’antenna centralizzata
omnidirezionale e una serie di antenne direzionali
puntate verso l’antenna centrale.

### La trasmissione può essere:
- Non-line-of-sight, su frequenze basse, utilizzata
in ambienti urbani; il range va dai 2 GHz agli 11 GHz
e il computer si connette alla rete WiMAX tramite piccole
antenne (dongle) portatili da collegare direttamente
al computer

- line-of-sight, su frequenze molto più alte, utilizzata
in aree dove la probabilità che il segnale venga
schermato sono molto basse; questa funziona
con frequenze vicine ai 60 Ghz ed è ideale per coprire
aree molto estese.

## WWAN 
- Offrono applicazioni mobili che coprono vaste aree,
come uno stato o un continente;

- Sono offerte a livello regionale e nazionale dai Wireless
Internet Service Providers (WISP) che garantiscono
la realizzazione di infrastrutture;

- Accordi di roaming permettono connettività globale.

## Sicurezza nelle reti wireless
### Possibili attacchi:

**sniffing**:
Attività di intercettazione passiva dei dati che transitano
in una rete. Usato per monitorare il traffico
o intercettazione fraudolenta di dati sensibili.
Efficaci meccanismi di crittografia consentono
di mantenere la segretezza dei dati.

**accesso non autorizzato**:
Accesso a una rete privata senza esplicita autorizzazione.
La tecnica più utilizzata è quella di servirsi di un Access
Point Rouge (APR) cioè un AP non autorizzato.
Per ostacolare l’accesso non autorizzato, è necessaria
l’autenticazione reciproca tra i WT e gli AP.

**sostituzione del SID (Security IDentifier):spoofing**:
Sostituzione del SID (identificativo univoco a cui vengono
associate delle autorizzazioni) posizionando un Wireless
Terminal Rouge tra un utente e un Access Point.
Per evitarlo, si può usare il protocollo SARP (Secure ARP),
che fornisce un tunnel protetto tra client e AP o router.

**attacco DoS**:
Attacchi brute force, oppure attacchi che utilizzano forti
segnali radio che si sovrappongono ai segnali della rete
rendendo inutilizzabili gli AP e i wireless terminal.
Per evitarli è possibile proteggere l’edificio dai segnali radio
esterni con barriere fisiche (finestre, vernici).

## CRITTOGRAFIA ANCHE QUI
4 tipi:
- WEP (Wired Equivalent Privacy)Crittografato il payload del frame da trasmettere con algoritmo a chiave
simmetrica RC4

- TKIP (Temporal Key Integrity Protocol) Si utilizza ancora RC4,
ma parte con chiave temporale rigenerata ad ogni pacchetto

- AES (Advanced Encryption Standard)  Indecifrabile grazie
all'utilizzo dell'algoritmo di crittografia a blocchi Rijndael

- WPA (Wi-Fi Protected Area)
Aggiornamento WEP dotato di distribuzione dinamica chiavi
ed autenticazione reciproca

## AUTENTICAZIONE
- Realizzata tramite il SSID, Access Point consente accesso
solo se SSID coincide con quello inviato dall'Access Point stesso

- Amministratore autorizza un elenco di indirizzi MAC, solo 
gli indirizzi appartenenti all'elenco vengono accettati dall'
Access Point

- Implementata con protocollo EAP (Extensible
Authentication Protocol) su parte wireless e parte
cablata, che utilizza
un server di autenticazione.


