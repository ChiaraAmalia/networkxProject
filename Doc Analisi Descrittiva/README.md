# Social Network Analysis della serie Rick And Morty
<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/logo.png">
</p>

## 2 Analisi descrittiva
In questo capitolo, verrà fornito un resoconto generale della rete in questione e delle sue caratteristiche sia attraverso la sua visualizzazione che attraverso delle prime “metriche”. Per questa parte del progetto viene preso in esame solamente il l’insieme più grande di nodi e archi connessi tra loro, in quanto il grafo iniziale ri-sulta essere sconnesso, data la presenza di più dimensioni spaziali all’interno della serie tv, con l’impossibilità di calcolare le metriche generali relative alla rete. 
La rete iniziale risulta quindi essere quella riportata nella figura sotto:

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/Immagine4.png">
</p>

Come possiamo vedere, la rete risulta essere estremamente frammentata e presenta 262 nodi e 520 archi. Si è quindi deciso di incentrare l’analisi relativa a questa sezione dell’analisi considerando solamente il grafo centrale. La rete che quindi vogliamo analizzare è riportata nella figura sotto:

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/Immagine5.png">
</p>

## Metriche generali
Il primo passo è stato quello di esplorare alcune proprietà tipiche della struttura di una rete, per farsi un’idea in generale della social network in esame. A tal proposito abbiamo considerato:

 - **Numero di nodi**
   
 - **Numero di archi**
  - **Densità:** è un attributo i cui possibili valori sono compresi tra 0 e 1; ci consente di misurare la probabilità che una qualsiasi
   coppia di nodi sia adiacente. Si tratta, dunque, di un indice che
   misura mediamente quanto sono legati, tra loro, i nodi del grafo.
 -  **Raggio:** corrisponde alla minima eccentricità dei nodi, dove l’eccentricità è definita come la lunghezza massima dello _shortest
   path_ tra un nodo e i restanti nodi della rete.
 -  **Diametro:** corrisponde all’eccentricità massima tra i nodi
 -  **Periferia:** rappresenta l’insieme di nodi tali per cui l’eccentricità è pari al diametro
 -  **Average Clustering coefficient:** il _Clustering Coefficient_ di un nodo fornisce una misura di quanti i suoi vicini tendano a formare
   una _clique_. Facendo una media riferita all’intero grafo, si ottiene
   una proporzione di quanti i nodi tendono ad essere connessi tra loro.
-   **Connessione:** attributo booleano che restituirà “True” se il grafo è connesso, “False” se presenta dei nodi isolati.

I dati risultanti confermano la teoria di “Six Degrees of Separation”, la quale afferma che ogni persona può essere collegata a qualunque altra persona attraverso una catena di conoscenze e relazioni con non più di 5 intermediari. Per il calcolo delle proprietà sono stati utilizzati opportuni metodi della libreria NetworkX.

-	NODI: 138 
-	ARCHI: 420 
-	DENSITA: 0.0444 
-	RAGGIO: 5 
-	DIAMETRO: 9 
-	PERIFERIA: ['Hologram Rick (Edge of Tomorty: Rick Die Repeat)', 'Jessica (Cronenberged Dimension)'] 
-	CLUSTERING: 0.377 
-	IS CONNECTED: True

Si nota una densità decisamente bassa, il che può lasciare presagire una disparità nella distribuzione dei gradi tra i vari nodi. Oltre a ciò, il basso rapporto tra il numero di archi del grafo e il numero di archi del medesimo grafo completo (n(n-1)/2=9453) lascia intuire il perché di una densità così esigua.
Proseguendo, nella lista relativa alla Periferia sono presenti effettivamente personaggi minori, come ad esempio l’ologramma di Rick e Jessica proveniente dalla dimensione Cronenberged.
Infine, l’Average Clustering Coefficient pari a 0.377 indica che, mediamente, circa il 40% delle figure che sono in relazione con un certo personaggio sono anche in relazione tra loro.

## 2.2	Visualizzazioni e layout
In conclusione dell’analisi descrittiva si è provveduto a rappresentare graficamente la rete, attraverso le di-verse possibilità di layout messe a disposizione dalla libreria NetworkX.
Inizialmente, il grafo è stato riorganizzato secondo lo Spring Layout, utilizzando poi la libreria matplotlib per la sua visualizzazione. Il risultato ottenuto viene riportato nella figura sotto:

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/Immagine6.png">
</p>

Come possiamo notare, il grafo risulta essere sparso ma, nell’insieme, una buona parte dei nodi è incentrata nella regione centrale della rete. Sono presenti un certo numero di nodi distanti dalla zona centrale della rete, a ragion del fatto che ogni episodio della serie presenta un certo numero di personaggi differenti o che co-munque sono presenti in un numero di scene minori rispetto ai personaggi principali.

La seconda visualizzazione adottata per il grafo si basa sul cosiddetto Spiral Layout, mostrato in nella figura sotto:

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/Immagine7.png">
</p>

Tale disposizione, dal punto di vista della significatività, viene sicuramente a perdere valore ma è interessante sot-to l’aspetto prettamente grafico.

Infine, è stato utilizzato il Kamada Kaway Layout, il quale dispone i nodi secondo l’omonima funzione-costo che calcola la lunghezza dei percorsi. Tale disposizione, riportata in nella figura sotto è del tutto sommato simile allo Spring Layout.

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/Immagine8.png">
</p>

Per leggere la documentazione delle analisi:
- [Capitolo 1: Introduzione](networkxProject/README.md)
- [Capitolo 3: Analisi delle Strutture](Doc%20Analisi%20Centralità/README.md)
- [Capitolo 4: Analisi delle Strutture](Doc%20Analisi%20Strutture/README.md)
- [Capitolo 5: Group Centrality](Doc%20Group%20Centrality/README.md)
