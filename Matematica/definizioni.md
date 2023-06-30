# Definizioni un sacco utili

- ### Definizione di derivata
    La derivata di una funzione in un punto è il limite del rapporto incrementale al tendere dell'incremento h a zero. Il rapporto incrementale in un punto di una funzione è il rapporto tra la variazione di ordinate e la variazione di ascisse definite a partire da un incremento h.
  $$
      \frac{\Delta y}{\Delta x} := \frac{f(x_0 + h) - f(x_0)}{h}
  $$ 

- ### Significato geometrico e definizione di derivata
    - **Definizione**: descrive la pendenza di una funzione rispetto ad una variabile
    - **Funzione derivata**:  funzione che associa a ogni punto proprio la derivata in quel punto.
    - **significato geometrico**: è una retta che collega due punti, dove uno dei due tende all'altro, in questa maniera si riesce a vedere in maniera approssimata la tangente rispetto ad un punto specifico.

- ### Cosa è un integrale definito e perchè serve quello indefinita per calcolarlo?
    - ***primitiva***: la primitiva è una funzione la cui derivata è la funzione di partenza
    - ***integrale indefinito***: insieme di tutte le primitive di una funzione (da aggiungere sempre c) 
    - ***integrale definito***: area algebrica(può essere positiva o no) sottesa tra l'asse x e la funzione
    
    Quindi, in poche parole, l'integrale definito è un *area*, quello indefinito è *un'insieme di funzioni*.<br>
    Per calcolare un itegrale definito serve quello indefinito perchè si usa il teorema di Torricelli-Barrow.

- ### teorema di Torricelli-Barrow
Il teorema di Torricelli-Barrow afferma che se f(x) è una funzione continua su un intervallo [a, b] e F(x) è una sua primitiva, allora l'integrale definito della funzione f(x) su quell'intervallo può essere calcolato come la differenza tra i valori di F(x) in corrispondenza degli estremi dell'intervallo. In altre parole, se F(x) è una primitiva di f(x), allora vale la seguente relazione:  $\int_{a}^{b}$ f(x) dx = F(b) - F(a). Dove $\int_{}^{}$ indica l'integrale definito e dx rappresenta l'elemento infinitesimo della variabile x.

- ### cosa è un'equazione differenziale? Quali tipi abbiamo affrontato?
    - ***equazione differenziale***: è una funzione la cue incognita è una funzione e l'equazione consiste in una ralazione tra l'incognita e le sue derivate 
    - ***edolcc e compagnia varia***: equadione differenziale ordinaria lineari coefficenti costanti
    - ***ordinaria***: quando la funzione incognita dipende da una sola variabile
    - ***lineari***: l'incognita e le sue derivate compaiono solo alla prima potenza e non moltiplicate 


- ### cosa è un termine forzante, come si riconosce e cosa la differenza tra equazione differenziale ompogenea e non ompogenea
    - ***termine forzante o termine non omogeneo***: termine nel quale la funzione o le sue derivate non sono presenti.
    - ***equazione differenziale omogenea***: equazione differenziale nella quale non è presente il termine forzante.
    - ***equazione differenziale non omogenea***: equazione differenziale nella quale è presente almeno un termine forzante.

- ### applicazioni delle differenziali
***Dinamica di un oggetto in caduta libera***:  Possiamo utilizzare un'equazione differenziale per descrivere il moto dell'oggetto. Ad esempio, l'equazione differenziale potrebbe essere: m * a = m * g, dove m è la massa dell'oggetto, a è l'accelerazione e g è l'accelerazione di gravità.*Risolvendo questa equazione differenziale, possiamo ottenere la funzione della posizione rispetto al tempo*.

***Circuiti RC***: Le equazioni differenziali vengono spesso utilizzate per analizzare il comportamento dei circuiti. Ad esempio, consideriamo un circuito RC semplice composto da un resistore (R) e un condensatore (C) collegati in serie. Possiamo utilizzare l'equazione differenziale: Q' = -1/RC * Q, dove Q rappresenta la carica accumulata nel condensatore e Q' rappresenta la derivata rispetto al tempo di Q. *Risolvendo questa equazione differenziale, possiamo determinare come la carica sul condensatore varia nel tempo*.

***Propagazione del calore***: Le equazioni differenziali sono ampiamente utilizzate per descrivere la diffusione del calore in vari materiali. Ad esempio, l'equazione del calore può essere utilizzata per descrivere come la temperatura in un oggetto varia nel tempo. Questa equazione differenziale può includere termini come il flusso di calore e la conducibilità termica del materiale. *Risolvendo questa equazione, possiamo ottenere una soluzione che descrive l'evoluzione della temperatura nel tempo e nello spazio*.

***Crescita di una popolazione***: Le equazioni differenziali possono anche essere utilizzate per modellare la crescita di una popolazione nel tempo.  L'equazione differenziale associata a questo modello può essere scritta come: dP/dt = r * P * (1 - P/K), dove P rappresenta la popolazione, t è il tempo, r è il tasso di crescita e K è la capacità di carico dell'ambiente. *Risolvendo questa equazione differenziale, possiamo ottenere un'idea di come la popolazione cambia nel tempo*. 

- ### parlare di distribuzioni(tipo calcolo della fila rimanente)
In generale, una distribuzione può essere vista come un'applicazione lineare definita su uno spazio di funzioni test, che sono funzioni di prova lisce e a supporto compatto. Le distribuzioni sono definite tramite la loro azione su queste funzioni test, che fornisce un valore numerico.

by ***Leonardo Canu*** *5B-IA*
feat. Gioele Falaschi, Enrico Marinelli, Alessandro Somigli (Gioele Failing, Enrcore Math, Algorithms Software).
