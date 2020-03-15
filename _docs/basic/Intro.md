---
layout: wiki
next_doc: docs/basic/Informazioni su git.html
title: Guida alternativa a git
breadcrumb:
  - /guides/basic
---

# Guida alternativa a Git

Spesso utiliziamo uno strumento senza conoscerlo fino in fondo. Continuiamo tutti i giorni ad utilizzare quelle poche funzionalita che lo strumento ci offre e per questo incominciamo a pensare che quello strumento abbia soltanto quella funzionalita'.

Ho notato che questa e' la triste storia di Git, uno strumento che vine imposto come metodo di condivisione codice sorgente il quale il suo unico compito e' quello di caricare il proprio codice su un server. 
Nonostante sia un compito semplice, capita spesso di essere bloccato con messaggi di errore tipo "attenzione, il tuo branch non e' allineato con quello del server" creando una frustrazione continua dello sviluppatore di turno.

Ovviamente per superare questi problemi basta documentarsi. Il [sito ufficiale di git](https://git-scm.com/) mette a disposizione una documentazione scritta benissimo che contine tutto quello che c'e' da sapere su questo programma.
E' presente un libro completamente [online](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control), un [libro](https://www.amazon.it/Pro-Git-English-Scott-Chacon-ebook/dp/B01ISNIKES/ref=tmm_kin_swatch_0?_encoding=UTF8&qid=&sr=) gratuito su amazon e una documentazione tecnica dei [singoli comandi](https://git-scm.com/docs).

Allora perche' leggere _La guida alternativa a Git_?

Ovviamente se hai intenzione di leggere tutto il libro non ti servira' proseguire oltre questa frase.

L'obbiettivo della guida non e' quello di insegnare git ad una persona che non lo conosce ma di far capire ad una persona che l'ha gia utilizzato che forse e' qualcosa di diverso rispetto a come l'ha inteso.

Incominciamo con fare un elenco degli argomenti toccati in questa guida.

* Intruduzione a Git  
  Introduzione alternativa di Git, far capire che e' uno strumento potente che puo' affiancare il programmatore nello sviluppo della applicazione, alla pari del proprio editor di testo e non e' uno strumento secondario.
* Un semplice metodo di versioning senza software per il versioning  
  Per aiutarci a capire la varsatilita di git immaginiamo di occuparci manualmente del versioning di un progetto. Creaiamo un archivio di backup, ripristiniamolo, creiamo semplici script per in mente un sistema con cui fare delle associazioni alle funzionalita di Git.
* __Dimentichiamoci__ delle repository __remote__ e dei __branch__  
  Questo puo' sembrare assurdo per molte persone. Se non conosci git e svn e se non sai di cosa si sta parlando con __remote__ o __branch__ allora __MEGLIO COSI__. Questi elementi portano a creare dei preconcetti che ci limitano nell'apprendere cio' che realmente e' importante quando si utilizza git.
* Commitiamo  
  Tutto il necessario per salvare le modifiche.
* Fare e disfare  
  Come sfruttare i commit e l'index per annullare o ripristinare le nostre modifiche.
* Imparare ad utilizzare l'index  
  Forse l'index di git e' lo strumento piu' sottovalutato di tutti. Quando si impara ad utilizzare git e si fanno i primi commit viene da chiedersi perche' devo aggiungere i file all'index? Committiamo direttamente e basta? Spammiamo git add --all ad ogni modifica? Ovviamente l'index e' di grande utilita' e dobbiamo essere in grado di sapere quando dobbiamo aggiungere dei file all'index durante la nostra modifica.
* __PANIC MOMENT__  
  Cosa fare quando si commettono errori. Come recuperare le informazioni committate e cosa fare quando git si blocca. Anche se non abbiamo ancora introdotto i branch vedremo alcune anticipazioni. Questo per evitare che interrompendo la lettura di questa guida non sappiamo che con git si possono sempre recuperare i commit. __Con git non si perdono mai le informazioni committate__.
* Lavoriamo in parallelo con i __branch__  
  Sempre __offline__ vedremo a cosa servono i branch e come questi ci permettono di lavorare in parallelo sul nostro codice sorgente. Spesso capira di dover affrontare un problema al quale ancora non sappiamo bene come approcciarsi e forse cambieremo idea molto spesso e git ci permettera di lavorare contemporanemante a diverse soluzioni senza mai perdere il lavoro fatto.
* Ispezionare tutti i nostri commit _parte 1_  
  Sia che piaccia utilizzare tool grafici che utilizzare il terminale e' importante vedere gli strumenti messi a disposizione di git per controllare il motivo per cui e' stata aggiunta una determinata modifica.
* Debug con Git  
  A volte viene da chiedersi se il programma non funziona a causa dell'ultima modifica oppure per un problema all'ambiente di sviluppo. Come possiamo rendercene conto? Quali sono le modifiche che hanno introdutto un bug nel programma? Impariamo ad usare il __checkout__ per capire cosa sta succedendo.
* Ripulire tutte le modifiche con __stash__  
  Capita spesso che nel bel mezzo di una modifica ci viene richiesto di interrompere il lavoro che stiamo svolgendo per poter completare un semplice task. In quel momento abbiamo il codice inconsistente siccome e' in una fase delicata de nostra modifica e l'unico modo consiste nel rimuovere velocemente tutte le modifiche ma essere in grado di poterle recuperare attrettanto velocemente. Questo e' possibile con git stash.
* Utilizzare Git su un progetto SVN  
  __SVN__ e' molto utilizzato e' puo succedere che siamo costretti a lavorare su un progetto che utilizza SVN al posto di Git. Possiamo utilizzare qualche trucchetto per poter utilizzare quasi tutte le funzionalita di Git e allo stesso tempo continuare a lavorare su un server SVN. Questo permette di mostrare di mostrare ad altri membri del progetto le funzionalita di Git.
