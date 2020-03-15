---
layout: wiki
# next_doc: /docs/basic/What is Jekyll.html
title: Un semplice metodo di versioning senza software per il versioning
breadcrumb:
  - /guides/basic
---

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