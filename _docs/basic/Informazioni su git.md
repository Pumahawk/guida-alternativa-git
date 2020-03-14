---
layout: wiki
# next_doc: /docs/basic/What is Jekyll.html
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

## Un semplice metodo di versioning senza software per il versioning

Cerchiamo di dimenticare quello che gia' sappiamo di git. Meglio eliminare fin da subito i preconcetti che abbiamo. Immaginiamo come comportarci nel caso in cui vogliamo tenere traccia dello stato del nostro codice sorgente ma senza avere un software specifico.

Prima di iniziare devo citare dei programmi alternativi che andremo ad usare. Sono programmi molto semplici, permettono di creare file di archivio come zip, rar, tar. In questo momento scegliamo di creare archivi di tipo __tar__.

* __Tar__ programma per creare archivi contenente file e cartelle.

__Iniziamo un progetto__, creiamo una cartella e al suo interno mettiamo tutto cio di cui abbiamo bisogno. Iniziamo a scrivere le prime righe di codice e dopo un paio di ore siamo soddisfatti del nosto lavoro. In questo momento vogliamo fare un backup del nostro lavoro in modo da poterlo rispristinare  nel caso qualcosa dovesse andare storto.

* Creiamo una cartella chiamata backup-codice in punto sicuro del nostro computer dove andremo ad inserire i nostri backup del progetto.
* Andiamo nella cartella principale del nostro progetto.
* Creiamo un file archivio nella cartella di backup.

```bash
tar -cf /cartella/di/backup-codice/backup-1.tar .
```

E il gioco e' fatto. Abbiamo creato un punto di ripristino del nostro codice sorgente.

Immaginiamo di tornare a lavorare al nostro codice sorgente e di combinare qualche pasticcio. Ci rendiamo conto che le modifiche che stiamo facendo non ci stanno portando da nessuna parte e vogliamo ripristinare il nostro lavoro allo stato dell'ultimo backup.

E' una operazione molto semplice.

* Entriamo nella cartella del nostro progetto
* Cancelliamo tutti i file all'interno
* Estraiamo i file dall'archivio con il seguente comando

```bash
tar -xf /cartella/di/backup-codice/backup-1.tar
```

In questo momento abbiamo recuperato tutto il nostro codice sorgente e abbiamo scartato tutte le modifiche.

Possiamo migliorare questa procedura creando uno script con un nome semplice in grado di creare l'archivio e di ripristinare le modifiche. Immaginiamo di creare il comando __commit__ e __reset__.

* __commit__ [nome-archivio] crea l'archivio nome-archivio.tar nella vostra cartella di backup
* __reset__ [nome-archivio] ripristina il codice sorgente recuperando il codice dall'archivio nome-archivio.tar 

Ora abbiamo 2 comandi in crado di tenere traccia delle modifiche e fare un ripristino velocemente.

Attenzione!! Non iniziamo a pensare che git si comporta in questo modo per la creazione dei punti di pripristino. L'esempio serve per avere delle similitudini con dei concetti spiegati successivamente.
{:.alert .alert-warning}