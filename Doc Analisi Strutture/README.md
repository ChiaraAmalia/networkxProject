# Social Network Analysis della serie Rick And Morty
<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/logo.png">
</p>

## 4 Analisi delle strutture
 In questa parte del progetto ci siamo concentrati sui sottografi presenti nella rete che potrebbero dare luogo a strutture quali le clique e le triadi, che sono note per la loro coesione e robustezza.
Abbiamo poi deciso di applicare il concetto di Ego Network ai due personaggi protagonisti della serie (come si può intuire dal nome della stessa, abbiamo scelto Rick e Morty) per farci un’idea del “vicinato” di tali perso-naggi e del loro campo di azione.

### 4.1	Triadi
Un insieme di tre nodi è quello che viene definita una triade e se tutti i nodi, di tale insieme, sono tra loro con-nessi, la triade è definita chiusa.
Si presta particolare attenzione alle triadi perché esse sono un sinonimo di stabilità per quel che riguarda la diffusione delle informazioni, se infatti si dovesse eliminare un arco da una triade chiusa tutti i suoi nodi sa-rebbero ancora in grado di comunicare, e quindi l’informazione riuscirebbe comunque a raggiungere tutti i nodi.  
Le triadi chiuse trovate sono state 801.
Abbiamo successivamente filtrato le triadi per prendere in considerazione solamente quelle che contenessero sia Rick che Morty e abbiamo così ridotto il numero a 32.

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_1.jpg">
</p>

### 4.2	Clique
Se si estende il concetto di triade chiusa a più di 3 nodi si parla allora di clique, essa è dunque un generico in-sieme di nodi totalmente connesso, e si può quindi assimilare ad un insieme di triadi tra loro sovrapposte.
Risultano di notevole importanza in quanto rappresentano la massima espressione di coesione tra i nodi di una rete.
Il numero di clique trovate è 6159 di cui 252 sono massimali.
Le clique massimali e massime (ovvero con il maggior numero di elementi) in questa rete sono composte da 10 elementi e sono 2.
Clique 1.
> ['Rick Sanchez', 'Morty Smith', 'Summer Smith', 'Beth Smith', 'Morty Jr.', "Rick's Father", 'Space Beth', 'Hemorrhage', 'Diane Sanchez', 'Sleepy Gary']

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_2.png">
</p>

Clique 2.	
> ['Rick Sanchez', 'Jerry Smith', 'Summer Smith', 'Beth Smith', 'Morty Jr.', 'Space Beth', "Rick's Father", 'Hemorrhage', 'Diane Sanchez', 'Sleepy Gary']

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap4_3.png">
</p>
