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
