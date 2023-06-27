Point Rouge (APR) cioè un AP non autorizzato.
Per ostacolare l’accesso non autorizzato, è necessaria
l’autenticazione reciproca tra i WT e gli AP.

**sostituzione del SID (Security IDentifier):spoofing**
Sostituzione del SID (identificativo univoco a cui vengono
associate delle autorizzazioni) posizionando un Wireless
Terminal Rouge tra un utente e un Access Point.
Per evitarlo, si può usare il protocollo SARP (Secure ARP),
che fornisce un tunnel protetto tra client e AP o router.

**attacco DoS**
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
all'utilizzo dell'algoritmo di crittografia a blocci Rijndael

- WPA (Wi-Fi Protected Area)
Aggiornamento WEP dotato di distribuzione dinamica chiavi
ed autenticazione reciproca

## AUTENTICAZIONE
- Realizzata tramite il SSID, Access Point consente accesso
solo se SSID conicinde con quello inviato dall'Access Poit stesso

- Amministratore autorizza un elenco di indirizzi MAC, solo 
gli indirizzi appartenenti all'elenco vengono accettati dall'
Access Point

- Implementata con protocollo EAP (Extensible
Authentication Protocol) su parte wireless e parte
cablata, che utilizza
un server di autenticazione.
