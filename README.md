# Social Network Analysis della serie Rick And Morty
<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/logo.png">
</p>

## 1	Introduzione
Il seguente progetto ha come scopo l’analisi una rete sociale basata sui personaggi di una nota serie tv, con l’obiettivo di trarre conoscenza da un insieme di dati che a primo impatto non è di facile lettura, come è ap-punto una rete.

### 1.1	Rick And Morty Social Network
Il dataset su cui effettueremo la SNA contiene la rete di relazioni tra i personaggi della famosa serie “Rick And Morty”.
Rick And Morty è una serie animata statunitense creata da Justin Roiland e Dan Harmon, di genere cosmic horror. La serie è composta da 6 stagioni (in Italia la 6° è in uscita in questo periodo), nelle quali si raccontano le avventure dello “scienziato” Rick e di suo nipote Morty.
Un dataset basato su questo mondo risulta interessante per l’analisi SNA, in quanto nella storia compaiono numerosi personaggi, provenienti da diverse dimensioni e di diverse specie che nei vari episodi sono portati a combattere insieme o a scontrarsi.
Nella tabella sotto è riportato una parte del dataset, così da mostrare la sua struttura:

<div align="center">  
<table>
<tr>
<td><center><b>src</b></center></td><td><center><b>dest</b></center></td>
</tr>
<tr>
<td><center>Rick Sanchez</center></td><td><center>Beth Sanchez </center></td>
</tr>
<tr>
<td><center>Rick Sanchez</center></td><td><center>Diane Sanchez </center></td>
</tr>
<tr>
<td><center>...</center></td><td><center>...</center></td>
</tr>
<tr>
<td><center>Jessica (Cronenberged Dimension)</center></td><td><center>Jessica's Grandma</center></td>
</tr>
</table>
</div>

dove src indica il nodo di partenza e dest il nodo di arrivo. Quindi ogni riga del dataset rappresenta un arco del grafo, ovvero una relazione che coinvolge due personaggi, i cui nomi appaiono negli attribuiti src e dest.

### 1.2.1	Creazione del dataset
Il dataset di cui si è parlato sopra non è stato scaricato da internet, in quanto non era presente un dataset con i dati che erano per noi di interesse; perciò, abbiamo deciso di “costruirlo” nella maniera che riportiamo di se-guito.
I dati sono stati raccolti dal sito: Rick And Morty Wiki, contenente svariate pagine relative ai vari personaggi della serie e contenenti informazioni su di essi, inoltre abbiamo appreso che tale sito consentiva la navigazio-ne mediante un crawler (per fare ciò basta aggiungere a qualunque URL “robots.txt/”).
Il primo step è stato quello di creare un dizionario contenente il titolo della pagina e il link ad essa.

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/Immagine1.png">
</p>

Ci siamo serviti della libreria Beautiful Soup che permette l’estrazione di dati da file HTML e XML e mediante un ciclo for, per ogni elemento del dizionario sopra illustrato abbiamo preso solamente le parti contenenti le relazioni e la famiglia e lo abbiamo trascritto in un file csv.

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/Immagine2.png">
</p>

Il dataset che ne è risultato è quello che abbiamo esplicato nel paragrafo precedente.

## 1.3 1.3	Strumenti utilizzati
### 1.3.1	Beautiful Soup
Abbiamo utilizzato la libreria Beautiful Soup, per poter estrarre i dati di interesse dalle pagine web dei vari personaggi.
A seguito dell’import di tale libreria, si hanno a disposizione classi e metodi per gestire lo scraping di dati da file di tipo HTML e XML, quindi permette di ricercare ed estrarre tag o il testo in essi presente, di effettuare il filtraggio in base al tipo di tag e così via… 
### 1.3.2	NetworkX
Per poter realizzare il progetto utilizzando l’ambiente Python, si è deciso di utilizzare la libreria NetworkX, lo strumento ideale per la social network analysis.
Questa libreria mette a disposizione classi e metodi per gestire e manipolare grafi di diverso tipo, tra cui grafi diretti, indiretti, multigrafi e tanti altri. Tramite questa libreria è possibile anche convertire grafi tra vari for-mati, visualizzandoli in 2D o 3D, inoltre, possiamo esplorare proprietà dei grafi, quali grado, raggio, diametro e tante altre. Infine, possiamo calcolare sottografi e altre strutture particolari.
NetworkX ha una notevole flessibilità di rappresentazione, infatti permette di associare a nodi ed archi qual-siasi tipo di dato, come ad esempio testo, immagini, numeri, record XML e tanti altri.
In conclusione, si tratta di un framework efficiente, ampiamente scalabile, portabile e molto aggiornato. Ver-rà utilizzato per effettuare le varie operazioni di analisi e visualizzazione sul grafo d’interesse.
### 1.3.3	Gravis
Abbiamo utilizzato il package Gravis, per poter rappresentare il grafo risultante dalla nostra analisi in maniera dinamica per una più chiara comprensione di quest’ultimo.
Il nome di tale package sta per graph visualization e il suo scopo è quello di creare grafi (e reti) interattivi sia in 2D che in 3D.
Usa Python per preparare i dati dei grafici e tecnologie web (HTML/CSS/JS) per effettuare il rendering.
Abbiamo scelto questo package, in primo luogo, perché compatibile con NetworkX ed anche perché a diffe-renza di altri package disponibili rende possibile incorporare i grafici risultanti in un Jupyter notebook oltre che come file HTML.

<p align="center">
  <img src="https://github.com/Simone-Scalella/networkxProject/blob/main/img_readme/Immagine3.png">
</p>

Per leggere la documentazione delle analisi:
- [Capitolo 2: Analisi Descrittiva](Doc%20Analisi%20Descrittiva/README.md)
- [Capitolo 3: Analisi Descrittiva](Doc%20Analisi%20Centralità/README.md)
- [Capitolo 4: Analisi delle Strutture](Doc%20Analisi%20Strutture/README.md)
- [Capitolo 5: Group Centrality](Doc%20Group%20Centrality/README.md)

Ulteriori dettagli relativi alle analisi effettuate sono riportati nella seguente [relazione](https://github.com/ChiaraAmalia/networkxProject/blob/main/Relazione_NetworkX.pdf)
