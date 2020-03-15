---
layout: wiki
next_doc: /docs/basic/Versioning manuale.html
title: Cos'e Git? Il primo approccio
breadcrumb:
  - /guides/basic
---

> Git e' software di __controllo versione distribuito__ per tracciare le modifiche del codice sorgente durante il suo sviluppoo del software.

Questa definizione di Git recuperabile dalla pagina di Wikipedia permette di capire di cosa stiamo parlando. Ovviamente tutti conosciamo questa definizione e chi programma da tempo non puo' immaginare di lavorare senza un software simile.

Se invece non sai cos'e' un software per il controllo versione allora vediamo di spiegarlo velocemente. E' un software che registra le modifiche al codice per permetterti di recuperare in un secondo momento lo stato del codice in un certo momento.
Ad esempio se abbiamo bisogno di recuperare un frammento di codice che qualche giorno fa abbiamo cancellato pensando fosse inutile, possiamo guardare la cronologia delle modifiche di quel file e recuperare il contenuto di cui abbiamo bisogno.

Ovviamente questa definizione e' possibile recuperarla su Wikipedia e sfogliando le prime pagine della documentazione ufficiale capisci subito le prime funzionalita' per tenere traccia delle modifiche.

Facciamo un breve elenco prima di iniziare la guida __alternativa__ (soprattuto dobbiamo ancora chiarire perche' questa guida e' alternativa).

* commit - salvare lo stato del nostro codice
* reset - ripristinare lo stato del nostro codice
* log - vedere la storia delle nostre modifiche

Sono centinaia i comandi di Git che possono tornare utili. E' inutile elencarli tutti in questo momento. Non si riuscirebbe a capire realmente la loro utilita'.

## Condivisione del codice sorgente

Una funzionalit' di Git che voglio che dimentichiate per il momento e' la possibilita' di condividere le proprie modfiche con altri sviluppatori.

Ma se voglio che voi la dimentichiate perche io ne sto parlando? Questo perche e' la funzionalita piu utilizzata da tutti i programmatori e quindi non posso fare finta che non esista. Se un programmatore inizia a lavorare su un progetto configurato con Git allora sara la prima cosa che gli verra spiegata.

Come ho spiegato precedentemente, git permette di vedere lo storico delle proprie modifiche, inoltre permette di caricare le proprie modifiche su un server in modo che tutti i programamtori possano sincronizzarsi. Questa funzionalita e' alla base del lavoro in team e nonostante sia soltanto una funzionalita, con il tempo e' diventato l'unico motivo per cui si utilizza questo strumento.

Cerchiamo di introdurre un po' di tecnicismi giusto per avere una idea di cosa si sta parlano. Ovviamente questi argomenti saranno ripresi quando si affrontera l'argomento della __condivisione del codice sorgente__

* __Repository__ - Termine utilizzato per indicare il server utilizzato per sincronizzare le modifiche
* __push__ - Comando di Git usato per inviare al server le modifiche
* __pull__ - Comando di Git usato per recuperare le modifiche dal server

Se sei espero di Git, sicuramente avrai storto il naso nel leggere che con __repository__ si intende un server e che __pull__ recupera le modfiche. Purtroppo non e' ancora arrivato il momento di spiegare che cosa succede usando __pull__ e cosa sono le __repository__.
{:.alert .alert-info}

## Usare git come strumento di sviluppo

Ora che sappiamo a grandi linea di cosa si tratta Git cerchiamo di approfondire di piu' l'argomento.

Ancora oggi, dopo anni dalla prima versione, gli sviluppatori lo utilizzando per condivide il proprio codice sorgente con altri sviluppatori.

Mediamente, l'utilizzo tipo di git per un programmatore consiste nell'accendere il proprio PC a inizio giornata, sincronizzarsi con le