# Social Network Analysis della serie Rick And Morty
<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/logo.png">
</p>

## 4 Analisi delle strutture
 In questa parte del progetto ci siamo concentrati sui sottografi presenti nella rete che potrebbero dare luogo a strutture quali le clique e le triadi, che sono note per la loro coesione e robustezza.
Abbiamo poi deciso di applicare il concetto di Ego Network ai due personaggi protagonisti della serie (come si può intuire dal nome della stessa, abbiamo scelto Rick e Morty) per farci un’idea del “vicinato” di tali personaggi e del loro campo di azione.

### 4.1	Triadi
Un insieme di tre nodi è quello che viene definita una triade e se tutti i nodi, di tale insieme, sono tra loro con-nessi, la triade è definita chiusa.
Si presta particolare attenzione alle triadi perché esse sono un sinonimo di stabilità per quel che riguarda la diffusione delle informazioni, se infatti si dovesse eliminare un arco da una triade chiusa tutti i suoi nodi sa-rebbero ancora in grado di comunicare, e quindi l’informazione riuscirebbe comunque a raggiungere tutti i nodi.  
Le triadi chiuse trovate sono state 801.
Abbiamo successivamente filtrato le triadi per prendere in considerazione solamente quelle che contenessero sia Rick che Morty e abbiamo così ridotto il numero a 32.

<p align="center">
  <img height=300 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_1.jpg">
</p>

### 4.2	Clique
Se si estende il concetto di triade chiusa a più di 3 nodi si parla allora di clique, essa è dunque un generico in-sieme di nodi totalmente connesso, e si può quindi assimilare ad un insieme di triadi tra loro sovrapposte.
Risultano di notevole importanza in quanto rappresentano la massima espressione di coesione tra i nodi di una rete.
Il numero di clique trovate è 6159 di cui 252 sono massimali.
Le clique massimali e massime (ovvero con il maggior numero di elementi) in questa rete sono composte da 10 elementi e sono 2.
Clique 1.
> ['Rick Sanchez', 'Morty Smith', 'Summer Smith', 'Beth Smith', 'Morty Jr.', "Rick's Father", 'Space Beth', 'Hemorrhage', 'Diane Sanchez', 'Sleepy Gary']

<p align="center">
  <img height=500 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_2.png">
</p>

Clique 2.	
> ['Rick Sanchez', 'Jerry Smith', 'Summer Smith', 'Beth Smith', 'Morty Jr.', 'Space Beth', "Rick's Father", 'Hemorrhage', 'Diane Sanchez', 'Sleepy Gary']

<p align="center">
  <img height=500 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_3.png">
</p>

È possibile notare che le due cliques in questione è costituita essenzialmente dai membri della famiglia di Rick Sanchez. Saltano all’occhio due personaggi che non sono della famiglia in senso stretto e sono Hemorrhage e Sleepy Gary, dei quali però il primo istaura legami di parentela con tutta la famiglia a seguito del matrimonio con Summer Smith nel secondo episodio della terza stagione e il secondo invece instaura legami con tutta la famiglia in quanto alieno parassita che vuole convincere tutti di essere parte delle loro vite.

### 4.3	K-core
Rilassando il concetto di clique, consentendo ad un nodo di unirisi al gruppo se è connesso a k nodi, indipen-dentemente da quanti sono i nodi a cui esso non è connesso, si arriva alla definizione di k-core.
Al variare della dimesione di k, ovviamente anche le strutture che risultano sono differenti.
Sostanzialmente un k-core è un gruppo massimale di nodi ciascuno dei quali connessi ad almeno k altri nodi del gruppo.
Il sottografo nella figura sotto è stato calcolato per mezzo del metodo k_core(), al quale non è stato passato il pa-rametro k al fine di ottenere il “main-core” del grafo di partenza.
Il numero dei nodi appartenenti a questo k-core è 17 e il valore di k è pari a 11. Se si presta attenzione ai nodi di tale grafo si può notare che tali nodi sono quelli delle clique massime con l’aggiunta di altri 6 nodi.
I nodi in più rispetto alle cliques sono: ['Jerry Smith (C-131)', 'Unnamed Uncle', 'Leonard Smith', 'Joyce Smith', 'Naruto Smith', 'Gwendolyn'].
Si ha un numero maggiore di nodi in quanto nei k-core, non c’è più il vincolo di connessione diretta a ciascun altro nodo, dunque, il percorso tra due nodi qualsiasi può comprendere più di un arco.

<p align="center">
  <img height=500 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_4.png">
</p>

I nodi in più rispetto alle cliques, rappresentano dei personaggi che possono comunque essere considerati del-la famiglia di Rick Sanchez ma in un senso più esteso e soprattutto sono personaggi che nella serie compaiono poche volte, non rendendoli fondamentali e legati con tutti gli altri delle cliques.

### 4.4	Ego Network
Una Ego Network altro non è che una sottorete, ma centrata un uno specifico nodo, ed è di notevole impor-tanza per avere maggiori informazioni sul nodo centrale, in quanto vedendo i vicini di tale nodo si possono ri-cavare informazioni che altrimenti non si avrebbero.
Formalmente la struttura di una Ego Network si basa sul concetto di omofilia, ovvero la tendenza delle perso-ne di circondarsi di quelle a loro più simili.
Per fare ciò ci siamo serviti del metodo ego_graph(), messo a disposizione da NetworkX.
#### 4.4.1	Rick
Si è proceduto costruendo l’ego network relativa al personaggio di Rick, e successivamente si è analizzata la rete risultante.

<p align="center">
  <img height=500 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_5.png">
</p>

Osservando l’ego-network riportata nella Figura sopra, emerge un aspetto particolare, ovvero la presenza di due regioni con caratteristiche assai differenti.
Nell’area in basso, si può vedere che i vicini del nodo “ego” presentano molte connessioni reciproche, for-mando una struttura alquanto fitta nella quale sicuramente le informazioni transitano in maniera più efficien-te. Questa regione è caratterizzata dai membri della famiglia, intesa in senso ampio.
Invece nella parte in alto, è visibile come i vicini di Rick Sanchez (che non fanno parte della famiglia), non siano propensi ad essere connessi tra loro, probabilmente perché provenienti da dimensioni differenti, domina dun-que l’ego e le sembianze sono quelle di una rete a stella, e Rick funge da “intermediatore” in quanto può viag-giare attraverso le dimensioni tramite la sua spara-porte.

### 4.4.2	Morty
Si è proceduto costruendo l’ego network relativa al personaggio di Rick, e successivamente si è analizzata la rete risultante.

<p align="center">
  <img height=500 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_6.png">
</p>

Osservando l’ego-network riportata nella figura sopra, emerge un aspetto particolare, ovvero la presenza di due regioni con caratteristiche assai differenti.
Nell’area in basso, si può vedere che i vicini del nodo “ego” presentano molte connessioni reciproche, formando una struttura alquanto fitta nella quale sicuramente le informazioni transitano in maniera più efficiente. Questa regione è caratterizzata dai membri della famiglia, intesa in senso ampio.
Si può notare come la parte densa sia alquanto similare a quella della ego network di Rick Sanchez.
Invece nella parte in alto, è visibile come i vicini di Morty Smith (che non fanno parte della famiglia), non siano propensi ad essere connessi tra loro. Questa parte è costituita prettamente dalle ex-fidanzate o interessi amorosi del nodo centrale.


- [Capitolo 1: Introduzione](../README.md)
- [Capitolo 2: Analisi Descrittiva](../Doc%20Analisi%20Descrittiva/README.md)
- [Capitolo 3: Analisi delle Centralità](../Doc%20Analisi%20Centralità/README.md)
- [Capitolo 5: Group Centrality](../Doc%20Group%20Centrality/README.md)

