# Social Network Analysis della serie Rick And Morty
<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/logo.png">
</p>

## 5 Group Centrality
In questo capitolo vengono analizzati i varie gruppi nell'universo di Rick & Morty, per vedere quale sono piu' significative.
Le metriche utizzate sono analoghe per analisi dei nodi singoli, con gruppi di nodi invece di un singolo nodo. I Tale funzione offerti dalla libreria di NetworkX sono:
  1. group_degree_centrality: viene definita come il rapporto della somma tra il numero dei nodi esterni al gruppo ma connessi ad uno dei membri del gruppo e il numero dei nodi non connessi al gruppo.
  2. group_closeness_centrality: viene calcolato sui nodi esterni dal gruppo, e definita come il rapporto tra la somma del numero di nodi e la somma delle distanze dei nodi dal gruppo.
  3. group_betweenness_centrality: viene calcolata come il rapporto tra il numero
  dei percorsi minimi tra le coppie di nodi del grafo che passano per almeno uno dei nodi
  del gruppo e il totale di shortest path di tutte le possibili coppie del grafo

### 5.1 Albero genealogico
<p align="center">
  <img height=300 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap5_1.jpg">
</p>

Nella figura viene mostrata albero genealogico dei caratteri principali, da notare che i caratteri possono essere duplicati in questo albero per la causa di multiverso.

## Per simone
Gli immagini sono nel notebook di "networkLeo.ipynb"
I label sono da aggiornare
Le suddivisione in tre gruppi sono del seguente modo:

<p align="center">
  <img height=300 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/toSimo.jpg">
</p>
Dove i tre label sono sinistro centro e destro come nell'immagine.


### 5.1 Group Degree Centrality

<p align="center">
  <img height=300 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap5_2.jpg">
</p>

### 5.2 Group Closness Centrality

<p align="center">
  <img height=300 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap5_3.jpg">
</p>

### 5.3 Group Betweenness Centrality
<p align="center">
  <img height=300 src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/cap5_4.jpg">
</p>





